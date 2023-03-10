# 运营开销——或者为什么傲慢是不好的。

> 原文：<https://devops.com/operational-overhead-or-why-hubris-is-bad/>

如果你听说过这个，请打断我:一个人走进一个会议，说“我们需要一个能做点什么的系统”，房间里的工程师回答说“哦，我们完全可以建造那个”。这个笑话的大部分笑点是“我们完全可以构建它，现在我们必须拥有它的生命周期，我们已经为一些我们本不应该构建的东西牺牲了宝贵的时间和资源。”八股经

我为自己在这些对话中扮演的角色感到内疚，我相信你们很多人也是如此。大约两年前，当我们刚刚起步的创业公司真正开始腾飞时，我参加了其中的一次会议。一些开发者想尝试一个推荐引擎，并打算使用 Mongo 作为它的一部分。坦率地说，我认为他们想和 Mongo 鬼混，需要一个借口，就像我认为他们真的要做一些事情一样。当时我正忙得不可开交——管理我们的云系统、局域网、设施、采购，我的任务是让我们的视频后期制作过程的技术方面变得更加健全。是的。不是。有。时间。因为。a .蒙哥。设置。

听着，事情是这样的。在那次对话中，大多数时候，系统管理员试图成为一个好的 devops 合作伙伴，回答“哦，我当然可以站起来 mongo”。但是说实话，不仅仅是站着 Mongo。它处理升级、安全性、故障切换/高可用性、备份和恢复。如果这个推荐引擎真的有效，它将很快成为我们基础设施的关键部分。我有足够的头脑知道，虽然我可能会找到一个小时站起来 mongo，但我没有其他几个小时来做好它。说真的，我没有一个小时。所以我打趣地说了一句现在很有名也经常被用来吓唬我的话:“听着，伙计们，我们需要减少运营开销。让我们找一个外包公司。”

十分钟后，刷了一张信用卡，我们就可以使用 [MongoLab](https://mongolab.com/welcome/ "MongoLab") 了。两年后？推荐引擎很牛逼，我对 mongo 一点都不在乎。没有升级。没有半夜的页面。没有架构讨论。它只是工作。我想花点时间来讨论一下标准异议:

*   好的，我们可以尝试外包，如果可行的话，我们会把它带进来。对吗？因为您永远不会让基础架构的关键部分脱离您的控制。对吗？因为，如果你做了…那么…那就不好了。对！在这一点上，旧世界的 IT 智慧是非常清楚的，只有当你在内部运行它时，你才能确信它是好的。然而，以我的经验来看，你可能*比那些唯一的工作就是做这些事情的团队更容易搞砸备份、升级失败或故障转移。*

*   **但是！好贵啊！**对吧？几乎所有的*aaS 提供商都有一个入门级的定价结构，让你可以以低于周五团队午餐的价格购买。如果你在生产，你在赚钱，或者更好的是*因为这个基础设施选择赚了更多的钱……证明成本是愚蠢的简单。只要服务的成本低于你的收入，干得好。如果你不是真的在赚钱，那么你到底在做什么？*

*   **我们不能信任服务提供商 X** 。伙计们，这些公司是来给你们提供一样东西的。他们实际上只有一份工作。你可能有 14 份工作。你是在要求第 15 次吗？第 15 件你必须观察、关心、喂养、爱和恨的事？对你的实际业务来说不是*核心的东西*？难道你不应该让第 15 份工作对你的团队/代码/组织直接有益吗？你不就是为此而来的吗？

*   **天啊没有不被小贩锁定的。嘿，天才，你知道吗？您必须编写代码，无论您是在自己的环境中编写与数据库对话的代码，还是在别人的环境中编写与排队系统对话的代码，都只是代码。我希望用余生的大部分时间来写这个论点是多么的愚蠢。是啊！如果你解雇一个供应商，你必须重构。你猜怎么着如果你升级你自己的东西，你可能需要重构。如果你改变内部系统，你必须重构。任何有足够先见之明预见到所有可能结果的人，任何能够做出完美的、无重构决策的人，都可以和我讨论供应商锁定问题。你们其余的人应该克服这种异议，回到有成效的事情上去。**

你知道我最喜欢的运营开销故事是什么吗？[亚马逊 SQS](https://aws.amazon.com/sqs/ "SQS") (简单排队服务)。不同的日子，不同的开发商，相同的想法。哇，我们的小网站现在正在处理足够多的订单，我们需要异步履行…我知道！让我们建立一个排队系统！我用过一次 ActiveMQ！或者 RabbitMQ！或者……我们可以使用这个星球上最大的电子商务网站的排队系统。那里有一群训练有素的猴子 24x7x365 全天候观察着每一件微小的事情。其他人已经想到了规模/弹性/安全性的每一种可能的组合。你知道吗？每个请求花费 0.0000005 英镑。我可以以 7 美元的净成本处理 1400 万份订单。是啊，让我们完全花时间站起来更好更便宜的东西。

好的工程师是好的，因为他们知道他们可以建造东西。即使他们不知道他们能做到，他们也非常确定他们能解决这个问题。DevOps 应该是关于做出明智的决定，傲慢是不明智的。使用手边最好的工具。重建每一个轮子、管理每一个平台、自己做每一件事……只会增加您的运营开销，降低您影响业务的能力。