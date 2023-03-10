# Pulumi 扩展了基础设施即代码的范围

> 原文：<https://devops.com/pulumi-extends-infrastructure-as-code-reach/>

在其在线 [PulumiUP 大会](https://www.pulumi.com/pulumi-up/)上，Pulumi 宣布将向第三方和 DevOps 团队提供其 [Pulumi CrossCode](https://www.businesswire.com/news/home/20220504005408/en/Pulumi-Infrastructure-as-Code-Goes-Universal) 翻译技术。开发这项技术是为了将多种编程语言与其基础设施即代码(IaC)平台集成在一起。

该公司还宣布增加了对 YAML(广泛用于配置 Kubernetes 环境)以及任何 Java 变体的支持。它已经支持。NET、Node.js、Go 和 Python 编程语言。

最后，Pulumi 还为 Oracle Cloud、Databricks 和 EventStore 添加了包，简化了这些平台上的部署。该公司已经为亚马逊网络服务(AWS)、微软 Azure、谷歌云、Kubernetes、Auth0、CloudFlare、Confluent Cloud、Datadog、DigitalOcean、Docker、GitHub、Kong、MinIO、MongoDB Atlas、PagerDuty、雪花、NetApp 的 Spot 和 SumoLogic 提供了类似的集成。现在还有一些组件为容器应用程序、Kubernetes 集群和无服务器应用程序以及 AWS 云开发工具包(CDK)提供支持。

Pulumi 一直在为一种 [IaC](https://devops.com/?s=IaC) 方法提供案例，这种方法使开发人员能够使用他们已经知道的编程语言来提供基础设施，作为部署和掌握 Terraform 等工具的替代方法。

该公司开发的 Pulumi 交叉代码翻译技术现在可供任何想要增加对另一种编程语言的支持的组织使用。它将任何基础设施即代码格式(包括 Terraform、CloudFormation、Azure Resource Manager 和 Kubernetes 配置)转换为 Pulumi 支持的任何编程语言。

Pulumi 首席执行官 Joe Duffy 表示，目标是扩展该公司为简化任何类型的基础设施而创建的翻译技术的整体范围。

Duffy 指出，虽然许多开发人员使用 Terraform 等工具，但限制错误配置的需求正促使许多大型企业重新审视他们的 IaC 方法，以提高软件供应链的安全性。如今，Pulumi 声称已有超过 2，400 家组织采用了支持开发人员提供基础设施和应用护栏政策以减少错误的平台。他补充说，这种方法可以防止开发人员犯配置错误，从而导致数据通过意外打开的端口泄漏。

太多的开发人员认为他们的云服务提供商正在保护底层平台及其配置，但后来发现验证这些配置是他们的责任。与此同时，安全团队无法跟上云基础架构资源调配的速度，因为他们无法在更大的 DevSecOps 工作流环境中应用策略来强制实施调配基础架构的规则。

最终，目标是随着越来越多的组织采用 DevSecOps 最佳实践，采用自动化来一劳永逸地解决这些问题。与此同时，挑战在于如何以一种普通开发人员能够接受的方式来实现。否则，他们将继续以生产效率的名义寻找绕过安全团队的方法，不管底层 IT 环境变得多么不安全。