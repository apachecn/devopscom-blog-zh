# devo PS Chat:Aviatrix 的企业多云主干网

> 原文：<https://devops.com/devops-chat-enterprise-multi-cloud-backbone-with-aviatrix/>

我们的播客嘉宾认为，六个月前的一个星期二，世界发生了变化，企业向云迁移势在必行，而不仅仅是一个远大的目标。在帕洛阿尔托网络公司(Palo Alto Networks)和尼奇拉公司(Nicira)获得成功后，这一灵光一现的时刻足以让史蒂夫·穆拉尼(Steve Mullaney)不再袖手旁观，重新回到游戏中担任 Aviatrix 的首席执行官。

“构建”对于云原生应用来说可能是一个很好的方法，但是企业希望在迁移到云之前就制定好框架。想想企业云 IT 参考架构，就像思科为企业 IP 网络提供的架构，DEC 为客户端-服务器提供的主流架构，以及 IBM 为大型机计算建立的架构。你必须把云带给他们。这种企业云参考架构正是 Aviatrix T1 的目标，与推动客户自由转向 AWS 的信用卡购买模式相同。

在我们的 DevOps 聊天播客中，Aviatrix 的首席执行官 Steve Mullaney 谈到了企业希望在真正的企业云计算主干中获得什么来支持他们的需求。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/636827859&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/636827859&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

米奇·阿什利:大家好，我是米奇·阿什利和 DevOps.com，您正在收听的是另一个 DevOps 聊天播客。今天，Aviatrix 的首席执行官 Steve Mullaney 和我在一起。我们今天的主题是企业云计算主干网——有内涵的好东西。

史蒂夫，欢迎来到 DevOps 聊天。

史蒂夫·穆拉尼:谢谢你邀请我，米奇。

阿什莉:太好了，很高兴你能来。我想从你自我介绍开始。我知道我们很多人从你的背景了解你，你是一个相当有名的人，但告诉我们关于你自己。

**Mullaney:** 我叫 Steve Mullaney，在过去的 35 年里，我一直从事网络和安全基础设施方面的工作。我实际上是在 80 年代中期开始我的职业生涯的，当时我们正在从大型机计算模式向客户机服务器模式发展。我实际上是一名来自 SynOptics 公司的 10Base-T 工程师。所以，你们中那些已经存在了足够长时间的人应该还记得以太网是什么时候开始的——

阿什莉:我记得。

**穆拉尼:** 10Base-T 开始了，耶。我职业生涯的大部分时间都在网络和安全领域，我是一个非常早熟的人，实际上，也是在帕洛阿尔托网络公司，我是那里的第一任营销副总裁，员工编号 25。然后是一家名为 Nicira 的公司的首席执行官，这实际上是许多 SDN 热潮和网络虚拟化的开始。我们被 VMWare 收购了，然后我在 VMWare 呆了几年，发展了这项业务，现在它已经是一个价值近 20 亿美元的 ________ 企业。

然后，在过去的五年里，我只是，我只是说不再担任运营角色，并且是董事会成员，我很满足于在我的余生中一直这样做，并且很高兴实现自己的梦想。大约六个月前，我看到了世界的变化，企业一直在谈论向云计算模式的转移，老实说，过去 15 年来一直在谈论这个问题，但我注意到，大约 6 个月前，主流企业真的说:“好的，我们正在这样做。”我只是看着那个机会说，“我的上帝。”

当时我是 Aviatrix 的董事会成员，所以我可以提前看到这一切的发生，然后说，“如果不参与的话，这将会非常有趣。”

阿什莉:那么，是什么？大约六个月前是什么？你是在什么时候看到一个让你不再退休的变化的？

穆拉尼:是的。有趣的是，我喜欢说，六个月前的一个星期二。感觉差不多就是那样——就像，真的是在星期二。企业就是这样运转的，对吗？他们谈论它，他们谈论它，他们谈论它，他们谈论它。就像在节食一样。你谈论它，“我要节食了。”“嗯，今天怎么样？”你会说，“嗯，你知道——今天不太好。”“嗯，明天怎么样？”"你得从周一开始"，对吗？然后，“下周一怎么样？”“嗯，那真的不行，因为我要去度假。”

