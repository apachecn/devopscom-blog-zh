# 重塑对私有混合云的监控

> 原文：<https://devops.com/reinventing-monitoring-private-hybrid-cloud/>

自从计算出现以来，对系统、网络和应用程序的监控就一直存在。然而，在过去的五年中，计算、网络和应用程序开发领域发生了巨大的变化和创新。

例如，基础架构是动态共享和分配的，通常是通过持续自动化实现的。VMware 的服务器虚拟化和动态资源调度(DRS)允许虚拟服务器基于 CPU 和内存限制在主机之间自动移动。包括 VMTurbo 和 Cirba 在内的自动化供应商在这方面更进了一步，整合了网络和存储拥塞等限制，并允许对工作负载进行优先级排序。

如今，虚拟化扩展到了网络和存储领域。在某些情况下，虚拟网络是在每两个必须使用 VMware NSX 等产品相互通信的事物之间的软件中建立的。存储正在被虚拟化，因此操作系统和应用程序访问的存储层与实际的物理磁盘或闪存阵列之间几乎没有相似之处。也就是说，在实际应用程序和物理硬件之间还有更多抽象层。其中可能包括 Docker、Java 虚拟机(JVM)、Cloud Foundry 等平台即服务(PaaS)堆栈以及上面列出的虚拟化层。

现在，应用层的特点是多样性和快速变化。它不再仅仅是一个 Java 世界；其他语言也一样受欢迎，每天都有新的语言出现。企业要求更快地将更多功能投入生产的压力导致了敏捷开发和开发运维，这两者都导致了应用程序在生产中被更频繁地修改。

私有云和混合云会导致基础架构层、管理层和团队层以及工具层，从而产生与过去的管理孤岛相同的问题。云架构中的每个基础架构即服务(IaaS)、PaaS 和软件即服务(SaaS)层都有自己的团队来管理它们，并有自己的工具来管理这一层。监控这些层的工具有:

1.  **对于 IaaS 层**–存储工具、存储区域网络(SAN)工具、网络工具、服务器工具、虚拟化(虚拟机管理程序工具)和监控广域网的工具。
2.  **对于 PaaS 层**——监控支持应用的所有软件服务的工具，包括数据库服务器、web 服务器、Java 应用服务器、PaaS 框架，当然，现在还有 Docker。
3.  **对于 SaaS 层**–监控应用本身的工具，包括应用性能管理产品，以及监控实际终端用户体验的工具。

## **私有云或混合云的各层**

![layer](img/0e26c499ae2dc8516764f152248eeffd.png)

### 问题:监控

为了使私有云取得成功，这些工具层有几个核心问题必须解决:

1.  **缺乏可见性**–来自这些层中每一层的每一个工具的数据不与私有云堆栈的其他层的所有者或运营商共享。私有云的业务成员或用户无法获得一组整合的数据或指标，因此他们无法端到端地了解其应用程序的行为以及支持这些应用程序的工作负载。
2.  **沟通问题**–当出现性能问题时(总是会出现)，工具集的分层以及拥有三层的团队之间缺乏协作使得问题解决成为一个耗时且令人沮丧的过程。
3.  **不正确的数据分析**—尽管所有这些工具都收集了大量的监控数据，但在许多情况下，根本没有收集到确保私有云为其托管的应用程序和业务成分正常运行所必需的数据，或者没有以所需的方式收集到这些数据。

### 需要什么:新型监控数据

高度动态和互动的系统有一个新的方法来收集和处理监测数据。为了在竞争中立于不败之地，现代监控数据管道必须包含以下概念:

1.  **指标流**–现代在线应用系统产生指标流，从响应时间(用户体验)数据开始，包括支持交互的所有软件和硬件层的行为数据。
2.  **关系流**–在现代在线应用系统中，感兴趣的事务与运行它的 JVM、运行 JVM 的操作系统、运行操作系统的虚拟化硬件以及支持该事务的整个虚拟化和物理基础设施(下至硬盘上的轴)相关。
3.  **状态流**–大多数企业都有配置管理数据库(CMDBs)。这些应该存储企业的整个软件和硬件环境的当前状态。但是现在，在线系统变化太快，CMDBs 无法跟上时代的步伐——让它们沦落为比无用的遗留技术还要糟糕的垃圾场。对于 CMDB 和 CMDB 来说，私有云及其现代应用程序实在是太动态了，必须用自动持续更新的东西来替代。

## 关键指标及其来源

监控最大的问题是一个错误的观念，即监控组成应用程序或私有云的一组设备和软件堆栈的资源利用率可以确保可接受的服务质量。

为了纠正这种误解，我们必须将性能重新定义为没有可用资源，而是根据完成工作需要多长时间(响应时间和延迟)以及每单位时间完成多少工作(吞吐量)。响应时间、吞吐量，当然还有错误，需要成为判断和交付服务质量的关键指标。

如果我们承认响应时间、吞吐量和错误是衡量标准的重要类别，那么接下来的步骤就是确定私有云堆栈每一层的这些衡量标准，然后确定这些衡量标准的来源。要认识到的最重要的事情是存在于栈的每一层的标准接口(SMIS、SNMP、Netflow、JMX 等)。)不测量响应时间、吞吐量和错误，我们不得不依赖于在收集这些指标所需的定制工具上投入大量资金的供应商。

我们还必须认识到，在特定层收集这些指标的投资是巨大的，因为收集这些指标所需的技术专业知识水平超过了单个供应商或工具所能收集的水平。

最后，我们必须认识到，行业变化太快，任何单一供应商都无法覆盖整个云堆栈。网络虚拟化、存储虚拟化和容器只是需要仪器进步和创新的创新的最新例子，而且这些进步将继续以更快的速度出现。

出于上述原因，适用于私有云和混合云的唯一监控策略是关注在云堆栈中的某一层收集所需数据的最佳供应商，然后将这些指标输入到通用大数据后端进行处理或分析。

## 专用混合云的监控体系结构

![monitoring](img/dcea9b9e3e3d54055f015c63e890d55e.png)

私有云和混合云都需要完全不同的方法来收集数据、处理数据并使这些数据对用户和分析师有用。企业 IT 运营组织必须采用这些现代方法来管理他们的私有云，否则这些云将无法与公共云产品在成本和功能上竞争，从而导致更多的工作负载外包给公共云提供商。

## 关于作者/Bernd Harzog

![Bernd Harzog_Headshot_2016](img/76507adf89a70ca7f799214c6f569e3f.png) Bernd Harzog 是 OpsDataStore 的首席执行官和创始人，ops datastore 是所有 IT 运营管理数据和供应商的实时大数据后端。OpsDataStore 的开放式大数据后端使用和关联来自多个来源的数据，并使用市场领先的 BI 和可视化工具立即使这些数据对决策者有用。在[www.opsdatastore.com](http://www.opsdatastore.com)了解更多信息，并关注 Twitter 上的 OpsDataStore、 [@OpsDataStore](https://twitter.com/OpsDataStore) 和 [LinkedIn](https://www.linkedin.com/company/opsdatastore) 。