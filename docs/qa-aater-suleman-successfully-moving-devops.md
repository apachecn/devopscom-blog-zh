# 与 Aater Suleman 的问答:成功迁移到 DevOps

> 原文：<https://devops.com/qa-aater-suleman-successfully-moving-devops/>

在关于 DevOps 实施的问答中，我们采访了总部位于奥斯汀的 IT 咨询公司 Flux7 的联合创始人兼首席执行官 Aater Suleman，该公司专注于云技术、DevOps 和高级开发。Suleman 的职业生涯始于硬件架构和性能优化，但近十年来一直从事云技术工作，并经常在 DevOps 和云开发活动上发言。苏勒曼也是奥斯汀德克萨斯大学的一名教师。

我们想问 Suleman 一些问题，关于他从 DevOps 实现中学到了什么，自从创建 Flux7 以来，他一直是 devo PS 实现的一部分。他就是那个采访者。

**DevOps:当你看到团队转移到 DevOps 时，你认为他们需要做些什么来推进良好的工作流程？**
**苏勒曼:**非常注重自动化和持续改进是必需的。为了取得成功，你需要非常谨慎地监控开发人员的工作流程。
单纯看建筑图，做平面图是不够的。你不能从图表中了解很多关于组织的信息。你当然想看看 IT 基础设施，但你需要与开发人员和 IT 团队成员就他们每天实际在做什么进行交谈。你会从这些面试中学到更多。当我们采访开发人员和 IT 团队成员时，从这些讨论中得出的结论令人惊讶。公司认识到，他们对员工的日常活动和工作流程并不像他们认为的那样了解。

DevOps:有哪些共同的经验教训？
**苏勒曼:**我们的一个客户最近请求我们帮助他们建立持续集成和持续交付(CI/CD)。我坚持要确保这是他们真正需要的。我们与业务主管进行了交谈，试图理解他们的业务需求，然后沿着企业和 IT 堆栈的其余部分前进。

通过这个过程，很明显，虽然 CI/CD 很棒，但是他们没有任何人有技能来设计自动化测试。因此，即使我们建立了自动化测试的框架，也没有 QA 人员能够编写这些测试。

另一件变得非常明显的事情是，他们的开发人员在他们的开发环境中经历了很多痛苦。他们试图执行基本的测试，但是他们没有有效的方法从他们的笔记本电脑上进行测试。

例如，开发人员登录到远程服务器进行测试，但是到服务器的互联网连接太慢，连接会中断。对于他们来说，按下一个键，长时间看不到结果是很常见的。

对于他们来说，这是一个非常令人沮丧的环境，他们无法完成任何类型的开发。这时，为这家公司建立一个健壮的开发环境就成了当务之急。

幸运的是，这是采访团队成员真正受益的地方，我们发现其中一个开发人员实际上已经创建了一个本地开发人员环境。他没有告诉任何人，只是在自己的笔记本电脑上使用它，但从未将其标准化用于整个企业。

有趣的是，尽管他们想转向 CI/CD，但他们还没有做好准备。更有趣的是，他们已经有了解决公司最大问题的方案，只是没人知道。

你认为企业经常失败的原因是什么？
**苏勒曼:** DevOps 的实现往往是非常流行的。人们听说过 CI/CD，他们想马上实现集成测试，因为每个人都说这是一件好事。

但是，您必须从业务需求和交付的角度来看您的具体需求以及您当前的首要问题。CI/CD 是一个很好的东西，我认为每个团队都需要它。但同样重要的是，要准确地看到你当前的挑战在哪里，并首先解决这些挑战。

此外，通常情况下，如果是一家中型初创企业，刚刚开始进入快速增长的“曲棍球棒”阶段，这些往往会成为非常有趣的评估。这时，公司有足够的灵活性来做出影响巨大的快速改变。这就是为什么对于公司来说，这也是一个非常重要的时刻。

在业务的这个阶段，评估的一个方面是这个基础设施团队是否真正理解企业对扩展能力的需求。我已经看到基础设施团队在等式的两端都犯了错误。有时，IT 团队高估了他们需要的扩展能力。他们从业务团队那里了解到，在他们扩展的同时，在其他地方还有更重要的挑战。

另一个极端是，有时，业务团队预见到需求的巨大增长，但 IT 更关注推出更多功能和部署更多功能，而不是扩展基础架构。我们无时无刻不在看到这种脱节。

**DevOps:当谈到能够更快地创新时，企业可以取得哪些轻松的胜利？**
**苏勒曼:**在 DevOps 环境中保持正常运行时间和可靠性也意味着你的 QA 团队对生产就绪负有更多责任，开发人员现在也需要搬出相对干净和正确的代码。

另一个方面是，开发人员仍然需要一个 IT 游乐场，以便他们能够创新。你想给他们提供适合他们的环境，这样他们就不会害怕尝试创造东西。这些环境需要速度快，并且需要像生产环境一样。它们应该是完全隔离的，并且易于重新创建，以便开发人员能够快速创新。如果他们打破了一些东西，错误的成本是非常低的，因为这是你创新的唯一方式，是通过降低失败的成本。

实际上，我们就是这么做的。因此，在一分二十秒内就完成了终止和启动一个新的开发环境。开发人员充分利用了这种能力。许多开发人员现在实际上每天都在多次重建环境。在拥有自动化开发测试环境之前，开发人员没有太多的创新，因为他们没有能力快速而廉价地失败。