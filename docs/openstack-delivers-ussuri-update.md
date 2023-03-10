# OpenStack 提供 Ussuri 更新

> 原文：<https://devops.com/openstack-delivers-ussuri-update/>

OpenStack 社区今天正式发布了 Ussuri，这是对云管理框架的[更新，它加强了组件之间的集成，包括使用讽刺的 IT 自动化框架自动供应裸机服务器的能力。](https://www.prweb.com/releases/openstack_ussuri_release_lands_today_delivering_automation_for_intelligent_open_infrastructure/prweb17114528.htm)

此外，该社区还在 Kuryr 项目中添加了 IPv6 支持，用于将 [OpenStack](https://devops.com/deploying-openstack-pick-a-distribution-with-these-7-qualities/) 与容器网络相集成，并在 Zun 容器运行时项目中支持 Kubernetes 集群的 CRI-O 映像规范。因此，IT 团队现在可以在 Kubernetes 集群上使用 Zun 创建的 pods，这些集群可以运行 OpenStack 基金会赞助开发的 Kata 容器。

OSF 的执行董事 Jonathan Bryce 表示，OpenStack 仍然得到了来自 188 个不同组织的 1000 多名开发者的大力支持。在此版本中，对 OpenStack 进行了超过 24，000 处代码更改。根据 451 Research 的数据，到 2023 年，OpenStack 生态系统的价值有望达到 77 亿美元。

大多数 OpenStack 部署都基于虚拟机。然而，随着对运行 Kubernetes 等平台的裸机服务器的兴趣增加，对使用 OpenStack 在该基础架构上自动进行配置的兴趣也在增加。

![](img/1a48ff7e702fd556b13091b0d865c7f5.png)

同时，【Kubernetes 和 OpenStack 之间的关系依然复杂。许多组织更喜欢在虚拟机上部署 Kubernetes，以确保隔离。其他人认为在裸机服务器上运行 Kubernetes 是完全消除虚拟机需求的一种方式。现在说这场辩论将如何结束还为时过早，但目前大多数 Kubernetes 实例都部署在虚拟机上。问题是，是在几个开源虚拟机中的一个上部署 Kubernetes，还是采用已经在企业 IT 环境中广泛采用的 VMware 商业虚拟机。

OSF 还试图推动 Kata 容器的开发，这将使 IT 团队能够在轻量级虚拟机上部署容器运行时，以实现工作负载之间的隔离。布莱斯说，IT 团队应该期待看到 Kata 项目的重大升级，这将使运行时更容易部署。

过去十年对 OpenStack 的投资是巨大的，所以已经采用它的许多组织不太可能很快放弃它。然而，在绿地环境中，许多组织正在考虑推出仅基于 Kubernetes 的下一代云原生应用。OpenStack 社区已经表明了其与 Kubernetes 尽可能促进互操作性的意图，Kubernetes 是在云本地计算基金会(CNCF)的支持下开发的。

在 OpenStack 历史的大计划中，Ussuri 不太可能作为一个重大更新被记住。然而，它确实提醒我们 OpenStack 社区仍然非常活跃，特别是在电信提供商继续依赖云框架来自动提供 4G 和 5G 网络服务的情况下。

与此同时，已经采用 OpenStack 的企业 IT 团队应该预计在未来几年内将使用它来配置基础架构，以运行基于单片和微服务的应用程序。