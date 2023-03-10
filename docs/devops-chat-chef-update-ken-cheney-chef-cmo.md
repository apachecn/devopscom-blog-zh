# DevOps 聊天:厨师更新与肯切尼，厨师 CMO

> 原文：<https://devops.com/devops-chat-chef-update-ken-cheney-chef-cmo/>

在 Chef 总是有新的发展。我们采访了厨师 CMO·肯·切尼，请他告诉我们最新情况。我们最后一次和肯谈话是在切夫康夫之后。从那以后，Chef 继续在包括 Habitat、Automate 和 INSPEC 在内的几个领域向前发展。我们每隔一个月左右就和 Ken 聊一次，因为知道 Chef“在做什么”总是很好的。

像往常一样，下面是我们对话的音频流，然后是我们聊天的文字记录。尽情享受吧！

## 声音的

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/336089509&color=ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/336089509&color=ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false)

## 副本

艾伦·希梅尔:大家好，艾伦·希梅尔，DevOps.com 的主编，又来了一次 DevOps 聊天。今天 DevOps 聊天的嘉宾是我们的朋友肯·切尼，厨师的 CMO。肯，欢迎回到 DevOps 聊天。

肯·切尼:艾伦，很高兴来到这里。谢谢你邀请我。

**Shimel:** 谢谢。肯，我很抱歉，在你和我的时间表之间，我们已经有一段时间没有机会叙叙旧了。我想我们上次停下来是——是在主厨会议之后吗，ChefConf？

切尼:实际上就在切夫康夫之前。已经几个月了，对吧？鉴于那是在五月底。**

肯，我想从那以后我每次回家的时间都不会超过两三天。是的，的确是这样。但是对于我们的听众来说，他们今年可能没有足够的运气来到奥斯汀和切科夫，你能告诉我们一些我们错过了什么吗？

切尼:是的，正如你提到的，今年的切夫 Conf 在德克萨斯州的奥斯汀。你知道，我认为 ChefConf 在产品方面的亮点是我们围绕 Chef Automate 发布的一些公告，并将我们的开源工具完全纳入 Chef Automate 的保护伞之下。因此 Chef Automate 是我们的商业产品。最重要的是，我们引入了全面的 InSpec，因此现在，从 Chef Automate 中的一个位置，您可以看到您在基础架构方面的表现以及您的基础架构自动化在 Chef 中的进展，而且从合规性的角度，您还可以通过 Chef Automate UI 看到在策略方面发生了什么。因此，实际上，该产品已经从以前的工作方式发展而来，以前我们基本上有两台服务器，现在您有一个单一的通用用户界面来查看所有不同的数据点

此外，我们引入了栖息地数据，因此现在您可以看到正在野外运行的栖息地实例的状态。你知道，我发现合规性前沿发生的事情非常有趣，你知道，我们正在快速发展，从只关注核心计算元素到现在扩展 InSpec 以涵盖基于云的 API。因此，我们现在可以使用 AWS 和 Azure，并且能够扫描它们以及 VMware 环境。所以你知道，我们正在扩展 InSpec，使之成为一种不仅适用于计算，而且还能作为代码广泛管理所有基础设施的语言。主厨会议上也宣布了这一点。我认为这是一个进步。在不久的将来，您将会看到 InSpec 语言和功能的持续扩展，以追求更广泛的其他类型的基础设施。

在这个领域，我们看到客户和用户表现出了极大的兴趣和热情。因此，如果您想真正看到 InSpec 数据汇总到通用策略视图中，并真正了解您在基础架构级别的表现，包括基础架构的状态以及您的基础架构如何符合法规遵从性和安全性方面的策略，我真的鼓励任何没有尝试过 InSpec 的人尝试将其作为 Chef Automate 的一部分。你从一个地方得到它。在这个 WannaCry 和其他正在发生的漏洞的世界里，我很惊讶有多少组织，当像 InSpec 这样的工具存在时，仍然有巨大的漏洞，对吗？在这里，我们有这个开源工具，可以解决这个问题，真正了解你的暴露程度。然后你可以使用像 Chef 这样的工具来修复它。让我震惊的是，这种事还是经常发生。

