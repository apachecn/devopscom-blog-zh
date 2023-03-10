# 巴拿马，码头工人管理

> 原文：<https://devops.com/panamax-docker-management-humans/>

CenturyLink 的一个新的开源工具 Panamax 带来了构建复杂的 Docker 环境的希望，就像一个孩子使用乐高积木一样。该工具是一个管理界面，用于管理和构建多个 Docker 环境。您可以搜索 Docker 官方存储库以及许多其他存储库，以找到同类最佳的 Docker 预建容器。Panamax 可在 GitHub 上获得，并在 Apache 2.0 许可下发布。

昨天，我与 CenturyLink 的首席创新官 Lucas Carlson 就 Panamax 进行了交谈。卢卡斯还领导着 CenturyLink 实验室，这是他们开发并发布的首批项目之一。卢卡斯给了我一个 Panamax 的演示。在短短的几分钟内，我们已经搜索并找到了几个 WordPress 容器。我们从官方 Docker 资源库中选择了一个，并快速安装了它。之后，很容易选择其他服务，比如 Ruby，并将它们添加到我们的实例中。我们很快就添加了几个不同的 Docker 容器，并构建了一个相当复杂的环境。下面是一些 Panamax 的屏幕截图。

[![panamax 1](img/d012b9e499959a5a9a75b8241505a342.png)](https://devops.com/wp-content/uploads/2014/08/panamax-1.jpg)

[![panamax 2](img/1a0f661b0c6945ddff9b92da883c8b3b.png)](https://devops.com/wp-content/uploads/2014/08/panamax-2.jpg)

卢卡斯向我解释说，他认为 Panamax 是“人类的码头管理”它使得构建多 docker 环境变得非常容易。摘自 Panamax 新闻稿:

在 Panamax 之前，使用 Docker 运行多容器、多服务器应用程序非常困难。开发人员需要学习多达五种新技术——libswarm、systemd、etcd、ambassador 和 fleet——以及特定于 Docker 的最佳实践。Panamax 将这些技术和最佳实践整合到直观的用户体验中，实现了复杂应用程序部署的自动化。开发人员只需拖放容器，就可以轻松访问开源云应用市场。Panamax 可以运行在笔记本电脑、虚拟机、裸机或任何支持 CoreOS 的公共云上，如 [CenturyLink Cloud。](http://www.centurylinkcloud.com/)

正如上一段所指出的，Panamax 目前只支持 CoreOS。当然，除了 CenturyLink 自己的云服务之外，这使它可以在亚马逊和其他一些云提供商上运行。然而，我认为 Panamax 移植到其他云 Linux 操作系统发行版只是时间问题。

Docker 已经是有史以来发展最快的开源项目之一。Panamax 等第三方应用程序证实，围绕 Docker 容器的整个生态系统正开始出现并蓬勃发展。在过去的一周里，一些公关公司向我推销了围绕 Docker 推出或推出产品的新公司。

其中许多公司认为，Docker 将紧跟 VMware 的步伐，因为它将成为首选的虚拟化解决方案。Docker 将提供什么，而其他人将提供什么，仍在研究中。VMware 也是如此。VMware 将提供什么样的安全性，有哪些第三方安全性可用？有一段时间，这是一个亟待解决的问题。类似的问题会在 Docker 周围被问到，每个人都会在桌子周围争夺位置。

CenturyLink 当然认为 Panamax 会帮助 Docker 开发者选择 CenturyLink cloud 而不是 Amazon 和其他公司。

因此，Docker 继续其在科技界的火热上升势头。Panamax coudl 成为 Docker 世界中的明星，让每个人都能像搭建乐高积木一样轻松地制作复杂的 Docker 环境。就像卢卡斯说的，对人类来说是 Docker 管理。