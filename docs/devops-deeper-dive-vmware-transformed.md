# DevOps 深入探讨:VMware 转型

> 原文：<https://devops.com/devops-deeper-dive-vmware-transformed/>

在本周举行的 [VMworld 2019](https://www.vmworld.com/en/us/index.html) 大会上，VMware in no determine 团队明确表示，它希望成为 DevOps 的主要力量。

继上周[收购姐妹公司 Pivotal Software](https://www.vmware.com/company/news/releases/vmw-newsfeed.VMware-Signs-Definitive-Agreement-to-Acquire-Pivotal-Software.1905769.html) 之后，VMware 正在着手构建一个应用开发框架，用于构建和部署基于 Kubernetes 的云原生应用。这项工作与对其 vRealize 管理工具套件的持续投资不谋而合，VMware 致力于通过该套件在内部 IT 环境和公共云计算环境中实现 IT 运营自动化。

为了推进这两个目标，VMware 本周推出了一系列用于管理任何 Kubernetes 发行版的 [Tanzu 管理工具](https://containerjournal.com/topics/container-management/vmware-doubles-down-on-kubernetes/)，同时推出了 [VMware 混合云平台](https://www.vmware.com/company/news/releases/vmw-newsfeed.VMware-Cloud-on-AWS-Helps-Customers-Migrate-and-Modernize-Applications-with-Consistent-Hybrid-Cloud-Infrastructure-and-Operations.1906446.html)，该平台结合了从 vRealize automation 工具到来自 from Wavefront 的监控工具的一切，以创建一个中央控制台，通过该控制台可以管理所有这些工具。

The VMware DevOps Timeline

*   【2015 年 10 月—戴尔与 EMC 一起收购 VMware
*   【2017 年 4 月—VMware 收购波前监控服务
*   【2017 年 8 月–VMware 通过亚马逊网络服务(AWS)联盟转变公共云战略；VMware 和姐妹公司 Pivotal Software 发布了 Kubernetes 发行版
*   【2017 年 11 月—VMware 发布 VRealize Management Suite
*   【2018 年 2 月–VMware 收购 CloudCoreo 以获得云配置工具
*   【2018 年 8 月—VMware 收购 CloudHealth Technologies 获得治理工具；VMware 推出 AppDefense 以提供零信任框架
*   【2018 年 11 月–VMware 收购 Heptio 以获得 Kubernetes 的专业知识
*   【2018 年 12 月–戴尔收购所有 VMware 流通股
*   【2019 年 5 月–VMware 收购应用打包工具 Bitnami
*   【2019 年 7 月–VMware 收购 Avi Networks 获得 Web 应用防火墙(WAF)；VMware 收购机器学习算法和 GPU 虚拟化软件 Bitfusion
*   【2019 年 8 月—VMware 收购 Pivotal 软件；VMware 收购炭黑；VMware 推出 Tanzu 平台管理 KubernetesVMware 推出混合云平台

在决定推出一系列服务来管理公共云上的软件实例(如亚马逊网络服务(AWS)和姊妹公司戴尔 EMC 的本地服务器)后，VMware 一直在慢慢将其触角伸向应用领域。迄今为止，这一努力最重要的因素是收购 Pivotal，Pivotal 是一家广泛使用的基于 Java 的 Spring 框架和基于 Cloud Foundry Foundation (CFF)开源软件的平台即服务(PaaS)环境的提供商。

CFF 正在将为 Cloud Foundry 创建的应用程序开发环境迁移到 Kubernetes，这是一个在云本地计算基金会(CNCF)的支持下开发的云本地容器编排引擎。CFF 和 CNCF 都是 Linux 基金会的成员。Kubernetes 的兴起导致许多组织将其应用程序开发策略转移到能够支持多种应用程序开发环境的平台上。

在宣布将被 VMware 收购的交易之前，Pivotal 将 2020 财年的收入预期下调了 4000 万美元，至 5000 万美元。

![VMware DevOps](img/d89a5de1a2887d2b9681edadfa4e6030.png)

VMware CEO Pat Gelsinger

Pivotal Software 于 2013 年从 VMware 剥离出来，因此在某种程度上，VMware 收购 Pivotal 的举动代表了上周估值为 27 亿美元的回归。Pivotal 目前拥有约 350 家客户，其中许多客户在 VMware 平台上托管云铸造平台即服务的发行版。VMware 还利用 Pivotal 联合开发了一个 Kubernetes 的策划实例，名为 Pivotal Container Service (PKS ),该实例针对 VMware 平台进行了优化。作为这项工作的一部分，VMware 还在开发一个 VMware vSphere 实例，该实例将在本机运行 Kubernetes。

在 VMworld 2019 大会上，VMware 首席执行官帕特·基尔辛格明确表示，VMware 计划利用 Kubernetes 来弥合开发人员和 it 运营团队之间的历史鸿沟。事实上，他告诉与会者 Kubernetes 是自虚拟机创建以来出现的最重要的技术。作为这项工作的一部分，Gelsinger 指出，收购 Pivotal 以及最近收购 Bitnami(一家打包应用程序的工具提供商)意味着现在有超过 500 万名开发人员参与到 VMware 生态系统中。

VMware 显然希望开发人员生态系统能够扩展，因为 VMware 使在每个主要的公共云和内部 it 环境上启动虚拟机变得更加容易。过去几年，由于开发运维团队绕过内部 IT 团队，在基于 AWS 或微软替代虚拟机的云服务上部署应用程序，VMware 面临着一个重大挑战。由于 Kubernetes 固有的可移植性，VMware 希望组织现在能够在 VMware 平台上部署云原生应用程序。然而，与继续使用这些虚拟机相比，DevOps 团队在公共云上采用 VMware 的程度还有待观察。

说到云原生计算，VMware 显然在迎头赶上。VMware 目前拥有 250 家 PKS 客户，而 Red Hat(现在是 IBM 的一个分支)等竞争对手已经在 Kubernetes 上重新部署了他们的应用程序开发和部署平台，作为云代工厂 PaaS 的替代方案。从好的方面来看，VMware 现在声称是 Kubernetes 的第三大贡献者，部分原因是它收购了 Kubernetes 工具提供商 Heptio。

与此同时，毫无疑问，VMware 在开发工具以自动化管理和保护运行其虚拟机软件的 IT 基础架构方面处于领先地位。不太清楚的是，VMware 在多大程度上能够将这种成功转化为跨多个平台统一应用程序开发和 IT 运营的真正有意义的开发运维方式，而不仅仅是以折扣价将一套不同的工具捆绑在一起。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)