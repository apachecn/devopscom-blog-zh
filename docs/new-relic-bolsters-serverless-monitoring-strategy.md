# 新遗迹支持无服务器监控策略

> 原文：<https://devops.com/new-relic-bolsters-serverless-monitoring-strategy/>

New Relic 通过[收购 IOpipe](https://blog.newrelic.com/product-news/iopipe/) 加强了其监控无服务器计算框架的能力，IOpipe 是亚马逊网络服务(AWS)提供的无服务器计算框架服务的监控工具提供商。

New Relic 的无服务器和新兴云服务总经理 Andrew Tunall 表示，IOpipe 的监控技术将用于增强今年早些时候推出的 New Relic One 平台中包含的 AWS Lambda 监控工具。

图纳尔说，New Relic 还计划根据客户需求将其无服务器计算的可观测能力扩展到其他平台。

无服务器计算框架越来越受欢迎，因为它们允许开发人员在其应用程序中编写更少的代码，允许他们使用功能调用云服务来处理，例如，外部分析而不是应用程序本身。从 DevOps 的角度来看，无服务器计算框架带来的挑战是它们不创建任何可分析的日志。相反，监控工具需要能够使用分布式跟踪工具来分析无服务器计算框架基于事件驱动架构创建的元数据流。这一需求迫使监控工具提供商扩展其核心平台的功能，以支持元数据的消费。

![](img/4d4ca74c06f5e051b6efbd94712b8a66.png)

无服务器计算框架的采用已经超过了许多 DevOps 团队的观察能力。据 AWS 称，成千上万的客户已经在一个月内对 AWS Lambda 进行了数万亿次调用。Gartner 预测，到 2023 年，100%使用 IaaS 或公共云的企业还将在生产应用程序中使用某种形式的无服务器平台即服务(PaaS)功能，高于 2019 年的 25%。在大多数情况下，这些无服务器计算框架将用于处理无状态工作负载，而有状态工作负载继续在虚拟机或容器中运行。

虽然迄今为止无服务器计算框架的大部分使用是在公共云上，但组织越来越多地在内部 it 环境中使用多种无服务器计算框架只是时间问题。已经有十几种不同类型的无服务器计算框架，其中大部分都是开源项目。

自然，无服务器计算框架的兴起使 DevOps 变得更加复杂。DevOps 团队现在需要构建、部署和更新频繁调用外部应用程序编程接口(API)的应用程序，这些应用程序可能会调用多个无服务器计算框架。与其要求组织购买单独的工具来监控无服务器计算框架， [New Relic 正在为扩展单个平台](https://devops.com/new-relic-extends-observability-reach-and-scope/)来监控所有正在使用的各种类型的 IT 平台创造条件。

几乎毫无疑问，大多数组织最终都会以这样或那样的方式调用无服务器计算框架，但是现在说无服务器计算框架会有多普及还为时过早。然而，开发运维团队需要监控这些无服务器计算框架，以及在日益多样化的 IT 环境中已经采用的所有其他平台。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)