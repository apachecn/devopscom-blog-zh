# DevOps 聊天:开源和 DevSecOps 与 Azi Cohen，WhiteSource

> 原文：<https://devops.com/devops-chat-open-source-and-devsecops-with-azi-cohen-whitesource-software/>

开源代码的安全性是许多组织正在努力解决的问题。再加上使用开源代码的应用程序被更新的次数以及这些更新带来的集成问题，难怪开源安全性受到质疑。

WhiteSource 认为它有一个解决开源代码安全问题的方案。在本次 DevOps 聊天中，我们采访了 WhiteSource 美国运营总监 Azi Cohen，讨论了围绕开源代码安全性的问题，以及他的公司如何帮助减少这一问题。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/499347006&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/499347006&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

艾伦·希梅尔:嘿，大家好，我是艾伦·希梅尔，DevOps.com，安全大道，我们在这里是为了另一个 DevOps 聊天。在今天的 DevOps 聊天中，我很高兴有一位我有幸与之交谈过几次的人加入，但我相信不是在播客上，而是 Azi Cohen——“Cone”或“Cohen”，取决于你如何发音。Azi 是 WhiteSource Security 的美国业务主管和联合创始人。Azi，欢迎来到 DevOps 聊天。

阿齐兹·科恩:你好。早上好。你好吗，我的朋友？

**Shimel:** 好。很高兴你和我们在一起。所以，阿兹——

**科恩:**好的，顺便说一下，公司的名字叫 WhiteSource Software。

**Shimel:** 哦，好的。

科恩:是的。

Shimel: 我道歉。白源软件。

**科恩:**是的。

Shimel: 你知道，那是一座很好的桥，Azi。在我们进入今天的主题之前，这是与 DevSecOps 相关的，对于那些可能不熟悉该公司的人，为什么不给我们介绍一点背景呢？

科恩:当然。完美。所以白源软件是我们三个人发起的。我们是三个合作伙伴，实际上在另一家公司工作，该公司被 CA Technologies 收购，正在进行收购。而且，通过这个尽职调查的过程，我们发现自己被质疑开源是否被包括在我们的技术中。这是一个非常繁琐的过程。花了很多时间和精力。因此，毫不奇怪，在我们三人被收购并花了一些时间收购公司后，我们意识到，“嘿，肯定有更好的方法来做所有这些事情，”几年后，我们创办了 WhiteSource。

这个想法是允许使用开源开发知识产权的公司——记住，我们说的是 2011 年，2012 年；开源是众所周知的现象或开源的使用，但仍然没有被大型企业很好地采用——所以前提是帮助软件公司或使用开源开发自己知识产权的公司更好地管理和控制库存、法律方面或合规性方面，以及后来的安全方面。

所以我们在以色列成立了公司。我们得到了以色列政府的一些资助。我们开发了一个解决方案，显然，我们开始关注公司——你知道，初创公司和科技公司。我们在相当长的一段时间里做得非常好。我认为巨大的变化发生在大约 18 个月前，也许是 24 个月前，我们开始感受到大型企业——银行和科技公司、咨询公司、大型连锁企业、医疗保健公司——日益增长的需求。所以所有这些人都开始使用开源软件，并开始寻找解决方案，这时我们意识到，“嘿，这里有一个很大的机会。”

我们走出去，从风投那里筹了很多钱，包括从微软等。开始了美国的行动。现在，我们在北美有一个非常大的办公室，超过 30 人。我负责美国的业务。我们每年增长 300%。几乎超过 500 个客户，从数十亿美元的公司到小公司，现在看来，需求不会下降。

**希梅尔:**妙极了。你知道，就像他们在美国说的，祝*好运*。

**科恩:** *【笑】*

Shimel: 这是一个美国人

科恩:谢谢你。

**Shimel:**–_ _ _ _ _ 成功案例吧？祝贺你和你的团队。但是，Azi，你知道，有时候——和你一样，我已经在商界工作了 30 年——有时候，幸运比聪明更好。两者兼而有之真好。但是你真的——white source Software 和你的团队在正确的时间出现在了正确的地方，是一个小小的捐助者。我们生活在这样一个时代，我们的大部分——嗯，一切都是软件和应用程序，但是我们的大部分应用程序主要是建立在开源组件上的，对吗？大多数——

科恩:绝对是。Gartner 的一份报告指出，大约 40%到 60%的新 web 应用程序是由开源软件组成的，而且这一数字还将继续增长。对吗？所以它不会就此停止。我们最大的客户肯定也看到了这一点。我们看到他们从 20%的代码开源开始，很快达到 30%，40%甚至更多，对吗？

