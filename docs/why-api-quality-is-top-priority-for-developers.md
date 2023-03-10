# 为什么 API 质量是开发者的头等大事

> 原文：<https://devops.com/why-api-quality-is-top-priority-for-developers/>

众所周知，web APIs 对现代企业的运营越来越重要。根据 RapidAPI 的开发者调查和洞察报告，61%的开发者在 2020 年使用了比 2019 年更多的 API，其中 71%计划在 2021 年使用更多。我们不再局限于少数几家单一的服务提供商。企业倾向于使用专门的托管服务，比如由 API 支持的计费和认证。新产品和服务的业务模型是基于 API 构建的。信任已经成为 API 的必需品。性能稳定且高质量的 API 会赢得信任，而性能不稳定的 API 会被竞争对手抛弃。

## 为什么质量很重要？

如果一个 API 存在市场，那么竞争是必然的。为了保持竞争力，API 必须建立并保持消费者的信任；销售和营销只能到此为止。最高质量的 API 必然会获得最大的市场份额。质量也不是目的地——它是需要持续投资的目标的集合。

## 质量对一个 API 意味着什么？

就像驱动 API 的代码一样，API 本身的质量是可以量化的。以下几个方面描述了用于衡量 API 质量的一些主要类别。每个方面的权重将根据 API 在生产中的业务关键程度而有所不同。

**富有弹性。**当原料药在不利条件下继续运行时，它是有弹性的。如果数据库停机，API 还能继续运行吗(即使容量减少)？它如何处理网络流量峰值？

**健壮。一个健壮的 API 在接受什么方面是自由的，但在发送什么方面是保守的。当出现一个格式不良的请求时，它会崩溃吗？还是会给出调用者如何自己解决问题的指示？可以在不破坏 API 契约的情况下重构代码吗？**

**安全。**在大多数部署中，API 安全性至关重要。是否努力检查 [OWASP 十大 Web 应用](https://owasp.org/www-project-top-ten/)的安全风险？开源漏洞是否已知并得到及时解决？安全端点是否通过身份验证进行控制？

**可发现的。**文档完善、结构良好的 API 更容易使用，也更容易与其他服务集成。

**一致。**一致的 API 是一种不会对现有消费者产生负面影响的 API。随着新功能的引入，更改是向后兼容的或版本化的。API 消费者应该提前很久就知道，如果无法避免的话，一个突破性的改变是否会到来。

## 我如何到达那里？

流程、工具，最重要的是文化，是高质量 API 的关键。让我们探索一下如何处理每个 API 质量方面。

**富有弹性。**混沌工程、负载测试和人工质量保证等流程可以发现 API 无法处理意外情况的情况。将您的 API 部署到具有令人信服的 SLA 的云提供商，而不是您自己的硬件和网络，将基础架构弹性的负担转移到服务上，让您有时间为客户构建功能。

**健壮。一套全面的自动化测试并不总是足以提供一个健壮的 API。编写测试套件时没有考虑到的请求可能会触发边缘情况、意外的代码分支和其他计划外的行为。传统的自动化测试应该辅以模糊测试，以帮助发现隐藏的执行路径。淡黄色和蓝绿色的部署可以以有限的方式进一步将您的 API 暴露给现实世界，并为更多意想不到的请求的到来做好准备。**

**安全。** API 安全是一个移动的目标。预计大多数 API 都建立在开源库和框架的基础上。软件组成分析是通过在发现易受攻击的依赖关系时立即识别它们来保持零日漏洞的必要条件。OWASP 指南是必备的——指导 API 开发人员实施攻击缓解策略，如 CORS 和 CSRF 防护。应用程序逻辑必须经过良好的授权和认证测试。

**可发现的。**对于[REST API](https://devops.com/?s=APIs)，OpenAPI 倡议为描述 API 提供了一致的语言。许多框架，比如 Spring Boot，甚至可以直接从你的代码中生成 OpenAPI 文档。基于 gRPC 的 API 提供了类似的好处，它既提供了访问 API 的指令，又构建了与 API 通信的客户机。添加对 GraphQL 的支持允许开发人员用一致的工具将多个 API 连接在一起。无论您选择哪个方向，保持 API 文档的最新和可访问性是至关重要的。

**一致。**为了保持一致，API 开发过程应该使不兼容的变更变得明显。代码评审可以在源代码中捕捉到许多突破性的变化。作为构建的一部分，API 契约测试和集成测试可用于发现 API 变更。当在微服务环境中工作时，如果 API 更改会在生产前导致问题，暂存环境可能会提醒工程师。

## 质量建立信任

根据 RapidAPI 的调查，58%的高管表示参与 API 经济是他们组织的首要任务。在电信等特定行业，这一数字甚至更高，达到 89%。无论你构建的 API 是供内部使用还是供公众使用，你的目标都应该是赢得 API 消费者的信任。投资于构建高质量 API 的文化、工具和流程，将为建立和维护这种信任铺平道路。