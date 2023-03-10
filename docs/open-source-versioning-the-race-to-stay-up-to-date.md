# 开源版本控制:保持更新的竞赛

> 原文：<https://devops.com/open-source-versioning-the-race-to-stay-up-to-date/>

开源库一度被认为有风险，还没有准备好进入黄金时段，现在已经被包括保险公司在内的大公司广泛使用。原因很简单:在时间和资源有限、试图保持技术竞争力的公司中，试图重新发明一个已经经过战斗考验的轮子已经没有意义了。然而，既然已经做出了开放源代码和解决方案集的承诺，就必须保持对开放源代码库的维护和更新。

## **开源的风险** 

一些活跃的开源库一年更新多次。过时意味着错过更新的功能。此外，如果升级之间的间隔跨越了几次迭代，一些未来的升级可能不是向后兼容的，这在最好的情况下会导致功能问题，在最坏的情况下会导致风险暴露问题。有时，过时的开源库版本可能会使系统和公司遭受攻击。2017 年，美国一家主要金融公司遭到黑客攻击，泄露了数百万客户的信息。黑客利用了一个已经公开一个月的软件漏洞，但该公司没有及时修补其系统。类似的脉络还有其他几个众所周知的例子。

保持现状并不容易。升级可能代价高昂，但落后会让追赶的代价更高。问题是，升级到新版本的频率应该是多少？

## **努力和成本**

公司选择不在每次有新版本时升级的原因之一是成本问题。虽然开放源代码本身是免费的，但是所需的时间和资源可能是巨大的，并且会占用更高优先级的业务技术计划的宝贵资源。另一个问题是，即使升级应该是向后兼容的，如果不实际执行升级，也无法验证这一点。如果存在兼容性问题，则需要进行更大的努力，包括升级、恢复或重建系统。任何大型系统在升级后都必须进行彻底的测试，如果没有自动化工具的帮助，测试会非常昂贵和耗时。

降低这些成本和风险的一种方法是开源库的[持续集成(CI)](https://en.wikipedia.org/wiki/Continuous_integration) 过程。一套好的自动化测试工具提供了很高的可信度，在最新的升级被实现到任何生产环境之前，没有任何东西被破坏。然而，如果没有自动测试来清除升级中的潜在问题，风险和成本会非常高，公司很难跟上，经理们会更愿意推迟升级，而不是执行升级。这就是为什么公司采用 CI 和[连续交付(CD)](https://devops.com/always-on-development-why-continuous-delivery-relies-on-security-by-design/) 过程包括健壮的自动化测试是很重要的。

此外，微服务的使用——一种越来越有效和流行的构建系统的方法——给保持开源库最新的努力和成本带来了另一个扭曲。单独来说，每个微服务都可以快速测试。然而，如果一个应用被分成 50 个、100 个甚至更多的微服务组件，那么即使是测试每个组件的少量手工工作也会很快增加。此外，在广泛部署了微服务的环境中，可能几个月内都不需要更改某些服务，这是使用微服务的好处之一。

## **开源的正确方法**

有一种处理开源库更新的正确方法，它具有以低风险、低工作量和低资源的方式利用新功能和代码稳定性的优势，如下所示:

**规划:**企业和应用程序架构师应该对任何大型框架的路线图保持警惕，这些大型框架将开源库作为任何项目或计划的关键组件。主动识别可能需要升级的开源库是关键。同样，应用程序项目经理应该将开源库升级作为常规和持续项目计划的一部分。例如，当涉及到微服务时，它们应该被它们所使用的库主动分类为服务，以此来识别通常会首先升级的少数服务。这样做的好处是，在向其他库推广升级之前，可以提供一些 sprints 的反馈。

**监控:**开源版本监控必不可少。有一些产品可以帮助识别和报告存在漏洞的库版本。这种监控可以而且应该作为 CI/CD 管道的一部分，并且还可以监控已经在生产中部署的工件。当新的开源库版本可用时，监控过程也可以报告，即使现有的库没有报告的漏洞。

**自动化兼容性筛选:**建立生产版本以总是使用最新版本的开源库通常风险太大。然而，独立的自动化过程可以识别新版本，通过构建和测试过程运行它们，并报告结果。如果测试失败，开发团队会得到一个早期警告，指出他们的代码与升级版本不兼容。这有助于计划和安排修复，如果在当前版本中发现了漏洞，这种主动计划可以更快地解决问题和扭转局面。

**流程:**强大的流程，最好是自动化的流程，是开源版本控制的基础。对于关键的安全升级，必须有一个流程来对确定的变更进行分类和优先排序。对于其他版本的更新，良好的流程有助于简化升级。例如，一个标准的、可重复的过程可能会将较小的版本升级合并到 sprint 工作的常规流程中，从而在降低风险的同时节省时间。

开源版本控制可能很困难，但也不一定如此。通过自动化测试、良好的监控工具和一些前瞻性规划，保持更新的成本和风险可以保持在最低水平，使公司能够获得新特性和功能的好处。

大流士·库珀