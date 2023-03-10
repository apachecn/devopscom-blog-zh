# devo PS Chat:vera code 的 Chris Eng 谈软件安全的现状

> 原文：<https://devops.com/devops-chat-the-state-of-software-security-with-veracodes-chris-eng/>

CA Veracode 每年都会发布“软件安全状况”报告，其中充满了关于软件在开发过程中和开发之后的安全状况的研究。这是令人大开眼界的东西，对于任何对帮助软件变得更安全感兴趣的人来说，绝对值得一读。

在这次 DevOps 聊天中，Veracode 的研究副总裁 Chris Eng 最近与我讨论了今年的报告发现以及一些值得注意的要点。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/518132022%3Fsecret_token%3Ds-LFbeX&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/518132022%3Fsecret_token%3Ds-LFbeX&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

艾伦·希梅尔:嗨，大家好，我是 DevOps.com 的艾伦·希梅尔，您正在收听的是另一个 DevOps 聊天。Veracode 的 Chris Eng 加入了我们这一期的 DevOps Chat。现在我很自豪地说，实际上，我认识克里斯，实际上，在 Veracode 出现之前。但是，这要追溯到一段时间以前。克里斯，我不记得你的确切头衔了，但你不是 Veracode 的研究负责人吗？

克里斯·英格:没错，是的。Veracode 的研究副总裁。

是的。欢迎你回来，克里斯。

英格:很高兴来到这里。

是的。所以，克里斯，你知道，我会假设，如果人们想知道你是谁，那就是克里斯·英格，你可以去找他。他是一个真正的网络安全战士，拥有长期的荣誉记录，是社区中的一个好人。除此之外，我想人们应该知道 Veracode 在过去的几年里，已经发布了一份名为“软件安全状况”的报告。实际上，这是第九卷，所以假设在那之前有八卷，对吗，克里斯？

没错。*【咯咯笑】*我们每年都这样做，它每年都变得更大更好。

是的。所以第九卷，你知道，现在是 CA Technologies Veracode，当然。一些变化。克里斯，这是你的孩子，对吗？你每年都负责这份报告，不是吗？

自从我们做的第一年起，我就一直参与其中。我的意思是，当然，回到早年，我们中很少有人分担负担，自己完成所有的写作。现在，谢天谢地，我们可以把它传播给更多的人，让更多的人关注它。这实际上是我们今年做的有点不同的事情之一，除了我们自己之外，我们还与 Cyentia Institute 的一些数据科学家合作，实际上帮助我们挖掘一些我们真正想要探索的东西，围绕补救工作并观察不同的组织行为。我稍后会谈到这一点。

绝对的。克里斯，在我们深入今年的细节之前，让我们花一分钟来谈谈，看，连续九年，我的上帝，世界在九年里发生了怎样的变化。对吗？今天早些时候，我与 Box 的首席信息官保罗·查普曼(Paul Chapman)进行了交谈，我们刚刚谈到了世界在过去 20 年甚至是过去 9 年中发生了怎样的变化。我的意思是，我们可以——你知道，安全仍然是安全，不幸的是，我们仍然有事故；我们仍然有易受攻击的软件；我们仍然有漏洞，在弥补漏洞方面有困难。但是游戏也变了，不是吗，克里斯？回顾过去，你认为最大的变化是什么？

英格:是的，它确实经历了巨大的演变。当我们在 2006 年开始 Veracode 时，应用程序测试主要是公司针对他们最关键的应用程序进行渗透测试，可能一年一次。而且，如果在这一年之间发生了任何变化，你知道，你可能只有一个时间点的评估。你有许多应用程序，许多软件，它们从来没有被测试过。从那以后，公司意识到，首先，他们需要更频繁地测试。这是他们能够发布安全软件的唯一方法，也是他们能够加快发布新功能和新产品的速度的唯一方法。对吗？

