# Platform9 推出行业首个独立于基础设施的托管 Kubernetes 服务

> 原文：<https://devops.com/platform9-launches-industrys-first-infrastructure-agnostic-managed-kubernetes-service/>

加利福尼亚州森尼维尔2017 年 1 月 24 日/美通社/ — Platform9，[开源即服务公司](http://www.platform9.com/)使云基础设施变得简单，今天宣布其托管的 Kubernetes 服务全面可用，这是业内首个与基础设施无关的 SaaS 托管服务。与传统软件分发模式不同，托管 Kubernetes 完全作为一个 SaaS 解决方案跨内部和公共云基础架构进行部署和管理。该公司还推出了[裂变](http://www.platform9.com/fission)，一个新的、开源的、基于 Kubernetes 的无服务器框架。这些产品的特点是大大简化了运营和消费模式，消除了目前与 Kubernetes 相关的陡峭的学习曲线，并允许开发人员和 IT 团队专注于解决核心业务问题。

Platform9 首席执行官 Sirish Raghuram 表示:“在许多开发团队致力于将微服务作为其云原生开发模式的时候，SaaS 管理的交付使 Kubernetes 能够面向更多的受众。“我们已经在我们的 OpenStack 即服务产品上建立了我们的声誉，这仍然是一个核心焦点，仅在 2016 年就推动了平台 9 400%的客户增长。虽然企业将在未来几年内在 OpenStack 上运行虚拟化工作负载，但对提供虚拟化、微服务或两者兼而有之的平台的需求不断增长。微服务尤其需要一种更直观、更受管理的方法来缩短 Kubernetes 项目的价值实现时间，并在任何选择的基础架构上工作:内部、云中或跨多个云。”

Kubernetes 已经成为容器编排和微服务的标准，但项目经常受到有效使用 Kubernetes 所需的极其陡峭的学习曲线以及完全集成和管理生产 Kubernetes 环境所需的技术复杂性的阻碍。Platform9 的托管 Kubernetes 服务是完全集成的，真正与基础设施无关，并引入了一种更快、更易于管理的方式来利用 Kubernetes。它为开发运维团队和 It 团队节省了大量时间和资金，使他们能够跨云平台或内部基础架构的任何组合进行集成，而无需重新设计任何一行代码，也无需担心后端配置和维护。

“平台 9 管理的 Kubernetes 是生态系统的积极补充，有助于使 Kubernetes 在任何地方运行，”谷歌的 Kubernetes 产品经理大卫·阿龙奇克说。“这体现了数千名项目参与者的创新和动力，他们推动 Kubernetes 成为云原生和容器化应用的标准。”

“在生产中运行容器化应用的一个重大挑战是管理容器编排软件堆栈。例如，工程师需要观察 Docker 运行时或集群协调代理的升级，以确保升级期间生产应用程序不会停机。托管 Kubernetes 为认真使用容器的公司提供了重要价值，因为它消除了管理容器编排层的复杂性，同时可以在任何基础架构上运行

**托管 Kubernetes 功能**

Platform9 Managed Kubernetes 具有许多重要功能，使其成为真正的企业级产品:

*   **纯玩法 Kubernetes，SaaS 托管:**托管 Kubernetes 将上游版本打包为“SaaS 托管”解决方案，这意味着它将始终是 100%纯玩法，避免供应商锁定。因为该解决方案是作为 SaaS 部署、监控、支持和升级的，所以用户可以专注于使用 Kubernetes，而没有管理开销。
*   **完全集成，可在任何地方运行:**开箱即用的 Kubernetes 集成包括:端到端安全性、支持 SSO 集成的用户配额多租户控制、与外部持久存储和负载平衡器的集成，使其易于在从内部部署到公共云提供商(如 AWS、Microsoft Azure 和 Google Compute Engine)的任何基础架构中使用。
*   **高可用性:**托管 Kubernetes 创建高可用性、多主、多 etcd 的 Kubernetes 集群，可以跨越您的私有或公共云环境中的可用性区域。这意味着您的 Kubernetes 环境可以跨一个或多个可用性区域容忍本地故障。
*   **与 OpenStack 并行运行:** Managed Kubernetes 作为 Platform9 Managed OpenStack 的对等服务提供，让客户可以自由选择。微服务开发者可以使用独立于 OpenStack 的 Kubernetes，虚拟化应用开发者可以使用 OpenStack，IT/运营可以通过单个管理面板跨两个框架进行管理。

有关 Platform9 管理的 Kubernetes 的更详细的技术概述，[单击此处](http://www.platform9.com/managed-kubernetes)。

**裂变:AWS Lambda 的事实上的开源替代品**

裂变代表了开始为 Kubernetes 开发应用程序的最快、最简单的方式。它提供了一个简单的、无服务器的接口来利用 Kubernetes，使开发人员和 It 团队能够编写基于 REST 的应用后端、事件驱动的自动化或定制的应用控制器。开发人员现在可以在几个小时内将简单的 REST 功能部署到 Kubernetes 上，而不是花费数周时间来实现 Kubernetes 强大抽象的价值。

裂变是完全开源的，在提供直观的无服务器开发者体验方面类似于 AWS Lambda。然而，裂变在几个重要方面不同于 AWS Lambda:

*   **随处运行:**裂变将无服务器与底层基础设施分离。它可以在 Kubernetes 可以运行的任何地方运行，从开发人员的笔记本电脑到企业和服务提供商的数据中心，以及公共云，如 Google Container Engine 或 Amazon Web Services。
*   **开放和可扩展:**裂变是一个开源项目(在云计算原生计算基金会的初始阶段)，从而使贡献者和用户的广泛生态系统能够在开源的保护伞下协作。该框架可扩展到各种语言和运行时。
*   **使 Kubernetes 更加用户友好:**裂变为 Kubernetes 或微服务的新用户提供了更直观的第一次体验，并将加快 Kubernetes 的应用时间。此外，裂变使得集成其他 Kubernetes 服务变得容易，为使用领先的微服务框架构建的应用程序提供了更大的自动化和灵活性。

**附加资源**

*   促成裂变:[https://github.com/fission/fission](https://github.com/fission/fission)
*   了解有关使用平台 9 简化 Kubernetes 的更多信息:[http://www.platform9.com/managed-kubernetes](http://www.platform9.com/managed-kubernetes)
*   请求免费试用平台 9 管理的库伯内特:[http://platform9.com/free-trial](http://platform9.com/free-trial)

**关于平台 9**

Platform9 为需要更快、更简单地管理跨多个平台的云基础设施的企业提供了开源即服务。与自己动手或传统解决方案不同，Platform9 提供了 OpenStack 和 Kubernetes 等同类最佳的云基础设施作为 SaaS 管理的解决方案，以降低成本和缩短价值实现时间，同时避免局限于单一供应商生态系统。Platform9 帮助开发人员和 IT 团队专注于解决核心业务问题，同时自动化后端的大部分设置和管理流程。它使 Box、Blue Cross Blue Shield 和 PlayStation 等客户实现了 99%以上的 OpenStack 项目成功率。Platform9 由早期 VMware 工程师团队于 2013 年创建，由 Menlo Ventures 和 Redpoint Ventures 提供支持，总部位于加利福尼亚州森尼维尔。欲了解更多信息，请访问[www.platform9.com](https://www.platform9.com/)。

——[儒勒·路易斯](https://devops.com/author/jules/)