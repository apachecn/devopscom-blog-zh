# 自动化时代的测试和认证

> 原文：<https://devops.com/testing-certification-age-automation/>

> 如果我们不改变我们的教学方式，30 年后我们会陷入困境。因为我们的教学方式，我们教给孩子的东西都是过去 200 年的东西。它是基于知识的。而且，我们不能教孩子与机器竞争，他们(机器)更聪明。
> 
> 我们必须教一些独特的东西，这样机器就永远赶不上我们了。
> 
> — [阿里巴巴首席执行官马云](https://www.youtube.com/watch?v=pahnlwG0_18)

| **tl;dr synopsis**鉴于现代 DevOps 的复杂性，技术认证变得更加精细。此外，作为就业的一个要求，它的使用正在爆炸式增长。大多数技术认证是通过由多项选择题组成的测试来授予的。通过多项选择题考试要求考生在短时间内吸收大量知识。这种获得的知识不需要保留。因此，认证只能证明持证人在测试时对某项技术的了解。而且，从本质上来说，该测试只衡量持证人参加认证考试的能力。最后，通过多项选择进行测试并不能确保认证持有人在所需经验或更高层次的思考能力方面的资格。在当前的商业环境中，技术认证很有价值。然而，在某种程度上，随着机器智能能够执行更多目前由人类完成的活动，认证测试的形式和方法需要改变。未来的认证测试方法将需要更加强调分析和创造性解决问题，而不是目前的知识获取和死记硬背。此外，我们教人类的内容和方式需要是独特的，超越人工智能的能力。 |

在过去的 10 年里，DevOps 已经成为一个更加复杂的景观。无论选择哪家服务提供商——亚马逊网络服务、微软 Azure、谷歌云、OpenStack、IBM、Joe 的本土云服务——你都必须知道很多东西。

从高层次来看，服务提供商提供的产品惊人地相似。例如，它们都提供某种机器虚拟化、存储服务、数据库服务、排队技术、授权服务、供应技术和 API 管理。但是你操作概念旋钮和开关来让这些产品工作的方式在不同的提供商之间会有很大的不同。这涉及到许多细枝末节。吸收供应商产品系列中生产所需的大量细节需要时间。而且，确保某人能够真正胜任地使用服务提供商的产品是一件冒险的事情。例如，部署工程师可能理解动态预配置背后的概念，但是让 Kubernetes 编排在 Google Cloud 中工作是一个难题。做总是困难得多。正如我所说的，这涉及到很多细节。

那么，公司如何确保他们雇佣来摆弄他们价值数百万美元的任务关键型技术堆栈的人能够交付产品而不会搞砸呢？大多数都有一个广泛的技术面试过程，伴随着严格的背景调查。有些只是希望。其他的需要认证。

# 微认证的兴起

证明一个人拥有胜任某项职业所需的技能和经验的概念，即使不是在此之前，也是从 1885 年就已经存在了。那一年，马萨诸塞州实施了第一次书面律师考试。在那之前，一个人做律师所需要的只是从法院拿到一张纸条，上面写着这个人可以成为一名律师。亚伯·林肯就是这样。最终这个职业成熟了。专业资格是通过基于测试的方法确定的。早期的律师考试使用论述题。1972 年，随着多州律师考试的增加，[选择题](https://magoosh.com/bar-exam/4-mbe-sample-questions/)被包括在内。

去做选择题看似微不足道的改变，其实不然。尽管一个知识渊博的专业人士需要对一个论文问题评分，但是任何人都可以用答案来评估多选题答案。因此， [SAT](https://www.princetonreview.com/college/sat-information) 中的选择题很受欢迎。这是给每年数百万的高中考生打分的最有效的方法。评估又快又便宜，一台机器就能完成。

正如我在本文开始时提到的，IT，尤其是 DevOps，已经成为一个越来越细粒度复杂的地方。这个领域有很多技术。这些技术中的每一项都有一个重要的学习曲线需要克服才能达到精通。传统观点认为，确定掌握程度的最佳方法是测试一个人对给定技术的知识，然后衡量测试的结果——高分，好；分数低，不好。与早期的测试实践一样，最快、最便宜的评估方法是进行一次由多项选择答案组成的测试。这有点像 sat，除了大多数技术认证是针对特定供应商的产品线，而不是一般的知识体系。(你可以在这里查看作为 DevOps 工程师专业人员的 AWS 认证的测试样本[)。](https://d0.awsstatic.com/training-and-certification/docs/AWS_certified_DevOps_Engineer_Professional_SampleExam.pdf)

这种类型的专业测试范式正在爆炸。它正在渗透科技领域的每一个角落。此外，越来越多的雇主要求将认证作为雇佣条件，无论是对未来的员工还是已经在职的员工。这是可以的，除了一件事:在你刮去所有关于基于测试的认证的价值的先入之见和假设之后，当它归结到测试测量的基本有效性时，测试真正测量的唯一事情是参加测试的能力。例如，一名部署工程师可能在系统故障后通宵工作以使公司重新上线，然后参加认证测试。筋疲力尽的接受者以悲惨的失败告终。然而，一些刚从高中毕业、从未见过数据中心内部的懒鬼可以使用偷来的答案参加考试，并顺利通过考试。请告诉我:谁才是真正最有资格的专业人士？

# 回流测试

认证不是问题。毕竟，当我知道将要打开我的手腕来缓解我的腕管综合症的外科医生得到了美国外科委员会的认证时，我真的感觉更舒服了。相反，问题在于认证测试的进行方式。在我看来，强调多项选择问答形式的认证测试过程是有缺陷的。即使问题回答正确，考试形式也不能真正验证应试者的能力，只能证明一些事实是已知的。只是通过反流来测试。

这种测试要求应试者吸收大量知识，然后根据手头的测试要求将其倒掉。不能保证长期保留。这是为考试而死记硬背的古老过程。一旦“时间到了！”铃声响起，考生很可能会忘记她所学的大部分内容。那些记忆力超强的人可能会记得所有的事情，但是对于我们大多数普通人来说，这只是一次性的事情。

在技术领域，很少有人使用死记硬背的方法工作。我们大多数人只是在需要的时候，使用这个叫做互联网的东西来获得我们需要的答案。这就是比尔·盖茨所说的“触手可及的信息”然而，此刻我们仍然在测试你头脑中的知识。

有更好的方法。

# 更好的方法

认证是好的，只要它确保持有者知道他或她在做什么。当认证仅仅是在在线测试中勾选正确的复选框时，就有问题了。把一只猴子永远放在多项选择测试前，最终这只猴子会得 100 分。

那我们该怎么办？我们执行以下操作:

## 支持开卷测试

如果测试的目的是确保一个人在参加测试时掌握一定的知识，那么在测试时提供所需的知识。这叫做开卷测试。现实生活就是这样。例如，您需要一个 NodeJS 包来提供模拟对象。你是否依赖于你现有的关于你所知道的软件包的知识？太好了，但是如果你不知道呢？工作会嘎然而止吗？不。你去 NPM 找一个符合你需要的。现实生活就是这样。一个称职的专业人员应该对他或她的专业领域有一个基本的、高水平的了解。对于日常细节，专业人士有能力快速找到问题的准确答案。

与其有一个基于填鸭式的认证测试过程，也许我们应该吃我们在现实生活中制作的狗粮，去开卷。当你需要的时候，研究你需要什么没有什么坏处。此外，一周前的测试问题可能最好由今天的新技术来回答。

## 把重点放在文章问题上

测试的实际机制因被测试的认知水平而异。几年前我写了一篇关于这个的文章。测试高阶思维——分析、综合、评估——的最佳方式是使用问答题。毕竟，如果不是一个非常大的论文问题，博士论文是什么？论文需要一定程度的思考，这是用低层次的测试方法如多项选择很难捕捉到的。作文不仅揭示了考生的想法*，也揭示了考生的想法*。你的高中数学老师希望你在参加代数考试时展示你的作品是有原因的。有时候你如何得到答案和答案本身一样有价值。**

**一个好的认证考试将提供一个问题格式，允许考生说明他们的想法以及他们得出答案的方式。因此，有必要偏向于论述题。还是那句话，你怎么想和你怎么想一样重要。**

## **把一个人放回检查过程中**

**跟你分享一个亲密的事:我不太会回答选择题。当遇到一个问题时，我会花很多时间试图弄清楚这个问题到底在问什么。你会对那些模糊不清、令人困惑的试题数量感到惊讶。**

**这对我来说是一个真正的问题，当我要去大学跳 SAT 舞蹈的时候。幸运的是，我的母校更关注我的论文，而不是我的 SAT 分数。此外，我大学期间的很多考试都是以论文的形式进行的，或者是以采访教授的形式进行的。后来，当轮到我来打分的时候，我的过程是通过采访学生来评估他们所做的一个或多个项目。我根据项目本身的质量和对工作的思考给自己打分。我通过与学生交谈和检查他们的作业来测试他们。我喜欢认为我对一个人的能力有相当准确的了解，比多项选择测试所能提供的还要多。**

**在考试过程中提供人际互动的机会，对于提供准确评估个人能力所需的信息大有帮助。**

## **要求证明候选人的经验、品格和能力**

**想一想:有可能成为一名 AWS 认证的专业解决方案架构师，而没有做过一天有报酬的实际工作。你所需要做的就是[通过认证考试](https://aws.amazon.com/certification/faqs/)。是的，通过考试当然有意义。这是一次严峻的考验。至少，该测试可能会证明应该能够使用给定 AWS 服务的概念转盘和开关。但是，就拥有在任务关键型企业中扮演关键路径角色的实际经验、能力和性格而言，还需要一些其他的认证工具。这个工具有时被称为参考——或者，正如《绿野仙踪》中巫师对铁皮人说的，[一个证明](https://www.youtube.com/watch?v=RUvrtAUscR4)。**

**正如你在上面读到的，在亚伯·林肯的时代，一封来自法庭的证明持有人良好道德品质的信是执业律师所需要的。你可以把良好的道德品质理解为准时出现、做可靠的工作、展现追求卓越的决心以及与他人友好相处的能力。这样的描述可能听起来很夸张，但它是有价值的。**

**诚然，一些证书要求持证人除了良好的考试成绩外，还要有现代版的“良好的道德品质”，但许多证书并不要求，尤其是在科技领域。雇主希望雇佣那些知道自己在做什么，并且有能力在组织中有效工作的人。潜在的候选人希望提供证据，证明他们具备成为一名优秀员工的素质。将持证人的经验、性格和能力的证明纳入技术认证，将为所有相关人员增加巨大的价值。此外，证明需要肯定持证人适应变化的能力。在不太遥远的将来，你的商业价值将不是你今天知道什么，而是你能以多快的速度使用明天将出现的技术。**

# **如何赢得比赛**

**不管是好是坏，我们都在和机器赛跑来保住我们的工作。他们不是真的想要我们的工作。他们没有欲望。但是，这并不是说，如果机器证明能够胜任，他们就不能做我们的工作。可悲的是，目前技术认证的实践集中于通过与知识获取相关的测试。**

**现在，我们正在赢得这场比赛。[机器在涉及高级图像识别和阅读理解的基于知识的任务方面仍然存在问题](https://www.wired.com/story/ai-beat-humans-at-reading-maybe-not/)。我们仍然比机器更知道如何区分狗、猫和苹果树。**

**但是，事情不会总是这样。请记住，20 年前，会说话的机器非常原始。他们的声音有一种人工的、不连贯的节奏，明显像机器人一样。今天，当一个机器人电话打扰你的晚餐时，很难区分人和机器。机器能够比任何人类更好地完成中高级知识型工作只是时间问题。马云在本文开头的引述支持了这一论断。**

**我们需要改变。我们未来带给工作场所的商业价值将是分析、综合和评估。机器将能够比我们更快更准确地进行低级思维。人类卓越的领域将是更好地理解我们周围的世界，并将新事物带入这个世界。我们开始的方式是教授一些如此独特的东西，以至于机器永远也赶不上。这个东西就是创造力。自相矛盾的是，创造力总是可以学习的，却很少被教授。尽管如此，我们必须努力。我们别无选择。**

**鲍勃·雷瑟曼**