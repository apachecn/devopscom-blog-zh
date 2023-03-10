# 使用微服务构建持久 API 的 7 个原则

> 原文：<https://devops.com/7-principles-for-using-microservices-to-build-an-api-that-lasts/>

SparkPost 三年前推出了我们基于云的电子邮件递送服务的第一个测试版。在其推出时，少数客户每月发送几百万封电子邮件。现在，我们的 API 被成千上万的客户使用，包括 Pinterest、Zillow 和 Intercom，每月发送超过 150 亿封电子邮件。这一惊人的增长表明，我们的业务从提供内部电子邮件基础架构转向运营完全基于云的电子邮件交付服务的速度有多快。

这是一个伟大的商业故事。但是在技术和开发管理方面，我们如何管理这种规模的变化呢？在本文中，我将回顾一些选择和最佳实践，它们不仅帮助我们管理这种变化的速度，而且实际上帮助我们从中茁壮成长。

## 休息是最好的:务实，而不是迂腐

从一开始，我们就采取了“API 优先”的方法。我们的电子邮件 API *是*我们的核心应用，而不是事后的想法。

我们采取的第一步，也是最重要的一步，是决定在我们的 API 中使用 REST。我们的理念是选择以下三个元素作为 API 的基础:

1.  HTTP:这包括响应代码和操作符。操作符包括 POST、GET、PUT 和 DELETE，它们可以映射到基本的 CRUD(创建、读取、更新、删除)操作。
2.  资源:这些是 HTTP 操作符作用的实体。
3.  JSON (JavaScript 对象符号):这是一种数据交换格式。

这三个元素提供了实用 REST API 所需的一切，包括简单性、可移植性、互操作性和可修改性。在 API 建立之后，用户可以轻松地集成它，而不管他们的编程语言是什么，包括 C#、PHP、Node.js、Java 甚至是 shell 中的 cURL。他们可以做到这一点，而不必担心底层技术，包括其对多个微服务的使用。

当我们创建 SparkPost API 时，我们试图不要过于拘泥于纯 REST 模型，而是选择易用性。这里有两个可能不遵循 RESTful 最佳实践的例子:

1.  GET /api/v1/account？包含=用法
2.  POST/API/v1/sending-domains/example . domain . com/verify

第一个示例使用 GET 的查询字符串参数来过滤实体中返回的内容。在第二个例子中，我们在端点名称中使用了动作词“verify ”,这可能不是 RESTful。我们讨论每个新的使用案例，并尽最大努力确保它的一致性和易用性。

* * *

相关内容:

API:自动化是伟大的。可用性也是如此

