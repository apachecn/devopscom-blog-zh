# 从 Kubernetes 工作负载中识别和提取商业智能

> 原文：<https://devops.com/identifying-and-abstracting-business-intelligence-from-kubernetes-workloads/>

在大数据时代，企业被数据点淹没。虽然他们知道有大量有价值的资源可供他们使用，但理解这些数据以获得可操作的见解通常仍然是一个挑战。

CNCF [行业调查数据](https://www.cncf.io/blog/2018/08/29/cncf-survey-use-of-cloud-native-technologies-in-production-has-grown-over-200-percent/)显示，在使用和部署 Kubernetes 方面，工作负载复杂性和监控仍然是企业面临的最大挑战。许多人知道这些环境中有宝贵的资源，但努力从机器数据中最好地识别和提取意义。虽然这些数据大部分都是现成的，但只需要合适的工具来收集和查看智能见解。

## 开源数据收集的好处

细读 [CNCF 网站](https://www.cncf.io/projects/)，围绕 Kubernetes 建立了大量[工具](https://www.cncf.io/projects/)，不仅可以监控，还可以联网、存储和安全。甚至有一个特定于 Kubernetes 的包管理器， [Helm](https://helm.sh/) ，使这些资源的部署和管理变得容易和一致。

利用这些开源收集器有几个主要好处:

1.  它们保持最新。这些工具都受益于深入的社区支持。随着 Kubernetes 新版本的发布，这些工具的广泛使用确保了它们的快速更新。
2.  它们与一切融为一体。例如，普罗米修斯有一份令人印象深刻的整合和出口商名单。不管您的栈是什么样的，都有可能支持您想要导出的数据。这些集成的重要性怎么强调都不为过，因为它们支持随着时间的推移发展和改进 Kubernetes 部署所需的灵活性。

## 确保完整和有组织的指标收集

由 CNCF 认可的 Prometheus T1 实际上是度量监控的首选工具，[为您收集度量数据提供了广泛的支持。](https://prometheus.io/docs/instrumenting/exporters/)

Prometheus 通过从 Kubernetes 中运行的所有组件和作业中提取数据来工作，因为 Kubernetes 的每个组件都以一种 [Prometheus 格式](https://prometheus.io/docs/concepts/data_model/)公开其指标。运行在这些组件后面的流程然后在 HTTP URL 上提供指标。例如，Kubernetes API 服务器在 https://$API_HOST:443/metrics 上提供其指标。

Prometheus 特别擅长自动发现 Kubernetes 集群中当前运行的作业和服务。随着 pod 的添加、删除或重启，Kubernetes 服务结构会跟踪给定服务中存在哪些 pod。这种自动发现能力是 Prometheus 受欢迎的主要原因之一，确保所有新的和现有的组件都受到监控。

## 集群级日志记录和事件收集的重要性

Kubernetes 没有定义单一的日志收集标准方法，但是最常用的方法叫做[集群级日志](https://kubernetes.io/docs/concepts/cluster-administration/logging/#cluster-level-logging-architectures)。集群级日志记录在每个节点上部署一个节点级日志记录代理，然后将数据传输到一个单独的后端，用于存储和分析日志。这种解决方案的主要好处是，如果一个 pod 死亡，详细记录发生了什么的日志会保留下来。实现节点级日志记录，而不将数据集中到日志后端，将不会在 pod 死亡或被驱逐时保留日志数据，而集群级日志记录确保数据被捕获和保留。实现集群级日志记录的一个常用工具是[Fluentd](https://www.fluentd.org/)——或 Fluentbit，fluent d 的一个轻量级版本——它充当节点级日志记录代理，将数据传输到日志后端。

事件提供了对集群所做决策以及 Kubernetes 中发生的意外事件的深入了解。事件由 API 服务器存储在主节点上，并使用与日志收集相同的方法进行收集——通过 Fluentd 这样的节点级日志记录代理。

## 建立连续的情报仪表板

最后，可以使用 Helm——一个开源的 Kubernetes 包管理器——轻松部署日志、指标、事件和安全性的收集器。Helm 可以显著简化设置过程，将数百行配置减少到一行。这些集合插件可以在任何 Kubernetes 集群上使用，无论是来自 Amazon Elastic Kubernetes Service(EKS)这样的托管服务，还是完全由您自己运行的集群。

根据 Sumo Logic 最近的[连续情报报告](https://www.sumologic.com/brief/continuous-intelligence-report/)，企业采用和部署的云计算同比增长了 50%，80%的跨云计算环境的用户现在正在使用 Kubernetes 架构。随着 Kubernetes 继续成为主流，企业必须了解这些工作负载是如何运行的，以及如何最好地提取有价值的见解来为业务决策提供信息。

— [凯蒂·莱恩](https://devops.com/author/katie-lane/)