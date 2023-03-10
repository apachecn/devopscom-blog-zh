# 一个小贩去了 Monitorama

> 原文：<https://devops.com/a-vendor-guy-goes-to-monitorama/>

I attended my very first [Monitorama](http://monitorama.eu) this year, in Amsterdam, and I have thoughts!![Monitorama Amsterdam](img/fe65c5c5036d0b7cc456bf47f149e20b.png)

Monitorama Amsterdam

首先，当你为监控和可观察性领域的供应商[工作时，在 Monitorama 发言是非常奇怪的，但你并不是作为赞助商。即使在最好的情况下，这也很奇怪，但 Monitorama 的观众是下一级的。他们对高技术含量的内容非常满意，所以他们很快就会对(他们认为的)营销垃圾感到恼火。“在杂草中”甚至不能开始描述它；大多数人从未听说过作为企业 IT 生活一部分的各种东西(AIOps、Netcool、Patrol 或任何我们通常怀疑的东西)，但是，另一方面，我遇到的每个人都可能会就哪种监控工具最糟糕进行长达数小时的争论。](http://www.moogsoft.com)

事实上，我想说 Monitorama 的亮点之一是走廊轨道上的对话。这是所有推动这个行业的推特代言人——我的意思是，“有影响力的人”和“思想领袖”——聚集的地方。如果你能和他们边喝咖啡或啤酒边交谈，两者都很自然，就能真正交流思想。我知道我从那些小组聊天中学到的东西可能和在大舞台上的演讲一样多。我希望我能够分享一些观点作为回报。

见鬼，虽然听起来很荒谬，但就连着装规范都是一个挑战。在我以供应商身份参加的活动中，基本上有两种速度:西装革履的战斗服或印有我雇主标志的 t 恤。这两种情况在包装时都不需要太多考虑。不过，Monitorama？我不再穿着我在系统管理员时代的旧 Thinkgeek 衬衫，但如果我打着领带出现，我会被嘲笑出房间。

## 准备

我回应了论文征集的号召，提出了分布式系统的人工智能。以下是我的摘要:

> The IT industry is in the middle of one of its regular swings between centralization and decentralization, driven by increased automation of the network fabric itself, as well as new use cases such as IoT. With more and more processing and autonomy devolved to the edges, old assumptions about how to manage and operate a network have to change. It no longer makes sense to try to forward all the edge alerts to a central location for analysis, but central visibility on the health of the network is more important than ever.
> 
> 人工智能支持的可观察性的新技术有望帮助 NOC 团队为其网络用户提供更好的体验，而不需要过多的手动工作或对运营团队的个人生活造成严重影响。机器学习使知识能够在最有用的时候被捕获并在上下文中可用，从而加快事件解决并改善用户体验。

我的第一个障碍是，尽管我每个月至少有一到两次公开演讲的机会——而且已经做了好几年了——但我通常会打着雇主的旗号出现。这个事实有利也有弊。从积极的方面来看，我通常可以依靠我(和其他人)过去创建的大量幻灯片库。我有一些已知的高音，我的目标是达到这些高音，结尾的行动号召非常明确(“试试我们的东西”)。硬币的另一面是，因为观众至少在某种程度上意识到这些因素，我必须更加努力地工作来赢得他们的注意，因为他们认为他们是被卖给了。作为一名供应商发言人，我也多少受限于自己的古怪和古怪程度——尽管我总是试图突破界限。在去年的一次演讲中，我谈了几分钟自行车，让组织者惊愕不已，直到他们弄清楚我在做什么。

因此，我花了一段时间苦读一个热门的主题演讲，观看往届 Monitorama 的视频，咨询业内人士，我尊重他们的意见，并对自己在阿姆斯特丹的表现非常满意——以至于在 monitor ama 开幕前一晚，我在 de wilderman 的[逗留的时间可能比我应该逗留的时间要晚。](http://indewildeman.nl/index.php?lang=en)

> ![](img/1413a2aa84378dd9aa694f57988a88e7.png)
> 
> 我刚刚在[@ un tapd](https://twitter.com/untappd?ref_src=twsrc%5Etfw)上赢得了“Bierproeflokaal In de Wildeman”徽章！【https://t.co/niR1D1UxqyT2[#英德威尔曼](https://twitter.com/hashtag/indewildeman?src=hash&ref_src=twsrc%5Etfw)
> 
> —多米尼克·🇪🇺(@ dwellington)[2018 年 9 月 3 日](https://twitter.com/dwellington/status/1036701148902825990?ref_src=twsrc%5Etfw)

## 准备不足

周二，随着一个接一个的发言人走上讲台，我在座位上越陷越深，意识到我完全没有说到点子上——似乎这还不够糟糕，我演讲中的几个关键类比已经被第一天的发言人使用过了。我确实去了在 [Delirium Café](https://deliriumcafeamsterdam.nl/en) 的聚会，但是很早就离开了，去睡那个紧张的演讲者的不眠之夜。凌晨时分，我放弃了这个糟糕的工作，花了几个小时基本上根据我所看到的重写了我的整个演讲。天知道我的邻居对我排练台词有什么看法，尽管我试图压低声音。

这是在 [Slideshare](https://www.slideshare.net/DominicWellington/how-ai-helps-observe-decentralised-systems) 里的结果，或者你可以在这里看视频[。该链接应该会带您找到正确的时间戳，如果没有，请滚动到大约 5 点 30 分。](https://youtu.be/_AgJnYLQkiU?t=5h31m49s)

Katja Budnikov 也在做惊人的 sketchnotes(现场！)的所有发言。这是我的一个会话:

![](img/c158b58610df0cd9b50e7e7b38d4c098.png)

## 减轻

![](img/1a76b99df5d2a7d71cb79e08ead87695.png)

> 在 [#Monitorama](https://twitter.com/hashtag/Monitorama?src=hash&ref_src=twsrc%5Etfw) 的舞台上。现在都完成了。深呼吸。😊【pic.twitter.com/FmGQd7AdHV 号
> 
> —多米尼克·🇪🇺(@ dwellington)[2018 年 9 月 5 日](https://twitter.com/dwellington/status/1037335885048688640?ref_src=twsrc%5Etfw)

In the end it seemed to go down pretty well. I did my level best (honest!) to call on my own now-obsolete experience as a practitioner and on conversations with people who are more current than I am with the nuts and bolts of modern IT, rather than relying on the crutch of vendor boilerplate, and I think I was mostly successful in that.

如果你正在为一家供应商工作，并考虑在这种活动中提交论文，无论是 Monitorama、DevOpsDays 还是配置管理营，我都建议尽可能广泛地测试你的内容。作为一个演讲者，你可能有很多下意识的反应，不适合这些活动吸引的观众。即使你意识到了它们，也很难完全根除它们，但要尽力而为。

另一方面，虽然我非常尊重 Monitorama 与会者的技术水平，但他们中的一些人似乎有失去全局跟踪的风险。我不希望 Monitorama 改变其作为技术人员会议的性质，但我很高兴我们有一些超出这种模式的演示，我希望我能够提供一些背景知识，说明所有精彩的技术是如何在这个糟糕的世界中使用的。

多米尼克·惠灵顿