我认为，另一个认识是，您不能只关注对业务最关键的应用程序，因为攻击者并不真正关心他们是如何进入的，对吗？如果他们找到了一种较弱的方法，即通过一些较弱的应用程序更容易地进入，这些应用程序可能不是业务的核心，但仍然连接到相同的基础架构，那么他们会继续下去。因此，人们已经意识到，理解你所拥有的一切，并在生命周期的所有阶段实际构建软件测试和安全测试是非常重要的，对吗？早点修理，会比以后修理便宜得多。

而且，您知道，我们前几天查看了一些统计数据，这些数据没有出现在报告中，但是为我们的客户进行第一次百万次应用程序扫描花了 10 年时间；第二百万次扫描花了一年时间。

**Shimel:** 哇。

**Eng:** 对吧？如此巨大的增长率表明，在所有行业、所有规模的公司中，组织都意识到他们必须扩展他们的软件安全计划以覆盖所有的基础。为了不增加安全债务，他们必须持续这样做。所以我认为这将是我们解决这个问题的最大变化。

希梅尔:我同意。我同意。但是，克里斯，真的，我们的时间有限。让我们进入今年的报告。我已经快速浏览了一遍，内容提要和其他一些东西。为我们的听众总结一下。你认为他们应该注意的三个最大的衡量标准或事实是什么？

英格:是啊。让我给你一个简单的-

Shimel: 当然可以。

**Eng:**–回顾–就像我说的，我们每年都这样做。我们收集了大约 12 个月的数据，涵盖了我们为所有客户进行的所有评估，当然是匿名的，然后我们观察趋势，尝试了解应用程序安全性方面的情况。这个数据集是在 12 个月内大约 700，000 个应用程序评估，我们这次能够做的一件大事是，我们过去不能做的事情实际上是查看缺陷一旦被发现会持续多长时间。对吗？组织修复这些缺陷需要多长时间？

因此，当我们检测到某些东西时，我们能够在多个评估中跟踪它，假设我们今天扫描一个应用程序，我们发现了一堆缺陷，我们修复了其中的一些而没有修复其他的，然后我们在一周内再次扫描它。我们能够识别那些我们第二次检测到的缺陷，和第一次检测到的是一样的。这样我们就可以跟踪每个缺陷的生命周期，直到它被修复，对吗？所以我们可以看看“有缺陷的持久性看起来像什么？”一种生存能力分析。

而且，如果你从整体上看，就我们看到的所有缺陷而言，这些数字并不是很大。完成 25%的调查结果平均需要 21 天，完成中间点需要 121 天，完成 75%的调查结果需要 472 天。所以那是一段很长的时间，对吗？这已经过去一年多了，所以总体情况并不乐观。因此，我们对此进行了细分，你知道，一旦报告出来，人们可以看看“根据不同的严重性和不同的行业，这看起来像什么？我们在那里看到了什么样的模式？”但我认为最有趣的，也是你们最感兴趣的，是 DevOps 或 DevSecOps 对 fix velocity 的影响。

现在，对于任何给定的应用程序，我们都没有一种简单的方法来判断“这是不是 DevOps 商店？”对吗？我们不能-我们没有这些信息，所以我们必须弄清楚我们是否认为他们是，我们一直使用的代理是扫描频率，对吗？如果你在做 CI/CD，你已经将扫描融入了你的构建过程，或者你已经以某种方式将它融入了你的自动化。因此，举例来说，如果你在做一个夜间构建，你每天晚上都要做一个测试。因此，我们查看了扫描频率，以确定–您知道，我们认为这些每年被扫描 300 多次的应用程序可能是 DevOps 商店，对吗？而那些一年扫描一到三次的，可能不会。

所以我们把它分解成桶。如果你面前有这个，你想跳到第 39 页，这是图 43，这是我真正想做的，这是一种，我们的假设是，“是的，我打赌 DevOps 商店修复得更快，因为他们扫描更频繁，他们不想积累太多的安全债务。”事实上，它确实表明。对吗？我们在报告中看到这样一行文字，“一年被扫描 300 次或更多次的应用程序正在修复，他们在五天内到达修复的中间点，并在七天内关闭了 75%的缺陷。”对吗？这比我刚才向你们描述的平均值要好得多。

