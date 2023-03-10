# 代码安全性:SAST、左移、DevSecOps 和超越

> 原文：<https://devops.com/code-security-sast-shift-left-devsecops-and-beyond/>

***自动化是推动代码安全超越 DevSecOps*** 的关键

几乎在每个行业，开发人员都在处理如何确保他们代码的安全性。无论是面向汽车、航空或工业控制的企业或应用，还是小型系统或大型系统，每个组织都面临着安全问题。作为回应，行业继续发展以提高自动化、交付速度和代码可靠性。让我们考虑一下当今应用程序开发生态系统的关键构件。

静态分析或[静态应用程序安全测试](https://en.wikipedia.org/wiki/Static_application_security_testing) (SAST)有助于实施编码指南和检测未定义的行为，通常用于整个开发生态系统。SAST 的一个优势是自动化。由于它不需要输入，SAST 很容易被引入到现有的软件开发过程中，在那里它将检查源代码构建并生成警告。MISRA、CERT C 等编码指南有助于避免常见的编程错误。然而，第二类，未定义的行为，是一个更大的问题。这是因为未定义的行为会带来风险。例如，空指针取消引用、缓冲区溢出或变量未初始化都是可利用的漏洞。根据其严重性，通常需要为客户发布补丁。

接下来，我们来考虑 DevSecOps，它横跨开发、安全和运营。尽管它在企业市场(如金融服务)中被广泛采用，但在汽车和工业等市场却相对滞后。尽管如此，对安全性的强调正在推动 DevSecOps 使软件开发人员的生活更轻松，并使他们更符合安全和操作功能。

例如，快速的反馈周期在每个行业都非常重要。考虑一个用例，在这个用例中，部署一个新开发的特性或一个补丁可能需要一个小时。这在今天这个时代是不可想象的，因为新的源代码必须几乎即时运行。

DevSecOps 中最重要的元素之一围绕着项目的分支策略。除了主分支之外，每个开发人员都使用自己单独的分支。他们开发他们代码，然后将它合并回主分支。主分支的一个关键要求是保持零个未解决的警告，以便通过所有的功能测试。

因此，在一个单独分支的开发人员提交他们的工作之前，它也需要通过所有的功能测试。并且所有的静态分析测试都需要通过。当拉取请求或合并请求有未解决的警告时，它将被拒绝，必须修复并重新提交。这些包括功能测试用例失败和静态分析警告。

功能测试失败必须修复。然而，失败的根本原因可能很难找到。一个功能测试错误可能会说，“输入 A 应该生成输出 B”，但是 C 却出来了，但是没有指示要更改哪段代码。另一方面，静态分析将揭示内存泄漏的确切位置，并为每个警告提供详细的解释。这是静态分析可以帮助 DevSecOps 交付最好和最安全的代码的一种方式。

最后，让我们回顾一下 Lean 和 shift-left，看看它们是如何联系在一起的。

精益开发专注于向企业交付价值。如果我们修复了这个缺陷，企业会获得价值吗？如果我们修复了这个警告，企业会获得价值吗？换句话说，消除浪费，在正确的时间点做出正确的决策。

零缺陷实际上是精益背后的重要哲学之一。当然，零缺陷绝不意味着零缺陷。它实际上意味着接近零的缺陷。例如，当修复一个特定的缺陷没有价值时，它可以被归类为不修复。同时，如果存在一个缺陷，当用户在 add 函数中输入一个负值时，应用程序将表现不佳，那么有两个选项:修复它或不修复它，如果期望用户永远不会输入负值。

目标是实现零缺陷基线并持续改进。在这个场景中，零缺陷指的是源代码问题以及来自静态分析的警告。

最后是左移的概念，这是一种将某些过程拉近开发人员的运动——在本例中是测试。通过对新代码提供更快的反馈周期，开发人员可以避免速度变慢。当在源代码项目中工作时，如果回归测试在一个块被提交几天后运行并揭示缺陷，开发人员可能很难回忆起他们当时在做什么。在几分钟而不是几天内得到更快的反馈，提高了质量和安全性。这样，左移就是 DevSecOps 和 Lean 的一个核心组件。静态分析是左移一部分。

那么下一步是什么？一句话，更多的自动化。确保开发人员有尽可能少的认知开销将允许他们更快更安全地构建代码。这可以通过结合上述概念以及使用基于行为的测试或测试驱动的开发来分析代码来实现。最终目标是加快反馈周期，从而加快开发周期。