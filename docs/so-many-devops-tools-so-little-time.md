# 这么多 DevOps 工具，这么少的时间

> 原文：<https://devops.com/so-many-devops-tools-so-little-time/>

我收到了数以千计的电子邮件、广告和针对应用生命周期每个阶段的工具的推销，从自动化基础设施构建到发布规划，再到构建和测试，再到交付应用。如果您正在构建或重新构建一个应用程序，那么您有太多的开发工具可供选择。

具有讽刺意味的是，当一个组织投资于各种 DevOps 工具时，它会导致被工具孤立的不相连的团队。Gartner 称之为“不相连的自动化孤岛”除了文化问题，它还会导致重大事故和停机。

你不能把自己变成 DevOps。但是下面是如何确保你不会用错误的工具伤害你的团队。

## **第一步:工具前处理**

找出你需要解决的问题，然后找到满足需要的工具。这听起来很简单，但许多公司却反其道而行之:他们已经选好了工具，然后用它来解决每一个问题。

"如果你只有一把锤子，所有的东西看起来都像钉子."如果你只有一两个主要工具，所有的问题都会被这些工具解决。我们的团队对此也有责任。当你真正擅长一种工具时，比如木偶或厨师，每个问题的答案都不可避免地是木偶或厨师。

对于我们的团队来说，解决方法是创建没有工具名称的流程和架构图。相反，我们描述了每个阶段需要发生的事情。如果我知道我正在构建一个长期运行的虚拟机，我知道我需要一个配置管理组件。一旦我们就流程达成一致，然后我们就讨论工具。

工程师是务实的人，他们被训练成受我们使用的工具的约束。为了打破这种思维定势，写出你想要的不带工具名称的代码管道，即使你“知道”你将要使用的 DevOps 工具。

## **第二步:基础设施和应用工具并重**

一家软件公司最近告诉我一个不愉快的故事:该公司花了数年时间来完善其持续交付渠道，一切都像钟表一样运转良好。开发人员可以在几分钟内测试并运行代码。

开发团队知道如何推送代码，但是在他们的区域什么也做不到。它的一些交付工具运行在同一个云区域，所以即使其他区域运行正常，团队想要用来执行故障转移的工具也不可用。当该团队进行故障恢复时，其灾难恢复基础架构的配置没有跟上生产的步伐，因此实例大小不足以运行应用程序。

这个故事的寓意是，您的基础架构和应用程序需要相同级别的自动化和敏捷性。即使你有一个非常成熟的 CI/CD 渠道，包括门控、审批、林挺等。，如果您的基础架构堆栈没有相同的规程和工具，那么您同样会失败。您应该能够将您的应用程序从一个区域移动到另一个区域(如果您真的很有野心，可以从一个云移动到另一个云)。此外，如果您没有将应用程序开发整合到基础设施开发中，随着时间的推移，您的基础设施将会过时。

你应该问这样的问题:

*   我们可以采取哪些步骤来自动化基础架构配置？
*   我们如何不断地测试失败？
*   我们可以采取哪些步骤来应对平台故障？

## **第三步。集成基础设施和应用工具**

从平台故障中幸存下来的最佳方式是不断“实践”构建全新的基础架构和应用程序堆栈，作为一个连续的过程，而不是两个不同的活动。

这里有一个极端的例子。Logicworks 的团队最近与一家大型企业软件公司合作，该公司正在推出一款具有定制部署管道的内部产品。流水线包括几十个并行的自动化和手动测试，每个都在一个独立的开发环境中。当对开发环境进行新的部署时，必须创建一组新的 45+ dev 实例，这些实例具有新版本的代码；测试完成后，必须终止实例。这意味着他们环境中的实例很少能持续超过 24 小时，在一周的时间里，数百个实例被终止和重建。

可以想象，该公司从未经历过无法恢复的基础架构宕机，因为它已经每周从“故障”中恢复数百次。这是不可变基础设施的真正含义:虚拟实例是可处置的，一旦实例化了基础设施和代码，就永远不会改变实例。通过这种方式，基础架构永远不会偏离其初始的已知良好状态，操作得到简化，并且系统能够很好地自我更新，因此故障不会发生。

理想情况下，基础设施自动化和应用程序自动化不是不同团队的不同堆栈，而是具有相同破坏性测试级别的相同堆栈，因此需要根据基础设施的当前状态来测试应用程序的进步。

## **总结**

新的 DevOps 工具和特性的不断发布可能会让人不知所措。但是您的 DevOps 团队面临的最大挑战可能与 CI/CD 工具无关。我发现人们很容易过分强调工具，而忽视关键的(尽管不那么迷人的)自动化组件，比如基础设施模板和测试。

您的开发人员一直在寻找新的库，并为您的应用程序尝试新的语言和工具。您需要对您的整个基础架构和应用程序堆栈进行同等程度的关注和测试。这会让你选择更好的应用级工具，为失败做好准备。

— [杰森·麦凯](https://devops.com/author/jason-mckay/)