所以这不是将要发生的事情，我认为有一个很好的理由。如果你看看今天的大银行等。–你知道，首席信息官被要求创造越来越多的创新。有人写了一篇关于它的文章。他们被要求年复一年地产生大约 25%的新想法和新应用，或者，如果你想要新的代码行，你知道，25 行代码，但是他们没有多 25%的人来做这件事。对吗？他们只能得到 2%到 3%的利润。所以重用而不是构建是最明显的解决方案，这就是为什么我们不会看到这个百分比下降，而是越来越高。

Shimel: 哦，这很有道理，对吧？这么多–你知道，当你看一般的应用程序时，有这么多是冲洗和重复的，对吗？发送电子邮件、发送电子邮件或注册、打开窗口。如此多的——没有必要重新发明这些东西的轮子 _ _ _ _ _ _ _ _ _—

科恩:哦，当然。

**Shimel:** 你知道，当你看的时候，有这么多的 Java 脚本被重用，有这么多的 Java 组件被重用。有太多这样的开源重用——就像你说的，随着这些库和存储库变得越来越大，只会越来越多。但这回避了一个问题，Azi，这并没有使我们变得更安全。事实上，有些人可能会认为这会让我们更不安全。你的立场是什么？

科恩:嗯，这是个很好的问题。你知道，很明显，当你有一个组件被数百万人使用时，这只是一个机会，攻击者可以找到一种方法来攻击它，破解它，现在他们有数千家公司可能容易受到这个攻击，对吗？然后，对他们来说，打开了进入这些账户的大门。因此，我们实际上看到的是，随着越来越多的开源软件被使用，在一端，我们看到攻击者试图利用这些开源组件，我们在过去已经看到了一些案例，对吗？

与此同时，社区试图找到更多的漏洞，并尽快修复它们，但是，如果你看看 DevOps 的家伙，这产生了一个巨大的问题，因为，想想看，一方面，他们使用越来越多的开源软件；另一方面，非常活跃的社区正在那些开源中发现越来越多的漏洞并提供修复，对吗？

所以现在 DevOps 的人有更多的东西要处理，有更大的库存要跟踪、检查和验证，但是，另一方面，我们知道攻击者知道这些人会很快修补这些漏洞，试图越来越快地攻击它们。所以 DevSecOps 或 DevOps 家伙在更少的时间里有更多的事情要做。所以唯一的解决方案是自动化，对吗？唯一的解决方案是通过某种控制，让他们知道什么是好的，什么是坏的，并在发生不好的事情时或当他们暴露的新漏洞是 _____ _____ 时提供警报。

是的。绝对的。你知道吗，阿兹？这就是——你刚刚描述的，是的，它对 DevSecOps 来说是百分之百正确的，但它也描述了我们在一般软件开发中看到的许多东西。如果机器，如果工厂要以最佳速度运转，我们必须自动化很多，对吗？因为，否则，它就跟不上，安全性当然也不例外。没有例外。_____ –

科恩:绝对是。这里的另一件事是，你必须检测或试图阻止坏事情进入大门，而不是以后，对不对？因为每一步都在后面——所以这是自动化，但也是在所谓的左移前面的自动化，对吗？在开发周期中尽可能早。然后，在 WhiteSource，我们正是这样做的。

是的。这就引出了一个问题，“听起来很棒。让我们都来做吧。为什么我们没有更安全？为什么没有更多的人去做？真的有那么容易吗？”

科恩:我认为这主要是意识和感知的问题。因此，首先，当我与 CIO、ciso 会面时，他们不了解——在许多情况下，他们不了解他们的环境中采用开源的程度。他们认为，在许多情况下，他们只使用了 10%或 15%的代码，这是开源的。事实是它更高。

因此，对问题的看法是一回事，许多地方的高层管理者不明白现在使用的开源软件数量比他们拥有的多，但另一件事是，你知道，人们的看法是标准工具，如来自 IBM 或 Checkmarx 和其他供应商的应用程序安全测试工具，正在解决这个问题。你知道，既然他们扫描专有代码，那么很可能也扫描开源代码，但这不是真的。事实并非如此。

最后一件事是，再次意识到，或者，如果你想，教育——大多数管理者的假设是开源的行为就像专有代码，对吗？你用扫描仪。你测试开源。你会发现弱点。不管怎样，你要么修好它们，要么不修好，它们就修好了。这是一次性的。他们忽略的是，开源是有生命的东西。你可能有一个清晰的开源组件正在使用，这很好，但是几个月后，它可能会有一个漏洞，对吗？你必须能够在以后追踪它。这不是一次性测试和消失。

一个很好的例子是 Apache 的 Struts 号，对吗？一年前，整个世界都被这个由攻击 Apache Struts 创建的 Equifax 事件震惊了。每个人都很可能在今天之前修好它。你猜怎么着？三天前，也就是一周前，发现了 Apache Struts 号的一个新漏洞，这个漏洞已经被修复。这不会是最后一次，对吧？所以开源是一个有生命的东西，漏洞来来去去，你必须保持跟踪。

