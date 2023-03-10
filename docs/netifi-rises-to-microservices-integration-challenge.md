# Netifi 迎接微服务集成挑战

> 原文：<https://devops.com/netifi-rises-to-microservices-integration-challenge/>

Netifi 本周推出了基于开源 RSocket 通信协议的集成平台，以取代 HTTP ad REST 应用编程接口(API)作为连接微服务的机制。 [RSocket](https://github.com/rsocket/rsocket) 最初由网飞创建，现在正通过 Netifi、脸书和 Pivotal Software 的贡献得到加强，用于企业 IT 组织。

刚刚筹集了 200 万美元的种子资金，Netifi 还承诺在今年晚些时候支持 RSocket 的社区版。

公司首席执行官罗伯特·罗瑟(Robert Roeser)表示，Netifi 平台旨在使构建微服务和互连微服务变得更容易。大多数微服务都是使用 Docker 容器构建的，但 Roeser 表示，作为多语言集成方法的一部分，Netifi 正在利用 RSocket 连接使用各种运行时构建的微服务，并提供对遗留单片应用程序的访问。Netifi 平台可以部署在内部、公共云中或以混合方式部署。![](img/92505b0954829f99712bcd3e5831073e.png)

Roeser 说 RSocket 是网飞的必然产物，因为需要大规模互联的微服务数量对于使用 HTTP 和 REST APIs 的任务来说太复杂了。不久之后，脸书也开始使用 RSocket，现在 Netifi 和 Pivotal 正在做出贡献，旨在使 Rocket 更易于传统企业开发人员使用。他说，就 Netifi 而言，这意味着提供发现和宣传微服务的机制，并提供一个抽象层，使开发人员免受网络底层复杂性的影响。

随着基于微服务的应用变得越来越广泛，企业组织往往越来越害怕与大规模管理它们相关的挑战。传统的企业 IT 组织无法获得一小群软件工程师来解决这个问题。结果，他们中的许多人退回到构建单片应用程序，其中所有需要访问的服务都被嵌入到应用程序本身中。Roeser 说，他们通常会牺牲规模和灵活性，以支持一个对他们来说既熟悉又容易导航的结构。

Netifi 和 RSocket 的其他支持者将面临的挑战是围绕 REST APIs 和 HTTP 的大量惰性。几代开发人员现在认为 REST APIs 是将各种应用程序连接在一起的默认机制。他们中的许多人需要考虑的问题是，微服务的兴起会在多大程度上打破这种集成结构。从 REST APIs 的转移也可能对服务如何对外公开、管道如何在 DevOps 环境中构建以及其他因素产生重大影响。

基于 RSocket 或其他方法的集成平台最终是否会让企业 It 组织更容易获得微服务还有待观察。但是，目前正在投入大量资源来解决这个问题，其中许多资源利用了网飞和脸书等公司的贡献，这些公司已经依赖数千个微服务来提供广泛的云原生应用程序。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)