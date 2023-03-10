# 何时一起使用 API 管理和服务网格

> 原文：<https://devops.com/when-to-use-api-management-and-service-mesh-together/>

尽管有时被描述为竞争架构，API 管理和服务网格有[稍微不同的用例](https://devops.com/how-are-api-management-and-service-mesh-different/)，并且实际上可以很好地一起工作。API 管理为面向外部的流量提供业务逻辑，而服务网格擅长处理微服务之间的相互通信。一个组织当然可以在他们的项目中同时采用这两种方法。那么，什么时候同时使用 API 管理*和*服务网格才有意义呢？

我最近和 Red Hat 的产品总监 Mark Cheshire 聊天，讨论了 API 管理和服务网格之间的细微差别。Cheshire 认为，对于特定的用例，API 管理和服务网格可以很好地并行工作。例如，使用服务网格的大型组织可以从应用 API 管理中受益，API 管理将微服务包装在内部部门可用的合同中。或者，API 管理可以帮助公司向外部合作伙伴公开网格中的特定 API。

## 何时将 API 管理与服务网格相结合

假设您已经有了服务网格，那么您还需要 API 管理吗？Cheshire 提出了四个可能影响你决策的问题。

**1。考虑连接的数量和消费者的数量:是多对一还是一对多？**

在一个单一的应用程序中，通信更加集中，更多的是一对一的关系。然而，当您将服务分解为微服务并在整个组织中重用它们时，一个服务现在可能有许多消费者。这是一个很好的迹象，表明您需要一种接口 API 管理方法。

Cheshire 解释说:“当环境变得越来越大时，你不能像平面网格那样管理它。“您需要按照业务线或您可能拥有的职能进行某种组织分组。”

API 管理可以在大型组织的内部团队之间创建更正式的接口，这些团队之间可能很少或根本没有联系。例如，也许客户数据团队需要一种正式的方法来与销售组织联系。或者，支持登录微服务的安全团队可能需要访问会计部门的财务细节。

**2。系统需要什么样的访问控制和限制？**

考虑需要什么样的访问控制来保护您的环境并避免服务中断。服务网格通常使用[零信任方法](https://containerjournal.com/features/zero-trust-architecture-zta-to-secure-a-nation/)，在每个微服务的每个入口应用相互 TLS。API 管理还可以带来认证控制和更高级的授权和流量机制。

API 管理可以为遵循业务逻辑的域间流量应用细粒度控制提供一种简化的方式。这有助于将特定资源的访问权限分配给不同的请求方，例如基本用户的只读访问权限或管理员的更新访问权限。在不断增加的 API 攻击中，围绕您的端点设置精细的 T2 策略和权限变得越来越重要，以避免数据过度暴露。随着更多公共云的使用、[远程工作](https://accelerationeconomy.com/digital-business/the-enterprise-security-paradox-it-freedom-vs-security/)和第三方承包商的出现，外部和内部流量之间的二元关系逐渐消失，这种必要性也随之增加。

API 网关也更加强调通信规则和模式。Cheshire 解释说，例如，速率限制对于避免整个网络崩溃非常重要。除了速率限制之外，过滤、分页和内容协商也是标准的 API 管理功能，可以进一步优化客户端和服务器之间的交换。

**3。您需要服务文档吗？**

Cheshire 解释说，在一个单一的系统中，你可能让所有的开发者共享同一个库。在分布式微服务的内部网络中，这可能仍然是正确的，其中每个微服务都是独立的，但是开发人员仍然可以访问彼此的存储库。当您在一个域内连接服务时，通常只有代码本身(可能还有一些内嵌注释)表示服务之间的契约。

然而，南北交通需要更多的正规化，他说。当一个域与同一公司内的另一个域进行通信时，正式的合同通常是必要的。在这种情况下，关于事物如何工作的部落知识更少。在这种情况下，API 管理非常有用，可以生成一个开发人员门户，其中包含解释方法、请求类型、URL 结构和示例调用的可读文档。这使得没有预先了解该系统的人更容易与它集成。

这种正式的契约通常由一个特定的文件生成，比如 [OpenAPI 规范，](https://www.openapis.org/)，它已经成为描述 REST APIs 的行业标准元数据。团体可以使用 OpenAPI 自动生成文档，甚至驱动规范优先的开发。总而言之，标准化您记录 API 和微服务的方式可以显著改善围绕服务如何连接的知识共享。

**4。互动的本质是什么？**

Cheshire 说，要记住的另一个特征是服务之间交互的性质。他将系统分为两大类:第一类是图模型，其中任何服务都可以连接到任何服务。第二种是分层模型，在这种模型中，南北向的流量使得一个服务可以有多个消费者。分层模型对于产品化和 SaaS 是必要的，因为它创建了对底层资源的单一拦截点。在这里维护层次结构对于保持简单性至关重要，因为您不希望消费者能够访问一个关联图([中的所有私有微服务，除非这是目的](https://devops.com/graphql-as-a-meta-layer/)！).

[API 管理](https://cloud.google.com/blog/products/api-management/got-microservices-service-mesh-management-might-not-be-enough)因此能够在网格上共享 API。Dino Chiesa 和 Greg Kuelgen 在[谷歌云博客](https://cloud.google.com/blog/products/api-management/got-microservices-service-mesh-management-might-not-be-enough)上写道:“虽然他们都使用通信代理，虽然功能上有相似之处，但领域上的差异使他们有所不同，大多数公司将从一起使用它们中看到巨大的好处。”。

## 一起更好

总之，API 管理和服务网格[配合得很好](https://lakwarus.medium.com/api-management-and-service-mesh-are-amazing-together-7b8002c4a4b90)。“这两个是互补的，可以一起工作，”威廉·摩根补充说，首席执行官，浮力。[若阿金·莫雷诺](https://itnext.io/api-management-and-service-mesh-e7f0e686090e)写道，“它们并不相互排斥；我们应该将它们视为基础架构中的不同层。”

具体来说，在以下情况下，将两者结合起来是有益的:

*   在网格上公开和生产 API
*   大型企业网络中服务间通信的形式化
*   应用细粒度的访问控制；基于 API 的微服务的速率限制
*   用更正式的文档标准化服务
*   交互是一种更具层次性的交流模式
*   为合作伙伴提供访问权限
*   当您需要将数据外部化到第三方插件或集成时

Cheshire 说:“API 和服务网格的世界正变得越来越紧密地联系在一起。API 管理不会停止不前——随着开发人员采用新的集成风格，如 Kafka、 [GraphQL](https://devops.com/graphqls-greatest-strength-is-also-its-greatest-weakness/) 和异步格式，解决方案将会不断发展。"它本质上是所有集成点的治理层."

寻求标准化组织内部域间流量的大公司可能会从 API 管理中受益。但是 API 管理也提供了将内部基础设施产品化的可能性。另一个好处是，API 管理网关还可以监控和记录请求，帮助发现外围的参与者，并对事件进行有帮助的记录。

当然，对于某些场景来说，同时采用 API 管理和服务网格可能有些过头了。此外，请记住，引入额外的层必然会增加整体延迟。由开发人员和架构师来[权衡选项](https://devops.com/how-are-api-management-and-service-mesh-different/)并确定什么适合他们独特的环境。为了实现这一点，开放沟通的健康文化很重要，以确保团队在跨部门的相似页面上，避免不匹配的采用，这只会增加[技术债务](https://devops.com/some-technical-debt-is-self-resolving/)。