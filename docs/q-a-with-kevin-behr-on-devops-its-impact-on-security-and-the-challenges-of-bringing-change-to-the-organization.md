# Kevin Behr 就 DevOps、其对安全性的影响以及为组织带来变革的挑战进行了问答

> 原文：<https://devops.com/q-a-with-kevin-behr-on-devops-its-impact-on-security-and-the-challenges-of-bringing-change-to-the-organization/>

Kevin Behr 从事 IT 行业已有 26 年，是 7 本 IT 管理书籍的作者，包括畅销书《可见运营手册》(他与 Gene Kim 和 George Spafford 合著)和由惠普公司出版的《IT 管理权威指南》。他最近的一本书《凤凰计划》(Phoenix Project)也是与 Kim 和 Spafford 合著的，这本书帮助在全球范围内引发了关于 DevOps 的讨论。Behr 还因其为国家科学院、惠普、SANS 研究所、AFCOM 和 IT 服务管理论坛等组织所做的技术和管理主题演讲而闻名。

Behr 还是信息技术过程研究所(ITPI)的创始人，也是 Praxisflow(以前的 Assemblage Pointe)的 CXO 和董事会咨询实践的首席科学官，在 praxis flow，Behr 就如何提高业务效率和竞争优势为 IT 组织和高管提供咨询、指导和训练。

我们采访了 Kevin Behr，讨论了 DevOps、其对安全性的影响以及为组织带来变革的挑战。

**Devops.com:我们现在听到很多关于持续部署的说法，但是与传统的企业部署相比，这意味着什么呢？这对安全等 it 领域意味着什么？**
**Behr:** 通过持续监控，您可以快速捕捉故障，即使导致故障的问题使其进入生产状态。有了今天的 SaaS 和云模型，失败不再那么重要，因为你不是在运输软件，而是在管理服务。一个补丁可以立即适用于所有用户。

这是传统企业 IT 思维和围绕持续部署的思维之间的区别，持续部署真的开始蔓延到企业中。新的想法是:我们如何做到这一点更小，更快，更安全地失败。组织还没有准备好让所有事情都不会发生故障，但是朝着这个方向发展就成了一种实际的安全策略，而不是让我们看看会发生什么。

这就是我们在持续部署中遇到的情况。您实际上已经使部署安全失败。你几乎不需要太多的测试，因为你可以实际部署，然后等待打开一个新的功能；如果它不起作用，你可以关闭该功能。我们开始看到的是这种单选按钮式的部署:他们将部署软件，软件将逐步打开，而不是老派的大爆炸。

仔细想想，这真的很棒。软件越来越像基础设施。你经常听到这句话:代码是基础设施，基础设施是代码。你会发现到处都有不同的含义。我认为这是对的。我认为安全实践必须是安全到失败方法的一部分。你需要非常好的监控和检测控制，因为它们将帮助你更有弹性。

DevOps.com:我认为，当与一些安全和 IT 专业人员以及其他习惯于控制流程的人合作时，这些概念可能会面临挑战。对于组织自我监督和保护的需求与持续部署的优势之间的平衡，您有什么看法？
**贝尔:**你可能会担心安全从业者和其他人可能会破坏他们已经实施的控制。他们意识到，这实际上可以增加更大的弹性—考虑对某些事情的持续授权、跨职能团队、持续监控，以及所有这些很可能增加弹性的事情。

如果安全部门能够支持 DevOps，您将会看到更多的成功，从这样的角度来看，“哦，天哪，这太棒了，那么我们必须做什么才能让 DevOps 发挥作用呢？而不是“这就是它不能工作的原因。“像这样设置路障的安全小组现在就要被打败了。

但并不是所有地方都是好消息。我讨厌说有些公司比其他公司更愚蠢。我看到一些地方用开发计划作为借口来为他们计划的所有裁员开脱:“我们需要解雇五个人，因为我们正在做开发计划。”这有什么意义？我认为在一些组织中会出现微小的反弹。其中之一将是组织称之为 DevOps 的东西，仅仅因为它服务于他们的想法。

例如，我去过几家创建了 DevOps 部门的银行，这是对整个运动的亵渎，因为整个想法是消除孤岛，而不是创建新的孤岛。

有时我会被组织称之为 DevOps 的想法所困扰，但有时我不会，因为这只是一个想法成功的结果。

DevOps.com:你认为企业会采取哪些措施来应对这种变化？你是否在一些人能适应变化的组织中看到了分裂？
**贝尔:**我认为，拥有他们工作的这些系统的人还有很长的路要走。我认为那些和 DevOps 过不去的人现在正在被打压。担任运营副总裁或运营总监的人:他们可能不喜欢 DevOps 的概念，因为这对他们来说是跨职能的挑战。第一个是:“所有这些不向我汇报的人现在都在我的数据中心。他们在做什么？为什么它们在键盘上？我怎么控制这个？”[故事]

想想吧。他们的整个工作角色是根据可靠性的概念来判断的。他们的试探法告诉他们，从长远来看，让许多不负责任的人做事与可靠性不一致。在 DevOps 取得成功的商店里，保安人员可以进来说:这太棒了。他们喜欢缩短周期时间。他们喜欢开发人员下来帮助打补丁。在他们需要的时候把事情做好。他们现在知道这些东西意味着什么了。这意味着他们的安全反馈直接反馈到 dev。

我想这是人们不明白的另一件事。开发运维如果做得好，会产生并行反馈环路，而不仅仅是串行反馈环路。在过去的方式中，有人要求某人做某事，他们做了，然后供应商问他们喜欢这项服务吗？这是当今大多数操作都有的反馈回路。但是，当开发人员加入进来时，突然之间，开发人员就增加了另一个反馈环。就像这样，“嘿，我只是看着你做这个我不是每天都做的事情。伙计，那是很多额外的步骤。你为什么这样做？”

这是一个反馈循环，来自于教某人一些新的东西，并从外界获得反馈。然后是你所交付的质量的反馈环。当你同时得到这两者时，平行反馈循环就是进化的方式。这是所有进化系统和适应系统的标志之一。

如果安全可以成为那些平行反馈循环中的一个，当它发生时，所有关于你正在做什么的文档，以及所有相关的东西都在一个地方，那么安全就成为重构的一部分。

我认为另一件事是，因为开发人员和运营人员的合作越来越多，你开始听到更多的开发人员发生的情况。他们会说这样的话，“我一直想知道，每当我硬编码 IP 地址时，他们为什么对我大喊大叫。现在我明白了:因为你们必须一直改变这些，因为我们现在正在这里改变其中的一些。”这种语境化的理解大有帮助。

这是一件大事。因为有大量的信息安全操作:修补、日志解析以及发生在操作级别的各种事情，这些都是真正由安全驱动的。如果你能让开发人员参与其中，帮助解决一些问题，他们就会开始理解你为什么要这么做。在许多情况下，我们花了很多钱在技术和安全上，这只是为了防止开发人员做我们认为我们无法改变的事情。

明白这一点并培养这一点的组织将会取得成功。