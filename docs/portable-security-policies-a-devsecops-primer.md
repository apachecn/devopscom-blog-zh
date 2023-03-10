# 可移植安全策略:DevSecOps 入门

> 原文：<https://devops.com/portable-security-policies-a-devsecops-primer/>

保护关键数据和应用程序在任何情况下都是一项挑战，但当资源驻留在云中时，这项挑战尤其艰巨。如今，大多数组织都在云中运行很大一部分工作负载，这增加了安全问题的复杂性-安全团队无法完全控制云环境，但负责保护工作负载和运行在那里的应用程序。

网络罪犯正在利用这种情况。他们在工作中变得越来越有侵略性和独创性，利用了在共同责任模式下谁对安全的哪些方面负责存在混淆的事实。云提供商的安全产品和能力之间的差异加剧了混乱。很简单，在大多数情况下，云提供商负责云的安全，消费者负责云中的安全，这意味着安全和网络团队仍然需要确保其组织的工作负载和应用程序不受恶意软件或其他篡改的影响。

为了实现这一目标，安全和网络团队不能仅仅依靠防火墙、威胁检测和漏洞修补来保护重要的数字资产。由于云的动态特性，为传统数据中心开发的安全工具无法有效保护云中的工作负载。安全和网络团队必须重新思考他们的方法。

不幸的是，许多组织仍然依赖于旧的、无效的策略—进一步强化边界，投资于额外的威胁检测，并添加侧重于识别而不是预防的新工具和控制。这种安全方法有其存在的理由，但一旦恶意行为者站稳脚跟，它无法阻止他们在网络中横向移动，这使得云托管的应用程序和工作负载极易受到攻击。

相反，安全团队需要在云环境中启用[零信任](https://devops.com/simplify-devsecops-with-a-zero-trust-approach/)，默认情况下将所有内部通信视为不可信。对于零信任，只有经过授权的应用程序和服务才被允许发送和接收通信，并且只能以最小特权原则控制的特定方式进行。

## 第二层

传统工具无法有效实现云中的零信任，因为安全和运营团队管理云开放系统互联( [OSI](https://en.wikipedia.org/wiki/OSI_model) )模型所有层的能力非常有限。具体来说，基础设施即服务(IaaS)环境中缺乏第 2 层控制，这使得为离散网络开发的工具对于锁定端口以及控制或审查 IP 地址几乎毫无用处。

即使组织设法在云中实现这些工具，它也无法提供阻止恶意横向移动所需的粒度级别。例如，当内部工具重新用于云环境时，它们通常依赖子网来定义通信的边界。因为云子网旨在处理弹性工作负载，所以它们需要比内部环境中的大得多。因此，云工作负载的暴露程度超过了必要的程度。

当依赖传统工具时，将工作负载和应用安全地迁移到云环境是一项巨大而繁琐的工作。使工作负载可移植且安全的最佳方式是将工作负载保护与底层基础架构分离。通过这种方式，组织可以确保在内部应用的任何策略都可以迁移到不受信任的云环境，而不存在映射变化的网络地址、编写策略异常或在此过程中失去精细控制的复杂性。

将工作负载保护与网络分离需要放弃基于网络地址的方法，转而采用基于身份的方法。通过使用工作负载的不可变属性，安全团队可以为应用和服务创建加密身份，然后可以使用这些身份来确定允许发送和接收通信的内容。这种模型不仅提供了更强的安全性，而且无论应用程序位于何处，它都可以工作，因为当网络元素发生变化时，这些身份不会受到影响。更重要的是，它们可以被构造成容许升级。通过构建基于身份的策略，安全团队可以围绕应用程序创建微型参数，无论工作负载走到哪里，这些策略都会在应用程序每次尝试通信时验证跨边界的通信。

实施与网络无关的策略不仅仅会加强安全性。软件开发人员也从中受益。没有将应用程序语言转换为网络语言的障碍，开发人员可以在任何有利于他们工作流的环境中构建软件和应用程序，同时定义策略来保护他们的工作。一旦软件构建完成，他们就可以安全地将成品部署到生产环境中，即使它由第三方托管。

任何组织都不应该为了受益于云和短暂的自动扩展容器所提供的效率而牺牲安全性。构建基于身份的策略，实现零信任并独立于底层网络，确保公司永远不必考虑这种取舍。

汤姆·希克曼