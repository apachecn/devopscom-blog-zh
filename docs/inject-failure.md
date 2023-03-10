# 注入故障，使您的系统更加可靠

> 原文：<https://devops.com/inject-failure/>

将失败注入到基础设施中来测试服务的弹性越来越受欢迎。大多数人会想到网飞和他们对“混沌猴”的使用，事实上，他们有一整个“猿猴军队”的测试和演习，他们运行，使他们的系统更加可靠。在 PagerDuty，我们不能只是复制已经发表的关于他们的做法。相反，我们需要一种适合我们的方法。与网飞相比，我们的基础设施相对较小，我们希望开发一种实践来支持我们这样规模的团队。为了回应这种需求，我们创造了失败星期五。

背后的想法很简单:我们封锁一个小时的时间，故意关闭我们基础设施的某些部分，看看我们的服务如何维持。例如，我们的第一次攻击将测试流程故障。我们通常会运行类似“sudo service cassandra stop”的命令，让服务停止大约 5 分钟。此时，我们的服务应该有足够的弹性来继续处理流量。如果没有，将需要立即采取行动。当然，将故障注入我们的系统的主要目的是确定在节点、数据中心或网络中断的情况下会发生什么。然后，我们可以利用这些知识来提高基础设施的容错能力。

## 故意破坏系统的好处

从表面上看，将失败注入你的系统似乎有悖直觉。为什么要破坏你的系统，尤其是在每个人都要去享受周末的周五？自 2013 年 6 月开始每周故障测试以来，我们的结果揭示了许多好处，我们相信这为所有团队开发他们自己的故障测试场景提供了理由。

*   **发现可能降低弹性的实施问题。**我们有机会在此问题导致非工作时间警报中断之前解决此问题。
*   **主动发现我们基础设施中的缺陷。**这些缺陷可能最终成为停机的根本原因，让我们能够在它们失控之前解决它们。
*   建立强大的团队文化。通过每周一次的团队聚会，我们分享知识。我们的运营团队了解开发团队如何调试生产问题，而开发人员则更好地了解他们的软件是如何部署的。
*   帮助我们接纳新员工。 Failure Friday 使我们能够与新员工一起经历实际的故障和警报场景，以便他们能够跟踪并学习处理上午 11 点而不是凌晨 3 点的停机。
*   **调整提醒和待命时间表。**参与故障测试的团队成员应该收到意外停机期间会收到的所有警报。这是进行调整以限制噪音并确保您收到所有重要警报的绝佳机会。当我们收到警报，但不需要采取任何措施时，我们知道需要调整您的监控阈值。或者，如果我们没有收到警报，但我们需要采取行动，我们需要调整我们的阈值，这样我们就不会在下次错过该警报或类似的警报。
*   提醒我们失败是不可避免的。失败不仅仅是偶然的反常事件，它可能会发生。现在，工程团队编写的所有代码都要经过测试，看它们能否在周五故障场景中存活下来。

## 周五发展你自己的失败

当你考虑把你自己版本的失败星期五放在一起时，你必须记住团队之间的沟通是关键。如果由单个团队执行，失败星期五不太可能成功。

#### 第一步:将你的团队集合在一起。

让每个团队的关键涉众一起讨论彼此的测试需求，并决定测试什么。不可能测试每一个可能的场景，所以列出一个对每个人都有意义的优先事项清单会帮助你在短时间内完成很多事情。

#### 第二步:找一个对你的团队最合适的时间。

在 PagerDuty，我们选择周五进行一个小时的会议，因为周五的部署往往较少。这样，我们就不会在测试实践中给我们的业务制造任何障碍。由于这是一个经常发生的事件，公司里的每个人都可以预料到周五会发生失败，并做好准备。虽然星期五看起来是一个危险的时间，但是运行失败测试之后，你可能会发现潜在的威胁，从而度过一个安静的周末。

#### 第三步:建立作战室

拥有一个所有团队都可以坐在一起的公共场所，可以让你的团队无缝协作。他们还将通过观察和向其他团队成员学习如何解决事件而受益。为了执行传呼机任务，我们在用餐区的角落里搭起了帐篷。你不需要做任何花哨的事情。

#### 第四步:为你的第一次攻击做准备

在注入故障之前，我们将禁用计划在该小时运行的任何非关键 cron 作业。我们要攻击的服务团队将准备好他们的监控仪表板来跟踪变化，并在必要时采取行动。(注意:cron 作业被禁用，因为我们不想让它们干扰攻击。例如，我们不希望在关闭服务的过程中运行 Cassandra 修复。)

#### 第五步:建立你的沟通渠道

因为沟通在失败星期五是必不可少的，你会想用失败星期五来测试你的沟通渠道。使用聊天室是非语言交流信息的一种非常有用的方式。聊天室还提供了时间戳，因此您能够记录和检查所采取的行动，以便将任何行动与您在测试场景中可能捕获的指标相关联。

## 这完全是关于可靠性

当我们恢复正常运作时，失败星期五并没有结束。从我们的学习中，我们将在我们的票务系统中为团队成员分配行动项目(就像如果我们的系统真的发生故障时我们会做的那样)，从而使我们能够采取预防措施，以防止这些情况在野外发生。通过把人们放在一个房间里，向他们抛出问题，我们使我们的团队和我们的产品变得更强大。