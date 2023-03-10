# DevOps 聊天:Mik Kersten，价值流可视化的 Tasktop

> 原文：<https://devops.com/devops-chat-mik-kersten-tasktop-on-value-stream-visualization/>

在本次 DevOps 聊天中，我们采访了 Tasktop 的首席执行官兼联合创始人 Mik Kersten 博士。Mik 除了是 Tasktop 的创始人之外，还是 Eclipse Mylyn 开源项目的创建者。Tasktop 继续引领价值流可视化和软件交付集成。

Mik 为我们提供了这方面的最新信息，并在本次对话中提供了更多信息。尽情享受吧！

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/308888922&color=ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/308888922&color=ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false)

Alan Shimel: 大家好，我是《DevOps.com》的主编 Alan Shimel，我们在这里进行另一次 DevOps 聊天。本期 DevOps Chat 的嘉宾是 Mik Kersten。Mik，对于那些不知道的人来说，他几乎是 Tasktop 的代名词。米克，欢迎你。

迈克·克斯滕:谢谢你，艾伦。很高兴再次和你谈话。

Alan Shimel: 几乎成为贵公司的代名词是什么感觉？

Mik Kersten: 既然你提到了，听起来不错。与 Tasktop 一起度过了一段奇妙的旅程。我认为这是一个伟大的十年，看看如何将敏捷和 DevOps 的好处带给大型组织。所以感觉很好是简短的回答。

Alan Shimel: 又一个创业界十年一夜成名的故事。Mik，玩笑归玩笑，我们的观众中可能有些人不熟悉 Tasktop。因此，如果可以的话，我们可以做一个 30 秒钟的电梯式快速介绍，介绍 Tasktop 是什么，它有什么作用。

是的，绝对是。大多数组织现在都知道，为了获得他们所追求的未来生产力和效率，以在当今世界中具有竞争力，他们需要面对一个敏捷的工具链，他们需要部署 DevOps 和持续集成，为此，您需要选择您的问题跟踪工具、您的持续集成工具、您的发布自动化工具，以及所有这些零碎的东西。如果你是一个大的组织，你选择需求管理工具。如果你在做任何实物产品，你需要一些额外的工具，比如需求和材料清单等等。

有趣的是，一旦组织规模扩大，就会出现开发运维转型。他们都在使用更多的工具和不同种类的划分器。因此，要让 DevOps 的所有这些优势大规模发挥作用，缺少的是集成基础设施这一块。我们可以将所有工具连接起来，以获得端到端的流程，从而获得敏捷和精益的好处，从商业想法到运行软件，以及收入结果和满意的客户。

这就是 Tasktop 一直在做的事情。在过去的十年中，通过发布，我们已经连接了不同的利益相关者、流程和工具，因此您可以拥有这种端到端的信息流。因此，在获得这种端到端流程的同时，您可以拥有同类最佳的工具、最新的问题跟踪器或敏捷规划工具、最新的持续集成工具等，因为我们正在解决的问题是，当您在大多数转换的背后查看时，您会发现 DevOps 和敏捷都已部署在这些本地优化中。团队可以做持续集成或者持续交付。或者组织有持续的交付，但是没有优化上游的任何东西，这确实是我们试图解决的问题。让我们让整个 IT 组织实现端到端的精益。

艾伦·希梅尔:太棒了。Mik，在我们今天开始录制之前的谈话中，你说 Tasktop 和 hub 的最新发布可能是你们十年来所做的最重要和最有意义的事情。你为什么不和我们的观众分享一下你为什么会有这种感觉？这个最新版本中的强大功能和强大特性集是什么？

当然可以。我们注意到的是，同样，你找任何尚未部署 Tasktop 的大型 IT 商店，看看他们如何支持他们的转型，你会注意到你会看到所有这些点对点集成。比如说，你会看到敏捷计划工具通过一些 API 或 Web 主机或一些数据集成技术连接到需求管理工具、时间跟踪工具、质量管理工具、自动化测试工具、这个 _____ 工具等等。

我们四年前注意到的是，点对点连接东西的奴隶要爆炸了。一旦你建立了点对点的连接，你就会得到这个指数因子。所以如果你有两三个工具也没关系。突然间你有了四五个工具。实际上，仅仅是 API 调用的数量就让您的服务器停机了。

我们知道很多客户表示，他们的 JIRA 问题跟踪器从这些集成中获得了如此多的 API 调用，以至于加载一个问题需要一分钟时间。所以你会有这些奇怪的症状。

