# 甲骨文和盟友推出基于 ARM 的云服务

> 原文：<https://devops.com/oracle-and-allies-launch-cloud-service-based-on-arm-processors/>

甲骨文今天宣布，它将首次在[甲骨文云基础设施](https://devops.com/?s=oracle+cloud+infrastructure) (OCI)上提供基于 ARM 的处理器，该处理器也将被支持作为部署使用 GitHub、GitLab 或 Jenkins 平台的应用的目标。最新的 Oracle 服务基于 Ampere Computing 的处理器。

该公司今天还透露，它已经加入了连续交付基金会(CDF)，这是 Linux 基金会的一个分支，负责监督开源 DevOps 平台和工具(如 Jenkins 和 Spinnaker)的开发。

OCI 计算副总裁 Matt Leonard 表示，OCI 安培 A1 计算为 Oracle 提供的基于 x86 的处理器的现有支持提供了一种替代方案。该服务将以每核心小时 1 美分的成本提供，虚拟机大小从 1 到 80 个 OCPUs 不等，每个核心配置 1 到 64 GB 的内存，或者作为具有 160 个核心和 1 TB 内存的裸机服务。每小时每 GB 内存的定价为 0.0015 美元。伦纳德说，在这个价位上，甲骨文现在提供的每核心价格是所有云服务提供商中最低的。

在组织显著增加在公共云上构建和部署的应用程序数量的同时，基于 ARM 的处理器的可用性不断提高，开始对云经济产生影响。Leonard 指出，为了降低总体成本，许多组织正在积极评估基于 ARM 的服务。

为了帮助在该平台上快速启动应用程序开发，Oracle 为组织提供了三类 OCI 安培 A1 计算服务。Oracle 云免费层为开发人员提供 300 美元的免费积分，为期 30 天。始终免费的 ARM 选项为开发人员提供了四个 A1 内核和 24 GB 内存，而 ARM 加速器选项则为开源开发人员、独立软件供应商(ISV)合作伙伴、客户和大学提供了基于 ARM 的开发项目，这些项目需要 Oracle 云免费层在 12 个月内提供的额外资源。

Oracle Linux、Java、MySQL、GraalVM 和 Oracle Container Engine for Kubernetes(OKE)服务也可在 OCI Ampere A1 Compute 上使用，并与 GitHub、GitLab 和/或 Jenkins 的 DevOps 平台集成。为 OCI 安培 A1 计算提供支持的其他供应商包括 SUSE、Datadog、OnSpecta、NGINX 和 Genymobile。

Oracle 还提供了 Oracle Linux Cloud Developer image，使 DevOps 团队能够通过 OCI 控制台安装、配置和启动开发环境，该控制台包括 OCI 客户端工具、实用程序和通用编程语言，如 Java、GraalVM、Python、PHP、Node.js、Go 和 C/C++。

最后，每个 Ampere 内核都是单线程设计，具有自己的 64 KB L1 I 缓存、64 KB L1 D 缓存和一个巨大的 1mb L2 D 缓存，以消除 IT 组织可能会遇到的任何“噪音邻居”问题。

甲骨文显然是在打赌，基于 ARM 的处理器将为该公司提供一个机会，以亚马逊网络服务(AWS)和微软 Azure 等更大的基础设施即服务(IaaS)竞争对手为代价，赢得市场份额。尚不清楚 It 团队会在多大程度上采用不同的云服务来访问基于 ARM 的处理器。然而，在一个 IT 团队现在经常使用多种云的世界中，就 Oracle 而言，竞争环境从未如此公平。