# 在传统企业中迁移到 DevOps

> 原文：<https://devops.com/moving-to-devops-traditional-enterprise/>

**简介**

在传统(即孤岛、瀑布等)企业环境中引入 DevOps 的挑战之一是从哪里开始。

这当然是我和首席技术官一起努力了很长时间的事情。

不可能传授多年来将一家大公司转变为 DevOps 思维方式的经验，但我希望给出我以前如何处理它的 3 个主要支柱。

注意…没有一个提到技术和工具！DevOps 主要是一种文化观念，因此对人们的影响最大。

**第一步——引入摇滚明星**

如果您的组织正在转向 DevOps，那么将来自不同筒仓的不同人员聚集在一起，然后期望他们(在他们自己的压力下)神奇地合作并就所有事情达成一致，这有点不现实。

如果你正在与历史团队和员工打交道——我怀疑你们大多数人都是如此——那么打破孤岛可能是一个重大挑战。

调整激励措施会让事情变得容易得多。例如，如果你的开发人员和运营人员都根据他们一年所做的“改变”的多少来获得奖金，这是让他们同意是否应该自动化发布的一个简单方法。这有点太简单了，但希望你明白我的意思。

不过，这很可能是以其他东西为代价的。在最后一个例子中，首先想到的是质量。

让我们把一切都直接投入生活吧！我们为此得到报酬！

好吧，这是行不通的。

有时，至少在开始时，你需要将人们聚集在一起，并最终授权某人在无法达成共识时做出决定。我已经看到了被委员会处死的真正危险。你召集的筒仓越多，他们不做决定的可能性就越大。

你可能听说过 DevOps rockstars 这个想法。从里到外了解 DevOps 的男人(和女人)。了解硬币各面的人(开发、数据库管理员、基础设施等)。

他们试图通过教育和说服来影响和引导人们走向正确的方向。他们帮助筒仓自己做出正确的决定，而不是自上而下的“照我说的做”。

总的来说，有时候这种开放的包容并不总是有效的，需要有人站出来参与进来。

那么我的观点是什么？

如果你想搬到德文郡，那就雇一个摇滚明星(顺便说一句，我怀疑洛德·斯蒂沃特是否合适)。以前做过的人。对什么是 DevOps 有非常成熟的认识的人，最好是完成了他/她试图影响的大部分工作的人。

此外，雇佣那些第一反应是试图让人们接受他们的思维方式的人。最后，有人最终不怕把自己的隐私暴露在危险中，做出一个该死的决定。

**第 2 步——看看你的人员结构**

DevOps 的传统定义是打破开发和运营之间的孤岛，以便它们实现共同的目标。

然而，我强烈主张 DevOps 不仅仅是 Dev 和 Ops(见 http://enterprisedevo PS . blogspot . co . uk/2014/07/devbiztestreleasesingyops . html)。

它是所有功能的集合，以实现有意义的改变。

开发人员、运营人员、业务人员和技术人员都应该有共同的目标和动机。如果可能的话，他们应该坐在同一张桌子周围。团队要集体起落(没有“我们和他们”)。团队应该从摇篮到坟墓管理变更(需求、构建、测试、部署、支持)。

我觉得应该把 Devops 改名为“DevBizTestReleaseThingyOps”。朗朗上口。

为此，DevOps 与“人”的关系比与新工具和流程的关系更密切。

考虑到这一点，你可能在谈论许多不同技能、经验和性格类型的人的一些相当激进的变化。我想这真的取决于你的组织结构，你的团队技能和许多其他因素。然而，对我的公司(一家大型英国保险公司)来说，这意味着一些根本性的变化。

我们首先将变更功能(开发人员、测试人员、BA 等)与单个业务单元(而不是单一的共享组服务)联系起来。

这种根本性的变化是在一些早期和小的成功的基础上发起的，通过实现持续集成和将其标记为“DevOps”之类的东西。好吧，这不是 DevOps，但如果使用这个术语开始在您的组织内获得可见性和运动，那么我不认为这是一件坏事。我一直认为我们需要一面部门现代化的旗帜。如果横幅上写着“DevOps ”,那就这样吧。

早期的小小成功对我们来说至关重要。

当我们刚开始的时候，我们有很多阻力和消极因素。

*   为什么你要告诉我怎么做我的工作？
*   你用错了工具
*   我看不出有什么好处
*   关于这件事，我知道的比你多
*   你要做的事情很简单
*   我们没有合适的人
*   对于脸书这样的人来说，这是一个时髦的想法
*   这种做法行不通是有监管原因的

基本上是天底下的一切。

当你试图做正确的事情并推动现任者前进时，这是有压力的。

我不认为我们一开始就帮了自己太多。我的团队中有太多的人试图学习和改变其他团队的技术和流程。带领另一个团队去饮水并帮助他们自己实现一些东西还不够。吸取教训。

**第三步——建立一个团队来帮助他人**

我之前提到过，DevOps 是一种文化理念，而不是一个职位头衔。肯定不是。难以想象。

我是如何管理一个“DevOps”团队的？想必那是一群“开发工程师”吧？！

我的团队“平台服务”支持我公司的变革平台理念。变革平台由诸如 Jenkins、Puppet、uDeploy、Teamcity、TFS 等工具组成。

有人最终需要“拥有”这些工具，确保它们得到维护，创建最佳实践并建立未来的路线图。

我的团队超越了这一点，帮助不同的变更功能适应变更平台，并且是 DevOps 和持续交付之类的事情的传播者。

DevOps 关心的是打破孤岛，让团队成为知识和技能的瓶颈是矛盾的。为此，平台服务是筒仓终结者——我们帮助其他人获得工具和流程并实施它们。

例如，我们自己不做部署，但是我们向其他团队销售好处，并帮助他们采用工具和流程。

我认为这是一个很好的模式，有助于在 IT 部门推广 DevOps 的成功。

我的人提供的咨询对 It 团队的其他部分实际上是免费的，这很有帮助(感谢开明的首席信息官和首席技术官)。

我希望你能从中找到一些有用的东西。请随意查看我的博客，关于我搬到 devo PS:[http://enterprisedevops.blogspot.co.uk/](https://enterprisedevops.blogspot.co.uk/)

祝您好运，如果您有任何问题或意见，请联系我们。