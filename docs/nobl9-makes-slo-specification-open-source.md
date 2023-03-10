# Nobl9 使 SLO 规范开源

> 原文：<https://devops.com/nobl9-makes-slo-specification-open-source/>

在今天的在线 [SLOconf](https://www.sloconf.com/) 活动中，Nobl9 透露，它为使 it 团队能够实现服务水平目标而创建的平台( [SLOs](https://devops.com/?s=SLO) )现在可以在开源 Apache 许可下使用。

Nobl9 的首席产品官 Brian Singer 表示，目标是制定一个用于定义 SLO 的 YAML 规范格式，其中包括一个解析器和基本的验证和测试功能，更易于通过 [OpenSLO](https://www.businesswire.com/news/home/20210518005315/en/SRE-Community-Launches-OpenSLO-Specification-at-SLOConf) 项目访问。当组织部署基于微服务的应用程序时，实现这一目标至关重要，因为这些应用程序的依赖性往往会对性能和可用性产生负面影响。

Singer 说，虽然 SLO 和/或服务水平协议(SLA)的概念已经存在很长时间了，但通过雇佣站点可靠性工程师(SREs)来接受 DevOps 最佳实践的 IT 团队正在有计划地尝试确保实现 SLO，同样重要的是，维护 SLO。从历史上看，大多数 SLA 都没有得到很好的执行。他指出，OpenSLO 通过将 SLO 目标嵌入到 YAML 文件中，成为基于 Git 的工作流的一部分，使实现这一目标成为可能。

![SLOs](img/3e1b324de88e1719c6c968597415af28.png)

《站点可靠性工程》一书的作者尼尔·理查德·墨菲已经签约成为 OpenSLO 的核心贡献者，与 GitLab、Dynatrace 和 Nobl9 的成员一起工作。Singer 说，最终的目标是通过使用一个对象模型来构建可移植的 SLO 规范，使得在多个应用程序开发项目之间共享和移植这些规范变得更加简单。

与此同时，Nobl9 将继续运营基于 OpenSLO 的软件即服务(SaaS)平台来管理 SLO。Singer 指出，随着 OpenSLO 的应用越来越广泛，对它的需求将会增加。Nobl9 SLO 平台与 Datadog、New Relic 和 Prometheus 等监测平台兼容，并使用从监测和可观测性平台收集的数据来计算每项服务的可接受误差率。它可以被配置为在预期停机时触发警报甚至工作流。

该平台可通过 CLI/GUI/API 访问，还支持开发运维团队根据所需的应用体验创建业务规则和定义用户的“方面”。除了跟踪用户组之外，DevOps 团队还可以识别服务不佳的用户。他们还可以将合同义务与关键业务期间的 SLO 相关联。

该平台还使确定如何使系统更可靠或降低可靠性目标以尽可能降低成本变得更加容易。IT 组织还将使用更易于访问的实时和历史数据来确定任何问题的根本原因，从而减少时间。如今，it 团队花费数周时间寻找应用程序降级问题的根源，却发现问题可以在几分钟内得到解决，这种情况并不罕见。

就采用 SLO 代码而言，现在还为时尚早，但是 SLA 或 SLO 充其量只是理想的意向声明的日子即将结束。预计 SLO 将很快通过嵌入在应用程序代码中的 YAML 文件来维护，并分布在一个快速扩展的企业中，其相互依赖性超过了任何 IT 团队可以手动跟踪的程度。