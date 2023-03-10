# 问答:Puppet Labs 首席信息官 Nigel Kersten

> 原文：<https://devops.com/qa-puppet-labs-nigel-kersten-high-performance-business-continuous-integration-quality-control/>

最近，我们采访了 Puppet Labs 的首席信息官 Nigel Kersten，他谈到了高性能 IT 以及他在 Puppet Labs 工作期间所看到的持续集成趋势。Nigel 从谷歌总部加入 Puppet Labs，在那里他是“傀儡师”，负责设计和实现世界上最大的傀儡部署之一。Kersten 也是一名经验丰富的 Linux 和 Mac 部署系统管理员。

如果你不熟悉的话，Puppet Labs 提供 IT 自动化系统配置和管理软件，它被初创企业和超大型企业所使用。这是我们与 Nigel 的讨论，我们讨论了最近的 Puppet Labs DevOps 报告和高绩效组织。

**DevOps.com:在 [2014 年 DevOps 报告](http://puppetlabs.com/2014-devops-report)中，高绩效 IT 和高绩效公司之间似乎存在某种关系。你能看出其中的因果关系和关联吗？是高性能公司驱动高性能 it，还是高性能 IT 驱动高性能公司？**
**奈杰尔:**目前，就我们拥有的数据量而言，这是一种相关性。调查数据实际向我们展示的是，采用 DevOps 实践可以提高 IT 组织的绩效。这意味着您更频繁地发布代码，您的故障恢复时间大大加快，我们所知道的所有这些都有助于打造一个优秀的 IT 组织。
实际上，我们已经能够将那些拥有更高绩效 IT 团队的组织与市场上的竞争对手联系起来，并且他们正在超越自己的企业目标。现在，在这个时候，我们只是有点试探性地说，这是一种相关性，而不是因果关系。
需要明确的是，从统计数据来看，我们非常确信这实际上是一种因果关系，而不仅仅是一种关联。但是我们还没有准备好做出这样的声明。

DevOps.com:我们想知道持续集成如何改变安全团队、应用团队、运营和 QA 之间的关系。从广义上讲，你认为这些关系与几年前相比有什么变化？
**奈杰尔:**我认为有几件事正在改变这些关系。我认为，从某种程度上来说，瀑布式的方法正在慢慢走向死亡，而敏捷方法正在走向死亡。这并不是说敏捷是好的，瀑布是坏的，因为我确实认为在一些开发环境和问题空间中，真正严格的基于瀑布的方法才是正确的做事方式。
但我们肯定会看到许多组织正在转向更敏捷的设置。我认为这意味着对持续集成系统和 QA 团队的需求已经发生了很大的变化。开发人员期望更多的自助服务，并且他们期望能够在更紧密的反馈循环中运行。他们不想提交代码，等到第二天——直到一组 12 小时的测试运行完毕——才发现他们的代码是否有问题。在此之前，我认为我们几年来所看到的是开发人员使用本地虚拟化技术，通过自己的方式开始了影子 QA。但是在过去的一两年里，我们看到了一种趋势，QA 团队被迫向开发组织提供更快的反馈和更多的自助服务。

DevOps.com:这一定会让那些习惯于严格、稳定、有序流程的人心痛。
**奈杰尔:**很有趣吧？这其中有些是推测性的，因为很多安全人员往往都是非常有远见的人，我不认为安全行业的每个人都是如此，就像每个行业一样。但我认为这迫使人们审视他们当前的安全实践，找出什么是安全策略，什么实际上提高了产品的安全性，或者他们发布的任何东西。
因此，我们如何能够自动执行那些实际上提高安全性的事情，以便安全性不会成为这些快速反馈循环中的瓶颈。我同意这肯定会让安全人员心痛，尤其是那些已经习惯了严格的代码变更审批和那种你把它放在你的作品中的职责分离的人。我在这里看到的是一种普遍的妥协，实际上我认为这是一种非常有效的方式。对于某些环境，您确实希望维护投入生产的内容，并拥有严格的变更批准流程。但这应该是一个快速且适度轻松的过程。
我们看到人们让开发人员能够运行测试，改变测试环境，并在生产前持续集成中对整个堆栈拥有很大程度的自主权。人们专注于让开发人员能够提升机器的类别，修改运行在机器上的测试，改变所有这些事情，以便他们获得真正快速的反馈循环。但是，当实际合并到生产中时，这是您现有的类型变更控制流程可以处理的事情。
这意味着，就持续集成而言，我们看到许多人将他们的基础设施分为开发、测试和生产。
开发人员在虚拟机上进行大量本地开发工作。说到测试，通常是在共享的基础设施上，使用类似 Puppet 的东西，可以配置成与生产系统完全相同。这对开发者来说已经足够好了。他们得到了紧密的反馈回路。他们测试代码的方式与在官方持续集成管道中测试代码的方式非常相似，但是您仍然可以围绕从测试到生产的合并管理紧密的变更控制过程。

DevOps.com:如果它像计划的那样工作，你会认为你会得到改进的代码结果，因为开发人员更接近任何缺陷。
**奈杰尔:**绝对。我认为这就是这种系统想要提供的全部承诺。我认为，如果你没有一个非常严格的开发组织，它确实会失败，而且它只是生产基础设施的开放季节。在这种情况下，它实际上变得适得其反，因为反馈回路变得越来越长。然后，如果测试失败了，你永远也不会确定是不是因为其他人扰乱了告诉你测试是否通过的系统。

DevOps.com:听起来它们是随着时间的推移而自我纠正的问题，因为安全通常会发现“隐藏的”或潜在的问题，直到发生不好的事情时你才会发现。但是，如果它对生产造成全面冲击，那么我可以想象您会遇到可用性和性能方面的其他问题，并且相关的质量问题会很快增加。
**奈杰尔:**绝对。我认为这是人们将大量工作转移到云的原因之一，我在这里是根据经验来说的，因为我管理的 sys ops 团队实际上管理着 Puppet Labs 持续集成系统的基础设施。我们有一个非常复杂的测试矩阵，显然安全性是我们非常关心的问题，因为当 Puppet 部署在某人的基础设施上时，它在许多方面都有通往王国的钥匙。
因此，小公司很难提供足够的内部硬件基础设施来支持这种弹性峰值消耗。我认为这是人们的一大驱动力，至少，使用云来消除他们的内部硬件需求，以便在容量达到峰值时，他们基本上可以向云爆发。

DevOps.com:我认为，走这条路的组织在从他们以前所做的——更多的手动驱动过程——转向持续集成之前，需要非常了解他们自己的过程？
**奈杰尔:**我认为我们倾向于看到的是，它最终会以逐个项目为基础。如果你是一家销售内部软件或软件即服务的公司，你在那里已经有了合理的投资，很少有公司会花时间暂停软件的交付。通常，他们需要不断赚钱；他们需要不断发布版本。
因此，我们倾向于看到人们开始尝试绿色的野外环境。根据我的直觉，这通常是通过人们转向更面向服务的架构来实现的，在这种架构中，他们不是发布大型的、单一的应用程序，而是发布彼此之间具有良好定义的边界的组件。随着重构的进行，当他们构建一个新的组件时，他们可能会以一种完全不同的方式对该组件进行测试和持续集成，并以这种方式逐步完成他们的代码库。
最终，你必须处理棕色区域的部署。但是，理想情况下，到那时，你已经从绿色领域持续集成系统中获得了一系列巨大的成功，使投资回报显而易见。

**DevOps.com:我想，从这些小组中获得的知识会与进行实验的小型工作组共享，然后会有大量知识共享和从内部有机扩展**。
**奈杰尔:**是的。人就是人，这往往是地盘之争爆发的地方。有很多次，我们走进组织，与 QA 团队、开发人员和运营人员交谈——开发人员和运营人员已经开始合作，他们可以通过这种方式更快地交付产品——但不知何故，QA 团队觉得自己被整个流程忽略了。这可能是一场相当复杂的谈话。

DevOps.com:您认为公司在向持续集成部署发展时会犯常见的错误吗？
**奈杰尔:**我看到人们在考虑时犯的一个更概念性的错误是，他们混淆了持续部署和大量的公开发布，它们不一定是一回事。我经常试图告诉人们，持续部署实际上是让人们能够选择交付某种产品。如果这种区别有意义的话，它应该是一个可运输的单元，而不一定要运输。许多公司将会开始紧张。他们会想知道他们现有的流程和对渠道经销商的培训。他们会认为他们根本负担不起每两周或每周发布一次的成本。但这不一定是持续交付的全部意义。通过拥有可发布的工件，您能够进行内部测试，您能够进行更容易的实验，并且如果您愿意，您仍然可以选择每六个月发布一次您的产品。但是事实上，在这些公开发行版之间可能有 20 个发行版，这一点很重要。它们都可以被发布，可以是针对某个客户的错误修复，或者使您能够在未来进行某些类型的开发。这些确实是巨大的胜利，即使最终用户实际上从未看到那些特定的版本。