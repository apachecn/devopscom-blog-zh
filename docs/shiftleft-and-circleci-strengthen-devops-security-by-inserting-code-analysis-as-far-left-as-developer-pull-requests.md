# ShiftLeft 和 CircleCI 通过在开发人员拉取请求的最左侧插入代码分析来增强 DevOps 的安全性

> 原文：<https://devops.com/shiftleft-and-circleci-strengthen-devops-security-by-inserting-code-analysis-as-far-left-as-developer-pull-requests/>

新的合作伙伴关系和产品集成在 CI/CD 管道的最早阶段之一提供了业界最快、最准确的漏洞扫描

### 加利福尼亚州圣克拉拉，2019 年 12 月 4 日

自动化应用安全领域的创新者 ShiftLeft Inc .今天宣布与 [CircleCI](https://circleci.com/) 合作并深度集成，使组织能够将安全性直接插入来自代码存储库的开发人员拉取请求中。ShiftLeft Inspect 是第一家与 CircleCI 合作提供这些功能的静态应用安全测试(SAST)供应商。

当今的组织正在努力将安全性尽可能地融入到开发运维流程中，但许多组织都在努力实现自动化安全质量决策所需的速度和准确性。迄今为止，唯一可以在构建阶段运行的工具需要花费数小时或数天来扫描，这大大降低了开发人员的速度。众所周知，这些工具还会产生大量的误报，这意味着组织不愿意在没有手动筛选结果的情况下自动使构建失败，这增加了进一步的延迟。

拉请求对开发人员来说是一个关键阶段，因为在这个阶段，新的开发人员代码被集成到整个代码库中。通过在“拉”请求时启用 SAST，合适的开发人员可以在合适的时间获得合适的漏洞信息。开发人员可以更有效地解决各自代码中的漏洞，从而提高最终版本的整体安全性。

这种合作和集成使 CircleCI 用户能够在 CircleCI 构建上运行 ShiftLeft Inspect，并从任何与 CircleCI 集成的代码库中提取请求。然后，可以根据安全标准自动升级、警告或拒绝拉取请求和构建。因此，CircleCI 用户可以用 DevSecOps 目标来反映他们的 DevOps 计划。

“作为一家在许多平台上提供多种产品的技术公司，我们一直在寻找最佳方法来确保我们的代码是最高质量和最安全的。我们很高兴与 ShiftLeft 合作，并与 CircleCI 合作，以确保我们的代码管道产生安全的代码。使用该产品所节省的时间和资源让我们变得更加敏捷和高效。”里克博姆，副总裁，信息安全，家庭顾问。

作为合作伙伴关系的一部分，ShiftLeft Inspect 将免费向 CircleCI 用户提供无限数量的应用程序和框架，每年总计不超过 20 万行代码和 300 次扫描。免费许可证将包括一种编程语言，并使 CircleCI 用户能够同时扫描多达两个应用程序。

CircleCI 业务开发副总裁 Tom Trahan 表示:“今天的开发人员正在以令人难以置信的高速度构建和交付软件，这是满足组织和客户需求所必需的。“从历史上看，安全性被视为减缓这一速度的一个步骤。CircleCI 很高兴与 ShiftLeft 合作，使开发人员能够在 CI/CD 管道中更靠左的位置插入安全性，以实现准确的漏洞扫描。”

“就源代码分析而言，目前应用安全领域提供的大部分内容都是为了自动化而自动化。ShiftLeft 的产品管理副总裁 Alok Shukla 说:“今天市场上的工具实际上并不能让组织自动做出正确的决策。“使用 ShiftLeft 和 CircleCI，组织和开发人员能够在涉及到发布质量时做出准确、快速的决策，比以往任何时候都更加远离开发生命周期。通过将安全性插入到拉式请求的最左侧，我们提供了行业首创的 SAST 功能，这将帮助我们的客户利用现代 CI/CD 管道的优势，而不会将安全性抛在后面。”

ShiftLeft 客户和 CircleCI 用户可以通过 CircleCI Orb 立即获得该集成，circle ci Orb 位于[https://circleci.com/integrations/.](https://circleci.com/integrations/)

##### 关于 ShiftLeft

ShiftLeft 是一个持续的应用程序安全平台，专为现代软件开发生命周期而构建。它将[下一代静态代码分析](https://github.com/ShiftLeftSecurity/codepropertygraph)(快速准确地识别漏洞)与自动化工作流中的应用程序检测(保护应用程序)相结合。这种基于运行时信息的代码分析和基于运行时信息的代码保护的结合提供了最准确、自动化和全面的应用安全解决方案。要了解 ShiftLeft 如何让应用程序安全性与 DevOps 的快速发展保持同步，请参见 https://www.shiftleft.io/。