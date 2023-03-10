# 开放标准是实现可观察性的关键

> 原文：<https://devops.com/open-standards-are-key-for-realizing-observability/>

[可观察性](https://containerjournal.com/features/the-state-of-cloud-native-observability-tools/)已经迅速成为企业开发的主要焦点。然而，工具蔓延和复杂性会阻碍一些可观察性计划。关于可观察性趋势的 [2022 年 CNCF 微观调查](https://www.cncf.io/wp-content/uploads/2022/03/CNCF_Observability_MicroSurvey_030222.pdf)发现，23%的组织使用 10 到 15 种工具进行监控、度量以及收集日志和跟踪数据。整整 50%的人还指出，使用多种工具的工程师和团队对可观察性提出了最大的挑战。

我最近会见了 Dotan Horovits，他是 Logz.io 的主要开发者支持者，询问他对改进现代开发团队如何处理可观测性的看法。根据 Horovits 的说法，开放标准和开源项目是实现全行业可互操作性的主要驱动力。下面，我们将考虑可观测性所面临的问题，并介绍 OpenTelemetry，这是一个 CNCF 项目，它很快获得了统一来自各种来源的遥测数据的牵引力。

## 获胜的开放标准

Horovits 说，尽管专有监控代理具有很多智能，但它们本质上使用遥测生成和后端存储分析之间的紧密耦合。这可能导致供应商锁定，并导致工具集之间遥测数据的格式变化。“开放标准有能力整合我们的行业，以防止供应商锁定，甚至是竞争环境，并允许我们获得任何来源的任何遥测数据，”Horovits 说。

没有一个开放的标准，在现代多语言软件栈的核心支持不断发展的技术套件是一个挑战。组织不断增加他们的技术堆栈，从 SQL 到 NoSQL、Kafka、API 网关和无服务器云服务，这些模块产生以独特风格格式化的不同数据。此外，公司通常使用不止一个云供应商，这进一步需要一种分离的方法来表示多种云指标。Horovits 解释说:“一旦您的 IT 堆栈变得如此复杂，就需要将所有遥测技术整合到一个统一的可观测性标准中。

## OpenTelemetry 简介

OpenTelemetry 被描述为一种“高质量、无处不在和便携式的遥测技术，以实现有效的可观测性。”使用 OpenTelemetry(有时缩写为 OTel)，工程师可以生成、收集和导出指标、日志和跟踪。OpenTelemetry 与许多流行的库一起工作，并且完全是厂商中立的，并且受到该领域越来越多的[工具](https://opentelemetry.io/vendors/)的支持。OpenTelemetry 于 2019 年 5 月 17 日被 CNCF 接受，是一个正在孵化的项目。

OpenTelemetry registry 拥有数百个库和插件，可以从许多不同的环境中导出和转换遥测数据，从传统资源到当代资源。Horovits 解释说，通过分离数据收集和导出过程，OpenTelemetry 是“一个统治所有人的代理”。当然，他补充说，采用 OpenTelemetry 的供应商可能仍然会提供他们自己的逻辑。

## 更开放的遥测数据的好处

在撰写本文时，[实时公共知识库数据](https://all.devstats.cncf.io/d/1/activity-repository-groups?orgId=1)显示 OpenTelemetry 是 CNCF 第二活跃的项目，仅次于 Kubernetes。那么，为什么可观测性社区对 OpenTelemetry 如此兴奋呢？首先，它提供的互操作性可以等同于效率和时间的节省。Horovits 表示:“OpenTelemetry 为您提供了在整个堆栈中集成的自由。这部分是因为它的开源根使它成为一个力量倍增器。Horovits 说:“你永远无法在一个完全开放的社区中获得如此大的覆盖面。

可以说，由于云原生架构的复杂性，开放的遥测工具集也变得很有必要。大多数组织正在转向由动态、弹性的基于容器的基础设施支持的分布式微服务架构。在这个世界中，一个服务可能跨越多个集群。因此，工程师在过滤数据时可能需要考虑集群、单元、节点和名称空间。

在这个复杂的现实中，有许多方面，增加了需要监控的内容。一般来说，传统的监控系统在这一级变得无效。当试图同时满足许多环境的需求时，会出现工具泛滥和缺乏整合的问题。因此，一个统一的、解耦的可观测性平台是非常有意义的。

## 开放式遥测的未来

我们已经看到云供应商和解决方案提供商大量采用 OpenTelemetry。而且，该项目进展迅速——open telemetry 已经发布了一年左右的分布式追踪规范。Horovits 说，这个项目几乎已经有了度量标准的发布候选，日志的发布也正在进行中。

除此之外，Horovits 感到兴奋的一个功能是连续分析，这可以帮助用户连续分析一个函数，并跟踪跨实例的使用趋势。另一个令人兴奋的潜在发展是 [eBPF](https://logz.io/blog/ebpf-auto-instrumentation-pixie-kubernetes-observability/) 。由于它是独立于语言的，并且在内核级运行，eBPF 可以提取可观测性信号，而不需要特定于应用程序的挂钩或集成。这可以增加对更多环境的支持。

要了解更多信息，您可以访问 [OpenTelemetry 网站](https://opentelemetry.io/)阅读文档或阅读 OpenTelemetry 的[功能路线图。Horovits 还在 KubeCon 2022](https://horovits.medium.com/opentelemetry-roadmap-and-latest-updates-a389144f3812) 上给[做了这个关于 OpenTelemetry 的有用的演示。](https://www.youtube.com/watch?v=qE1ggEmvz2Y)