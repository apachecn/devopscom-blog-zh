# Log4j:开源有“太多”这种东西吗？

> 原文：<https://devops.com/log4j-is-there-such-a-thing-as-too-much-open-source/>

Log4j 漏洞让我思考:有没有开源太多这样的事情？

在任何人立即发出愤怒的电子邮件、愤怒的推特或尖刻的博客帖子之前，请听我说一会儿。如果你了解我，你就知道我是一个开源狂热者。我被问过很多次，“我们应该使用开源软件吗？如果应该，应该使用多少？”我的回答是(现在仍然是)开源软件是创新的巨大源泉，我可以向你保证，不管你是否使用它，你的竞争对手肯定也是！

我可以继续赞美[开源](https://devops.com/?s=open+source)的优点，以及它如何实现云、重塑软件架构、创造新产品类别，并为我们提供遥测等有价值的工具，以及增加对云原生应用、基础设施等的可见性。

当我在 12 月 9 日第一次听说 [Log4j 漏洞](https://devops.com/u-s-govt-cx-eo-mozilla-revenue-log4j-latest/)时，像许多其他人一样，我迅速通知了我网络中的技术负责人、工程师和 sre 关于[严重的潜在风险](https://securityboulevard.com/2021/12/update-log4shell-rce-zero-day-reactions-and-recriminations/)这样一个广泛使用的 Log4j 工具中的零日漏洞。在某种程度上——可能是唯一的方式 Log4j 漏洞利用与 2020 年末的网络安全管理软件产品供应链攻击有一个非常重要的特征:该软件在应用程序、系统和组织中的广泛分布和无处不在的使用。可以说，Log4j 的应用要广泛得多。

这种相似性提出了我在如此广泛使用的软件环境中没有充分考虑的问题。我们可以过多使用开源软件吗？Log4j 的使用是否过于普遍，从而导致单点故障？如果一个补丁没有立即可用或者没有出现，Log4j 的情况会有多糟糕？

我不断得到的回答是响亮的“不”。我仍然不认为有使用太多(插入任何开源项目名称)软件这种事情。log4j——以及许多其他开源软件项目——对我们大有裨益，在当今无处不在的软件时代，没有这些系统、工具和解决方案，我们几乎无法运作。

当前的 Log4j 漏洞、最近的软件供应链攻击和其他具有广泛影响的网络安全事件突出表明，我们需要[快速响应安全事件](https://devops.com/log4j-puts-effective-it-operations-at-center-stage/)，并在软件堆栈中发现安全事件的任何地方采取补救措施。这包括开源软件。高影响安全漏洞可能出现在我们使用的众多软件堆栈和服务的任何地方，尽管当它们出现在广泛使用的基础架构、可重用组件和微服务中时，影响甚至更大。

在基础设施即代码(IaC)的世界里，不再是修补一组特定的路由器或服务器的问题。不幸的是，许多软件栈没有容器化，或者没有使用更小的、容易替换的容器和微服务来构建——至少现在还没有。我们的心态和流程必须从这一事件中改变，我们必须准备好[在软件堆栈的横向和纵向上响应和修复](https://securityboulevard.com/2021/12/here-we-go-again-second-log4j-flaw-surfaces/)漏洞。在某些情况下，我们必须大规模地这样做。

与活跃的开源项目一样，Log4j 贡献者很快做出了响应，提供了一个现成的补丁。我上面的原始问题的真正答案是，很少有人像那些不可思议的、勤奋的、积极的和投入的开源软件开发人员那样准备好应对一个重要的安全漏洞。