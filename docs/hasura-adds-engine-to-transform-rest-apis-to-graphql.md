# Hasura 添加引擎将 REST APIs 转换为 GraphQL

> 原文：<https://devops.com/hasura-adds-engine-to-transform-rest-apis-to-graphql/>

Hasura 今天发布了一个用于集成应用编程接口(API)的[数据中心](https://hasura.io/blog/bring-rest-apis-as-a-data-source-to-hasura-announcing-rest-connectors-data-hub/)仓库。该存储库包括一个连接器，使得 it 组织更容易将 REST APIs 转换成基于 [GraphQL](https://devops.com/?s=GraphQL) 规范的 API。

Hasura 首席执行官 Tanmai Gopal 表示，该连接器使用 Hasura 开发的转换引擎的更新，无需编写自定义代码来将现有的 REST 端点连接到 GraphQL API。相反，GraphQL API 的模型会自动覆盖在 REST API 端点之上，Gopal 解释道。

GraphQL 最初由脸书开发，现已成为 REST APIs 的流行替代方案，因为它使开发人员能够在更细粒度的级别检索数据，从而提高了性能。Hasura 提供了该公司围绕一个项目开发的 GraphQL 引擎的实例，该项目现在由 Linux 基金会的一个分支 GraphQL 基金会托管。GraphQL 提供了对通过 API 可用的数据的完整描述，并按照类型和字段而不是传统的端点来组织。除了阐明哪些数据可以通过 API 获得之外，开发人员还可以使用类型来避免编写手动解析代码。

![](img/42a6e4a47980d36d99d0b989ed74d2f7.png)

Hasura 声称，自 2018 年推出以来，其引擎已被下载超过 4 亿次。它通过为分页、过滤、连接、设置授权规则和优化性能提供通用的访问模式，自动化了将模型映射到 API 的重复性工作。Hasura 还提供能够连接到多个服务和数据源的 API，嵌入特定于域的授权逻辑，并提供额外的安全层。

Gopal 表示，Hasura 现在还增加了一种为任何 GraphQL 服务或数据源创建特定于身份的授权策略的方法，通过限制 GraphQL APIs 的模型和字段来加强安全性，从而消除了 IT 团队拼凑不同库和框架的需要。

此外，Hasura 正在将对谷歌云的支持添加到测试版的 Hasura Cloud 中，这是一种托管 API 集成服务，该公司已经通过亚马逊网络服务(AWS)云提供了这种服务。Gopal 补充说，对微软 Azure 云的支持将于 2022 年推出。

尚不清楚组织在多大程度上希望用基于 GraphQL 的 API 替换现有的 REST APIs。然而，Gopal 指出，在很多情况下，组织需要在他们可能不拥有的 REST API 之上覆盖一个 GraphQL API。他说，例如，目前公开 REST API 的软件即服务(SaaS)平台可能没有任何支持 GraphQL 的计划。

毫无疑问，企业中使用的 GraphQL APIs 的数量将会急剧增加。现在的挑战是找到一种方法来管理它们和现存的前几代 API。问题是，许多 API 是由开发人员创建的，他们可能没有记录他们创建的 API，或者在某些情况下，根本没有通知 DevOps 团队他们的存在。