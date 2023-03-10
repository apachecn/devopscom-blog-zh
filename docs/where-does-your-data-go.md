# 你的数据去哪里了？

> 原文：<https://devops.com/where-does-your-data-go/>

近年来，[安全性和合规性](https://securityboulevard.com/?s=security+and+compliance)方面最有趣的发展之一是能够通过应用程序从输入到消费跟踪一段数据，并查看与之相关的每一位。对我来说，这之所以如此有趣，是因为它允许事后分析实际上确定在数据泄露中到底丢失了什么。“哦，那个图书馆被攻陷了？好的，让我们来看看这个库实际上接触了哪些输入…”考虑到传统上应用程序中的所有数据都是免费的，这真是太酷了。

出于各种原因，我不是一个超级合规粉丝，但这是强制合规的一个很好的结果。我认为，如果没有合规性要求的推动，我们就不会有这种级别的[数据跟踪](https://devops.com/?s=data+tracking)。

那么我们能用这些信息做什么呢？这是有趣的部分，我认为我们会看到随着时间的推移而发展。如果我们知道某个给定的数据在哪里被使用，我们就有了一个强大的开发信息。现在实施还为时尚早——这并不容易——但想想吧。我可以预见一个所有冗余数据访问都被消除的未来。如果我们从多个来源获得相同的数据集，并且这些数据集被提供给相同的内部消费者，那么我们可以对这些数据进行标准化。标准化格式的单一库，标准化查找的单一库，等等。

在大多数情况下，我们目前对输入进行验证和格式化。就像数据一进入系统就马上开始。对于一个系统来说，这是一个很好的想法，在这个系统中，我们不确定数据的去向，但可以确定一些攻击是通过这些输入来的。但是，如果我们发现要维护的代码比必要的多了 10，000 行，那会怎么样呢？如果数据跟踪允许我们通过集中这些功能来消除代码，会怎么样？我们将不得不强化进行验证和格式化的例行程序——因为它将得到脏数据——但不会比我们今天在任何地方所做的更多。

如果我们可以通过使用旨在提高安全性的工具来减少源代码，这难道不是最终的转变吗？处理进入系统的数据的源代码的数量也是惊人的。对于企业系统，我们开发的大部分实际上是数据处理，不管它有多复杂。数据存储是中央存储库，应用程序只需访问和修改它。所以数据的左移是巨大的。

考虑一下。我知道你们都忙于其他项目，但是更少的源代码减轻了每个人的负担；看看您已经拥有的产品中的数据跟踪功能(主要在漏洞管理和源代码扫描工具集中提供)，看看它是否符合您的需求。这可能会节省每个人的时间，也有助于满足一些以数据为中心的合规性要求。这让您有更多的时间来改进系统。