我的意思是，有所有这些借口，企业，大约五年前，真的说，“好吧，我们要转移到云。”老实说，那时每个企业供应商都会说，“我们死定了！”对吗？“我们死定了。所有东西都会进入亚马逊，我们就死定了。”

阿什利:嗯。

Mullaney: 而发生的事情都不算什么，因为企业只是说说而已。他们不是真心的，对吗？因此，每个人都一个季度接一个季度地创下新高。直到大约六个月前，我还是 Aviatrix(一群其他基础设施公司)的董事会成员，我注意到这些标识正在发生变化。这不再是网飞，也不是中小型企业，这些都不是早期采用者。这些是中西部的制造业，保守的公司。到底发生了什么事？他们不应该这样做！

人们认为仅仅因为 AWS 有 300 亿美元的运行率，我们现在就一定已经跨越了鸿沟。我们没有。我注意到，在我所在的所有基础设施公司中，他们看到的都是同样的事情。没有人做任何不同的事情，只是，市场发生了变化。而且企业走的路，都是从众心理。当大多数，你知道，早期和晚期的大多数客户都决定做一些事情时，他们都在同一个星期二早上决定，我看到了这种情况。

我们在客户端服务器中看到了这一点。当时我在 SynOptics 工作。大型机计算是企业计算的方式，而客户机服务器——PC 客户机服务器被视为玩具，只是娱乐和游戏。所以，打印共享，对不对？个人电脑——那不是真正的计算，对吗？

**阿什利:**嗯哼，嗯哼。

**穆拉尼:**然后发生了什么？突然，在 90 年代早期，在一个星期二的早上，每个人都认为互联网协议是唯一重要的协议。一夜之间，所有其他协议都消失了，PC 客户端服务器是我构建架构的方式——这是一夜之间发生的。我看到同样的事情发生在云上。

阿什利:嗯。所以，这真的有点成为主流，你会看到一个真正的—

穆拉尼:已经成为主流了。我作为 Aviatrix 的首席执行官已经在该公司工作了三个月，每天我都看到越来越多的证据表明，公司正在烧毁船只，也就是说，公司的数据中心和公司的主干已经死亡。现在这是一项支出。我将它视为一项支出，并将我在公共云中利用公共云所做的任何事情视为一项投资。

阿什利:嗯。

穆拉尼:这意味着我所有的人都在关注这件事以及我的所有开销。它会在一夜之间改变，这是一个群体。全世界的每一个企业现在都在同一个星期二的早上做出同样的决定。

阿什利:嗯。我喜欢你周二早上的比喻。

**穆拉尼:**是不是很搞笑？不过，这是真的——这是真的！

阿什利: [ *笑声* ]这就像是突然发生的一样。

穆拉尼:是的。

阿什莉:所以，你是多家公司的董事会成员。你说“这是我要骑的那辆”是怎么回事？这就是我要搭上的，我要成为首席执行官，带着这个宝贝去它要去的地方"？

**Mullaney:** 是的，我认为是这样的——因为这符合我们所说的使命，我们的使命是构建企业云计算骨干。

所以，当你看到 AWS、Azure 和 GCP，甚至 AWS 对企业的口头禅都是，“去构建”嗯，当你是一个早期采用者，他们递给你电动工具，而你—

阿什莉:嗯，绿地。

穆拉尼:是的，你很有创新精神，你想去建造。当你是一家中西部的保守制造业公司时，这种情况就不太好了。我要用电动工具砍掉我的胳膊。我不想要电动工具。我想要一栋房子，我想要家具，我想带着它走进去。我不想建造任何东西。

阿什利:我想要一个简易机场，我不想建跑道。

**穆拉尼:**绝对。我不想建造。所以，老实说，我认为这也让 AWS 措手不及，对吗？因为他们认为——我们所有的客户都喜欢这一点——这是一句“开始构建”的口号。不是主流吧？翻转的时候不会。不是当你已经越过了鸿沟，现在你在龙卷风中，每个人只是，他们已经走了，说，“这是它。”

