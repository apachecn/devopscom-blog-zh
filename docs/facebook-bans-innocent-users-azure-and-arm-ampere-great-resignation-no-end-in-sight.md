# 脸书禁止无辜用户| Azure 和 ARM/Ampere |“大辞职”——看不到尽头

> 原文：<https://devops.com/facebook-bans-innocent-users-azure-and-arm-ampere-great-resignation-no-end-in-sight/>

欢迎来到[![](img/192e179aefc763c8958ca3d10035f1ea.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周:对被禁的脸书用户没有任何补救措施，微软 Azure 上基于 ARM 的新虚拟机，以及大辞职在可预见的未来仍将是一件事。*

 *## 1.“您的脸书帐户已被禁用。这个决定是无法逆转的。”

本周第一条新闻:脸书用户在无缘无故地被阻挡在 Meta 的社交粪坑之外后开始反抗。一个明显的错误信息提高了无数无辜者的压力水平。

### 分析:不要像脸书一样

不要让制裁自动化。或者，如果必须的话，至少要有一个健壮、高效的流程来审查关于**假阳性**的投诉。

[简·韦克菲尔德](https://www.bbc.co.uk/news/technology-60959811 "read the full text") : **脸书用户无缘无故账户被锁后怒不可遏**

世界各地的脸书用户一觉醒来，发现自己的帐户无缘无故地被锁定了:……“您的脸书帐户被禁用，因为它不符合我们的社区标准。这个决定是无法逆转的。”…没有任何警告或解释。Meta 的安迪·斯通说:“我们知道一些用户在访问他们的脸书账户时遇到了问题，我们正在努力尽快解决这些问题。”他没有说有多少人受到影响，也没有说问题是什么。Jen Roberts 就是其中一个发现自己被锁在账户之外的人。…尽管她不是一个狂热的用户，但发现自己的账户被锁定仍然令人不安:“我大学时代和家庭聚会的所有照片都在脸书上。我将不再有机会……这是真正的悲哀。不知道问题出在哪里，又没有解决问题的方法，这也是一种相当大的压力。”

算法审核很难，哟。但是这更糟糕，正如 [gurps_npc](https://tech.slashdot.org/comments.pl?sid=21087484&cid=62413748 "read the full text") 解释的那样:

问题不在于锁定，而在于“不可审查”人们可以接受错误“定罪”的风险，其他人也会接受这种风险。但是没有人喜欢被告知“不上诉”是的，上诉程序很昂贵，可能不值得[但是]没有上诉程序是一个非常糟糕的主意。这意味着你提供的是****而不是有价值的东西，傲慢得不可信，最重要的是你鄙视你的选民。

留意[u/无名之辈](https://www.reddit.com/r/technology/comments/tubwao/comment/i340fb2/?utm_source=reddit&utm_medium=web2x&context=3 "read the full text")的经历:

脸书…完全没有客户支持。…大多数现代公司现在至少有一个即时获得帮助的聊天系统。[关于]脸书，你可以提交一个请求，得到零反馈。或者在几个星期后得到计算机生成的答案。没有来回尝试解决问题的机会。

* * *

## 2.手臂上的蓝色:更快、更绿、更酷

微软对 ARM 是认真的。正如我在之前[说过的，ARM 芯片在云和本地数据中心越来越重要——尤其是那些看重**“性能功耗比”的数据中心**](https://devops.com/css-tricks-sells-out-peloton-spins-out-arm-axes-1000/#tlv3 "ARM Axes 1,000")

### 分析:有什么不喜欢的？

无论你的客户是 Linux 还是 Windows，Azure 都是不可知的。库伯内特是国王。凭借扩展到 64 个内核、208 GB 内存和 2.4 TB 固态硬盘的能力，这款**可不是玩具**。

玛丽·乔·福利 : **微软为 Azure 带来 Arm 支持**

4 月 4 日，微软通过与 Ampere Computing……一家制造服务器芯片的初创公司的合作，宣布了 Azure 虚拟机上 Arm 支持的预览。[它]将提供比基于 x86 的同类虚拟机高 50%的性价比。
…
预览版最初在美国西部 2、美国中西部和西欧 Azure 地区提供。Dpsv5 和 Epsv5 Azure VM 系列采用基于 Ampere Altra Arm 的处理器，工作频率高达 3.0GHz 新 VM 提供多达 64 个 vCPU，包括每个 vCPU 2gb、4gb 和 8gb 内存配置的 VM 大小，高达 40 Gbps 的网络，以及可选的高性能本地 SSD 存储。
……
【他们将】支持 Canonical Ubuntu Linux、CentOS 和 Windows 11 专业版和企业版。…对其他操作系统的支持正在进行中，包括 Red Hat Enterprise Linux、SUSE Linux Enterprise Server、Debian、AlmaLinux 和 Flatcar。

奥利·安迪科指出，这是一个加速发展的趋势:

AWS Graviton2 与此类似:AWS 表示，Graviton2 的性价比比英特尔高 40%。他们将 vCPU 与 vCPU 进行比较，例如将 8 核英特尔处理器与 16 核 ARM64 处理器进行比较。但是那个 16 核 ARM64 还是*便宜*。
…
功耗也大大降低(即使内核数量是以前的两倍)。因此，就可持续发展而言，ARM 是赢家。

但是有一只苍蝇在[黑暗](https://slashdot.org/comments.pl?sid=21093950&cid=62418384 "read the full text")的美中不足:

可惜他们只支持 Windows 和 Linux。…计算世界不仅仅是这两个内核。例如，BSD 拥有强大的 Aarch64 支持，并且从第一天起就得到 VMware ARM 产品的良好支持。他们也在 AWS 和 OCI 上工作。微软，请加强你的支持游戏！

* * *

## 3.WTH？我们仍然想要 WFH

一项新的研究表明，员工不想回到办公室，或者至少不想回到他们讨厌的工作。在供需平衡的情况下，他们觉得自己掌握了所有的牌。

### 分析:短期内不会有变化

正如我们在一月份所看到的，DevOps 的消耗正在以惊人的速度增长。三个月过去了，对于喜欢亲身体验的人来说，事情也同样令人沮丧。一位评论者称之为回到办公室的“虐待狂折磨”正在严重地集中员工的思想——包括 DevOps 专业人员。愤世嫉俗、低价值的激励不会让**改变主意**。

[卡根·科奇](https://www.bloomberg.com/news/articles/2022-04-03/great-resignation-isn-t-slowing-and-may-persist-randstad-says "read the full text") : **大辞职没有减缓，可能会持续**

大规模辞职没有缓和的迹象，工人供应的减少可能会持续下去。…在长期人口趋势的支撑下，就业市场中的人数减少，这使得有才华的员工有了更多的选择——他们会去自己的需求得到满足的地方。从疫情反弹回来的经济和在家工作的选择，使得员工更容易辞掉没有吸引力的职位，寻找其他工作，从而推高了工资。…在任仕达的调查中…超过一半的千禧一代和 Z 世代受访者表示，如果工作让他们无法享受生活，他们会辞职。相比之下，刚刚超过三分之一的……婴儿潮一代。
……
83%和 71%的受访者认为弹性工作时间和工作场所很重要。(但)随着新冠肺炎案例的减少，越来越多的公司把员工叫回办公室，至少在一周的部分时间里。

雇主应该做些什么？免费赠送！安德鲁·j·霍金斯:

谷歌准备本周让员工回到办公室。作为额外的奖励，它将为他们提供免费的电动滑板车，以帮助他们轻松过渡。…员工还必须每月至少使用代步车九次，才能全额报销其每月订阅费。在疫情颠覆工作模式的两年后，雇主们加倍投资办公地产，这使他们与习惯于在家工作的员工产生了冲突。…而且，为了以防发生任何摩擦，谷歌已经表示愿意花钱提供额外津贴，以吸引员工回来。

每月 44 美元的福利够吗？我猜[风暴掠夺者](https://tech.slashdot.org/comments.pl?sid=21093940&cid=62417938 "read the full text")代表了很多人的心声:

没有什么能让回到办公室的虐待狂折磨比灵魂粉碎更轻。所有公司的办公空间都应该卖掉。…个人工作空间是一个时代错误，需要从轨道上清除。

* * *

## 这个故事的寓意:
**没有比诚实更丰富的遗产了。**

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#abdfc7ddebd9c2c8c3c285c8c485dec094d8dec9c1cec8df9686ffe7fd86) 联系他。*

图片:[董杰克](https://unsplash.com/photos/FS07gIT-hss)(via[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)*