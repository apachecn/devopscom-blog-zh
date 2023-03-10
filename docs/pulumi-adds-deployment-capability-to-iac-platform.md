# Pulumi 为 IaC 平台增加了部署功能

> 原文：<https://devops.com/pulumi-adds-deployment-capability-to-iac-platform/>

在 [Pulumi 云工程日](https://www.pulumi.com/cloud-engineering-days/)活动上，Pulumi 今天宣布其 Pulumi 云平台增加了代码部署功能，用于管理基础设施即代码(IaC)。

Pulumi 首席执行官 Joe Duffy 表示，Pulumi 部署将使 DevOps 团队能够通过一个 Git commit 提供基础设施和部署应用程序，该 Git commit 可通过应用程序编程接口(API)或图形工具调用。

Git Push to Deploy 功能允许 DevOps 团队连接到任何 Git 存储库，以推动给定项目路径的部署，推动到任何给定分支，并设置[gitop](https://devops.com/?s=GitOps)工作流，如拉式请求审查。除了提供漂移检测和补救功能之外，部署操作还包括更新和销毁。

Pulumi 开发的部署和自动化 API 还使用 Pulumi 提供的模板库支持临时代码审查环境、跨多个云平台的自动清理和部署编排。Duffy 说，实际上，Pulumi 现在正在提供一个开箱即用的 GitOps 工作流。

Pulumi 已经将这些功能与 GitHub 集成在一起，并计划添加对 GitLab、Atlassian Bitbucket 和其他 DevOps 平台的支持。Duffy 说，目标是使 DevOps 团队能够使用 GitOps 工作流有效管理每个工程师十倍于当前依赖 Terraform 等 IaC 工具的云基础设施资源。

![](img/b3bab59ddd1aa515f5038500f69551c3.png)

作为 Terraform 的替代产品，Pulumi 平台越来越受欢迎，因为它可以使用一组嵌入式护栏更轻松地集中管理和配置基础设施。企业 IT 组织目前面临的一个主要问题是，当开发人员使用 Terraform 等工具自行调配基础架构时，会产生大量错误配置。例如，这些错误配置通常会导致端口开放和网络罪犯泄露数据。在一系列引人注目的违规事件发生后，越来越多的组织开始审查其软件供应链的安全性，包括如何通过将策略即代码嵌入开发运维工作流来调配基础架构。

Duffy 补充说，与此同时，在经济衰退期间，组织也对提高开发运维团队的生产力非常感兴趣，因为经济衰退限制了组织可以雇用的 IT 专业人员的数量。

Pulumi 声称其平台现在有超过 500 万用户，遍布 1000 多个组织。不太清楚的是，组织在多大程度上采用 GitOps 工作流来统一 IaC 和应用程序代码的部署。随着平台使这种转变变得更加容易，使用更加固执己见的开发运维方法的组织数量应该会稳步增加。

与此同时，DevOps 团队需要找到更快地构建和部署更安全的应用程序的方法。近年来，人们主要关注的是加速应用程序部署，而很少关注网络安全。那些日子显然即将结束。