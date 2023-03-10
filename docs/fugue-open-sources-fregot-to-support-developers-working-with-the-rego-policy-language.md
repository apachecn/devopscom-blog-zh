# 河豚开源 Fregot 支持开发者使用减压阀政策语言

> 原文：<https://devops.com/fugue-open-sources-fregot-to-support-developers-working-with-the-rego-policy-language/>

**马里兰州弗雷德里克(Frederick)，2019 年 11 月 14 日—**[赋格](https://www.fugue.co/)，这家让工程师能够构建和运行符合企业政策的安全云系统的公司，今天宣布开源[赋格减压阀工具包(Fregot)](https://github.com/fugue/fregot) ，以增强使用减压阀政策语言的体验。Fregot 使开发人员能够轻松评估减压阀表达式、调试代码和测试策略。减压阀是开放策略代理(OPA)策略引擎的一部分，Fugue [今年](https://www.fugue.co/press/releases/fugue-adopts-open-policy-agent-opa-for-its-policy-as-code-framework-for-cloud-security)采用该引擎作为其策略，作为云安全和合规性的代码实现。

Fregot 是作为开放策略代理(OPA)内置解释器的替代产品开发的，它提供了易于理解的错误处理，并通过逐步调试来管理。此外，Fregot 通过观察减压阀和输入文件的变化并支持快速增量加载，加快了开发反馈循环。您可以使用 Fregot 根据减压阀策略验证几乎任何类型的 JSON 或 YAML 文件。

Fugue 在内部创建了 Fregot，作为增强减压阀开发体验的轻量级工具集。它提供:

*   仅减压阀语言实现，而不是完整的 OPA 代理
*   调试减压阀查询和模块的有用工具
*   增强的错误消息有助于更正减压阀表达式
*   易于扩展和试验新的语言特性

“富格的云基础设施可见性和安全性 SaaS 产品大规模使用减压阀和 OPA，每天执行超过 1 亿次策略评估，并为我们的客户提供一种简单的方法来创建云基础设施的定制策略，”富格的联合创始人兼首席技术官 Josh Stella 说。“我们开发 Fregot 是为了加快这些评估的实施，并为我们的客户和社区提供有用的工具，以使用减压阀政策语言开发和测试政策。”

Fregot 开源项目可以在 Github 上找到[。](https://github.com/fugue/fregot)

**关于赋格**

神游是由工程师为工程师开发的企业云安全。Fugue 防止云错误配置，确保持续符合企业安全策略，并提供对 AWS 和 Azure 云环境安全状况的全面可见性。Fugue 自动执行 CIS 基础基准、GDPR、HIPAA、NIST ISO 27001 800-53、PCI 和 SOC 2 的合规性验证。PBS、Sparkpost、SAP NS2 和 TrueCar 等客户信任 Fugue 来保护他们的云环境。富歌的投资者包括新企业联合公司、未来基金和 In-Q-Tel (IQT)。Fugue 是 AWS 高级技术合作伙伴，也是 AWS 云管理工具能力计划治理类别的发布合作伙伴。Fugue 曾两次被评为网络安全突破奖获得者和云计算领域的 Gartner Cool 供应商。要了解更多信息，请访问 www.fugue.co。