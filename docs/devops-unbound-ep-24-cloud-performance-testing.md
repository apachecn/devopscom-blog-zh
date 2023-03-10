# DevOps 自由 EP 24–云性能测试

> 原文：<https://devops.com/devops-unbound-ep-24-cloud-performance-testing/>

云性能测试的目的是识别和消除应用程序中可能出现的性能瓶颈。[性能测试](https://devops.com/?s=performance%20testing)允许 DevOps 团队检查应用的速度、可扩展性和稳定性，以确保在指定的工作负载下一切按计划运行。在《devo PS unbounded》的这一集中，克里斯汀·韦伯([特里森蒂斯](https://www.tricentis.com/))、唐纳德·卢茨([陶斯](https://www.taos.com/))和安德烈亚斯·格拉伯纳( [Dynatrace](https://www.dynatrace.com/) )将与主持人艾伦·希梅尔和米奇·阿什利一起讨论云性能测试的主要优势，以及在构建云性能测试策略时需要考虑的事项。加入专家的行列，了解如何确保您的应用平稳运行，并在关键时刻保持可用。下面是视频，后面是对话的文字记录。


艾伦·希梅尔:大家好。这是艾伦·希梅尔，Techstrong 集团的首席执行官，你正在观看的是另一个*devo PS unbounded*。对于那些可能不熟悉我们观众的人来说，*devo PS unbounded*是一个由我们在 Tricentis 的好朋友赞助的双周视频系列。我们围绕开发运维以及与开发运维相关的技术、实践、流程和人员探讨了广泛的主题。如我所说，我们两周做一次。每隔一周，对于那些有一点挑战的人来说，然后大约每月一次，我们也有一个现场-我们称之为圆桌形式的 *Devops Unbound* ，在那里我们通常会有一点点更大的小组。但是我们有一个非常大的小组，我们向现场观众开放，你和每个参加的人都被邀请参加圆桌会议，与小组和我们的主持人互动，问问题，给我们你的想法，这真的成为一种集体大厅/市政厅式的会议。如果一切顺利，那就太好了，参与面很广。

实际上，今天是个很好的时机，提出这个问题。今天的面板版本*devo PS unbounded*是对性能测试的整体方法。但是，即将到来的或下一次现场圆桌会议，我将在本月晚些时候在节目中了解更多信息，时间是 2 月 24 日，也就是周四，它将在云中进行性能测试。我一会儿会给你实际的标题。但是我们这里的一个小组成员，克里斯汀，会去那里，还有其他一些伟大的客人。你可以在 devops.com 上注册。如果去参加即将到来的网络研讨会并查看一下，现在是 2 月 24 日 ^日 。如我所说，我稍后会带来更多相关信息。

但是现在，让我们谈谈性能测试的整体方法。在这样做的时候，我认为正确的起点是我们的观众。我已经提前通知了克里斯汀，所以如果可以的话，我想让她先来。嘿，克里斯汀，欢迎来到*devo PS unbounded*。请向观众介绍你自己。

克里斯汀·韦伯:当然。谢谢艾伦。我是克里斯汀·韦伯。我是 Tricentis 公司的产品营销总监。目前围绕新型装载机性能和负载测试解决方案运行产品线。我从事技术工作大约有 20 多年了。我已经记不清了。我在产品开发方面工作了很长时间，所以我记得当我们在 Macromedia 和 Adobe 测试大型软件版本时，试图将我们的产品作为更广泛版本的一部分按时推出，并确保没有西瓜，我们过去称之为三周平均故障间隔测试结束时的性能瓶颈。因此，性能测试是我最关心的事情，所有的应用程序开发、背景都是如此，我很高兴来到这里。

艾伦·希梅尔:当然。Macromedia，这个名字我已经很久没听过了。它曾经是我工作场所的一大部分。我完全不记得了，直到你提起。但它带回了美好的回忆，所以这是件好事。是的，对我微笑。接下来，我想向你介绍安德烈亚斯。我们叫他安迪。是格拉布纳，对吗，安德里亚斯？

安迪·格拉伯纳:是的，但是你可以随意用你喜欢的方式发音，只要你叫我安迪。我总是开玩笑，如果你叫我安德烈亚斯，那么我通常会做错或粗鲁的事情，因为如果我做了不适当的事情，我妈妈会叫我安德烈亚斯。

艾伦·希梅尔:我明白了。我们最小的儿子是布拉德利，每个人都叫他布拉德，你说布拉德利，他有点-他知道他有麻烦了。但是，无论如何，安迪，欢迎你。如果你不介意的话，向观众介绍一下你自己。

安迪·格拉伯纳:好的，谢谢。所以我第一次开始研究性能工程，我想，大概是在 20 或 21 年前，也许是现在。我在赛格威软件公司工作。我是一个名为 Performer 的性能测试工具的性能测试人员，现在还在使用。但是我记得那些日子，那是一个大型的负载测试项目，我——我做的第一个客户项目。我还记得我的表演项目被安排在一周内，花了整整十分钟，因为我们用两个虚拟用户破坏了系统，虚拟用户是我的左手手指和右手手指在两个不同的键盘上点击刷新按钮。我很快了解到性能测试，虽然我们总是想到神奇的 10，000-百万虚拟用户，但有时它就像在您的网站上点击刷新按钮一样简单。

这些年来，我已经从一名表演工程师变成了一名演员。实际上，我在 Dynatrace 工作了 14 年，在可观测性领域，我自称是 devops 的积极分子。我真的很喜欢 devops 背后的想法，我试图使用像你和我自己的渠道这样的渠道来真正倡导 devops 允许组织在工具转型、人员转型、流程转型方面做些什么。我很高兴来到这里。

*艾伦·希梅尔:*优秀。谢谢你，欢迎你，安迪。谢谢你能来。我们今天的第三位小组成员是我有幸认识的人——我不知道，唐纳德。有 20 年，19 年了。

唐纳德·卢茨:已经 20 年了。是啊，太长了。

*艾伦·希梅尔:*二十年。在我们最初的团队“仍然安全”中，我和米切尔一起做了“仍然安全”项目，但他是一名出色的开发测试人员。我会让他自我介绍。我不想让我们的朋友唐纳德·卢茨为难。嘿唐纳德。欢迎光临。

唐纳德·卢茨:欢迎。我叫唐纳德·卢茨。我做软件架构大概有 30 年了。我一直专注于如何正确地进行开发，如何正确地使用设计模式。在过去的十年里，我真的被遗忘了。现在，我是 Taos 的高级云和软件架构师。我们是一家公共云公司。IBM 刚刚收购了我们。Sullivan 将我们评为公共云第一名。我们也在 Gartner 魔力象限中。所以我花了很多时间来帮助我们将咨询服务产品化。因此，测试的整体理念以及如何正确地进行性能测试和混沌工程，这些都是我非常关心的问题。您如何在代码中使用正确的设计模式来避免所有这些性能问题？

Alan Shimel: 正如人们所说，一盎司的预防抵得上一磅的治疗，对吗？我们会谈到的。最后一位成员是我的搭档兼朋友米切尔·阿什利。不过，我想让米奇自我介绍一下。米奇，拿着。

米奇·阿什利:哦，很高兴和大家在一起。谢谢你让我追随一些很难追随的人。哦，我的天啊。顺便说一下，Macromedia、Dreamweaver、Authorware，还记得那些好东西吗？我认识唐纳德-图钉又十年了。所以世界真小。不，我是与 Alan 一起工作的 Techstrong Group 的首席技术官，也是我们的分析公司 Techstrong Research 的负责人。很高兴来到这里，我想我们可以用关于性能测试的战争故事来填满整个会议，Andy。或许我们可以留到以后再说，对吧？但是很高兴大家都在这里，感谢观众的参与。

艾伦·希梅尔:谢谢你，米切尔。很快，我想回到仍然安全的性能测试，Mitch，如果你还记得的话。这超出了我们的预算，因为我们没有所有的虚拟设备，那时您无法从一台机器上完成这项工作。我试着去一个地方，那里有足够的东西来做很多事情

米奇·阿什利:你让戴尔忙个不停。

艾伦·希梅尔:–耶稣。伙计，太疯狂了。不管怎样，让我们开始吧。在我看来，我在科技领域听到的最常被滥用的词之一是“整体性”。所以让我们开始吧。当我们谈论性能测试的整体方法时，它真的是整体的吗，或者我们是在谈论“嘿，什么是性能测试的好方法？”我们应该如何进行性能测试？

克里斯汀·韦伯:我可以从这个开始。因此，基于 Andy 之前所说的他的两个手指是负载测试的开始，我认为我们所说的整体或仅仅是性能测试的合理方法是从代码开始，从 API 开始，从一个用户开始，并确保在您签入代码或 API 之前，您的微服务对一个用户有效吗？

然后，随着开发过程的进行，您开始构建应用程序的组件并集成这些组件，您可能会遇到 100 个左右的用户。在这个过程中，你会得到反馈，这样当你有一个模拟预生产的应用集成到你的整个系统中时，你就有可能达到几十万的负载。但是你已经有了反馈，反馈循环说，“表现如何？什么不是？在这个过程中，我需要解决哪些问题，以便在您达到真正的高负载时，您已经解决了许多问题？”最后，您要解决的问题是，“我需要在系统中进行哪些调整，以确保这个应用程序或 API 能够正常运行？”所以这是整体的一部分，或者我们需要想一个更好的词。

我倾向于使用的词是标准化，也就是说，你需要涵盖整个流程中的所有基础，但你也需要确保涵盖所有协议和所有用例。因此，像我们刚刚谈到的那样，从 API 到 monolith 的所有东西都有一个标准化的方法，但从 HTTP 到 JavaScript 到 SAP 和 Citrix 的所有协议又是什么呢？因此，无论是从协议角度还是从浏览器角度来看，都要有一种适用于所有协议和所有用例的方法，因为这是两种不同类型的性能测试，但我在标准化方面要考虑的第三件事是执行性能测试的人员的技能。

因此，您不仅希望您的卓越中心能够进行性能测试，而且当您迁移到 devops 时，您还希望能够有一个更分散的模型来确定谁可以参与性能测试流程，并创建更多的自助服务方法，以便在很多时候，如果他们可以访问浏览器，他们可以运行性能测试。他们可以分享成果。这包括为希望使用 as-code 方法或 CLI 在 CI 管道中构建的性能测试人员提供方法，或者为希望使用 GUI 工具的无代码方法的团队提供方法。所以，这就是我要说的三个意思——当我们考虑整体性时，我们的意思是什么。

艾伦·希梅尔:爱死了。有什么想法吗，团队，小组？同意，不同意？你想补充吗？

安迪·格拉伯纳:我想补充一些东西。再说一次，我的母语不是英语，所以也许“整体”这个词对我来说也有不同的含义。但我想补充一点，然后再补充一点。但是你所说的第一个的事情，克里斯汀，我认为在开始时你说过开发人员需要了解他们的代码在 1 个用户、5 个用户、10 个用户和 20 个用户的情况下是如何运行的。我认为我们在这里谈论的是人们理解哪里是断点，哪里是可伸缩性问题，因为我认为如果你正在构建新的代码，无论它是大是小，如果你把它放在不同的负载下——我的意思是，你不必面对数百万的用户，但是如果你看着 10，100 和 1000 个用户， 您可以立即知道组件之间的连接问题和扩展负载的问题在哪里，哪些地方可能会出现问题，哪些地方不会扩展，因为显然我们不能在一个问题上投入大量硬件，但我们会以一定的成本获得性能。 因此，正如你所说，我认为从一开始就让开发人员了解他们在哪里是非常重要的，他们可能会做出一些糟糕的架构决策，这些决策后来会让他们为了扩大规模而花费大量资金。我认为这是一方面。

但对我来说，整体性还意味着不仅要在开发中关注它，并尽早开始，但对我来说，整体性意味着我首先需要了解我真正的绩效目标是什么。如果我正在开发一个新的功能，一个新的应用程序，我应该和提出这个想法的人坐下来，试着了解他们对我的软件有什么期望？在一定负载下应该如何运行？这就像我们生产中的非功能需求。然后真正地把它分解成，作为一个开发者，这对我意味着什么？举个例子，如果我们正在开发一个新的移动应用程序，假设有一个登录功能，我们预计登录需要多长时间？先说一秒钟。好吧，如果是一秒 10，000 用户以下，这对于我这个在后端实现 2 或 3 个 API 的开发者来说意味着什么？

因此，我认为绩效预算这个术语也是我多年来听到的。因此，如果您按照我们与业务部门达成的一致意见分解绩效，如果我们有绩效目标，那么我们可以将其分解为各个团队的更多技术目标。然后我们，我认为，采取一种整体的方法，因为这样每个人都可以真正致力于他们的组件，并真正始终确保他们的组件在他们的性能预算范围内工作和运行，这样最终，当所有组件在生产中放在一起时，他们就有更大的机会真正满足我们的业务和生产中的性能要求。所以我认为这是我想补充的两点。

唐纳德·卢茨:是的，我想补充一点。我想了很多的事情是因为我在过去的十年里已经建立了很多微服务，并且思考同步和异步通信以及它们是如何进行的，因为如果你有太多的 API，你必须使用断路器之类的东西。有很多因素会影响它。因此，如果你开始研究像卡夫卡这样的东西，我应该在哪里拆分我的工作负载，以便它是异步的？这是怎么回事？我们在里面放什么样的图案？这有很大的不同，因为大多数开发人员总是想同步，我发现这是一个真正困难的问题，因为你知道吗？我们可以把这个放在背景中。当你看亚马逊的时候，仅仅因为你下了一个订单并不意味着它真的进入了你的账户并立即从你的卡上扣除了。整个同步性的概念必须嵌入到性能的概念中。

安迪·格拉伯纳:是的，没错。是的，这也是一个很好的组件解耦，对不对？我的意思是，这就是你所说的事件驱动模型，对吗？你在中间放了一个队列，但它基本上是一个事件驱动的架构，非常重要。因为事件驱动架构还允许您更好地测试和隔离性能测试组件，然后提出测试版容量规划模型，对吧，因为您知道第一个组件会产生多少事件，当您对其施加一定的负载时，这意味着，我们需要如何调整队列或其最终位置，然后我们需要在另一端对队列进行什么操作？我的意思是，这是一个非常好的观点。

米奇·阿什利:艾伦，也许这就是为什么整体治疗被过度使用的原因。这个话题不仅发生了变化。我认为它成长了，因为我记得我与 Donald 合作的第一次经历是在 ISS 和 TP 网关服务器上，这是一个第三方产品，他对我来说是新的，他知道如何调整它。我们当时称之为调整，但负载、容量、可扩展性，以及我们添加到客户体验或用户体验目标中的指标。在移动设备上登录需要多长时间，而在网络浏览器上登录需要多长时间才能得到响应，不管那是什么？我们对合作伙伴和第三方服务的 API 性能目标是什么？所以我认为这让这个世界变得更复杂了，也许要处理起来更复杂。但它也让我们更接近我们试图用任何系统或软件完成的最终结果。提供这种服务或实现这种功能。帮助我们从横向和纵向的角度思考我们要传递的东西。

艾伦·希梅尔:是的。不过，我想还有另一个因素，我对你们的想法很感兴趣。当我回顾我的职业生涯时，性能测试发生了怎样的变化，最大的因素是什么？嗯，我认为正如 Andy 提到的，在早期，它依赖于硬件，对吧，因为，我的意思是，如果你想扩展性能测试，你必须能够在运行的硬件上进行测试。这很快就变得昂贵起来，不仅是设备的实际成本，而且从人的角度来看也是如此。对吗？然后是性能测试的虚拟化，哇，真是天赐良机。我们可以让安迪在这里工作，正如他所说，他的左手和右手食指，这足以打破他的-他当时正在测试的应用程序或软件。

然后，我认为对于 devops 和 dev 测试等等，自动化我们的性能测试的想法，对吧，能够将其转移到–进一步转移到我们的开发流程中，对吧，制作–因为过去是你完成所有的编码，这需要你三个月周期中的一个月，而现在三个月周期中的两个月是你的测试周期，对吧？伙计，通过左移，我真的把它去掉了很多。所有这些深刻的变化，在性能测试中——当我们今天坐在这里，我们能说真的有一个性能测试的最佳实践，整体的或不整体的吗？人是其中的一部分，对吗？总有人员、流程和技术。其中的人是什么？克里斯汀，你介意开始吗，或者-

Kristen Webb: 所以，我认为有一些方法是最佳实践，第一步是真正理解你的应用程序中的优先事项和风险领域，因为你不能测试所有的东西。因此，您需要真正确定首先测试什么以及最有可能出现问题的地方。第二，在你这样做之后，就要确定你的服务水平目标是什么，你的服务水平目标是什么，并了解你需要达到什么样的虚拟用户水平，在什么样的响应时间内，以及你希望最终用户体验是什么样的。在管道中构建这些 SLO，这样当你以连续的方式运行测试时，你就可以说，“当我们对 XYZ 负载运行测试时，这没有影响到 SLO，”然后你把它发送回去，你可以根据结果采取措施使构建失败，例如，发送一张票到吉拉，这样它就可以集成到你现有的开发流程中，这是一个很好的方法。

此外，接受生产反馈也是一个很好的部分，以确保您了解生产中实际发生了什么，以及我的测试是否模拟了我的用户在何种负载条件下的真实体验，并确保您正在更新您的 Kubernetes 环境以匹配该级别的代码。您是否需要一个基于从 APM 工具(如 Dynatrace)或其他监控工具(如 Prometheus 或 Microsoft Monitoring)获得的信息的新集群。并将可观察性数据带回测试定义中，并持续更新它们，以确保您能跟上事情的变化，因为事实上事情确实在变化。我的意思是，我们有季节性，或者我们有新的营销活动，这可能是一个数字化的业务。现在他们需要跟上他们的负荷峰值。所以你要能够走在前面，而不是被动反应。

*艾伦·希梅尔:*同意。小组讨论，有什么想法？

*Donald Lutz:* 遥测的想法已经成为——实际上在过去的两年里，我已经做了很多开放式遥测，这样我们就可以知道每个点上发生了什么。我们把它放在 l 中。我们把它放在 Datadog 中。我们把它放得到处都是，还有整个 Kubernetes 集群，你如何正确地监控它？什么是正确的事情？我用过很多工具，但是由于 Kubernetes 中控制循环的工作方式，整个 Kubernetes 的事情打开了一个更大的蠕虫罐。所以你必须弄清楚你想如何部署它们？环境看起来像什么？那里合适的负载测试是什么？这就是为什么我进入了很多混沌工程，打破生产中的东西，看看会发生什么。我刚刚关闭了这项服务。它不再和 Slack 说话了。那些信息都去哪了？我们注意到这不起作用了吗？我认为这个想法非常有价值。令人惊讶的是，它让开发者变得非常神经质。他们不太喜欢，因为你基本上是在说——这有点像即兴表演，因为我们只是要做，然后把东西关掉，他们会说，“嗯，我觉得这很有用。”所以这是一种非常奇怪的反应。

艾伦·希梅尔:是的。安迪，你在动力公司，对吧？这是你们的拿手好戏。

安迪·格拉伯纳:没错。所以补充一下你们已经说过的，你们两个都已经说过，在一个非常成熟的规模上，我认为 IC 的人总是直接进入生产，可能使用金丝雀或未来标志，只是部署他们的新代码，然后暴露给，比方说，一小部分用户。我说的是非常成熟的，这显然是我们希望更多的人去做的，但现实是只有少数组织能够真正做到这一点。但这是最理想的情况。你部署。然后你用你的遥测技术算出，代码现在改变了吗？它实际上比现在的表现更好还是更差？

我想补充的是，我想克里斯汀也说过。我认为我们需要做的是从一开始就接近开发者。我知道这是不同的术语，我只是在这里再抛出一个术语，性能驱动的开发，因为我认为我们已经教会了工程师——我的职业也是工程师，对吗？在过去的 10、20 年里，我们教他们做测试驱动的开发，在那里你写你的单元测试和功能测试来覆盖功能。我认为，我们还应该教育他们进行性能驱动的开发，这意味着您正在——当您编写公开五个 API 的新微服务时，然后编写您的 API 测试，您可以运行一次，也可以连续运行，或者与多个虚拟用户一起运行，以实际生成一些负载。我也认为，它们变得对开发者更加友好。Kristen，再次指着你，我知道你有一个很棒的产品，你实际上允许开发者将他们的东西定义为代码，对吗？代码可以是 JavaScript 之类的东西，不管它是什么。但是我认为，随着工具的成熟，我们正在让开发人员编写这些类型的测试变得更加容易和自然，我认为我们也会有更多的选择。我认为这非常重要，因为我们总是谈论向左移动。这是一个很棒的术语，但如果你想一想，如果你把所有东西都拿走，然后把所有东西都向左移动，我们就把所有的负担都推给了开发者。我认为这是不可持续的。因此，我们需要让开发人员尽可能容易地完成我们要求他们做的所有事情。

所以这意味着我们需要给他们工具，在他们的栖息地，也就是说在他们的本我中，对吗？他们需要能够签入代码，作为提交过程的一部分，他们不仅会自动获得关于代码覆盖率和功能覆盖率的反馈，而且，“嘿，你的代码更改现在已经使你的性能降低了 20%。你是否意识到了这一点，或者你正在消耗 50%以上的内存？顺便说一下，然后让 Donald，也就是你所说的从生产中学习，然后你可以将它与你的生产数据相关联，并说，“嘿，你的服务在生产中运行，有一定数量的实例，如果你进行代码更改，这意味着你有 50%以上的内存消耗。你知道额外的费用吗？“因此，我认为我们需要做很多事情，但首先要让开发人员能够在他们所处的自然环境中做更多的事情。

克里斯汀·韦伯:安迪，我将继续你所说的，因为我想确保我清楚我所说的左移是什么意思，我确实认为它是作为一种服务带给开发者的。因此，我认为这是构建一个自助服务，而不是让开发人员承担在管道内构建性能测试的责任。因此，如果他们在其中操作的管道是自动化的，那么就真的要由性能工程师来构建，自动化工程师为他们构建测试平台，以便他们真的像你说的那样，在他们的生命周期内和他们的生命周期内运行，无论他们使用什么来检查。

事实上，一旦他们这样做了，他们就可以得到反馈，这样他们就知道如何针对某个用户开始执行他们的代码。然后，随着他们继续深入，他们会获得更多关于负载增加到几百的信息，也许，一旦他们有了，像你说的，可能会公开更多 API 的微服务。一旦你以这种方式分发代码，它将如何影响其他代码，以及其他影响代码和端点将如何影响你引入的新代码，所以真的有点交付，这就是我之前谈到的创建自助服务方法，以便更多人可以参与到流程中，但性能工程师仍然是构建该方法的幕后策划者。

米奇·阿什利:我有一个问题要问专家组。我很好奇。你认为这方面怎么样？对我来说，一个比整体更好的词可能是系统，我正在考虑所有部分如何配合在一起，以有助于您提供的性能，以及其他事情。这不仅仅是测试我们的应用和应用代码。它正在测试整个堆栈，包括垂直测试和各种测试，以及它可能运行的不同环境。很多都不是我们的代码。唐纳德谈到了 Kubernetes，这是一个很好的例子。这也是我们所说的整体的一部分吗？

唐纳德·卢茨:我想是的。对我来说，我认为整体问题的一个方面是，你建立了所有这些 CICD 管道，但你没有一个保持平台一致的 gitops 流程。你正在努力，所以从根本上说，你没有集群。在集群有效满足您需求的情况下，您没有将基础架构作为代码来实现。因此，当开发人员部署代码时——运行所有测试，但基本上集群的一部分没有得到——所以我最近在我目前的职位上思考了很多，我们如何在整个组织中部署 gitopss，在我们团队的所有元素中部署 gitop，所以我们在做其他事情时有效地使用它，因为这是正在发生的一件事。Argo CD 是一个很好的例子。它确实工作得很好，但只是让它发生并意识到你正在建立一个平台也是人们需要考虑的事情。

*艾伦·希梅尔:*同意，同意。你猜怎么着我只想在火上再扔一根木头。所以，云。游戏规则改变者？没什么区别吗？更容易？更用力？唐纳德，你是这里的开发者的代言人，也是 IT 的代言人。你怎么想呢?和云，您与公共云提供商合作。你——什么 T3

*Donald Lutz:* 是的，我的意思是，公共云是我们从根本上关注的。这就是我们为所有客户所做的，云更简单，但同时也更复杂，因为他们——从根本上来说，公司习惯于让不同的人在他们的数据中心工作。当你迁移到云时，这是令人不安的。他们必须想出如何移动所有的工作负载，但我一直在思考的云带来的一个问题是，如果你可以与所有三个公共云一起工作，你就可以开始增加你在所有方面的可靠性，但你如何控制成本，以便我可以在 GCP、Azure 和 AWS 中运行它？公司想去那里，但他们总是在想，“我该怎么做？我们为什么要这么做？所有这些术语是什么意思，你如何让不同的主管理解，因为我们试图在咨询服务上销售它们。这就是你应该这么做的原因。这就是你如何让你的 devops 工作。这是所有这些东西。这是你应该做的。“这是一个非常复杂的问题，因为他们觉得这有点像很多行业发生的事情。他们把它外包给所有这些人，这些人都在做什么？他们是真的在造一辆平托，还是在造一辆豪华车？他们在做什么？

克里斯汀·韦伯:我的意思是，我很好奇，唐纳德，你们是如何为公众做性能测试的。但我要说的是，云在很多方面改变了游戏规则，因为它没有消除风险，对吗？只是把它从一个地方移到另一个地方。它正在从内部迁移。这也带来了新的风险——以前不必考虑的新问题。对于自动扩展系统，有时人们会认为迁移到云意味着他们不必再担心性能，因为自动扩展。

令人担忧的是，当你在云中时，你真的会遇到更多的服务。您还可能遇到嘈杂的邻居和许多不同的场景，这些场景会从分布式系统引入瓶颈。我的意思是，你可以把 SaaS 应用程序放在法国，把硬件放在中国，把中间件放在第三个地方。您需要确保像这样的混合系统能够运行，可以假设它能够运行，因为它是云。您确实需要确保您的——无论是迁移应用程序还是对其进行平台迁移——您都有一个性能测试基准，您知道您正在衡量这些基准，以确保您在迁移到云时不会退步，并且您能够在迁移到云时再次测试这些基准  。

*唐纳德·卢茨:*我还有一个想法想补充一下，因为我已经差不多做到了。你可以运行你所有的服务——选择 AWS，Azure 或者 GCP。然后还有另一件事，你说，“嗯，我想在三个公共云中运行我在 Kubernetes 的所有服务。我真的不想直接消费提供商的服务。有一些新的、很酷的 API，我只想在 Kubernetes 中使用它们。所以你已经改变了你的混血儿不管跑哪都是 Kubernetes 的想法。因此，您并没有真正在公共云中使用它；您通过集群消费服务。所以这也改变了整个讨论。

*Andy Grabner:* 也许我想快速补充的是——我对你的问题的第一个回答是，Alan，这没关系，因为它——或者说它不应该有关系，云原生也是如此。当我们谈论云原生时，云原生并不意味着您的云原生应用程序必须在云中运行。云原生实际上意味着你如何设计你的应用，它们基本上可以在任何地方运行，对吗？所以不是哪里。云原生并不定义它在哪里运行，而是定义系统如何运行。这就是为什么我认为，也是 Kristen 的观点，比如说，你不能免费获得性能，或者你不能仅仅通过选中你最喜欢的云提供商的复选框来注册性能即服务或弹性即服务，然后突然之间你就会有奇迹发生。但是您仍然需要将所有这些决策考虑到您做出的架构决策中，并且最终您必须进行适当的测试。我也认为云是伟大的，因为突然之间我们有了许多我们可以建立并真正关注的服务。这是我们可以创造的商业价值，因为我们不需要投入时间，我不知道，维护一个数据库和某些类似的东西，因为有人会照顾它。

所以我认为总体来说，云是一个伟大的东西。从测试的角度来看，再补充一点——我想 Kristen，你也说过了，如果你必须做出明智的决定，在哪里运行你的软件，因为你总是需要记住你的最终用户在哪里，你的消费服务在哪里，因为这也意味着你需要从这些位置进行测试，因为你现在可能有不同的延迟。某个数据中心和某个提供商可能会产生不同的成本。我认为这些是一些额外的考虑因素，但一般来说，对于性能测试和可伸缩性测试，理论上我构建的应用程序是在一个云中、三个云中还是在本地运行并不重要。这是我的回答。不应该。

*Mitch Ashley:* Alan 也是，我认为云的一个真正改变游戏规则的因素就是对资源的访问。在组织中，当您在内部进行时，两个最大的瓶颈是硬件的获取和防火墙规则，说实话。你可以控制自己的环境，无论是资源还是安全，无论是什么。但是这种灵活性给了你更多，而不仅仅是更多的选择。您可以重新考虑如何自动设置环境，“让我们这样配置它”，您的排列，或者，“我们正在考虑以某种特定的方式改变它”，并且您可以自动测试它。所以看起来它给了你更多的灵活性。有时候，灵活性也意味着复杂性，但对我来说，这是迁移到云的最大改变之一。

*Kristen Webb:* 是的，我的意思是，硬件是性能测试中最昂贵的部分，就像你说的那样，通过它来采购资源、进行资源调配，以确保你可以在正确的时间访问它们并且没有冲突，这既困难又耗时。所以，你所说的实际上更多的是应用开发，云 CI 系统中的应用测试，这是一个完全不同的层次，除了云中的应用部署。这也是真正的爆炸式增长，它确实最小化了——使用 neo-load SaaS，您现在可以在五分钟内启动它并运行性能测试，因为它是使用 AWS 和 Google 的完全托管服务，我们会为您做到这一点。因此，这也是一个游戏规则的改变者。

但是，这也是我不同意安迪的一点点。无论你的应用在哪里，它都必须运行。它必须运行良好，但云确实会带来更多风险，因为——首先，它将风险从内部转移。到云，但这也是——你现在会遇到更多的服务，特别是当你有一个新的架构时，这是一个现代化的架构，它可能是——他们现在叫它什么，一个微型电梯？因此，在这种架构中，更多的服务将会对您产生影响。它可能真的是不相关的，当你有那种分布式系统时，你可能不知道瓶颈来自哪里。

Alan Shimel: 我的意思是，我认为云确实带来了更多的复杂性，如果你愿意的话，但是我的意思是，看。云的优点我觉得远远大于云的缺点吧？我认为在天平的两边都有筹码。但是你知道吗？我在开头提到，除了这个预先录制的*devo PS unbounded*集 2 月 24 日 ^日——我们确实为我们的观众举办了现场圆桌会议。因此，我想邀请正在观看此视频的所有人，如果您想了解更多关于构建云性能测试策略的信息，我们确实有这个现场圆桌会议。2 月 24 日我们邀请了来自 Dynatrace 和 Tricentis 以及更多公司的员工。有趣的是，圆桌会议被称为“云中性能测试的策略”，如果你在网上研讨会部分去了 devops.com，你可以在那里注册这个网上研讨会。我们称之为网上研讨会。这是现场圆桌会议。您将有机会回答您的问题，通过聊天直接与小组成员交流，并帮助您制定策略。所以不要错过，2 月 24 日 ^日 ，离现在只有几个星期了。

我们时间不多了。为了观众的利益，我想向你们三个提出另一个问题，对吗？好吧，好吧，你说服了我。我需要一个整体的性能测试方法。除了听我们三个或五个今天在这里，你能给我指一些好地方吗，如果我是观众，在那里我可以找到更多关于这个的信息，在那里我可以快速变聪明？唐纳德，我们让克里斯汀负责一切，所以如果可以的话，我想请你先来。

唐纳德·卢茨:好吧。嗯，我的意思是，有几本我喜欢的书不一定是关于性能测试的，但是其中一本——我总是忘记名字。就在那里，*建立微服务*山姆纽曼。这是一本非常好的书，已经出了第二版。还有一个是来自——哦，天哪，我想不起来他们在哪里了，但对我来说这是一个很好的参考，因为它涵盖了从文化到如何构建微服务，如何对其进行性能测试的所有内容。我喜欢很多书面的东西。有各种各样的视频。马丁·福勒夫妇特别谈到了这一点。所以这些都是我想不出来的。

Alan Shimel: 所以，如果我没弄错的话，我认为 Sam Newman 和 Martin 一样，都在 ThoughtWorks 工作。

唐纳德·卢茨:是的，他现在独立了。他自己走了，现在他做顾问。

艾伦·希梅尔:是的，是的，他们确实离开了。我记得。没错。安迪，你呢？

安迪·格拉伯纳:是的。我想说的是，这是我们在 Dynatrace 方面所做的一点商业内容，我们对 SLO 和服务级别目标有一个整体的方法，我们的 CNCF 项目 Kaptn，拼写为 K-A-P-T-N。这是一个 CNCF 项目，我们在那里所做的是，我们提供事件驱动的编排，将性能工程实际嵌入到您的交付流程和运营流程中。Neutis 和 neo-load 也有很好的集成，这意味着我们实际上在 Kubernetes 的基础上提供了一个框架，使开发人员能够简单地签入他们的代码，然后 Kaptn 协调部署和测试，如触发和 neo-load 测试，然后自动评估您的 SLO，然后将其推向生产，但始终评估 SLO，因此始终评估您的性能标准、弹性标准和业务标准。因此，如果有一件事，看看 Kaptn，我们的 CNCF 项目，因为我认为它肯定会有助于对性能工程有一个更全面的方法。

艾伦·希梅尔:谢谢你，安迪。克里斯汀，我把你留到了最后。

克里斯汀·韦伯:谢谢。有几件事。一个是我们有一个通过 Tricentis 运行的性能顾问委员会，但实际上它更多的是关于方法而不是产品，它组织了来自世界各地的所有性能专家，包括–Andy，我想你经常参与其中。Henrik 将在本月晚些时候参加我的网络研讨会，他以前负责这些性能顾问委员会，现在在 Dynatrace 工作。所以他也是一个很好的资源。

但是我们有一个绩效咨询委员会的网站，在那里你可以看到世界各地的专家讲述他们的故事，他们发现什么对他们有效，他们学到了什么，以及他们如何与各种开发过程相结合。除此之外，在 Tricentis.com/neoload 上还有大量关于 neo-load 正在解决的问题和我们如何解决这些问题的信息，我们在传统技术堆栈和 devops 技术堆栈之间的集成，以及我们如何与 Dynatrace 合作来帮助转移和带来生产反馈，以及我们拥有的所有可观察性监控工具。我们也有一个试验，可以了解更多。

艾伦·希梅尔:我喜欢它。嘿，克里斯汀，非常感谢。再次强调一下，Kristen 提到过，2 月 24 日，“云中性能测试的策略”，有一些非常棒、非常聪明的人，包括 Kristen。去 devops.com 看看。你可以注册，但是你需要注册才能参加现场圆桌会议。嘿，米切尔，我让你把它带回家。

米奇·阿什利:嗯，谢谢你，艾伦。我只是在思考并真正吸收我们的小组成员今天所说的话，我要说的是，我对我们思考方式的复杂性印象深刻，对现在从事测试工作的人的复杂性印象深刻。测试员是不喜欢编码的人，对，是不喜欢做开发人员的开发人员的日子已经一去不复返了。我们在测试中有一些非常出色的思想领导，无论是在正在创建的产品中，还是在试图解决复杂问题和有时有趣问题的人们中。所以对我来说，这是测试时间的一种复兴。现在是做测试员的大好时机。这是一个 QA 人员和从事测试工作的软件工程师的大好时机。所以这是一个很棒的话题，我希望人们能看看大家推荐的资源。

艾伦·希梅尔:你说得对。确实是。是一句古老的爱尔兰谚语，“愿你生活在有趣的时代”，还是类似的话？这是一个测试者的伟大时代。总之，唐纳德、安迪、克里斯汀，非常感谢你们今天来到我们的小组。米切尔，一如既往，谢谢你。感谢我们的观众。我们希望你觉得这很有趣，如果你发现了，我会再一次鼓励你:2 月 24 日，“云中性能测试的策略”报名参加吧。不要错过它。我觉得会很棒。但在那之前，我是艾伦·希梅尔，为大家带来*devo PS unbounded*。非常感谢我们的赞助商特里森蒂斯。感谢大家的收看，我们很快会在另一期*devo PS unbounded*节目中再见。