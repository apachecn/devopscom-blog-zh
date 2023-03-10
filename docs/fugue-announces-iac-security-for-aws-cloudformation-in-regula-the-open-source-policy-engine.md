# 在开源策略引擎 Regula 中，Fugue 宣布为 AWS CloudFormation 提供 IaC 安全

> 原文：<https://devops.com/fugue-announces-iac-security-for-aws-cloudformation-in-regula-the-open-source-policy-engine/>

Regula 在 AWS CloudFormation 和 Terraform 基础设施上执行安全检查，作为 AWS、微软 Azure 和谷歌云环境的代码

马里兰州弗雷德里克——2021 年 5 月 11 日——帮助组织在云中更快、更安全地创新的公司 Fugue 宣布在开源基础设施代码(IaC)策略引擎 Regula 中支持 AWS CloudFormation。云工程和安全团队现在可以在部署之前使用 Regula 来保护他们的 AWS CloudFormation 和 Terraform 配置，并将这些规则应用于使用 Fugue 平台运行的云环境，以保护整个云开发生命周期。自 2015 年以来，扩展 Regula 功能代表了 Fugue 在 IaC 代码政策创新和运行云基础设施方面的持续领先地位。

Regula 非常适合拥有使用 AWS CloudFormation 和 Terraform 的 DevOps 团队的组织，以及那些运营多云环境的组织。Regula 是唯一一个可以解决涉及多个资源的漏洞的 AWS CloudFormation 安全工具，也是唯一一个帮助团队满足 CIS AWS Foundations 基准 1.2.0 和 1.3.0 的工具。Regula 可轻松集成到 CI/CD 管道中，支持预提交 IaC 检查，并提供拉请求反馈。神游提供了 [Regula 为 CI/CD](https://github.com/fugue/regula-action) 使用 GitHub 动作的例子。

Cadwell Industries，Inc .的企业支持专家 Sawyer Ward 表示:“在 Cadwell，我们需要一种有效的方法来检查我们的基础设施代码，以确保我们的云基础设施部署是安全的，这样我们就可以放心地在云中更快地移动。Regula 非常适合我们的基础设施代码安全要求，并且能够使用 Fugue 将这些规则应用到我们的云环境，这意味着我们可以保持我们的基础设施持续合规，并避免维护多个策略框架的风险和开销。”

虽然 Regula 独立于 Fugue 工作，但团队可以使用 Fugue 应用相同的 Regula 规则来评估他们正在运行的 AWS、Azure 和 Google Cloud 云基础架构环境的安全状况，从而消除与针对云开发生命周期的不同阶段和不同云平台使用和协调不同策略框架相关的投资和云风险。

Fugue 联合创始人兼首席执行官 Josh Stella 表示:“在云中大规模运营的公司需要一个灵活的政策代码框架，它可以与领先的基础设施一起作为代码工具，并可以在云开发生命周期的每个阶段跨云平台使用。“通过将 Regula 支持扩展到 AWS CloudFormation，云工程和安全团队现在有了一个统一的云策略框架，可与其工具和工作流配合使用，让他们有信心在云中更快地移动，而不会违反保持云基础架构安全和合规所需的规则。”

Regula 的规则库检查各种各样的云错误配置漏洞，如危险许可的 AWS IAM 策略和安全组规则，未启用“阻止公共访问”选项的 S3 桶，允许全局访问的 Lambda 函数策略，禁用流日志的 VPC，禁用加密的 EBS 卷，以及未标记的云资源。点击查看全套规则[。](https://www.github.com/fugue/regula)

Regula 使用由开放策略代理项目开发的减压阀查询语言支持用户定义的规则，并包括帮助程序库，使用户能够轻松构建符合企业策略的规则。Fugue 创建并开源了 [Fregot](https://github.com/fugue/fregot) ，这是一个让开发者能够轻松评估减压阀表达式、调试代码和测试策略的工具。

Regula 今天可以在 [Fugue 的公共 GitHub 库](https://www.github.com/fugue/regula)和[docker hub](https://hub.docker.com/r/fugue/regula)上获得。

关于赋格

Fugue 帮助组织在云中更快地移动，而不违反保持云环境安全所需的规则。Fugue 平台保护整个云开发生命周期——从作为代码的基础设施到云运行时。Fugue 使云工程和安全团队能够证明持续的合规性，将安全性构建到云开发中，并消除云错误配置。Fugue 支持亚马逊 Web 服务、微软 Azure 和谷歌云，并为 CIS 基础基准、CIS 控制、CIS Docker、CSA CCM、GDPR、HIPAA、NIST 800-53、PCI 和 SOC 2 提供一键报告。美国电话电报公司、SAP NS2 和 Red Ventures 等客户信任 Fugue 来保护他们的云环境。要了解更多信息，请访问 www.fugue.co。