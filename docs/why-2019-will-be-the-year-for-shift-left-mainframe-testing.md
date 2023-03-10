# 为什么 2019 年将是左移大型机测试年

> 原文：<https://devops.com/why-2019-will-be-the-year-for-shift-left-mainframe-testing/>

虽然 2018 年是在测试中规划和实施左移方法的一年，但大型机和服务器测试人员在很大程度上落后了。这些传统的基础设施专家依赖于老式的测试工具。大型机保持运行，但是工具和测试实践经常成为瓶颈，阻止性能测试团队在周期中期和预发布时更快地进行测试。

直到现在。

[测试的未来在开源](https://info.blazemeter.com/moving-from-loadrunner-to-open-source-testing-tools-shifting-left-democratization-0?utm_source=devopscom&utm_medium=blog&utm_campaign=mainframe) ，终于有为大型机测试人员开发和定制的开源解决方案了。现在，大型机测试人员也可以左移，变得敏捷。

以下是大型机开发人员和测试人员将从转移 lift 和拥抱开源测试技术中受益的四个原因:

## 频繁发布

[Apache JMeter](https://jmeter.apache.org/) ， [BlazeMeter](https://www.blazemeter.com?utm_source=devopscom&utm_medium=blog&utm_campaign=mainframe) (基于开源)， [Taurus](http://gettaurus.org/?utm_source=devopscom&utm_medium=blog&utm_campaign=mainframe) 和 [Jenkins](https://jenkins.io/) 是遗留工具的理想替代品，原因有二。这些开源工具非常容易使用，因此开发人员和测试人员可以自己使用它们。此外，它们可以很容易地实现自动化——一旦脚本建立起来，它们就可以运行，开发人员可以得到结果并监控系统和他们的代码。

这两个原因是左移的基础:频繁释放。有一个比开发快得多的选择，等待 QA 运行测试， [与 QA 争论结果](https://www.blazemeter.com/blog/6-developer-phrases-qa-engineers-love-hate?utm_source=devopscom&utm_medium=blog&utm_campaign=mainframe) ，修复代码，再次等待测试结果，意识到你忘记提交修复的重要部分，再次发送代码，等待测试，熬通宵最后一次修复代码，却意识到你的代码与团队成员的代码冲突，你不能发布。

通过将您的代码测试集成到开发管道中，每一段代码都会立即被自动测试，无论是单独测试还是与代码的其他部分封装在一起。一旦代码被批准，为了客户/用户的利益，新的版本将立即发布。这也有利于开发人员，给他们一个干净的石板继续工作。如果代码需要修复，没有问题——会向开发人员发送一个警告，他们可以很容易地识别问题并修复它。固定代码立即被测试和发布。现在，这对于参与其中的每个人来说都更容易、更有动力。

## 更少的错误，更高的代码质量

向左移动意味着运行更多的自动化测试——并且更加频繁。通过不断地检查系统中的错误，并在每次构建时运行测试，您和您的团队会不断地被警告错误，然后您可以立即修复这些错误。结果是更高质量的代码和更好的系统性能。

另一个积极的结果是减少了团队开发时的麻烦，因为您不必一直纠结于以前的版本错误。那些已经被修复或处理，所以你可以专注于未来的计划和令人兴奋的发展，这将在更高的代码质量中实现。

## 成本降低

向左移动意味着更快和自动化的测试，从而产生更高质量的产品。通过一直并行运行更多的测试，测试人员和开发人员可以专注于开发新的代码，从而为企业节省成本。如果你在云中运行测试，你也节省了基础设施成本。

更高的发布速度、更快的修复和新特性会让客户更满意，他们会和你在一起，而不是转向你的竞争对手。客户与他们认为专注于未来的公司在一起，这就是为什么 [Gartner 的魔力象限](https://www.gartner.com/en/research/methodologies/magic-quadrants-research)“远见”认可被认为是测试行业的一件大事。

## 更好的团队协作

自动化和[连续测试](https://www.continuoustesting.com/)的想法可能会给人以不利于团队合作的印象，但事实恰恰相反。即使开发人员对他们自己的代码变得更加自给自足，这种完全的所有权实际上鼓励了团队合作。团队成员将通过共享的工作区和仪表板在联合功能开发上进行更多的协作，每个开发人员都将他们开发的代码与其他人集成。他们还将一起工作，发现系统的缺点，并学习如何修复漏洞和瓶颈。

大型机的左移和自动化意味着更多的时间用于特性开发、获取客户反馈并对其做出反应；更快的修复；和更快的发布。这对于参与市场竞争、提供最佳服务、吸引最优质的劳动力和维护产品安全至关重要。

## **使用开源工具开始您的大型机测试**

BlazeMeter 最近向开源社区贡献了 JMeter [RTE 插件](https://www.blazemeter.com/blog/introducing-jmeter-mainframe-testing-with-the-new-rte-plugin?utm_source=devopscom&utm_medium=blog&utm_campaign=mainframe) 。该插件支持在 JMeter 上对基于 IBM 3270 和 5250 的应用进行负载和功能测试。

运行大型机测试使大型机开发人员和测试人员最终能够将敏捷性引入到他们的测试习惯中，使大型机测试人员与他们已经接受了 shift left 和开源测试工具包的同事保持一致。

— [Refael Botbol Weiss](https://devops.com/author/refael-botbol-weiss/)