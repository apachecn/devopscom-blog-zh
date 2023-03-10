# 为开发运维选择云原生安全平台时要问的 5 个问题

> 原文：<https://devops.com/5-questions-to-ask-when-choosing-a-cloud-native-security-platform-for-devops/>

如果你在 DevOps 工作，你可能听说过 DevOps 的成功在于正确的[人、工具和流程](https://www.twistlock.com/2018/03/12/operationalize-devsecops-practices/)。

Below, we take a look at how you can address the “tools” part of that equation when it comes to security. Specifically, we’ll discuss which questions to ask and what features DevOps teams should look for when choosing a security tool for today’s cloud-native infrastructures.

## 什么是云原生，它对 DevOps 意味着什么？

我们的讨论基于两个主要考虑。首先，我们将重点关注在[云原生](https://www.twistlock.com/2018/08/23/preparing-cloud-native-world/)环境中出现的安全挑战，这意味着这些环境采用的技术包括但不限于容器、无服务器功能和(当然)虚拟服务器。

其次，我们将关注开发运维团队的安全需求。虽然 DevOps 职位可能不明确涉及安全，但我们现在生活在 DevSecOps 时代，DevOps 团队中的每个人都有责任保护基础架构和应用程序的安全。在本文中，我们将考虑哪些类型的工具最适合帮助 DevOps 团队做到这一点，同时也促进可视性和协作，这是健康的 DevOps 策略的重要部分。

这就是我们的目标。现在，让我们看看在为 DevOps 组织评估云原生安全平台时应该问的问题。

### 你到底在保护什么？

这个问题可能看起来很明显——如此明显以至于你可能不会认真考虑它。但是，由于当今的基础架构和环境千差万别，退一步，弄清楚您到底需要保护什么是非常重要的。

您的[工作负载](https://www.twistlock.com/2018/04/03/gartner-market-guide-cloud-workload-protection-platforms/)是否在容器中运行？你也在使用无服务器功能吗，或者你打算增加它们吗？您如何协调您的工作负载？(使用您的云供应商提供的原生 orchestrator，Kubernetes 作为服务运行，您自己的 Kubernetes 构建还是其他？)您预计未来会采用哪些新的云原生技术？

回答诸如此类的问题对于确保您选择能够支持您当前和未来所有云原生环境的安全平台非常重要。在大多数情况下，您会发现专为[保护一系列环境](https://www.twistlock.com/resources/continuum-cloud-native-topologies/)而构建的安全平台(不仅仅是容器化平台，容器化平台通常是大多数自称“现代”安全平台的重点)是最适合您需求的安全平台。

### 您的安全威胁是什么(以及如何阻止它们)？

这是另一个似乎过于明显的问题。但是在这里，威胁的快速变化性质意味着花一些时间来评估您的威胁实际上是什么是值得的。

也要记住，你的特定团队或者你交付的应用所面临的威胁可能与威胁其他团队的不同。这是跨组织通信的 DevOps 原则对于有效的安全管理至关重要的一个地方。

### 安全平台保护哪些层？

扫描容器图像中已知的漏洞是很好的。然而，就其本身而言，它很难构成一个完整的容器策略。设置防火墙或锁定访问控制也是如此。

为了实现真正的安全性，您需要保护基础设施的所有层(包括由其他团队管理的层)免受各种攻击。因此，您需要一个专为整体安全性而设计的云原生安全平台，而不是一个只保护一两层的工具。

### 安全平台从哪里获得其漏洞信息？

当涉及到识别漏洞时，安全平台可以从许多来源获得信息。他们可以查看公共 CVE 数据库或工具供应商提供的列表。

然而，最好的安全平台会从多个来源提取漏洞数据。毕竟，如果你只依靠一个数据源来确定威胁在哪里，你不太可能抓住所有威胁，就像在神奇宝贝的世界里一样，抓住所有威胁是 DevOps 安全的主要优先事项之一。

### 平台的自动化程度如何？

[自动化](https://www.twistlock.com/2018/11/05/automation-crucial-ingredient-microservices-security/)是 DevOps(或者类似的东西)之母。

我的意思是，没有自动化，你就不能非常有效地做 DevOps。

顺便说一句，除非你非常依赖自动化，否则你无法实现云原生安全性。这是因为容器化、无服务器和其他云原生环境的高度动态性意味着试图解释它们生成的所有数据、识别漏洞并手动应对它们是行不通的。这就是为什么您想要一个随时随地都可以自动化的云原生安全平台。

当然，您仍然应该预计到必须手动执行一些任务(这实际上是一件好事——如果我们可以自动化一切，DevOps 工程师就不再需要存在了)。但是在可能的范围内，您的安全平台应该自动化您的安全相关的工作流。

索尼娅·科普耶夫