# AWS 在峰会上推进 DevOps 议程

> 原文：<https://devops.com/aws-advances-devops-agenda-at-summit-event/>

亚马逊网络服务公司(AWS)在其云平台中增加了旨在自动创建虚拟专用云(VPC)的服务，并提供了额外的工具来构建应用程序和集成外部数据。

首席技术官沃纳·威格尔在 AWS 峰会上表示，这些最新的服务是自动化开发运维流程的持续努力的一部分，开发人员只需编写运行在 AWS 公共云之上的业务逻辑代码。

该公司为实现这一目标而推出的最新工具之一是[AWS Cloud Development Kit](https://aws.amazon.com/blogs/aws/aws-cloud-development-kit-cdk-typescript-and-python-are-now-generally-available/?)(CDK)，这是一个软件开发框架，用于以代码形式定义云基础设施，并通过 AWS CloudFormation 提供它。AWS CDK 目前支持 TypeScript、JavaScript 和 Python，并支持 C#/。预览版中提供了. NET 和 Java。沃格尔斯说，这种能力将消除仅仅为了在 AWS 上运行 VPC 而使用不同工具编写低级代码的需要。

AWS CDK 还允许组织设计和组合他们自己的定制组件，用于管理基础设施和他们的应用程序代码。

![](img/d87f3dfd597270a7fc11656fd4869805.png)

云服务提供商还宣布了 [AWS EventBridge](https://aws.amazon.com/blogs/aws/amazon-eventbridge-event-driven-aws-integration-for-your-saas-applications/) ，这是一个可编程的事件总线，用于在任何基于无服务器计算框架的平台上集成 AWS 上的数据和驻留在软件即服务(SaaS)应用程序中的数据，以及 AWS Toolkit for Visual Studio Code 的全面上市，这是微软集成开发环境(IDE)的一个插件，可以更容易地在 AWS 上构建、调试和部署代码。

最后，该公司宣布[亚马逊 CloudWatch Container Insights](https://aws.amazon.com/about-aws/whats-new/2019/07/introducing-container-insights-for-ecs-and-aws-fargate-in-preview/) 现已推出预览版。该产品提供了对自动化仪表板的访问，这些仪表板按任务汇总了 Amazon 弹性容器服务(ECS)和 Fargate 集群的性能和运行状况。这些产品紧随 [AWS Fluent Bit](https://aws.amazon.com/blogs/opensource/centralized-container-logging-fluent-bit/) 之后，这是一款用于集装箱记录的工具，将于本周早些时候上市。

沃格尔斯强调，在云时代，应用程序的构建方式已经发生了根本的变化。开发人员正在更多地使用容器和无服务器计算框架。他说，容器面临的挑战是，在没有云服务提供商来管理环境的情况下，底层中间件和基础设施的复杂性共同减少了开发人员花在编写实际应用程序代码上的时间。

沃格尔斯解释说，为了解决这个问题，AWS 正在加大对容器和 Kubernetes 服务以及按需无服务器计算服务的投资，如 AWS EventBridge，这些服务不需要组织为闲置进程付费。

总的来说，沃格尔斯表示，AWS 继续倡导消除独立的 IT 运营和网络安全团队，支持利用 AWS 提供的自动化服务的更统一的方法，例如，确保整个持续集成/持续部署(CI/CD)平台的安全。然而，尽管采用 best DevOps 和 DevSecOps 流程的组织数量持续稳定增长，但在对多种云的依赖也持续稳定增长的情况下，有多少组织会在单个云平台上标准化这些流程还不太清楚。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)