# 推动产品创新，Arcweb 的 Chris Cera 的问答

> 原文：<https://devops.com/driving-product-innovation-qa-arcweb-chris-cera/>

总部位于宾夕法尼亚州费城的 Arcweb 于 2011 年成立，是一家专注于移动和云计算的企业软件开发公司。Arcweb 的团队在产品管理、敏捷软件开发和精益启动方法方面经验丰富，帮助客户管理产品生命周期，包括设计、架构、开发、部署和支持。

我们最近与 Arcweb 的 with Chris Cera 就平衡安全性和可用性、构建新产品以及开发实践的演进进行了一次对话。以下是我们的对话:

DevOps.com:你能给我们介绍一下 Arcweb 吗？

我们专注于企业软件的产品设计和开发。从纵向角度来看，我们所做的大部分工作都是金融技术解决方案。我们服务于金融科技领域的三个微型垂直市场。一个是银行业务，人们有时称之为零售银行业务。第二个是投资管理软件，所以我们做了很多经纪人-交易商和经纪人和财务顾问软件。第三是保险，如理赔管理、保险方面的销售支持。

这是我们的大部分业务；另一面是通用企业软件。这涵盖了整个业务领域，包括运营、营销和销售。从技术角度来看，我们大约三分之一的业务是移动应用部署——许多 iOS 企业应用。我们也做传统的 web 应用软件开发。

DevOps.com:好吧，既然你在那里，我们就从那里开始吧。我的意思是，你认为在可用性、安全性和合规性之间取得平衡的关键是什么？

**Cera:** 自然，我们会遇到许多以安全为导向的场景，我们总是在应对这些挑战。我发现设计和安全几乎是截然相反的。如果你想要真正有用的东西，那通常意味着它也有点不安全。在银行业领域，这对创新者和颠覆者来说是一个巨大的挑战；你试图构建一些易于使用的东西，但它也需要有银行级别的安全性。可用性和安全性总是在相反的道路上，所以我们总是遵循这两个世界的路线来生产满足这些需求的产品。

当发布一个新的应用或产品时，是什么将成功的创新和失败的想法区分开来？

这最终取决于最终用户。他们是第一位的，第二位是顾客。我们最近在做一个被终止的移动应用项目。风险、安全性和法规遵从性方面的人杀死了它，因为创新常常会吓到人。

我认为这在很大程度上归结于教育，因为如果一个大公司不这样做，那么一个小公司就会去做创新。这对任何一家大公司来说都是一个挑战:它想在自己的领域创新，但往往真的做不到。

**DevOps.com:创新和现状之间似乎总是存在斗争，所以你如何在设计过程的早期引入安全人员？**

在客户那里，通常需要更有远见的人来推动这样的事情。这通常意味着企业高管需要真正认可正在发生的事情。最终，让创新在大公司发挥作用是一个非常高层次的商业决策。我看到被扼杀的产品是那些产品经理有预算的产品。

他们将尝试测试市场，产品的反馈非常好。接下来，他们希望通过产品治理，或者公司称之为必须批准任何新产品开发的部门来获得它。这就是产品被扼杀的地方——因为从事风险和合规工作的人会给出 100 个理由说明为什么它会导致法律或欺诈风险。

**DevOps.com:随着开发方法从 10 年前的方法转变为今天的敏捷和持续集成/部署组织，这些挑战发生了怎样的变化？**

我想说的是，人们对于如何启动软件项目变得越来越聪明了。我认为，如果你看看 15 年前有多少软件项目失败，而现在有多少失败，我敢肯定，你会看到我们正在学习如何提高项目的成功率和最小化项目的风险。很明显，总会有异常值和失败的项目，但我们正在变得更好。

此外，敏捷软件开发已经存在了 15 年多，其中很大一部分集中在更紧密的迭代和持续集成或持续部署上。我认为这在很大程度上被认为是一件好事，但许多大企业仍然没有采用它。如果你有一个庞大的跨国员工队伍，试图让他们做一到两周的迭代几乎是不可能的。有太多的挑战。

从安全的角度来看，这也意味着可能每个季度被调用一次来进行审查、渗透测试等的安全人员现在需要更频繁地参与进来。这意味着更加关注自动化测试工具。我的意思是，在正常的开发周期中，自动化测试工具已经有了大量的创新。

良好的安全性只需要投资，并让企业明白这是您必须在项目中投入时间和精力的方式。安全测试只是构建过程的一部分。所以，如果你和敏捷项目经理交谈，一切都集中在迭代上。安全测试只是部署过程的一部分。然后，当然，你总是想做一些手工测试。我的意思是，即使我们试图尽可能地自动化，一些测试对于自动化来说太昂贵了，所以你只需要让一个可信的团体运行一个手动测试计划。我们对我们制造的每一个产品都这样做。

**DevOps.com:你喜欢如何开始一个产品？你喜欢做一个最小可行的产品，然后试一试，看看人们是如何使用它的吗？**

**Cera:** 对于我们的一个客户，我们走进咖啡店，让人们为我们测试一些应用。这不是真实的数据或任何东西；这是一个模拟。我们试图了解这个设计对顾客来说是否有意义。他们明白吗？他们真的会使用它吗？这是我们的专长，因为我们经常试图证明一个企业是可行的，而不是仅仅假设产品是可行的，然后就去建立它。顺便说一下，这是一个巨大的假设，我认为现代企业家更清楚地知道，不要马上假设这个产品或这个愿景会成功。

因此，在我看来，你的第一级测试应该始终是基于纸张的原型，以查看业务是否可行。然后，你应该创建一个 vaporware 移动应用程序。
放在面前:其实可以点一下；可以刷卡；你可以移动它。不涉及任何编码。我可以让我们更好的设计师在三天内完成，而我可能需要三个月才能让工程团队完成。然后，测试它的生存能力。如果有意义，继续前进，直到你验证了商业模式，并且证明了对产品的需求。现在，您可以更有信心投资于这一过程。