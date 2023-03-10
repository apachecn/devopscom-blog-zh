# DevSecOps 实现:静态分析

> 原文：<https://devops.com/devsecops-implementation-static-analysis/>

我最近为[加速策略小组](https://accelst.com/)做的一件事就是调查[开发工具集](https://devops.com/?s=DevSecOps%20toolsets)。对我来说，这是一个有趣的领域，因为在我看来，开发和安全非常契合。拥有一个独立的安全组是有用的，甚至在某些情况下是必要的，但是让开发人员编写代码并在之后寻找漏洞总是显得非常低效。每当我管理开发人员时，安全培训只是我带来的一揽子计划的一部分。第一次写好(相当于 shift-left)要比重写容易得多。

我不会在这里指名道姓——这是我为 ASG 做的工作，它不是我要放弃的——但我今天将谈论 DevSecOps，并走向未来。我计划本系列的三到四个部分，讨论 DevSecOps 工具的不同方面。

为了清楚起见，我们将 DevSecOps 工具定义为“开发人员支持的安全工具”这意味着在某种程度上，他们帮助开发人员改善整体安全状况，同时让他们成为开发人员。我们都知道，如果要在 DevOps 世界中发挥作用，安全性必须在各个方面左移，但大多数组织还没有认真开始转移安全性。希望这个系列有所帮助。

根据你更喜欢哪家金融分析公司，预计未来几年 DevSecOps 市场每年将增长 28%至 33%。虽然这对 DevSecOps 供应商来说是个好消息，但这意味着很少有组织系统地采用了 DevSecOps，否则就没有这样的增长空间。

无论是传统团队还是 DevOps 团队，DevSecOps 的静态分析部分(通常)很容易设置和配置，并且大多数产品在编码时和构建时都提供反馈。IDE 插件已经走过了漫长的道路，有些甚至在编写代码时提供建议，有些则允许开发人员对他们的工作进行按需静态扫描。整个行业都在努力降低误报率，这使得大多数组织不愿意广泛部署它们，并且在最好的产品中可以对问题进行优先级排序，从而使识别和补救变得非常容易。试用:选择一个供应商和项目，抓住 IDE 插件，看看他们能做什么。大多数还不直接支持代码气味，但我怀疑这将很快实现，因为系统已经被设计为查看源代码并确定问题。增加可能出现的问题将是一个差异化因素，并迅速转化为市场需求。

要检查的事项:

*   **语言支持:**你使用的语言有扫描仪吗？虽然市场上的大多数工具都支持多种语言，但还是有差异的，所以请检查一下极限情况。这确实是一个决定成败的决定——如果市场上最好的产品不支持您使用的语言，那么它对您的组织来说是没有用的。
*   IDE 集成:这很简单，你的开发人员每天使用的 IDE 都受支持吗？这些工具中的大多数还提供了命令行变体，因此即使没有 IDE 的直接支持，给定产品的安全功能也可能要求命令行更好。在这种情况下，确保开发人员运行扫描的过程是一个好主意。
*   **检测到的漏洞**:至少应要求支持国家漏洞数据库(NVD)中的现有内容，并符合 OWASP 标准。大多数供应商在 NVD 之外提供支持，因此需要进行一些研究，看看检测到哪些类型的漏洞。
*   **点击通过支持:**使用 IDE 插件，扫描的最大优势之一是开发人员能够简单地点击结果列表中的漏洞，并转到有问题的代码。确保这行得通——而且像广告宣传的那样行得通。
*   假阳性率:这在历史上一直是个问题，但整个行业已经降低了这个问题。请你的潜在供应商分享他们的数字。我们的经验显示，百分之一位数很低，这比过去好得多，但仍有改进的余地。

静态分析的另一部分是将静态分析插入到构建过程中。这些产品中的大多数都集成到了最流行的构建管理工具中。扫描整个应用程序允许静态分析看到应用程序的更广阔的视野，并注意由不同开发人员编写的部分之间的交互问题。构建时扫描的报告通常在应用程序/团队级别，如果您愿意，最好的工具会将开发时扫描的结果与构建时扫描一起显示。

要检查的事项:

*   **语言支持:**再用语言。这里非常简单:应用程序的核心可以使用给定供应商支持的语言构建，但关键部分可能不支持。集成是一个真正的问题。确保需要扫描的内容能够得到扫描。
*   **集成:**这些工具中的大多数通过与构建工具集成来提供自动扫描，或者构建经理可以启动的手动扫描。从长远来看，自动化是首选，所以检查您选择的工具是否集成到您组织的构建工具中。
*   **深度:**我们不打算在这里讨论源代码组成分析(SCA)——那是另一篇博客的内容——但我们将观察漏洞可能来自您的源代码。在静态分析情况下，扫描工具可以跟踪多远？它的深度是否足以涵盖给定应用程序的集成和相互关系？虽然 SCA 会检测到很多静态扫描检测不到的东西，但是诸如“发送到[插入外部 API]的不安全值”之类的东西在静态代码分析中应该是可用的。
*   **报道:**在这里你可以找到最多样的流行工具。看看他们的报告和点击支持，找到最适合你的需求。
*   **误报率:**与上面的 IDE 集成相同——确保它足够低，让您的组织感到舒适。
*   **扫描运行位置:**这将成为该领域的一大优势，您希望您的扫描在云中运行吗？在数据中心？两者都有吗？检查你的供应商；对这些选项的支持程度有很大差异。

当然，这只是冰山一角。这是一个完整的细分市场，静态分析工具已经存在很长时间了。许多组织还没有认真对待开发时安全性，尽管我们都知道我们需要这样做；我只是提供一个开始的地方。

DevSecOps 才说得通。静态扫描是成熟的，通常集成良好。这是开始向左转移安全性的好地方。我们明白:开发人员不想成为安全分析师，否则他们已经填补了许多安全空缺中的一个。但是 IDE 集成使这些扫描工具更具交互性，侵入性更小，向开发人员展示了如何在编码时安全地进行扫描。这对我来说很棒，因为良好的编码实践将成为实时、现场提醒和指示的第二天性。这也意味着，如果开发人员按照该工具的建议进行操作，那么第一次开发的代码会更加安全，并且不需要重新进行安全检查。

你们都在艰难时刻保持着光明。DevSecOps 试图让你惊人的工作不被打断的可能性更大。获得这些工具来保护您组织的投资组合和您的辛勤工作是有意义的。