# VMware 旨在提高应用程序安全性

> 原文：<https://devops.com/vmware-aims-advance-application-security/>

大多数与维护 IT 安全相关的任务都假定 IT 安全专业人员应该发现并消除对应用程序的所有潜在威胁。在本周举行的 [VMworld 2017 大会](https://www.vmworld.com/en/us/index.html)上，VMware 正试图通过将 IT 安全专业人员的工作重点放在已知产品上来彻底改变 IT 安全的概念。

VMware 安全产品高级副总裁 Tom Corn 表示， [VMware App Defense](https://www.vmware.com/company/news/releases/vmw-newsfeed.VMware-Transforms-Security-for-Applications-Running-on-VMware-vSphere(R)-Based-Virtualized-and-Cloud-Environments.2184703.html) 采用机器学习算法和 VMware 从其管理控制台和运行应用程序的主机收集的数据来确定哪些元素构成了应用程序工作负载，而不是追逐所有可能对应用程序产生负面影响的潜在坏事。这些元素会与首次部署工作负载时创建的清单进行比较，如果它们被更改，VMware App Defense 将调用预加载的事件响应例程库，以使用 VMware 网络虚拟化软件来实施策略。VMware App Defense 从主机收集的数据是通过将代码插入内核而不是部署代理软件来完成的。

Corn 表示，VMware App Defense 独一无二地为 DevSecOps 团队提供了对运行在 VMware 之上的客户操作系统环境的可靠遥测。IBM 将把 VMware App Defense 收集的遥测数据输入其安全分析软件产品组合，最终这些数据将被输入 IBM Watson 认知计算平台，以生成应用安全建议。承诺支持 VMware App Defense 的其他供应商包括 VMware 姐妹公司 RSA 和 SecureWorks，以及 Carbon Black 和 Puppet。

Corn 说，从长远来看，VMware 希望能够将这种能力应用到任何连接到 VMware NSX 虚拟网络覆盖的生产环境中。

尽管 VMware 应用程序防御可能很有吸引力，但 Corn 指出，IT 组织不应试图煮沸 IT 安全海洋。相反，他们应该专注于目前正在开发的新应用程序。否则，管理由数千个微服务组成的数百个应用的安全策略以及通过微分段网络覆盖进行通信可能会过于复杂，难以管理。

一段时间以来，VMware 一直在论证采用 NSX 来利用微分段来限制数据中心内东西向流量的流动。这种想法是，如果一个节点受到恶意软件的攻击，它只能与参与虚拟网络同一微段的节点共享该恶意软件。VMware 现在扩展了这一理念，在应用程序堆栈上提供了更高的可见性。

VMware App Defense 的定价为每 CPU 每年 500 美元，VMware 希望这会吸引更多的 IT 安全专业人员推荐部署其堆栈，而不是任何其他可用的选项。IT 运营团队和网络安全专业人员能在多大程度上影响开发人员朝着这个方向发展还有待观察。但 VMware 应用程序防御确实实现了它的承诺，开发人员很可能会欣赏不必花太多时间来防御现有应用程序，而不是编写新的应用程序。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)