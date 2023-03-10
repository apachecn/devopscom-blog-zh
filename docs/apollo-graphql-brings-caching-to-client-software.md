# Apollo GraphQL 为客户端软件带来了缓存

> 原文：<https://devops.com/apollo-graphql-brings-caching-to-client-software/>

Apollo GraphQL 本周[更新了其同名的 GraphQL 客户端软件](https://www.apollographql.com/blog/announcing-the-release-of-apollo-client-3-0/?mc_cid=e593721cc7&mc_eid=4e4f820c6a)，该软件使用内存缓存应用编程接口(API)来提高性能。

GraphQL 已经成为 REST APIs 的流行替代品，因为它为开发人员提供了一个查询引擎，可以更好地控制所请求的数据。与 SQL 的概念相似，开发人员 GraphQL 也使开发人员能够描述他们通过 API 公开的数据。

最后，GraphQL APIs 是根据类型和字段而不是端点来组织的。这使得开发人员可以在一个图形中组织 API，使它们可以通过单个请求获得，而不是要求 API 之间的每次通信都以点对点的方式进行。

Apollo GraphQL 已经创建了客户端软件，允许开发人员使用 GraphQL 来查询外部数据，以及使用图形来对应用程序前端可用的服务进行分类。

Apollo GraphQL 客户端软件的 3.0 版本解决了一个缓存限制，该限制源于通用 HTTP 缓存不能与 GraphQL 一起工作这一事实。每次对稍有不同的数据发出 HTTP 请求时，缓存的值都会失效。当 Apollo GraphQL 客户端从您的服务器获取数据时，它使用与 Apollo GraphQL 模式相匹配的规范化结构缓存数据，这允许它在本地重建后端数据图的子集。下次 Apollo 客户机查询任何相同的数据时，它可以直接从缓存中获取。

开发人员现在还可以为出现在缓存中的任何 GraphQL 字段定义字段策略。字段策略可以包括一个 read 函数和一个 merge 函数，前者定制从缓存中读取字段时发生的事情，后者定制写入字段时发生的事情。

Apollo Graph CTO Matt DeBergalis 表示，通过在一个地方定义所有这些自定义字段逻辑，开发人员可以避免重复代码。他说，其他开发人员也可以与类型和字段进行交互，而不需要了解它们是如何存储或获取的。

Apollo 客户端库 3.0 版现在还支持一个反应变量值，它在读取时注册一个依赖项。

最初由脸书开发的 GraphQL 在后端系统上获得了很大的吸引力，因为它允许开发人员描述可以访问的数据。然而，因为它也使得查询数据更有效，所以它现在也更广泛地部署在客户机上。目前还不清楚 GraphQL 会在多大程度上取代 REST API，但至少在新的应用程序开发项目中对 REST API 的依赖可能会显著下降。

这种转变对于 DevOps 团队来说意义重大，因为与 REST APIs 相比，依赖 GraphQL 的应用程序的整体性能应该会有很大的提高。事实上，目前 GraphQL 采用的最大阻碍可能是简单的惰性。太多的开发人员只是反射性地构建 REST APIs，而没有必要调查替代方案。然而，用不了多久，DevOps 团队中的每个人都会开始意识到，当使用 GraphQL 时，最终用户体验到底有多好。