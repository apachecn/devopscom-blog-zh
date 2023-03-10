# Aqua 3.0 引入了本地 Kubernetes 安全控制和自动化

> 原文：<https://devops.com/aqua-3-0-introduces-native-kubernetes-security-controls-automation/>

*最新版本基于当前的 Kubernetes 功能来增强安全性，进一步深化 Aqua 对云原生应用安全性的跨平台支持*

**马萨诸塞州波士顿——2018 年 3 月 7 日**—市场领先的基于容器和云原生应用安全平台提供商 Aqua Security 今天宣布推出其平台的 3.0 版本，该版本为基于 Kubernetes 的运行时环境提供了新的安全自动化和控制。新版本还引入了 120 多项附加功能，扩展了该公司端到端集装箱安全平台的功能，以满足当今多平台企业客户的需求。

Aqua Security 的技术宣传员 Liz Rice 指出:“Kubernetes 的采用率随着其功能的成熟和企业就绪性而不断增加。“随着企业安全技能的短缺，企业正在寻找利用 Kubernetes 来自动化部署和加速应用交付而不影响安全性的方法。这就是 Aqua 3.0 的意义所在”。

Aqua 3.0 基于 1.8 和 1.9 版本中引入的当前 Kubernetes 安全功能，在几个关键领域提供自动化的 Kubernetes 本地控制:

*   **Kubernetes-基于本地角色的访问控制:** Aqua 3.0 使客户能够利用 Kubernetes webhook 准入控制器来创建细粒度的用户访问控制角色和策略，控制对 kubectl 命令的访问，并将它们分配给特定的服务和节点，或者由 Aqua 的可扩展标记方案进行管理。
*   **Kubernetes-本机映像保证控制:**除了能够阻止未经批准的映像在单个主机级别上运行之外，Aqua 现在还可以防止 Kubernetes 在整个集群中运行未经批准的映像，从而提供一种更高效的机制，可跨大型部署进行扩展。
*   **Kubernetes-本地网络控制:** Aqua 的容器级防火墙现在使管理员能够根据 Kubernetes 名称空间、集群或部署来控制网络流量。这使管理员能够出于合规性目的实施网络分段，并限制跨群集和应用程序的攻击“爆炸半径”。
*   **CIS Kubernetes 基准测试:**基于 Aqua 的开源 [Kube-Bench](https://github.com/aquasecurity/kube-bench) ，该工具被社区广泛用于验证 Kubernetes 部署的安全状况，Aqua 现在将 CIS Kubernetes 基准测试与更新的 Docker CIS 基准测试相结合。自动检查可以每天运行，提供详细的报告，该报告也可以导出以符合要求。
*   **审核 Kubernetes 事件:** Aqua 的事件日志现在包括特定于 Kubernetes 的信息，如 pod 名称、类型、部署和命名空间数据，为合规性和取证提供了额外的可见性。

Aqua 的平台目前正被数十家全球 1000 强客户使用，为保护基于容器和云原生的应用程序提供了最全面的全生命周期解决方案，这些应用程序在本地或云中运行，并支持 Linux 和 Windows 运行时环境，以及最近宣布的 Pivotal Cloud Foundry 公共测试版。Aqua 平台推动了 DevSecOps 自动化，并为运行时应用程序提供了可见性和安全性，包括主机级和网络级控制。

Aqua 3.0 与 Kubernetes 1.8 或更新版本的实现兼容，可供现有 Aqua 客户使用。它通过了基于 Kubernetes 的流行部署的认证，包括谷歌 GKE、Azure AKS、Azure ACS、亚马逊 EKS 和 RedHat Openshift，并且是 Kubernetes 的技术合作伙伴。欲了解更多信息:

*   博客
*   网站页面
*   网络研讨会:保护企业 Kubernetes 1.8-1.9 部署

Aqua 3.0 还引入了许多其他新功能，包括对图像和主机的恶意软件扫描，对主机的漏洞扫描，以及对网络覆盖绒布、印花布、编织和 Contiv 的增强支持。此外，在 3.0 版本中，Aqua 推出了正在申请专利的 MicroEnforcer 技术，用于保护“零基础设施”容器即服务产品，包括 AWS Fargate 和 Azure Container Instances(ACI)——有关更多详细信息，请参见我们在此发布的配套公告。

**关于 Aqua Security**

Aqua Security 使企业能够从开发到生产保护其容器和云原生应用，从而加快应用部署并弥合开发运维与 IT 安全之间的差距。Aqua 的容器安全平台提供了对容器活动的全面可见性，允许组织实时检测和防止可疑活动和攻击。Aqua 平台与容器生命周期和流程编排工具相集成，提供了透明、自动化的安全性，同时有助于执行策略和简化法规遵从性。Aqua 成立于 2015 年，由光速创投(Lightspeed Venture Partners)、微软创投(Microsoft Ventures)、TLV 创投(Bernstein Partners)和 IT 安全领域的领军人物提供支持，总部位于以色列和马萨诸塞州的波士顿。欲了解更多信息，请访问[www.aquasec.com](http://www.aquasec.com)或关注我们的[twitter.com/AquaSecTeam](https://twitter.com/aquasecteam?lang=en)。