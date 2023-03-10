# GraphQL 最大的优势也是它最大的弱点

> 原文：<https://devops.com/graphqls-greatest-strength-is-also-its-greatest-weakness/>

> ***迈克尔·斯科特:**我何不告诉你我最大的弱点是什么？我工作太努力，我关心太多，有时我对工作投入太多。*
> ***大卫华莱士:**好的。你的优势呢？*
> ***迈克尔·斯科特:**嗯，我的缺点其实也是优点。*
> ***大卫·华莱士:**哦。是的。非常好。*

GraphQL 是一种新的查询语言，它提供了一种与结构化数据交互的简单方式。GraphQL 设计中最好的一点是它方便的数据获取过程，这使得请求方能够收集无限的数据并执行多种操作，所有这些都只需要一个 API 调用。这种交互方式让它超级有用，非常好用。然而，从安全角度来看，它最大的优势也可能是它最大的弱点。

我最近会见了 Salt Security 的首席产品官 Elad Koren，以了解 GraphQL 安全性的细微差别。根据 Koren 的说法，GraphQL 提供了比 REST APIs 更好的可用性，但它的捆绑请求模型可能会危及没有采用正确的对象级授权检查的系统。此外，由于开发人员与 GraphQL 服务的交互不同于典型的 web APIs，黑客可以避开典型防火墙的检测，这需要一种新的安全方法。

这些担忧并不会妨碍领养；相反，它们是对那些在生产中使用 GraphQL 的人的现实检验。下面，我们将探索一些潜在的弱点，并查看一些提供者可以用来提高其 GraphQL 端点的机密性的一般缓解措施。

## GraphQL 是什么？

GraphQL 最初由脸书开发，并于 2015 年开源。它是一种查询语言，使外部数据源的数据检索和操作变得非常容易。GraphQL 使客户机能够将查询捆绑到单个请求中，而不是用传统的 HTTP API 请求编程和链接复杂的调用。这种设计模式减少了 REST APIs 通常会遇到的欠取和过取模式。

“你得到的正是你需要的，而不是更多或更少，”科伦描述道。这使得 GraphQL 比 REST 更受现代数据库机制的欢迎，因为它类似于 SQL 查询。

GraphQL 的采用正在稳步增长；2020 年 RapidAPI 的一项调查发现 GraphQL 的使用率翻了两番。GraphQL 现在被 22.5%的 API 开发者使用。但是当谈到整体 API 设计模式时，REST 仍然是 93.4%的 API 使用的主导架构风格，Postman 的 2020 年[API 状态报告](https://www.postman.com/state-of-api/#key-findings)发现。

GraphQL 很有前途，有许多好处，但仍处于早期采用阶段。“这仍然是一项早期采用者开始研究的技术——它没有那么广泛，”科伦说。由于其历史久远，GraphQL 安全实践还不成熟，暴露了一些使用 GraphQL 的平台的潜在漏洞。

## 独特的安全问题

那么，GraphQL 范式中有哪些独特的安全问题呢？根据科伦的说法，这是从缺乏理解开始的。“大多数时候，安全不一定是最重要的，”他说。“当开发人员选择实现 GraphQL 时，他们假设他们不再使用 API，并且传统的 REST API 漏洞不再适用。”

事实上，可能正好相反。与 REST APIs 一样，GraphQL APIs 很容易遭受对象级授权的破坏，这是 OWASP 的头号 API 漏洞。但是，由于对许多底层系统的访问更加容易，单个 GraphQL 查询可以比典型的 API 请求泄漏更多的信息。如果 GraphQL 提供程序没有对每个特定的方法和资源进行粒度授权检查，GraphQL 端点可能会遭受数据过度暴露。

另一个问题是发现恶意行为。通常，当黑客对一个 API 执行侦察时，他们会用许多请求来暴力破解它；尝试不同的名称空间并在此过程中更改用户代理。使用 REST APIs，这种恶意行为更容易被标准 web 应用程序防火墙(WAFs)捕获，因为它更容易注意到数百个特殊的畸形请求。然而，使用 GraphQL，进行查询批处理的黑客可以完全避开典型阈值的雷达。

Koren 说，这很容易导致帐户被接管，他已经在生产中看到了这一点。他描述了一个使用 GraphQL 的产品支付服务；调用者可以执行他们不应该被允许执行的变异和功能，比如调出其他用户的帐户信息，甚至启动交易。

通过给每个资源分配访问参数并一次处理一次授权检查，使用 REST API 可以更容易地限制这种恶意流量。但是，这个剧本在 GraphQL 中被抛弃了。“当你使用单点访问数据时，你可能会有一些错误的安全感，”科伦说。实际上，拥有单个接入点需要付出艰苦的努力来保持其完整性。Koren 解释说，一个可用的 GraphQL 前端也可能经常掩盖由不同 API 风格组成的复杂后端，这使得跨各种微服务将用户授权与特定资源和突变关联起来变得更加困难。

## 减轻弱点的技巧

那么，考虑到这些弱点，基于 GraphQL 的平台应该如何应对呢？Koren 提供了以下建议来保护 GraphQL APIs:

*   **在开发中采用安全思维**:从一开始就建立安全文化至关重要。可用性不应该损害安全性；理想情况下，它们应该是互补的。
*   **确保适当的授权检查到位**:每当向用户提供资产时，您需要考虑用户是否被授权访问它— *尤其是*如果他们同时访问多个资源。
*   **设定特定于 GraphQL 的新基线** : GraphQL 所有者需要调整他们的外围安全系统，以寻找新队列。这些验证应该考虑典型的 REST API 安全检查*和*考虑嵌套查询和批处理查询的细微阈值。
*   **了解您的 API 清单**:保持对 GraphQL 端点下的底层架构的清晰了解。验证数据源并确保它们正确对应于用户权限。
*   **增加对 API 调用的可见性**:如果可能，增加对查询、突变、属性、变量和底层规范以及它们如何相互作用的可见性。

## 强化 GraphQL 端点

API 攻击正在迅速增加。Gartner 估计 API 将在 2022 年成为头号威胁载体，Salt Labs 的数据显示，到 2021 年年中，恶意 API 流量将惊人地增长[300%](https://securityboulevard.com/2021/07/api-attack-traffic-grew-300-in-the-last-six-months/)。

“像任何其他成为主流的创新技术一样，它会越来越受欢迎，但在可预见的未来，它不会超过 REST，”Koren 说。或许在三到四年内，GraphQL 目前 20%的采用率会上升到 30%到 50%。虽然 GraphQL 仍然是一个相对小众的工具，但它的使用正在增长，特别是在 API 优先的云原生技术公司中。这种采用会带来新的安全问题。

根据 Koren 的说法，查询批处理使得使用普通防火墙捕捉恶意攻击变得棘手。因此，训练一个新的基线来发现 GraphQL 特有的异常是必要的，以便在黑客仍处于侦察阶段时发现并限制他们。因此，我们可能会看到未来的安全投资进入发现这些非典型的 GraphQL 交互。

总的来说，也许最好的建议是像对待任何其他类型的 API 一样对待 GraphQL 如果不是更多的话。作为许多底层系统的单一入口，GraphQL 需要额外的安全考虑和用户授权的谨慎应用。

有了这些，GraphQL 最大的优势有望保持不变——一个巨大的优势。