# 开发运维对 IT 运营管理的影响

> 原文：<https://devops.com/devops-impact-on-it-operations-management/>

DevOps 运动的大部分焦点是应用程序开发到部署周期，这是恰当的。当人们谈论 DevOps 的 IT 运营方面时，您会听到人们谈论 Puppet、Chef 和 Ansible 等 IT 流程管理工具，这些工具用于自动化软件和虚拟机的部署、更新和补救。然而，DevOps 被广泛认为不仅仅是一个过程，它是一种协作文化，通过自动化实现高质量的结果。因此，更多的 IT 学科正在研究如何将 DevOps 原则应用到他们的领域中。这些领域包括可归入 IT 运营管理(ITOM)的领域:网络工程和运营、灾难恢复和基础设施运营管理。这些规程和组织中的许多目前在传统的 IT 组织中高度孤立，并且工具套件来自当前强调 API 自动化之前的时代。有些人可能想知道这些 IT 领域是否能够适应和采用 DevOps。更恰当的问题可能是“IT 组织能承受不这样做吗？”

ITOM 是一个很大的话题，不可能在一篇文章中详尽阐述 DevOps 是如何影响它的。然而，我们至少可以从几个角度来看一看。第一个角度是考虑 DevOps 对运营管理职能领域的影响。ITOM 可以大致分为管理供应、容量、可用性和性能。其中，配置可能是 DevOps 影响最大的领域。这很有意义，因为如果没有基础设施和应用程序组件的自动化供应，将很难实现持续的流程，而这是 DevOps 团队的标志性实践。所有 IT 基础架构变得“软件定义”的趋势与这一调配自动化运动相一致。

一旦我们偏离了资源调配，DevOps 的覆盖范围就会变得更加稀疏。DevOps 的成功案例是应用性能管理(APM)。五年前，试图了解应用程序性能的工程师感到非常不满意。以至于出现了一个#监控混蛋迷因。从那时起，APM 已经显著地现代化，并深刻地向开发人员友好的方法发展。像 ELK stack(elastic search+Logstash+Kibana)这样的开源软件选项正在被越来越多的人采用。与此同时，来自 New Relic、AppDynamics、BMC 和 Riverbed 的商业 SaaS 产品正在提供高度支持 API 的下一代选项。注意，尽管 APM 被认为是 ITOM 的一个类别，但它肯定是最以开发为中心的。

相比之下，基础设施监测相对滞后。典型的运营中心安排自己在一个多层次的技能层次。实践是围绕单一的、GUI 驱动的工具形成的，手动过程是标准。事实上，公平地说，许多 ITOM 实践中的许多制度知识实际上是“肌肉记忆”也就是说，知道在屏幕上点击哪里。这些层次结构的烟囱是围绕不同类型的基础架构(计算、存储和网络)形成的。烟囱之间的协作是例外，而“烫手山芋”故障排除例程是规则。协作通常需要自上而下的压力，而不是源自组织的 DNA，通常是为了应对危机。在工具方面，整体式企业软件部署和基于设备的架构很常见。这些产品主要被设计来提供 GUI 体验。从供应商的角度来看，他们的 API 通常是二等或三等公民，并不面向最终用户。相反，API 主要是为供应商到供应商的合作集成和高成本的定制集成项目而存在的。显然，这张照片不是 DevOps 涅槃——那么 DevOps 是如何影响它的呢？到目前为止，答案是渐进的。

IT 领域正在为 DevOps 做准备的一个明显迹象是云和开源中断，我说的中断是指超越狭隘的点工具到通用平台。那些用于 APM 的开源工具正在进入系统管理，并在较小程度上进入网络管理。随着新 SaaS 产品的推出，我们也开始看到系统和网络管理工具变革的“萌芽”,尽管我们在这些领域还远未达到临界点。然而，真正转换到基于云的 DevOps 方法的一个有趣挑战是需要解决大数据问题。现在，IT 基础架构和网络设备生成的数据量非常庞大，传统的系统和方法已经跟不上了。起源于 20 世纪 90 年代的遗留系统基于纵向扩展模型，而不是为今天的数据量而构建的。即使是基于云的解决方案也不一定适合处理 IT 大数据。除非 ITOM 广泛面对这一技术挑战，否则它仍将是转型变革的障碍。

***作者简介/Alex Henthorn-Iwane***

亚历克斯·亨索恩-伊万是肯蒂克公司的营销副总裁。Henthorn-Iwane 拥有 20 多年将网络、安全和软件领域的新技术推向全球市场的经验。Henthorn-Iwane 领导 Kentik 的全球营销战略，并帮助该公司将其创新故事和解决方案带给世界各地依赖网络的组织。

在加入 Kentik 之前，Henthorn-Iwane 曾担任 QualiSystems 的营销副总裁，负责监管面向混合 IT 基础设施的业界领先的 DevOps 云流程编排软件供应商和 Packet Design Inc .的全球营销，Packet Design Inc .是一家由连续创业者 Judy Estrin 创立的网络管理软件供应商。在此之前，他曾在 CoSine Communications、Corona Networks、Lucent Technologies 和 Livingston Enterprises 担任产品管理职务。

通过在 QualiSystems、Packet Design、CoSine Communications、Corona Networks 和 Lucent Technologies 的工作，他获得了云计算方面的专业知识以及虚拟化带来的机遇。他为《嵌入式计算》、《虚拟战略杂志》、《数据化》、《SDN 中心》、《数据中心知识和信息周刊》撰稿。

在 LinkedIn、Twitter 或 SlideShare 上与他联系。