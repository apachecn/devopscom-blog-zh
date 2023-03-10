# 特征标志的寿命和时代

> 原文：<https://devops.com/the-life-and-times-of-feature-flags/>

不久前，我有机会仔细观察了 DevSecOps 工具(目前市场对它们的定义)。有很多值得喜欢的地方，他们正朝着“随时发现所有漏洞”的未来前进…只是一旦我们到达那里，会有新的漏洞不容易发现，我们的旅程将继续。

最近，我有幸深入研究了应用程序和 API 保护，目前我还不能(实际上，我不确定我能不能，所以不会)说太多，但它们也在以类似的方向前进，如果不是以类似的方式。

作为一名开发人员，[特性标志](https://devops.com/?s=feature+flags)从一开始出现就引起了我的兴趣。

和我一起唱《芝麻街》的歌曲《T1》:“其中一件事与众不同。”特征标志是…一个特征。

当他们第一次出现时，实际上是开发人员在他们的代码中编写#if 和#ifdef 语句来在编译时打开和关闭 bits。这让我想起了《宋飞正传》的那一集，在那一集里，他们向电视网的高管们解释这部剧的内容。“一个开发者做他的工作…那是一个产品！”

自那以来，市场已经走过了漫长的道路。但是，老实说，我不认为这些是独立的产品。看看目前大多数产品正在做的事情的广度——CI/CD 工具，我刚才提到的两个市场中的任何一个，或者类似领域中的任何其他市场。功能标志仍然只是“关闭这个功能，再打开它”。更新的版本允许这样做，而不需要重新构建整个应用程序。但它只是没有当前工具市场提供的大杂烩那么好。

我认为这些工具最终会成为一个更大的工具集的一部分。[微软](https://www.microsoft.com)、 [Atlassian](https://www.atlassian.com/) 和 [Cloudbees](https://www.cloudbees.com/) (举几个我不太费力就见过的例子)已经实现了功能标志，缩小了可用市场。他们实施这些计划是因为它非常适合几个市场。DevOps 工具是最适合市场的工具之一，这也是这些供应商实现它们的地方。

哪个市场会以他们告终？我不知道，这也是作为分析师的乐趣之一。最适合的是像 Atlassian 提供的 DevOps 工具链系统，无论你的工具链是什么，你都可以使用它们来加速验收测试或者保存一个版本而不用重新发布。但我也可以为其他地点提出有效的论点，所以我想你们都会在有选择时做出决定——也就是说，用你们的钱做出决定。

小心点。我根本不是说“避免特色标志公司，因为它不是真正的产品！”我只是说，您的功能标志供应商可能会在某个时候成为更大的解决方案的一部分，所以请确保您有一个计划来摆脱它，以防更大的解决方案是您的组织不想处理的。

我*说*“如果你还没有一个特征标志解决方案——即使是一个自己开发的——是时候把它放在适当的位置了。能够说“哦，是的，那个功能把事情搞砸了，让我们把它关掉，快！“是巨大的。对于需要多次冲刺的较大的子项目来说，通过常规的检入将代码放在流中，但是在构建中标记出特性的能力也是巨大的。没有合并或其他疯狂，只是在源文件或配置文件中“BuildNewFunction=FALSE”。功能标记系统越先进越好——最新的系统可以通过仪表板上的环境变量打开和关闭东西。这使得特性标志代码的包含比“我们考虑到数据库更新没有发生吗？“手卷解决方案。仍然不完美——因为这是一段旅程——但是商店里买的比你可能手工卷的任何东西都要好。

继续摇摆。不管有没有特色标志，你都在制造为这个世界——或者至少是你所在的那个角落——提供动力的系统，却没有得到应有的认可。所以再次感谢你。对于那些甚至不知道他们应该感谢你的人。