肯，这让你大吃一惊？20 年来它一直困扰着我。对于我们这些安全领域的人来说，超过四分之三的攻击(实际上，可能超过 80%或 85%的攻击和成功的攻击实际上并不是因为我们过去所说的零日或未知漏洞，而是因为已知的漏洞没有被修补，这不是什么秘密。

切尼:完全正确。完全正确，是的。【T2

Shimel: 这是关键。我的意思是即使在今天

**切尼:**是的，而且——

**Shimel:** 太疯狂了。对不起，继续，肯。

**切尼:**哦，我只是想说，一个常见的事情，你知道，因为许多组织还没有真正完全自动化，所以他们一直在重新引入漏洞。我喜欢 InSpec 的一点是，你实际上可以——因为你是作为代码来管理的，每次你测试你的软件，每次你用 Chef 推送一个配置，你都可以验证你没有重新引入文件或键盘上的其他东西，从而在你的组织中重新引入潜在的漏洞。

是的，你知道——对不起，你能听到吗？

切尼:好的，好的，说吧。

Shimel: 我收到了一点声音。我希望这是记录良好。Ken，我们不久前做了一项调查，只有 75%的组织在部署之前实际扫描了代码的漏洞。你知道，另外 25%的人在想什么吗？和我想的差不多。但是，无论如何，关于安全性的话题，Ken，我想快速提一下，Chef 的 Matt Ray 实际上正在一个会议上发言，下周我将作为 RSAAPG 的一部分在 DevSecOps 上发言。我想马特的工作地点在澳大利亚，对吗？

切尼:是的，他是。是的，Matt 在澳大利亚，他将谈论 InSpec，那里的人们可以参加他的会议并了解更多信息。**

**Shimel:** 也许是因为我要去新加坡旅行，所以它就在我面前，但对我来说，它是全球性的——我的意思是，DevOps 真的已经成为一种全球性的——我不想用“现象”这个词——而是一种全球性的力量。我们看到了

切尼:是的，是这样。

席梅尔:–你知道，当然是在 EMEA，但是我们在美联社也看到了。就在本周，Ken，我想 Chef 刚刚宣布了他们的第一个拉丁美洲合作伙伴，对吗？

**切尼:**正确，正确。是的，我们确实在全球层面上看到了 DevOps，看到了广泛的兴趣。有趣的是——Alan，我在这个行业已经有一段时间了，过去有一点滞后——你知道，在你看到拉丁美洲或亚洲部分地区的市场获得源自美国的技术之前，会有几年的滞后。或者流程思路。但现在事情发展得更快了，你会看到跨国公司在印度和中国都有业务。因此，作为一家公司，我们在全球范围内开展了许多活动。你知道，如果你看看我们是如何见面的，我们在哪里见面，他们在任何地方都在发生。我们的合作伙伴生态系统有 300 多个合作伙伴，覆盖全球，因为我们看到了这种需求。

现在，我们如何进入任何给定的市场都取决于在该市场中什么最有效。因此，有些市场我们通过合作伙伴来应对，而有些市场我们实际上在该市场中设立了自己的实体机构。

是的，我们在 DevOps.com 也看到了同样的事情，肯。你知道，当我们刚开始时，我们的读者群几乎有四分之三是美国人，现在只有大约 37%，其余的是全球读者。但这不仅仅是在全世界传播。就像你说的，没有那么大的滞后时间。拉丁美洲一度是三年——我们过去常常告诉人们，“哦，它比我们在这里做的事情落后三年。”当然，现在情况不再是这样了。

**切尼:**是的，我要告诉你，我们得到的最多的线索来自亚太地区。

**Shimel:** 真的。

切尼:是的，所以那里有巨大的需求。我告诉你，如果我们在班加罗尔或德里会面，我们会有 300 人到场。

Shimel: 哇，太棒了。你知道，我们会多谈谈那个麦克风。但是 Ken，推动 300 人参加集会等强劲数字的很多因素是培训和培训的可用性，对吗？

**切尼:**没错。

Shimel: 这是 Chef 一直做得很好的事情。但是你们最近推出了——不好意思，不是试播——叫什么名字——

切尼:厨师自动化。厨师自动化飞行员，是的。事实上，我们推出了一个全新的在线学习网站，名为 Learn Chef Rally，它的采用速度非常快，每天都有很多用户点击它。作为其中的一部分，我们有所谓的厨师自动化试点，它真正针对的是那些希望在午餐过程中真正了解厨师的人，对吗？所以那种午餐时间的评估，他们想感受一下 Chef 是如何工作的，它为他们做了什么。但作为一个整体，Learn Chef Rally 由一整套模块组成，将带您了解我们技术的各个部分。因此，如果你想了解合规，有一个 InSpec 模块和一个 Chef 合规模块。如果你想学习 DevOps 的概念，你可以去 Learn Chef Rally 网站学习。

我们的接受度如此之高。你知道，我们已经看到许多客户希望将该学习网站带入内部，并为他们自己的公司定制学习环境。人们对此非常感兴趣。所以这是一个很好的资源，我鼓励人们去看一看。

Shimel: 当然可以。肯，那么，合乎逻辑的问题是，他们如何到达那里？

切尼:对，所以去那里很容易。你只要去 learn.chef.io 就可以开始了。

**希梅尔:**优秀。这个不错。这就是主厨拉力赛，强烈推荐。听起来好像有很多，我相信你们正在计划添加更多。所以，肯，我们这里有点像夏天的三伏天，但它肯定不慢，看起来不慢，在任何地方。还有其他新闻事件吗？

**切尼:**是的，我们刚刚度过了人居一周年纪念日，我要指出的是，你知道，我们在切夫孔做了一些人居新闻。因此，我们宣布了一项 Habitat build 服务，并对 Habitat scaffolding 进行了改进，Habitat scaffolding 本质上是一种构建包，使人们能够更容易地打包他们的应用程序，同时我们正在编写一套企业就绪的 Habitat 计划或通用语言、通用平台，如 BigData、Cassandra、Spark 和真正常见的 web 应用程序。因此，Habitat 继续发展，就在过去几周，我们宣布了 Habitat for Windows 的预发布。因此，除了我们对 Linux 的支持，人们现在可以使用 Habitat 来打包他们基于 Windows 的应用程序。在我们看来，Habitat 现在是集装箱的首选包装解决方案。这是打包应用程序并让它在容器中运行，并能够在整个生命周期中管理它的最快、最简单的方法。

那块石头。我的意思是，因为肯定的是，肯，我们在这里看到的一件事是——你知道，我们谈论互联网时间挤压或压缩时间。集装箱上的皮卡？我已经够老了，也许你也是—还记得 VMware 第一次出现的时候吗？

**切尼:**没错。

**Shimel:** 通过虚拟化，进展非常迅速。向虚拟化的转移比我们说的从客户端服务器或类似的东西，从点对点，或点对点到客户端服务器或诸如此类的东西的转移要快得多。但是转向容器——伙计，我最近看到的几项调查显示，50%以上的组织都在生产容器。坦白地说，我认为这不是真的，但这说明了一些问题。对吗？

切尼:是的，你知道这一举动有什么有趣的吗？艾伦，这一举动的有趣之处在于，那里运行的大多数容器几乎都像虚拟机一样被使用。你知道，现在 75%的容器运行完整的操作系统。

**Shimel:** Yep.

**Cheney:** 他们基本上只是将它作为一种尝试更高抽象级别的方法，并消除他们在使用虚拟机时遇到的更多基础架构复杂性。因此，我认为下一波浪潮将会发生，我认为人们将会真正找出如何更好地打包他们的应用程序，以充分利用他们可以做的事情来消除不必要的依赖关系，并消除他们目前正在做的大量围绕应用程序的工作，他们现在只是打包完整的操作系统和他们现在正在打包的所有广泛的不相关依赖关系。因此，我预计这将是下一波浪潮，当他们到达那里时，我们将在那里帮助他们。

**Shimel:** 同意，同意。Ken，除了我提到的 DevSecOps 之外，接下来还有什么节目或会议，主厨会出席吗？

切尼:是的，是的，我们会在虚拟世界，接下来。我们会参加微软即将举行的大型活动。当然，当我们展望 11 月时，我们将在秋季召开自己的社区峰会。所以这些是我们把我们的社区聚集在一起的好方法。所以第一场将于 10 月 10 日和 11 日在伦敦举行。这也是即将发生的事情。因此，预计在未来几个月内，我们将在许多不同的地方看到 Chef 和我们的品牌。

**Shimel:** 太好了。非常酷。肯，我们快没时间了。15 分钟过得很快。但希望不要过几个月你就能回来了

切尼:是的。

**Shimel:**——我们可以从这里停下来的地方继续。

**切尼:**是的，艾伦，祝你旅途愉快，非常感谢你今天抽出时间。

没问题。肯切尼，厨师 CMO，在 DevOps 聊天。我是艾伦·希梅尔，这里是 DevOps Chat 和 DevOps.com。感谢大家的收听，我们将很快在另一次 DevOps 聊天中再见。

— [Alan Shimel](https://devops.com/author/ashimmy/)