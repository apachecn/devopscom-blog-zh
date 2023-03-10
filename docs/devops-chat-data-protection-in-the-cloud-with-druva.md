# DevOps 聊天:使用 Druva 在云中保护数据

> 原文：<https://devops.com/devops-chat-data-protection-in-the-cloud-with-druva/>

任何首席信息官都知道，数据管理架构对于保护组织最有价值的资产之一:数据至关重要。数据管理听起来很简单，但事实并非如此。备份和恢复、灾难恢复、数据保留、治理和电子发现都是任何有效数据保护策略的组成部分。

随着企业在云中的迁移和发展，同样的功能也适用于这个非常动态和有弹性的环境。

最近，Druva 获得了由 Viking Global 领投的另一轮 1.3 亿美元投资。Druva 的首席采购官 Mike Palmer 参加了本期 DevOps Chat，我们将讨论 Druva 对这些资金的计划使用，以及 Druva 提供基于 SaaS 的数据保护平台的方法。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/660753635&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/660753635&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

米奇·阿什利:大家好。我是 DevOps.com 的米奇·阿什利，您正在收听的是另一个 DevOps 聊天播客。今天，德鲁瓦公司的首席产品官迈克·帕尔默和我在一起。我们今天的主题是随着您向云迁移，数据保护在您的未来会如何。迈克，欢迎来到 DevOps 聊天。

迈克·帕尔默:谢谢你，米奇。我一直期待着和你的这次谈话。

阿什莉:我也是。很高兴我们在一起在线讨论数据保护。首先，让我们介绍一下你自己，告诉我们你作为首席产品官做了些什么，并告诉我们一些关于 Druva 的事情。

帕尔默:嗯，如你所言，作为首席产品官，我的主要工作是管理产品。我负责公司的工程、定价和战略。Druva 是一个令人惊叹的组织，我大约一年前来到这里，来自行业的不同职位，观察存储和数据保护软件的发展，以及它在公共云采用的世界中是如何发展的。

Druva 是数据保护领域的第一家也是唯一一家 SaaS 公司，这让我非常感兴趣，因为当我们看企业以及他们如何采用 SaaS 时，无论是从 CRM 到 ERP 再到协作平台，数据保护都是 SaaS 采用的下一个大浪潮。因此，我们专注于这一领域并迅速发展。

阿什莉:你们做得很好。事实上，我知道一点旧闻，大约 30 天，但你有 1.3 亿美元的投资。我想维京环球为你引领了这一潮流——顺便祝贺你。太棒了。

帕尔默:非常感谢。我不认为 1.3 亿美元有任何过时之处。

**阿什利:** *【笑声】*

帕尔默:但这是对战略的一个很好的验证，维京公司是一个巨大的投资者。业内人士知道他们的起源可以追溯到几十年前，我们很高兴有他们加入。在讨论我们的业务和行业在未来 5 到 10 年内的发展时，他们是一个很好的合作伙伴，他们看到了我们所看到的，你知道，这是云和云存储采用的无情步伐。 企业希望找到简化其当前环境的方法，并将技术技能从数据保护等传统领域转移到更高级的领域或机器学习和分析等下一代领域，我们站在这些趋势的交叉点上，他们与我们站在一起，成为了很好的合作伙伴。

**Ashley:** 清晰的看到你美好的未来。让我们来谈谈——那么，这 1.3 亿英镑和你的其他投资，他们不是让你把它存在银行里，而是要你把它投入使用。那么，当你开始投资这些类型的基金时，Druva 的未来会是什么样的呢？

帕尔默:是的，这是一次很好的讨论，因为坦率地说，我们在几个不同的 _______ 展望方面展开了竞争。大家知道，第一个也是最基本的一个问题是，对于那些要管理的数据量不断增加、与数据相关的法规环境的风险和责任也不断增加的企业来说，我们如何实现最佳的总体拥有成本。我们如何为他们扩展应用和工作负载覆盖范围，因为他们不仅支持当前的应用，还支持他们在原生云中采用的应用？

然后，当我们稍微向前看时，正如一位投资者告诉我的，你知道，这要么是一项好投资，要么是一项伟大的投资，这将取决于我们如何将数据保护定义扩展到一个客户可以从复制和存储的数据中获得更多价值的定义。如果我们能够找到方法来帮助他们使用这些数据，并将其扩展到生态系统中，更好地了解这些数据，这不仅会有效地改变架构，而且会改变整个价值主张，这就是我们的目标。

**Ashley:** 现在，你在一个灵活的环境中运营 AWS，你知道，存储就在那里，你想要更多，你只需抓住它，使用它。我可以想象这是很容易失控的扩散。您需要一些数据管理功能，包括您现有的数据以及备份数据、还原、恢复的整个过程，确保您不会丢失信息—所有这些。

