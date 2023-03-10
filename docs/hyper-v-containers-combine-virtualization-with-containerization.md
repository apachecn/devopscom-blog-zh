# Hyper-V 容器将虚拟化与容器化相结合

> 原文：<https://devops.com/hyper-v-containers-combine-virtualization-with-containerization/>

集装箱最近很流行。如果你不使用 [Docker](https://devops.com/features/puppet-labs-talks-docker-and-containerization/) 或其他容器技术来构建和部署你的 IT 基础设施，你就不够酷。然而，传统容器对于一些行业和公司来说缺乏足够的安全性，因此微软开发了 Hyper-V 容器。

像 Docker 和 [Rocket](https://devops.com/features/shooting-rocket-dockers-bow/) 这样的容器平台势头强劲，并且已经迅速成为开发和部署应用程序的事实方式。微软已经达成协议，将[本地 Docker 容器支持引入 Windows Server](https://devops.com/features/microsoft-partners-docker-bring-containers-windows-server/) ，但现在它更进一步，创建了 Hyper-V 容器，将容器的灵活性与虚拟化的安全性结合起来。

Hyper-V 容器确保在一个容器对象中运行的代码保持完全隔离。Hyper-V 容器对象不能影响其他容器对象或主机操作系统，反之亦然，因为它是一个单独的虚拟化容器。微软 Windows Server 总经理 Mike Neil[在一篇博客文章](https://azure.microsoft.com/blog/2015/04/08/microsoft-unveils-new-container-technologies-for-the-next-generation-cloud/)中解释道，“利用我们深厚的虚拟化经验，微软现在将提供具有新隔离级别的容器，以前只为完全专用的物理机或虚拟机保留，同时通过完全 Docker 跨平台集成保持敏捷和高效的体验。”

IT 管理员会意识到，Hyper-V 容器可以使用与传统 Windows Server 容器相同的开发和管理工具来创建和部署，并且可以与 Docker 集成以实现跨平台部署。Neil 指出，作为 Windows 服务器容器开发的应用程序可以轻松地部署为 Hyper-V 容器，无需任何修改——使组织能够采用现有的容器化应用程序，并以更安全的方式重新部署它们。

安全性似乎总是任何新技术概念的补充，容器也不例外。它开始是一个着火的好主意，但直到它达到临界质量并实现主流采用，安全性才成为一个因素。然而，随着大型公司或高度管制行业中的组织考虑加入容器潮流，安全性成为一个强制性的组成部分。

虚拟化已经在托管环境中使用多年，作为一种隔离在同一物理硬件或网络上运行的不同系统的方法。微软的 Hyper-V Containers 采用了这些相同的原则，并将其应用于容器应用程序级别，以便安全意识强的组织可以高枕无忧，并在接受容器化时遵守安全要求。

微软在 Windows Server 和 Azure 中集成 Windows Server 容器和原生 Docker 支持的策略是朝着正确方向迈出的一大步。增加 Hyper-V 容器的安全性是明智的。微软在转变其商业模式方面做得非常好，不仅采用了云和 DevOps 技术，还提高了标准并处于领先地位。

作为补充说明，微软还宣布了 Nano Server——一种针对云托管和容器技术优化的 Windows Server 的新的最小占用实现。Nano 服务器安装包括最少的必要组件。微软声称其结果是更小的服务器映像、更快的部署时间、更少的网络带宽消耗和更少的管理开销。换句话说，Windows Server 的 Nano 服务器安装将在最少的交互或监督下完成它应该做的事情，因此 it 人员可以专注于更重要的事情，如在其上运行的 Hyper-V 容器应用程序。