# SASE 对开发团队意味着什么

> 原文：<https://devops.com/what-sase-means-for-devops-teams/>

您可能听说过安全接入服务边缘(SASE)这个缩写词，很难忽视它对技术行业的影响。SASE 是在混合环境中实现联网的一种很酷的新方法，最重要的是它将安全性融入到网络结构中。简单地说，当你插入时，默认情况下你是安全的。

SASE 将对 DevOps 团队最关心的两个领域产生特殊影响:

1.  [**云安全**](https://devops.com/cloud-security-requires-shared-responsibility/) —SASE 有潜力改变我们在多云中实施安全的方式，并将其与中央数据中心的安全统一起来。
2.  **[**DevSecOps 采用**](https://devops.com/what-is-devsecops/) —SASE 可以使 DevSecOps 更容易采用，并可能成为全球分布的 DevSecOps 团队的基本基础设施。**

**我们先来了解一下萨塞兽的解剖，了解一下它在未来的岁月里会对 DevOps 产生怎样的影响。**

## **什么是 SASE？**

**[SASE 是一种云服务](https://www.catonetworks.com/sase/) ，它扩展了网络和安全功能，以支持混合组织的动态、安全访问需求。**

**SASE 将 WAN 功能与网络和安全功能相结合，如防火墙即服务(FWaaS)、[零信任网络访问](https://securityboulevard.com/?s=zero+trust+network+access) (ZTNA)、安全网络网关(SWG)等。**

**SASE 平台捆绑了多种安全功能，包括 SD-WAN 和 SWG、CASB、ZTNA、FaaS 和 SaaS 等服务。这种多区域、多租户架构支持分布式远程工作人员。SASE 使用位于端点附近的存在点(pop)而不是数据中心的检查引擎。SASE 客户端向最近的 PoP 发送流量。**

**一个 [SASE 架构](https://www.catonetworks.com/sase/sase-architecture/) 的核心特征是:**

*   ****全球 SD-WAN**—专用 SD-WAN 主干网通过避开公共互联网来帮助减少延迟。**
*   ****分布式架构** —SASE 使用多个检查引擎在边缘检查流量并实施策略。**
*   ****云基础设施** —SASE 通过云提供服务，因此租户不必维护硬件和其他基础设施资源。这种方法具有可扩展性和成本效益。**
*   ****基于身份的访问**—访问控制使用身份标记，如用户的位置和设备。**

## **SASE 采用驱动因素:组织为什么需要它？**

### **成本降低**

**使用来自多家供应商的物理和虚拟设备非常麻烦且成本高昂。SASE 使组织能够用单一的云原生解决方案取代这种不同的模型。组织可以使用 SASE 通过一个提供商而不是几个提供商交付更多的技术和服务。因此，它消除了各种网络设备的成本，而 [通过减少运营云环境所需的资源和带宽，优化了云成本](https://spot.io/resources/cloud-cost/cloud-cost-optimization-15-ways-to-optimize-your-cloud/) 。**

### **边缘到边缘的安全性**

**SD-WAN 是 SASE 不可或缺的组成部分，提供主动-主动故障转移和 WAN 优化等功能，可提高性能和网络弹性。SASE 解决方案基于 [安全自动化](https://www.mend.io/resources/blog/security-automation/) 的概念，具有全面管理的网络安全堆栈，通常包括 swg、下一代防火墙(NGFW)、下一代网络架构和入侵防御系统(IPS)。该模型有助于保护所有边缘，实现更好的网络可见性。**

### **数据保护**

**SASE 提供全面的数据保护体验，自动执行多个 DLP 流程，包括存储位置、数据使用和传输中的数据的数据发现和数据分类。它采用各种安全措施，如用户和设备身份验证，以便随时控制对数据和资源的访问。此外，SASE DLP 在整个网络中无缝部署保护策略。**

## **影响:SASE 将如何转变云安全体系**

**PaaS、SaaS 和 IaaS 等服务的出现鼓励组织允许远程工作。云支持分散的劳动力并简化业务流程，但它也使公司面临基于网络的威胁。许多组织将敏感数据存储在可在线访问的第三方处。**

**云安全堆栈很容易变成孤岛，团队成员不确定他们的职责，并且忽略了关键流程。由于安全团队使用多个安全系统，孤立的堆栈更加耗费人力，也更难跟踪。它还会产生警报疲劳，使识别威胁变得困难。**

**虽然员工大多在云中工作，但安全工作通常集中在数据中心。SASE 将重点转移到云，同时确保安全服务之间的无缝集成。**

**借助 SASE，单个提供商可以提供整个安全体系，确保其作为一个整体发挥作用。例如，SWG 使用威胁情报数据来阻止可疑流量，将未识别的文件发送到沙箱进行测试。安全团队可以从一个直观的界面管理整个堆栈。**

**大多数活动发生在边缘—SASE 使用身份驱动的方法保护边缘。它也是云原生的，确保无缝体验。**

## **影响:SASE 将如何促进 DevSecOps 的采用**

**SASE 为采用 DevSecOps 提供了以下优势。**

### **促成协作**

**SASE 有助于减少跨团队协作中的挑战。本质上，SASE 将网络安全与广域网优化相结合。现代 DevOps 团队在物理上是分离的，但必须一起工作，这要求团队成员之间有可靠和安全的连接。**

**DevOps 方法强调上市时间，因此 DevOps 团队寻找加速 [CI/CD](https://devops.com/?s=CI/CD) 周期的方法，并更快地推动发布。该过程的一个重要部分是减少 DevOps 团队对网络和安全团队的依赖。SASE 解决方案有助于优化性能和增强安全性，因此 DevOps 团队不必等待基础架构团队来配置资源。SASE 为 DevOps 团队提供了必要的控制和运营节奏，而不会影响安全性或性能。**

### **增强的网络**

**SASE 可以通过提供集成的故障转移和负载平衡功能来提高整体网络性能。DevOps 团队必须拥有可靠的连接，并且在部署新软件或修复错误时不能容忍中断。快速、可靠的应用性能是开发运维工作流的关键。**

**SASE 架构改进了网络，确保组织的边缘设备、云资源、数据中心和远程用户保持连接。DevOps 团队不必处理基础架构，因为它是自我修复、完全优化且安全的。如果某条线路出现故障或某条路径变得拥塞，该解决方案会自动切换到另一条路径。**

### **默认安全性**

**SASE 通过内置的安全功能保护 DevOps 项目。如果实施得当，它会将许多安全技术集成到网络堆栈中。DevOps 团队不用担心攻击者拦截敏感信息。每个安全服务共享相同的统一上下文，以提高可见性并填补传统安全架构中经常出现的缺口。SASE 减少了攻击者在单一架构中使用 NGFW、SWG、IPS、MDR 和防病毒服务所利用的漏洞。**

**SASE 可以保护内部应用程序及其交互，从而减轻 DevSecOps 团队的负担。运行在基于 SASE 的 SD-WAN 上的应用受益于零信任网络访问(ZTNA)和软件定义的边界(SDP)的额外保护。这些技术有助于确保应用程序和端点之间的所有交互都是安全的。**

**专有应用通常过于敏感，不能暴露在公共互联网上。SASE 通过混淆流量、使用 NGFW 保护所有入口点以及使用零信任网络架构限制访问来保护这些应用程序。它会持续检查所有内部应用程序流量中的网络安全威胁。**

## **结论**

**在本文中，我解释了 SASE 的基础知识，它将多个网络和安全解决方案打包到一个托管服务中。**

**SASE 为组织的核心基础设施带来了新的灵活性和敏捷性，并引入了设计安全的概念。我们并没有努力去“保护所有的东西”，而是正在向一个世界靠近，在这个世界中，我们组织运行的“网格”在默认情况下是安全的。这不会降低 DevSecOps 的重要性。但它将允许我们在一个安全、可控的混合环境中构建我们的应用和服务。**