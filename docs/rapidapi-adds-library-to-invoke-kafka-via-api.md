# RapidAPI 添加库以通过 API 调用 Kafka

> 原文：<https://devops.com/rapidapi-adds-library-to-invoke-kafka-via-api/>

RapidAPI 宣布它已经[增加了对开源 Kafka 消息软件](https://rapidapi.com/blog/kafka-api-types-with-rapidapi/)的支持，作为 DevOps 团队可以集中访问的另一种类型的应用编程接口(API)。

RapidAPI 提供了一个开源库，现已推出测试版，可以通过 RapidAPI Marketplace 或 RapidAPI Enterprise Hub 从浏览器中发现 Kafka 集群和主题、查看模式以及测试和使用记录。该库基于 Apache Avro 和在开源汇合模式注册库中找到的汇合线格式。RapidAPI 扩展了这个库，增加了对 JSON 的支持和一个协议缓冲区，现在正与开源 Kafka 社区共享。

RapidAPI 首席执行官 Iddo Gino 表示，DevOps 团队现在可以在同一位置发现所有可用的 Kafka 集群和实例，他们可以在同一位置找到、测试并连接到基于 REST、SOAP 和 GraphQL APIs 的微服务。Gino 指出，这一努力旨在补充一些倡议，如目前正在 Linux 基金会的支持下推进的 AsyncAPI 规范。

![](img/76b834af0e5165ad34bef8d7de01349e.png)

Gino 说，RapidAPI 正在增加这一功能，因为使用 Kafka 实现跨事件驱动应用程序的异步通信已经显著增加。随着新冠肺炎疫情之后数字业务转型计划的数量增加，Gino 表示，依赖 Kafka 等异步消息平台成为一种要求。Gino 补充说，在许多情况下，高度分布式应用程序之间的同步通信根本不可行。

这并不意味着异步需求将取代对传统同步 API 的需求。Gino 指出，相反，随着企业 IT 环境变得更加分散，开发人员会发现他们正在更好地融合两者。Gino 补充说，应用程序越来越成为一个大难题，开发者需要使用各种类型的 API 来构建。

RapidAPI 创建的库预计将在第三季度全面推出。与此同时，对卡夫卡的接受继续加速。在 Apache Software Foundation 的支持下，负责监督 Kafka 开发的开源社区声称，超过 80%的财富 100 强公司正在使用该平台，从构建数据管道到运行流媒体分析应用程序。在某些情况下，数据在传输过程中被直接查询，而不是等待数据存储在本地或云中。

不管 Kafka 是如何使用的，开发人员正在重新发现事件驱动的架构，这种架构可以追溯到 20 世纪 80 年代，用于构建应用程序。现在的区别是有一个开源框架来处理大规模构建和部署这些应用程序所需的异步通信。

随着事件驱动应用程序的构建和部署越来越普遍，事件驱动应用程序的兴起将如何影响 DevOps 工作流尚不清楚。然而，随着 API 在这些应用程序的上下文中被更广泛地使用，合并它们应该变得更简单。

挑战在于，事件驱动的架构通常要求开发人员从不同的角度思考他们的应用程序是如何构建的，因此 Kafka(以及其他类似的平台)在整个企业中广泛使用可能还需要一段时间。