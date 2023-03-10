# Chef 推进合规自动化

> 原文：<https://devops.com/chef-advances-compliance-automation/>

Chef 今天通过一次更新扩展了其 InSpec 平台的自动化合规性管理范围，该更新增加了对 Amazon Web Services (AWS)和 Microsoft Azure 公共云的支持，以及与其他第三方工具的集成。总之， [InSpec 2.0](https://www.businesswire.com/news/home/20180220005216/en/Chef-InSpec-2.0-Delivers-Compliance-Velocity-Accelerate) 增加了 30 多种附加功能，包括对 Docker 容器、微软 IIS 和 NGINX web 服务器以及 PostgreSQL 数据库软件的支持。

此外，InSpec 结果现在可以导出为 JUnit 格式，以便集成到 Jenkins 等持续交付工具中。合规性配置文件现在也可以从 Chef Automate 中提取。

此外，根据 Chef 的说法，InSpec 2.0 在 Windows 上的运行速度比 InSpec 1.0 快 90%，在 Linux 上快 30%。

Chef 的产品营销总监 Julian Dunn 表示，InSpec 的主要目标是使 DevSecOps 团队能够在应用程序部署到生产环境之前解决合规性问题。Dunn 说:[对于任何 DevSecOps 团队来说，记住任何软件或硬件配置时必须应用的所有合规性要求](https://devops.com/survey-not-much-compliance-progress-in-devops-world/)是不可行的。

InSpec 提供了一种机制，使用一组声明性工具来自动化合规性管理，这些工具不要求 IT 团队中的任何人拥有编程技能。Dunn 承认，就将合规性纳入任何 DevSecOps 计划而言，这仍处于早期阶段，其中大多数计划本身都是新生事物。但邓恩指出，现在合规性与安全性一起转移只是时间问题。

邓恩说，在云时代，安全性变得更加突出，因为开发人员现在经常在基础设施上部署工作负载，而这些基础设施通常不由内部 IT 运营团队管理。事实上，最近出现了一系列安全漏洞，其根源在于数据暴露在 AWS 等公共云上。

关于遵从性在多大程度上鼓励安全性，一直存在激烈的争论。倡导者说，如果没有一些基本的法规遵从性要求，大多数组织内部的安全级别会比现在更糟糕。其他人认为，法规遵从性要求只会鼓励组织实施最低限度的安全性要求；从而产生一种虚假的安全感，网络罪犯很容易利用这种安全感。然而，无论从哪个角度来看，法规遵从性要求都不会很快消失。事实上，重大的安全违规通常不会伴随着巨额罚款，这是基于被忽略的法规遵从性要求的数量。

在比以往任何时候都更快地部署和更新应用程序的压力下，开发人员并不总是意识到法规遵从性的所有细微差别。当今的组织需要找到在不降低应用程序开发速度的情况下强制执行法规遵从性要求的方法。如果不增加对自动化的依赖，这是不可能实现的。不幸的是，今天，大多数被认为是合规性过程的东西直到应用程序被部署到生产中很久之后才开始，这使得修复那些一旦被发现的疏忽比在应用程序开发生命周期的更早阶段被发现要昂贵得多。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)