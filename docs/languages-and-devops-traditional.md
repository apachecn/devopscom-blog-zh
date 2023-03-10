# 语言和德文:繁体

> 原文：<https://devops.com/languages-and-devops-traditional/>

很长一段时间以来，所有酷孩子都在不停地谈论“全栈开发”、“API 优先”以及大量类似的方法/实践。然而，大量的应用程序仍然针对单个系统来完成特定的工作。有胖客户端，有内部服务器，有独立的应用程序。所有这些都还在开发中，炒作机器并没有对它们做出太多的解释，尽管它们相当普遍。

我们仍然需要维护它们，或者再写一个。他们哪儿也不去，因为有些问题他们是正确的解决方案。所以我们来说说他们。

为了清楚起见，我将传统定义为“针对特定的操作系统/硬件平台，并且主要不是基于 web 的。”我们将排除大型机，因为工具集和与 DevOps 的集成仍然不同，足以保证它们有自己的博客。

在线论坛上满是试图重新定位传统应用的人(感觉到的 Windows 10 问题导致许多人想离开 Windows，越来越多的 Linux 发行版成为 beta 甚至 alpha 测试版的趋势使许多人想离开 Linux)，而其他人只是试图让它们随着他们脚下的世界变化而运行。

**简单集成**

虽然这些开发工具是敏捷围绕着它们成长起来的，但这使得它们很好地集成到了敏捷和开发运维中。编译器和各种构建工具的输入/输出与我们正在研究的其他空间相同(或者更准确地说，其他空间与传统空间相同)，因此 AppDev 的集成通常不是问题。整合运营更难，但确实存在。各种侧重于操作的 DevOps 工具(我喜欢称之为 devOPS，而不是 DEVops)可用于传统开发，您当然可以通过它们进行部署，但它们就像是“全栈”的第二代堂兄弟足够好的规则一天，一点点工作将是必需的。幸运的是，Ansible 和 Puppet 等工具为部署铺平了道路，不太关心您是在部署传统应用程序还是 web 服务，只要您告诉他们如何成功部署。

**你得移动它，移动它……**

便携性正日益成为一个问题。“首选”Linux 发行版的兴衰，成为微软商店的成本……有很多理由想要移动你的应用。最好的第一步(也是一些人唯一需要的一步，我认为)是集装箱化。把它放在一个容器中，你的底层硬件可以在公司决定的任何操作系统上运行，而你的应用程序将在他们需要的操作系统上的[容器](https://devops.com/?s=containers)中运行。对大多数组织来说，这只是权宜之计；一种快速将服务器从一个操作系统转移到另一个操作系统的方法，但应用程序最终必须完全转移到新的操作系统。微软有针对 Linux 的 Windows 子系统，可以帮助从 Linux 迁移到 Windows，Linux 有 Wine 帮助在 Linux 上运行 Windows 应用。两者都朝着互操作性的方向迈进了一大步，但都不完美——甚至都不容易。这需要一点工作，但远不如自顶向下重写目标操作系统。如果你不想使用微软的解决方案，像 Cygwin 这样的工具也可以让你的 Linux 应用在 Windows 上运行。最终，你将不得不修改代码，但是你*正在*移植一个应用程序，所以这并不奇怪。

**考虑未来**

我在 20 世纪 90 年代末和 21 世纪初工作过的一个地方有一台 OS/2 机器，它是关键的基础设施。我们不被允许碰那个盒子。我想如果管理员有他们的方式，我们就不会被允许看物理盒子。当然，我们尽可能快地进行了虚拟化，类似于我上面的“容器化”建议。现在是考虑编写具有可移植性的应用程序的好时机，所以你可以从等式中删除这种类型的系统。在这一点上，RHEL 5 或 Windows XP 应用程序应该*真正*现代化或淘汰。跨平台开发的工具就在那里，从 Mono 到 [Java](https://www.java.com) 到 Xojo 与平台相关的位可以被隔离，以便快速重定向。当需要改变目标平台时，前期工作会带来巨大的回报。

**你。摇滚。**

无论你选择哪种语言，最终，都有可能是你的构建工具将它与 DevOps 联系起来。在不久的将来，您对 DevOps 最大的担忧可能是可移植性。同时，继续摇摆。你在做需要做的工作，即使这不是每个人目前都在谈论的 DevOps 的一部分。