因此，我认为高层管理者——首席信息官，有时是首席信息官——并没有意识到随着开源的增加，当前的工具并没有解决这些问题。最后，他们需要一个工具来跟踪开源软件安全性的变化。

**Shimel:** 正是。我的意思是，你谈到 Struts 2，它是这里的一个典型，因为 Equifax 得到了所有的媒体和恶名。我看了一个演示，我忘了是哪家公司，但真正让我吃惊的是，即使我们知道它不好，你必须修补它，你必须升级它，仍然下载和使用旧版本的人的数量从每月大约 80，000 下降到每月 70，000。对吗？

**科恩:**意识，对吧？顺便说一下，这些数字正在变化，所以你可能不知道，但我们刚刚发布了一个工具，称为“漏洞检查器”它可以从我们的网站，whitesourcesoftware.com 下载，基本上，它会检查-它会自动检查，为客户检查 _ _ _ _ _-那些对他们的系统是否受 Apache Struts 2 影响感兴趣的人，对吗？因此，对于那些意识到这一点并想知道他们现在是否有一些问题的人来说，他们可以免费下载并快速检查他们的系统，看看他们是否受到了影响。

希梅尔:是啊。但这也是公司未来的发展方向。他们需要这样做，然后他们需要–你知道，Azi，我记得我在 2005 年销售漏洞管理和补丁。我和一位首席信息官聊过。花旗银行有三位首席信息官。这是在它被称为“花旗”之前；是“花旗银行”他们有三位全球首席信息官。我向他们展示了一个可以扫描漏洞的系统，如果有已知的漏洞补丁，它会将其与补丁管理器集成，自动修补这些漏洞。

科恩:当然。

**Shimel:** 他说，“这很好，但是，Alan，我们不会因为发现漏洞就安装补丁。在安装补丁之前，我们必须对所有应用程序进行回归测试。我们落后了大约三个月。“因此，实际上，他们修补发现的已知漏洞需要三个月的周期。是的，我不是说今天的情况有多糟糕，但是那种心态，那种方法，在今天的业务发展速度下是行不通的。

科恩:你百分之百正确。我敢打赌，如今花旗每个应用程序的漏洞比过去多了几百倍，但这是一个重要的问题，因为我们面对的是我们的任何大客户，事实上，我们刚刚提出了一个非常非常聪明的解决方案。正如你提到的，我们知道他们需要很长时间来修补，对吗？我们知道他们有时有成千上万的漏洞，他们需要知道把时间放在哪里，对吗？尤其是需要更长时间的时候。

所以我们想出了一个叫做“有效使用分析”的工具，这个想法非常简单。当开发人员选择一个新的开源组件时，这个组件通常会附带 10 到 15 个不同的功能。它们中的每一个都可能有一些弱点，等等。，所以这整个包可能带有，比如说，10 个不同的漏洞。但是开发人员将只使用一两个函数，因此，您将只暴露于这 10 个漏洞中的两三个。因此，有效使用分析是我们发布的一个新模块。它检查代码并识别开发人员如何使用开源软件，因此清除了所有不相关的代码。

因此，对于这种——对于世界上有数千个漏洞的城市来说，有效的使用分析会将相关漏洞的数量减少 70%—7%。这些是统计数据。现在，他们只剩下最严重的 30 %,他们可以并且应该花三个月的时间来修复它们，以获得更好的安全解决方案。它是巨大的。这种差异是巨大的。我们从正在测试的客户那里得到了很多很好的反馈。这确实有助于他们确保他们度过的每一个小时都更加有效。

**希梅尔:**优秀。这个东西你也能在 WhiteSource 软件公司买到？

科恩:绝对是。是啊。这是我们刚刚发布的新型号。

**Shimel:** 那它叫什么名字来着？

**科恩:**有效使用分析。

**Shimel:** 生效-

**科恩:**美国。

**Shimel:**–使用分析。EUA。

科恩:是的。是啊。

**Shimel:** 明白了。好吧，Azi，正如我在开始录音前向你提到的，15 分钟过得很快。

**科恩:** *【笑】*

Shimel: 我们已经超过 15 分钟了。我们可能会谈论一整天，但我们必须结束这一集的 DevOps 聊天。但是也许我们很快会让你回来，我们可以继续谈话。

科恩:当然。谢谢你。艾伦，和你谈话总是很愉快，所以我很期待。

不，这是我的荣幸，阿紫。我觉得我们可以坐下来谈一整天，但我们会称之为一个总结。Azi Cohen 是 WhiteSource Software 的联合创始人兼美国运营总监，感谢您成为我们本期 DevOps Chat 的嘉宾。

科恩:谢谢你给我这个机会，艾伦。总是很高兴。

**Shimel:** 快感。我是 DevOps.com 保安大道的艾伦·希梅尔。您刚刚听到了另一个 DevOps 聊天。

— [Alan Shimel](https://devops.com/author/ashimmy/)