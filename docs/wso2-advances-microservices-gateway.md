# WSO2 推进微服务网关

> 原文：<https://devops.com/wso2-advances-microservices-gateway/>

在[开源和软件开发大会](https://conferences.oreilly.com/oscon/oscon-or) (OSCON)上，WSO2 本周宣布，它已经更新了一个开源微服务网关，使得通过单个应用编程接口(API)公开多个微服务成为可能。

此外，[WSO2 API Microgateway](https://www.globenewswire.com/news-release/2019/07/15/1882671/0/en/WSO2-Introduces-WSO2-API-Microgateway-3-0-to-Simplify-Creating-Deploying-and-Securing-APIs-in-Microservice-Environments.html)的 3.0 版本现在包括自动发现微服务并将遗留 API 请求转换为更现代的格式的能力。WSO2 还增加了对 [OpenAPI 规范](https://github.com/OAI/OpenAPI-Specification) (OAS)的支持，以前称为 Swagger，使开发人员更容易合作创建 API，并且将 WSO2 API Microgateway 工具包从运行时中分离出来，以实现更大的可伸缩性和更平滑的升级。

WSO2 产品营销副总裁 Ken Oestreich 表示，WSO2 API Microgateway 旨在加速应用开发的融合，并集成到一个团队中。作为这一努力的一部分，WSO2 一直倡导采用 [Ballerina](https://ballerina.io/) ，这是一种从头开始设计的通用编程语言，旨在使开发人员更容易自行集成分布式应用程序。他说，例如，Ballerina 使开发人员有可能在分布式应用程序中创建和嵌入他们自己的微型企业服务总线(ESB)。

奥斯特里奇补充说，这些集成引擎可以在基于持续集成/持续部署(CI/CD)的任何 DevOps 流程中进行部署和更新。

WSO2 API 微网关设计用于在不到一秒的时间内启动，并提供认证、授权、速率限制、服务组合、发现、转换和分析功能。它旨在与 WSO2 API Manager 集成，后者是一个开源 API 管理平台，可以在内部或云中运行。

![](img/37a40ab97d952b289bc49eaef23dbb10.png)

由于容器的兴起，组织内创建的微服务数量增加，奥斯特里奇指出，现在组织迫切需要找到一种轻量级的方法来构建和管理连接数千个微服务所需的所有 API。WSO2 提供了一个流程图，通过它，组织可以可视化地管理这个过程。作为对容器支持的一部分，WS02 API Gateway 提供了对 Kubernetes 等容器编排工具的内置支持，这使得生成可以直接应用于 Kubernetes 集群的构件成为可能。

如今，各种规模的组织显然都在 API 管理方面苦苦挣扎。理论上，当 API 连接的软件组件更新时，它们应该保持稳定。问题是，每个新的微服务都生成自己的一组 API，不久之后，组织就会发现自己要管理成千上万个相互依赖的 API。删除任何一个 API 都不会导致应用程序崩溃，但是会对性能产生负面影响，因为 API 调用会绕过应用程序进行重新路由。

目前还不清楚大多数组织内部谁负责管理 API。开发人员当然会创建 API。然而，一旦它们被部署到生产环境中，它们的照顾和供给通常会移交给 IT 运营团队。然而，不管是谁，一旦这些 API 被破坏，整个 DevOps 团队很快就会知道。现在的挑战是弄清楚如何使所有这些 API 的管理尽可能自然地成为 DevOps 流程的扩展。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)