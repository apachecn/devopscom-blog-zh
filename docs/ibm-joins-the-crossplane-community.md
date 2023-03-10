# IBM 加入了交叉平面社区

> 原文：<https://devops.com/ibm-joins-the-crossplane-community/>

IBM 加入了 Crossplane 社区，以推进混合云应用平台的开发。

克里斯·贝利、保罗·德托里、约翰·庞佐
2020 年 12 月 15 日出版

Today IBM is pleased to announce that it is joining the [Crossplane community](https://crossplane.io/) and releasing an experimental release of a Crossplane provider for IBM Cloud. This enables IBM Cloud managed resources to be exploited from Crossplane.

## 什么是交叉平面？

Crossplane 是一个云本地计算基金会(CNCF)沙盒项目，提供管理基础设施和资源的能力，包括使用 Kubernetes CRDs 的云托管服务，并得到许多主要供应商的贡献和支持。其中包括微软、阿里巴巴、GitLab 和 Red Hat，以及两年前创立 Crossplane 项目的 Upbound。

一个独特的特性是定义组合来表示资源(如数据库)的能力，并用部署和管理资源实例的一个或多个可插入的提供者来支持这些组合。

这使得创建可跨云提供商移植且仍使用云托管资源的应用程序成为可能:应用程序使用交叉平面组合 CRD 定义资源的部署，例如 PostgreSQL 数据库，然后数据库由配置的提供商创建和控制。

该功能扩展了已经来自 Kubernetes 和 OpenShift 的混合、多云可移植性。您可以将同一个应用程序部署到 Amazon AWS 和 IBM Cloud，在第一种情况下使用 Amazon 关系数据库服务，在第二种情况下使用 PostgreSQL 服务的数据库。这个概念还扩展到混合云场景，使用集群内提供者部署 PostgreSQL 的容器化实例。

![Crossplane architecture](img/ce472a156bed4b36b35c4a4a791c1210.png)

## 混合多云应用

混合、多云战略有可能减少供应商锁定，降低服务中断风险，实现更好的灾难恢复，并提供敏捷性、可扩展性和弹性等核心云优势。企业广泛采用这种方法，35%的 IT 基础设施支出用于私有云，21%用于公共云( [IDC](https://www.idc.com/getdoc.jsp?containerId=US46801420) ，2020)，81%的企业与两家或更多提供商合作( [Gartner](https://www.gartner.com/smarterwithgartner/why-organizations-choose-a-multicloud-strategy/) ，2019)。

然而，要发挥混合云计算战略的全部潜力，需要应用程序的可移植性:

*   将工作负载部署到多个云中，以避免服务中断并实现灾难恢复
*   放置工作负载以满足本地性、安全性、合规性或数据治理要求
*   迁移工作负载作为云采用路线图的一部分

当前的应用程序可移植性问题意味着“一旦应用程序被部署到生产环境中并被企业采用，很少有应用程序会移动”( [Gartner](https://www.gartner.com/smarterwithgartner/4-trends-impacting-cloud-adoption-in-2020) ，2020)。

虽然 Kubernetes 越来越被视为容器化的云原生应用程序的无处不在的应用程序可移植层，但其他应用程序可移植性挑战仍然存在。这是因为任何给定的云平台都超越了 Kubernetes 本身。每个托管的 Kubernetes 服务都提供了一种微妙的不同风格，这是由于它所运行的基础设施实现以及它所提供的供应商特定的功能、服务和 API。无服务器功能、托管服务(如数据库、数据存储和消息服务)、负载平衡和代理服务、身份和访问管理以及可观察性等功能的使用都增加了应用程序可移植性的摩擦和障碍。

Red Hat OpenShift 的使用通过为 Kubernetes 和许多其他服务(如服务网格和无服务器)提供跨混合多云部署的一致层，解决了许多这些问题。Crossplane 将此扩展到更广泛的资源。

## 提高应用程序的可移植性

Crossplane“为您的 Kubernetes 集群增压，使您能够从 kubectl 供应和管理基础设施、服务和应用程序”。本质上，Crossplane 提供了一个发布 Kubernetes CRDs 来管理基础设施和资源的框架。

对于托管服务，这使得发布复合资源类型成为可能，例如 PostgreSQLInstance CRD，应用程序可以使用该复合资源类型来创建、配置和管理 PostgreSQL 数据库的实例。PostgreSQLInstance 资源是一个接口层，由一个或多个提供程序组成，这些提供程序可以管理提供 PostgreSQL 数据库具体实现的基础结构资源。这些具体的实现可以是运行在集群中的托管服务，在亚马逊 AWS、微软 Azure、谷歌云平台、阿里云以及现在的 IBM Cloud 上。

虽然托管服务是提高应用程序可移植性的关键，但 Crossplane 可用于部署和管理广泛的资源，包括用于配置集群本身，例如在混合的多云管理场景中。

## 用于交叉平面的 IBM 云提供商

IBM 刚刚发布了一个用于 Crossplane 的 IBM Cloud provider 的实验版本。这提供了一组定制资源定义(CRD)和控制器，以便从交叉平面控制平面提供和管理 IBM 云基础设施和服务。

该提供商目前提供以下功能:

*   从 IBM Cloud Catalog 中调配和管理 85 个以上的托管服务及其凭据
*   将现有的 IBM 云服务导入提供者
*   使用 Go 模板为应用程序的需求创建凭证。

在接下来的几周里，我们将寻求使用额外的 IBM Cloud APIs(包括 IBM Cloud Databases 和 IAM)来增强提供商，并使用来自 IBM Cloud Services 的 OpenAPI 规范的代码生成来维护提供商的 API 兼容性。

[访问 GitHub](https://github.com/crossplane-contrib/provider-ibm-cloud) 在 Crossplane Contributions 组织中找到 IBM 云提供商。

#### 有关系的