# AWS 保存乌克兰数据| WPF“还没死”| Devs 为现金退出

> 原文：<https://devops.com/aws-ukraine-russia-wpf-devs-quit-richixbw/>

欢迎来到[![](img/29acf8e4b52ec4b989beac6eb3cf87f7.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周:亚马逊 S3 正在保护乌克兰的数据安全，我们问 Windows Presentation Foundation 是否已经死亡，开发者告诉我们他们为什么跳槽。*

 *## 1.AWS 雪球边缘隐藏来自俄罗斯的数据

本周的第一件事是:大量乌克兰政府数据被悄悄地移除并储存在亚马逊网络服务中。[坦南鲍姆是对的](https://www.goodreads.com/quotes/7298190-never-underestimate-the-bandwidth-of-a-station-wagon-full-of "“Never underestimate the bandwidth of a station wagon full of tapes hurtling down the highway.”"):一堆 80 TB 的雪球边缘 S3 单位已经泄露了 **1 万 TB 的重要数据**。

### 分析:普京在云端的数据

在现代战争中，数据可能成为目标。有远见的政府领导人意识到了这一点，并采取行动防止其损失给敌人。

[Russ Mitchell](https://www.latimes.com/business/story/2022-12-15/amazon-ukraine-war-cloud-data "read the full text") : **亚马逊如何把乌克兰的‘政府’放进盒子里——并从俄罗斯手中拯救了乌克兰的经济**

**`You can’t take out the cloud with a cruise missile`**乌克兰 31 岁的数字化转型部长米哈伊洛·费多罗夫说，迄今为止，这些 1000 万千兆字节的数据代表着“关键的信息基础设施……对经济、税收系统、银行和整个政府的运作至关重要”。总部设在伦敦的亚马逊网络服务公司的政府转型主管利亚姆·马克斯韦尔(Liam Maxwell)已经与乌克兰合作多年，直到今年 1 月，俄罗斯计划进攻的事情才变得明朗起来。…装在防震灰色容器中的雪球装置从都柏林空运到波兰的克拉科夫。他说，然后乌克兰人“偷偷把这些装置运过了边境”。
……
数据还包括……人口登记、土地和财产所有权记录、纳税记录、银行记录、教育登记、反腐败数据库等等。…数据下载完成后…每个雪球都装载着高达 80tb 的加密数据，被运回亚马逊。……“用巡航导弹是打不出云的。”

这个[匿名懦夫](https://tech.slashdot.org/comments.pl?sid=22588186&cid=63143548 "read the full text")苦思原因:

不管你喜欢还是讨厌亚马逊，事实是，将数据转移到国外的物理存储意味着，这比把数据保存在俄罗斯物理入侵和攻击的国家内部的网络上要安全得多。俄罗斯可以用 SRBM 炸掉乌克兰的数据中心，但他们绝对不敢炸掉法兰克福、巴黎、伦敦和爱尔兰的 AWS 数据中心。亚马逊在防范国家支持的黑客方面也有丰富的经验，因此他们在保护数据数字化方面几乎肯定比乌克兰做得更好。…这需要企业中的多个人都受到影响。

带着必须的零食，是 [TheOtherOne](https://forums.tomshardware.com/threads/amazon-saved-over-10pb-of-vital-ukrainian-data-using-snowball-edge-ssds.3789598/post-22886234 "read the full text") :

构建天网的第一步？…在一个地方保存世界上所有政府的数据。

* * *

## 2.生命支持的 Windows 演示基础？

微软和 WPF 搞什么鬼？微软高级项目经理 Olia Gavrysh 上周散布恐慌，称其为一个社区运营项目。

### 分析:又一个 Windows 用户界面死胡同

我已经数不清有多少半废弃的、半生不熟的、不兼容的微软框架。这似乎更多的是关于在雷德蒙的产品所有者的自我，而不是实际开发者的需求。

蒂姆·安德森 : **微软令 Windows 桌面开发者担忧**

**`Microsoft has struggled to establish a successor`**
一个微软。NET 社区的支持让 Windows 桌面开发人员想知道该公司为……Windows 窗体和 Windows 演示基础(WPF)计划了什么样的未来。一张“最新消息”幻灯片[显示]“社区运营项目”作为第一个要点，引起了与会者的惊愕。这张幻灯片可能被误解了。它旨在更新来自社区的 pull 请求。……然而，对框架未来的担忧是有充分理由的。…但是管理一个广泛使用的项目从来都不容易。
……
为什么开发者还在用这些老框架？Windows 窗体可以追溯到。NET 在 2001 年，WPF 在 2006 年从 Windows Vista。问题是，微软一直在努力建立一个具有开发人员生产力和能力的良好组合的后继桌面框架。…发展的步伐一直很慢。……信息似乎是，这些框架对微软不再具有战略意义——除了作为它渴望继续发挥作用的遗留技术。

对开发者来说，这是一个生活质量的问题，[托马拉西](https://news.ycombinator.com/item?id=34028816 "read the full text")说:

WPF 总是觉得未完成和错过许多生活质量的特点。我希望他们会进一步完善，使它更容易工作，但我想它从来没有打算。…我对 Windows 生态系统上的用户界面开发感到非常困惑。在我想开发桌面应用的罕见场合，我使用了 Avalonia UI，它似乎……比 MSFT 每一两年粗制滥造的东西更稳定，强烈推荐。他们每隔几年就推出一个新的框架，但在进入下一个框架之前，总感觉只完成了一半，这真的是在破坏 Windows 生态系统。当然，总体来说，这是在 Windows 版本的基础上，他们如何堆积新的半成品 UI 返工，这只是不断堆积疯狂数量的技术债务和未来维护的遗产。

这是另一张 Avalonia 的选票，由[荷兰枪](https://developers.slashdot.org/comments.pl?sid=22596486&cid=63145820 "read the full text")投出:

Winforms 和 WPF 可能会在某些时候被弃用，但有太多这样的应用程序，不用担心微软会真的取消对它们的支持。这只是意味着未来只会有最低限度的维护。本机 Win32 应用程序也是如此。
…
我已经基本上不再依赖 MS 作为 UI 框架了。…我的下一个个人项目可能会使用 AvaloniaUI。他们称之为 WPF 的“精神继承者”(但是)开源和跨平台:Windows，Mac，Linux，Android，iOS。

* * *

## 3.开发商调查结果出来了

StackOverflow 一直在询问开发人员他们的跳槽计划，以及他们留下或离开的动机。我不认为你需要成为统计学博士来解读结果。

### 分析:没有人对调查感到惊讶

开发人员为了更多的钱、更好的灵活性和发展机会而跳槽。我知道，我知道:停止媒体。祝大家节日愉快。

[Liam Tung](https://www.zdnet.com/article/three-quarters-of-developers-are-willing-to-quit-for-a-new-job-and-its-not-just-about-the-money/ "read the full text") : **四分之三的开发者愿意为了新工作而辞职**

根据 StackOverflow 对 2600 名开发人员的调查，积极寻找下一份工作的年轻开发人员的比例比去年增加了 9 个百分点。StackOverflow 调查中约 54%的受访者表示，在考虑新机会时，更高的薪水是最大的激励因素。薪水固然重要，但它不是找新工作的唯一动力。…开发人员还希望获得在家工作的灵活性和选择，46%的人认为在精确的时间开始/结束一天的工作或者希望在办公室工作(44%)是他们当前角色的最大缺点。

马嘴？艾琳·叶皮斯:

过去的一年是技术专业人员重新评估和寻找机会的一年。…2022 年 10 月，我们调查了 2，600 多名技术专业人员，以了解更多关于开发人员的需求和期望。年轻的开发人员更有可能积极寻找他们的下一个角色。…年轻求职者的增加…表明一波新的技术人才准备进入劳动力市场。
……
虽然工资仍然是开发人员的主要动力……但对新技术的渴望成为第二大离职原因。[而]灵活性(58%)、薪资(54%)、学习机会(54%)……说服他们留在目前的岗位。…受访者表示，关注开发人员体验(42%)、公司正在销售的产品或解决方案(35%)以及向团队以外的个人学习(34%)是公司更具吸引力的首要因素。

等等。*暂停。*这其实是*新闻*吗？cuda13579 听起来有点讽刺:

多么令人震惊的消息！还不如说“有工作的人愿意接受更好的工作。”

* * *

## 这个故事的寓意:
**每个人都想出名——但是没人想做这个工作**

*—凯文·哈特*

*你一直在读*Richi Jennings 的《长观*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#5420382214263d373c3d7a373b7a213f6b2721363e313720697900180279) 联系他。*

图片:[以赛亚·麦卡蒂](https://unsplash.com/photos/3inCeNKjGbM)(via[Unsplash](https://unsplash.com/license "Some rights reserved")；*