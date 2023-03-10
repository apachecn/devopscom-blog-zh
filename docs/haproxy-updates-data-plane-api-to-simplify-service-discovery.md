# HAProxy 更新数据平面 API 以简化服务发现

> 原文：<https://devops.com/haproxy-updates-data-plane-api-to-simplify-service-discovery/>

HAProxy 更新了开源 HAProxy 数据平面[应用程序编程接口](https://devops.com/?s=API) (API)以包括服务发现功能以及对 HashiCorp 正在开发的 Consul 服务网格的本地支持。

[ha proxy 数据平面 API 的 2.2 版本](https://www.haproxy.com/blog/announcing-haproxy-data-plane-api-2-2/)还为其流处理卸载引擎(SPOE)增加了对文件处理、SSL 证书、映射文件和配置文件的支持。

HAProxy 最出名的是由 DevOps 团队广泛部署的开源[负载平衡](https://devops.com/?s=load%20balancing)软件。作为该平台的扩展，HAProxy Data Plane 可以动态添加和配置前端和后端，然后在它们之间路由应用流量。

HAProxy 的产品和营销总监 Daniel Corbett 表示，HAProxy 负载平衡软件与数据平面相结合，允许 IT 组织创建一个网关，通过该网关他们可以管理他们的 API。

Corbett 表示，该公司目前正在推出一套产品，称为 HAProxyOne，是其负载平衡软件的扩展，并为其产品组合添加了控制平面和服务网格。该公司已经在其产品组合中增加了一个 Kubernetes 入口控制器。

然而，与此同时，HAProxy 数据平面将使 DevOps 团队更容易在 HAProxy 开发的控制平面内集成其他产品，如 Consul，Corbett 说。

Corbett 说，总的来说，HAProxy 将提供一套工具，通过这些工具，DevOps 团队将能够更容易地管理跨多个平台的 IT 环境中的应用程序交付。

HAProxy 并不是唯一一家有类似雄心的负载平衡软件提供商。Corbett 说，HAProxy 要解决的问题是需要一个能够同样适用于单片应用程序和基于微服务的应用程序的框架。

2021 年，一场争夺基础设施控制权的大战正在酝酿，DevOps 团队利用基础设施大规模部署应用。除了代理服务器和负载平衡软件，IT 组织也开始使用 API 网关、服务网格和入口控制器，因为数据流经的 API 数量迅速增加。实际上，这些技术提供了在组成分布式计算环境的应用程序之间路由数据所需的连接基础设施。

然而，现在还为时过早，因为支持竞争性开源项目的人正在为开发人员的心灵和思想辩护。然而，考虑到这些决策可能对 IT 运营产生的深远影响，许多组织可能很快会标准化一套产品以最大限度地降低复杂性。

无论结果如何，实际上，应用程序环境正变得越来越复杂。IT 组织将很快发现自己在运行大量基于微服务的应用程序的同时，也在运行单一的应用程序，所有这些应用程序都需要使用 API 来相互集成。今天做出的关于如何最好地集成这些 API 的决定将对未来几年产生深远的影响。