你还会遇到这种很难维护的事情，因为一旦一个工具发生变化，或者有人在项目的用户故事定义中添加了一些新的字段，或者类似的事情，多个集成就会中断，你就会得到这个疯狂的 Web 主机和 API 集成的意大利面条代码。

因此，四年前我们意识到，我们甚至无法以点对点的方式测试我们支持的所有集成。仅仅是以点对点的方式测试我们支持的所有工具，就已经耗费了我们数十万美元的资源，基本上是虚拟机资源。所以我们在四年前说，“我们必须停止以点对点的方式做事。它不会扩展。我们需要支持现有的所有敏捷和开发运维工具，它无法扩展到支持大规模的开发运维转型。”

所以我们开始创造模型的概念。首先，你期待开放标准。所以我们尝试了一下，我们加入了 OSLC 委员会，但是让每个人都采用开放标准是行不通的。这些工具非常复杂，因为利益相关者的工具现在已经变得非常优雅。开发工具非常适合开发过程，随之而来的是开发人员、测试人员等的复杂性。

所以我们意识到开放标准不能解决这个问题。单靠 API 是解决不了的，实际上是问题的一部分。你需要采取不同的方法。所以在内部，我们建立了这个集成工厂，这样我们就可以测试一切，我们建立了这些通用模型。模型基本上是敏捷和 DevOps 以及 ALM 和 SDLC 系统的通用，比如需求、用户故事、构建、发布、安全性、漏洞等等。

这就是我们如何开始测试一切，然后我们说，“好吧。如果你提出了 slave 抽象，那么连接所有东西就变得容易多了。随着上周 Tasktop Integration Hub 的发布，我们实际上采用了基于模型的方法，并将其展示给所有用户。因此，你只需在你的价值流中定义所有的模型，同样，像用户故事、需求、构建、发布、链集等等，然后你可以在这些模型中插入任何你想要的工具，你就会得到这个神奇的东西。您的价值流实现了完全自动化。

所以我们称之为价值流整合，因为端到端你现在可以有这些流，你可以实际跟踪周期时间等事情，你基本上可以获得 100 或 200 人的创业公司在非常大的规模上，在数千或数万 IT 员工的交付速度方面获得的好处。因此，您已经获得了我们提供的价值流集成层。

这样，您还可以检查正在发生的事情，并且您基本上可以支持这些大规模的敏捷和 DevOps 转换，这都是因为我们已经提高了从抽象来制作这些模型，您已经在模型中映射了不同的工具链，因此，我们实际上已经将工具链本身模块化了。因此，您可以插入同类最佳的工具这是一些点网。这里有一些爪哇咖啡。这里有一些 JavaScript 代码，也许还有一些 Python 代码。您可以将所有这些独立的工具流整合到一个端到端的统一价值流中。实际上，我们在这里做的关键事情，改变游戏规则的事情是基于模型的集成的概念。

*艾伦·希梅尔:*优秀。我同意，米克。你猜怎么着显然你在 Tasktop 工作。你对他们所做的感到非常兴奋。但是对于我们这里的观众来说，他们通常都是非常复杂的技术专家，我希望他们真的欣赏——我的意思是它让人们的生活变得更容易，对吧。当你可以让人们的工作和生活变得更容易时，这是一件好事，这听起来像是一个真正的游戏规则改变者。

迈克·克斯滕:是的。艾伦，那对我来说是非常亲近和珍贵的东西。我的整个背景来自生产力工具，通过我们在 Mylyn 和开发工具上所做的所有开源工作，赋予开发人员权力并消除他们一天中的浪费。我们的任务是改变人们大规模工作的方式，因为情况会变得更糟。

你看看外面的大型 IT 商店，世界上大多数 IT 员工工作的地方，我们已经衡量了他们做什么。每个开发人员或每个测试人员，每个业务分析师，他们至少花费 30 分钟，在某些情况下，我们看到他们每天为每个代码更改重复输入两个小时的信息，例如，因为所有的治理和合规性以及大规模组织中需要的其他规则，但所有这些工作都是浪费，这让人们发疯，因为他们不喜欢这样做，因为这基本上是手动数据输入。

当您想到它实际上是什么时，他们正在输入信息并登录到不同的系统，如果我们再次采用这种基于价值流的方法，所有这些都可以自动完成。您更改了代码。所有这些信息都传播到组织必须设置的工具中。您可能必须以不同的方式跟踪不同种类的需求和变更。没关系。

因此，我们看到的最令人满意的事情是，由于我们实际上从 4 月份开始就有客户参与早期访问计划 Tasktop 集成中心目前正在客户站点的生产中运行——所有的浪费都被立即消除了。基本上，我们的期望是，在它部署的那一刻，我们已经看到了这一点，你的员工敬业度得分在那一周、那一个月、那一个季度会上升，因为你已经消除了所有浪费的工作，这些工作会让他们公司的最优秀的人发疯，事实上你正在让他们这样做。

