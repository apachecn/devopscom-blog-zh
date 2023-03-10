# 31 开发运维及持续交付的参考架构

> 原文：<https://devops.com/31-reference-architectures-devops-continuous-delivery/>

在 QCon London 上，David Farley([@ Dave Farley 77](https://twitter.com/davefarley77))告诉观众“持续交付改变了软件交付的经济学”。我完全同意。

如果您被像 David Farley、Jez Humble 和 Gene Kim 这样的布道者所吸引，您就会知道高性能 IT 组织正在看到他们的持续交付投资的巨大回报。大大小小的行业领导者都分享了显著的成果:

*   生产部署频率提高 8 倍
*   变更失败率降低 50%
*   出现问题时，服务恢复速度提高 12 倍

**5 项原则**

他们是如何实现这些结果的？他们正在遵循大卫和杰斯在他们的开创性著作《持续交付》中概述的几个关键原则(强烈推荐)。他们的书和大卫的 [QCon 演讲](http://qconlondon.com/system/files/presentation-slides/The%20Rationale%20of%20Continuous%20Delivery%20-%2045%20Minutes.pdf)中概述的原则如下:

*   快速交付
*   几乎一切自动化
*   让一切都在版本控制中
*   将质量建立在
*   授权给团队

**开发运维及持续交付的参考架构**

在他们的书中，他们还提供了对持续交付工具链和过程的见解，突出了构建工具、CI 平台、测试套件、工件库和许多其他组件。有许多参考体系结构的例子，每一个都有不同的详细程度、突出的工具和遵循的流程。然而，工具集中有一个不变的主题:Jenkins、Maven、Nexus、Subversion、Git、Docker、Puppet/Chef、Rundeck 和 Sonar 似乎一次又一次地出现。

为了帮助您踏上持续交付和开发运维之旅，我 [**整理了一套由持续交付和开发运维社区用户创建的 31 个参考架构**](https://bit.ly/1JbI6m4 "Continuous Delivery Reference Architectures") 。

**[![CD and DevOps tool chain](img/50b60fdf94068b8fece0cf8802156bf0.png) ](https://devops.com/wp-content/uploads/2015/04/Screen-Shot-2015-04-21-at-9.34.39-AM.png) [](https://devops.com/wp-content/uploads/2015/04/Screen-Shot-2015-04-21-at-9.18.30-AM.png)** 

每个体系结构都附有一个到引用该体系结构的原始演示文稿或博客的链接，以确保您可以访问讨论的完整上下文。您也可以从 SlideShare 免费下载演示文稿，我们现在有超过**7000 次浏览**。

**主动帮助他人:**如果您有要分享的参考架构，请考虑在下面的评论部分发布一个链接。我相信其他人会很乐意看到它并从中学习。