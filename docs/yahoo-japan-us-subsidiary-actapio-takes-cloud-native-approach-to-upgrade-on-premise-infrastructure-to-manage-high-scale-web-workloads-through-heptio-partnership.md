# 雅虎日本美国子公司 Actapio 采用云原生方法升级内部基础设施，通过 Heptio 合作伙伴关系管理大规模 Web 工作负载

> 原文：<https://devops.com/yahoo-japan-us-subsidiary-actapio-takes-cloud-native-approach-to-upgrade-on-premise-infrastructure-to-manage-high-scale-web-workloads-through-heptio-partnership/>

*合作伙伴关系体现了新客户数量的增长和员工招聘的加速*

华盛顿州西雅图。东部时间 2018 年 4 月 23 日上午 6 点今天， [Heptio](https://heptio.com/) 与雅虎日本公司(Yahoo Japan Corporation)的子公司 Actapio 合作，宣布推出 Gimbal，这是一项开源计划，旨在将网络流量统一和扩展到由多个 Kubernetes 集群和包括 OpenStack 在内的传统基础设施技术组成的混合环境中。

Gimbal 通过将大量流量路由到 Kubernetes 集群和 OpenStack 等现有解决方案，为希望在其环境中采用 Kubernetes 的公司消除了障碍，这些解决方案通常在企业基础架构中并存。这种云原生解决方案是为管理 Kubernetes 工作负载的高度动态性而定制的，而昂贵的现有解决方案并不具备这种特性。通过使用 Gimbal，公司可以利用[云原生](https://blog.heptio.com/cloud-native-part-1-definition-716ed30e9193)系统的灵活性来实现传统基础设施的现代化，从而以更低的成本加快上市时间。

万向架的优点包括:

*   **成本效益。** Gimbal 是一种运行在商用硬件上的软件解决方案，其功能与昂贵得多的专用硬件解决方案相同。这为真实世界的环境创造了一个更加经济实惠的解决方案。
*   简单灵活。多团队 Kubernetes 集群(各种规模)的框架规模，降低了复杂性，提高了可靠性。由于是 API 驱动的，它可以轻松地与传统和云原生系统集成。
*   **云原生第一；传统友好。**现有解决方案不支持动态、快速扩展的云原生部署。Gimbal 是为了与 Kubernetes 无缝集成并处理动态工作负载而从头开始构建的。它还与现有系统集成，以创建一个可以跨越新旧后端系统的统一流量层。
*   **多云就绪。** Gimbal 支持在任何内部云上、在部署了 Kubernetes 的云平台上以及作为跨多个云的网络实现负载平衡。它可以作为云提供的负载平衡器的替代方案，确保工作负载与其运行的基础架构完全分离。

Actapio 首席执行官兼总裁 Norifumi Matsuya 表示:“我们联系了 Heptio，希望它能帮助我们在 Kubernetes 上实现基础设施的现代化，同时又不影响我们在 OpenStack 和其他后端系统上的传统投资。“大规模应用交付是我们业务的关键。我们需要更快的服务发现和 canary 部署功能，以提供即时回滚和性能测量。Gimbal 使我们的开发人员能够应对这些挑战，这在宏观层面上有助于他们提高工作效率和优化系统性能。”

“这一合作展示了云原生技术和开源的全部潜力，不仅可以管理应用程序，还可以解决更广泛的基础设施问题，”Heptio 的创始人兼首席执行官 Craig McLuckie 说。“Kubernetes 是一个自然的起点，但将其完全融入现实世界仍是一个不断发展的故事。Gimbal 等系统有助于在现有系统和新的云原生基础设施(如 Kubernetes)之间建立务实的桥梁。我们很高兴能与 Actapio 合作，更广泛地研究交通管理。”

Actapio 的实施凸显了 Heptio 自 2016 年 11 月从[隐身](https://blog.heptio.com/founding-members-of-kubernetes-team-create-company-heptio-to-bring-kubernetes-and-containers-to-5c185724f412)以来的业务势头。在 Accel Partners 和 Madrona Venture Group 的支持下，该公司从 2017 年第四季度到 2018 年 Q1 奥运会的收入增长了 140 %,这是其逐年增加大量新客户的势头的一部分。该公司还将其员工人数从 2017 年的 Q1 增加了三倍。

Gimbal 目前处于 alpha 阶段，正在积极开发中。Heptio 和 Actapio 期待与开源社区合作，建立一个灵活的系统。

*   在这里下载[链接](https://github.com/heptio/gimbal)
*   此处提供了该项目的技术细节

KubeCon Europe 的与会者还可以通过 Heptio:

*   Heptio booth 展位上的 1:1 专家对话和演示
*   与 Actapio 的 Boothside 问答
*   “云原生基础架构”的现场签售会
*   会议从周二的[“我们如何建造轮廓”](https://events.linuxfoundation.org/events/kubecon-cloudnativecon-europe-2018/program/schedule/)开始，一直持续到周五(所有九场演讲[在此](https://events.linuxfoundation.org/events/kubecon-cloudnativecon-europe-2018/program/schedule/?gclid=EAIaIQobChMI1r-am7SN2gIVQZppCh3R4w6IEAAYASABEgJSPfD_BwE)

**关于七肽**

Heptio 通过产品和服务释放技术驱动型企业，帮助客户实现 Kubernetes 的全部潜力，并将其转变为业务加速器。该公司的培训、支持和专业服务加速了 Kubernetes 和相关技术与企业 IT 架构的集成，同时其产品降低了在生产环境中运行这些系统的成本和复杂性。要了解更多信息，请访问 heptio.com。

###