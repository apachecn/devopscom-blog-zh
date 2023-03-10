# 脸书工作怎么样？他们不知道！|卡利。支付法| NASA RISC-V 发射

> 原文：<https://devops.com/facebook-fail-cali-pay-law-nasa-risc-v-richixbw/>

欢迎来到[![](img/7f79857c224e6131d94924fd14a6413c.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周:脸书的工程师承认他们不知道什么是 Meta stores(或在哪里)，加州要求招聘广告引用工资，RISC-V 将为未来的 NASA 航天器提供动力。*

 *## 1.Meta 的“奇怪的工程文化”

本周首先:没有人真正知道脸书是如何运作的了。“代码是它自己的设计文件，”一位**工程总监**坦白道。

### 分析:他们动作很快——他们打碎东西

这就是你不预先设计的后果。Sprints 和 Scrum 是超级的，但是*敏捷*不能成为不记录设计的借口。上个月说过: **[敏捷烂](https://devops.com/agile-sucks-devops-mars-richixbw/ "Agile Sucks (Redux)")。**

萨姆·比德尔 : **脸书的工程师不知道他们把你的数据放在哪里**

**`Facebook’s sprawl has made it impossible to know`**拥有……20 年经验的工程师们，甚至都在努力探索脸书子系统中可能储存的东西。“我不相信有一个人能回答这个问题，”脸书工程总监尤金·扎拉肖回答道。“与大多数在工程过程中不生成大量工件的公司相比，我们有一种有点奇怪的工程文化。实际上，代码通常是它自己的设计文档。”[他]和软件工程经理 Steven Elia 将脸书描述为一个如此复杂的数据处理设备，以至于无法从内部理解它，一个不可知的机器。脸书的扩张让人无从知晓。…该公司从未费心培养关于这些组件系统如何工作、它们做什么或谁在使用它们的机构知识。…脸书数据存储系统的模糊性使得回答最基本的问题都是徒劳的。

他们是认真的吗？ [kixiQu](https://news.ycombinator.com/item?id=32751130 "read the full text") 不敢相信:

就法律合规性和安全性而言，“这只是分层和有机增长”，不是你能说的。如果我们在喝咖啡休息时思考这样的事情，也许我们会得到这里给出的那种答案，但是如果对于法规遵从性所必需的东西没有一个单一的引用，人们就会被呼叫直到它出现。在我看来，找出如何满足系统刚开始时不存在的新需求完全是工作的一部分。…遵循法律就是赌桌赌注。…对用户数据进行真空处理是一个*的选择*。…这不是不可避免的。…这是一个令人尴尬的难题。

但是这个[匿名懦夫](https://tech.slashdot.org/comments.pl?sid=22017561&cid=62861153 "read the full text")得出了显而易见的结论:

欢迎来到敏捷！BDUF——大设计先行——是整个“快速行动，打破常规”哲学的敌人，这种哲学被像脸书这样的公司错误地应用于软件开发。

* * *

## 2.招聘广告必须说明加州的工资范围

作为无数 DevOps 商店的所在地，加州将通过法律强制在招聘广告中公布工资。人们希望增加的透明度将缩小**性别和种族之间的薪酬差距。**

### 分析:一个像埃利奥特·内斯一样碰不得的国家

在黑暗的沙漠公路上:黛西·杜克斯，比基尼在上面。我甚至会亲吻一头**夕阳猪**。

[杰西卡·盖恩](https://eu.usatoday.com/story/money/business/2022/08/30/california-law-salaries-pay-gap-women/7945920001/ "read the full text") : **加州通过法律要求公司披露薪酬**

**`California joins other cities and states`**
美国州议会周二通过一项法律，要求该州所有雇主公布空缺职位的薪资范围。…加州州长加文·纽瑟姆必须在 9 月 30 日之前签署或否决。国家推动薪酬透明的背后是什么？薪酬公平。加州的一项研究发现，2020 年，在类似职位上，女性比男性少挣 460 亿美元。有色人种的工资比白人工人低 610 亿美元。
……
加州联合其他城市和州颁布法律，强制雇主交出更多薪酬信息。……联邦立法……去年被参议院共和党人阻止，他说《薪酬公平法案》将主要惠及出庭律师，而不是女性。

简单的解决方案:公布 1 美元到 1，000，000 美元的工资范围。根据 T2 的说法，这是行不通的:

该法案要求您根据要求向劳工部提供支持您声称范围的记录。…你可能必须证明所有人都在做同样的工作，这对于员工、经理和高管等来说是个问题。

撇开平等不谈，法律能帮助人们吗？[提示 pc](https://forums.theregister.com/forum/all/2022/09/06/california_lawmakers_pass_bill_requiring/#c_4527077 "read the full text") 这么认为:

这肯定会帮助求职者知道是否要去申请。我讨厌那些对薪资范围不坦诚的招聘人员。我的第一个问题是，“多少钱？”然后，“哪里？”如果他们不想回答 Q1 的问题，那就和我说再见。…从一开始就知道薪水可以节省我们所有人的时间。

* * *

## 3.RISC-V 将为未来的美国宇航局宇宙飞船提供动力

开源指令集架构 RISC-V 将成为 NASA 下一代高性能航天计算(HPSC)的基础。“核心 CPU”将由 SiFive 基于 **RISC-V ISA** 设计。

### 分析:RISC-V power 击败 POWER power

这对 RISC-V 国际非营利组织和该技术的粉丝来说是一个重大的推动。权力移交的舞台已经搭好——rad 750 的形状被用于航天器，如**毅力号和 JWST** 。

[Liam Tung](https://www.zdnet.com/article/nasa-has-chosen-these-cpus-to-power-its-next-generation-of-spaceflight-computers/ "read the full text") : **美国宇航局选择 RISC-V 芯片设计师 SiFive 帮助更换其老化和过度设计的航天计算机**

**`Important win for the open-source RISC-V`**
美国国家航空航天局 6 月宣布，其 HPSC 项目将开发新的飞行计算技术，其计算能力将是当前航天计算机的“至少 100 倍”，这些计算机是近 30 年前开发的。…旧的航天计算机的主要问题是它们设计过度。
…
si five 表示 X280 已经展示了 NASA HSPC 所需的 100 倍速度提升，非常适合在功率受限的情况下需要高吞吐量、单线程性能的应用。…这些 CPU 需要能够抵抗辐射损坏，以最低功耗运行，并在不需要时关闭。12 年前，加州大学伯克利分校的 David Patterson 和 Krste Asanovic 教授发明了开源的 RISC-V(发音为“risk-five”)标准，这是一个重要的胜利。与主导个人电脑和服务器的英特尔 x86 的封闭 isa 以及 Arm 有限公司授权的 ARM 指令不同。

确实重要。 [omegalulw](https://news.ycombinator.com/item?id=32743371 "read the full text") 是超级粉丝:

我绝对喜欢美国宇航局正在做的这*和*鼓励 RISC-V 生态系统。…一种开源的硬件替代方案，其影响力堪比 Linux 在软件领域的影响力。

但是为什么不是手臂呢？这个[匿名懦夫](https://forums.theregister.com/forum/all/2022/09/06/nasas_spaceflight_computer_risc_v/#c_4527458 "read the full text")知道为什么:

早在 2000 年到 2010 年早期，ARM 就非常热衷于涉足航天工业。他们做了相当多的内部 R&D，完全自费，并有专门的销售经理、产品经理和航天工业开发团队。尽管他们尽了最大努力，但从未赢得一份*单*合同。…‘大约在 2012-2013 年的 IIRC，ARM 实际上放弃了航天工业。

* * *

## 
故事的寓意:**国王万岁**

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#087c647e487a616b6061266b67267d63377b7d6a626d6b7c35255c445e25) 联系他。*

本周最长的长视角:[美国宇航局](https://www.nasa.gov/image-feature/goddard/2022/nasa-s-webb-delivers-deepest-infrared-image-of-universe-yet)*