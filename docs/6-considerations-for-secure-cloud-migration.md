# 安全云迁移的 6 个注意事项

> 原文：<https://devops.com/6-considerations-for-secure-cloud-migration/>

***规划安全的云迁移？这里有一些技巧可以帮助你顺利完成这个过程。【T2*** 

地球上四分之三的组织都有某种形式的云存在。根据 [2018 年 IDG 调查](https://www.idg.com/tools-for-marketers/2018-cloud-computing-survey/)，77%的企业现在至少有一个应用程序或其企业计算基础架构的一部分位于云中。此外，报告发现，企业计划在云应用、平台和服务上平均投资 350 万美元。

展望未来，依赖于技术的行业(包括制造业、高科技和电信)的管理层越来越倾向于实现 100%云支持。这也意味着，除了那些从完全基于云的基础设施起步的新公司，大多数组织目前要么积极地将其基础设施和/或应用程序迁移到云；尝试在本地物理网络和位于公共云中的一个或多个网络之间架设业务流程、应用和工作流的桥梁；或者正在计划这样做。

这些组织面临的挑战之一是跨本地和基于云的资源创建一致的安全态势。事实是，并不是所有的安全策略都可以在多云环境中成功无缝地实施，尤其是在使用各种工具时。这是因为大多数供应商解决方案要么不支持所有主要的云平台。对于那些支持的，许多不支持利用云资源描述的原生云集成。随着工作流和应用程序在不同的云环境之间移动，这可能会给实施一致性和策略定义带来挑战，从而导致可被利用的安全漏洞和盲点。

## 成功将安全性迁移到云

在不扩大攻击面或增加安全开销的情况下，将基础架构、应用程序或服务迁移到云需要精心准备。首先要明白，任何基于云的部署，无论是构建新的基础架构还是构建新的应用程序，都需要业务线、IT 和安全团队之间进行清晰的沟通。如果没有关于业务需求和目标的明确沟通以及对相关威胁的坦诚讨论，组织将面临一系列新的风险，包括针对云资源的拒绝服务攻击、云恶意软件注入、web 应用程序利用、云 API 攻击以及帐户或服务劫持。

成功的云迁移还需要成功地将安全性迁移到云，使组织能够部署和管理跨整个云计算基础架构的单一、一致的安全框架。

以下是每个组织在规划云采用或云迁移策略时应该考虑的六个步骤:

### **在云迁移之前确定您的安全基准**

太多的组织拥有围绕孤立的安全设备、分散的管理和不一致的安全策略应用构建的安全架构。

如果您的组织是这种情况，您将需要从控制您的安全蔓延和实施中央安全策略开始。一旦准备就绪，您需要问以下问题:

*   您知道您当前的安全状况及其对您未来业务目标的影响吗？
*   您是否为当前和未来的环境制定了适当的策略和程序？
*   您是否对云将如何改变您的安全模式进行了差距分析？
*   基于云的分布式网络对风险管理有什么影响？

### **规划带宽需求**

您需要建模并了解数据流和带宽要求，以确保您的安全解决方案能够满足性能要求，尤其是需要通过 VPN 隧道的延迟敏感型服务。

### **了解合规问题**

对于在云上处理和存储的数据，以及在不同云和物理网络环境之间移动的数据，您必须满足哪些要求？在您开始构建或采用任何种类的云程序之前，咨询您的法律团队是至关重要的。

### **提供高可用性和灾难恢复**

在解决了安全问题之后，大多数组织在考虑云解决方案时最大的担心是基于云的资源的可用性。您还需要认识到是否需要动态扩展，以及您的安全解决方案是否能够满足新的性能要求。最后，您需要考虑诸如流对称和负载平衡之类的事情，尤其是对于遗留应用程序，以保持可用性、性能和保护，即使在利用动态的基于云的服务时也是如此。

### **在正确的位置应用正确的安全性**

云安全需要的不仅仅是在云基础架构的外围放置一个防火墙。根据运行的应用程序和使用的服务，将需要应用广泛的安全解决方案。下一代防火墙(NGFW)解决方案是最常见的安全工具，但也经常需要其他解决方案，包括 web 应用防火墙(WAF)、入侵保护或检测服务(IPS/IDS)和云访问安全代理(CASB)。

### **建立生命周期管理框架**

确保安全解决方案和策略实施之间的一致性至关重要，尤其是当它们跨越多个环境时。选择安全工具时，不仅要考虑它们在特定云平台中本地运行的能力，还要考虑它们在整个安全策略生命周期中与部署在其他环境中的姐妹解决方案无缝互操作的能力。这包括一致的安全变更策略、动态配置和扩展、单点管理(包括与中央 ITSM 解决方案和中央日志收集的集成)以及相关性。

## 不要让云的便利欺骗了你，让你走上了安全捷径

采用云服务就像点击一个链接一样简单。此外，添加新的基于云的基础设施虽然复杂得多，但比构建物理基础设施要容易得多。但这可能看似简单。太多的组织不得不为匆忙采用新的云解决方案付出代价，而没有仔细考虑与安全性相关的挑战。这些问题包括向网络中引入新的攻击媒介，对新的基于云的威胁毫无准备，或者因未能充分准备新的合规性考虑因素而被罚款和处罚弄得措手不及。

在您开始构建新的云基础架构、平台或服务之前，仔细准备可以节省您的时间、金钱和声誉，并使您能够在当今新的数字市场中有效竞争。

— [利奥·科恩](https://devops.com/author/lior-cohen/)