与传统的内部数据中心相比，在云环境中运行有哪些关键的不同之处？

帕尔默:问得好，首先让我给大家一些背景数据，来说明这个挑战有多大，机会有多大。你知道，我们牢记在心的是，如果你看一下亚马逊的云存储价格的五年 Kager，它是负 60%。

阿什莉:嗯。下去了。

**帕尔默:**在这样一个世界里，它正在走下坡路，如果你与亚马逊交谈，他们会说这是他们在未来五年将继续走的道路，足以挑战客户，“告诉我，当你今天购买一件电器时，明年或后年会便宜多少？”很可能是一样的，所以他们会失去行业创新，甚至是创造更好的价格和性能的能力。ESC 做了一项非常好的调查，询问数据中心的首席信息官，提高成本效率的五大机会是什么？列表中的第一项是存储管理。

阿什利:嗯。

**Palmer:** 您知道，企业正在处理这一漫长的历史，您之前也谈到过您作为 CIO 的历史。所有首席信息官都要应对存储供应商和硬件本身的几代人的激增、不兼容性，甚至是跟踪它的能力、严峻的挑战，以及第三个统计数据，这是我发现最有趣的一个，因为它表明转折点是在 2021 年，所以从现在起大约一年半后，我们将看到在云存储上花费的美元比场所存储更多的交叉点。因此，从存储的角度来看，这将是公司可以有效地被视为云的第一点，也是他们必须捍卫*【音频跳过】*的点。在这种情况下，你的第一个问题是，我们必须帮助他们做些什么——我们必须帮助他们实现节约的承诺。

你提出了一个很好的观点——它很容易失去控制，特别是当你有非常分散的团队，他们正在构建应用程序并以一种更加分散的方式利用基础设施的时候。我们必须帮助他们管理分层，我们必须帮助他们管理数据分类，我们不仅要帮助他们管理成本，还要为他们提供性能方面的建议。这其中很大一部分可以通过机器学习实现自动化。因此，我们将为他们提供一种新的模式，来替代 ILM、信息生命周期管理、HSM 或分层存储管理等旧术语，我们将把它们真正转变为后台自动化流程，让他们专注于重要的事情，即我是否有正确的策略，我是否可以将这些数据用于其他用途，我是否可以在没有特殊技能的情况下做到这一点？

**Ashley:** 嗯，你知道，你提出了一些非常好的观点，那就是，对于一家初创公司或作为年轻公司构建云原生应用程序的人来说，这是一回事，或者可能是一次性的应用程序。企业寻找能够消除迁移到云的风险的环境或事物。我会想象有一个至少是熟悉的结构，这样你不仅有数据保护和数据管理，而且还有治理之类的东西。你可以做一些取证，预测分析之类的事情。他们习惯于在内部部署的功能，但可能在云环境中，甚至可能在混合模式中。

帕尔默:我认为——是的，你说对了。我经常使用的一个词是融合。你知道，云的好处之一是，因为你有所有的基础，你有计算，你有存储、网络、政策和你周围的各种东西，像 Druva 这样的公司的工作，甚至企业开发人员的工作只是专注于应用程序逻辑。

正如您所提到的，在我们的领域中，这意味着您的数据中心有很多环境。在我以前的世界里，客户会购买备份产品、灾难恢复产品、电子发现产品、归档产品和数据分类产品。

阿什莉:去过那里，做过那个。[笑声]这些我都经历过。

**帕:**痛苦吧？你知道，你所看到的是你的成本上升，复杂性增加，不同的技能组合，你要参加的培训和会议，这些都在拖你的后腿，对吗？当你在单个平台中考虑 Druva 时，我们只是将电子发现或数据分类等辅助价值主张视为按需调用的应用程序。

阿什利:嗯。

**Palmer:** 因此，当您使用我们的产品进行备份时，您只需添加灾难恢复服务，只需添加数据分类即可。您有一个用于法律封存的工作流。顺便说一下，您可以按需购买，不必预付容量许可证，也不必预付存储费用。

阿什利:嗯。

**Palmer:** 因此，我们不仅会替换您当前的应用程序，而且当客户来找我们时，我们每隔一周发布一次新功能，他们可以将一些东西放在路线图上，并在几周或几个月内在他们现有的数据集上看到一个正常工作的应用程序，只有在他们使用时才付费。你知道，这对大多数首席信息官来说是革命性的。

**Ashley:** 通常你必须购买你认为是最大容量的存储量，并在使用时使用，然后可能升级，当然，在云中，它是弹性的，是可替换的。我们可以改变，根据需要添加更多。

帕尔默:当然，你必须对你的软件许可证做同样的事情，然后你必须整合这些产品，你必须在你的搭配设施中找到空间。你知道，当你真正分析采用一个新的软件或硬件需要多少成本和努力时，这远远超出了显而易见的范围。