[针对扩展优化云的技巧](https://devops.com/tips-optimize-cloud-scaling/)

* * *

## **发展和管理变革**

我们有许多开发人员和团队在我们的 API 微服务上工作，不断地进行变更。当一个工程师(和另一个工程师)认为变更已经通过了我们的测试时，我们自动将变更部署到产品中。当产品团队决定我们准备好告诉客户变更时，它就“发布”了。

我们很早就决定让我们的 API 在使用约定和管理变更的方式上保持一致。我们建立了一个治理小组，包括代表每个团队的工程师、产品管理小组的成员和我们的 CTO。这个小组建立并执行我们的 API 约定，这些约定都有完整的文档记录。

记录我们的约定减少了不一致性，并使定义每个新的端点变得更容易。以下是我们建立的一些惯例:

*   分隔单词时，URL 路径是带连字符的小写，并且区分大小写。
*   URL 查询参数和 JSON 字段也是带下划线的小写，并且区分大小写。
*   应该忽略请求正文中意外的查询参数和 JSON 字段。

我们的治理小组还为如何进行变更以及允许什么类型的变更设置了基本规则。有许多有益于用户且不会破坏他们的集成的好的 API 变化，包括:

*   现有资源上的新 API 资源、端点或操作
*   一个新的可选参数或 JSON 键
*   JSON 响应体中返回的新键

相反，重大变更包括任何可能破坏用户集成的事情，例如:

*   更改字段的数据类型
*   新的必需参数或 JSON 键
*   删除现有端点或请求方法
*   现有资源方法的本质上不同的行为，例如将选项的默认值从“false”更改为“true”

这些变化要么会破坏用户的集成，要么需要添加新版本，这会带来更多的开销。

## **做出改变时不要放弃——几乎所有的时间**

应该避免破坏性的改变，即使它们是修复错误或不一致的结果。通常最好的办法是绕开这种特质，而不是冒险破坏客户的集成。如果一个变化是突破性的，我们会非常谨慎地继续下去，并寻找其他方法来实现我们的目标。有时这可以通过简单地允许用户通过帐户设置或 API 参数改变他们的行为来实现。

然而，有些时候，我们的用户得到的好处超过了变化带来的任何潜在的负面影响。但是，在这些情况下，我们遵循了这些最佳实践:

*   我们得到了产品、支持和开发者关系团队的支持。
*   我们分析了 API 日志，以了解这一变化可能会影响多少用户。
*   我们给了用户至少 30 到 60 天的提前警告。
*   我们发送了一封电子邮件或发表了一篇博客文章，其中包含了这一变化的详细信息以及我们做出这一变化的原因。
*   我们在 API 文档中提供了指导。

## **一个版本统治所有人**

在过去的三年里，我们对 API 做了成千上万的修改，但我们仍然在第一个版本上。我们很早就决定不更新我们的 API，因为这样做增加了不必要的复杂性，会减缓用户对我们最新最好功能的采用。对 API 进行版本控制还会降低开发和测试的速度，使监控变得复杂，并混淆用户文档。

此外，不对我们的 API 进行版本控制意味着我们可以避免围绕这个主题的争议。有三种方法可以对 API 进行版本控制，但它们都有潜在的缺陷:

*   **将版本放入 URL:** 这很容易做到，但从语义的角度来看，这是一个糟糕的选择，因为实体不会在 v1 和 v2 之间改变。
*   **添加自定义标题:**也很容易做到，但语义不正确。
*   **将版本放入 accept 头:**语义更正确但最复杂的方法。

## **使用客户端库帮助非 JavaScript 用户**

与 JavaScript 相比，我们的一些用户更喜欢 Python、C#、Java 或 PHP。我们通过维护为他们的代码提供一组易于使用的函数的客户端库，使他们能够快速轻松地将我们的 API 集成到他们的应用程序中。

随着时间的推移，我们的客户端库已经发生了变化，我们确实对它们进行了版本化。我们已经知道，当包装一个活的、不断增长的 API 时，抽象是很难的，所以我们专注于提供一个抽象的薄层，提供一些语法快捷方式来简化我们的 API 的更复杂的区域。这样做可以让我们的用户快速、灵活地访问我们的任何 API 端点——这也让我们的 API 在某种程度上“经得起未来的考验”。

## **还有一个“文档优先”策略**

我们将我们的文档视为代码，并在我们编写或更改一行 API 代码之前用它来记录我们的 API 更改。这样做有助于我们执行我们的约定，保持一切一致，并保持良好的客户体验。它还降低了支持成本。

我们在 GitHub 中维护我们的文档，这使得技术和非技术用户很容易做出修改。我们还发现，这样更容易审查变更。我们使用 API Blueprint Markdown 格式和 Jekyll 来生成 HTML 文档，还有一个很好的搜索服务 Algolia。这样做可以让我们完全控制客户体验，包括移动体验。

对于那些不想“自己卷”文档的人，我们推荐 OpenAPI(以前称为 Swagger)、Apiary 和 API Blueprint。避免使用不太适合 REST API 文档的工具很重要。我们建议在文档中包含一个亮橙色的“Run in Postman”按钮，这样就可以很容易地尝试一个 API，以及成功和失败场景的好例子。

## **倾听用户**

最后，我们建议所有开发者注意他们的用户所说的话。SparkPost 有一个社区 Slack 频道，成千上万的用户可以在这里轻松访问我们的产品、支持、工程和执行管理团队成员。我们还有一个专门的开发人员关系团队，专注于与开发人员社区合作。所有这些都允许我们倾听用户的声音，并将他们的反馈整合到我们的 API 中。

克里斯·麦克法登