所以，我看着那个，我说，“我的上帝，所有这些企业都在乞求——乞求——有人为他们定义架构。”这就像在客户端服务器中，他们需要思科出来为他们定义网络和安全架构。给我每个人都会做的规范架构，然后我会去实现它。

阿什利:事实证明，我们不是在发明。

Mullaney: 这就是人们想要的，他们想要一个经过验证的设计。他们希望能够去，“这是每个人都在做的，我们都同意，这是你应该做的。哦，顺便说一句，我不能从亚马逊得到，因为亚马逊试图把我锁在亚马逊。我做不到——我无法从 Azure 或谷歌获得它。我从旧世界得不到，从思科得不到，因为他们连这个都不懂，“对吧？

能够——就像，你不会去 IBM 或 Deck 寻找客户机服务器架构。这是一个完全不同的计算模型。你不能——根据定义，旧的领导人永远不会是新的领导人。那么，我该去找谁？

**Ashley:** 是的，说到多云，你可能不会只有一个云，对吧？对于一些微软应用程序来说，在 Azure 上运行可能很有吸引力，但你也有令人信服的理由去其他地方。

Mullaney: 我还没有见过一家企业说他们只会在一个云中。他们至少在三楼。因为如果你在中国，你就在阿里巴巴。然后，你知道，数据主权和 GDPR 以及所有这些其他问题，我可能不得不在欧洲有多个供应商，一个国家一个国家，对不对？甚至不是 AWS。

所以——当然，绝对，它将会是，也应该是。因为并不是说你要把工作负载从一个转移到另一个。就像，那是不可能的。但接下来会发生的是，也许营销团队因为人工智能的原因喜欢 GCP，或者，你知道，我从 Azure 的 Office 365 开始，所以我正在离开。或者说我是大企业，制造企业，微软真的懂我。或者我是一个零售商，我不会有任何 AWS，对不对？

阿什莉:是的。

**Mullaney:** 或者我看，甚至，我是一个客户，我是一个公司——一个软件公司。我要卖给其他企业。如果我向零售商销售，我就不能拥有我的基础架构。我甚至不能在 AWS 上拥有自己的内部基础设施，因为他们不希望这种情况发生。

所以，毫无疑问，它必须跨越这一切。另一件事是“去构建”的咒语——所以，即使你可以说，“我能想出如何在 AWS 上构建”，Azure 和 GCP 的构造是不同的。

阿什利:没错，你必须到处去建造。

Mullaney: 所以，现在我需要学习这些构造，现在我必须去那里建造，但使用不同的工具，以不同的方式工作，比如，一个在公制系统中，一个在美制系统中。就像——哦，我的上帝，你知道吗？工具也不管用。就像—好吧，这太荒谬了。

阿什利:所以，你描绘了一幅多种令人信服的理由的图画，有人需要为我打下基础。我必须是多云计算，所以我需要能够跨多个提供商工作的参考体系结构。我不想再坚持构建，我希望能够走进去，将我的应用程序插入一个框架，一个我可以使用的参考架构——这就是 Aviatrix 的意义？

**穆拉尼:**是的。然后在上面分层，利用这些结构，对吗？利用美妙的衬底，对不对？想想所有的光纤、pop、数据中心和区域，以及 AWS Azure 和 Google 提供的所有精彩的东西，并且还在增长。

阿什莉:所有你不需要做的基础设施。

穆拉尼:这太不可思议了，对吧？你猜怎么着？我是一个网络和安全软件高手。所以，当你想到像 WhatsApp 这样的人时，你知道，在& T 总是非常生气，因为 WhatsApp 被脸书以 300 亿美元或其他什么价格收购，在& T，他们有所有的纤维、所有不同的 pop、所有的权利和其他类似的东西——他们的市值是多少？我不知道。可能不会比那更多。你会问，“这是为什么？比如，我做了所有这些事情，却没有得到任何荣誉。”

阿什莉:去那里要花更多的钱。

Mullaney: 然后 WhatsApp，你知道，六个工程师以 300 亿美元被收购，在哪里？嗯，是的，因为在顶端的家伙，这是所有的价值所在。他们在利用它。

