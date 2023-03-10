# 深入了解 DevOps 报告:与木偶实验室的问答

> 原文：<https://devops.com/inside-look-at-state-of-devops-report-qa-with-puppet-labs/>

上周，Puppet Labs 在 [2015 年 DevOps 报告](https://puppetlabs.com/2015-devops-report)中发布了 DevOps 和持续交付实践年度研究背后的分析。该报告现已进入第四个年头，它深入探讨了团队对于成为高绩效 it 组织意味着什么的研究结果——这些组织共有的文化特征、它们参与的精益工程实践以及它们所依赖的技术架构。然而，和去年一样，当涉及到实际的统计发现时，这份报告似乎有点像一个黑箱。虽然一些数字确实通过了，例如，经常被抨击的高性能组织的部署速度是低性能组织的 30 倍，交付时间是低性能组织的 200 倍，但报告本身在确定低、中、高性能指标的统计基础上有些拐弯抹角。

DevOps.com 与 Puppet 的首席信息官奈杰尔·克斯滕和高级产品营销经理岚娜·布朗就该报告进行了交谈，以获得更多细节，让他们解释分析背后的过程，并提供他们在过去几年中发现的一些最重要的方面。

***DevOps.com:*** *能不能给我们的读者稍微介绍一下报道中的高点？*

2013 年的一个重大发现是，使用 Devops 实践的组织部署代码的频率增加了 30 倍，失败减少了 50%。在 2014 年，非常令人着迷的是，我们实际上发现了这些实践与整体组织绩效之间的联系，而不仅仅是 IT 绩效。绩效较高的 IT 组织超出自身盈利能力、市场份额和生产力目标的可能性是其他组织的两倍。

如果我们快进到今天，使用 Devops 实践的高绩效组织比以往任何时候都更加稳定和可靠。他们从故障中恢复的速度快了 168 倍，并且由于他们的更改，故障减少了 60 倍。因此，我们实际上并没有看到吞吐量比前一年有所增加，但我们看到的是质量和速度确实有所提高。因此，人们正在进行质量更高、需要更少回滚的更改。

因此，我们从今年的报告中看到的数据得出的结论是，生产装配线的左侧受到了极大的关注。因此，如果我们设想开发人员工作流应用交付，基本上我们从最左边的开发人员笔记本电脑开始，最右边是实际存在于生产中的应用。因此，从开发人员的笔记本电脑和实际发布之间的角度来看，我们看到组织更加关注该阶段，将更多的测试放在开发人员手中，所有这些实践不仅关注发布，而且关注应用程序生命周期的预生产阶段，这对质量有着巨大的影响。

***DevOps.com:*** *为什么 Puppet 不公布调查的实际数据？你在这里有很好的分析，但背后很少有统计证据——你为什么不提供呢？*

布朗:我们有大量的数据，我们不发布这些数据的部分原因是，如果不进行大量的数据清理和统计分析，你实际上不可能得到相同的结果。所以我们的分析实际上是相当严谨的，其中一些分析并不太适用于图表和视觉效果之类的东西，因为它们都是基于相关性和预测性回归。所以这是部分原因。

我认为这在很多方面类似于向世界发布软件。我们内部有所有这些工具。我们收集了所有这些 Excel 电子表格。我们有所有这些数据透视表和不同的聚类分析，但它们只是-它们现在对其他任何人都不是特别有用。

尽管我们很想知道如何完善和共享所有这些内容，使之成为一个包含所有工具的大数据集，但我们最大的担忧是，由于所需的分析水平，人们实际上会从数据中得出某种误导性和不正确的结论。

***DevOps.com:*** *您能告诉我们，当时您是如何得出高绩效、中绩效或低绩效组织的判定的吗？因为如果你看看这些数字，你会说他们的部署频率增加了 30 倍。但他们当然会这样做，因为他们是高绩效者。那么这在统计学上是怎么算出来的呢？*

布朗:不，不，你说得完全正确，我也认为 IT 性能指标有点不全面。然而，这些是对 IT 组织很重要的实际指标，因此他们关心部署频率、部署交付时间、恢复和更改故障率的平均时间。因此，我们觉得这是一个很好的近似值或 IT 性能的代理，最好添加那些与整体性能更高相关的事情。

**Kersten:** 还有一件事，尽管人们实际交付和发布代码的速度有很大的差异，但今年和前几年的调查显示，高性能(org)在数据点上确实是成簇的。这不仅仅是一个平滑的光谱，而是有一个非常明显的高性能集群，它们都与他们使用的实践类型有非常高的相关性。所以它有点圆，但也不是我们看到的从 0 到 100 的平滑光谱。我们看到的是大众，然后是高绩效者，他们分成了非常清晰的群体。

布朗:是的，它们不是任意的集群；它们实际上是统计学上的。因此，低 IT 绩效者共享所有相同的特征，而高 IT 绩效者共享所有相同的特征，所以他们非常清楚。

***DevOps.com:*** *好了，如果你有这些的统计基础，让我们来谈谈这些群体之间的一些共同特征。告诉我一些关于低绩效者的情况，我们会继续讨论，我们可以谈论他们共有的特征。*

**Brown:** 因此，对于 IT 性能来说，部署困难实际上是最相关的因素。部署难题由几个问题组成。

比如你的部署有多痛苦？它们是非常具有破坏性的事件吗，等等？因此，我们围绕部署难题提出了三个问题。

与 IT 性能高度相关的下一件事是版本控制。我们对所有生产工件使用版本控制。接下来是文化，我们用的文化模型来自一个叫罗恩·韦斯特罗姆的人，他是一个社会学家。他创建了一个文化类型学，你可以在报告中看到这个表格。所以他有一种病态的文化，官僚，然后生财。因此，你的文化越富有创造力，你就越有可能拥有更高的 IT 绩效。

Kersten: 我认为这是我们去年开始采用 Westrum 时最感兴趣的地方，我们实际上采用了 Westrum 作为模型的一部分，在这种病态与生殖文化中，这是我们在这一领域的从业者用来谈论在那里工作的伟大之处的语言:“我的想法受到重视。我可以创造想法。我可以创造影响力。”类似地，在另一个地方工作是多么可怕。它完美地映射了组织的病理和生殖描述。

***DevOps.com:*** *那么，根据您的数据，您认为从低性能到中等性能的第一次飞跃的关键特征是什么？*

**Brown:** 因此，在 IT 性能方面表现不佳的人会减少自动化和测试工作。例如，他们还没有实现部署自动化。

Kersten: 我认为我至少想到的一个方法是，这些特性是必要的，但没有一个特性是足够的，所以你会看到有人说只是采用了版本控制。他们无疑走在了那些还没有采用这些工具的人的前面。

但是一旦你真正采用了版本控制和连续交付以及高度自动化的冲突管理系统，就会有一个革命性的飞跃，这些东西加在一起比它们的部分加起来还要大。至少在我们看来是这样的，因为我们实际上没有低绩效者和刚刚采用这些技术的高绩效者之间的这种平滑的小范围。

我们确实看到了这些人的进步，但只有当他们全部采纳时，他们才会突然有这种数量级的飞跃。