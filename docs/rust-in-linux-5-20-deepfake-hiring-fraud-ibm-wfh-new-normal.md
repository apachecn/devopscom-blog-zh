# Linux 5.20 中的 rust | deep fake 招聘欺诈| IBM WFH“新常态”

> 原文：<https://devops.com/rust-in-linux-5-20-deepfake-hiring-fraud-ibm-wfh-new-normal/>

欢迎来到[![](img/599b9205c10137b1694ea55b577bc0fa.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周:Linus 表示下一版本将支持 Rust，FBI 警告骗子正在 deepfake 面试中被雇佣，80%的 IBM 员工呆在家里。*

 *## 1.Rust Language 将用于 Linux 5.20

本周的第一个消息是:Linux 的下一个版本将会在秋季包含对 Rust 的支持。莱纳斯·托沃兹听起来“谨慎乐观”，认为这件事会发生。

### 分析:但是值得吗？

一方面，Rust 使得[更容易编写安全软件](https://devops.com/aws-outage-outrage-rusty-linux-arm-latest/)——例如，没有免后使用错误。另一方面，Rust 有一个不成熟的工具链，并以构建**臃肿的可执行文件**而闻名。

Steven Vaughan-Nichols:**Linus Torvalds 对将 Rust 引入 Linux 内核的下一版本持谨慎乐观态度**

如果一切顺利，我们将在 2022 年 10 月底或 11 月初在 5.20 中看到 Rust。……你可能会问:“为什么？”… Rust 更容易编写安全的软件。托沃兹…喜欢 Rust 更安全的记忆。"有真正的技术原因，比如内存安全，以及为什么 Rust 进入内核是有好处的."
……
请注意，没有人会重写整个 3000 万行左右的 Linux 内核。…Rust 支持的三个潜在关注领域是利用内核中现有的 API、架构支持以及处理 Rust 和 c 之间的应用程序二进制接口(ABI)兼容性

通灵肯特·布罗克曼，这是[布鲁诺布拉克](https://linux.slashdot.org/comments.pl?sid=21593266&cid=62644458 "read the full text"):

我猜，欢迎来到我们的生锈超载。…我有点不愿意让内核生锈，但我想 Linus 知道得更清楚。…无论如何，内核中有 Rust 将是我学习它的一个很好的理由。

抑制你的热情，[二元香蕉](https://www.phoronix.com/forums/forum/software/programming-compilers/1329923-linus-torvalds-rust-for-the-kernel-could-possibly-be-merged-for-linux-5-20?p=1329946#post1329946 "read the full text"):

很好。我以前做过一些内核黑客，但我总是担心任何可能导致随机破坏的不可预见的副作用。Rust 的类型系统会有所帮助。我想知道驱动程序或更有趣的子系统(DRM/KMS、netfilter 等)会多快掌握它。).用 Rust 编写 ip/nftables 模块将会非常棒！

圭希尔认为，这只是一个精心策划的佯攻:

Linus 给了 Rust fanbois 足够的绳子去上吊，所以他们最终闭嘴了。…我们面临的主要问题是大量不称职的开发人员。

* * *

## 2.通过视频进行工作面试，有 Deepfakes

联邦调查局警告说，诈骗者正在使用窃取的身份和 deepfake 视频申请远程技术工作。显而易见的担忧是实际做这项工作的非熟练员工。不太明显的是来自那些不能通过背景调查的人的内部线索。

### 分析:远程工作的意外后果

受访者和来上班的人之间的差异并不是一个新现象。但是，如果“出现”是虚拟的，就不太容易发现这个骗局。

[Sergiu Gatlan](https://www.bleepingcomputer.com/news/security/fbi-stolen-pii-and-deepfakes-used-to-apply-for-remote-tech-jobs/ "read the full text") : **偷来的 PII 和 deepfakes 用来申请远程技术工作**

美国联邦调查局警告说，越来越多的投诉称，网络犯罪分子正在使用美国人窃取的个人身份信息(PII)和 deepfakes 申请远程工作职位。…这种合成内容以前曾被用于传播假新闻和制作复仇色情片，但缺乏关于其使用的道德限制一直是争议和担忧的来源。
…
目标远程工作包括技术领域的职位，这些职位将允许恶意行为者在受雇后获取公司和客户的机密信息。…一些受害者向联邦调查局报告说，他们被盗的 PII 被用来申请一份远程工作，他们还说，就业前背景调查信息被用于其他申请人的个人资料。

大汤匙说:[这是老问题的新进展:](https://news.ycombinator.com/item?id=31912757 "read the full text")

我之前的一个线索怀疑一个承包商为了一个面对面的角色做了这样的事情。我们只做了一两次电话面试……这个人做得很好，得到了一份 3 个月的合同。…出现的那个人似乎没有受访者知道的多，而且总是在打电话。[我们]推测，一些不择手段但相对有见识的家伙坐在那里参加面试，然后日复一日地指导不称职的申请人，降低他们的工资。
…
那段时间的很大一部分是在入职阶段，然后慢慢变得可疑。当我们带来承包商时，我们希望他们中的一些是无用的，这个家伙唯一有趣的是他的怪异行为。…最后他让合同失效了。…提出指控只会让你看起来疯狂和偏执。

归咎于 HR，kvetches [geekmux](https://slashdot.org/comments.pl?sid=21626520&cid=62659640 "read the full text") :

然而，没有人在乎，因为每个人似乎都采用了相当客观的过程。被烧伤？哦好吧。

【It’s】作为雇佣的成本而被驳回。…如果它变得过于繁重，他们会考虑自动化…在承认一个非个人化的过程是一个错误之前。

* * *

## 3.IBM 首席执行官说 80%的员工呆在家里

IBM 首席执行长阿文德·克里希纳(Arvind Krishna)对他的美国员工不回办公室一事听起来很乐观。回到立方体农场的人数少得惊人。

### 分析:谁会为 IBM 工作？

IBM 老板听起来对远离办公室的员工听之任之。但是蓝色巨人在员工士气方面有更大的问题。

[埃里克·罗森鲍姆](https://www.cnbc.com/2022/06/27/only-20percent-of-us-workers-in-office-three-days-or-more-ibm-ceo.html "read the full text") : **只有 20%的美国员工在职**

IBM 首席执行官最近的评论显示，许多大公司的员工更喜欢在办公室以外的任何地方工作。……Arvind Krishna 说，IBM 在美国的员工中，只有 20%的人每周在办公室呆三天或更长时间。在远程工作变得普遍之前，IBM 是第一批接受远程工作的大型科技公司之一。…但它最终改变了方向，要求员工在 2017 年再次在办公室工作。现在，范式又发生了转变。
……
他认为余额不会回到 60%以上。…“我想我们已经了解了一种新的常态。”

这在多大程度上是科技行业的趋势，在蓝色巨人工作是什么感觉？ [u/ibmgummies](https://www.reddit.com/r/IBM/comments/vk18u9/been_here_a_few_months_figured_out_ibm_business/ "read the full text") :

来了几个月，发现了 IBM 的商业模式:在不该削减的地方大力削减成本。通过提供非竞争性的医疗保健计划来尽可能地节省开支，最重要的是，尽可能地(在海外)外包，以使提供的服务低于标准。

哎哟。IBM 选择解决“[恐龙宝宝](https://devops.com/ibm-is-ageist-and-sexist-ibm-mainframe-aas-ibm-vaccine-mandate/)”年龄歧视投诉。这里是[詹姆斯·安德森](https://forums.theregister.com/forum/all/2022/06/27/ibm_age_discrimination_emails/#c_4484577 "read the full text"):

可能是股东诉讼的时候了。管理层烧钱掩盖他们的错误，如果我还傻到持有 IBM 的股票，他们会把我解雇。

* * *

## 这个故事的寓意是:

### 如果我们对自己诚实，我们就不会对任何人虚伪

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#4c38203a0c3e252f2425622f23623927733f392e26292f38716118001a61) 联系他。*

图片:[豪尔赫-西蒙斯-瓦伦苏拉](https://unsplash.com/photos/iCqMhGcW4HU)(via[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)*