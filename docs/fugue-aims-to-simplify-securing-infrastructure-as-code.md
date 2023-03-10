# Fugue 旨在简化代码基础设施的安全保护

> 原文：<https://devops.com/fugue-aims-to-simplify-securing-infrastructure-as-code/>

Fugue 今天发布了 Regula 的 1.0 版本，这是一个针对基础设施即代码( [IaC](https://devops.com/?s=IaC) )安全的开源策略引擎，带有预构建的库，用于实施数百个策略，这些策略在亚马逊网络服务(AWS)、微软 Azure 和谷歌云服务上验证配置。

Regula 基于开放策略代理(OPA)软件，该软件是在云本地计算基金会(CNCF)的支持下开发的，并且与用于配置云基础设施的 Terraform 和 AWS CloudFormation 工具兼容。

开发人员也可以在 OPA 的基础上使用 Fugue 为减压阀编程语言创建的库来构建自定义规则，这些库是 OPA 规范的一部分。Regula 支持输出格式，如 JUnit、Test Anything Protocol (TAP)和 JSON，以便更容易将 Regula 与构成 DevOps 工作流的其他工具和框架集成。支持的输入格式包括 Terraform HCL、Terraform plan JSON、AWS CloudFormation 和无服务器应用模型模板。

除了 Fugue 定义的其他策略之外，Regula 还为 CIS Foundations 基准提供现成的支持，如危险许可身份访问管理(IAM)策略、允许全局访问的 Lambda 函数策略、禁用加密的卷和未标记的云资源。

它被部署为一个预打包的二进制文件，包括一个命令行界面(CLI ),通过它可以将 Regula 集成到 DevOps 工作流中，并且可以使用 Homebrew 等工具进行安装，或者部署为 Docker 映像。

Fugue 首席执行官 Josh Stella 表示，Regula 为 DevOps 团队提供了一个广泛的规则库，用于检查常见的安全和合规违规行为以及高级的多资源错误配置。后一个问题尤其具有挑战性，因为开发人员通常不太了解依赖关系，这些依赖关系可能会无意中为网络犯罪分子提供对 S3 云存储桶的访问，而该存储桶看起来配置正确。Stella 补充说，Regula 还将识别任何可能缺失的所需资源。

Stella 说，Regula 1.0 提供了一种更简单的方法来保护云基础设施。仅仅因为开发人员犯了一个错误，云基础设施就经常被错误配置。Stella 指出，不幸的是，网络罪犯已经变得特别擅长扫描云平台来寻找这些错误配置。

目前还不清楚，在最近软件供应链受到高调破坏后，对 IaC 的反弹可能会达到什么程度。组织已经采用 IaC 工具来提高开发人员的工作效率。然而，每个涉及云基础设施资源配置错误的安全事件都表明，开发人员缺乏安全配置 it 环境所需的专业知识。Stella 说，Fugue 没有创建一系列会降低开发人员生产力的网络安全审查，而是提出了一种开发人员易于理解和实施的代码合规性方法。

无论如何，云基础设施必须变得更加安全。企业领导人越来越厌倦安全事故，在他们看来，这些事故是由粗心大意的错误造成的。他们的第一反应是授权网络安全团队一劳永逸地解决这些问题。现在唯一需要解决的问题是，如果为开发人员提供保护云平台本身所需的工具，这些安全审查会有多麻烦。