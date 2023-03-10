# Pivotal 采用 Spinnaker 实现连续交付

> 原文：<https://devops.com/pivotal-embraces-spinnaker-for-continous-delivery/>

Pivotal Software 为开源云代工厂 PaaS 的平台即服务(PaaS)环境添加了对 Spinnaker 连续交付平台的支持。

Pivotal 产品营销副总裁 Richard Seroter 表示,[Pivotal Cloud Foundry](https://content.pivotal.io/blog/pivotal-cloud-foundry-2-6-now-ga-offers-more-ways-to-build-run-and-wire-your-apps)(PCF)的 2.6 版本将网飞开发的 Spinnaker CD 平台扩展到其 PaaS 环境和企业 PKS，这是 Pivotal 及其姐妹公司 VMware 策划的 Kubernetes 的一个实例。

同时，PAS 的最新版本增加了对自定义 sidecar 进程的测试实例的支持，这使得开发人员能够将在隔离容器中运行的附加功能直接嵌入到他们的应用程序中。Seroter 说，这种能力使得在应用程序中部署服务网格成为可能。

![](img/d94d79538641488444e4e2b87aceec1b.png)

最后，Pivotal 计划为 MySQL 数据库添加多中心复制功能，并为 Concourse for PCF 添加一个权限模型，这是一个持续集成工具，用于在 Pivotal CF 环境中构建应用程序管道。Seroter 指出，后一种能力提供了一种机制，通过这种机制，DevOps 团队可以端到端地自动化应用程序更新，包括补丁。他说，随着越来越多的补丁发布，以解决越来越多的涉及利用超线程技术的微处理器的关键缺陷，自动化部署的能力现在比以往任何时候都更加重要。

Pivotal 在其 PaaS 环境中部署了传统的 12 因素应用程序和更现代的容器化应用程序。与此同时，负责监管 Cloud Foundry PaaS 开发的 Cloud Foundry Foundation 已经通过 [Project Eirini](https://www.cloudfoundry.org/project-eirini/) 使得部署依赖于 Kubernetes 而不是为 Cloud Foundry 开发的 Diego orchestration 平台的容器成为可能。然而，Eirini 仍然是一个 alpha 项目，Pivotal 尚未完全承诺对 Kubernetes 的整体 PaaS 战略提供特定级别的支持。

与此同时，Seroter 说，PCF 继续在寻求像技术公司一样构建和部署软件的组织中获得动力。他指出，随着越来越多的组织意识到他们如何依赖软件来推动收入，他们希望依赖一个平台，使他们能够更容易地管理软件开发和部署平台。

作为这项工作的一部分，Pivotal Software 正在积极整合工具，使使用其 PaaS 的组织能够实施最佳开发运维流程。许多企业孤立地采用了各种现代开发平台，但继续依赖云计算平台即服务来自动构建和部署任务关键型应用。现在，两类开发平台正在合并成一个实体，这使得使用轻量级开发平台来拥抱敏捷开发方法变得更加容易。

无论结果如何，PaaS 环境都不会很快消失。然而，随着更多的容器技术被注入到平台中，组织所认为的 PaaS 环境在任何企业中所扮演的角色可能很快就会大大扩展。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)