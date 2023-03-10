# 使用 ElasticBox 部署 MongoDB 集群

> 原文：<https://devops.com/mongodb-cluster-elasticbox/>

我们的创始人在过去是。微软的. NET 框架团队。所以他们的第一个 ElasticBox 版本是用 C#写的也就不足为奇了。NET 框架和 SQL Server。

快进到 2012 年。随着 ElasticBox 愿景的具体化，我们需要一个健壮的、可扩展的架构来匹配我们的愿景。所以我们重新评估了所有现有的技术。

此外，我们决定从关系数据库模型转向基于文档的方法。主要原因是因为我们希望存储分层数据，并能够对其进行版本控制。

今天，为了满足我们的数据需求，ElasticBox 依赖于 MongoDB 集群，我们在三个独立的提供商上运行这些集群——两个公共的，一个私有的。多亏了 ElasticBox，我们现在可以在几分钟内部署我们的 MongoDB 集群。

**基础知识**

什么是 MongoDB？ [MongoDB](https://www.mongodb.org) 是一个开源文档存储数据库。

为什么要集群 MongoDB？为生产部署提供冗余和高可用性。

**我们如何使用 MongoDB**

在我们的例子中，MongoDB 使用的是副本集模型。副本集是一组托管相同数据集的 MongoDB 实例。一个 MongoDB(主节点)接收所有写操作。所有其他实例(辅助节点)都从主节点应用操作，因此它们具有相同的数据集。

**主服务器**接受来自客户端的所有写操作。副本集只能有一个主要副本集。因为只有一个成员可以接受写操作，副本集提供了**严格的一致性。**

[![Screenshot 2014-06-18 16.47.20](img/cfa9598b68277bd28f37e9e18bf18099.png)](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-18-16.47.20.png)

**通过 ElasticBox 部署 MongoDB】**

ElasticBox 提供了一个默认的 MongoDB box，可供公众使用。它部署了 MongoDB 服务器的一个独立实例。我们的 MongoDB 生产机器非常类似于默认机器，只是我们的生产场景需要一些配置设置。

虽然默认的 MongoDB box 配置适合于开发目的，但需要进一步配置才能在生产中使用。要将 MongoDB 默认框配置为生产使用，请遵循以下步骤:

**第一步。**创建一个名为 MongoDB 副本的新盒子。为 **MongoDB 服务器**添加一个 box 变量(这是使用默认的 box 设置)。 [![Screenshot 2014-06-18 16.11.18](img/b6c245eab45b8cb7ba6fd45f2c7dada0.png)](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-18-16.11.18.png)

[![Screenshot 2014-06-18 16.12.08](img/3718232f72ce2d869992372193cd2aa5.png)](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-18-16.12.08.png)

**第二步。**添加一个文本变量**副本集**来保存副本集名称。该值必须在集群的所有成员之间共享。

[![Screenshot 2014-06-18 16.12.42](img/09976a46aa80fe7e3164ddddb0ddb199.png)](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-18-16.12.42.png)

**第三步。**展开 MongoDB 服务器框。编辑其文件变量 **COMMON_YAML** 并粘贴以下内容:

[![Screenshot 2014-06-18 15.35.45](img/1fdff89dc77a4d5fd174cba6b9ee75a6.png)](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-18-15.35.45.png)

mongodb::副本集:{{副本集}}

MongoDB::key _ file:/etc/mongod . key

[![Screenshot 2014-06-18 16.15.36](img/fe72cf06f9e1b95a20b0f2975583415d.png)](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-18-16.15.36.png)

hiera 将使用该文件自动向 puppet 传递参数，而无需修改现有的 puppet default.pp 文件。

**第四步。**添加一个名为 primary 的绑定，类型为 **MongoDB 副本**(您刚刚创建的盒子)。

[![Screenshot 2014-06-18 16.14.05](img/9b7a69a760613d9e02bbaf4ad92974a8.png)](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-18-16.14.05.png)

**第五步。**添加安装脚本。在这里获取剧本[。](https://gist.github.com/adamdaigian/5677fa177a38a4b0e48d)

![Screenshot 2014-06-18 16.16.10](img/961bc46d2ca5840a26f3fdb1db451c02.png) [](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-18-16.16.43.png)

[![Screenshot 2014-06-18 22.34.28](img/b94cba235452b0179b2dad0ca23b5143.png)](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-18-22.34.28.png)

**第六步。**添加一个启动脚本。在这里获取剧本[。](https://gist.github.com/adamdaigian/ed6b83ab14d6444deead)

[![Screenshot 2014-06-20 11.40.08](img/b0f57507fc63ca540db2e52e5b06de71.png) ](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-20-11.40.08.png) [ ![Screenshot 2014-06-20 11.40.35](img/a889bc39b868d6afdda662c1fd88871b.png)](http://elasticbox.com/blog/wp-content/uploads/2014/06/Screenshot-2014-06-20-11.40.35.png)

当您在没有绑定的情况下部署机器时，它会为您创建一个具有初始配置的集群。另一方面，如果绑定到一个现有的实例，它会将该实例添加到现有的集群中！

现在，只需几个简单的步骤，您就拥有了 MongoDB 集群！