我们按桶来分类，对吗？所以你每年有 300 多次扫描，你有 51 到 299 次，一直到每年 1 到 3 次扫描，这需要将近 4 年的时间才能达到 75%的接近度。所以我认为这实际上是——这是我们希望看到的。这是我们期望看到的。但很高兴看到数据证明，事实上，是的，当你经常扫描时，当你早期扫描并保持在结果之上时，这实际上是一件非常可行的事情，对吗？在合理的时间框架内修复缺陷。

绝对的。有两件事，克里斯。第一，我认为与 DevOps 齐头并进的是自动化。

英格:是啊。

**Shimel:** 对吧？我想知道，在支持 DevOps 的文化和组织中，组织文化，无论是什么，进行 DevOps 的公司，他们是否正在自动化扫描流程，这就是为什么我们看到他们进行 300 多次扫描？对吗？然后他们会部署更多，如果他们的维护对象，如果他们的标准流程是“不先扫描就不部署任何东西”，对，这就是你开始累积 300 多次扫描的地方。对吗？我的意思是，当你-

英格:哦，是的。是的，我们——

**Shimel:**–将其构建到您的管道中，对，将其构建到您的 CD 流程中，这些扫描就完成了。

**Eng:** 是的，我们假设这些——你知道，我们已经——我认为，在最大程度上，有一个应用程序被扫描了超过 1000 次，当然，那是——我的意思是，我真的希望那不是人类上传东西或按下—

*【相声】*

**Shimel:** 右，_ _ _ _ _–点击“扫描”按钮–

**Eng:**–每次一个按钮对吧？

**Shimel:**–每次。你希望不会，对吗？

**Eng:** 对。没错。我假设即使是那些一年扫描 50 次的，对吧，我假设是每周扫描一次，我假设那些也是-

*【相声】*

**Shimel:** 还是一次比一次好 _ _ _ _ _—

**Eng:**–_ _ _ _ _ _ _ _ _ _ _ _ 通过构建管道。对吗？而且，任何时候你都可以——我的意思是，这一直是我们的一大焦点，一般来说，就是“我们如何消除进行测试所需的任何人力？你如何让它变得更简单、更透明，并消除任何障碍？”所以--

**Shimel:** 不，见鬼，你怎么——你必须将它纳入你的 CI/CD 渠道。我是说，这是其中的一部分。就像你呼吸空气一样，对吗？如果你停止呼吸，你就死了；你不能部署未经测试和扫描的软件。并且–

**Eng:** 对。没错。

克里斯，你知道，我们谈论这个听起来很简单，但事实是这样的，对吗？在我们的听众中，并不是每个人都像你或我一样在安全领域工作了这么长时间。很多人看到报告，克里斯，他们说，“哦，我的上帝，这是第九年，”我忘了威瑞森做了多少年的报告，每年，很难显示一些事情的进展，对不对？我们确实展示了“嘿，如果你扫描得更多，你会有更少的漏洞没有被修复，至少它们不会留下来，你知道，它们会更快地被修复。”

英格:是啊。

**Shimel:** 但事实是我们仍然看到——Chris，你看看这里的执行摘要，情况并不乐观，因为你——我想这是你自己说的。我们每天仍会看到违规事件，这里有 3000 万条记录，这里有 2000 万条记录。你知道，不安全的人说，“我们要做什么？这种情况何时会发生根本改变？”

是的，我的意思是，事情不会在一夜之间得到解决，对吗？我的意思是，如果公司只是在几年前才意识到他们需要处理他们拥有的所有事情，并开始了解他们的风险状况，并且他们已经有了 10 年、20 年、25 年的软件价值，数以千计的应用程序，这不会在一夜之间发生；这是一小步。当然，在启动任何新的绿地项目时，如果有一个适当的 SDLC，能够尽早发现并解决问题，将会防止它们累积更多的安全债务。

