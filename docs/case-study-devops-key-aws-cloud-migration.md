# 案例研究:DevOps 是 AWS 云迁移的关键

> 原文：<https://devops.com/case-study-devops-key-aws-cloud-migration/>

### *DevOps practices 将这家 SaaS 公司迁移到 AWS 的时间减半*

总部位于澳大利亚的 Whispir 提供通信应用服务。产品和运营负责人乔纳森·斯威夫特(Jonathan Swift)表示，其目标之一是尽快将产品送到用户手中，这需要开发、运营和产品人员共同努力。

Whispir 以前从一个协同定位数据中心运营，这种模式随着其国际扩张而延续。但是运行这些系统所需的时间和精力对于这样规模的组织来说并不划算，所以该公司主要转向了 AWS。一些客户面临的治理问题迫使公司仍然在某些地理位置运行自己的系统。

在这个过程中，“[我们]了解了很多关于我们的应用程序以及如何让它为云做好准备，”Swift 说。“云不是免费的，云也不便宜”，如果软件构建不正确，它可能比将服务器放在协同数据中心更昂贵。

例如，充分利用物理服务器是有意义的，因为它在很大程度上是固定成本。但是在云中，你使用的资源越少，花费就越少。

## 危机导致价格飙升

另一方面，Whispir 的许多业务都是以危机为中心的(例如， [Caltex 在悉尼的 Kurnell 炼油厂使用 Whispir 来发送紧急消息)，并且它需要一定的时间来增加额外的实例来处理消息量的激增。“这是一个真正的挑战，”斯威夫特说。](http://www.whispir.com/stories/case-studies/caltex)

这些危机沟通客户希望 Whispir 有足够的资源来满足突发需求。对于协同定位的硬件来说，这是一个昂贵的提议，而 Ccloud 资源可以快速扩展，尽管不是即时的。

季节性必须考虑在内。一个相对可预测的危机信息驱动因素是澳大利亚的森林火灾季节。不幸的是，这与圣诞节重叠，圣诞节是营销信息的高峰期。因此，Whispir 计划在火灾季节以正常基线容量的 200%左右运行。这可以通过云基础设施轻松实现，Swift 在本文中将云基础设施描述为“一件美好的事物”。

一些组织害怕多租户环境。在 AWS 上建立专用实例的能力是 Whispir 可以提供的一个很好的特性，尤其是对金融行业的客户。

该公司的 DevOps 实践一直专注于协同定位环境，因此即使在迁移到 AWS 后看板仍然“对我们非常有用”，一些以前的选择也必须重新考虑。特别是，需要新的监控工具来应对云固有的弹性，因为关注点从硬件扩展到了整个堆栈。

选择的工具包括用于趋势分析的 [Zabbix](https://www.zabbix.com/) 开源监控平台和 [Sumo Logic](https://www.sumologic.com/) 。

今年早些时候，Whispir 将其所有澳大利亚客户转移到“纯 AWS”环境中。Swift 说，有一些很好的迁移工具，“但并不像你想象的那样简单或无缝。”他建议将此类项目所需时间的初步估计增加一倍。

有一些令人讨厌的意外:AWS 第一个月的账单“巨大”,花了几个月才确定原因，即使有 AWS“真正有益”的高级支持服务的帮助。

必须考虑不同管辖区的安全要求，更新各种程序以确保新的云环境合规。例如，当一个物理系统退役时所需要的过程是很好理解的，但是如何将它们转化到云环境中呢？一个具体的例子是，内部存储设备可以在达到其生命周期时被销毁，但在云中，这在很大程度上取决于提供商的控制。

## 避免锁定

但 Swift 警告称，“挑战在于不要把自己局限于”某个特定的云提供商。对于运行混合云/内部环境的 Whispir(没有云提供商在新西兰提供合适的陆上设施，并且 Whispir 在新加坡安装的硬件太新，无法被 IaaS 取代)，这是一种要求，而不是一种战略选择。

Whispir 会避免使用 AWS 特有的特性，这些特性会使平台更容易使用，更难摆脱，尽管使用特定于提供商的工具集可以节省大量成本。

Whispir 正在关注 Azure——“伟大的工具，伟大的合作伙伴，伟大的生态系统，”Swift 评论道——并可能在 18 个月左右迁移到微软的云。

一个特别的优势是 Azure Stack 可以在私有硬件上运行，如果 Whispir 决定进入微软 Azure 不存在的市场，这可能是有用的。

无论哪种方式，目的都是尽可能实现百分之百的云计算。

## “基础设施即代码”意味着运营能力更强

他观察到，向云的迁移使得 Whispir 的操作人员更加强大。基础设施即代码的概念允许快速部署，使运营部门能够为产品开发做出更大贡献，降低风险，并使公司能够更好地响应市场。

此外，由于所涉及的延迟和依赖性，处理内部硬件在很大程度上仍然是瀑布式的。但是转向 IaaS 意味着基础设施问题可以轻松地放在看板模型中。

IaaS 还意味着各种与网络相关的任务消失了，但取而代之的是其他问题。例如，Whispir 使用的一些外部服务(例如，短信网关)需要使用来自已知 IP 地址的 VPN 连接，但对于云基础设施，您最多可以指定一个地址范围。Whispir 的短期解决方案是通过 co-lo 中心的特定服务器路由此类连接，从长期来看，它找到了限制较少的提供商。

Swift 表示，如果没有 DevOps，从 co-lo 迁移到云将“极其困难”。他指出，这至少需要两倍的时间，而且该公司将无法像现在这样良好地运行混合环境。

他说，没有 DevOps，“我们不可能如此成功”。

斯蒂芬·威瑟斯