顺便提一下，这是我向很多人引用的一个数据。根据我的经验，当一个软件供应商发布一个产品的新版本时，可能需要 12 到 18 个月，甚至一半的客户群才会采用这个版本。因此，如果敏捷性和速度对于采用能力的企业来说很重要，那么在获得能力之前，你必须承担风险并等待很长时间，而在 SaaS，你可以毫不费力地按需获得能力，这再次完全改变了模式。

阿什利:我之前提到了混合动力，这是我们还没有谈到的东西。大多数企业无法将所有东西都搬到云中。事实上，他们可能不愿意。他们可能希望保留一些混合云或本地云。这是一个你可以轻易与他们沟通的领域吗？

帕尔默:是的，谢谢你的提问，因为在你的领域独一无二的困难之一就是首先解释你的模型。从 SaaS 的角度来看，虽然我们的应用架构是云原生的，但我们在客户的场所数据中心和公共云中为客户提供服务，包括他们的 SaaS 提供商。

这意味着，正如您所说，如果您有一个客户，并且大多数属于这一类别，他们有一个数据中心，其中的工作负载恢复时间非常好，为了利用我前面提到的云中的所有优势，我们帮助他们将工作负载迁移到云中，并为他们管理和恢复本地设施。但是，如果有一个应用程序具有 RPO 或恢复点或恢复时间目标，要求它位于数据中心内，我们也可以为他们提供一个虚拟设备来解决这些问题。

然后，当他们构建原生云应用程序，例如 Amazon、AWS，或者他们采用 Office 365 或 Salesforce 时，我们还会帮助进行数据保护和分类，既包括在 Amazon 中进行，也包括与 SaaS 提供商一起进行。因此，我们确实是在他们当前的体系结构中。我们也支持他们的未来架构。

阿什莉:是的，我认为这是转变的关键。同样，我之前提到过消除风险，其中一部分是熟悉度，以及给我一条去我想去的地方的路径，我可能不会完全去云，对吗？正如您所提到的，由于本地的 RTO 或 RPO 要求，我可能总是需要一些东西。

**帕:**没错。

**Ashley:** 请告诉我们一些产品自带的功能，你知道，开始使用 Druva 需要什么？我是否可以像 Amazon 一样，只需支付信用卡，就可以获得所有信息，或者是否有一套规划流程有助于正确构建这样的数据保护架构？

**Palmer:** 哦，我们喜欢这个问题，因为在这个行业中，进行概念验证是一个非常复杂的过程，包括管理规则、软件安装以及寻找硬件和磁盘容量。有了 Druva，你就可以在在线平台上注册了。我们让您可以访问您正在寻找的代理类型，所以让我们以 VMware 为例。您可以下载一个代理，向它提供您的凭据，输入一个策略，在大约 10 到 15 分钟内完成所有这一切，然后您就可以启动您的第一次备份了。

您可以做到这一点，而且我们已经反复测试了这一点，而无需具备专业的备份管理员技能，这意味着您也可以开始向应用程序团队委派权限，这样您作为管理员就有能力实施和创建总体策略。因此，现在你有了一个世界，你最平凡的日常任务变得如此简单，你可以将它们委托给你的客户，从 IT 提供商的角度来看，这增加了他们的满意度，因为他们可以按需做这些事情，他们可以腾出你的时间来做更重要的事情。

阿什莉:太棒了。当我问那个问题时，我出了一身冷汗。在多家公司完成了这一工作后，将不同的产品整合在一起并不是一个有趣的过程，而且确实需要进行适当的设计，因为您必须担心如何监控合规性之类的问题。你提到了电子发现。现在，我们有了 GDPR 合规性以及我们自己关于数据保留的内部流程，并确保我们能够保护自己免受勒索软件之类的攻击。

**Palmer:** 我们与世界上一些最大的公司打交道，我们非常了解的一个特定使用案例是在终端方面，客户要么要处理法律案件，要么担心终端用户的行为以及他们对数据的处理。因此，我们不仅为他们提供保护设备的能力，而且我们还为他们提供关于数据情况的想法，当然还有您提到的工作流，将数据拉到一边或在他们需要的地方暂停—同样，这只是一个界面中的工作流。它不是试图让一个产品与另一个产品一起工作，或者确保版本升级或兼容或修补充分。我们会处理好所有的事情。

阿什利:嗯。我在这里就像剥洋葱一样，记住了您必须用数据管理方法解决的问题，您知道，您必须处理这些问题—您之前提到过分层存储。去杜平在云环境中适用吗？缓存在云环境中适用吗？这些也是你要解决的吗？