但是，是的，很多这些——我解释其中一些事情的方式——例如，OWASP 前 10 名的通过率没有得到很大改善，或者某些缺陷类别的流行，如跨站点脚本和 SQL 注入，保持相对稳定——是一些更成熟的应用程序已经被扫描了一段时间，这些应用程序实际上正在减少。如果我们把它们分开，我们会看到比率下降。但是，从整体来看，在这 700，000 个应用程序中，有许多是首次扫描到的。因此，他们将更容易遇到这些问题，而更成熟的应用程序已经解决了这些问题。对吗？所以它们相互平衡。

我们每次都看到这种情况。事实上，我们可能应该开始单独报告其中的一些事情——这是一件很难做到的事情——但我认为正在发生的是一些较新的应用程序正在提高这些数字，这就是为什么我们看到线条保持相对平坦。还有很长的路要走，但我们确实看到了——你知道，还有我刚才描述的 DevOps 补救案例。我的意思是，我们看到了乐观的小点，你可以看到某种行为和某种结果之间的明确关联。因此，我们喜欢专注于这些东西，是的，大多数公司需要一段时间才能真正开始清除遗留应用程序并将其锁定。

绝对的。绝对的。克里斯，我们快没时间了。我应该——我们应该把这个放在那里:对于那些对这份报告感兴趣的人来说，他们可以从哪里得到它呢？去 Veracode.com？

英格:它将于 10 月 24 日在 Veracode.com 上映，而且，他们可以在那里下载。这里有大量的。我们把它分成不同的缺陷类别。我们将不同的行业进行对比。甚至还有一点地理上的细分，当然，就像我提到的，围绕缺陷持久性和组织修复缺陷需要多长时间的大量数据，我的意思是，最终，这才是重要的，对吗？如果你不修理东西，不管你扫描多频繁。对吗？除非你解决问题，否则你不会降低风险。因此，在这方面有很多很好的数据，我们以前从来没有能够报告出来，所以我们真的很高兴能够得到这些数据。

绝对的。克里斯，你知道吗？我知道我对你有点苛刻，这不是你的错，安全行业也不是安全行业，因为，上帝知道，我们想解决导致这些违规的问题；这实际上只是软件的状态，以及安全性在这些组织中作为优先事项的位置，以及管理其风险等等。

但是，出于同样的原因，克里斯，你知道吗？首先，谢谢你，谢谢你，谢谢你，每年都参与进来做这个报告，不管这些指标描绘了一幅美好的画面还是一幅悲伤的画面，然而，这是一幅需要被讲述的画面，对吗？我们需要这种洞察力；我们需要这些指标来了解我们所处的位置以及我们需要达到的位置。再一次，非常棒的工作，把这些放在一起。你知道，我认为非安全人员阅读这些报告和安全人员一样重要。对吗？真的——

是的，我们希望——

**Shimel:** 至-

是的，我们肯定希望人们能从中得到一些东西，并希望能利用这些东西来思考他们是如何建立自己的项目的，对吧——他们是如何补救的，他们的数字是什么样的——并希望能告诉人们不同的组织是如何考虑扩大他们的项目的。不管怎样，这是我们所希望的。

**Shimel:** 好。好吧。克里斯，我们就到此为止吧。这里是周五下午。再次感谢您对报告的深刻见解。感谢您年复一年地管理这份报告，参与其中并提供帮助。我们很快会再见的。我们即将进入会议季；我相信您将会忙于展示和获取更多信息——

英格:我确定，是的。我相信我们很快就会相遇。

绝对的。Chris Eng，CA Technologies Veracode 的研究副总裁，我们本期 DevOps 聊天的嘉宾。各位，这是艾伦·希梅尔。祝你愉快。

— [Alan Shimel](https://devops.com/author/ashimmy/)