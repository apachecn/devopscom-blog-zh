# Apollo GraphQL 使联邦服务器更容易访问

> 原文：<https://devops.com/apollo-graphql-makes-federated-server-more-accessible/>

在本周举行的在线 GraphQL 峰会之前，Apollo GraphQL 今天宣布[已经更新了其 Apollo Federation 产品](//www.businesswire.com/news/home/20210406005358/en/Apollo-Federation-Surpasses-2-Billion-Queries-Per-Day-as-It-Helps-Software-Teams-Collaborate-Better-Ship-Faster)，该产品使 GraphQL 服务器能够跨多个平台，使使用不同工具的更广泛的开发人员更容易访问它。

Apollo Federation 现在集成了 Apollo Studio 和 Apollo Workbench，前者是一个基于 web 的工具，用于导航 GraphQL 应用程序编程接口(API ),后者是一个用于 Microsoft Visual Studio 的插件。

与此同时，Apollo GraphQL 正在提供一个命令行界面(CLI)，称为 Rover，这使得在 DevOps 工作流中集成 Apollo Federation 变得更加简单。

Apollo GraphQL 的首席技术官 Matt DeBergalis 表示，随着越来越多的组织开始意识到他们对软件的依赖程度，GraphQL 作为更严格的 REST APIs 的替代方案正在继续获得吸引力。DeBergalis 指出，开发人员创建 REST APIs 可能更简单，但基于 GraphQL 的 API 更容易更新和管理。

![Apollo GraphQL](img/e09669d3435723c63b5780298420266a.png)

组织遇到的挑战是 GraphQL 服务器可能变得太大而不容易导航。DeBergalis 解释说，Apollo Federation 提供了一种机制，可以在多个平台上管理这些 API 的子集，这些平台组成了一个 GraphQL 服务器的联合实例。

DeBergalis 还指出，已经采用 GraphQL 的 IT 厂商也开始增加对 Apollo Federation 的支持。DataStax 是开源 Cassandra 数据库管理实例的提供商，它将 Apollo Federation 添加到开源数据网关 Stargate 中，以访问存储在 Cassandra 数据库中的数据。

QraphQL 的核心是为 API 提供一个开源的数据查询和操作语言，以及一个执行查询的运行时。GraphQL 基金会最初由脸书开发，现在是 Linux 基金会的一个分支。随着越来越多的组织采用 API 来构建基于微服务的应用程序，GraphQL 的采用稳步增长。然而，鉴于 REST API 已经被广泛部署，GraphQL 不太可能在短期内完全取代 REST API。

然而，DeBergalis 说，需要更敏捷的方法来构建和部署软件的组织正在用脚投票选择更容易更新的 GraphQL APIs。DeBergalis 补充说，随着软件环境的变化率不断增加，对部署和更新 API 的更灵活方法的需求变得更加明显。

就客户机和服务器之间来回传输的数据量而言，GraphQL 也比 REST APIs 更高效。当消耗的数据量稳步增长时，让客户端对如何从服务器返回数据进行更多控制的需求变得更加迫切。Apollo GraphQL 声称，现在每天有超过 20 亿个查询是针对其 GraphQL 服务器实例发起的。

不管使用什么类型的 API，它们每天都在增加。随着新冠肺炎疫情之后数字业务转型计划数量的增加，面向内部和外部的 API 数量也在增加。开发人员可能对他们想要使用的 API 类型有自己的偏好，但是随着开发人员越来越多地承担在部署后构建和管理 API 的任务，GraphQL 的吸引力变得难以忽视。