**帕:**以上皆有。所以，你之前问了一个很好的问题。如果我是采用云的客户，我的一些风险领域或事情在哪里没有提供给我？其中一个例子就是重复数据消除。因此，如果我要采用 S3 或者将数据移动到 Glacier，我将如何高效地做到这一点呢？在这样一个世界中，我可能会从本地的重复数据消除位置开始，我将在云中丢失这些数据。

借助 Druva，我们可以为您消除重复数据，从而最大限度地减少您的云存储空间。一旦我们做到这一点，我们还会考虑分层，无论是 S3IA、Glacier 还是 Glacier Deep Archive，我们不仅会取代您的 HSM 战略，而且正如我前面所说，我们会以自动化的方式完成这一工作。

阿什利:嗯。同样好的是，我又一次有了负面的回忆。旧流程是第一层，您的第一层存储会有多少内存存储，在此速度下会有多少，在第三层速度下会有多少。亚马逊提供了不同的服务，这就是你在一个完整的数据管理架构中收集的内容，当然，你可以根据需要动态分配这些内容，但这就是你绑定的服务以及你提供的内容。

**Palmer:** 在云和 SaaS 世界中，容量规划不是问题。当然，我们将与您合作，正如您之前提到的，在您知道该使用情形不适用于远程数据中心的现场，您有 RPO 和 RTO。我们将通过虚拟设备与您合作。我们也有客户总是想要陆地速度恢复，但是他们越来越多地配置在像 Equinix 这样的地方，例如，他们可以交叉连接到云提供商。

因此，即使您有看起来像数据中心要求的要求，这几乎就像您的数据中心正在迁移到某些搭配设施中的云中，即使没有虚拟设备，您也可以利用 SaaS。

**Ashley:** 您认为您为客户解决的最大难题是什么？显然，他们有需求、功能、能力——诸如此类的东西。但是当有人来敲你的网站说，“我想我需要这个”，他们最常试图解决的最大问题是什么？

**帕:**有两个问题，但引人注目的事件不同。所以，我们为他们解决的两个问题是成本。他们展望未来，意识到他们的成本在上升，而不是下降，云可以帮助解决这个问题。

第二个是复杂性。他们不希望雇用更多的存储管理员或备份管理员，跟踪不同的供应商。他们不必进行硬件更新。他们不想要孤立的系统。这些问题都可以通过 SaaS 提供的 Druva 和公共云解决。所以，这些是核心问题。

另一方面，引人注目的事件可能非常不同。我们的财富 100 强公司在世界各地都有数据中心，他们的云之旅可能包括今天将卫星设施迁移到云，明天越来越多地关注云和核心数据中心。因此，他们有更多的数据中心迁移整合使用案例。

我们还有其他拥有远程办公室或现场设施的公司，他们支持设备的成本很高，甚至是不可能的，因为他们没有员工。因此，第二个是更新和将设备带出设施。

**阿什利:**嗯哼，嗯哼。

**Palmer:** 我们的客户因为勒索软件而来到我们这里，我们提供了一个空气间隙解决方案，在这里唯一的替代方案是磁带。因此，我们通过加密为他们提供了同样的安全性，并为他们的主网络提供了一个无人能及的“空挡”解决方案。因此，他们采用了具有磁带安全性的云。

当然，还有备份和灾难恢复的基本使用案例，在这种情况下，客户不仅希望能够恢复数据，还希望能够移动应用程序，拥有完整的流程编排能力，并在不增加拥有自己的体系结构甚至管理自己的云集成的成本的情况下进行实例化。

因此，我们在平台中集成了灾难恢复功能。因此，客户来了，他们获得了本机备份，他们获得了本机灾难恢复，所有这些都在一个界面中，无需其他产品或其他培训。因此，我们有引人注目的事件，我们在客户现有传统体系结构的基础上为他们节省了 50%的成本，我们已经通过外部专家以及客户自身和复杂性证明了这一点，并真正利用所有传统的普通任务和技能，让它们过时。

阿什莉:嗯，迈克，感谢你的加入。我们没时间了。我想我们可以再谈一个小时的数据管理*【笑声】* —

**帕:** *【笑声】*肯定。

阿什莉:——也分享一些一路上的战争故事。所以，我要感谢您，Mike——dru va 的首席产品官 Mike Palmer 加入我们。

帕尔默:米奇，非常感谢你。和你聊天很愉快。也许我们会再做一次。

阿什莉:那太好了。随着事情的进展，我们很乐意听到更新，你会花掉一些钱。*【笑声】*当然，我要感谢你——我们的听众——参加我们今天的节目。我是 DevOps.com[的米奇·阿什利](https://devops.com/)，你已经听到了另一个 DevOps 聊天播客。在外面要小心。

— [米切尔·阿什利](https://devops.com/author/mitchellashley/)