# Splunk 推出统一观察平台

> 原文：<https://devops.com/splunk-unveils-unified-observability-platform/>

[Splunk](https://www.splunk.com/) 今天发布了一个以云服务形式交付的可观察性平台，它可以实时捕获所有指标、跟踪和日志，而无需依赖采样。

Splunk 负责可观测性和 IT 运营的产品管理副总裁 Spiros Xanthos 表示，Splunk 可观测性云通过基于开源 OpenTelemetry 软件的单个代理收集所有数据，以便为应用程序提供工具。

过去，应用性能管理平台(APM)仅分析数据样本来识别潜在的异常。Xanthos 说，Splunk Observability Cloud 分析其代理软件捕获的所有流数据，使 IT 团队能够更快地找到问题的根本原因。

因此，Xanthos 表示，与传统监控平台相比，信噪比显著提高。Xanthos 补充说，然后将由每个 It 团队决定在分析后他们希望存储多少数据。Splunk Observability Cloud 的定价基于使用的主机数量，而不是收集的数据量。

Splunk 观察云统一了 Splunk 分析产品组合，包括通过 Splunk 日志观察器、Splunk 真实用户监控(RUM)、Splunk 合成监控、Splunk 基础架构监控、Splunk APM 和 Splunk 电话技术支持提供的功能。Splunk 合成材料监控基于 Splunk 去年通过[收购 gracience](https://devops.com/splunk-adds-plumbr-and-rigor-to-observability-portfolio/)获得的技术。

![Splunk](img/9aaf17fa756d2789eb4b30229ddb93e3.png)

Splunk Observability Cloud 是第一个完全依赖 OpenTelemetry 代理软件来收集数据的平台，该软件是在云本地计算基金会(CNCF)的支持下开发的。该项目不仅降低了检测应用程序的成本，还减少了 it 团队为收集指标、跟踪和日志数据而部署的代理数量。

许多竞争对手的可观测性平台可以从 OpenTelemetry agent 软件中收集数据，但也倾向于鼓励 DevOps 团队部署他们声称更容易安装的专有代理软件，并在更细粒度的级别上收集数据。Xanthos 说，Splunk 认为 OpenTelemetry 已经成熟，不再需要那些专有代理。

可观察性平台的兴起为 IT 团队提供了一个机会，使大量经常出现冲突分析的监控工具合理化。如今，IT 团队花费大量时间召开所谓的“作战室”会议来确定问题的实际来源。这些会议可能会持续几个小时，最终发现一个只需要几分钟就能解决的问题。

虽然可观察性一直是 DevOps 的核心原则，但大多数 IT 团队对其应用程序环境的可见性水平是有限的。监视工具并不缺乏，但是因为没有观察 IT 环境的统一方法，所以根本没有提供足够的环境。随着 IT 环境变得越来越复杂——这主要归功于基于微服务的应用程序的兴起，这些应用程序之间存在许多依赖关系——缺乏上下文很快成为一个主要问题。基于微服务的应用被设计成在一个微服务突然变得不可用时适度降级。问题是发现性能下降的根本原因可能需要很长时间。

大多数 It 团队实现真正的可观察性可能还需要一段时间，但是一旦他们做到了，许多人会想以前没有它他们是如何管理的。