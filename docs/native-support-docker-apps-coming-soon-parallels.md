# Parallels 即将推出 Docker 应用的原生支持

> 原文：<https://devops.com/native-support-docker-apps-coming-soon-parallels/>

当我想到 Parallels 时，首先想到的是虚拟机。多年来，我一直使用 Parallels 在 Mac OS X 上运行 Windows 操作系统的虚拟化实例。除了虚拟机，Parallels 在 containers 变酷之前也在做 containers，上周[宣布](http://sp.parallels.com/news/pr/release/article/parallels-announces-support-for-docker-applications-on-parallels-containers/)将很快包括对 [Docker 应用](https://devops.com/blogs/docker-as-a-framework-for-your-devops-culture/)的原生支持。

几年前，Parallels 与 container technologies 合作开发 Virtuozzo 和开源 OpenVZ 平台。该公司声称是世界上部署最广泛的容器平台，拥有超过一百万个实例。随着原生 Docker 支持的推出，服务提供商将能够在 Parallels Cloud Server 平台上为希望使用 Docker 应用程序构建的客户提供基于容器的虚拟专用服务器。平行线

Parallels 虚拟化首席技术官 James Bottomley 解释道:“如今客户面临的挑战是在基于虚拟机管理程序的虚拟化环境中运行 Docker 映像。“这利用了 Docker 的核心优势——应用程序以更高的密度和性能在容器中运行——并大大降低了这一优势。”

Bottomley 补充道:“借助 Parallels 解决方案，服务提供商可以为客户提供 Docker 运行在基于 Parallels Cloud Server containers 的虚拟化之上的环境，以实现最佳性能和高密度。”

为什么这很重要？我亲自和博顿利谈过，想得到更多的信息。他告诉我，容器的主要优势——尤其是在云中——是它们具有不同于虚拟机管理程序的弹性和密度功能。扩展容器比扩展整个虚拟机更快更容易。

也有一个缺点。Bottomley 强调容器技术要求所有的容器共享同一个内核。因此，举例来说，不可能在 Linux 内核上启动基于 Windows 的容器，或者在 Mac OS X 内核上启动基于 Linux 的容器。

Parallels Cloud Server 中包含原生 Docker 支持对小型公司来说意义重大。像微软或亚马逊这样的大型企业几乎拥有无限的资源来投资可伸缩性。他们可以简单地在单独的虚拟机管理程序实例中运行容器应用程序，并继续添加更多的虚拟机管理程序实例来满足需求，但这是一种成本高昂且效率低下的解决可扩展性问题的方法。

借助运行在 Parallels Cloud Server 上的 Docker 应用程序，小型云服务提供商将拥有一个安全、高密度的虚拟服务器环境，其灵活性和可扩展性可与大型公共云提供商竞争。Bottomley 告诉我，带有 Docker containers 的 Parallels 解决方案将物理服务器开销减少了三分之一。

Structure Research 董事总经理 Philbert Shih 认为，云服务提供商为开发和部署 Docker 应用程序提供经济高效的平台存在巨大的市场机遇。“答案在于构建一个优化的基础架构环境，该环境既密集又可扩展，同时能够保持高水平的性能并促进工作负载的可移植性。”

Parallels 的发布只是 Docker 一连串胜利中的最新一个。今年早些时候，微软在 Azure 的 Linux 虚拟服务器上增加了对 Docker 容器的支持，最近宣布与 Docker 建立合作伙伴关系，将原生容器支持引入 Windows Server 的下一代产品。

然而，随着集装箱概念逐渐成为主流，Docker 也面临着来自 Rocket T1 等竞争对手的日益激烈的竞争。通过在流行和广泛使用的平台上提供原生支持来扩大 Docker 的影响范围，将有助于巩固其作为容器应用程序事实上的领导者的地位。

Parallels Cloud Server 将于 2015 年第一季度推出原生 Docker 支持。