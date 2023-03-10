# Grafana Labs 增加了可视化工具来简化 Prometheus 查询

> 原文：<https://devops.com/grafana-labs-adds-visual-tools-to-simplify-prometheus-queries/>

在其[Grafana online](https://grafana.com/about/events/grafanacon/2022/)活动上，Grafana 实验室今天宣布了对开源 Grafana 仪表板的更新。此次更新增加了可视化查询工具，使任何技能水平的 it 专业人员都可以更容易地对 Prometheus 监控平台或该公司的 Grafana Loki 日志聚合框架进行查询。

此外，Grafana 表示，Grafana OnCall 的开源版本，一个调度和寻呼应用程序，现在也可以作为开源软件在内部 IT 环境中使用。此前，Grafana OnCall 仅作为托管 Grafana 云服务的一部分提供。

Grafana 实验室的产品营销总监 Archana Kesavan 表示，Grafana 核心平台的 9.0 版本使 Prometheus 监控更容易实现。普罗米修斯是在云本地计算基金会(CNCF)的支持下推进的。它最广泛地用于 Kubernetes 环境，但也可以用于单片应用程序。Grafana 的最新版本增加了对痕迹和 Prometheus 稀疏直方图的样本覆盖的支持。

此版本添加的其他功能包括仪表板预览和标题搜索功能，默认情况下支持信封加密，扩展的导航栏和改进的热图面板，其渲染速度比前代产品更快。
’
![](img/654af978cdb9fa1214b8039ceb4a1c1a.png)

最后，Grafana 实验室最初作为一个选项引入的警报系统现在是一个默认设置。

Kesavan 说，除了使启动查询变得更容易，Grafana 实验室的方法还限制了一个糟糕的查询影响运行 Prometheus 的集群的能力。

总的来说，普罗米修斯的采用率随着库伯内特的增加而增加。至少在最初，采用 Kubernetes 的 DevOps 团队经常雇佣 Prometheus 来监控平台。不太清楚的是，一旦在生产环境中部署了云原生应用程序，IT 团队将在多大程度上继续依赖 Prometheus。许多 IT 团队已经使用了一个监控平台，并选择将其扩展到 Kubernetes 环境中。然而，反过来，一些组织选择用 Prometheus 监控平台取代传统工具来监控 Kubernetes 环境和传统的单片应用程序。

至少， [Prometheus](https://devops.com/?s=Prometheus) 已经为从 Kubernetes 环境中收集监控数据建立了事实上的标准，这些数据可以通过各种工具进行查询。

无论如何，Kubernetes 集群很快就会部署在需要监控的扩展企业中。DevOps 团队自然需要自己决定如何最好地监控这些集群，并最终以一种能够启动查询和在问题变成大问题之前发现问题的方式来观察它们。

与此同时，DevOps 团队可能会考虑整合他们目前使用的许多监控工具，作为简化运营工作的一部分。目标应该是拥有足够的工具来确保验证，而不是花费数小时来整理相互冲突的报告，而不是必须将十几个工具中的事件关联起来以确定问题的根本原因。