这就是我们的全部目标。人的目标是通过消除所有浪费，让所有人的生活变得更好。当然，组织的经济目标是:使您的组织更具创新性，因为您现在能够以初创公司的速度交付产品，并获得大规模开发运维的承诺。

艾伦·希梅尔:当然。Mik，我们的时间不多了，因为我们总是在 DevOps 上聊天，但让我快速转向我想和你谈的其他事情，那就是该工作与 DevOps 之间的桥梁或该工作与 DevOps 之间的桥梁。当我在四年前，或者更久，五年前开始使用 DevOps 的时候，有这样一句话，“嗯，DevOps 真的继承了敏捷留下的东西，”但是它们显然是两件不同的事情。敏捷是为开发者准备的。DevOps 适合所有人。

但是我们已经看到 DevOps 越来越多地借鉴敏捷，越来越多地借鉴精益。如果有意义的话，你在哪里看到敏捷和开发运维之间的联系？

Mik Kersten: 这是由不同的思想领袖、不同的供应商等等提供的。最后，都是一样的。它是软件和大规模软件的精简版。因此，就组织如何调整而言，我认为已经发生的事情是，对于如此多的大型组织来说，软件交付的如此多的瓶颈在于部署可靠性、速度和自动化。DevOps 已经形成了一个大的新运动，并真正成为敏捷停止的运动。

最终，技术是你需要持续的交付。您需要实施持续交付，但 DevOps 运动来自开发和运营部门，他们说:“我们需要更快、更可靠地交付东西，并自动化他们客户的所有手动工作。”这实际上改变了敏捷运动开始的地方，也就是我们需要跟踪工作，对变化做出反应，并将客户带入反馈循环。

因此，有两个关键组成部分，我认为我们现在在组织转向 DevOps 方面的绝对速度使它成为更重要的转型代理。敏捷带来的一切都是转型的关键部分。我认为，对于那些领导者来说，将这些 DevOps 转换放在一起，不要停留在代码提交上，这是非常重要的。

你必须真正采取精益快速反馈循环，不断学习，直到业务分析、设计等等，因为如果你停下来，你将不得不解决部署瓶颈，而不是上游瓶颈。例如，如果您没有足够的 UI 设计师，那么部署速度再快也没用。你会在你的 UI 设计上遇到瓶颈。你需要更高一点。

因此，我认为我们都需要采取这种端到端的精益观点，而 DevOps 只是一个伟大的转型代理和一个伟大的运动来帮助我们所有人做到这一点。

艾伦·希梅尔:好东西。Mik，我们的时间就要结束了。我想问你最后一个问题，不是一个恶作剧的问题，但如果可能的话，我总是喜欢问。对于我们外面的读者，如果你能推荐一本他们读过的书，而不是一本显而易见的书，不要告诉我们*凤凰计划*或者甚至 *DevOps 手册*。不一定和 DevOps 有关系。你会推荐什么书？

Mik Kersten: 我现在正举着它。我知道你看不到，但这是迈克·罗泽尔和约翰·舒克写的《T2 学看 T3》。如果你只是翻阅这本书，你会看到价值流图和价值流整合和管理方法，使制造工作。当我们进入这个后开发运维、后敏捷的更广阔的世界时，这是对价值流的相同看法，关注端到端的价值流，我认为这需要激励下一代领导者创造这些变革。

我认为 DevOps 手册包含了很多这方面的内容。这是一本很棒的书。我快读完了。它有许多正确的来源，但就你可能没有看到的东西而言，它是这本*学习看*书，它实际上是关于学习看生产。我们需要学会看到软件在价值流中的流动，大多数组织还没有做到这一点，这真的是-我们的使命是帮助组织做到这一点，但想法就在这里。我们以前做过。同样，它已经在制造业中完成了，现在需要应用到软件交付中。

艾伦·希梅尔:太棒了。Mik Kersten，Tasktop，感谢您成为本期 DevOps Chat 的嘉宾。继续取得成功，并期待着更多，也许会在伦敦的 DevOps 企业峰会上见到您。

当然可以。谢谢你艾伦。和你聊天很愉快，一如既往。

艾伦·希梅尔:好吧，米克。你会好的。

Mik Kersten: 谢谢。

艾伦·希梅尔:我是 DevOps.com 的艾伦·希梅尔。

— [Alan Shimel](https://devops.com/author/ashimmy/)