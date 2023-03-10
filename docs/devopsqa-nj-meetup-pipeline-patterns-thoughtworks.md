# 新泽西州会议:ThoughtWorks 的管道模式

> 原文：<https://devops.com/devopsqa-nj-meetup-pipeline-patterns-thoughtworks/>

[DevOpsQA NJ](https://www.meetup.com/DevOpsandAutomationNJ/) 举行了我们一月份关于管道模式的会议，来自 [ThoughtWorks](https://www.thoughtworks.com/) 的 Max Griffiths ( [@_maxamg](https://twitter.com/_maxamg) )、Max Lincoln ( [@devopsy](https://twitter.com/devopsy) )和 Gary Stafford([@ Gary Stafford](https://twitter.com/garystafford))担任演讲人。见面会在轰动一时的 ThoughtWorks NYC 地点举行，有一个欢迎、开放的见面会区和一个巨大的展示区，展示区有明亮、独特的壁画。

随着披萨和啤酒的快速联网，讨论以演讲者的简短介绍开始，他们每个人都在 DevOps 领域工作了 10 多年。他们对 ThoughtWorks 进行了高度概括，并推荐了一些书籍，包括 Jez Humble 的《持续交付》(Continuous Delivery)、“发布吧！”迈克尔·尼加德和吉恩·金的“凤凰计划”。

那么我们试图解决的问题是什么呢？我们正努力获得在早期做出决定的能力，以影响我们的渠道如何扩展，重点是文化、反馈和治理。

Max Lincoln 给“好”管道下了一个很好的定义。它应该有增量 QA，快速反馈，进度的可见性和一致的，可审计的软件交付过程。对于如何命名管道中的东西，非常有选择性是一个好主意。“管道的目的是尽快扼杀建设，”他说。随着管道变长，快速反馈变得更加困难。

接下来，每个演讲者都谈到了管道如何在三个不同的方向上扩展:X(提交和生产之间的更多阶段)；y(更多项目/应用)；和 Z(并发发布)。Max Griffiths 给出了 X 轴模式的概述，其中包括线性、平行和分层模式(带有工件推广和发布渠道)。线性模式是最简单的模式，适用于简单的应用程序。使用并行模式，您可以在可能的地方开始并行化；然而，这可能会产生依赖性，并使重新排序变得困难。分层模式鼓励并行化，但防止阶段之间的直接依赖。

通过为每一层添加一个单独的工件存储库，进一步增强了分层模式，这使得工件保留策略更加容易。您可以使用青铜、白银、黄金作为层的名称，以便于理解候选版本是如何从一个阶段发展到另一个阶段的。

加里·斯塔福德介绍了 Y 轴模式，包括联合标记、集合标记、独立管道和 VCS 标记。在其他人中。Gary 使用微服务的例子来演示如何对松散相关的应用程序或服务进行连续交付。

Max Lincoln 谈到了 Z 轴模式的并发发布。按照 Max 的说法，dev 需要的不是分支策略，而是合并策略，特别是如果提前六个月创建了一个发布分支。“如果你让 Jenkins 一天做 1000 个构建，并不意味着你有 CI，”他说。![IMG_6637](img/29049bb47bea06c00a697ccbc2d7a0cd.png)

演讲者最后都介绍了一种他们称为“不同维度”的额外模式。最后的建议是将 CI(无论是 Jenkins 还是 GoCD)放在源代码控制中，并持续测试您的管道。最后，我们进行了精彩的问答环节和热烈、开放的讨论。

期待我们的下一次会面。

![FullSizeRender (2)](img/36aff1f3a551aa2355b5c272afdfc4dd.png)
如果你想了解更多关于 ThoughtWorks 和/或 Pipeline 模式的信息，你可以在 GitHub 页面继续对话:【https://github.com/thoughtworks/PipelinePatterns】T2