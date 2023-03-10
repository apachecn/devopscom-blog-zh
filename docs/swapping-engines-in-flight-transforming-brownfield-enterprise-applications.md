# 飞行中交换引擎:改造棕色地带企业应用

> 原文：<https://devops.com/swapping-engines-in-flight-transforming-brownfield-enterprise-applications/>

随着 DevOps 思想变得越来越主流，企业需要将开发和交付应用程序的新方法整合到他们的标准 IT 流程中。通常情况下，复杂且受现有遗留基础设施、组织和流程限制的企业必须考虑如何以及何时将棕色地带企业应用程序过渡到敏捷方法。对于遗留基础设施上的生产应用程序，您如何看待“在飞行的飞机上更换引擎”？

DevOps 大师和实践者 [Rob Berger](https://twitter.com/rberger) 和我一起参加了最近在 DevOps.com 举行的[网络研讨会](https://info.vistarait.com/devops-transform-brownfield-enterprise-applications)来深入探讨这些话题。

什么是棕色地带？

环境保护局将棕色地带定义为“不动产，其扩张、再开发或再利用可能因危险物质、污染物或污染物的存在或潜在存在而变得复杂。”

将我们的企业遗留应用程序想象成有毒的垃圾场是很幽默的，在我们努力改造它们的不同阶段可能会有这种感觉，但在我们的世界中，棕色地带只是指已经投入生产的现有应用程序或服务。从几十年到几年前，它很可能是使用上一代工具构建的，服务于大型机或客户机服务器架构。

虽然“遗产”给人的印象是一个死气沉沉、停滞不前的企业，但棕色地带实际上无处不在。任何现有的基于计算机的服务的公司都有棕色地带过渡要解决，因为你不能就这样扔掉今天生产的东西。即使在创业的时候，遗留问题发生的速度也是惊人的。

那么，在将现有的棕色地带应用程序转化为现代化的 web 级应用程序的同时，如何继续为客户提供服务呢？

**关于 DevOps 的一个注释**

首先要记住，DevOps 是一个过程和旅程。不同的组织将处于开发运维的不同阶段。

Rob 提到了康威定律，该定律指出“设计系统的组织……必须生产这些组织的通信结构的复制品。”要点是，确保组织与你试图实现的目标相一致。打破孤岛，改善所有相关方之间的沟通，这一点非常重要，甚至比技术更重要。

**那么，有哪些 app 呢？**

企业应用程序大体上分为三类。许多将是预先存在的定制应用程序，那种围绕核心组织结构或业务功能的应用程序。它们既是最具挑战性的应用程序，也是最高的奖励。你想知道如何提供移动或网络应用程序，利用现有的应用程序慢慢转变为新的做事方式。

与现有应用程序相关的是来自供应商的打包应用程序，因为它们可以像定制应用程序一样包装在您的业务方式中。一些供应商可以支持迁移，但更常见的是，您必须确定最关键的新业务功能，并将其迁移到新的 DevOps 风格。

在某些方面，最容易处理的是新的应用程序。它们是全新的机会，可以与新的 DevOps 风格的团队一起从头开始，持续集成，测试驱动的开发，以及反映这一点的组织结构。

假设您有一个大型系统集成商在 8-10 年前使用标准开源技术 C++或 Java 以瀑布模型编写的单片现有应用程序。市场要求服务现代化，超越长周期版本中出现的增量变化。要将这个应用程序转变为 DevOps 世界，您需要经历哪些步骤？

**第一步–最小可行产品**

您不希望创建一个遗留应用程序的完整替代品，当然也不希望中断现有业务。但是你确实想发展它，以便你能满足你更现代的需求。

在组织层面，确定你必须交付的最重要的东西。什么是最优先的需求，什么能给你带来最大的回报？你想做的这个新事物的“最小可行产品”是什么？找出影响最大的最小转型范围。一个简单的例子可能是向现有系统添加一个移动接口，因为它只是在后端用相同的业务逻辑映射用户接口。

**第二步——创建(正确的)团队**

你需要一个由合适的人组成的小团队来交付这个最小可行的项目。它需要跨职能部门的代表性

*   业务组或产品经理，
*   主要开发商，
*   将自动创建服务的 IT 运营人员(不仅仅是操控服务器)

查看您当前的组织和架构，确定能够适应新的工作方式的人员。根据康威定律，找到相信新的做事方式的合适的人对于构建响应性应用至关重要。了解内部政治以及如何缓和人际关系。不要陷入过去，但是你需要一个运作良好的团队，能够很好地合作，不会中断你的业务。

**第三步——构建 REST API**

您的新应用程序将构建为可管理性和可伸缩性的自包含服务，通过 REST APIs 公开。确定您需要从遗留系统中获得什么服务，并围绕遗留系统创建 REST API，它可以将服务从遗留系统公开给新系统。你需要既了解旧系统又了解新系统的人来完成这项工作。

最大的变数之一将是如何最温和优雅地将 REST 接口包装在遗留应用程序周围。你希望新系统只是和 REST 对话，它不需要知道任何关于遗留 app 的事情。

**第四步——设计新服务**

使用现代工具。微服务应该是你做任何事情的基础。找出可以被认为是独立的、有自己生命周期的组件，通过 REST 或 JSON 接口将它们联系在一起。通过确定最小可行产品，您应该在 2-3 周的周期内工作，这样您可以很快看到结果。

**为什么选择微服务**

你的新应用应该是松散耦合的架构，称为微服务。微服务倾向于使用 RESTful APIs 作为它们通信的主要方式。

将每个微服务视为一个功能块，就像在函数式编程中一样，有特定的输入和输出，副作用应该是不存在的或非常可控的。这可以让你准确地知道每个盒子里发生了什么。互操作通过 REST 或流接口是显式的。在这两种情况下，您都可以拥有模式存储库，它成为微服务如何相互通信的定义。

**自动化一切**

每当软件开发人员将代码提交到 Git 存储库中时，它应该被自动部署到 QA 或登台环境中。从一开始就定下规则。如果您正在手工构建单独的服务器，这很好地表明您将会遇到问题。我们的目标是使用 Chef 和 Puppet 之类的配置自动化系统，在部署服务的核心位置编写脚本，或者将您的基础设施表示为代码。

你几乎想把服务器当作不可变的东西，当你想更新它的时候就扔掉。做到这一点的唯一方法是自动化，这导致了连续交付或连续集成的应用程序端概念。实现策略驱动的管理，其中策略嵌入在代码中。

**记住，你不是在取代你的遗产**

这是一次旅程，你刚刚开始走向独立的进化之路。

请记住，您可能会在短时间内同时运行旧版本和新版本。您需要弄清楚如何使用您的遗留系统作为后端，一个解耦的前端可以独立地发展到后端。说到下一点，请记住，当您转变企业时，运行新组件和遗留应用程序的团队必须紧密协作。

# 关于作者/ Varma Kunaparaju

[![YaCNNVuU](img/9fde196d104c43184303f7d9233b515b.png) ](https://devops.com/wp-content/uploads/2015/03/YaCNNVuU.jpeg) Varma Kunaparaju 是 Vistara 的首席技术官，也是一位经验丰富的技术专家，拥有 20 多年的经验，带领工程团队开发企业软件。在推特上联系他: [@varma1](https://twitter.com/varma1)