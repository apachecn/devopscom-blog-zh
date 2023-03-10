# DevSecOps:策略管理的现实

> 原文：<https://devops.com/devsecops-realities-of-policy-management/>

策略管理对于扩展云环境至关重要，也是安全开发运维实践的关键。它使组织能够管理保护云环境的策略，确保 Kubernetes 配置的安全性，并实现对公司整体安全状况的持续监控。

事实上，IDC 2020 年的调查发现 云 [中 67%的漏洞](https://cts.businesswire.com/ct/CT?id=smartlink&url=https%3A%2F%2Fwww.idevnews.com%2Fstories%2F7376%2FIDC-Study-Finds-Cloud-Data-Breaches-Impact-80-of-CISOs&esheet=52568428&newsitemid=20220126005115&lan=en-US&anchor=67%25+of+breaches+in+the+cloud&index=3&md5=db50672fea703b57bf441a3d6ae53b02) 是由错误配置的应用程序或基础架构引起的， 包括 一些业界最大的漏洞，如[万豪的第二次漏洞](https://threatpost.com/millions-guests-marriott-data-breach-again/154300/)。

对此，第一份 [策略管理状态报告](https://info.nirmata.com/the-state-of-cloud-native-policy-management-2021) 由 Nirmata 和 CNCF 项目[Kyverno](https://kyverno.io/)的创建者透露，云原生环境中近 50%的用户现在已经采用了某种类型的策略管理解决方案。这一跨越生产云原生环境的主流采用的临界点，使得 DevOps 团队审视其实践并通过内置的管理策略消除漏洞来简化和操作化其 Kubernetes 堆栈中的策略管理变得至关重要，而没有学习复杂策略语言的障碍。但这种广泛的采用也承认，组织最终意识到需要将注意力、投资和创新放在解决安全性和合规性差距上，因为他们通过适当的[DevSecOps](https://devops.com/what-is-devsecops/)实践和工具采用 Kubernetes，以便构建的应用程序可以增强业务。

要自信地在 Kubernetes、开发团队需要接受这些 开发团队 现实，并有效地应用策略管理。

### 定制产生安全隐患

Kubernetes 可以高度定制，但是 DevSecOps 团队需要随着组织的扩展了解每个集群中发生的情况，以确保应用程序的可靠性和安全性。对容器的利用(包括恶意软件安装、密码挖掘、主机访问和权限提升)为更多安全漏洞提供了机会。它们可以存在于 Kubernetes 集群中的映像、生产可访问的容器注册表、失败的构建和第三方准入控制器中。

为了解决在 Kubernetes 上运行的应用程序的这些风险，用三个 A 来保护您的环境是很重要的:认证、授权和许可。 这应该在集群层完成，这样可以安全访问被授权执行特定操作的认证实体 。 实现这一目标的一种方法是通过策略管理。事实上，根据 [状态的策略管理报告](https://info.nirmata.com/the-state-of-cloud-native-policy-management-2021) ， 策略管理的顶级用例是针对 Kubernetes 准入控制(31%)。当请求被授权时，制定一个策略可以确保请求通过另一组过滤器。例如，由于配额或其他更高优先级的请求，许可控制器可能会拒绝授权的请求。除了验证之外，准入 webhooks 还可以改变传入的请求，作为在到达 Kubernetes API 服务器之前处理请求对象的一种方式。

### 配置问题

容器映像、名称空间、运行时特权、永久存储和控制平面，以及与最佳实践不兼容的网络策略，是错误配置和风险暴露的来源。正是这种更大风险暴露的可能性，使得配置管理成为采用策略管理的关键驱动因素。在 Nirmata 的政策管理状态报告中，it 在目前采用的安全工具中排名第三，在组织未来采用的计划中排名第四。

有几种方法可以定义安全策略来保护云环境。策略可用于审计目的，拒绝 pod 创建或改变 pod 并限制其功能。默认情况下，pod 可以从任何来源接收流量，并向任何目的地发送流量。网络策略允许您限制 pod 的入口和出口访问。网络策略通常转化为防火墙规则。

### 缺乏足够的授权

云认证允许授权用户通过基于云的服务提供的认证安全地访问存储在云中的信息。在策略管理状态报告中，主要调查结果显示，目前超过 24%的受访者正在使用策略管理等工具对访问应用的用户进行身份验证。随着数据盗窃成为增长最快、代价最大的 网络犯罪 ，处理信息的能力和强大的授权措施需要成为 DevSecOps 最佳实践的一部分。

在 Kubernetes 环境中，当一个用户请求被认证时，它会通过一个 [授权工作流](https://kubernetes.io/docs/reference/access-authn-authz/authorization/) 来决定该请求是否应该被批准。它根据所有策略评估请求属性，并允许或拒绝请求。主要的授权机制是基于角色的访问控制(RBAC)。每个经过身份验证的请求都有一个 HTTP 动词，如 GET、POST 或 DELETE，经过身份验证的实体有一个角色，可以允许或拒绝请求。其他授权机制包括基于属性的访问控制([【ABAC】](https://kubernetes.io/docs/reference/access-authn-authz/abac/))[节点](https://kubernetes.io/docs/reference/access-authn-authz/node/) 授权和 [webhook 模式](https://kubernetes.io/docs/reference/access-authn-authz/webhook/) )。

随着安全在应用生命周期中进一步左移的趋势加速，开发人员需要主动承担起责任，这就产生了对自动化的更高要求。快速发布会使应用程序暴露于许多漏洞之下，增加了违规的风险。使用 DevSecOps ，组织可以通过将安全性和合规性转移到左边来转变开发管道，使开发人员能够在每次提交之前检查代码。通过这样做，可以在开发过程中识别和修复安全和法规遵从性漏洞，从而使组织避免高成本和潜在违规的负面影响。

毫无疑问，Kubernetes 很复杂，很难采用。除此之外，开发领域充斥着各种工具，对工程师的要求也越来越高。这些转变正在改变开发人员的传统角色，为组织留下了一个缺口，以充分利用开发运维。但是，通过采用一种安全、持续、迭代的方法，其中还包括策略管理，公司可以降低其云环境的风险和暴露程度。一个组织的 DevOps 实践越成熟，通常安全性和合规性实践就越强——它们彼此相关。最具创新精神的公司在 DevSecOps 接受策略管理作为发展的必要条件，并采用某种级别的策略管理最佳实践。借助策略管理、安全性和合规性最佳实践等正确的实施工具，组织可以在敏捷和开发运维方面保持高效，同时遵守关键的上线期限，这在这个快节奏的业务环境中是不容错过的。