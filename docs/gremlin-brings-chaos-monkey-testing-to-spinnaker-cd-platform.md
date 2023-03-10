# Gremlin 将混沌猴测试引入 Spinnaker CD 平台

> 原文：<https://devops.com/gremlin-brings-chaos-monkey-testing-to-spinnaker-cd-platform/>

Gremlin 本周宣布，从网飞开发的开源 Spinnaker 项目开始，它将[将其托管的混沌工程服务与连续交付平台相集成。](https://www.businesswire.com/news/home/20190402005098/en/Gremlin-Introduces-“Continuous-Chaos”-Spinnaker-Integration-Helping)

Chaos engineering 的根源可以追溯到弹性测试哲学，该哲学假定应用程序应该能够在任何服务或基础设施故障的情况下保持运行。然而，大多数 IT 组织不具备构建测试弹性所需的工具所需的专业知识，这些工具基于那些随机关闭服务以查看应用程序是否失败的“混乱猴子”原则。

Gremlin 的首席软件工程师 Matt Jacobs 表示，与 Spinnaker 集成的决定是由在更细粒度的级别上将 chaos monkey 弹性测试直接注入应用程序开发和部署管道的需求驱动的。这种能力现在比以往任何时候都更需要，因为随着组织采用微服务来构建下一代云原生应用程序，DevOps 团队根本不可能手动跟踪每个依赖项，他说，添加基于混沌猴原则的弹性测试只是另一种类型的测试，应该作为更大的持续集成/持续交付(CI/CD)平台的一部分自动进行，以确保应用程序不会完全失败。

与一个已经得到谷歌、微软和甲骨文支持的 Spinnaker 项目整合，为实现这一目标提供了最简单的途径。 [Spinnaker 现在也是由阿里巴巴、ancore、Armory、Autodesk、Capital One、CircleCI、CloudBees、DeployHub、GitLab、谷歌、华为、JFrog、网飞、Puppet、Red Hat、SAP 和 Snyk 领导的持续交付基础的核心元素。](https://devops.com/the-linux-foundation-launches-continuous-delivery-foundation/)

![](img/173dfdd1c2b8660c703eb85cd9a74c94.png)

Gremlin 服务通过用户界面访问，有两种形式:免费版和企业版，后者由 Gremlin 提供支持。虽然混沌猴子测试的概念在最高级的 DevOps 实践者中已经存在了一段时间，但是在引入任何可能故意破坏其应用程序的东西时倾向于更加保守的企业 IT 组织将需要大量的指导。Gremlin 被设计成在将应用程序部署到生产环境中之前，以一种受控的方式引入混乱的方式来学习应用程序环境。

雅各布斯说，从积极的一面来看，基于混沌猴原则的弹性测试往往会加快 IT 人员了解应用程序是如何设计的速度。他指出，在培训 DevOps 团队的新成员时，这一点尤其重要。

最终，采用弹性测试的决定取决于组织在防止停机时希望有多主动。当任务关键型应用程序离线时，会对组织的收入产生直接影响。有很多功能和性能测试工具，但是出现问题和发生灾难性事件(需要 DevOps 团队半夜起床)之间的真正区别通常在于任何给定的任务关键型应用程序的真正弹性。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)