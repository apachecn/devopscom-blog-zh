# 我们的 API 乱局来了

> 原文：<https://devops.com/our-api-mess-is-coming/>

API 满足了在不同的系统、操作系统和数据集之间创建一致和可靠的集成的长期而深刻的需求。当我们开始使用[基于 REST 的 API](https://devops.com/?s=REST+APIs)时，我们也意识到它们填补了自动化中一个以前很少被提及的空白。坦率地说，他们是 DevOps 交付的力量倍增器。

早期在独立于系统的 API 方面的努力不是很大，但是我们吸取了教训，并且正在稳步变得更好。虽然 REST 是 API 的默认解决方案，但它可能不是路的尽头，因为我们会继续学习和改进。这就是我们在技术领域所做的——对一个想法感到兴奋，推动它广泛应用，然后反复改进它。

这就是问题的根源。我们已经并且正在用 API 饱和我们的应用程序。内部的，外部的，依赖他人的外部的。每当我看到一个中型应用程序的 [API](https://securityboulevard.com/?s=API) 依赖图时，我想到的就是“意大利面条代码”这些线到处都是，经常回到自己身上。

我们必须保持这种创造。也许不是单独的*我们*，而是 IT 和开发团队中的*我们*。唯一不变的是变化，我们中有太多的人不仅没有计划 API 的变化，甚至没有考虑到它们。因为事情通常进展顺利，大多数 IT 经理和开发团队有更紧急的事情要考虑。

但风险管理——尤其是广义风险——是未来规划的重要组成部分。如果您失去了对外部 API X 的访问，您将如何保持您的应用程序运行？如果您丢失了承载 API Y 的整个内部系统，如何及时恢复呢？虽然大多数组织会识别并修复单点故障，但解决方案是一个池，并且需要了解池中 Z 台服务器丢失的影响(如果没有其他影响的话)，例如“用户体验会在哪个点受到影响？”需要被询问，并制定一个计划来防止这种情况发生。

我们已经看到了使用外部 API 带来的问题。所有这些都是可以预测的——一个 API 下线，甚至完全消失；API 接口或伴随的数据格式改变；API 底层算法的改变，导致数据结果的改变等。

API 的使用比以往容易得多——公司正在努力使访问 API 变得更容易，不管是你的还是别人的。这是一件好事，因为这意味着花在计算和调整 API 调用和请求数据上的时间更少了。但这意味着我们对 API 的依赖只会增加，依赖图中的行数——每一行都代表一定的风险——只会增加。

“但我们正在云中工作，因此我们可以自动扩展，失败不再是我们的问题！”有人喊。虽然这可能有助于一些场景，但对其他场景没有帮助——如果某个供应商破产并采用了您使用的 API，或者某个首选供应商(或内部组件)成为安全风险，您仍然需要采取措施。在你的弱点变成问题之前知道它们是什么和在哪里是很重要的，并且值得你花时间去做。

你们大多数人都在扼杀它，更快地推出解决方案，迭代以使它们更好，使用 API 来扩展功能并减少交付时间。我只是说，要意识到你正在制造的技术债务，因为债务总是要到期的，风险最终会成为问题。因此，要知道基础设施中的风险是什么，并制定一个计划，在它确实导致问题时做出反应。