# 开放式遥测技术在可观测性方面的价值

> 原文：<https://devops.com/the-value-of-opentelemetry-in-observability/>

随着基础设施变得越来越复杂，对更好的可观测性的追求仍在继续。随着容器化、第三方应用的增加以及网络复杂性的普遍增加，组织很难跟踪稳定性和性能问题。但是 OpenTelemetry 可以通过增强和整合所有应用和服务的报告来提高整个网络的可观测性。

那么，[什么是](https://opentelemetry.lightstep.com/) OpenTelemetry，它如何帮助您组织的流程？以下是你需要知道的。

## **什么是 OpenTelemetry？**

OpenTelemetry 是由云本地计算基金会(CNCF)管理的开源库、代理和组件集，旨在提高服务的可见性。通过 OpenTelemetry，组织能够更好地收集遥测数据，以便进行调试和管理。OpenTelemetry 是一种可扩展的灵活解决方案，能够随着组织的不断发展而进行调整。

使用 OpenTelemetry，通过以下方式收集数据:

*   韵律学
*   分布式跟踪
*   资源元数据
*   日志

然后，数据被发送到 Jaeger 或 Prometheus 等后端平台进行处理。所有这些共同增强了组织的可观察性，使组织更容易收集观察和适当缓解问题所需的数据。

更高水平的可观察性提高了组织的可靠性并减少了停机时间。凭借更好的可靠性，组织能够更快地跟踪和解决事件。在 OpenTelemetry 解决方案之前，开发人员可能已经使用了 OpenCensus、OpenTracing 或其他类似的产品。虽然这些产品本身非常优秀，但它们不一定能满足现代网络的所有需求。

## 它是如何工作的？

OpenTelemetry 工作在三个主要的可观测性系统上:跟踪、度量和记录。对于跟踪，OpenTelemetry 通过跟踪系统内的请求，使识别故障和性能问题变得更加容易。对于指标，系统内运行的流程将被密切跟踪和报告，并提供直方图、量表和其他易读的图形报告。对于日志记录，可以分析特定于应用程序的消息。

整个系统的可观察性总是依赖于跟踪、度量和日志记录。但如今完成追踪变得更加困难，因为每个动作都需要经过这么多层应用程序和资源。当使用模糊的日志数据时，追踪单个事件的过程可能需要几个小时，因为这些信息并不总是孤立的。OpenTelemetry(和其他类似产品)致力于通过创建一个整合的系统来纠正这一点，通过该系统可以将指标、跟踪和日志记录结合在一起。

作为一个开源项目，OpenTelemetry 可以在 GitHub 上获得，对于那些想成为社区一员的人来说，可以影响和改进它。当然，OpenCensus 和 OpenTracing 也是开源解决方案。

那么 OpenTelemetry、OpenCensus 和 OpenTracing 有什么区别呢？什么时候应该使用一个而不是另一个？它们可以一起使用吗？

## **OpenTelemetry 与 OpenCensus**

让我们来看看 OpenTelemetry 和 OpenCensus。两者都用于提高可观测性，但它们通常是互斥的平台，因为它们都从不同的角度处理可观测性问题。OpenCensus 通过一组库提供来自应用程序的分布式追踪和时间序列指标。应用程序需要下载一个指标导出器，使用哪个取决于所涉及的应用程序微服务。OpenCensus 将收集跟踪数据，但 OpenCensus 也将收集时间序列指标。OpenTelemetry 用于连接 OpenCensus 和 OpenTracing，提供两者的优势。这就产生了一个更加鲁棒的可观测性解决方案。

## **OpenTelemetry 与 OpenTracing**

OpenTelemetry 对 OpenTracing 类似于 OpenTelemetry 对 OpenCensus。OpenTracing 也解决了与 OpenCensus 相同的问题，但通常是互斥的。OpenTracing 是跟踪 API 而不是库的规范。开发人员既可以创建自己的跟踪器，也可以使用 OpenTracing 版本。OpenTracing 通常更快、更容易部署和使用，但可能无法提供像 OpenCensus 那样强大的分析或指标。但是，OpenTelemetry 通过其统一的库和支持，使同时使用 OpenTracing 和 OpenCensus 成为可能。

OpenTelemetry 是希望提高其可观测性的组织的理想技术。通过 OpenTracing，开发人员能够在整个网络中实现更高级别的可见性；跟踪指标和绩效；并对组织内的问题做出快速而准确的反应。

虽然在过去，开发人员可能只限于 OpenTracing 或 OpenCensus，但今天，开发人员可以将 OpenTelemetry 用于这两种功能集。更好的是，由于它仍然是一个开源解决方案，开发人员能够为 OpenTelemetry 社区做出贡献。