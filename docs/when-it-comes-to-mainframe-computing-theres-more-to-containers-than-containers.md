# 说到大型机计算，容器比容器更重要

> 原文：<https://devops.com/when-it-comes-to-mainframe-computing-theres-more-to-containers-than-containers/>

当 DevOps 世界中的人们听到“容器”这个词时，大多数时候他们会想象轻量级的、独立的、可执行的 [Docker 二进制文件](https://www.docker.com/what-container) ，这在今天的云基础设施中已经变得司空见惯。然而，令人惊讶的是，大型机计算世界不仅支持传统的 Docker 容器，还将隔离和安全的概念扩展到另一种称为 IBM 安全服务容器的容器化技术中。对于在 IBM Z 上运行 Linux 的公司来说，安全服务容器为大型机计算带来了新的安全性。

大型机计算已经提供了商用 x86 环境难以匹敌的强大功能。例如， IBM z14 大型机可以存储高达 32TB 的内存。它有一个 10 核 z14 CPU，运行速度高达 5.2 GHz，比 4 核 [英特尔 i9 处理器](https://en.wikipedia.org/wiki/Skylake_(microarchitecture)) 的约 4 GHz 快得多。凭借这种能力，大型机可以在标准 Docker 容器中运行 Node.js 和 MongoDB，每天执行 300 亿次 RESTful 事务。结合在大型机上运行 Linux 所提供的多功能性和代码重用，您将获得难以忽视的计算能力。

在应用程序开发方面，将 Linux 放在大型机上允许用流行语言如 Java、Python 或 Node 编写应用程序。JS 在 IBM Z 系统上运行，就像它们在一个充满 x86 机器的数据中心中运行一样。与商用系统相比，大型机的总拥有成本具有惊人的竞争力。

尽管有这些好处，大型机上的 Linux 面临着许多其他平台所面临的同样的安全挑战，包括硬件和软件入侵。不同之处在于，IBM Z 开箱即用更加安全，并提供了许多额外的技术来应对这些挑战——100%的应用程序数据加密、多租户环境的隔离工作负载、具有加密密钥的全生命周期加密密钥管理和篡改响应加密硬件。但是很多时候，安全归结于系统管理员的安全意识和组织内部灌输的整体安全原则。一些组织拥有出色的安全实践。其他人受到挑战。不管胜任程度如何，都很难防弹地锁住一个箱子。这就是安全服务容器技术发挥作用的地方。

# 使用安全服务容器

安全服务容器将硬件虚拟化、应用程序和数据结合到一个安全、加密的“容器”(分区)中。加密密钥在安全服务容器分区中受到保护。如果密钥被泄露或试图篡改密钥，安全服务容器将使密钥无效，加密的内容将变得不可访问。

一旦部署了安全服务容器(通过物理上安全的硬件和固件)，容器中的所有内容都将被完全加密。引导扇区变得防篡改，并且存储器访问被禁止。此外，通过 [SSH](https://en.wikipedia.org/wiki/Secure_Shell) 对系统的访问也被移除。因此，除了用于通信和管理的 RESTful 接口之外，硬件和操作系统系统管理员无法直接篡改环境。

使用 SSH 来管理系统给灾难留下了很多机会:虽然 Linux 允许您根据组和用户权限来限制对命令的访问，但是在环境中错误地安装一个不安全的可执行文件就可能导致灾难。

另一方面，访问支持安全服务容器的环境的唯一方式是通过一组 API。与安全服务容器 API 相关联的每项管理功能都被表示为一个具有访问方法的端点。因此，通过 API 进行安全访问的优势在于，工作是在一个公共接口上逐个任务地完成的。不同的安全策略可以应用于每个端点和相关联的访问方法。这是一个非常细粒度的安全模型。

使用“只使用 API”的方法访问意味着对于所有意图和目的来说，系统是完全锁定的。根据给定端点上的安全策略，即使根用户和系统管理员没有被授予访问权限，也会被拒绝。因此，“斯诺登式”攻击得以避免。

HSM——加密和保护密钥的物理设备——被认证为 [FIPS 140-2 Level 4](https://en.wikipedia.org/wiki/FIPS_140-2#Level_4) ，这是在 [联邦信息处理标准](https://en.wikipedia.org/wiki/Federal_Information_Processing_Standards) 中定义的最高安全标准。此外，各个安全服务容器被隔离到[【eal 5】和更高的](https://en.wikipedia.org/wiki/Evaluation_Assurance_Level#EAL5:_Semiformally_Designed_and_Tested) 级别，从而在容器之间提供近乎空气间隙的隔离，以确保 [旁道攻击](https://en.wikipedia.org/wiki/Side-channel_attack) 不会起作用。这是一种工业级安全性，旨在满足银行、电网、原子能委员会和中央情报局等高度安全敏感环境的需求。安全服务容器对于严肃的企业来说是严肃的技术。然而，Secure Service Container 可以使任何希望进入大型机计算世界的公司受益，其成本可以令人惊讶地承受得起。

# 一种新的思维方式

当大多数人想到大型机计算时，他们会想到拥有大量预算来购买高价硬件的大公司。虽然这可能是过去的情况，但今天，大型机技术是小公司力所能及的。与 x86 竞争对手相比，今天的大型机的信息总成本可以降低 92%。当您考虑到增加的灵活性、规模和安全性时，使用 IBM 大型机而不是 x86 机器的机架来设置内部云安装似乎非常合理。

除了成本之外，大型机还提供了显著的优势，尤其是当安全服务容器技术被加入进来的时候。首先，在大型机上运行 Linux 在应用程序开发方面创造了一个共同的竞技场。大多数基于 Linux 的应用程序代码既可以在大型机上运行，也可以在 PC 上运行。这意味着一个 Java 开发人员可以利用他或她的专业知识为各种环境——PC、Android 或大型机——编写代码。

| **Security Risks by the Numbers**●到 2021 年，网络犯罪给世界带来的损失达 6 万亿美元●2017 年一次数据泄露的平均成本为**[【360 万美元](https://www.ibm.com/security/data-breach)**●60%的网络攻击受害者面临被停业的风险●每隔**[14](https://www.csoonline.com/article/3237674/ransomware/ransomware-damage-costs-predicted-to-hit-115b-by-2019.html)**[秒](https://www.csoonline.com/article/3237674/ransomware/ransomware-damage-costs-predicted-to-hit-115b-by-2019.html) 一家企业就会成为勒索软件攻击的受害者●只有 企业的**[【⅓】](https://www.zdnet.com/article/what-is-docker-and-why-is-it-so-darn-popular/)**[为生产用安检容器](https://www.zdnet.com/article/what-is-docker-and-why-is-it-so-darn-popular/) |

大型机还提供非常大的存储空间、难以置信的高计算能力和统一的环境。应用程序和数据库可以放在同一个盒子里，减少了网络延迟，提高了整体处理速度。

安全服务容器技术使安全性变得更加可靠和易于管理。系统管理的“仅 API”访问方法使支持成为一项安全、标准化的任务。从 DevOps 的角度来看,“仅 API”方法提供的标准化很容易自动化，并且您不必在较低的操作级别上适应系统管理的特性。

最后，如上所述，IBM Z 上的 Linux 支持 Docker。将大型机资源与 Docker 生态系统集成在一起，可以在单台机器上实现高性能、高容量、短暂的计算。IBM Z 上的单个 [Linux 安装可以支持多达 100 万个 Docker 容器。而且，由于这些容器驻留在同一台机器上，它们可以利用与其他大型机工作负载的协同定位，并将外部网络延迟的影响降至最低。任何使用过分布式架构的人都会告诉你，容器化的微服务的可用性决定了它的好坏。将所有容器放在一台计算机上可以显著降低服务间通信失败的风险。这是一件大事——尤其是考虑到 IBM z 99.999%的正常运行时间。](https://www.ibm.com/it-infrastructure/z/os/linux)

# 把所有的放在一起

容器正迅速成为现代云计算的基础。然而，容器化不仅仅是创建 Docker 图像的实例。容器化背后的概念有着广泛的应用，远远超出了基于商品的计算。Secure Service Container 结合了硬件和软件安全性的最佳实践，创建了一个基于 Linux 的环境，使大型机技术成为现代云计算领域的一流参与者。

考虑到 IBM Z 和安全服务容器等技术的成本降低和收益增加，大型机计算可以成为任何公司的重要资产。所有真正需要的是花时间去理解可用的力量和探索手边的可能性。

# 了解更多信息

您可以通过以下资源了解 IBM 上的 Linux 和安全服务容器:

*   [攀登数字之山:实现安全、敏捷、高效的组织](https://www.ibm.com/account/reg/us-en/signup?formid=urx-32942)
*   [IBM Z 上的 Linux](https://www.ibm.com/it-infrastructure/z/os/linux)
*   [IBM 安全服务容器用户指南](https://www-01.ibm.com/support/docview.wss?uid=isg2bb79df265313634d85258088005188e3&aid=1)
*   [安全服务容器是针对敏感工作负载的虚拟设备框架](http://ibmsystemsmag.com/mainframe/trends/security/secure-service-containers/)

鲍勃·雷瑟曼