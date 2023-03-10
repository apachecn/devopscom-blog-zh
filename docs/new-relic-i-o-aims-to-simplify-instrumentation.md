# New Relic I/O 旨在简化仪器仪表

> 原文：<https://devops.com/new-relic-i-o-aims-to-simplify-instrumentation/>

New Relic 今天在 kube con+CloudNativeCon North America 会议上推出了一项 New Relic Instant Observability(I/O)计划，通过该计划，它可以提供开源工具来简化应用工具。

New Relic 工程高级副总裁 Marck Robinson 表示，工具目录将帮助 DevOps 团队开发更广泛的应用。New Relic 将把这些工具作为其通过云交付的可观察性平台的免费层的一部分。Robinson 说，DevOps 团队将能够使用 400 多种预配置的快速入门工具来检测应用程序和创建仪表板。

New Relic 本身正在为云服务、开源工具和平台(如 Kubernetes、Istio 和 Cassandra)提供快速入门服务。已经为目录做出贡献的第三方供应商包括 Cribl、Fastly、Gigamon、Kentik、Lacework 和趋势科技。Robinson 指出，作为促进更大的开源可观测性生态系统发展的努力的一部分，每个贡献都受到 New Relic 的审查。

![](img/51e13de6e27400760c4fb913c66fd6da.png)

Robinson 说，总的来说，New Relic 正试图让 DevOps 团队更容易弥合阻碍 it 组织超越监控以拥抱其 IT 环境的真正可观察性的仪器差距。最近的 New Relic 2021 可观测性预测报告指出，只有四分之一的受访者(26%)拥有成熟的可观测性实践，最常提到的可观测性障碍是缺乏资源(38%)和技能差距(29%)。

Robinson 说，因此，当涉及到检测应用程序和构建仪表板时，DevOps 团队经常会遇到最后一英里的可观察性挑战。

作为简化应用程序测试的更大努力的一部分，New Relic 拥有开源代理软件，在云计算原生计算基金会(CNCF)的支持下对 OpenTelemetry 工具进行了标准化，并且[为 CNCF](https://containerjournal.com/kubeconcnc/new-relic-to-donate-pixie-observability-platform-to-cncf/) 贡献了用于 Kubernetes 环境的 Pixie observability platform。

在某个方面的可观察性一直是任何 DevOps 最佳实践的核心原则。最初，DevOps 团队将持续监控作为主动管理应用环境的最有效方式。然而，发现问题的根本原因仍然需要几天甚至几周的时间。然而，可观察性平台的出现使得分析工具更容易识别指示 it 问题根本原因的异常行为。有了这些见解，it 团队更快地解决问题就变得简单多了。

相比之下，监控侧重于预定义的指标，以确定特定平台或应用程序何时在预期范围内运行。例如，被跟踪的度量通常集中在资源利用上。另一方面，可观察性将指标、日志和跟踪(日志记录的一种特殊形式)结合起来，以某种方式检测应用程序，从而简化问题的故障诊断，而不必仅依赖于一组有限的预定义指标来监控特定流程。

随着基于微服务的应用的兴起、向云的转移以及越来越多的终端用户远程工作，对可观察性的需求变得前所未有的重要。现在的问题是找到一种方法使它更容易实现。