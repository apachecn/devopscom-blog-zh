# 问答:吉恩·金谈积累技术债务的痛苦

> 原文：<https://devops.com/qa-gene-kim-technical-debt/>

上周，我们报道了偿还技术债务的故事。本周，我们将与吉恩·金(@ [realgenekim](https://twitter.com/realgenekim) )讨论这个话题。作为 DevOps trends 的追随者，你可能已经知道他最近的书籍项目，[DevOps 食谱](http://itrevolution.com/books/devops-cookbook/)，当然还有他之前的作品，*可视操作手册*和*凤凰计划:一部关于 IT、devo PS 和帮助你的企业成功的小说*。

吉恩还创建了安全公司 Tripwire，并在那里担任了 13 年的首席技术官。Gene 以研究高性能公司为职业，我们很高兴他花时间与我们分享他对技术债务的想法。

告诉我们吉恩·金最近在忙什么？

**基因:**事情很多。现在，我非常专注于 10 月 21 日至 23 日在旧金山举行的 DevOps 企业峰会。峰会将重点关注精益 it、DevOps 和持续交付。我们对此非常兴奋。我们有 50 位来自大型企业的演讲者，如通用电气、迪士尼和梅西百货，以及其他令人难以置信的演讲者。

Gene，听起来是一件大事。我很好奇你对技术债的看法。有人辩称不存在。其他人则认为确实如此。技术债是否存在，如果存在，如何定义？

**基因:**沃德·坎宁安对技术债有一个很棒的[定义:“出货第一次代码就像负债。少量的债务可以加速开发，只要通过重写及时偿还。…当债务没有偿还时，危险就发生了。花在不太正确的代码上的每一分钟都算作债务的利息。在未整合的实现(面向对象或其他)的债务负担下，整个工程组织可能会陷入停顿。”](https://en.wikipedia.org/wiki/Technical_debt)

我对这句话的简单理解是，技术债务是你下次想要做出改变时的感受。它不仅来自于你在一个匆忙的项目中所做的所有捷径，甚至来自于每次开发人员不写自动化测试——每次你不做数据代码分析。当你跳过这些事情，债务每天都在增加。基本上是所有的变体，从正确的做事方式到我们实际做事的方式。积累的越多，就产生了越来越多的技术债务。

DevOps.com:企业中的技术债务通常是什么样的？

**Gene:** Randy Shoup 在这方面做了一个很棒的演讲，[速度的良性循环:我在 2013 年旧金山流量大会上从易贝和谷歌学到的快速发展](https://www.youtube.com/watch?v=EwLBoRyXTOI)，当时他是 KIXEYE 的首席技术官。在那次会谈中，Shoup 提出了应对技术债务的对策。他指出，任何影响性能和质量的事情，如伸缩的可靠性所定义的，都被视为优先级为零的缺陷。

本质上，他的意思是，无论何时出现可靠性或伸缩性问题，都会被视为零优先级缺陷。换句话说，这和网站宕机问题一样糟糕。它的意思是，这就像丰田，当他们有一个严重的问题时，每个人都停止工作，以便集中解决问题，直到问题得到解决。如果他们能帮助解决问题，他们会的。这与大多数组织中发生的情况相反，在那里“从来不是我的问题”,技术债务被允许增加。当您将问题放入缺陷计划时，您将它放入安全补救队列中，但是它永远不会完成。

它去那里等死。这是从未实施的好主意的垃圾填埋场。兰迪·肖普告诉我们，投资是有回报的。我认为这正是实现高绩效的文化。高性能是指部署 30 个或更少的代码，非常短的交付时间，部署时的高成功率，以及较短的准备时间。对于运营和信息安全来说都是如此。

所以，技术债务对运营不利；这对安全不利。这也不利于发展，因为它减缓了未来的流动。

Shoup 指出了良性循环和恶性循环之间的区别。良性循环被描述为一个坚实的测试循环。你有很好的测试，所以你有一个坚实的基础，这让你更自信。这让你越来越快。恶性循环是你没有测试。你的基础很不稳固。你害怕做出改变。你走得越来越慢。

**DevOps.com:在你观察高绩效组织的经历中，从讨论恶性循环和技术债务世界的幻灯片到良性循环的幻灯片，有什么挑战？我想，您是如何实施第 13 张幻灯片上详细介绍的内容的？**

基因:真的是政策。我们必须有一个策略来提高技术债务的偿还，并使团队能够关注非功能性需求——一个策略，一个人对完成的定义是无论何时开发人员说它完成了，它就完成了。直到有了自动化测试，自动化部署流程，任何人都可以按下按钮，通过测试周期并部署到生产中，这才算完成。

可交付成果还必须按照设计在生产中运行。这是完成的一个很好的定义。这阻止了我们从一个冲刺到另一个冲刺，并在我们身后积累技术债务。我会说技术债务的对策是*正确的*完成的定义。这就像敏捷哲学中的一句名言:完成的定义是在我们有工作的和潜在的可发布代码的每个冲刺阶段结束时。

我要补充的是，它是成块集成的。有一个支票存款处。在部署代码之前，任何人都可以运行自动化测试。我觉得这些都是很好的对策。

Devops.com:太棒了。现在，要从恶性循环进入良性循环，我想在获得回报之前需要大量的前期投资？

不幸的是，这是那种在你能走得更快之前先走得更慢的事情。但好处是如此引人注目。我们知道，高绩效人员的代码部署频率是他们的 30 倍，他们的速度可以提高 8000 倍。速度快了 8000 倍。所以回报是巨大的。

想一想:如果你一天不做部署，这意味着你比高绩效者慢 100 到 1000 倍。高绩效者可以在几分钟或几小时内完成部署，而低绩效者则需要几周、几个月或几个季度。当然，我们必须进行投资，从几周、几个月、几个季度到按需，在几分钟内执行。但这样做的价值太高，不容忽视。