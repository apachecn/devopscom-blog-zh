# 使用 Datadog 代理获取 OpenTelemetry 跟踪和指标

> 原文：<https://devops.com/ingest-opentelemetry-traces-and-metrics-with-the-datadog-agent/>

[OpenTelemetry](https://opentelemetry.io/docs/concepts/what-is-opentelemetry/) 是云本地计算基金会(CNCF)的一项倡议，它为检测服务和应用提供开放的、厂商中立的标准和工具。许多组织使用 OpenTelemetry 的 API、SDK 和工具集合来从他们的环境中收集可观测性数据并将其导出到他们的首选后端。

作为我们对 open telemetry 的持续承诺的一部分，我们很自豪能够向 CNCF 社区贡献我们的分布式跟踪库。我们还提供了[多种解决方案](https://docs.datadoghq.com/tracing/setup_overview/open_standards/)，以确保 OpenTelemetry 用户能够灵活地将他们的可观测性数据轻松发送到 Datadog 代理中的 Datadog OpenTelemetry 协议(OTLP)支持，使您能够可靠地从已配备 open telemetry 库的应用程序中获取轨迹和指标。 [OTLP](https://github.com/open-telemetry/opentelemetry-specification/blob/main/specification/protocol/otlp.md) 是一种在源、中介(如采集器)和后端之间编码和传输遥测数据的规范。凭借对 OTLP 的本机支持， [Datadog 代理](https://docs.datadoghq.com/agent/)现在使您能够深入了解您的 OpenTelemetry 仪表化应用，而无需更新您的代码或从您现有的工作流程中迁移。

**直接向数据狗代理发送 OpenTelemetry 跟踪**

如果您已经使用 OpenTelemetry 库对应用程序进行了检测，则可以通过 gRPC 或 HTTP 将 OTLP 跟踪直接导出到 Datadog 代理(7.35 版以上)，而无需安装单独的 OpenTelemetry 收集器。下面的代码片段显示了如何更新 Datadog 代理配置文件( **datadog.yaml** )以使代理能够通过 gRPC 接收 OpenTelemetry 跟踪:

datadog.yaml

otlp_config:
接收方:
协议:
grpc:

还可以通过设置环境变量来配置跟踪摄取。有关 Kubernetes(包括 Helm)和其他配置示例，请参见[我们的文档](https://docs.datadoghq.com/tracing/setup_overview/open_standards/otlp_ingest_in_the_agent/)。

一旦收集了 OTLP 跟踪，就可以开始用 Datadog APM 可视化和监控这些数据。您还可以使用这个方法来收集 [OTLP 格式的指标](https://docs.datadoghq.com/metrics/otlp/?tab=sum)。

由于 Datadog 代理还可以从 500 多个集成中收集应用配置文件、网络数据、基础设施指标，以及从您的环境中收集其他遥测数据，因此您可以获得有关 OTLP 跟踪的丰富上下文，并更好地了解您的系统和应用。您还可以[将跟踪与日志](https://docs.datadoghq.com/tracing/connect_logs_and_traces/opentelemetry/)连接起来，以获得您的堆栈的更完整的图片。

或者，您可以使用 Datadog exporter 和 OpenTelemetry Collector 将 OTLP 跟踪和指标导出到我们的平台。此选项有助于简化后端的工作流程。

**使用 Datadog APM 和 OpenTelemetry 的可观测性**

无论您是通过 Datadog 代理还是 Datadog 导出器接收 OpenTelemetry 数据，Datadog APM 都将使您能够通过以下方式深入了解您的应用:

–[实时查询您的所有跟踪信息](https://www.datadoghq.com/blog/real-time-performance-monitoring-with-datadog-distributed-tracing/)以解决关键业务应用程序的性能问题。

–通过检查[请求流图](https://www.datadoghq.com/blog/apm-request-flow-map-datadog/)和[服务图](https://www.datadoghq.com/blog/service-map/)，可视化依赖关系以了解数据如何流经您的架构。

–通过 APM [服务页面](https://www.datadoghq.com/blog/service-page/)了解每项服务的关键信息，该页面提供遥测、SLO、相关事件、部署跟踪数据等的集中视图。

–通过看门狗、数据狗的人工智能引擎自动检测性能异常、[错误部署](https://www.datadoghq.com/blog/faulty-deployment-detection/)、异常值以及关键故障的[根本原因](https://www.datadoghq.com/blog/datadog-watchdog-automated-root-cause-analysis/)

**开启更多可观察性的途径**

Datadog 致力于确保我们的用户能够深入了解他们的服务和应用，无论他们使用的是我们的开源 APM 库、OpenTelementry SDKs 还是其他 OpenTelemetry 兼容的仪器方法。我们很高兴能继续通过提供灵活、可扩展的解决方案，从服务和应用中收集遥测数据。

阅读我们的[文档](https://docs.datadoghq.com/tracing/setup_overview/open_standards/otlp_ingest_in_the_agent/)以了解更多关于 Datadog 代理对 OpenTelemetry 的支持。或者，如果你是 Datadog 的新用户，可以从 14 天的[免费试用](https://docs.datadoghq.com/tracing/setup_overview/open_standards/otlp_ingest_in_the_agent/)开始。