# PyMongo 指针:如何生成健壮且高度可用的 Mongo 查询

> 原文：<https://devops.com/pymongo-pointers-make-robust-highly-available-mongo-queries/>

在今天由商用服务器组成的集群中，故障是家常便饭。当您查询时，由于一个数据节点发生故障而导致代码失败，这令人沮丧，也不好玩。根据我强化我们产品的经验，我想分享一些快速简单的指针，可以帮助您的 MongoDB 查询对节点故障更加健壮。让我们开始吧。

## **初学者背景**

*注意:如果你对 MongoDB 完全陌生，我会推荐你阅读下面的链接。它们应该让您对构成 MongoDB 集群的组件有一个较高层次的理解。*

*   [MongoDB 特性介绍](https://docs.mongodb.com/manual/introduction/)
*   【MongoDB 如何维护冗余和数据可用性(也称为副本集)
*   【MongoDB 如何水平扩展(又名分片)

我们先从了解 PyMongo 及其优势开始。正如你已经知道的， [Python](https://www.python.org/) 是一种高级编程语言，用面向对象编程提供代码可读性。与用其他语言编写的代码相比，它的语法和代码更容易阅读，而且代码更小。而 [MongoDB](https://www.mongodb.com/) 是一个面向文档的可伸缩数据库，设计用于处理大数据应用(比如内容管理系统)。由于 MongoDB 支持动态模式，它还提供了将任何类型的数据存储到数据库中的灵活性，而没有任何刚性。

因此，如果您以前从未使用过 [PyMongo](https://api.mongodb.com/python/current/) ，PyMongo 发行版包含使用 Python 与 MongoDB 数据库交互的工具。它是使用 Python 的实用程序处理 MongoDB 的最有效的工具。PyMongo 的创建融合了 Python 作为编程语言和 MongoDB 作为数据库的优势。由于 Python 提供了一种易于实现的编程方式，而 MongoDB 可以处理大型文档存储库，因此 PyMongo 工具非常有用，因为它提供了这两种技术中的最佳技术。

PyMongo 的核心是 [MongoClient 对象](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html)，用于连接和查询 MongoDB 数据库集群。它可以用来连接独立的 mongod 实例、副本集或 mongos 实例。要指定要联系的 mongo 端点，只需将端点传递给对象的*主机*参数。例如，如果我们在 10.0.0.3 上有一个独立的 mongod 节点监听端口 27017，您可以按如下方式联系该节点:

```
import pymongo
```

```
client = pymongo.MongoClient(host=“10.0.0.3:27017”)
```

传入主机的节点称为*种子*节点。一旦您初始化了 MongoClient，它将在后台连接到指定的种子节点。有了一些基础知识，让我们来谈谈如何让您的查询更健壮！

## **提示 1:增加你的主机种子列表**

第一个技巧非常简单，但是非常有用。不是传入单个种子节点，而是传入一个种子节点列表。传入一个种子节点列表可以让 MongoClient 对象联系更多的端点，以防其中一个输入节点的连接中断。这不仅使初始化 mongo 连接更加健壮，而且使客户机对初始化后出现的连接失败也更加健壮。就代码而言，它看起来如下所示:

```
client = pymongo.MongoClient(host=“10.0.0.3:27017”) # Fragile; single point of failure 
```

```
client = pymongo.MongoClient(host=[”10.0.0.3:27017”, “10.0.0.3:27018”, “10.0.0.3:27019”]) # More robust; can contact two other nodes in case one goes down
```

请注意，种子列表中的所有节点必须属于同一个逻辑组。例如，种子列表必须包含属于相同副本集的 mongod 节点，或者连接到相同配置服务器的 mongos 查询路由器，或者相同分片集群中的配置服务器。混淆这些会导致不可预测的行为。

## **提示 2:如果第一次你没有成功，尝试，再试一次**

初始化到 mongo 节点的连接后，连接可能会随时失败。这可能是由多种因素造成的，从网络连接问题到实际的 mongo 节点故障。如果发生其中一个故障，下次发出查询时，MongoClient 将尝试联系不可用的节点，确定它不可达，然后抛出异常。之后，MongoClient 对象将自动尝试在后台连接到您提供的种子列表中的另一个活动节点，这意味着您的后续查询可能会成功。但是，您的代码仍然有一个异常需要处理。

处理这些情况的一个简单明了的方法是将所有查询包装在一个 retry decorator 中，该 decorator 将捕获异常，然后重试查询。以下是一些示例代码:

```
def retry(num_tries, exceptions):
```

```
    def decorator(func):
```

```
        def f_retry(*args, **kwargs):
```

```
            for i in xrange(num_tries):
```

```
                try:
```

```
                    return func(*args, **kwargs)
```

```
                except exceptions as e:
```

```
                    continue
```

```
        return f_retry
```

```
    return decorator
```

```
# Retry on AutoReconnect exception, maximum 3 times
```

```
retry_auto_reconnect = retry(3, (pymongo.errors.AutoReconnect,))
```

```
@retry_auto_reconnect
```

```
def get_count(client, db, collection):
```

```
    return client[db][collection].count()
```

通过将查询包装在重试修饰器中，可以使它们对节点故障和其他临时故障(如初选重选)更加健壮。当然，这种方法并不能保证您的查询在所有情况下都会成功，因为它假设集群中还有其他健康的节点可以故障转移到。但是，假设一个相对稳定的集群，这种方法可以处理大量的故障。

## **提示 3:捕捉正确的异常**

在上面的示例中，我们重试了 AutoReconnect 异常，当与数据库的连接丢失时会引发该异常。虽然这是一个需要捕捉的异常，但它绝不是完整的。其他异常可以在 pymongo 文档中找到(参见下面的链接)。您可能还想了解的几个问题包括:

*   **py mongo . errors . connection failure**:每当无法连接到数据库时抛出(实际上是上面 AutoReconnect 的超类)
*   **py mongo . errors . serverselectiontimeouterror**:每当发出的查询找不到服务请求的节点时抛出(例如，当不存在主节点时，在主节点上发出 read)

这两个例外在非共享和共享的 MongoDB 集群中都很有用。但是，在处理分片集群的节点故障时，会有一些额外的复杂性。在分片集群中，大多数查询应该通过 mongos 发送，因为它可以将查询路由到适当的分片。如果 mongos 实例失败，那么将引发一个连接失败。然而，如果您到 mongos 的连接是健康的，但是 mongos 无法连接到副本集，会发生什么呢？在这些情况下，mongos 将汇总所有错误并发回一个错误，该错误随后被作为 OperationFailure 引发。

虽然重试操作失败似乎很简单，但这并不完全，因为操作失败可能代表各种各样的错误，从可重试的错误(如初选重选)到不可重试的错误(如身份验证错误)。您可以通过检查错误的代码字段来区分不同类型的错误。虽然在某个时间点有一个错误代码及其含义的列表，但它们已经过时并被删除(参见 SERVER-24047)，这意味着您必须进行一些尝试和错误，以发现您应该重试哪些代码。

## **结论**

希望这些提示对所有 MongoDB 爱好者有所帮助！如果你有任何问题，意见，或者有你自己的建议要分享，请在下面随意评论，让讨论进行下去。

— [布莱恩·尹](https://devops.com/author/brian-yin/)