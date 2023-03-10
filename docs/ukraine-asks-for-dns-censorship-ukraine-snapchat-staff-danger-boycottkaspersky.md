# 乌克兰要求 DNS 审查|乌克兰 Snapchat 工作人员危险| #抵制卡巴斯基？

> 原文：<https://devops.com/ukraine-asks-for-dns-censorship-ukraine-snapchat-staff-danger-boycottkaspersky/>

欢迎来到 [*的乌克兰周，远景*](https://devops.com/author/richi/)——我们在这里细读本周新闻，并将其剥离至要点。让我们弄清楚**什么才是真正重要的**。

本周:审查俄罗斯互联网，数百名乌克兰员工陷入恐慌，尤金·卡巴斯基表现得像个****。

## 1.ICANN，但是 IWONT

本周第一条新闻:乌克兰要求 ICANN 将俄罗斯从域名系统中删除。ICANN 政府咨询委员会的乌克兰代表 Andrii Nabok 认为，DNS 封锁将“帮助用户在替代域名区域寻找可靠的信息，防止宣传和虚假信息。”

鉴于今天莫斯科 K12 学生因向乌克兰大使馆献花而被捕的消息得到证实，这一目标似乎更值得称赞。但坦率地说，片刻的思考说这是一个**坏主意**。

### 分析:“网络将审查解释为损害并绕过它”

约翰·吉尔摩是对的。这样的举动将不可避免地失败。而且真的有不良的风险，**意想不到的后果**。

[Kat Bouza 和 Noah Shachtman](https://www.rollingstone.com/politics/politics-news/ukraine-icann-russia-internet-runet-disconnection-1314278/ "read the full text") : **乌克兰试图切断俄国的互联网**

乌克兰向互联网名称与数字地址分配机构(ICANN)提出的请求旨在撤销在俄罗斯发布的域名，并关闭该国的主要域名系统(DNS)服务器。(它)将向一个大肆进行数字宣传的政权发出一个强烈信号。
…
DNS 根区域是互联网整体功能的重要组成部分，负责处理对顶级域名的查询，例如。取消俄罗斯对这一服务器集群的访问将阻止俄罗斯互联网服务提供商进行通信。
……
但是……这个前所未有的要求有可能弊大于利。ICANN 的代表…拒绝置评。

但是这个要求很天真，这个[匿名懦夫](https://forums.theregister.com/forum/all/2022/03/01/ukraine_icann_domains/#c_4421981 "read the full text")认为:

他们所要做的就是让 ISP 给他们的 DNS 添加一个区域，上面写着“ru。在 NS x.x.x.x”中，然后对于他们的所有用户，任何对. ru 域名的请求都将被定向到 x.x.x.x

好吧，世界上的其他人会错过，但我怀疑他们会在意。

有更好的方法吗？[铠甲龙](https://tech.slashdot.org/comments.pl?sid=20891889&cid=62317699 "read the full text")喷火:

更好的办法是……要求西方认证机构撤销所有(俄罗斯)证书。然后要求主要的操作系统和浏览器供应商删除任何不符合的 ca。那会让 T2 真的和他们在一起，因为俄国对此无能为力。这甚至会影响俄罗斯与中国公司和中国客户做生意的能力。

* * *

## 2.Snap 300 名乌克兰员工的担忧

Snap，Inc——前身为 Snapchat——拥有一家乌克兰公司，该公司创造了用于实时视频恶作剧“[我不是猫](https://twitter.com/JudgeFergusonTX/status/1491399207793885186)”背后的技术它在**基辅和奥德萨**有数百名员工。

### 分析:团结不能停止战争，但是制裁可以

这个非常人性化的 DevOps 故事只是科技公司回应西方政府制裁的更广泛图景的一个脚注。这会给我们带来一点痛苦，但与乌克兰人感受到的痛苦相比，这算不了什么。如果它能缩短战争，那就值得了。

[J. Clara Chan](https://www.hollywoodreporter.com/business/digital/snap-snapchat-ukraine-russia-1235102170/ "read the full text") : **三百名 Snap 员工来自乌克兰**

Snapchat 的母公司……Snap 在一份公开声明中表示……Snap“最具创造力和才华的团队成员”中有 300 人来自乌克兰……这是 Snap 在 2015 年收购的增强现实平台 Looksery 的诞生地。……Snap 表示已承诺提供超过 1500 万美元的人道主义援助来支持乌克兰。…公司还为需要帮助安全搬迁的员工提供紧急援助。“我们声援我们的乌克兰团队成员和乌克兰人民。…这是一场毁灭性的冲突，具有深远的影响。…这是对我们许多团队成员及其家人的直接威胁。
……
“多年来，我们与乌克兰的同事和朋友一起工作，了解了乌克兰人民的创造力、力量和韧性。…我们将继续不懈努力，帮助我们的乌克兰团队成员及其家人，支持我们的 Snapchat 社区，并确定我们如何才能为正在进行的巨大人道主义努力做出积极贡献。"

据报道[科琳·瑞切特](https://www.cnet.com/news/snapchat-joins-tech-giants-in-halting-ad-sales-in-russia/ "read the full text")称，这是一种时尚:

在脸书、Twitter 和 YouTube 上周五开始暂停广告后，Snapchat 也采取了同样的行动，称在俄罗斯入侵乌克兰后，它现在已经停止了在俄罗斯、乌克兰和白俄罗斯的所有广告。Snapchat 应用仍在乌克兰、俄罗斯和白俄罗斯运行，[但] Snap 正在监控该平台，以防出现错误信息或其他滥用情况。苹果还停止了其产品在俄罗斯的销售，以及在线交易、Apple Pay 和一些苹果地图功能。谷歌暂时禁用了一些谷歌地图的实时功能，在搜索中添加了 SOS 警报，并屏蔽了俄罗斯国家控制的媒体。它表示，谷歌支付“可能会变得不可用。”

但是不要挂[大德“+++ATH”海斯](https://deadline.com/2022/03/snapchat-ukraine-halts-ads-from-russia-1234968436/ "read the full text") : *【问父母】*

就放弃广告机会所带来的任何财务损失而言，Snap 是否会面临如此大的风险尚不清楚。……尽管 Snap 在俄罗斯-乌克兰局势上的立场明确而强硬，但与许多科技竞争对手相比，Snap 也更容易接受这一立场。

* * *

## 3.叶夫根尼·瓦伦迪诺维奇·尤金·卡巴斯基选择了支持压迫者

卡巴斯基实验室有名无实的负责人因其对乌克兰战争的评论而公开蒙羞。与 Snap 的声明形成鲜明对比的是，他被指控公开保持中立，淡化战争的严重性——甚至被指控在某些营销活动中强行推销。

### 分析:#抵制卡巴斯基

德斯蒙德·图图是对的。但是，虽然“取消”Eugene 很有诱惑力，但请冷静下来，考虑一下您的安全状况。如果您在内部使用卡巴斯基产品，您的组织会面临哪些风险？俄罗斯政府会如何向**公司施加压力，迫使其破坏你的网络？**

[詹姆斯·库克](https://www.infosecurity-magazine.com/news/cybersecurity-reacts-kaspersky/ "read the full text") : **尤金·卡巴斯基的声明引发争议**

网络安全行业资深人士尤金·卡巴斯基(Eugene Kaspersky)激起了该行业领军人物的强烈反应。…总部位于俄罗斯的 IT 安全供应商卡巴斯基(Kaspersky)的首席执行官打破了他对冲突的沉默:
…
“我们欢迎开始谈判解决乌克兰当前的局势，并希望它们将导致停止敌对行动和妥协。我们认为，和平对话是解决冲突的唯一可能手段。战争对谁都没有好处。…在这种情况下，我们能做的主要事情是提供不间断的产品和服务。”
……
他将冲突描述为一种“情况”，并明显试图为自己的公司做广告，这引发了许多愤怒的回应。…在卡巴斯基的推文之后，出现了#抵制卡巴斯基的标签。

从平衡的角度来看，是[尼克·法雷尔](https://fudzilla.com/news/54456-kaspersky-sits-on-the-fence-on-ukraine "read the full text"):

卡巴斯基持观望态度……在俄罗斯，看风景不是一个好主意。(但)无论是谁在公关方面给卡巴斯基提供建议，都可能需要三思。毕竟，当一方向居民区发射导弹时，妥协并不总是可能的。如果他将同样的前提应用于勒索软件，他会建议…“你最好和劫持你服务器的人谈谈。”…卡巴斯基公司受俄罗斯政府的影响有多大？

你的店用卡巴斯基吗？[尼克·兰格](https://twitter.com/Nick_Lange_/status/1498612984096120837 "read the full text")开门见山:

我想提醒所有的读者，在战争的情况下，……能够访问公司并能在几个小时内同时在世界范围内更新的软件是一个很高的目标，会被专制政府强迫合作。

* * *

## 这个故事的寓意:**如果一头大象的脚踩在一只老鼠的尾巴上，你说你是中立的，老鼠不会欣赏你的中立。**

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#b5c1d9c3f5c7dcd6dddc9bd6da9bc0de8ac6c0d7dfd0d6c18898e1f9e398) 联系他。![](img/9ff0801a05401c655fdc3ecf267a1b20.png)*

图片:[布兰顿·莫拉莱斯](https://unsplash.com/photos/H887Atn5WPU)(via[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)