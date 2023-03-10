# 42Crunch 扩展了与微软的 API 安全联盟

> 原文：<https://devops.com/42crunch-extends-api-security-alliance-with-microsoft/>

42Crunch 本周宣布，它已经[扩展了与微软](https://42crunch.com/42crunch-launches-new-rest-api-static-security-testing-extension-azure-pipelines/)的现有联盟，现在包括对微软 Azure Pipelines 的 REST API 静态安全测试工具的支持。以前，42Crunch 只提供对 Microsoft Visual Studio 集成开发环境(IDE)的支持。

42Crunch 的首席产品和营销官 Dmitry Sotnikov 说，对微软 IDE 的支持假定开发人员将自己进行安全测试。他说，通过将其 API 安全测试工具与微软持续集成/持续交付(CI/CD)平台集成，现在有可能使安全漏洞测试 API 成为 DevOps 过程的一部分。

这种方法意味着组织不必依赖开发人员来记住对他们的 API 进行安全测试。相反，API 的安全测试成为 CI/CD 过程中自动进行的另一个入口，他指出。

应个别客户的要求，该公司已经将其 API 安全测试工具与其他 CI/CD 平台集成在一起。Sotnikov 说，在接下来的几个月里，Crunch 将会使这些集成技术商业化。

随着 IT 组织越来越擅长挫败针对最终用户的攻击，网络犯罪分子现在越来越多地将注意力集中在 API 上。内容交付网络提供商 Akamai 最近报告称，从 2017 年 12 月到 2019 年 11 月，该公司在其客户群中观察到 85，422，079，109 次凭据滥用攻击。[这些攻击中有近 20%，即 16，557，875，875 次，是针对被明确标识为 API 端点的主机名的](https://securityboulevard.com/2020/02/report-attacks-on-financial-services-targeting-apis/)。Sotnikov 指出，这些攻击中有许多涉及到，例如，向 API 调用中意外注入值。

REST API 静态安全测试工具可以在存储库中定位 API 契约文件，并基于 OpenAPI 标准要求、认证、授权和数据验证运行 200 多项安全检查。这确保了在生产中不会部署不符合这些标准的新的或更改的 API。

发现的问题还按影响划分优先级，每个问题都附有一篇知识库文章，解释该问题、其严重性、利用情形以及建议的修复方法。

![](img/cc19d842fc96c47f0028c4c692781f40.png)

Sotnikov 说，REST API 静态安全测试工具为 DevOps 团队提供了一种切实可行的方法来拥抱最佳的 DevSecOps 流程。他指出，今天太多被认为是 DevSecOps 的东西只不过是试图将网络安全问题归咎于开发人员，并补充说，希望以有意义的方式接受 DevSecOps 的组织需要将工具交给 DevOps 团队，使他们能够在发现漏洞并确定优先级后解决漏洞。

在现有开发运维流程的背景下提供这些工具也很重要；索特尼科夫说，否则，开发人员可能会抵制对他们现有工作流程的改变。

DevOps 和网络安全团队将如何融合各自的文化来推动 DevSecOps 还有待观察。网络安全团队可能会继续定义控制措施并发现漏洞。然而，随着 DevOps 团队继续将安全性作为与构建任何应用程序相关的质量保证过程的自然延伸，在应用程序部署到生产中后发现的漏洞数量应该会稳步下降。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)