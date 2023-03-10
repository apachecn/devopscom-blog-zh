# CircleCI 向 CI/CD 平台添加安全球体

> 原文：<https://devops.com/circleci-adds-security-orbs-to-ci-cd-platform/>

CircleCI 将其自动化软件包管理器(称为 orbs)的范围扩大到网络安全软件，这些软件可以集成到该公司同名的持续集成/持续部署(CI/CD)平台内构建的管道中。

CircleCI 工程副总裁 Mike Stahnke 表示，将 orbs 扩展到网络安全领域将使组织更容易采用最佳 DevSecOps 流程。

第一套 orb 旨在运行在亚马逊网络服务(AWS)和谷歌云上，由七家第三方网络安全供应商创建，包括 Alcide.io、NeuVector、Snyk、WhiteSource、Aqua Security、Anchore、Contrast Security、Probely 和 Twistlock，后者现在是帕洛阿尔托网络公司的一部分。

CircleCI 一直在利用 orb 包管理器来简化 CI/CD 管道中各种功能的集成。迄今为止，已经为 CircleCI 平台开发了大约 900 个 orb。Stahnke 表示，目标是为 DevOps 团队提供采用 orb 的选项，而不是必须手动实施任务，如秘密管理、漏洞扫描或在 DevOps 工作流中执行策略。

Stahnke 说 CircleCI 并没有设想管道的每一个元素都将成为一个球体；有些情况下，开发运维团队会希望对管道的某些方面进行更细粒度的控制。然而，在很多情况下，DevOps 团队不想一次又一次地手工集成相同的功能。

Stahnke 说，CircleCI 预计 orb 将证明在推动采用最佳 DevSecOps 流程方面特别有用，因为需要实施的许多控制在多个管道中是相同的。通过更容易地将网络安全软件整合到管道中，DevOps 团队将不必牺牲速度和敏捷性来确保安全性。

![CircleCI orbs](img/851e6d528da7cb489de7b20e2792f1fb.png)

如今，大多数组织都刚刚开始走上 DevSecOps 之路。在很多情况下，DevOps 流程的采用情况并不均衡。试图将网络安全团队纳入这些流程以确保更高的安全级别是下一个巨大的挑战。然而，鉴于网络安全专业人员的长期短缺，DevOps 管道中的网络安全功能必须以某种方式自动包含在内。在大多数情况下，网络安全团队将继续定义越来越多地由开发人员实施的策略和控制。然而，网络安全团队仍然需要在应用程序部署到生产环境之前，验证这些控制措施是否已经实施和测试。然后，网络安全团队将让开发人员了解他们发现的任何漏洞，团队可以决定在他们认为合适的开发过程的任何下一阶段解决这些漏洞。

当然，DevSecOps 也意味着网络安全团队必须学会信任开发者。从历史上看，这是有问题的，因为许多网络安全专业人士倾向于将开发者视为网络安全问题的主要来源。然而，在将应用程序部署到生产环境中之前解决的漏洞越多，参与构建、部署和保护该应用程序的每个人都会受益越多。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)