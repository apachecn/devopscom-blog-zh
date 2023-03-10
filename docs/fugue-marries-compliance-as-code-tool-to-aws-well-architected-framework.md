# Fugue 将代码合规工具与 AWS 架构良好的框架结合起来

> 原文：<https://devops.com/fugue-marries-compliance-as-code-tool-to-aws-well-architected-framework/>

Fugue 将亚马逊网络服务(AWS)定义的最佳实践融入其软件即服务(SaaS)产品中，使用其基础设施即代码(IaC)平台提供基础设施。

Fugue 首席执行官 Josh Stella 表示，IT 团队现在可以评估使用 AWS CloudFormation 或 Terraform 工具创建的 AWS 基础设施配置模板，以确保它们符合 AWS 良好架构的框架。

AWS 架构良好的框架跨越了 AWS 为在云中设计和运行可靠、安全、高效且经济实惠的系统而定义的五大支柱。AWS 为每个支柱定义了一套最佳实践，并通过提供额外的云积分来奖励遵循这些实践的组织。目标是通过提供指导来提高整体[云安全](https://devops.com/?s=cloud+security)，最终减少错误配置的数量，使网络犯罪分子无法发现和利用它们。

![](img/f51cb1431278ef3d19804fddd895c062.png)

Fugue 平台是对这一努力的补充，因为它基于开放策略代理(OPA)，这是一种在云本地计算基金会(CNCF)的支持下推进的用于管理代码合规性的通用引擎。Fugue 通过创建 Regula 扩展了 OPA，Regula 是一个开源工具，用于评估 IaC 文件的潜在安全性和合规性违规。然后，Fugue 创建了一个 SaaS 平台，该平台广泛使用 AWS Lambda 无服务器计算平台，使其更容易执行合规政策。

这些政策包括针对 SOC 2、NIST 800-53、GDPR、PCI、HIPAA、ISO 27001、CSA CCM、CIS Controls、CIS Docker 和 CIS Foundations 基准测试(适用于 AWS、Microsoft Azure、Google Cloud 和 Kubernetes)等规范的交钥匙服务。

Stella 说，Fugue 现在已经整合了 AWS 架构良好的框架的技术方面。然而，仍然要由每个 it 团队来导航 AWS 等云服务提供商遵循的合规性和安全性的[共享责任模型](https://devops.com/mastering-the-shared-responsibility-model/)的文化方面。

不幸的是，使用 IaC 工具来提供云基础设施的开发人员经常对云服务提供商维护的安全级别做出一些错误的假设。结果通常是大量的安全性和遵从性问题，这主要是因为大多数开发人员在这两个领域都没有很多领域知识。

目前还不清楚有多少组织已经采用了 AWS 架构良好的框架，但是随着各种工具使实现 AWS 定义的这些最佳实践变得更加容易，云计算环境应该变得更加安全和高效。事实上，在许多情况下，这些工具被嵌入到跨多个云实现的更大的 DevSecOps 最佳实践集合中。

Stella 说，他怀疑在适用于多种云的安全性和合规性框架方面是否会有任何标准化；然而，很明显，云服务提供商至少在制造一些可以互相借鉴概念的可用框架。

无论采用哪种方法，随着更多护栏的自动实施，云安全和合规性的整体状态将继续改善。接下来的问题不仅是找到一种方法来确保云基础架构在部署时是安全的，还包括确定目前所依赖的基础架构中有多少是不安全的。