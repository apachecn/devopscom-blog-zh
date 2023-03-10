# Hasura 发布了企业级特性，因此开发人员可以更快地构建关键任务应用程序

> 原文：<https://devops.com/hasura-releases-enterprise-grade-features-so-developers-can-build-mission-critical-applications-faster/>

**Hasura 的 GraphQL 引擎在 2.5 年内从 0 增长到 1 亿次下载，成为过去两年增长最快的开源 GraphQL 项目**

旧金山，2021 年 2 月 23 日(环球新闻网)——数据访问基础设施公司 Hasura 今天宣布，它已经发布了其流行的开源 GraphQL 引擎的 2.0 版本。该版本现在允许组织从一个配置中同时部署 REST 和 GraphQL APIs，从而在现代应用程序开发和支持现有 REST APIs 之间架起一座桥梁。该版本包括业界第一个 GraphQL API 网关，为任何 GraphQL API 提供粒度授权。此外，除了 PostgreSQL、SQL Server 和 MySQL 之外，该版本现在还支持 Google 的 BigQuery 数据库，因此开发人员可以轻松地即时访问数据，以加速应用程序开发。

Hasura GraphQL 引擎自 2018 年上线以来，呈现爆发式增长。下载量在 2019 年增长到 200 万，2020 年增长到 1 亿，成为过去两年增长最快的开源 GraphQL 项目。今天，该项目拥有超过 20，000 名 GitHub 明星。今天的发布对于开源项目和 GraphQL 社区来说是一个重要的里程碑，并使 Hasura 更接近于实现其提供跨数据平台和信息孤岛的通用安全数据访问的愿景。

[Pipe.com](http://pipe.com/)的产品工程主管伊恩·马卡里诺说:“Hasura GraphQL 引擎 2.0 证实了使用 Hasura 作为我们基础设施的基础部分是正确的选择。“作为金融科技领域的一家初创公司，我们必须不断创新，同时为客户提供最高级别的数据安全。Hasura 中的新企业功能为我们提供了快速利用不同 API 格式和数据源的灵活性，同时安全地将高特权数据仅授权给正确的实体。”

今天，Hasura 还宣布了 GraphQL Engine 的托管服务产品，Hasura Cloud，现在具有 AWS VPC 对等功能，可以在安全的专用网络中将他们的数据和基础设施安全地连接到 Hasura Cloud。Hasura Cloud 和 Hasura 的内部部署企业版都由 Hasura 的 GraphQL 引擎提供支持。

Hasura 的联合创始人兼首席执行官 Tanmai Gopal 表示:“Hasura GraphQL Engine 2.0 拥有我们最期待的功能，使在企业中构建任务关键型应用成为现实，加快了关键计划的上市时间。Hasura 的声明式配置方法和现代开发人员体验，加上强大的授权引擎，意味着组织可以在不牺牲安全性的情况下快速创新。事实证明，Hasura 是下一代关键任务应用程序的支柱。专有数据访问的时代已经结束。技术和用户行为发展得太快，以至于无法完全重新设计系统。Hasura 的愿景让开发人员能够专注于用户体验，同时以新的方式重用他们的数据。”

组织在构建新的应用程序时需要访问有价值的数据，但这些数据被困在孤立的数据库中。Hasura 没有尝试使用手动方法来构建 API 并担心安全性、性能，也没有尝试整合快速移动的运营数据，而是提供了一个新的选项，使开发人员可以轻松地访问数据:使用基于 API 的现代方法，通过联合对数据所在位置的访问来连接应用程序。有了 Hasura，开发人员可以在几分钟内从这些来源获得灵活的数据 API，从而即时访问在线数据。

有了 Hasura，开发人员可以快速构建连接到数据的应用程序，而不必等待昂贵、耗时的集成和基础设施项目来完成他们所需的构建。相反，他们可以专注于利用数据解决业务问题，并快速构建和发布为其组织增加价值的应用程序。Hasura 提供的速度和灵活性对于受遗留系统限制的组织来说是真正的变革。

RedMonk 联合创始人 James Governor 表示:“当今的组织希望提供对 API 和数据服务的 GraphQL 访问，同时利用他们现有的 REST 资产进行粒度控制。“Hasura GraphQL Engine 2.0 旨在满足这一需求，通过一个单一的管理和身份验证模型，在行级别跨越各种数据库源，将 REST 和 GraphQL 连接起来。”

Hasura GraphQL 引擎 2.0 的新特性

• Simultaneous auto-generation of REST and GraphQL APIs. To ease the transition to GraphQL, Hasura GraphQL Engine 2.0 provides the ability to auto-generate REST and GraphQL APIs, enabling organizations to support both formats within a single configuration – saving significant time and cost. This also enables organizations to continue to support existing investments in REST APIs.• Enhanced security and authorization. Hasura GraphQL Engine 2.0 includes the industry’s first GraphQL gateway with built-in authorization so that developers can easily secure all the GraphQL APIs in their organization – not just ones created by Hasura. Using GUI tools or declarative configuration, developers can easily configure granular role and attribute-based access control rules and inheritance policies to prevent unauthorized data use and security breaches in complex enterprise systems.• Expanded database support for Google BigQuery. In addition to relational database support for PostgreSQL, SQL Server, and MySQL, Hasura GraphQL Engine 2.0 provides auto-generated GraphQL APIs for Google BigQuery, eliminating complex data migrations and enabling data unification at the GraphQL layer.

借助对 AWS VPC 对等的新支持，企业可以安全地连接到 Hasura Cloud
AWS VPC 对等和 Hasura Cloud 安全认证。Hasura Cloud 用户可以在私有、安全的跨场所网络中使用其托管的无服务器产品，利用 AWS 的 VPC 对等技术加速企业环境中的数据访问。Hasura Cloud 还通过了 SOC2 Type 1 和 HIPAA 认证。

关于 Hasura
Hasura 正在帮助构建全球相关的、数据驱动的应用程序和 API 的现代世界。Hasura 的一系列数据访问解决方案通过 GraphQL APIs 将数据和服务即时连接到应用程序，帮助组织加快产品交付。欲了解更多信息，请访问: [https://hasura.io](https://hasura.io/) 或关注@HasuraHQ。