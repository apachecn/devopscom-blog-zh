# Supergraph:一个 GraphQL 模式来管理它们

> 原文：<https://devops.com/supergraph-one-graphql-schema-to-rule-them-all/>

GraphQL 作为一种与后端服务无缝交互的方式已经获得了很多关注。查询语言对前端开发人员来说也是一个福音，因为它允许您方便地获取您需要的特定字段，从而消除了对 REST APIs 的潜在过度提取或提取不足的担忧。随着 [GraphQL 在组织内的采用越来越成熟](https://devops.com/managing-graphql-at-scale/)，人们对企业如何使用 GraphQL 来安全地统一不断增长的不同微服务和 API 目录越来越感兴趣([和投资](https://devops.com/netlify-acquires-onegraph-to-integrate-graphql-apis/))。

使用 GraphQL 作为[元层](https://devops.com/graphql-as-a-meta-layer/)可以帮助将许多不同的系统统一在一个统一的模式下。这将实现古老的承诺[可组合性](https://nordicapis.com/how-apis-enable-the-composable-enterprise-model/)，其中软件构建块被无缝地拉到一起，为不同的客户端类型组装应用程序和独特的体验。然而，[大规模管理 graph QL](https://devops.com/managing-graphql-at-scale/)可能会变得棘手。当一个模式变得非常大时，它可能需要一个自己的模式！这就是超级图概念的由来。

我最近会见了 Apollo GraphQL 首席执行官 Geoff Schmidt，以了解什么是超级图以及它如何帮助平台聚合其后端微服务。根据 Schmidt 的说法，“开发人员希望这个组合层是他们所有服务的一个抽象视图。”下面，我们将探索超图的概念，并查看一些新的开源组件，它们可能会帮助您在组织中实现基于 GraphQL 的可组合性。

## 微服务支持可组合性

首先，我们所说的可组合性是什么意思？嗯，[可组合架构](https://nordicapis.com/how-apis-enable-the-composable-enterprise-model/)与微服务有着内在的联系。您可以将每个微服务想象成构成应用程序一个方面的一个乐高积木。例如，优步使用[4000 个](https://www.cncf.io/case-studies/uber/)微服务来驱动其后端。这些服务包括地图、货币兑换、司机点评、支付和其他部分。当两者结合时，它们最终创造了便利和圆滑的用户体验，这就是优步。

施密特解释说，从历史上看，软件开发人员监管的是较大的单体应用程序，其中单个客户端与 web 服务器互连。另一方面，微服务更倾向于特定领域，并与其他微服务一起使用。与单一代码库相比，它们通常更容易迭代，发布速度更快。

## 对聚合的需求

由于微服务时代的到来，应用程序通常会从各种来源获取更多的数据。例如，一个银行应用程序可能会循环输入抵押贷款服务、投资服务和其他数据源，以在屏幕上显示组合的净值。施密特说，微服务的这种[爆炸创造了一个跨越数据库和 API 的“多边形环境”,增加了服务的复杂性。](https://devops.com/api-sprawl-a-looming-threat-to-digital-economy/)

现在很多第三方组件必须组合在一起才能渲染出一种体验。然而，支持这种可组合性对于开发人员和后端 API 团队来说是一个挑战——更不用说编写一个[后端对前端的](https://nordicapis.com/decoupling-the-presentation-layer-from-the-backend-using-bff/)可能会很麻烦。“应用程序开发人员因为需要集成或组合这些后端服务而变慢了，”施密特说。"开发者需要一种方法将所有这些碎片重新组合在一起."

## 什么是超图？

超图可以被认为是图中的图。愿景是用一个 GraphQL 模式和一个入口端口来监控许多服务。随着越来越多的开源项目出现，创建超级图也变得越来越容易。例如， [Apollo 最近开源了一些组件](https://www.apollographql.com/blog/announcement/backend/the-supergraph-a-new-way-to-think-about-graphql/)，可以帮助构建和操作一个超级图。其中包括[联盟](https://github.com/apollographql/federation)，它帮助创建跨多个服务的数据图，以及[阿波罗路由器](https://github.com/apollographql/router)，一个用 Rust 编写的工具，它决定如何路由查询。阿波罗还开源了一个[超级图演示](https://github.com/apollographql/supergraph-demo)以及其他资源。

Schmidt 说，超图架构已经在驱动 Expedia、沃尔玛、[、网飞](https://nordicapis.com/graphql-microservices-gqlms-as-a-backend-a-netflix-case-study/)、Paypal、纽约时报和其他大型环境。例如，Expedia 已经使用一个超级图来结合航班、租车和其他微服务，以创建集成的体验。现代连锁超市新贵 Hivee 也使用超级图将其投资整合到 API 中。

根据 Schmidt 的说法，最根本的好处是花在编写集成代码上的时间更少，这意味着更快的开发速度和快速改变业务的能力。“它允许你快速改变业务，以满足客户的需求。”超图还可以使您的 API 资产更加清晰可见，从而使审计更加容易。

上述组件的一个主要优点是，它们已经有了在商业规模上运行的良好记录。但是在 Apollo 项目之外，其他小组也在尝试编写类似的 GraphQL 模式聚合概念。例如，WunderGraph 在一个“[虚拟图](https://devops.com/graphql-as-a-meta-layer/)中使用 GraphQL，该虚拟图作为一种公共语言来调用各种底层 API。

## “一张图统治一切”的反响

施密特说，希望在一天结束时，这种抽象可以有助于“让世界变得更加以人为本”这是因为 GraphQL 可以启用符合独特用户口味的不太死板的应用。但是健壮的合成层将是允许这种重新配置所必需的。

当然，正如我之前提到的，当向一个入口通道提供如此多的电力时，有重大的安全障碍需要解决。增加对 GraphQL 的依赖将需要预先考虑新的[潜在的安全风险](https://devops.com/does-graphql-introduce-new-security-risks/)，比如模式自省和对象级授权控制。

根据 Schmidt 的说法，GraphQL 复合层提供了一个加强安全控制的机会。他将这些定义为为一组特定用户创建访问规则的契约。通过声明性地管理 GraphQL 安全性，开发团队本质上可以公开超图的子图供合作伙伴使用。该图甚至可以针对内部团队进行细分。

入口的中心点将需要授权规则来保护用户隐私，并避免违反最低特权规则。施密特还提倡为了解他们需求的应用程序开发人员构建后端模式，而不是精确地将逻辑映射到业务模型。

## 超级图表:图表的图表

软件变得越来越模块化，这导致了独特的微服务和 API 的激增。施密特说，我们现在正处于软件架构如何划分和组合的另一个转折点。他现在认为 GraphQL 是创建软件架构的最佳机会，这些软件架构可以用一个 GraphQL 查询调用多个后端服务。

“GraphQL 是构建现代应用程序所需的组合层，”Schmidt 说。“我们对此感到非常兴奋。用户已经表明 GraphQL 就是未来。Supergraph 是一项如此强大的技术，我们很高兴将它带给每个人。”