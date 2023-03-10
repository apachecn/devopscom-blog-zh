# IBM 将云代工厂 PaaS 加入私有云

> 原文：<https://devops.com/ibm-adds-cloud-foundry-paas-cloud-private/>

随着 IT 组织被要求调配和支持越来越多的平台，他们越来越需要一种尽可能消除复杂性的方法。考虑到这个目标，IBM 创建了 IBM Cloud Private，这是一个基于 Kubernetes 容器编排软件的本地平台，可以自动部署私有云。本周，IBM 宣布将 IBM Cloud Private 的范围扩展到包括对开源 Cloud Foundry 平台即服务(PaaS)环境的支持。

IBM Cloud Private 旨在部署在虚拟或物理服务器之上，包括基于 Nutanix 软件的超融合基础设施实例。IBM Cloud Private 的杰出工程师 Michael Elder 表示，IBM 已经开发了一些工具，不仅可以自动供应底层基础设施，还可以自动供应 IBM 中间件的容器化和遗留版本，如 IBM DB2 数据库、WebSphere application server 的 Open Liberty Edition 和 IBM Microservice Builder。此外，Elder 说 IBM Cloud Private 可以用来部署各种开源数据库，包括 MongoDB 和 PostgreSQL。

IBM Cloud Private 还提供了大量的 DevOps 工具，包括 APM、Netcool、UrbanCode、Cloud Brokerage、Jenkins、Prometheus、Grafana 和 ElasticSearch。Elder 说，无论采用何种平台，IT 组织都应该能够应用一套一致的 DevOps 流程来管理 Kubernetes 或 Cloud Foundry。

IBM 还通过包括安全漏洞顾问来扫描容器和加密传输中的所有数据的能力来解决安全问题。

Elder 表示，许多 IT 组织将在 PaaS 环境中部署 12 因素应用程序，以及在 Kubernetes 上运行的容器化应用程序。IBM Cloud Private 旨在为管理这两种环境提供一个通用的管理框架。然而，IBM 没有将该管理框架扩展到 IBM 公共云。Elder 表示，该公司认为，试图为两者创建一个通用的管理框架会导致太多的复杂性，特别是对于需要更加简化的用户界面体验的公共云服务管理员来说。

当然，大多数 IT 组织都可以打造自己的私有云。IBM Cloud Private 通过提供通用管理框架下所需的所有部分来简化这一过程。IBM 没有花几个月的时间将这些元素组合在一起，而是提出了一个集成平台，使 IT 组织能够将更多的精力集中在部署应用程序上，而不是管理基础架构。

现在整个 IT 行业都在争论基于 Kubernetes 的容器即服务(CaaS)环境会在多大程度上取代传统的 PaaS 环境。作为 Kubernetes 和 Cloud Foundry 的主要支持者，IBM 显然认为两者都有发展空间。最近， [Cloud Foundry Foundation 通过增加对 Kubernetes 运行时](https://containerjournal.com/2017/10/11/cloud-foundry-embraces-kubernetes-runtime-environment/)的支持，进一步推进了这一目标。

然而，到目前为止，建立 PaaS 环境的复杂性限制了 Cloud Foundry 在财富 1000 强 IT 组织或云服务提供商中的采用。与此同时，基于 Kubernetes 的 CaaS 环境越来越多地由开发人员建立，然后移交给 IT 运营部门管理。考虑到部署模式的差异，用不了多久，CaaS 环境的数量就会超过传统 PaaS 环境的实例数量。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)