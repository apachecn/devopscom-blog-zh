# 中间层 DC/操作系统 1.11 支持边缘计算、多云操作和数据服务的弹性扩展

> 原文：<https://devops.com/mesosphere-dc-os-1-11-enables-edge-computing-multi-cloud-operations-and-elastic-scale-for-data-services-kubernetes/>

*跨云智能地池化资源，并自动化各种工作负载的操作，为企业提供个性化、机器学习和物联网应用*

**三藩市**–2018 年 3 月 8 日–今天，[meso sphere](https://mesosphere.com/?partnerref=press-release)—[DC/OS](https://mesosphere.com/product/?partnerref=press-release)的创建者，构建和运行数据密集型、容器化应用的首要平台——宣布 Mesosphere DC/OS 1.11 的上市。最新版本支持边缘和多云计算运营，具有智能资源池、安排各种工作负载以及从单一管理界面管理动态分布式基础架构的新功能。在企业客户 [athenahealth](https://mesosphere.com/blog/dcos-athenahealth/?partnerref=press-release) 和 [Royal Caribbean](https://mesosphere.com/blog/royal-caribbean-real-time-microservices/?partnerref=press-release) 的需求推动下，DC/OS 独特地自动化了底层基础设施，以便团队能够更快、更高效地提供高价值服务，如个性化体验、机器学习和物联网应用。

德国电信集团创新部 SVP 产品部的 Thorsten Mueller 表示:“Mesosphere DC/OS 为实时决策引擎提供动力，使我们的数百万移动用户能够在蜂窝网络和 Wi-Fi 网络之间自动无缝切换，以获得最佳的客户体验。“我们很高兴看到 Mesosphere 继续使跨数据中心和多个云提供商同时运行容器化应用程序和开源数据工具变得更加容易。”

DC/操作系统 1.11 中的新功能包括一个新的统一控制平面，可实现无缝边缘和多云操作。这种一致的管理体验，无论是在内部还是在边缘，都支持业务连续性、灾难恢复和云爆发功能。DC/操作系统 1.11 极大地简化了混合云和多云操作的部署和管理:与其他解决方案不同，DC/操作系统可以跨越多个云环境，因此工作负载可以自动部署到云 X 或云 Y。DC 操作系统上的生产 Kubernetes 即服务现在也可以通过一次点击获得，允许运营团队部署、扩展和升级 Kubernetes。该版本还增加了多层安全功能，以帮助保护整个应用程序堆栈，包括数据管道。

Moor Insights and Strategy 副总裁兼高级分析师瑞德·迪林厄姆(Rhett Dillingham)表示:“在急于实现堆栈现代化的情况下，企业公司有时会首先求助于公共提供商，以高昂的价格(包括资金和技术价格)获得“即服务”功能，因为在这些服务上开发的任何应用程序都与专有 API 相关联。“DC/操作系统不仅支持这些相同的数据服务，而且该平台还允许企业自由选择基础架构的任意组合，包括公共云、私有云或数据中心，实现真正的弹性扩展。”

“正如我们从全球 1000 强公司的客户群中看到的那样，企业面前有一个巨大的机会:控制他们的数据，这是企业最大的资产，并将其转化为推动利润和增长的洞察力和行动，”Mesosphere 首席执行官兼联合创始人 Florian Leibert 说。DC/操作系统提供了支持实时数据驱动应用的平台，如联网汽车、个性化体验和机器学习等应用，所有这些都具有符合您要求的合适基础设施。"

**边缘和多云操作**

DC/操作系统 1.11 能够将云、数据中心和边缘计算基础架构的任意组合整合到单个逻辑资源池中，并从统一的用户界面智能地随时随地调度工作负载。运营商可以专注于他们需要的服务，而不是底层基础设施。

DC/操作系统 1.11 中的新功能支持以下功能:

*   **边缘和多云联盟**:单个 DC/操作系统界面可以链接到多个集群，以实现一致的管理。DC/操作系统群集还可以扩展到本地节点之外，这意味着远程办公室或边缘基础架构可以占用最少的空间。
*   **业务连续性和灾难恢复**:使用容错域提供高可用性服务，使服务能够抵御机架、可用性区域甚至云区域内的中断。
*   **云爆发**:从区域数据中心或公共云中轻松添加或删除本地集群的远程容量，以适应快速需求高峰并优化基础设施利用率。

**Kubernetes 即服务**

DC/OS 使得在任何基础设施上建立和运行一个纯粹的、开源的、生产就绪的 Kubernetes 集群变得轻而易举。只需轻轻一点，DC/OS 就能自动完成设置安全且高度可用的 Kubernetes 集群所需的 20 多个不同步骤和许多小时的工作。在不中断任何服务的情况下进行纵向扩展、横向扩展和升级也是如此。DC/操作系统 1.11 通过了云本地计算基金会最新发布的 Kubernetes 1.9 的认证。由于 DC/OS 有一个模块化的架构，并使用一个纯开源的 Kubernetes 实现，最新版本的 Kubernetes 将总是很快在 DC/OS 上可用。

**增强的安全性**

数据丰富的应用程序有许多组件，保护所有这些组件可能很困难。容器化的微服务是通过设计动态调度、发现、负载平衡、终止和重启的，这进一步加剧了安全挑战。

DC/操作系统 1.11 为数据服务增加了新的安全层，简化了法规遵从性。首先，传输中的敏感信息现在已经加密。其次，DC/OS 提供了数据服务与通用认证、授权和访问控制机制的集成，如 Kerberos、LDAP 和 Active Directory。此外，DC/OS 1.11 改进了机密管理，授权应用程序使用该管理来共享敏感信息。还包括对层次结构和多团队隔离的新支持，使管理哪些秘密可以被应用程序或团队访问变得更加容易。

**可用性**

中间层 DC/OS 1.11 现已在 https://dcos.io/install/发布。通过访问 Mesosphere 的 [DC/OS 1.11 发布博客](https://mesosphere.com/blog/dcos-1_11-overview/?partnerref=press-release)或注册参加即将到来的[网络研讨会](https://event.on24.com/wcc/r/1597916/3164F4235F9AB067E321578EAD8EA9C3?partnerref=press-release)了解更多信息。

**关于中间层**

Mesosphere 正在引领企业向分布式计算和混合云转型。中间层 DC/OS 是构建、部署和弹性扩展现代应用和大数据的首要平台。DC/OS 使得在你自己的硬件和云实例上运行容器、数据服务和微服务变得容易。Mesosphere 由 Airbnb 和 Twitter 的超大规模基础设施设计师以及 Apache Mesos 的联合创始人于 2013 年创建。Mesosphere 的总部设在旧金山，在纽约也有办事处；德国汉堡；还有北京。中间层投资者包括 Andreessen Horowitz、Hewlett Packard Enterprise、Khosla Ventures、Kleiner Perkins Caufield & Byers 和微软。