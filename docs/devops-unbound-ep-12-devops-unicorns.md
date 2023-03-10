# EP 12: DevOps 独角兽

> 原文：<https://devops.com/devops-unbound-ep-12-devops-unicorns/>

选择 DevOps 供应商时，您应该寻找什么？你所在行业的其他人在做决定时使用的是什么标准？您如何选择一个非常适合您组织的供应商？你怎么知道你的选择是否正确？在这一集的 devo PS unbounded 中，主持人 Alan Shimel 邀请 Comcast 的 Larry Maccherone、Red Hat 的 John Willis、Smithsonian 的 Ravyn Manuel、Capital Carbon Consulting 的 Garima Bajpai 和 Accelerated Strategies Group 的 Mitch Ashley 参加关于 devo PS[unicorns](https://devops.com/?s=unicorns)的专题讨论。下面是视频，后面是对话的文字记录。

[https://player.vimeo.com/video/540307174](https://player.vimeo.com/video/540307174)

**艾伦·希梅尔:**大家好。欢迎来到 DevOps unbounded 的另一个版本，在这里我们谈论 devo PS，因此得名。感谢加入我们。这一集的标题是开发独角兽:寻求端到端的开发。

你知道，我已经在 IT 行业工作了 30 多年，总是有这种紧张或这种钟摆在一个令人窒息的解决方案和任何领域的最佳解决方案之间摇摆。如今是开发运维以及软件交付和部署。但是在任何事情上，在安全领域，在所有事情上，在主机上，在基础设施上，它总是一个共同的主题。但现在在 DevOps 领域，这个问题变得非常非常尖锐。我们召集了一个我们认为很棒的小组来讨论这个问题。让我把你介绍给他们，然后我们从那里开始。

首先，我想欢迎，很久以来第一次来到这个小组，我的朋友拉里·麦克切龙。拉里，欢迎来到自由的 DevOps。给人家一点背景，如果你不介意的话。

拉里·麦克彻龙:当然。谢谢你邀请我来，艾伦。首先，我想说的是，我在康卡斯特发起了开发精神病转化项目，并持续了五年。不过，我本质上是一名开发人员，所以我是那种理想的人，在大企业之外采取实际上变得越来越普遍的做法，开发心理变态者，并尝试在像 Comcast 这样的大企业内部实际上采取多样化的方法。所以我所有的经历都是围绕着这个，最近五年左右，围绕着这个。

**希梅尔:**优秀。接下来让我给你介绍，她是 devo PS unbounded 的常客。加里玛，如果我弄错了你的姓，我提前道歉，但是加里玛·巴杰帕伊。接近？

**加里玛巴杰派:**差不多。是啊。所以我是加里玛·巴杰帕伊。我住在加拿大的 _____，我是加拿大 DevOps 实践社区的创始人，该社区有三个分会:多伦多、渥太华和埃德蒙顿。我还是 11 月 8 日和 9 日在加拿大举行的 DevOps 峰会的组织者。我还作为大使与 DevOps Institute 和 CD Foundation 等组织有联系。

**希梅尔:**妙极了。加里玛，我为你的姓道歉。我的错。我正试着读它，但是不戴眼镜的话，显示器离我太远了。但是谢谢你纠正我，欢迎。

接下来，我的另一个好朋友，我在数字无政府主义上的商业伙伴。虽然这不是他这些天的全职工作；他正忙于他的红帽子事业。独一无二的笨蛋约翰·威利斯。约翰，欢迎你。

约翰·威利斯:谢谢你，先生。谢谢你艾伦。嘿，是的，约翰·威利斯，推特上的 Botchagalupe。我目前的工作是在红帽公司一个名为全球转型办公室的团队中。我很幸运能和安德鲁·克莱·谢弗在一起。凤凰计划的合著者凯文·贝尔；还有杰贝·布鲁姆。很快，你知道，我已经在这个行业 40 多年了，10 或 11 家创业公司，12 本书，如果有人数的话。可能最值得注意的是《DevOps 手册》的合著者。

基本上也参与了最初的 DevOps 时代的开始和建设。我是第一个 DevOps 日的唯一美国人，达蒙·爱德华兹和我在美国创立了第一个 DevOps 日活动。

是的。这只是部分清单，约翰。谢谢你今天加入我们，伙计。

然后我想介绍——她现在不在镜头下，但希望当你在看这个的时候，至少你能看到她的照片，但她在视频上有些困难，但很高兴有她的音频，我的朋友，Ravyn Manuel。瑞雯，欢迎你。如果你不介意的话，给大家介绍一下背景。

谢谢你，艾伦。我很感激能上你的节目。太棒了。它让我发笑。我是美国国家非裔历史和文化博物馆的高级应用程序开发人员。我也是那个部门的开发工程师。作为一名开发人员，我实现了一些你在博物馆里玩的动手互动，作为一名开发运维工程师，我负责开发运维的所有事情，从云解决方案到我们如何——从应用程序开发方面，我们如何使用云以及工具和编写策略，并让我的领导了解所有的好事情。

**希梅尔:**妙极了。Ravyn，欢迎并感谢你今天加入我们。

最后但并非最不重要的是，我在 devo PS unbounded 的搭档，米奇·阿什利。嘿，米切尔，欢迎你。你想自我介绍一下吗？

米切尔·阿什利:太好了。很高兴来到这里。伙计，多好的面板。我很高兴今天能和这些人在一起。是的，我是加速战略小组的负责人，当然是专注于开发运维、数字化转型、全面网络安全和云的分析师。我还是 MediaOps 的首席技术官，负责平台战略和技术，所以我们过去常常交付这样的项目。

像 John 一样，我认为我们在这个行业的时间可能差不多，我的学分为零，所以他在这些领域取得了很大的进步，但他也是一名初创人员，管理许多软件项目、产品、IT 团队以及供应商。所以这将是一个有趣的讨论。

绝对的。我应该提到 DevOps Unbound 是由我们在 Tricentis 的朋友赞助的。为了让你知道他们是多么伟大的赞助商，他们今天甚至没有任何人在我们的小组里。但他们确实让这部剧每隔一周就能上演一次，非常非常感谢特里森蒂斯。

John，我已经说了，这是一个棘手的问题，我们可以支持多少供应商，我如何打包不仅仅是单点解决方案的解决方案，或者我只是想要单点解决方案。这里的答案是什么，约翰？

威利斯:答案是，艾伦，如果我有正确的答案，我会说我现在在墨西哥湾的格雷迪-怀特号上。

**Shimel:** 正是。我会和你在一起。

威利斯:但是不，我认为这是一个很棒的小组。我同意米奇的观点；我对我们所有人都可以进行的讨论感到兴奋。我认为这个问题——你知道，我想的是那种中文诅咒翻译，“愿你生活在有趣的时代”，对吗？这显然是我们现在的处境。我想你的问题是从转变开始的，对吗？就像这样——谈到你，Mitchell，我们中的一些人已经在这里呆了很久了，就像以前一样，有这样一个问题:一个喉咙哽住了，还是我应该和计算机同事一起做 ELA，还是零碎的事情，对吗？可能只有不到 1%的企业是自己动手的。

今天你可能会发现——我只是在炫耀这个数字，但它可能超过 10 %,也许 15 %,也许更高的公司现在正面临着自己做这件事的挑战。你知道，库伯内特就是一个很好的例子。这是一个开罐器，让公司决定我的供应商是否跟上了我应该自己构建的基本上游技术。

因此，我认为这就是我们要探讨的问题，更重要的是，您是通过内部构建来解决您的问题，以跟上市场和技术的变化，还是尝试寻找一对供应商或一家供应商，而很少有一家供应商能够让您全面了解当今现代技术的发展。但我认为这是一个问题，我认为我们今天谈论它会很有趣。_____.

**Shimel:** 我不反对。面板？

曼纽尔:艾伦，这是雷文。我同意你，约翰。我认为其中一件事——因为这对我和我的组织来说是一场斗争，那就是我们在实施 DevOps 方面需要帮助，但我认为供应商非常注重工具，而工具就像是堆栈中的第三优先级。当我为如何实施 DevOps 制定战略时，我看了看，我们在谈论工具。我关注标准，因为如果他们正在制定标准，并且该工具必须遵循该标准，那么它就是即插即用的，你不会得到——就像如果 Docker 决定他们将停业，那么你可以有另一种容器类型的技术来做这件事。

所以当我们看到御术师的时候，我们实际上是在一点一点地做，因为我们真的是独角兽。我们不是软件公司，我们没有软件产品；我们有数码产品，而且都是一次性的。所以这真的取决于什么适合我们。因此，我们并不真正倾向于单一供应商解决方案；实际上，我们会根据我们的业务问题，寻找能够帮助我们实现目标的人。

**巴杰派:**优秀。我想补充一些东西，因为当我们更深入地探讨这个话题时，我们会发现这个硬币有两面。一部分是从成熟度的角度来看一个组织所处的位置。第二件事是您正在寻找哪些供应商和关键能力。但是，如果你看硬币的两面，有三件事需要在整体环境中校准这些 DevOps 工具。首先，我想重申一个事实，因为我来自一个非常复杂的大型组织背景，拥有一个企业架构视图非常重要。因此，我建议甚至在采用单供应商或多供应商讨论的方法之前，我们需要对所需的关键功能进行分类。因此，无论是单个供应商可以为您提供企业 it 架构功能，还是您的组织将提供这种功能。所以这很重要。

我认为同样重要的第二件事是协调层。您知道，您必须对总拥有成本、合规性、安全性、身份访问管理进行治理，并且必须有一个协调层来整合所有经过校准的开发运维工具。因此，这是一个问题，即您是否希望在组织内部构建它，或者您是否有一种以供应商为中心的方法，在这种方法中应该或可以引入这种功能。

这就像两件事，然后你开始校准这些 DevOps 工具。因此，您不必考虑法规遵从性、安全性、治理、总拥有成本等基础方面，工作变得容易多了。问题是，你知道，如何带来这些 DevOps 工具并实现商业价值。

**Maccherone:** 我想重复一下流程编排层的概念，但我想稍微回顾一下——在这里，unicorn 和同类最佳之间有一种二元差异。但我认为，在独角兽这个范畴内，真的有两种截然不同的主要独角兽，所以我想把这两种味道说出来。你有这些弗兰肯斯坦供应商，他们将收购拼凑成这个怪物，这些都不是愉快的经历。在这种情况下，您从一个供应商那里获得的唯一好处是拥有单一主服务级别协议的合同好处。你没有得到一个集成的产品，它真的允许你实际上平稳地做工作流，坚持开发人员用来为你的公司产生价值的工作流。

此外，在 DevOps 领域还有另一类独角兽，但在安全领域就没那么多了，我马上会谈到这一点，它们采取了市场方式。这不是 DevOps 供应商，但我认为第一个真正实现这种市场方法的供应商是 Atlassian。你知道，他们有一个非常棒的产品，但他们说，“好吧，插入这个产品”，他们创建了 API，他们创建了工具包，他们创建了整个社区。大多数人都是免费做的，他们只是为自己做，然后与社区分享。但是其中一些人成为了小贩，在亚特兰蒂斯的市场上出售他们的产品，然后亚特兰蒂斯收购了他们。当他们被收购时，他们已经与 Atlassian 的其他产品预集成，所以他们的收购 unicorn 方法最终看起来不像是弗兰肯斯坦的怪物，因为他们是用供应商的 API 构建的。

我认为 Github 确实采取了市场的方式，而且做得非常好，甚至进入了安全领域。所以我认为这种独角兽——在较小的程度上，Github 也不存在弗兰肯斯坦怪物的问题。然而，安全领域还没有人真正实现市场方法。我们有一些弗兰肯斯坦和弗兰肯斯坦怪物，但我们没有一个完整的市场方法。我在等人来做这件事。我认为这将是一个巨大的胜利，有人 _____。

**Willis:** 我想就此做一个完整的播客，因为这是我现在一直在思考的问题，即什么是端到端安全。但是如果我现在开始的话，会占用太多时间。所以我想对一些事情发表评论。首先，Ravyn，我认为关于标准有趣的是，我同意，对吗？我们现在的问题是弄清楚哪些标准实际上会持续下去，具有可塑性。我的意思是，这是我一直在努力研究的事情之一，就像 OSCAL 对 OVAL 对 S-CAT 对，你知道，只是 NIST _ _ _ _ _-为了-我的意思是有这么多事情，他们都有一点点不同的方法。

所以我同意，我们现在必须处理的问题是，你知道，我们可能生活在一个有趣的时代，就像选择一个早期的供应商，就像我喜欢这种供应商技术，但他们会出现吗？他们会被一家我不太想与之做生意的公司收购吗？我认为标准太复杂了。

我想说的另一件事是，我认为对于供应商来说，我不是 _____，因为我为 Red Hat 工作。因为我现在要说的是，在宏大的技术计划中，如果你打算选择一家供应商，请四处看看。你知道，我要说的是。我很乐意被纠正，我不是说，你知道，红帽，因为我在红帽工作。任何认识我的人都知道，我不是我工作过的任何供应商的骗子。但是是 VMware 和红帽吧？他们可以跟上——因为你必须——在这个世界上，你必须有员工，他们的全职工作是开源项目的贡献者。

如果你想一想 Kubernetes、clusters 和 server list 的情况，你会想到这两家公司在这种规模的版本中定位非常好，能够跟上技术的复杂性和变化，因为他们投入了资源。我的意思是在那之后你可以列一个更长的清单。我也不包括云提供商，因为这是一个不同的故事。

但无论如何，这是我想对人们谈论的一些事情发表的两点意见。

阿什莉:我只是想跳进去。这场对话的迷人之处在于它的多样性和复杂性。有许多方面需要考虑，无论是像 Garima 和 John 所说的企业架构，还是能够实现它的供应商。拉里也是，如果你说的是这种累积战略，而是复古整合战略。

我认为另一个需要考虑的方面是，当涉及到供应商、软件和工具时，每个组织都有一个关于他们如何思考和操作的 DNA。虽然我并不总是一个随波逐流的倡导者，但有时当你在思考我们如何采纳一些东西时，想想组织是如何运作的。如果您是一家大型工具供应商，让我们与 Red Hat 或 VMware 或 Broadcom 或任何可能的供应商合作，考虑一下这一点。通常，你知道，给自己留点脑细胞，多活一会儿。

还有创新曲线，驾驭创新曲线的一些最佳方式是开源路线和围绕这种策略构建的供应商。所有这些都有组合。

因此，我想我要在这里的谈话中补充的一点是，想想你如何将你的战略与组织的 DNA 相匹配，这样你就可以在不杀死尽可能少的脑细胞的情况下完成尽可能多的事情。

**Bajpai:** 谢谢你，Mitch，提出了组织 DNA 的这个观点。我认为这是我们正在进行的对话的途径。我确实相信这种心态正在转变，甚至我在大型传统企业中也看到，他们已经开始意识到，这种基于供应商的方法需要转变，他们需要在这种背景下让人们成为合作伙伴。因为当您考虑 DevOps 时，它基本上是探索您的机会，打破您的技术入门的障碍，差距-您在过去创造的一致性和结果差距。

我认为这是一个机会，组织可以通过这些合作伙伴转变并带来更多的创新机会。因此，我真的认为，这次对话还有一些更软的方面，我们需要考虑一下，传统上合同是如何 _____ 的，我们如何从供应商的角度看待这些 DevOps 工具，我们如何让他们成为合作伙伴，如果我们开始这样做，我们需要改变什么。

这不是一朝一夕的事，对吧？所以我们必须设定我们需要引入什么样的建模实践。这打开了另一扇可能性的大门。在这次谈话中，我们可能会有机会讨论我们在组织中建立的这些 SLA 约束，这些约束引导我们选择特定的供应商，或者引导我们选择特定的窗口，通过该窗口我们可以外包大量功能，这是一种“掐脖子”的方法，对吗？

因此，让我们在即将到来的讨论中提出这些观点并加以强调。

Ravyn，我知道史密森尼是一种准政府，或者说它不是真正的政府。但是对于 Garima 关于 SLA 的观点，以及只能与这样选择的供应商打交道，它是；这是一个真正的管理者，取决于你选择最佳产品的能力，取决于你选择如何做事的能力。对你的经历感兴趣。

曼纽尔:这很难。我一直在听这段对话，我不知道为什么我会有这种感觉，但是供应商，我喜欢红帽，所以我不想谈论红帽或任何东西，也不想谈论开放式。但是，如果你有一个合作过并且信任的供应商，比如史密森尼，我们会在 OCIO 大量使用 Red Hat。Red Hat 正在做 open shift 和 Kubernetes，他们正在将自己的工具推向这些特定的工具。对我来说，作为史密森尼的一个单位，我可能不想使用开放班次，我可能不想使用 Kubernetes，但我实际上没有选择，对不对？因为该供应商是一个很好的供应商，他们有很好的工具，但是他们为我选择了我将要使用的工具，这让我很难说“这真的符合我真正需要的吗？是不是太多了？”

因为我可以告诉你，我交谈过的许多供应商，他们希望我们使用这种产品套件，这对于我们想要做的来说太多了，所以我只能选择要么与该供应商合作，超支并使用我并不真正需要的工具，要么我必须自己做，因为我真的找不到可以为我定制的人。所以这是一个挑战。

Shimel: 对，听起来是这样。

威利斯:你知道，我很纠结的一件事，你知道，我有点喜欢委员会，讨厌委员会，对吧？因为就像我一样——hashi corp 有这个集群管理器，叫做 [Nomad](https://www.nomadproject.io/) ,我实际上已经看到人们有效地使用它，非常不费力，它有 80%的功能，但它永远不会有任何逃逸速度。它没有，也不会。

我担心我们的行业太专注于只有一种方法来进行集群管理，所以 Ravyn 的观点是，无论是 Red Hat 还是其他什么，似乎你甚至无法探索可能出现的容器化集群管理解决方案，因为我们行业的所有氧气现在都被 Kubernetes 消耗掉了。

**手册:**阿门。

对此有什么想法？我想就此谈一些想法。我的意思是这是一个梦/噩梦般的场景。对吗？我要它——让我们把它从 Kubernetes 上拿下来，让我们回到 PC 操作系统上。很棒的是，我们只能在 Windows 上开发，这样如果你是一个不称职的开发人员，你只需要担心在 Windows 上开发。你有一个操作系统，你可以在这个系统上开发你的应用程序，它可以工作，你可以用它获得 90%的市场份额。对于应用程序开发人员来说，这是一件多么美妙的事情。当然，它给了微软 Office 和他们所做的一切内幕。从安全的角度来看，这是一个多么大，多么肥，多么多汁的有效载荷，对，去攻击。

所以我们开始看到，只要我在里面，“这将是 Linux 桌面的一年。”对吗？我们听到这句话多久了？所以，你知道，然后当然 Mac 重新露面。

但这是我们争取的某种一致性。我们努力让 Kubernetes 成为标准，因为它是开源的，由一个基金会管理，我们需要一个标准。但接着我们又生气了，“嘿，我们不可能都符合同一个标准。我们想成为自己的独角兽。”这正是我们今天要讨论的。如果你追溯到早些时候，约翰，你把公司卖给了 Docker，在 Kubernetes 统治地位之前，对吗？有几个群集管理解决方案在竞争。对吗？那里有中间层和牧场主。

**威利斯:**中间层和 _____，对。[笑]

**Shimel:** 你记住了。是的，正是这些。所以，你知道，这是——但这是我们——你知道，引用海曼·罗斯在《教父 2》中的话，“这是我们选择生活的世界”，对吗？我们争取这些单一的标准，放之四海而皆准。也许这是一个巨大的错误。我不知道。也许这是一个错误。拉里，你怎么看？

是的，我确实看到了这个问题，John，你有点太专注于此了，有时事实上的标准并不是最好的技术选择。你们可以一直追溯到 Betamax 和 VHS 的对比，对于你们这些年龄足够大的人来说，应该还记得吧？VHS 胜出了，但 Betamax 被所有人认为是一种优越的技术。为什么？

你知道，所以我认为如果你要采取一种最佳的方法，你就必须——当你有一个像 Kubernetes 这样的真正事实上的标准时，你不必孤立于它之外，但当你打赌哪一个会胜出时——约翰在这方面非常擅长；约翰一直在谈论这件事。约翰不想把他的筹码放在那些不会长期存活的东西上，所以他想考虑什么会存活下来。

因此，为了对冲您的赌注，我认为您需要之前谈到的这个编排层。您需要在某种程度上将工具供应商与它的使用方式隔离开来，这样随着时间的推移，您就可以即插即用了。这就是我们在 Comcast 所做的，我们在安全工具的所有工具供应商之间建立了一个层，因为他们没有一个好的 unicorn 解决方案。无论如何，那里没有好的独角兽解决方案，即使我想。因此，我们在每个工具类别中都有不止一个供应商在内部竞争，有时我们有三个工具供应商。但是从开发人员的角度来看，他们很容易从一个切换到另一个，他们得到了相同的反馈渠道，相同的可视化，在所有这些不同的供应商之间以相同的方式聚合和评分。

我认为，当您拥有同类最佳的方法时，流程编排层真的很关键，而且我认为您必须自己构建它。我觉得你今天买不到。我真的认为你做不到。

威利斯:我会尽量快点闭嘴。我只想做个评论。我认为有两本书可以帮助我们了解我们的世界。一个是贾雷德·戴蒙德的《枪支、细菌和钢铁》,它实际上向你展示了为什么我们会陷入这些困境。如果你还没有读过，这是一本极好的书。然后从西蒙·西内克的《为什么》开始，这是一种反模式，我会说就像有集群一样——原子计算的东西，比如无服务器、功能或容器，将会存在 10 到 15 年。这些东西的集群将会存在 10 年。因此，如果你从这些方面考虑，而不是考虑 Kubernetes 和 Docker——Docker 已经在慢慢消亡，那么你就会开始思考为什么要隔离这些枪支、细菌和钢铁趋势。

**Bajpai:** 对。然后，我还想介绍另一个方面，即互联，但我认为公司可能会从扩展的角度来看待它。我们讨论了许多工具，以及如何在 DevOps 管道中校准这些工具。当然，当您有一个大型组织时，您有多个产品线，这些产品线将选择灵活，因此他们需要以他们选择的方式灵活地部署他们的 DevOps 管道。这就是 DevOps 的全部力量，对吗？

但我也认为，这次讨论中的对话将引导我们开始从治理的角度来看待我们的技术监督委员会，我们可以将这些点缝合起来，我们实际上可以奠定一个共同的基础，这是人们不需要一次又一次地倒回 _____ 所必需的。所以我认为这是关键。

当然，当我们谈论一个具有巨大能力的特定随机 _____ 时，它有优点也有缺点，对吗？因此，一个专业人士可能会认为他们可以相互加强新的能力。因此，当他们在一个产品中引入一个功能时，它是在相互强化另一个产品，这是他们带来的一个美丽的优势。但这也限制了我们超越供应商带来的东西的可能性。因此，我们基本上没有利用我们自己的创新周期来引入更多的能力，这些能力围绕着我们希望如何进行实验，我们希望如何在生命周期中构建创新的新功能。

这些都是值得考虑的因素，我真的相信技术监督委员会是大型组织中的一个亮点，当涉及到 DevOps 时，它会以一种更大的方式出现。

**Ashley:** 还有一点很有意思，当你想到技术市场上不同规模的公司时，你知道，Larry 提到了他在 Comcast 做的事情，或者他参与创建了一种架构，工具可以插入、拔出、替换等等。这听起来很简单，但我知道他们有一个架构可以做到这一点。一些组织有资金来创造这些东西。从数据中我们可以看到，在市场中，小型企业，也就是 200 人以下的公司，他们拥有非常优秀的高绩效团队，可以开发软件或建立自己的环境，为自己创建非常高效的设置、工具链等等。

然后在高端或大型企业，你知道，他们有很多可用的资源，他们可以潜在地利用这些资源来找出如何做这些事情。中端市场，中型公司通常是他们面临最大挑战的地方，他们希望做企业可以做的事情，但是他们没有资源。他们没有资金或全面的供应商关系来做所有这些事情，他们被期望以几乎企业级的水平交付，但是他们没有能够做到这一点的所有资源。这通常是某些人——在提供一套解决方案方面做得不错的非弗兰肯斯坦供应商——可以在这些情况下工作的地方。不是说他们不能在别人那里工作；他们也可以。

但取决于你在那种公司中的位置，公司的规模，你可以采取什么样的策略会有很大的不同。

我认为这是一个很好的观点，而且我最近五年的经历确实很有进取心。但在此之前，我与许多公司进行了交谈，你是对的，中型公司有时处于无人地带，他们需要一些标准化，需要一些一致性，但他们没有必要的资金将所有这些整合在一起。在这种情况下，供应商 unicorn 方法实际上可能更好。

嘿，伙计们，我想——Ravyn，我想让你待一会儿。约翰，你提到的第一本书的名字——我想把这些书放在笔记里的某个地方。

威利斯:哦，是的。很久以前我和乔什·科尔曼一起做过一个关于枪支、细菌和钢铁的演讲。无论如何，这是一本关于文明如何从某种程度上——你知道，他们如何从某种农业发展到这些集群的令人惊叹的书。如果你能看到树后的森林，你就能看到我们是如何进入的，像 Kubernetes 是我们唯一能使用的词。总之，贾雷德·戴蒙德，枪支，细菌，还有钢铁，真是不可思议。

Shimel: 好的，我们会试着把它放进去。Ravyn，你想说什么，我打断了你？

不，我不认为那是我。

**希梅尔:**加里玛？

**巴杰派:**是啊。我想实际上加强拉里所说的中型公司。这完全基于我在加拿大 DevOps 实践社区的经历和接触。我们看到越来越多的中型公司，不仅是咨询公司，还有希望构建 DevOps 功能的公司，来到实践社区，并开始引导关于工具评估的讨论。我也看到了冬天的一面。你知道，我们在这里具体谈论的是二级公司。winters 和 coming 在实践社区中展示了工具的功能，他们希望我们能得到一些支持和帮助来引导这场对话“这是一个好工具吗？在他们所处的环境中，这是一种好的能力吗？”

这是一个非常有趣的讨论，因为技术方面是故事的一个方面。我还想强调这样一个事实，我们问这些供应商和这些公司的问题是，“好的，你们有这个产品的产品负责人吗？”因为本质上，你知道，它的意思是问责制是如何在一个特定的工具视角下建立的。我还确保我们会询问他们有什么样的主题，比如他们有什么样的跨职能主题，这样我们就不会错过互操作性、集成、自动化等要点，所有这些都很重要。

所以我只想提一下，当我们被要求进行某种评估时，我们如何从实践社区的角度采取这种方法。

威利斯:你知道，我完全同意这些。我想到的一件事是，我有幸参与了这些不同的社区。就像我在艾伦的社区里一样，你知道，所以我通常会被艾伦的世界里发生的有趣的事情所吸引，这是一个相当大的世界。我已经深深地陷入了 Gene 的世界，你知道，DevOps 企业论坛/委员会。然后，你知道，我是 DevOps Days 的联合创始人和顾问之一。

我看到的一件事是真正的领导者。我不想把所有这些重量和重力放在你必须有一个伟大的领导者才能成功的身上，但就像我对人的看法一样，拉里是一个很好的例子。就像，你知道，你可以整天谈论康卡斯特做什么。我见过拉里的行动。好像这就是你想要的那种人。

Courtney Kissler 现在，你知道，曾在耐克工作，现在她去了一家创业公司。罗斯·克兰顿现在在美国航空公司，希瑟·米克曼。我的意思是，我可以在这个名单上继续下去，但这些人在更大的组织中影响变革，这是非常困难的。这就是其中的原因。

然而，大企业有一种免疫系统，这使得像我这样的人很难真正被雇佣并获得成功。你知道，颠覆性变革的想法并不是企业所追求的。所以，如果你有点像草根，你有点像草根，你有几个试点，这很容易；没有太多的阻力。当你获得足够的动力，有人觉得他们的领域受到威胁时，你就会在企业中遇到政治阻力。你知道，这真的很难克服。公司必须非常清楚这一点。康卡斯特过去在这方面为我做了很好的工作，但我认为这是企业免疫系统的本质。

阿什利:我们可能会把最后三条评论中的任何一条变成另一段对话。也许我们可以从生产部门的人那里得到一些帮助，让我们重新团结起来。

艾伦，你想结束吗？

有一件事是肯定的，那就是在这个问题上我们还有很多要谈的。我很乐意——我邀请大家回来继续对话。但是现在，Ravyn，我很感激你只用音频来解决这个问题。如果我们再做一次，我们会确保让视频工作。加里玛，很高兴你能来这里。你带了这么多。拉里和约翰，我能说什么呢，很高兴见到你们。我迫不及待地想见到你本人。我知道我们很多人都打过预防针。不会太久的。但是非常感谢你加了这么多。米切尔，干得好。

最重要的是，嘿，谢谢正在看这个节目的人们，因为这就是我们做这个节目的原因，让你们从中得到一些东西，加入到对话中来，让我们听到你们的想法。非常感谢 Tricentis 赞助 devo PS unbounded。

不过，下一次，我是 Alan Shimel，devo PS unbounded 的媒体运营。祝大家今天愉快。拜拜。

[End of Audio]