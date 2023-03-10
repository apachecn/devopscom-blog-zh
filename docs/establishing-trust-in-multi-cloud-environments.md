# 在多云环境中建立信任

> 原文：<https://devops.com/establishing-trust-in-multi-cloud-environments/>

现代应用正在将企业转变为数字创新工厂。然而，现代应用程序的分布式和复杂性使得组织很难在多平台、多云计算环境中保持信任和合规性。

虽然 [Kubernetes](https://kubernetes.io) 是当今应用平台的标准，但每个云服务提供商(CSP)都有不同的基础设施即服务(IaaS)或他们自己的平台即服务(PaaS)产品，具有不同的功能和 API。不仅这些 API 不兼容(Kubernetes 除外，如果没有使用供应商扩展的话)，而且每个基础设施和平台都是在孤岛中处理和管理的。这些孤岛充当一个隔离的、非重叠的管理边界，  防止微服务之间的跨边界可见性和信任。  这使得企业更加难以了解和持续修正他们跨云和平台的安全状况，从而使他们更容易受到攻击。

为了解决这个问题，组织正在将企业安全控制扩展到云环境。问题是，应用程序团队和安全团队传统上有相互竞争的目标，即敏捷性与风险和控制，而安全运营没有与应用程序运营同步发展。这就造成了团队之间的摩擦，迫使应用[操作团队](https://devops.com/?s=IT+operations)做出选择:

1)减缓应用交付和运营速度，以降低风险并错失云计算或  的变革性优势

2)在不考虑安全性和合规性的情况下，继续尽快开发和发布应用程序。

两者都不是好的选择。为了释放在多平台和多云环境中运行的现代应用程序的力量，组织需要找到一种方法，以用户期望的速度在整个软件交付生命周期中无缝集成安全性。

## **将零信任整合到应用交付周期中**

在多云世界中保护应用的关键是零信任。将零信任原则直接构建到现代应用程序中，使组织能够尽早发现威胁，减少攻击面，并将安全功能与应用程序堆栈的其余部分一起提供，而不管底层的应用程序平台和云堆栈。

在这个用例中，零信任的关键组件之一是应用程序分段；换句话说，如何在不同的应用程序或应用程序的组件之间做出访问决策。零信任必须通过一种可扩展的模式，以提高应用访问的灵活性和敏捷性的方式，从任何用户或应用向任何应用*提供身份感知、自适应和按需访问*。**

应用程序分段必须提供给应用程序操作团队，以便他们可以将其作为另一个入口嵌入到他们的应用程序质量流程中。应用程序运营团队可以通过实施应用程序分段策略来实现这一点，这些策略通过丰富的动态属性来识别创建的工作负载。更多的内在/静态属性(IP、数字证书、名称空间、标签等。)和外在/动态属性(用户行为、工作负载行为、网络行为等。)越多，您的访问决策就越精细。

令人难以置信的是，今天的应用程序分段仍然是手动完成的。但是，随着数以百万计的事务在多个云环境中发生，一个人甚至一个团队都无法手动为每个工作负载分配策略。组织需要一种方法来以可扩展、透明和自动的方式提供零信任应用程序分段。

## **连接和安全平台**

做到这一点的方法是通过使用现代应用程序连接和安全平台。通过服务网格，基于属性的访问控制(ABAC)模型整合了多个第三方工具，这些工具提供了跨应用平台和多云环境的可见性和安全性。这种单一视图运营模式使应用程序团队能够自动、大规模地无缝、简单地协调跨多种云环境的安全服务。

不幸的是，通过微分段的精细策略管理增加了复杂性，这是安全性的大敌。突然之间，一个组织可能会发现自己有数以千计的策略，这些策略规定了不同的工作负载如何访问网络内部的实体并与之交互。这些策略需要不断更新和维护，这给应用程序和安全团队带来了巨大的难题。

部署工作负载时，相关联的策略会随之创建，并随着工作负载在环境中移动，直到工作负载达到其生命周期的终点并退役。随着应用程序随着时间的推移而运行，它们被其独特的行为所表征。这种运行时安全特性允许策略被自动选择并直接应用于工作负载。

然而，要让服务网格在多云环境中工作并实现安全应用，it 需要遵循零信任原则，而不增加复杂性，也不减缓敏捷交付周期。你可以这样做:

1.  **基线信任 :** 一个现代的 app 连接和安全平台应该具备原生的可观察性和自我发现能力，比如能够自动发现 API，对 API 进行编目，生成基于 OpenAPI 标准的 API 文档。现代的应用程序连接和安全平台应该能够持续基线化应用程序行为，并检测异常的应用程序行为。这需要对未知攻击和零日攻击发出警报，尤其是敏感数据的泄露。
2.  **建立信任 :** 立即定义应用程序不同部分的互连性需求至关重要。这种明确的意图声明通常由应用程序团队在作为 CI/CD 管道的一部分部署应用程序的过程中手动完成。另一种选择是在应用程序的测试阶段自动发现连接意图，并允许服务网格识别和记录微服务 API 之间的通信流。这些是应用程序分段策略的基础。
3.  **实施信任 :** 还必须有一种机制来自动应用适当的应用程序分段策略，以实现应用程序按预期运行所需的通信。在微服务模型中，应用程序的不同部分动态地上下旋转，以使应用程序能够按预期运行。控制可访问性的应用程序分段策略也要适应这些变化，这一点至关重要。这是通过服务网格控制平面完成的，该控制平面与应用平台交互以收集工作负载的清单。
4.  **动态调整信任 :** 当应用程序随着时间的推移而运行，并且客户端与它们进行交互时，它们被表征为一种行为。在这种情况下，安全行为。观察这种行为可以通过各种运行时分析工具来完成，这些工具可以检测流程、容器、网络和用户行为以提供安全上下文。然而，为了维护信任，需要有一种方法通过服务网格来集成这些工具，以创建单一的事实来源。
5.  **将信任模式扩展到边缘 :** 应用程序还会与 Salesforce 或 SAP 等软件即服务(SaaS)平台以及数据中心之外的其他应用程序进行交互。理想情况下，服务网格/零信任应用程序细分模型可以与云中的其他安全解决方案集成，如安全访问服务边缘(SASE)、安全 web 网关(SWG)、云访问安全代理(CASB)和其他零信任安全组件。这标准化了在数据中心、多个云服务提供商、SaaS 平台和 web 应用之间建立信任的流程，从而确保整个组织的一致性安全性和合规性。

现代应用通过实现敏捷性和实时决策正在改变企业的工作方式，但除非应用团队与安全团队合作保护用户、数据和应用，否则它们永远不会发挥出全部潜力。很明显，组织需要一个发展的安全模型，应用程序团队可以使用它来无缝地建立信任，并协调跨多云、多平台环境的应用程序分段。服务网格可以提供建立和持续评估信任所需的可见性和控制。