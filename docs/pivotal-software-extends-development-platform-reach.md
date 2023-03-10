# Pivotal 软件扩展了开发平台的范围

> 原文：<https://devops.com/pivotal-software-extends-development-platform-reach/>

Pivotal Software 宣布对其 Cloud Foundry 平台即服务(PaaS)环境的实施进行[扩展，此外还将其对 Kubernetes 的支持扩展到亚马逊网络服务(AWS)公共云。](https://investors.pivotal.io/news/financial-news/press-release-details/2018/Pivotal-Announces-Updates-to-Pivotal-Cloud-Foundry-at-SpringOne-Platform/default.aspx)

在其 [SpringOne Platform 2018](https://springoneplatform.io/) 大会上，Pivotal 透露，Pivotal Cloud Foundry (PCF)现在可以跨多个数据中心扩展其开源 PaaS 分布的单个实例。此外，Pivotal 使得自动更新其 PaaS 托管的操作系统成为可能，并为其 PCF Healthwatch 监控工具添加了一个更具可扩展性的用户界面。

此外，Pivotal 宣布，其 Kubernetes 的实现 Pivotal Container Service (PKS)现在可以部署在亚马逊网络服务(AWS)公共云的 EC2 实例上。PKS 目前基于 Kubernetes 的 1.11 版本，该版本已与一个软件定义的运行时打包在一起，用于旋转称为 Kubo 的集群，该运行时是在云计算基金会(CFF)的支持下开发的，该基金会也负责监管 Cloud Foundry。PKS 是与 VMware 合作开发的，VMware 是 Pivotal 的姐妹公司，在同一个戴尔技术保护伞下运营，最新版本增加了配置命名空间或群集的功能，可将日志发送到特定目标，如 VMware vRealize Log Insight，无需操作员干预。

Pivotal 产品高级总监 Richard Seroter 表示，Pivotal 和 VMware 正在合作，使 Kubernetes 集群更易于企业 IT 组织访问，这些组织通常没有工程师来管理 IT 运营。他补充说，通过结合 VMware 和 Pivotal 的自动化框架，预计 PKS 将获得更多关注，因为 IT 组织正在评估在生产环境中部署哪种类型的 Kubernetes。云原生计算基金会(CNCF)最近发布的一份研究报告表明，这一策略正开始获得关注。

Pivotal 显然在追求双重应用程序开发策略。第一个是基于 PCF 框架，它在应用程序应该如何构建和部署方面有很强的规范性。第二个是基于 Kubernetes 的更灵活的容器即服务(CaaS)平台。

一般来说，已经投资 Cloud Foundry 来部署 PaaS 的组织不太可能在一夜之间放弃它而转向容器平台。但 Pivotal 和 CFF 面临一些压力，要求它们在统一 Cloud Foundry 和 Kubernetes 方面更加积极:已经有几个 Cloud Foundry 实例运行在 Kubernetes 之上，Pivotal Software 本月早些时候透露，它最近一个季度的账单收入比华尔街的预期低 25%。

Cloud Foundry 和 Kubernetes 之间的关系可能需要一段时间才能在 It 专业人士的心目中更加牢固地建立起来。但是，在开发现代应用程序时，肯定不缺少选择——在未来的许多年里，将有不少组织采用多种框架来构建这些应用程序。真正的问题可能在于从这些投资中获取价值。

Pivotal 本周发布的调查结果显示，只有 39%的全球组织持续、每小时或每天部署代码，只有 40%的组织每月、每季度或每年部署代码。调查还发现，与维护或修复旧代码相比，开发人员只有 35%的时间花在为新产品或新功能编写代码以交付价值上。此外，三分之一的美国受访者(33%)报告称，由于安全问题，应用程序发布延迟超过 11 次，而全球这一比例为 21%。显然，还有更多 DevOps 工作要做。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)