所以，从某种意义上说，我们是一个软件玩家，但我们超越的不是美国电话电报公司之上的互联网，而是新的互联网。是超大规模的。它是 AWS、Azure、Google 等等，所有这些都具有巨大的带宽和最佳的延迟，当我们在上面覆盖这些分离的安全服务时，组合是一个惊人的架构和网络。

阿什莉:那么，谈谈那些服务吧。谈论安全操作、扩展、传输—所有这些你需要注意的事情，协调—这些如何与 ABHS 一起工作？

穆拉尼:是的。是的，在这个我们称之为企业多云主干网的系统中，你知道，现在可能有七八种不同的服务可供客户开始使用。这件事的美妙之处在于，你可以使用 Aviatrix。我们现在有 300 多个客户，并且在全球范围内快速增长——客户遍布全球。我们甚至不知道这一点，因为这是低摩擦土地和扩大。一个真正的云模型，他们可以真正开始。可能是 500 美元一个月。可能是每月 50 美元。也可能是每月 3000 美元。他们刚刚开始使用它，他们可能会停止使用一个用例。“让我试试看。”他们获得信用卡，通过 AWS Marketplace 或其他市场整合，突然之间，他们就开始收费了。你猜怎么着——下个月，他们补充道。他们补充道，下个月。他们补充道，下个月。然后他们说，“哦，我现在需要额外的东西，”对吗？

所以，他们可能会从一项我们称之为用户 VPN 的服务开始。所以，基本上，我们采用 OpenVPN，并为其添加许多附加功能，将其与 SAML 和其他身份验证方法集成，添加一些更多的安全控制，并说，“嘿，我有用户，我想让他们通过 VPN 进入云，因为我在云中有资源。我希望他们能够安全地连接到云。”

这可能是你开始的第一个用例，也许你每月支付 1000 美元，但从那里开始，它将开始增长，然后你会说，“嗯，现在我需要公交网络”，对吗？或者，“我需要出口过滤。所以，你猜怎么着，我开始进入云端。”你猜怎么着，你的大多数 VPC 和云中的资源都必须访问互联网上的东西来构建包等等，对吗？因为这是一个非常分散、混合的世界。所以，不仅仅是在云中。你猜怎么着？我想对出站进行过滤，我想做所谓的 FQDN，完全合格的域名，我不想根据 IP 地址进行过滤，或者让他们去任何他们想去的地方。我想说，“你可以去任何地方，yahoo.com 或任何你需要去的地方。”

阿什利:嗯。

**穆拉尼:**就这样。因此，您希望能够将其列入白名单，并且希望能够为每个用户和每个 VPN 定义它。因此，您希望能够制定谁可以去哪里的安全策略。这是另一个用途。

另一个用例是加密。你知道，现在，人们说，“好吧，你运行”——你知道，六个月前，当云是一种乐趣和游戏时，“嘿，我把工作负载放在那里，这真的没关系，这不是我的企业。”你知道，也许你不担心加密。但是现在，你是一个零售商或者银行，你知道，突然之间，你关心了。所以，你会想要—

**Ashley:** 是的，如果你要放一个企业应用程序，你会错过加密，安全，这是很高的[ *相声* ]。

是的，是的。你想在飞行中加密，对吗？因此，我们不仅允许加密，还允许高性能加密，对吧，到 10 千兆、20 千兆、30 千兆甚至更多，这一点很重要，因为人们正在把 PII 数据和其他东西。此外，从安全角度来看，人们知道—看，我只是要加密所有内容。数据以及在途数据。

然后，你知道，正如你所说的，能够跨多个云实现这一点，对吗？因此，我可能可以连接，我希望能够连接一个云中的多个区域，但我也希望能够连接到其他云，并在我们正在做的基础上创建一个共同的框架。

