# 监控 Kubernetes 和 Docker 的六大开源工具

> 原文：<https://devops.com/top-six-open-source-tools-for-monitoring-kubernetes-and-docker/>

Kubernetes 和 Docker 是现代 DevOps 对话中最常听到的两个流行语。Docker 是一个工具，它使您能够容器化和运行您的应用程序，Kubernetes 为您提供了一个平台来编排或管理这些容器——因为使用 Docker CLI 手动管理数千个容器将是一个现实的噩梦。

然而，仅仅运行数千个容器并通过 Kubernetes 管理它们是不够的。您必须正确地观察和分析它们，以确保您的服务启动并以最佳方式运行。这个过程被称为[【SRE】](https://en.wikipedia.org/wiki/Site_Reliability_Engineering)【站点可靠性工程】，一个由 Google 发起并推广的术语。可观察性和分析是 SRE 的主要元素。它可以细分为以下三个方面:

*   **监控** 允许您从您的应用程序和资源中提取数字指标，稍后可以对其进行可视化和分析，以呈现您的资源的当前状态。一旦提取了指标，就可以使用它们来设置警报规则，促进分析和调试，并做出更好的 SRE 决策。
*   **日志** 使开发者能够在失败的情况下调试他们的容器。容器是短命的，日志也是。Kubernetes 和 Docker 确实提供了一种浏览容器日志的本地方式，但是它的功能非常有限。因此，在任何面向容器的环境中，集中式日志平面都是必不可少的。
*   **跟踪** 允许你调试运行在网络上的服务，并跟踪请求，直到确定问题的根源。在微服务架构中，当多个服务/容器相互发送请求以执行一项业务任务时，适当的跟踪解决方案是必要的。

本文将列出并描述最有效的开源工具，用于监控和分析作为容器运行的服务。

## **普罗米修斯**

[普罗米修斯](https://prometheus.io/) 是讨论开源监控解决方案时首先想到的工具。在开发界很受欢迎，是 [CNCF](https://www.cncf.io/announcement/2018/08/09/prometheus-graduates/) 项目的毕业生，重点是 SRE 的监控端。Prometheus 最初由 SoundCloud 创建并开源，它简化了根据时间序列从给定指标端点提取数字指标的过程。它是为了监控高度动态的容器环境而构建的。

Prometheus 细分为三个要素:Prometheus 服务器、Alertmanager 和 exporters。导出器是独立的流程/容器，可以在目标资源上运行，通过 metrics API 生成和导出指标。然后，Prometheus 服务器负责服务发现，并从导出器中提取指标，存储在 Prometheus 数据库中，稍后用于可视化或警报。Alertmanager 负责设置警报规则，分析 Prometheus DB 中的数据，并在触发特定规则时向多个接收者发送警报消息。有大量的出口商， [列在这里](https://prometheus.io/docs/instrumenting/exporters/) ，它们都是由普罗米修斯官方支持，由社区维护。

Prometheus 已经成为监控云原生架构的行业标准。虽然它以其服务发现的简单性、易用性、警报能力以及与 Kubernetes 的集成而闻名，但它的轮询架构并不理想。目前，metrics 端点必须能够被 Prometheus 服务器访问。但是，在 Prometheus 中实现了一个[push gateway](https://prometheus.io/docs/practices/pushing/)，它支持度量推送而不是轮询。普罗米修斯的另一个缺点是扩展性不好。这个问题可以在《普罗米修斯》的[灭霸改编中得到修复。](https://improbable.io/blog/thanos-prometheus-at-scale)

相关工具和技术:Grafana、Cortex、灭霸、普罗米修斯出口商、警报管理员、Istio、普罗米修斯操作员。

![](img/801a119178d88a771a8c0c026c21c9e9.png)

Figure 1: Prometheus Graphs. Source: [SoundCloudDev](https://developers.soundcloud.com/blog/prometheus-monitoring-at-soundcloud?source=post_page---------------------------).

## **格拉法纳**

[Grafana](https://grafana.com/) 是一个开源的度量分析和可视化套件。它允许您使用来自多个来源的数据创建自定义仪表板，如 Prometheus、Elasticsearch、MySQL、Postgres 和 Redis。此外，Grafana 拥有自己的警报系统和基于角色的软件访问控制(RBAC)系统。作为一个数据可视化工具，Grafana 在 Prometheus 用户中很有名，因为它使他们能够有效地可视化存储在 Prometheus 中的指标。Grafana 中有各种各样的官方和社区构建的自定义仪表盘，允许用户轻松设置仪表盘( [见此链接](https://grafana.com/grafana/dashboards) )并进行监控。Grafana 提供了另一个名为[Loki](https://github.com/grafana/loki/blob/master/docs/README.md)的关联产品，它在 Kubernetes 中聚合日志，并与 Grafana UI 很好地集成。

相关工具和技术:洛基，普罗米修斯。

![](img/ec43856ae2a4d70d7b4cb1d5eae943d3.png)

Figure 2: Kubernetes Resources Dashboard in Grafana. Source: [Replex](https://www.replex.io/blog/kubernetes-in-production-the-ultimate-guide-to-monitoring-resource-metrics-with-grafana).

## **弹性堆叠**

[Elastic Stack](https://www.elastic.co/products/) 是一组来自 Elastic 的开源产品，旨在帮助用户实时搜索、分析和可视化来自任何类型来源、任何格式的数据。这个产品以前被认为是 ELK stack，其中每个字母的缩写代表该公司的一个主要产品:Elasticsearch、Logstash 和 Kibana。Elastic Stack 借助其大数据数据库 Elasticsearch 提供监控和日志记录解决方案。

为了聚合日志，人们倾向于使用 Elasticsearch 进行存储，使用 Logstash 或 Fluentd 进行日志流传输，使用 Kibana 进行可视化。Fluentd 不是 Elastic Stack 的一部分，但它广泛用于 Kubernetes，以代替 Elastic Stack 提供的工具 Logstash 来传输日志。类似地，Metricbeat 用于在 Kibana 上收集指标和设置可视化。弹性堆栈的企业版附带 X-Pack，这是一套附加工具，可实现报告、警报和基于角色的访问控制(RBAC)等功能。默认情况下，弹性堆栈 GUI ki Bana 不支持 RBAC。您必须使用前面提到的弹性堆栈企业版来启用它。

相关工具和技术:X-pack，Metricbeat，Logstash，Kibana。

![](img/7cb66de1071d9ba02ebbf434a5c1033f.png)

Figure 3: Discover View in Elasticsearch. Source: [XpresServers](https://www.xpresservers.com/how-to-set-up-an-elasticsearch-fluentd-and-kibana-efk-logging-stack-on-kubernetes/).

## **Sensu Go**

[Sensu Go](https://sensu.io/) 是一个遥测和服务健康检查解决方案，用于大规模的多云监控。它允许您了解任何公共云或私有云上的服务器、容器、服务、应用程序、功能和连接的设备。Sensu 可以与 Prometheus 并行运行，以获得两种解决方案的最佳效果，也可以在没有 Prometheus 的情况下在本机运行。Sensu 与 Prometheus 配合使用效果最佳，因为将应用程序级指标导出到 Prometheus 需要将 Prometheus SDK 加载到您的应用程序代码库中，并公开一个指标端点。然后，端点被抓取并存储在 Prometheus 服务器中。这可能听起来工作量很大——有时确实如此。Sensu 通过使用边车概念避免了这种复杂性。Sensu 代理与您的应用程序一起部署。该代理不断收集指标并向 Prometheus 服务器公开，而无需您更改应用程序代码库。

Sensu 的作品也没有普罗米修斯。它可以在 Kubernetes 中本地运行，在那里它有自己的服务器来存储和可视化前面提到的 Sensu 代理公开的度量数据。

相关工具和技术:普罗米修斯。

![](img/2173ab25b7b10a703d9a5fd17929f488.png)

Figure 4: Events in Sensu. Source: [becon](https://www.becon.de/new-it-monitoring-solution-sensu-go-part-1-of-3/?lang=en).

## **系统检查**

[Sysdig](https://sysdig.com/opensource/inspect/) 有两款开源产品:Sysdig Inspect 和 Falco。这里，我们将重点关注 Inspect，它监视和捕获系统中运行的容器进程，并允许您深入这些进程进行事后取证。这使您能够分析您的应用程序性能，排除错误并监控任何可能行为不当的处理器。此外，如果您的系统遭到破坏，Sysdig 允许您了解破坏是如何发生的，以及在此过程中获取了哪些数据。Sysdig Inspect 是一个非常强大的工具，它专注于系统的性能调优和安全性调查。

相关工具和技术:Grafana，Sysdig，Sysdig Falco。

![](img/c115b5119ba1eb8cb5960c1d1d47fb8e.png)

Figure 5: Sysdig Inspect Overview. Source: [Sysdig](https://sysdig.com/blog/sysdig-inspect/).

## 耶格

[耶格](https://www.jaegertracing.io/) 是优步工程开源的端到端分布式追踪解决方案。它允许您监视复杂的分布式系统中的事务并对其进行故障排除。在现代微服务架构中，大多数操作问题都属于网络和可观察性的范畴。当服务出现故障时，您不知道请求是如何通过网络从一个服务传递到另一个服务来完成单个业务事务的。这使得调试极其困难。Jaeger 目前正在 CNCF 的指导下，使用跟踪来实现根本原因分析、性能和延迟优化以及分布式事务监控。Jaeger 用 [Istio](https://istio.io/) 开箱即用，这是 Google 开源的一个流行的服务网格实现。

相关工具和技术:普罗米修斯，耶格，齐普金，伊斯蒂奥。

![](img/a38157f84d76f9bffce5ebd95bfbc98b.png)

Figure 6: Jaeger Find Traces. Source: [Jaeger](https://www.jaegertracing.io/docs/next-release/).

## **结论**

这些工具在科技行业被广泛使用，它们都有自己的好处。然而，这些解决方案中的大多数都需要熟练的实现和持续的手动维护，这对于开发运维团队来说是一种负担，而且会分散他们的业务精力。没有一个解决方案可以满足您的所有需求，因为每个工具都专注于可观察性和分析的一个或两个特定方面。通过将这些工具混合在一起，您可以为您的个人业务需求找到一个独特的解决方案。

为了便于比较，下面的图表概述了本文中讨论的每个工具所提供的特性。

![](img/73b4625cbd2f4a6f6fdbf41c7d467582.png)

— [Ran Ribenzaft](https://devops.com/author/ran-ribenzaft/)