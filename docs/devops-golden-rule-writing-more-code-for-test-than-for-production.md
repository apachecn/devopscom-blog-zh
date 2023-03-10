# DevOps 黄金法则:为测试编写比生产更多的代码

> 原文：<https://devops.com/devops-golden-rule-writing-more-code-for-test-than-for-production/>

持续改进可以帮助一个古板的 IT 组织完全转变成一个创新机器。但是没有有效的测试自动化，这种转换是不可能的。加里·格鲁弗如是说，他曾在惠普和梅西公司领导过 DevOps 之旅，现在是一名顾问，通过他的公司指导其他组织实践大规模敏捷。

上个月，在 IBM InterConnect 上，格鲁弗给观众们提供了大量关于从食物链顶端领导开发者的宏观建议。但是，当深入到细节时，也许最好的收获之一是他对测试驱动开发的强调。

“它需要可靠，需要稳定，需要可维护。我想说，如果你要转变你的组织，测试自动化是最重要的事情，”格鲁弗说。“这是最容易出错的事情之一。如果你做对了，它就非常有价值，如果你做错了，那将是一场维护的噩梦。”

他提供了他在 Macy's 和 HP 工作期间学到的真实世界的经验，例如，他解释了 HP 的一个情况，在这个情况下，trunk 上不稳定的测试和不稳定的代码使团队四天不能签入代码。面对一家 20 亿美元的企业“紧追不舍”，格鲁弗承认当时他有些坐立不安，并发现这种不稳定性促使他们在流程中增加更多的测试。

“所以我们并没有变得更好，因为没有代码进入并得到修复，我们真正需要的是一个让好代码进入并阻止坏代码进入的过程，”他解释说，他的团队最终决定采用门控提交。“如果代码没有通过 red build 所需的系统测试，那么它就不会进入 SCM，也不会进入主干。”

与此同时，当他到达梅西百货时，他被告知有 1000 种自动化测试可供使用。但是当他开始将这些测试与迅速发展的持续交付团队结合起来时，他们发现没有一个测试足够可靠。他建议观众看一看杰夫·摩根的 *[黄瓜和奶酪](https://leanpub.com/cucumber_and_cheese)* 中提出的架构哲学，这有助于他在梅西百货的工作，在他的任期结束时，IT 部门一天几次运行超过 5000 个自动化测试，而每 10 天就有 1300 个。

他解释说，他坚信质量保证应该与架构师结合在一起，以确保自动化框架能够长期持续。

“让你在开发方面的首席架构师参与到你在质量保证方面的领导中来，并考虑如何为你的测试自动化构建可维护的框架，”他说。"如果没有，你将会在测试自动化的重压下死去."

如果做得好，一个组织很可能会为测试编写比运行其产品更多的代码。

“这不是一件坏事，”他说。"你会发现当你写好测试自动化时，它会迫使你写更好的代码."