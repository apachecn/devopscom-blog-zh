# 持续播客:开源中的冲突

> 原文：<https://devops.com/continuous-clash-open-source/>

欢迎来到 To Be Continuous，这是一个关于持续交付和软件开发的节目，由 CircleCI 的创始人 Paul Biggar 和 LaunchDarkly 的首席执行官 Edith Harbaugh 主持。在这一集里，伊迪丝和保罗谈论了开源软件中寻求付费的开发者和寻求免费的软件公司之间的冲突。

这个播客是由 heavy bit(T1)带给你的，这是一个帮助以开发者为中心的公司将他们的产品推向市场的项目。

[soundcloud url=”https://api.soundcloud.com/tracks/244279037?secret_token=s-oeBCP” params=”auto_play=false&hide_related=true&show_comments=true&show_user=true&show_reposts=false&visual=false” width=”100%” height=’166′ iframe=”true” /]

伊迪丝:保罗，你喜欢开源的什么？

保罗:所以我想这取决于我们是在谈论编写开源软件还是将开源软件作为公司的一部分。写开源，我喜欢把我所有的代码放在外面。

我会尽可能经常这样做。每当我开始写一点代码，一个小的库，我都希望开源它，有一个自述文件，让其他人使用。我进行了很长时间的讨论，最终我赢了，关于…

伊迪丝:我喜欢你认为所有讨论都是输赢的方式。

保罗:嗯，是啊，是啊。更多的是讨论中的争论。但是和我写的 PHP 编译器的其他合著者，最初是 GPL。我非常强烈地争辩说，我其实不在乎人们是否回馈，我只是希望人们使用我的软件。所以对我来说，开源是让人们使用我的软件的一种方式。

伊迪丝:那真的很有趣。所以，我喜欢你在开头说的话，比如，你喜欢开源，因为这意味着更快地发布东西。因为我很喜欢这个。

就像，我总是说你应该发表东西。比如，我的联合创始人约翰上周在我们的团队会议上说了一些非常好的话。他说，如果已经完成了 90%而你没有发表，那实际上就是 0%完成了。

保罗:是的，已经完成了百分之 0。

伊迪丝:是的，这是一个很难的教训，因为你最近总是追求完美。

保罗:对，对，对。嗯，我认为这也有一些不好的方面。所以当你在某个东西准备好之前发表它，在你真正——

伊迪丝:嗯，准备好了。

保罗:好吧，有现成的现成的，但是让我们假设现成的是，假设你在阐明软件要做什么，或者软件的价值观或使命之前发布它。

然后你会看到一些贡献者说，“哦，这很棒，但是我真的希望它能做其他的事情，”你会说，“嗯，这不完全是我想要的。”

伊迪丝:嗯，我得说大多数开源项目都很幸运，能够得到贡献者。

保罗:真的，真的，真的。所以我举个例子。我为 Closure 编写了 V8 绑定。所以一个允许你写 JavaScript 并在 Closure 中运行的绑定。我这么做纯粹是出于自私，另一个原因是为了我正在建造的一条名为 Stefan 的新生管道。

然后人们来了，他们想用它做其他事情。他们会说，‘好吧，让我们给这个东西加一个绑定。’我就像是—

伊迪丝:嗯，这有点像一个支点。

保罗:是的，是的，但是我真的对它不感兴趣。

我更希望有人接手它，接手这个项目，并实际上带着它去他们想去的地方，我可以坚持旧版本，或者我可以看看新版本是否为我解决了它，但我对成为这个东西的维护者不感兴趣，我感兴趣的是解决我的痒。

我只是碰巧开源了它，因为我觉得它可能对其他人有用。

伊迪丝:保罗，我不想这么说，但我同意你的看法。

保罗:不，又来了。

伊迪丝:又来了。不，我的意思是，我认为你说的完全正确，你说，我这样做是因为这个原因，我想让别人现在接管它。

> 我认为当开源遇到人们喜欢的问题时，它只是这个目的，除了我最初的东西，你不能用它做任何事情。

保罗:你认为这是好事，还是有问题？还是在社区中引起问题？

伊迪丝:我认为开源被滥用于如此多不同的目的，以至于很难说。比如，所以，在欧洲，人们说开源是好的，因为它意味着自由软件。

**保罗:**免费还是免费？

伊迪丝:对不起？

保罗:免费的啤酒或免费的，那另一面是什么？

伊迪丝:天下没有免费的午餐，你是这个意思吗？

保罗:不，不，不，就像人们说的开源软件，它就像啤酒中的免费软件，就像没有成本的软件，没有价格标签的软件，他们用法语单词 libre 来表示—

伊迪丝:哦，对了，这就是我说的。我记得我在 2004 年或 2005 年去了欧洲，他们大力推动开源，因为他们认为这意味着免费。

保罗:哦，这就像是德国政府之类的。

**伊迪丝:**就像字面上的意思一样，所以我去找这位顾客，他们说，‘所以你不用再为我们多花一分钱了。’那么，为什么不应该是免费的呢？

保罗:哦，好的，是的。

伊迪丝:所以我认为开源已经被许多企业滥用了，他们认为开源就像是，嘿，我们让所有的开发者免费工作。

保罗:所以我认为开源商业的主要优势不在于它是免费的，而在于它的低风险。

**伊迪丝:**低危？

**保罗:**降低风险。所以它移除了—

伊迪丝:啊，我认为—

保罗:嗯，我的意思是，它消除了一定的风险。Joss Belsky 写了一篇博文，关于你不应该使用，我认为这是一个你没有源代码的数据库。

伊迪丝:好吧，所以我会反过来说，我认为开源有时风险更大。因为我现在跟一些人说，没有人维护我所依赖的这个开源项目。

保罗:对，对，对。但这与闭源版本相比。

伊迪丝:那么，相反的风险是，你最终要对这个开源项目负责，你会说，嗯，实际上，我只是想用这个东西。我不想做维护工作。

**Paul:** 当然，你不想成为唯一一个使用这个东西的人，事实上，成为唯一一个使用这个东西的人是很好的。

伊迪丝:嗯，不，不是—

保罗:不太理想。

**伊迪丝:**就是很多人在用，但是没人付钱，然后你就卡了。

**保罗:**因为没人维护。

**伊迪丝:**没有人在维护，你依赖它。

保罗:对，但是想象一下，没有人维护它，你所能得到的就像一个二进制块。这才是真正的问题。公司倒闭了。你有随机数据库第七版，二进制的，只能在 32 位上运行，你在维护，就像公司在维护 COBOL 一样—

三十年前的 Fortran 语言。它在机器里，你不能碰它，不能修复它，不能对它进行安全更新。

伊迪丝:是的，这很公平。蒂姆·周，他是一个很棒的人，他是早期的甲骨文，他说人们不买，当他们买软件时，他们买的不是今天的东西。

保罗:对。

伊迪丝:因为基本上，你今天买的任何东西，你只需要雇佣 20 名工程师就能制造出来。他们在买什么—

保罗:对，你可以直接复制。

伊迪丝:是的，他们买的是稳定的承诺，这种承诺将继续保持下去。有一个愿景。实际上，我找到了一个大客户，他还不让我们使用他们的名字，但是他们说他们喜欢 LaunchDarkly，因为我们每天都在考虑功能标志。

保罗:对，对，没错。这就是人们购买情景应用程序的原因，因为，因为人们整天都在想 CI、QA 即服务、队列，或者我刚刚游说的各种重量级公司的任何东西，他们是，你可能通过查看主页就能自己找出他们是哪些。

伊迪丝:顺便说一句，保罗，非常感谢你今天穿上你的黑色 t 恤。看起来很帅。

保罗:我绝对同意这东西的好处是你每天都用它。但是你也可以通过开源来做到。你可以有开源软件，例如，我们的前端是开源的。

Edith: 哦，我绝对是开源的粉丝。比如，我们每天都使用开源软件。我们的客户端库是开源的。我不是说这是，我不认为这是一个宗教的事情，开源与不是，我只是认为很多时候人们假设开源是它不是的东西。

保罗:对，很公平，很公平。

伊迪丝:我的意思是，如果你有开源软件，那就意味着开发者愿意并乐意每天更新你的软件。

保罗:绝对是喜忧参半。如果真的发生了。

**伊迪丝:**我记得，所以我记得当孙，所以我曾经工作，我曾经在 Epicentric，我们有一个门户服务器，我们杀了孙。绝对要杀了孙。那是在 2003 年，所以他们说，‘哦，我们要把我们的门户服务器开源。’

保罗:对。

伊迪丝:所以不知何故，这整件事，我们就像，一切都将是开源的，就像，开发人员将从地下冒出来，就像，嗯，不，开发人员，他们不会每天醒来就像，'我要做你的东西。'

保罗:对，对。如果性感或刺激，他们会的。有很多开发人员出现在 Mozilla 上只是为了做出贡献。事实上，他们克服了难以置信的巨大障碍，为 Mozilla 的软件做出了贡献。

伊迪丝:嗯，这很有意思，因为我经常看到相反的情况，人们，你怎么看待 Mozilla 让人们愿意做出贡献？

保罗:我认为这是一个开源第一的公司，而且是一个非盈利性的公司，它的一切都是关于免费和开放的网络之类的东西。此外，我在火狐的时候，人们已经对火狐有了很好的体验，大概十年了。嗯，也许七年，但是，你知道。

**伊迪丝:**这很有趣，因为我昨晚和 MySQL 的首席执行官共进晚餐，我不知道我是否应该这么说，但他说—

保罗:这是貂皮米克？

伊迪丝:是的。所以他做了一个演讲—

保罗:他有一家新的创业公司？

**伊迪丝:**叫哈克罗内？

保罗:哦，他加入了 HackerOne。

伊迪丝:是的，他是新的首席执行官。所以晚餐对他来说有点像初次社交舞会。

保罗:很好，很好。

伊迪丝:所以他说有人直截了当地问他 MySQL 有多少是来自贡献者的。他说百分之一。

保罗:看起来差不多。

伊迪丝:他说开源不仅仅是一个品牌的事情。好像这不像是一件生产力的事情。这不仅仅是一个品牌的事情。

**Paul:** 所以在 Mozilla 中也有这种情况，任何时候只要有真正热心的贡献者，Mozilla 就会雇佣他们。

伊迪丝:是的，他是这么说的。

保罗:对，如果 Mozilla 没有雇佣他们，他们通常就不再是贡献者了。就像，这是一把真正的双刃剑。

所以有人做了六个月，他们是出于对这项运动的热爱。他们这样做不是为了被雇佣，至少我认为在大多数情况下，他们这样做不是为了被 Mozilla 雇佣。然后六个月后，有人会说，嗯，你知道，你做得非常好，难道你不想全职工作吗？他们说，是啊，太令人兴奋了。他们坐飞机去面试了。然后就像，你知道，实际上，我不这么认为。

伊迪丝:等等，他们不想为 Mozilla 工作，还是 Mozilla 不想雇佣他们？

保罗: Mozilla 不想雇佣他们。我是说，这不是特例。但是你知道，Mozilla 不想雇佣某些人。然后会发生什么？嗯，你可能不想继续为那个让你滚蛋的公司做贡献。

是的，我是说，这是真的。我是说，我认为志愿服务很人性化。

保罗:对，对。

**伊迪丝:**我是一名志愿者，我曾长期担任 Lean Startup Circle 的主持人，后来新来了一个人，他们说，是的，我想筹集一些资金，这样我们就可以得到报酬，我说，他们付不起我的工资。

就像，我做这个不是为了得到报酬，因为—

保罗:是的，这就像是人们正在努力做的利他主义。

伊迪丝:是的，我每周贡献 10 到 15 个小时，以我现在的速度，我这样做不是为了得到报酬，我这样做是因为我喜欢回报。

**Paul:** 我们之前谈过这件事，关于人们在开源中获得报酬的讨论。

伊迪丝:是的，我认为推动开源的很大一部分是整个 20%的时间。比如，谷歌会给他们的工程师 20%的开源费用，我知道其他大公司，比如 Twitter 等等，也是这么做的。所以这些人，本质上，得到了报酬。

保罗:对，对，在大多数公司里，至少在大多数初创公司里，都有一条潜规则，那就是你应该为你的应用程序中的库做出贡献，诸如此类的事情。如果你花时间在你已经部署的上游路径上，那就是工作。

伊迪丝:是的，所以我想我们都同意了，我想我们都同意我们不会同意。这很有趣，因为我和一个从未谋面的人是推特上的朋友，他创立了赞高，现在他在推特上聊得最多的是—

保罗:这是雅各布·卡普兰-莫斯？

伊迪丝:是的。

保罗:好的。

伊迪丝:人们在晚上和周末工作，为开源做出贡献，但是，由于没有更好的词，人们有点像混蛋。人们就像—

保罗:人们都是混蛋。

伊迪丝:是的，就像—

保罗:即使你拿到了钱，人们也是混蛋。

伊迪丝:但这更让人恼火。

保罗:对，对，因为你是免费做的，或者别的什么。

伊迪丝:是的，所以人们会说，‘我有一个拉取请求，它已经打开两个小时了。“你为什么没有复习呢？”

保罗:对，对。我是说，我们得到了完全一样的东西。我们有给我们发电子邮件的客户，或者更常见的是收到邮件的人，他们使用免费版本，向我们发送支持请求，然后，30 分钟后他们在 Twitter 上说，我不敢相信 Circle 还没有解决我的问题。已经 30 分钟了。

伊迪丝:你认为是什么推动了这一切？

保罗:总的来说，人们都是混蛋。

感谢收听由我、Circle CI 的 Paul Biggar 和 LaunchDarkly 的 Edith Harvaugh 主持的 Heavybit 为您带来的这一集。

你可以在这里找到本期播客的完整片段。想了解更多关于连续播放的内容和收听其他重量级播客，[将此链接](https://feeds.soundcloud.com/users/soundcloud:users:123515298/sounds.rss)复制到你最喜欢的播客播放器中。我们将很快推出针对特定节目的 RSS 和 iTunes 订阅选项。你也可以在推特上关注 [@continuouscast](https://twitter.com/continuouscast) 的连续报道。