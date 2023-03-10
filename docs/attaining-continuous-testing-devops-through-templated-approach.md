# 通过模板化方法在 DevOps 中实现连续测试

> 原文：<https://devops.com/attaining-continuous-testing-devops-through-templated-approach/>

通过先进的软件开发技术和持续交付，无缺陷应用程序的持续需求市场正在得到解决。因此，许多组织采用左移方法和敏捷最佳实践——这暗示了“尽早测试，经常测试”的格言——通过这种方法，他们可以在软件开发管道的早期吸收 QA 实践和测试。这也包括对许多组织的持续测试。

# **devo PS 中的连续测试**

如今，持续测试是领先软件公司最喜欢的实践。持续测试意味着通过整合完整的产品周期，在整个软件开发管道中进行测试，从产品设计到产品发布。即使在产品发布后，公司也会测试以排除客户投诉，从而进一步改进产品。

DevOps 中的持续测试包括鼓励开发工程师和操作人员也实践测试，并使他们成为整个周期的一部分，而不是一个单独的团队。持续测试不仅包括早期阶段的测试，还包括每一个过程的测试。它的目标是尽可能自动化几乎所有的过程。

## **devo PS 中持续测试的模板方法**

DevOps 中持续测试的完美方法应该是手动和自动化测试之间的正确平衡，为了实现这一点，组织必须实践虚拟化，以成功地规划整个产品开发管道。许多组织还没有准备好冒持续测试的风险，因为如果他们不知道如何执行，大错误仍然是可能的。但是，连续测试方法中的错误可以很容易地纠正，因为它是在每个过程中实施的。

当涉及到产品开发时，错误是常见的；因此，正确的自动化测试工具集对于发现和纠正错误至关重要，因为手动测试可能会遗漏某些错误。手动测试也需要相当多的时间，这是一个巨大的缺点。公司可以实践一种计划良好但结构严谨的模板化方法，从而向持续测试进行全面的转变。

连续测试是通过吸收特定参数的多个用例来确定该方法的强度而实现的。那些被证明是确定持续测试是否值得的可靠方法的参数包括分布、技术、规模和负载、环境、安全性和发布。

## **检查参数**

完全检查一个维度的参数，如连续测试，可以基于消除和加权评分来创建读数，以从用例场景中获得结果。让我们看一个通过这些参数运行面向公众的托管服务的简短应用程序:

**配送—**考虑本产品的配送区域和地理位置。

**规模和负载—**测试用例的数量(举例来说，在这个场景中有 3，500 个自动化用例)、基于浏览器使用的套件、云测试平台和用户数量都在这个类别中考虑。

**环境和安全性—**该参数考虑了各种设备使用、跨浏览器测试、安全的云环境和版本批准。

**发布–**该参数考虑了发布的数量和频率以及技术堆栈。

用于这个场景的工具有 Selenium web driver、Selenium GRID、Jenkins、Sauce Labs、Sauce On-Dand Plugin。

检查参数的过程是通过在部署期间使用 Jenkins 从 Bitbucket automation repository 触发自动化测试用例，以及在 Sauce Lab cloud 中执行自动化脚本来完成的，因为并行线程是通过将 Sauce Lab 插件与 Jenkins 连接来完成的。

控制机制首先包括通过冒烟测试、回归和集成自动化测试执行。然后，捕获所有测试用例的测试证据。稍后，当测试完成并且自动化测试捕获的屏幕截图得到验证时，UAT 就完成了签署。

测试自动化框架的一些参数在 Selenium 中进行比较，在不同的类别上完成测试，比较它们的分数，然后将它们传递到测试环境中。一些套件、回归套件和集成测试套件是在开发和 QA 阶段执行的，稍后来自这两个环境的变更被部署。Smoke suite 是在前期制作、编辑和制作阶段进行的。最后，成功地导出了这些阶段的验证结果。

此用例场景在这些阶段的已证实结果是:

*   并行测试明显地将回归时间从 150 小时减少到 15 小时。
*   增强的测试覆盖矩阵解决了各种设备和操作系统碎片以及浏览器组合的问题。
*   代码升级到产品的质量把关人。
*   减少生产中的回归问题。

## **结论**

经历这样一个用例场景的例子帮助我们更好地理解如何通过仔细的观察、计划和通过这样的参数的部署，将连续测试逐渐集成到产品开发管道中。

在 DevOps 环境中移植连续测试需要小心执行，以避免错误和将来的缺陷。借助正确的工具和完美的执行，我们可以成功地缩短上市时间，降低时间和成本。

有关如何在不同场景中应用模板化方法的更多信息，请观看[本次网络研讨会](https://ter.li/frxp2b)。

— [尼兰贾尼·拉梅什](https://devops.com/author/niranjani-ramesh/)