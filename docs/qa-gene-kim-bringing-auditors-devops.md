# Gene Kim 的问答:将审计员带到 DevOps

> 原文：<https://devops.com/qa-gene-kim-bringing-auditors-devops/>

随着越来越多的企业采用 DevOps，在 DevOps 团队拥有的控制和审计员认为需要的 IT 控制之间经常会产生组织脱节。如果正确的控制确实到位，那么绝对需要与审计团队进行沟通。弥合这些差距对于 IT 团队和审计人员来说都是痛苦的。

帮助企业更好地了解审计人员需要他们做什么是 DevOps 审计防御工具包的首要目标，其目的是“在 DevOps 实践到位的情况下，定义管理层和审计人员应如何进行审计的权威指导”，根据该努力的主页。“通过这样做，DevOps 审计防御工具包将提升管理实践的状态，定义如何理解业务目标的风险，正确界定和证实控制的有效性，从而降低审计成本并提高审计的有效性。”

本月早些时候发布了 DevOps 审计防御工具包的审查草案，以供审查和评论。作者[詹姆斯·德鲁西亚](https://www.linkedin.com/profile/view?id=4608109&authType=OUT_OF_NETWORK&authToken=wZu8&locale=en_US&trk=tyah2&trkInfo=tarId%3A1403280377654%2Ctas%3AJames Del%2Cidx%3A1-1-1)、[杰夫·加利莫尔](https://www.linkedin.com/profile/view?id=2742080&authType=name&authToken=2oL4&trk=prof-proj-cc-name)、[吉恩·金](https://www.linkedin.com/profile/view?id=14159909&authType=OUT_OF_NETWORK&authToken=-Get&locale=en_US&trk=tyah2&trkInfo=tarId%3A1403280601850%2Ctas%3AGene%2Cidx%3A2-1-2)和[拜伦·米勒](https://www.linkedin.com/profile/view?id=2954514&authType=name&authToken=1uEy&trk=prof-proj-cc-name)预计最终版本将在未来几个月内面世。

为了更深入地了解这个工具包，我们花了几分钟时间采访了凤凰计划的作者 Gene Kim。

为什么你认为像 DevOps 审计防御工具包这样的东西是必要的？我认为 DevOps 的核心是变革性的。这是通过 DevOps 价值流增加工作流量的方法。DevOps 提高了可靠性、稳定性和安全性。这也有助于组织在市场中取胜。

然而，当组织真正开始这一旅程时，他们遇到的最大障碍可能是他们的“法规遵从性人员永远不会让我们这样做。”

我认为这是有一定道理的。由于在您开始 DevOps 之旅时提出了如此多的建议，您实际上取消了传统 IT 组织使用的一些关键控制，如职责分离，如变更批准流程。

因此，当他们听到“嘿，我将让我们的开发人员随时部署，而不需要从变更顾问委员会获得变更批准令”时，审计员、合规经理和安全人员通常会抓狂。

你有亲眼目睹这一切的经验，对吗？这就是为什么我认为这是一项非常重要的工作。我与人们交谈得越多，我就听到越多关于试图以这种方式前进的组织中的审计团队和审计组之间的摩擦。

你如何看待 DevOps 审计防御工具包实现这一点？

DevOps 审计防御工具包旨在培训。既然不能带 DevOps 给审计员，那就必须带审计员来 DevOps。我的意思是我们的目标是训练 DevOps 的从业者如何像一个审计员一样思考，并且在检查一个过程和系统的时候实际上走一遍审计员会做什么。这是从自上而下的风险评估的最高级别开始到细节，就像审计员会检查列表，询问什么可能出错。

DevOps Audit Defense Toolkit 展示了企业如何拥有可以防止坏事发生的环境，如果我们无法防止，我们可以检测并纠正它。然后，它显示了我们如何证明它。我认为通过做所有这些，一个人正在做检查 DevOps 组织的最好的审计员自己做的事情。

通过培训 DevOps 组织中的人像审计员一样思考，我们实际上可以把审计员带在身边，展示我们的工作，将点点滴滴联系起来，并有希望让审计员成为 DevOps 最好的朋友。

所以，这是在训练 IT 如何像审计员一样思考，并以审计员的方式看待系统和流程？

在很多方面，是的。这是一种结构化的思维过程，任何世界级的审计师都会这样做，以实际创建审计计划，然后审计实地工作。

该工具包提出了类似这样的问题:为什么要对其进行审计？描述环境通过代码如何转移到生产的过程，以及开发环境的来源。它还问:你如何防止开发人员将后门代码引入生产；我们如何确保未经测试的代码不会进入生产环境？

我从与其他团队成员的合作中学到了很多，展示了我们如何有理由说我们知道自己在做什么，以及我们真的在思考如何建立一个有效的控制环境。

这从某种程度上来说是老生常谈，并声称这是我们对代码进行同行评审的方式。我们确保所有部署都被放入构建系统中。我们运行所有的自动化测试。每当有人提交代码时，我们都会在它进入阶段环境之前运行所有的安全测试。我们可以确认部署的东西确实通过了所有测试。

当我们写下并展示我们的作品时，我们的交流最有效。我们揭露了一个审计员所需要的一切，这样他就可以看着它说，“你知道吗？这实际上比我最好的审计师在这个领域做的还要好，你知道你在做什么。”

我可以想象，简单地学习审计人员的语言和他们说话的方式本身就非常有价值。

是的，我们现在使用一种审计员之间使用的语言。我认为，即使只是揭示这种语言的样子，也有助于把我们自己的点连接起来，以便能够说，“哦，我知道为什么它被这样表述了。大量的价值，仅仅通过提供这些。

在创建 DevOps 审计防御工具包的过程中，你学到了什么让你惊讶的东西吗？有趣的是，我从这项工作中学到了很多。你可能认为参与编写凤凰计划的人会知道这看起来像什么？但是，当我看到什么是实际的业务流、受监管的数据可能驻留在哪里，以及法规遵从性领域范围内具体有哪些应用程序时，我学到了很多东西。

第二件事是通过管理风险分析——通过结构化的思考过程，了解一家公司如何真正做到尽职调查，决定其最大的业务风险是什么，以及它是否真的有一个可以预防、检测和纠正的控制环境。

当然，我们都知道 DevOps 让一切变得更好，但我们需要知道为什么以及如何证明这一点，你用什么标准让开发者负责？您谈到了同行评审，但是这在哪里记录呢？标准是什么？是如何执行的？

你想要遵从，这很重要。但是你也不希望人家插后门。您不希望在部署变更时系统崩溃。所以你真的需要说出所有的点，把它们连接起来，然后对其进行处理。我在这个项目中学到了很多。