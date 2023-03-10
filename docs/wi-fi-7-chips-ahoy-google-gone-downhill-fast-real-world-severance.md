# Wi-Fi 7 芯片 Ahoy |谷歌“迅速走下坡路”|现实世界的“断绝”

> 原文：<https://devops.com/wi-fi-7-chips-ahoy-google-gone-downhill-fast-real-world-severance/>

欢迎来到[![](img/3e5ae80e6953c8d5e74d851542630aa7.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周:Wi-Fi 7 的第一个芯片，谷歌的搜索质量“正在”失败，以及 *Severance* 告诉我们什么是伟大的辞职。*

 *## 1.全新闪亮的 802.11be 更好、更强、更快

本周首先报道:Broadcom 声称它是第一个推出新 Wi-Fi 7 标准芯片的公司(尽管“标准草案”更准确)。802.11 be 套件应该更快、更确定、受干扰更少并改善延迟。联发科和高通也有望于今年在 T2 推出硅芯片。

### 分析:不仅仅是速度的问题

所谓的“极高吞吐量”并不是唯一的好处。组合不相邻的频道——甚至跨越三个不同的波段——并支持 16 个空间流应该会在人口密集的地区带来巨大的质量改善。

[保罗·礼来](https://hothardware.com/news/broadcom-sampling-wi-fi-7-chips "read the full text") : **博通正在测试 Wi-Fi 7 芯片**

Wi-Fi 7 (802.11be)是下一代无线标准…随着 Broadcom 提供完整的端到端芯片组解决方案样品，wi-Fi 7(802.11 be)正式(在某种程度上)启动。…如果您被野外的所有无线标准弄得不知所措，也不要难过。就在不久前，802.11ac 还是霸主，然后是 Wi-Fi 6 (802.11ax)，不久之后，Wi-Fi 6E……利用了 6GHz 频谱。
…
Wi-Fi 7 的部分优势在于，理论上它支持高达约 46Gbps 的吞吐量，而 Wi-Fi 6/6E 的吞吐量为 9.6Gbps。[它]引入了一种称为多链路操作(MLO)的技术，这种技术使设备能够聚合信道并在它们之间快速切换，以挑选出不太拥挤的信道。…消费者和企业客户的净收益是…容量增加了五倍，延迟大大降低，覆盖范围更广。
……
不过，如果你刚刚升级到 Wi-Fi 6 或 Wi-Fi 6E，也不用担心。Wi-Fi 7 渗透市场还需要一段时间。

我只想让我的 AP 覆盖这所老房子的所有角落。[赞迪卡尔](https://news.ycombinator.com/item?id=31107512 "read the full text")解释了为什么这个行业没有走这条路:

[你]要求更高功率的设备相互干扰。…想象一下，如果每个人都有一个“智能”家庭，并且所有这些设备都在为相同的频谱相互竞争，那会有多糟糕。

更低的功耗、更低的延迟、更低的渗透率……以及更低的成本绝对应该是我们的目标。这并不是说高渗透无线没有用武之地……但在消费者使用案例中，这种情况很少，尤其是如果你可以运行一个负担得起的低功耗、低渗透的 meshnet，并且不会对你自己的设备或邻居造成干扰。

袖手旁观对于更无用的营销，认为 [kpb321](https://www.anandtech.com/comments/17346/broadcom-launches-wifi-7-portfolio-for-access-points-and-client-devices/770961 "read the full text") :

我知道他们想要/需要更大的数量来吸引更大更好的消费者，但是…那些速度的提高永远不会适用。…如果路由器支持多空间和 MU-MIMO，允许它在不同的空间流中同时与多个客户端对话，则总体性能可能会有所提高。…低延迟…和多链接的东西实际上看起来很有用…但它并没有提供大量的广告。

* * *

## 2.谷歌的搜索质量正在下降

很难忽视一个在 48 小时内有 3000 条评论的 Reddit 帖子。r/NoStupidQuestions 上一个简短、无辜的问题爆炸了，似乎**拨动了许多**的心弦。

### 分析:为另一个 SERPS 算法变化做准备

总而言之，答案似乎是，“是的:谷歌的搜索质量*已经*迅速走下坡路了。”而罪魁祸首呢？**搜索引擎优化的乱象**。

[u/PizzaInteraction](https://www.reddit.com/r/NoStupidQuestions/comments/u74vx6/does_anyone_else_think_google_search_quality_has/ "read the full text") : **还有人认为谷歌搜索质量下降得很快吗？**

感觉 SEO(搜索引擎优化)毁了 Google。除非你在寻找一些显而易见的东西，否则所有的搜索结果都是与你的搜索词无关的网站。当我输入四个搜索词，而所有的结果都集中在其中一个词上时，我总是会笑。……是的，谷歌，当我添加这些额外的术语时，我只是在瞎搞。谢谢你为我忽略了他们。
……
然后你只要输入“MX518”，所有的结果都是，“518 种给你的生活增添情趣的方法！”

如果莎士比亚笔下的屠夫迪克今天还活着，他会说:“让我们把所有的 SEO 专家都杀了吧”？这里是 [u/Healthy-Contest-1605](https://www.reddit.com/r/NoStupidQuestions/comments/u74vx6/does_anyone_else_think_google_search_quality_has/i5eh4qs/ "read the full text") :

就像资本主义一样，当没有人知道 SEO 是如何工作的时候，SEO 是很好的，所以系统通常会改善这种情况。然后每个人都知道了它是如何运作的，并滥用这个系统来让他们的产品/网站在顶部，以获得更多的广告浏览量。YouTube 也发生了同样的事情。
…
所以…我们得到了，“Buzzfeed 的崇拜者将一个四句话的段落变成了一个勉强连贯的单词沙拉，试图提到该关键词 50 次以上。”

谷歌的替代品怎么样？[大 _ 盲](https://news.ycombinator.com/item?id=31096858 "read the full text")已经试了几个:

我个人更换了搜索引擎，这使得编码、一般搜索和浏览互联网的速度提高了 10 倍。我试过像 DDG，勇敢的搜索，和凯奇夫妇。我开始使用 You.com，发现搜索结果比谷歌的好。更少的搜索引擎优化网站陷入搜索结果，网站过滤，优化结果布局。

* * *

## 3.伟大的辞职仍然是一件*事情*

复工令引发的摩擦继续引发火灾。正如我几周前提到的，在供需平衡的情况下，DevOps 工人觉得他们**掌握了所有的牌**。

### 分析:看不到尽头

DevOps 的减员率仍然很高。那么反乌托邦科幻能教会我们什么呢？Apple TV+系列， *Severance* ，一直在调侃**可怕的小玩意在**鼓励我们的想法。

[Elizabeth Spiers](https://www.nytimes.com/2022/04/14/opinion/severance-apple-tv-office.html "read the full text") : **关于将办公室津贴幼稚化的“遣散费”有哪些正确之处**

在 Apple TV+上播出的反乌托邦职场惊悚片《断绝》(Severance)中，有许多精彩之处，其中包括该系列发生地 Lumon Industries 提供的津贴。…很难不看到现实世界中的类似情况…特别是在大流行后的办公室欢乐时光和礼品卡赠品热潮中，因为公司试图吸引…员工回到办公室。公司察觉到一些员工不愿意回到办公室，这并没有错。…两年后，那些能够在家工作的人已经看到了真正的好处——从通勤中节省时间，灵活承担家庭责任，摆脱永久的分心和限制性的着装规范——现在他们无法忽视这些好处。…谁愿意放弃一天中因不用通勤去买咖啡杯而获得的两个小时呢？
……
并不是所有的公司都否认他们需要做些什么来让员工回到办公室；许多公司为远程工作和混合时间表提供永久的灵活性，并最终解决工作场所的歧视问题。…更大的背景也很重要。我们仍在经历一个疫情，乌克兰战争让所有人都更加意识到全球稳定是多么脆弱。

快来给我们你的[冷门观点](https://www.youtube.com/watch?v=Q1MvMTHmD9E)拜托，[国代](https://entertainment.slashdot.org/comments.pl?sid=21185840&cid=62461120 "read the full text"):

我很惊讶有多少人认为 IT 工作不是创造性的工作。事实上，大多数管理者似乎认为这是一项传送带式的工作——因此像敏捷这样的白痴行为时有发生。当面试官开始列举他们提供的所有“额外津贴”时，我开始嘲笑他们。我通常的问题是，“你的公司如何确保它不会妨碍我完成工作？”

哦，不，[西蒙诺兹](https://entertainment.slashdot.org/comments.pl?sid=21185840&cid=62461162 "read the full text")，你也是？

不要让我开始谈论敏捷——天哪。

等等。*暂停。*这是怎么回事？[戈登·弗里曼](https://news.ycombinator.com/item?id=31090293 "read the full text")记得:

刚刚看完《断绝》这部电影，非常激动人心，发人深省。…我不知道为什么没有更多人像谈论乌贼游戏那样谈论它。

* * *

## 
这个故事的寓意:**适度的怀疑被称为智者的灯塔**

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#becad2c8feccd7ddd6d790ddd190cbd581cdcbdcd4dbddca8393eaf2e893) 联系他。*

图片:[彼得·乌尔巴内克](https://unsplash.com/photos/RcBiV6ksfQ4)(经[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)*