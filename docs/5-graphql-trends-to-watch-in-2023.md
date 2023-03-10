# 2023 年值得关注的 5 个 GraphQL 趋势

> 原文：<https://devops.com/5-graphql-trends-to-watch-in-2023/>

GraphQL 查询语言在 2022 年迎来了重要的一年。我们见证了其生产用例的增加，解决了困扰传统 API 集成的过度蚀刻和欠蚀刻问题。GraphQL 可以显著提高可用性，聚合多种服务，并优化数据在系统间的传输方式。

然而，GraphQL 也容易出现新的[安全问题](https://devops.com/graphql-vulnerability-analysis-the-top-threats/)。随着对 API 的攻击不断增加，并且变得越来越复杂，毫无疑问将需要一个增强的[安全焦点](https://devops.com/graphqls-greatest-strength-is-also-its-greatest-weakness/)来避免漏洞。在接下来的一年中，架构师可能还会努力解决他们的 GraphQL 成熟度问题，因为他们会考虑如何最好地在组织及其各种利益相关者之间扩展其使用。

下面，我们将考虑 GraphQL 在 2023 年的发展趋势。这些预测是基于我在 2022 年的报道和来自网络开发社区的报告。

## 1.增加生产用途

根据 RapidAPI 的[API 状态报告](https://stateofapis.com/2021)，有整整 62.6%的开发者报告称，他们在 2022 年比 2021 年更加依赖 API。随着[正在使用的 API 数量的增加](https://devops.com/api-sprawl-a-looming-threat-to-digital-economy/)，我们无疑会看到更多的 GraphQL 例子。GraphQL 之所以受欢迎，是因为它的可用性和灵活性超过了传统的集成点。[研究表明](https://devops.com/key-findings-from-the-2022-state-of-graphql-report/)它主要用于公开内部数据，尽管合作伙伴和公共使用案例并不少见。

表述性状态转移(REST)仍然是现代 API 的主导风格。根据 Postman 的 API 报告的 [2022 状态，89%的开发者使用 REST。GraphQL 以 38%的份额排在第四位，被 webhooks (35%)和 SOAP (34%)取代。尽管相比之下使用量仍然很小，但它正在稳步增长，并将继续扩大。](https://www.postman.com/state-of-api/api-technologies/#api-technologies)

## 2.统一不同的 API

GraphQL 有助于以易于使用的方式公开字段。但它也有利于将不同的微服务聚合到一个统一的模式中。因此，它经常被用作一个[元层](https://devops.com/graphql-as-a-meta-layer/)，它结合了多个 REST 服务、数据库甚至 GraphQL 模式。就目前而言，REST 似乎具有持久力。并且[没有必要将*所有*的 REST 服务迁移到 GraphQL](https://devops.com/smoothing-the-transition-from-rest-to-graphql/) 。展望未来，它更有可能被采用为现有 REST APIs 之上的一层。

将多个后端服务组合在一起，并在一个统一的模式中公开它们，可以创建一个更有用的、本地化的接口，前端开发人员可以从中工作。在未来，GraphQL 可能会成为更多组织的元层，增加内部服务的发现，并帮助团队重用内部微服务。

## 3.超图和子图

如上所述，GraphQL 不仅用于组合遗留 REST 服务，还用于组合多个 GraphQL 模式。有人称之为图表的图表——或[超图](https://devops.com/supergraph-one-graphql-schema-to-rule-them-all/)。组合了多个 GraphQL 模式的超图将提供无与伦比的开发人员体验，因为工程师可以从同一个端点访问许多服务。

然而，使用统一的图表进行集中也有不利的一面。不同的内部团队或合作伙伴可能只需要访问一组特定的功能。将*整个*模式交给每一个进门的人将是 TMI，更不用说违反最小特权的[规则的潜在安全风险了。因此，](https://accelerationeconomy.com/cybersecurity/understanding-and-deploying-least-privilege-security-models/)[T5 subgraph](https://www.apollographql.com/docs/federation/v1/subgraphs/)的想法获得了支持。子图是一个 Apollo 概念，但是该理论当然可以应用于其他实现。在未来，我们可能会看到更多的用例使用子图来帮助整个组织联合一个超级图，帮助分割一个图来满足特定利益相关者的需求。

## 4.打开 GraphQL 安全控制

截至 2022 年，不到一半(43.2%)的 GraphQL 实现禁用了查询自省。禁用现场建议和自省是降低公开图表暴露风险的方法。随着 GraphQL 安全最佳实践越来越明显，这些数字可能会变得越来越常见。其他安全控制，如实现查询超时、查询速率限制和查询成本分析，也有助于抑制潜在的恶意行为。

正如我们之前所介绍的，通过模糊性实现的安全性不足以保护 GraphQL。然而，许多本地 GraphQL 安全和性能指令没有被使用。除了开启这些高级特性，新的工具即将上市，可能会强化 GraphQL。安全厂商继续[增加对 GraphQL](https://devops.com/salt-security-adds-support-for-graphql-apis/) 的支持，让非安全工程师更容易获得它的保护。

## 5.大规模管理 GraphQL

近年来，GraphQL 已经出现在一些大型生产用例中，帮助 GitHub 的开发者提高可用性，提高网飞的生产力，并帮助 Shopify 的 API 战略。这些案例研究证明了它在大型企业中的实用性。但是我们如何在一个大型组织中有效地[扩展 GraphQL](https://devops.com/managing-graphql-at-scale/) ？

超级图和子图的概念有助于在整个公司范围内进行扩展。但是保持高性能对于保持有效的、可扩展的足迹也是至关重要的。因此，随着 GraphQL 的成熟，我们可能会继续看到公司优化其使用方式。这包括优化查询和查询深度，以及应用过滤和速率限制来满足应用需求。对 GraphQL 响应时间进行[测量对于建立随时间改进的基准是必要的。](https://www.marketplacer.com/blog/how-we-measure-graphql-response-times/)

## 我们只是在质疑表面

以上，我们只是触及了 GraphQL 在未来几个月中令人兴奋的发展的表面。关于查询语言的更新和周围工具环境的改进还有很多要说的。你认为 2023 年 GraphQL 会走向何方？请在下面的评论中告诉我们！