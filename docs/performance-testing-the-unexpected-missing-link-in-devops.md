# 性能测试:DevOps 中意想不到的缺失环节

> 原文：<https://devops.com/performance-testing-the-unexpected-missing-link-in-devops/>

开发运维与持续交付在企业中携手并进已经不是什么秘密，但是诸如性能测试之类的过程如何适应这个等式呢？

许多企业仍然保留着传统的思维方式——QA 和性能测试团队完全独立于开发团队。一个广为流传的神话是，每个人都有不同的角色、职责、背景和专业领域。然而，随着 DevOps 在企业中越来越受欢迎，测试、开发和操作之间的明显分离不再存在。事实上，为了成功地实现性能测试，曾经孤立的部门必须协同工作。

## 为 DevOps 创造文化

DevOps 最常见的目的是拥有软件和应用程序部署更新的自动化管道。除非所有人都参与进来，否则企业无法实施 DevOps。要做到这一点，不仅要有软件工程师和技术购买者的认可，还要有高管层的认可。这确保了 DevOps 流程和策略得到适当的实施。

然而，这不仅仅是获得 DevOps 所需的工具；要使其有效，必须有一种向合作的文化转变。这是企业从向开发运维的转变中获得最大收益并变得最敏捷的时候。

一旦采用 DevOps，专家和高级用户可以帮助促进如何使用它来实现最大收益，并帮助组织从它那里获得更多。确定和评估这种最大收益的关键方法是在整个开发过程中不断进行测试。虽然首先想到的可能是“功能性”测试(确保代码正确运行，并在出错时向开发人员提供快速反馈)，但没有任何组织能够发布交付缓慢用户体验的应用程序，因此具有快速反馈的“性能”测试同样至关重要。持续测试只有在自动化的情况下才是可扩展和可持续的。

## DevOps 使负载测试更容易

DevOps 的一个主要优势是自动化使一切(从实施到功能和性能测试)变得更快、更可预测。工具链确保每次代码推送都做了“正确的事情”。那些还没有实现性能测试的人经常提到的一个问题是，它“太费时间了”,并且他们将不能以有效的速度来促进不同的测试。但是惊喜！已经实施开发运维的组织能够更好地以完全自动化的方式将性能测试添加到组合中。像 BlazeMeter 这样的解决方案只需几分钟就可以启动并运行 API 测试，只需为要测试的特定页面或端点添加 HTTP 事务。一旦设置好了，这些测试将会持续自动运行，并且当有任何问题或者潜在的问题区域时会通知团队。当已知网站流量激增时，可以将更多的统一资源标识符( URIs)添加到测试中，但这不会影响 it 的自主性。

DevOps 的另一个关键功能是整个企业的可伸缩性，用户流量的可伸缩性极其重要。虽然性能测试在没有 DevOps 的情况下仍然可以扩展，但是基于相同的原则运行使得每个概念与分析两者结果的人更加相关。关键是将性能测试与已经存在的连续交付或集成管道直接集成，比如 Jenkins 或 CircleCI。在这里，快速、小范围的性能测试能够并行运行，以确保在将构建提升到下一个阶段之前，性能达到预期。在测试或 QA 环境中运行的测试，比如 IBM BlueMix 或 Chef，也可以被自动化和集成。

性能测试也很重要，不仅仅是因为它可以轻松集成到 DevOps 实践中，以及它如何适应 CD 管道，还因为它可以改善整体客户体验。一个正常运行的网页或移动应用程序是你的品牌和你的目标客户之间的联系，如果它不能正常或及时加载，你可能会失去一个竞争对手的客户。性能测试确保用户不会经历速度变慢或可怕的停机时间，这通常是后端系统运行不良的结果。将性能测试合并到工作流中创建了一个集中的环境，在这个环境中，所有的团队成员都有他们需要的东西来设计、运行或分析测试，同时彼此之间以及与企业中的每个人进行快速而清晰的通信。

性能测试和 DevOps 不是对立的力量；工具链中自动运行的性能测试节省了时间，而不是消耗更多。现实是，在这个快速软件交付的时代，测试是保持开发过程在轨道上和高质量的粘合剂。性能测试应该是每一个软件交付工作流的一部分，DevOps 允许这种情况发生。

## 关于作者/迈克尔·塞奇，首席福音传道者

Michael Sage 为 BlazeMeter 带来了 15 年的企业软件血统和客户成功。在 BlazeMeter 之前，Michael(更好的称呼是“Sage”)是软件交付和性能管理领域的解决方案架构师和顾问。他曾与包括 Mercury Interactive、Hewlett-Packard 和 New Relic 在内的行业领先公司合作，帮助团队实施集成解决方案，增强客户的性能和体验。作为一名自学成才的黑客和开源倡导者，Sage 总能把握住文化时代精神的脉搏，并加入健康的幽默元素。