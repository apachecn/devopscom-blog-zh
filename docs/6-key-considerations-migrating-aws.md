# 迁移到 AWS 时的 6 个关键考虑事项

> 原文：<https://devops.com/6-key-considerations-migrating-aws/>

每天，越来越多的组织冒险迁移到 Amazon Web Services 公共云。他们留下的是传统数据中心的繁琐，但尽管云在可扩展性、敏捷性和效率方面具有优势，他们发现了一系列需要克服的新挑战。

Gartner 估计，到 2017 年，超过 50%的企业将采用混合云方法。然而，从传统的内部 IT 基础架构过渡到公共云可能会令人望而生畏，成功需要不同的思维模式和一系列技能。这种转变对传统企业来说尤其具有挑战性，因为它们有很多利害关系。以下是迁移到 AWS 云的五个主要挑战。

## 云金融

不同的组织有不同的财务方法，他们对 IT 基础设施的选择反映了这一事实。对于一些人来说，预先投入大量资金购买基础架构，然后随着时间的推移将投资转化为资本，这种内部部署方法可能是更好的选择，因为他们更喜欢保持对其 IT 环境的完全控制。然而，对于其他人来说，高昂的初始费用并不理想，因此只有持续运营成本的云方法更合适。此选项可能特别适合每月需求波动的组织，因为内部数据中心无法提供他们所需的灵活性。

不管采用哪种方法，在决定哪种方法最合适之前，比较各自的成本是很重要的。最佳选择可能是结合内部部署和云来创建混合云环境。这将允许稳定的工作负载保留在现场，而突发的需求可以由按需公共云处理。

## 安全性、可用性

由于明显的安全性和可用性问题，将所有数据移交给公共云提供商的想法可能令人望而生畏。但是，公共云提供商必须遵守严格的合规性协议，并且可以实施和维护比本地安装高得多的安全级别，因为他们有更多的可用资源。

事实上，出于安全考虑，企业长期以来一直避免向云迁移。然而，这种情况正在慢慢改变，因为 IT 领导者现在意识到，在公共云上运行实际上可以带来更高安全性的优势，因为 AWS 拥有符合行业标准的云基础设施(例如 HIPAA 和 PCI-DSS 标准)。

尽管如此，AWS 客户必须了解他们在保护用户数据和实施服务水平协议(SLA)方面的责任。更多信息，请看一下 [AWS“分担责任”模型](https://aws.amazon.com/security/sharing-the-security-responsibility/)。

## 主机更换(提升和转移)与重建(重新设计)

在内部应用程序可以迁移之前，向云的迁移需要一些准备工作。 [Gartner 描述了](https://www.gartner.com/newsroom/id/1684114)五种不同的应用程序迁移方法，其中两种在讨论 IaaS 时特别相关——重新托管和重建。

重新托管(也称为“提升和转移”方法)包括将应用程序重新部署到不同的硬件环境中，而不改变应用程序的架构。虽然这是一个快速解决方案，可以让您的应用程序快速在云上运行，但重新托管的应用程序可能无法利用云的主要优势(如水平可伸缩性)，因为它们是在定制的垂直集成硬件之上构建的。重新托管使组织能够摆脱高昂的内部基础设施成本，但是这种方法主要适用于具有容易定义的模式的应用程序。

资源密集型应用程序(如用于图像渲染或大数据分析的应用程序)更适合重建(或“重新架构”)方法，在这种方法中，原始代码被废弃并用新代码替换。这些类型的应用程序自然依赖于商用硬件，并具有扩展能力，因此将它们放在封闭的本地孤岛中可能意味着最终会出现性能问题和高成本。

重建自然是一个耗时耗力的过程。因此，解决方案介于这两种方法之间，主要决定因素是工作负载的成本和安全性。

## 从一开始就把它做好

在这个过程的开始，要小心选择你要迁移到云中的应用或服务。如果前几个成功了，那将为整个迁移定下基调。如果一些早期的项目失败了，对迁移的热情将会减少，并使其更难完成。

明智地选择最有可能成功的项目，例如可以轻松迁移的非关键应用程序或服务。通过使用现代的监控和日志记录系统，确保您的环境从一开始就是透明的，这些系统可以收集大量的日志数据，然后对其进行解析以发现事件并提供有见地的信息。

此外，了解您的云环境将显著提高您的成功率。不要野心太大，试着一次完成。随着一个个小成功，您的团队将确保顺利迁移。

## 当心员工的担心

IT 环境中的任何重大变化都会引起员工的担忧。您可能认为这种转变会遭到公司管理层的抵制，但是真正的怀疑来自您的 IT 团队。在使用本地基础架构多年后，管理员不会欢迎任何他们认为可能危及其工作的变化。帮助你的团队接受这种转变，确保他们接受适当的培训，为新的挑战做好准备。

## 日志分析和指标收集

转向 AWS 的组织突然发现自己管理着一个高度可扩展和高度动态的环境，这需要一种新型的日志分析和指标收集。在动态环境中，数据集中化的需求是至关重要的，因为您经常会发现自己试图在不再存在的服务器上排除故障。

在最近的 [re:Invent](https://reinvent.awsevents.com/) 中，AWS CTO 沃纳·威格尔强调了集中日志收集的必要性，这是 AWS 迁移成功的必要条件:

> IT 组织突然能够访问数以千计的服务器，这些服务器运行的应用程序比以往任何时候都多，最终生成的日志文件也比大多数 IT 组织能够处理的要多。…为了在云中取得成功，IT 组织需要不懈地衡量系统和应用程序的运行情况。问题是日志收集和处理很麻烦。

沃格尔斯描述的所有单个组件都有自己需要分析的重要日志数据输出。为了确保 AWS 迁移成功，必须监控来自您的应用程序、基础架构和 S3 访问存储桶等的日志，以确保您的新 AWS 环境的所有部分都以安全、高度可用和可扩展的方式运行。(为了帮助 IT 组织，我们发布了关于 AWS 日志分析的免费电子书[和开源的 ELK 堆栈](http://logz.io/aws-loganalytcis-elk-lp/)。)

## AWS:最后一点

AWS 是当今企业首选的公共(IaaS)云，而且看起来将继续如此。为了在将工作负载和产品迁移到 AWS 的过程中实现成功的过渡，需要以循序渐进的方式仔细规划和实现该过程，向所有利益相关者证明迁移的好处。