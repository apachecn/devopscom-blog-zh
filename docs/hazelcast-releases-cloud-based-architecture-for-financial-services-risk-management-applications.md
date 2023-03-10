# Hazelcast 发布基于云的金融服务风险管理应用架构

> 原文：<https://devops.com/hazelcast-releases-cloud-based-architecture-for-financial-services-risk-management-applications/>

*Hazelcast Cloud Enterprise 现已在所有主流云上可用，包括谷歌云平台*

**加利福尼亚州圣马特奥，2021 年 2 月 24 日**–[快速云应用平台 Hazelcast](https://hazelcast.com/) 发布了一项参考实施，该实施可简化金融服务机构在云中执行和扩展金融风险计算的能力，同时获得实时性能并充分利用资源密集型投资。此外，Hazelcast 还宣布其托管服务 Hazelcast Cloud Enterprise 在谷歌云平台(GCP)上的可用性，该平台用作本参考实施的环境。

信用价值调整(CVA)是在交易对手违约的情况下，对一组给定交易的风险进行的金融衡量。Hazelcast 参考架构展示了内存计算平台如何利用云环境的优势，尤其是在弹性和敏捷性方面。CVA 计算是大规模的计算工作，按需扩展的能力使金融服务公司可以通过只为他们使用的资源付费来控制他们的计算成本。

“云的经济效益是众所周知的，尤其是它能够只为你消耗的资源付费。Hazelcast 首席技术官(CTO)John des jardins 表示:“专用于特定工作负载的内部部署无法充分利用可用资源，因此您的基础架构投资无法实现全部价值。“对于延迟、可预测性和规模至关重要的使用情形，例如这种风险管理场景，Hazelcast 为金融服务行业提供了一个蓝图，用于将任务关键型应用程序迁移到云，并使用超快内存技术来获得竞争优势。”

**实施细节**

一旦实现了内存技术，就可以从数据库中加载交易，并分布在多个节点的缓存层中。然后，可以将输入输入到计算网格中，并行运行计算块，将结果捕获回更为分散的缓存中。在这种情况下，通常需要大约 40，000 个内核的大型服务器群在最短的时间内完成大量计算。

具有数据感知流处理功能的 Hazelcast 分布式数据存储将这种模式从批处理方法转变为管道方法，将输入数据推送到计算场，高效地协调计算，然后在产生结果时汇总结果。“直通处理”方法消除了每个计算阶段的数据写入，从而进一步加快了计算的整体速度。好处是，客户可以从每天或每小时进行计算，转变为基于任何可能改变市场动态的事件进行特别计算。这种演变使金融机构能够对不断变化的市场条件做出更快速的反应，无论这些条件是由商业新闻、国家灾难、地缘政治事件还是其他因素引发的。具有成本效益的风险管理不仅有利于金融机构，也有利于更广泛的市场和全球经济。

当在云中部署这种实现时，就像在 GCP 进行的演示一样，公司可以轻松地扩展基础架构，以适应计算量或所需的运行时间。为了展示这种云原生方法，Hazelcast 将其 GCP 的使用扩展到一个包含 300 个容器化 Hazelcast 节点的集群，该集群运行在一个包含 110 个基于英特尔 Cascade Lake 硬件的虚拟机实例的 Kubernetes 集群上。使用传统的内部部署方法，将不得不购买大量的机器，迫使客户在经济上做出妥协，在峰值负载和低负载之间选择一个机器数量，这对两者都不理想。

**Hazelcast 云企业**

Hazelcast Cloud Enterprise 是一项托管服务，由 Hazelcast 专家代表客户维护软件部署，使员工能够专注于开发业务关键型应用程序，从而提高实时洞察力。随着 Hazelcast Cloud Enterprise 在 GCP 的推出，它现在可以在所有主要的云上使用，包括亚马逊网络服务(AWS)、微软 Azure 和 IBM Cloud。

Hazelcast Cloud Enterprise 具有内置的 WAN 复制功能，可以高效地将数据从任何位置复制到另一个位置，从而确保应用程序及其数据的可用性。这种多云战略支持更广泛的地理数据分布，以运行更接近最终用户的应用和数据，通过跨区域、地区、云提供商和内部站点提供活动副本集群，实现更高的可用性级别。因此，开发人员可以在相同的应用程序框架上构建业务应用程序，无论应用程序部署在哪里，甚至是在边缘或混合云环境中。

有关 CVA 参考实施及其优势的更多信息，请在此下载白皮书:[https://hazel cast . com/resources/credit-value-adjustment-calculation-reference-implementation/](https://hazelcast.com/resources/credit-value-adjustment-calculation-reference-implementation/)

首先，Hazelcast 提供了一个适用于开发和测试场景的 Hazelcast 云企业入门版:[https://hazelcast.com/get-started/](https://hazelcast.com/get-started/)

**关于 Hazelcast，Inc.** Hazelcast 是全球 2000 强企业信赖的快速云应用平台，可提供超低延迟、有状态和数据密集型应用。Hazelcast 平台采用实时流和内存优先数据库技术，简化了本地、边缘或云中分布式应用的开发和部署，成为一项完全托管的服务。

Hazelcast 总部位于加利福尼亚州圣马特奥，在全球各地设有办事处。要了解更多关于 Hazelcast 的信息，请访问 https://hazelcast.com。