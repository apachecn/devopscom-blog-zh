# DevOps 中新的人工智能监督者角色

> 原文：<https://devops.com/the-new-ai-overseer-role-in-devops/>

机器人霸主是科幻幻想的素材。今天，随着越来越多的团队实施人工智能(AI)，DevOps 团队需要努力、持续地看待现实。一个人工智能监督者在工作中观看应用程序可能会在你的努力中产生悲伤和兴奋之间的差异。

我们看到人工智能越来越频繁地失误。脸书最近承认，其算法未能阻止上传一个特别令人发指的直播视频。自动驾驶汽车已经撞上了汽车和人。中国的乱穿马路者被错误地识别并公开羞辱。不是因为在发展上不够努力。格言“如果很容易，任何人都可以做到”适用。

几周前，我在 Booz Allen Hamilton 的数据科学家 Kirk Borne 主持的一个关于人工智能的 Twitter 聊天会上。问题出现了，当创建使用数据和无偏见人工智能的指南时，组织应该考虑什么。以下是我的回应:

> 答 4: DevOps 团队应该有一个负责人工智能监督的人——实际观察它在做什么，并不断测试/验证它的发现 [#MITSMRChat](https://twitter.com/hashtag/MITSMRChat?src=hash&ref_src=twsrc%5Etfw)
> 
> —唐·丁吉(@ StratisetDon)[2019 年 2 月 14 日](https://twitter.com/StratisetDon/status/1096101185621241863?ref_src=twsrc%5Etfw)

## **常见问题**

大多数失败都是由于“发射并忘记”造成的，在这种情况下，人工智能系统被训练、对照训练进行测试，然后变得松散。即使是设计良好的人工智能系统也会遇到几个问题:

错误:这是 AI 做出事实上不正确的决定的地方。假阳性和假阴性以及错误分类问题都属于这一类。

**差距**:存在 AI 理解冲突选项而无法选择的情况。然后，在一些情况下，人工智能不能识别它所看到的。

偏见:也许系统更喜欢绿色的 M & Ms 或者德国牧羊犬，因为在“糖果”或者“狗”的训练数据中有一些微妙的趋势

伦理:这可能是更高层次的偏见，基于年龄、性别或种族的偏好。有时这是典型的两败俱伤的情况，两种选择都是有害的。

一个人工智能监督者几乎每天实时地防范这些类型的问题，直到把它们清除掉。有些问题比其他问题容易。当自动驾驶汽车研究人员意识到并非所有的交通标志都是全新的、明亮的时，一个更困难的问题出现了。阴影，树枝，风，划痕，丁丁，弹孔，贴纸，涂鸦和更多类型的缺陷存在于现实世界中。

## **复杂性增加**

不可避免地，人工智能监督者领导的解决方案的一部分是更好的场景规划和更多的训练数据。再培训成为一种生活方式，在某种程度上，更大的数据集也导致更复杂的实施和另一个挑战:速度-在进行再培训以纠正问题后，重新加载的实时分类引擎就像被困在糖蜜中一样运行，产生正确的结果为时已晚，毫无用处。

当 A 系统运行时，B 版本应该正在开发中，具有新的训练和分类器盒。对于非常大的数据集，团队应该考虑设计一个工作负载优化的培训服务器复合体，而不是依赖弹性云资源。这是 NVIDIA 最近收购 Mellanox 的背后原因——使用 InfiniBand 在人工智能服务器复合体中的 GPU 集群之间获得更多带宽。

训练系统通常是可伸缩的，而实时系统通常不是。它们针对尺寸和功耗进行了优化，只能接受这么多附加功能。当瓶颈出现时，它会扼杀整个应用程序。新一代的 CPU、GPU 和 FPGAs 不断推动设计师应对人工智能挑战。

## **人在回路中**

在许多用例中，人工智能系统的工作不是自主地做出每一个决定。相反，系统应该做出常规决定，并引导人工智能监督员查看异常情况。将人类快速引导到需要关注的区域通常比冒着做出错误决定的风险更有价值。开发团队应该更多地将人融入到系统中。

这听起来可能很明显，但它指出了开发人工智能与开发基于代码的算法之间的巨大差异。如果代码中有 bug，您可以调试它并找到需要修复的代码行。但是调试人工智能要困难得多。Digital twin 实现使用实际工作输入的回放来查看分类器黑盒内部发生了什么。在灾难来临之前，通常会有问题出现的迹象。运行好的和坏的数据有助于发现问题。

理想情况下，人工智能监督者是数据科学家和系统架构师的混合体。找一个既懂数据集又懂硬件实现的人，至少在高层次上。他们可能需要调用团队中的其他资源进行详细调查。

在开发一个系统的所有艰苦工作之后，你最不希望的事情就是让它在几个月或几年后变得疯狂。这只是墨菲定律。人工智能系统会在最糟糕的时候做一些完全意想不到的事情。人工智能监督员可以帮助 DevOps 团队提前解决人工智能问题。