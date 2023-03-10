# 8 CI/CD 的安全注意事项

> 原文：<https://devops.com/8-security-considerations-for-ci-cd/>

在软件开发企业中，CI/CD 指的是持续集成和持续交付或持续部署的组合实践。通过在构建、测试和部署应用程序时使用自动化，CI/CD 使组织能够在开发、运营活动和团队之间架起一座桥梁。

您如何在频繁部署的情况下保持质量和安全性？虽然 CI/CD 可以提高组织的效率，但仍有许多安全问题需要考虑。

为了深入了解 CI/CD 的顶级安全考虑，我询问了即将到来的[](https://devopsinstitute.com/cicd-2021/?utm_campaign=SKILup%2520Day-CI-CD-July%25202021&utm_source=DevOps-8-Security-Considerations-for-CI-CD)滑雪日的演讲者和赞助商以及几位 [DevOps Institute 大使](https://www.devopsinstitute.com/about-us/ambassadors/?utm_campaign=Brand%2520Awareness%25202021&utm_source=DevOps-8-Security-Considerations-for-CI/CD) 的想法。以下是他们在这个两部分系列的第一部分中所说的话:

**演讲人、** [**格兰特·弗里奇**](https://www.linkedin.com/in/grant-fritchey/) **、产品宣传员、Redgate 软件**

“谈到 CI/CD，有很多安全考虑因素。作为一个专注于数据和数据管理的人，我要说的是，首要的安全考虑是确保您的非生产环境有合规的数据。光是能够访问这些信息的人数就意味着，如果您暴露了受保护的信息，那么您就有大量可能的泄密途径。”

**演讲人，** [**安德斯·沃格伦**](https://www.linkedin.com/in/anderswallgren/) **，技术战略副总裁，CloudBees**

“保护您的软件交付管道本身，而不仅仅是通过这些管道交付的软件。每个人都应该只拥有履行其职责所需的访问级别。

维护一个软件材料清单(SBOM ),这样你就知道你在生产中有什么。当一个新的漏洞被披露时，如果您不必追踪您在生产中拥有的东西，您将更容易决定是否以及如何减轻它。您的编排软件应该完成这里的大部分工作。"

[**特雷西·拉冈**](https://www.linkedin.com/in/tracy-ragan-oms/) **，CEO 兼联合创始人，DeployHub**

“CI/CD 工具主要由一次性脚本驱动。一次性脚本绝对不安全。从构建到部署，我们需要开始考虑实施自动化和策略驱动的工具，并抛弃一次性脚本。”

[**蒂芙尼**](https://www.linkedin.com/in/tiffanyjachja/) **，技术传道者，线束**

“供应链管理是 CI/CD 的主要安全考虑因素。如果一个实体获得了不应该访问的 CI/CD 资源或组件，这可能会导致漏洞、停机甚至恶意代码。例如，在 2020 年的网络安全管理软件产品黑客事件中，攻击者通过将软件恶意软件注入网络安全管理软件产品的构建过程来使其合法化。这个构建管道在发布给全球 18，000 多个客户之前，生产了可信的软件工件并获得了数字认证。黑客入侵后，网络安全管理软件产品采取了行动，进一步限制对其构建环境的访问，并审查其构建过程，但在此之前为时已晚。这不仅关系到开发人员和运营工作流的自动化，还关系到我们如何对待和处理 CI/CD 渠道。”

[**贾马尔沃什**](https://www.linkedin.com/in/jamalwalsh/) **，技术产品负责人，非常集团**

“您必须确保在管道中实现安全工具；仅仅使用 CI/CD 来构建和部署应用是不够的。流程中的步骤应该包括安全测试工具，如 SAST、DAST、依赖性检查等。”

[**陈**](https://www.linkedin.com/in/martin-chan-86310023/) **，系统分析师，环球行政顾问有限公司**

“最重要的是定义访问控制列表和规则来控制 CI/CD 管道中的访问，以便审核日志可以轻松跟踪问题。此外，系统应该要求验证，并为所有用户定义密码策略。”

[**布莱恩·芬斯特**](https://www.linkedin.com/in/bryan-finster/) **，软件工程师，国防部平台一号**

“安全性必须作为流水线的一部分实现自动化。就像任何其他质量关一样，管道必须是安全真相的唯一来源。代码提交后的任何手动过程都会增加交付的工作量。增加努力会增加每个变化的规模。更大的变化更难检查质量，失败也更引人注目。手动安全只是安全剧场，很容易被绕过或忘记。这项工作最好用于提高管道使用安全即服务的能力。”

[**Dheeraj Nayal**](https://www.linkedin.com/in/dheerajnayal/)**，DevOps Institute 全球社区大使**

“遵循 CI/CD 的三个安全最佳实践。我们通常将安全实践分为三个部分，您可以使用不同种类的解决方案来解决。这些是:

1.  安全管道配置
2.  代码和 Git 历史分析
3.  安全策略实施

这三个方面同等重要。"

如果您想了解 CI/CD 和类似主题的更多最新信息，请查看即将推出的[SKILup Day schedule](https://www.devopsinstitute.com/all-events/?utm_campaign=SKILup%2520Days%25202021%2520%255BGeneral%255D&utm_source=DevOps-8-Security-Considerations-for-CI-CD)。或者，了解更多成为 [DevOps 学会会员](https://devopsinstitute.com/membership?utm_campaign=Paid%2520Membership%2520Launch%2520Campaign&utm_source=DevOps-8-Security-Considerations-for-CI-CD) 的好处。