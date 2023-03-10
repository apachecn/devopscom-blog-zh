# 理解开发者体验的重要性

> 原文：<https://devops.com/understanding-the-importance-of-developer-experience/>

如果你正在创建一个开发者工具，你一定会遇到这种困境——你非常了解它的内部工作原理，但是其他人不了解。如果没有可靠的文档和示例可以遵循，那么对于另一个人来说开始工作可能是一个挑战。与我们所用工具的摩擦会导致[精疲力竭](https://devops.com/leverage-empirical-data-to-avoid-devops-burnout/)，抑制创造力并减缓创新。

开发者体验(DX)正成为任何软件公司考虑的一个不可或缺的因素。我最近会见了 Nylas 的首席技术官兼联合创始人 Christine Spang，讨论了投资开发人员体验的好处。下面，我们将看看 DX 到底是什么，并考虑实现它的一些最佳实践。

## 什么是开发者体验？

开发者体验(DX)类似于用户体验，但是是面向开发者的工具。DX 在用某个框架、语言或平台开发的同时，考虑开发者的旅程。Spang 说:“开发者体验是开发者在明确他们想要实现什么和到达你已经创建了那个东西的点之间所经历的摩擦的数量。

例如，考虑与 API 集成，以解决支付集成这样的常见用例。这里涉及到许多步骤，从阅读参考文档到获取 API 密钥、测试调用和理解服务如何响应。在开发人员最初将 API 集成到他们的应用程序中之后，他们可能还必须随着服务版本的变化而不断更新。斯潘说，在整个旅程中，DX 可以被认为是“弄清楚如何将想法转化为输出有多难”。

同样重要的是要注意，DX 不仅仅是面向公众的平台。拥有高质量的开发者体验对于内部软件来说同样重要。根据 Postman[2022 年 API 状态报告](https://www.postman.com/state-of-api/api-first-strategies/#api-first-strategies)，随着正在开发的 API 的[激增，改善内部开发者体验的紧迫性正在增加，特别是因为其中大多数(58%)是私有 API。根据公司的规模，内部 DX 可以包含许多领域。](https://devops.com/api-sprawl-a-looming-threat-to-digital-economy/)

## 投资开发人员体验的最佳实践

那么，有哪些全面提升开发者体验的方法呢？嗯，拥有最新的文档、代码样本、更好的例子和标准化的文档是积极的开发者体验特征。Spang 还分享了一些有助于提高 DX 的最佳实践:

**为最常见的情况提供脚手架**。测量人们用平台构建的东西的模式，并提供脚手架来支持常见的用例。这可能相当于一个常见场景的入门指南。

**提供样本代码库**。编辑代码比从头开始写要容易得多。考虑到这一点，创建一个预先烘焙好的环境，让开发人员可以尽情发挥。提供可工作的应用程序、用例模板和粘合代码是帮助开发者更加无缝地进行开发的实用方法。

**从参考手册**开始。演练和示例代码不应该取代完整的参考手册。从一开始就拥有最新的文档来迎合高级用户是非常重要的。从这里，您可以生成围绕参考规范构建的 Postman 集合或交互式沙箱。

**测量 DX 成功，迭代**。监控开发人员体验指标的一种方法是记录入职流程并测量转换率。就 API 而言，这可以通过询问有多少人打通了电话来跟踪。使[成为第一个呼叫](https://nordicapis.com/why-time-to-first-call-is-a-vital-api-metric/)的平均时间是多少？了解这些指标可以了解您的工具的自助服务功能有多有效。

对于 DX 来说，重要的一点是在过多的定制工作和专注于核心项目之间找到平衡点。在这一点上，斯潘建议“确保你建立的任何东西都符合公司的整体愿景。”本质上，如果你不是一家咨询公司，而是一家产品公司，你应该坚持这个目标。

“你想让人们通常想做的事情变得非常容易，”斯潘说。"然而，你不希望高级用户感觉受到平台的限制."

## 优质开发人员体验的例子

对于那些创建面向开发者的服务的人来说，有一个框架来建模是很有帮助的。那么，有哪些优质开发者体验的例子呢？

Spang 说,[顶级公共 API](https://nordicapis.com/13-api-directories-to-help-you-discover-apis/)是这些天来为开发者的期望设置障碍的很好的例子——像 Twilio 或 Stripe 这样的服务展示了相对无缝的开发者之旅。Spang 还指出了拥有强大 DevOps 和 CI/CD 背景的公司，[如 Etsy](https://www.simform.com/blog/etsy-devops-case-study/) ，这些公司多年来投资于可用的后端基础设施，以加速内部开发。

对于高质量开发人员体验的其他来源，考虑来自最新的 [2022 堆栈溢出调查](https://survey.stackoverflow.co/2022/#technology-most-loved-dreaded-and-wanted)的高级开发人员最喜欢的技术。工程师喜欢使用 PostgreSQL、AWS、Phoneix 和 Docker 等技术。更新的、流行的语言也越来越有用。例如，86%的开发人员说他们喜欢使用 Rust，而 76.65%的人害怕使用 Objective-C。

## DX 的总体优势

Spang 说，对开发人员体验的投资有助于提高敏捷性和开发人员的满意度。首先，一条更容易的开发路径增加了你如何随着时间运送和发展项目的速度。其次，开发人员体验等同于更少的倦怠和更少的流动，这两者都会产生真正的业务影响。

软件开发行业像野火一样迅速发展，每年都有大批初级开发人员涌入。Spang 说，有趣的是，平均经验水平正在下降，增加了对更抽象的工具和工具包的需求。在这种环境下，开发者体验无疑是一种竞争优势。

因此，如果您正在创建面向开发人员的工具，请考虑其他人在使用它们时的体验。增加开发人员的体验可能只是项目成功和开发人员社区长期幸福的决定性因素。