# DevOps:这都是开源的错

> 原文：<https://devops.com/devops-its-all-open-sources-fault/>

要怪就怪 DevOps 开源。毕竟，是开源运动给了开发者这样一个想法，即他们可以自由地编码，自由地为他们的公司构建应用程序和其他软件，而不需要事先获得批准。正是开源给开发者加冕了国王。开源不仅给了开发者编写代码的自由，也给了他们管理代码的自由。

是开源给了我们 DevOps。

**DevOps:完成工作的自由**

传统上，IT 运营是一项专门的任务，主要控制允许在企业内运行的代码。鉴于所有软件在运行前都必须购买，开发人员或其他人将流氓软件引入数据中心神圣大厅的风险很小。

企业能够强制执行策略，因为所有软件都必须从采购开始，到运营结束。根本没有其他可行的方法让软件进入企业。

也就是说，直到开源。

开源毁了采购和运营之间整齐划一的关系。突然间，软件不再需要购买了。它可以简单地下载。随着业务线加快创新步伐的压力越来越大，开发人员加快了步伐:“我有一个开源项目。”

运营部门进行了反击，试图阻止开源软件的采用。他们失败了。

开发人员完成工作的压力实在太大了。一旦 Amazon 在数据中心之外为开发人员提供了一个部署代码的地方，战斗就结束了，一种构建和管理代码的新模式诞生了。这项被称为 DevOps 的运动让开发者对他们的作品拥有端到端的控制权。

根据 Puppet Labs 2013 年的一项调查，自 2011 年以来，DevOps 的采用增加了 26%,导致 50%的应用程序故障，恢复速度提高了 12 倍。DevOps 的增长也转化为将代码交付速度提高 30 倍的能力。所有这些都体现在 CA Technologies 对高级 IT 决策者的一项单独调查中，该调查发现，客户体验的改善是企业采用 DevOps 的最大原因。

鉴于这些改进，我们不可能回到以运营为中心的 IT。

**祝福还是诅咒？**

所有这些并不是说 DevOps 是一个纯粹的祝福。根据我的经验，开发人员通常没有准备好或者不愿意承担在生产中管理应用程序的负担。开发人员接受了多年的培训，认为他们可以构建一个应用程序并将其转储到运营中进行管理，他们发现开发运维中的“运营”是真实的，有时真的是一种痛苦。

例如，一个大问题是生产环境和开发/测试环境通常非常不同。在小规模测试环境中完美运行的应用程序可能会错过一整类错误，这些错误只会在更复杂的生产环境中出现(例如，只有在应用程序更改与复杂的分区网络拓扑交互时才会出现的问题)。

事实是，对运营(安全、可靠和缓慢)或开发(快速、机会主义、迭代)的过度优化证明是次优的。需要一种平衡。

但是这种平衡越来越倾向于升级 Ops 来满足开发者的需求。事实上，开发人员正在编写大量的基础设施和工具来帮助其他开发人员更好地管理他们的作品。通常这种工具是基于 SaaS 的，并且很大一部分是开源的，允许开发人员在保持灵活性的同时继续绕开操作控制。像 Boundary、Puppet Labs、SumoLogic 等公司的出现使开发人员的操作变得更容易。

我自己的公司， [MongoDB](https://www.mongodb.com) ，为现代应用开发最流行的数据库。MongoDB 的开发变得如此简单，这一点受到了普遍的称赞，但是我们用于促进 MongoDB 大规模运行的工具却落后了。在过去的两年里，我们一直在为 MongoDB 构建[监控、备份和其他管理工具。仅仅忘记 DevOps 中的“Ops”是不够的。]( https://mms.mongodb.com/?pk_campaign=devops-com-blame-oss-02-14 )

**不要把 DevOps 精灵放回瓶子里**

我预计我们会看到这种趋势继续下去。开发人员的力量将在很大程度上增加，因为行业将使他们能够更好地管理他们的应用程序，或者与他们的运营同行更无缝地合作。但是 Ops 对开发者发号施令的时代已经结束了。

怪开源。