然后，我会说另一种服务是我们所说的防火墙网络服务，这是另一种服务，我可以更具体地谈论它。但是每一个即将进入云计算的人——再一次，这不再是有趣的游戏，这是一件严肃的事情。他们说的第一句话是什么？安全和策略，我需要将我的下一代防火墙策略带入云中。我需要—因此，如果我是 Palo Alto Networks 的客户，我想做的第一件事就是将我的虚拟机系列引入云中。当我尝试这样做时，AWS 说您可以将 VM 系列防火墙连接到 AWS 的结构会在性能、可扩展性和可见性方面强制妥协，这是站不住脚的。有了 Aviatrix，我们消除了这些权衡。

**Ashley:** 这当然是你开始构建基础设施的基本要素。如果你能把你自己的网络安全带入云中，那就更好了——这就是你的策略，是的。

穆拉尼:是的。嗯，你知道，我认为重要的是，我认为像亚马逊这样的人正在意识到这一点，当你不得不处理，当你处理企业-我的意思是，企业。中西部，保守，经典的主流企业，对吧？你必须把云带给他们。你不能让他们去云端，对吧？他们看着这个，说，“好吧，我全押。我已经烧了船，我要摆脱我的数据中心，我全身心投入。”但是他们看了看，然后说，“草没有我想象的那么绿。”

阿什利:嗯。

穆拉尼:这里有很多烧坏的斑点。这个“去建造”的咒语？哇，哇，哇，哇——等一下。我以为我只要点击几下就完事了。哦，顺便说一下，公司的首席执行官和首席信息官，他们都被收买了，他们说，“嘿，你知道，我们以前有数百人管理本地的基础架构，但我了解云。我现在只需要十元，对吗？

阿什利:嗯。

**Mullaney:** 所以，问题是，【*笑声*】他们去了云，同样，我到处都看到这种情况，每个企业都说，“我们真的没有足够的人。”就像，我们在这里卖了一堆东西。每个人都告诉我们这就像咔嚓，咔嚓，咔嚓——你完了。没那么容易，对吧？然后你抛出，“现在，我要穿过多朵云——我不知道我们要怎么做。”

**Ashley:** 那么，让我来问你，我们在这里的时间即将结束，如果你对那些在前六个月时间内真正考虑迁移到云或正在迁移的企业有一个临别建议，他们想了解 Aviatrix，他们可能想做一个原型或参考，他们如何在平台上构建参考架构，他们如何开始？做那件事的最好方法是什么？

我的意思是，我总是告诉人们的第一件事，最好的开始方式实际上就是开始。这个现代世界的好处是，我们不必做概念验证。我们不需要这样做——您实际上可以在周末开始，我们的许多客户就是这样开始的。他们只是开始玩我们的软件，比如在 AWS Marketplace 上，这是一个很好的起点。他们只需旋转一个控制器，旋转几个网关，他们——我们有快速入门指南来告诉您如何以非常简单的方式完成。人们开始玩它，他们说，“哦，那很有趣。”

因此，他们从一个用例开始，对，非常小的一点点，他们有效地做他们自己的小概念验证。他们说，“好吧，这很有趣。”现在，我们也可以为他们这样做，但这是一个很好的开始。

我要说的另一件事是，你真正要寻找的是——我的意思是，人们现在不使用 Aviatrix 的原因只有一个，那就是他们从未听说过我们。一旦他们——一旦我们和人们交谈，他们就被卖掉了。因为他们看了看，然后说，“这正是”——人们说，“这正是我要找的。我需要有人来帮助我构建我的多重云、我的企业——我的、我的，而不是其他人的，我的企业的多重云主干，以及所有这些网络和安全服务。这就是我需要的，而你们是为我做的？这正是我所需要的。”

阿什利:嗯，太好了。非常感谢你和我们在一起。我们已经到达另一个 DevOps 聊天播客的结尾。似乎时间永远不够。感谢 Aviatrix 首席执行官史蒂夫·穆拉尼加入我们的讨论。

**穆拉尼:**太好了。

阿什利:谢谢你，当然也谢谢我们的听众加入我们。我是 DevOps.com[的米奇·阿什利。您已经听到了另一个 DevOps 聊天。感谢加入我们。](http://DevOps.com)

— [米切尔·阿什利](https://devops.com/author/mitchellashley/)