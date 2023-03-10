# 会话令牌与 jwt:选择您的会话管理解决方案

> 原文：<https://devops.com/session-tokens-vs-jwts-choosing-your-session-management-solution/>

在今天的[认证](https://devops.com/authentication-in-serverless-apps-what-are-the-options/)世界中，会话令牌和 JSON Web 令牌(jwt)是管理用户会话和维护用户在两次调用之间的认证状态的两种最流行的方式。激烈的辩论使这些解决方案相互对立，但是每一个都有值得评估的优点和缺点。根据您的应用程序的需要，甚至可以考虑将它们结合起来使用，以达到两全其美。

### 会话令牌和 jwt 之间的主要区别

为了理解会话令牌和 jwt 之间的区别，查看它们的设置和影响是有帮助的。

### 设置

会话令牌和 jwt 设置方式的最大区别在于用户的身份验证信息存储在哪里以及如何存储。

使用会话令牌，用户的身份验证状态作为记录存储在服务器端数据库中，该记录包括会话的主要标识符(通常是至少 128 位长的随机字符串)、用户的标识符、会话开始的时间、会话的到期时间，有时还包括 IP 地址等其他上下文信息。一旦存储在数据库中，会话标识符就被发送回客户机，作为 cookie 存储在用户的浏览器中。

使用 JWTs，用户的身份验证数据一被服务器发布，就被存储为客户端的 JSON 对象。该对象包含一个头、一个有效负载(存储敏感用户信息的地方)和一个签名，该签名是通过结合头和有效负载创建的，然后用一个秘密密钥散列以保护用户信息。

### 影响

您还可以根据性能和控制来查看会话令牌和 jwt。

一般来说，jwt 基于性能胜出:它们支持更快的授权和与外部应用程序更好的互操作性。但他们需要更多的开发人员投资来解决他们的安全复杂性，并确保正确的护栏到位，以防止漏洞。

另一方面，会话令牌支持更多的控制，但会带来一些延迟。虽然它们提供了更强的保证，保证每个请求都得到授权，并且更容易安全地实现，但它们在服务器端数据库验证上的瓶颈带来了延迟开销，这可能会破坏用户对高响应性应用程序的体验。

虽然这个框架对于总结 jwt 和会话令牌是很有帮助的，但是它陷入了安全性和性能之间的矛盾，好像这两者是相互排斥的。但是，增长和安全领域的前瞻性领导者都认识到，最佳解决方案利用安全性来优化用户体验，并加快产品的采用和增长。使用会话管理做到这一点的最佳方式之一是将 jwt 和会话令牌结合成一个强大的混合体。

### 组合 jwt 和会话令牌

到目前为止，公司有几种不同的方法来组合会话令牌和 jwt。[最简单的方法之一](https://stytch.com/)是当用户开始一个会话时，返回一个 session_token 和一个 JWT。session_token 是一个静态值，适用于会话的生存期(存储在服务器端)，而 JWT 有自己的较短的到期时间。

在这个设置中，可以将过期的 JWT 传递给会话 API，以便检索新的 JWT，服务器确保底层会话在传递回新的 JWT 之前仍然是活动的。如果用户注销，这个[访问](https://devops.com/how-to-revoke-json-web-tokens-jwts/)的撤销将在您为您的 JWT 设置的任何令牌年龄内发生。换句话说，您只在 JWT 过期时或者在授予对特别敏感的操作的访问权之前调用服务器。

通过这种方式配置，这种分离管理方法大大降低了性能开销，同时还保护您和您的最终用户免受基于陈旧信息授权操作的风险。jwt 和会话令牌一起被用来优化安全性和性能，而不是折衷。

### 选择适合您的解决方案

尽管有如上所述的新的混合方法，仍然有一些最大化主义者会告诉你一种方法总是更好的。当然，事实是每个应用程序都是独特的，安全性和延迟的权衡需要在上下文中进行评估。

无论您是追求会话令牌、jwt 还是如上所述的混合解决方案，会话管理的选择实际上可以归结为如何回答四个关键问题:

**1。你存储的信息有多敏感？**

一个非常注重安全性的组织，如银行或政府机构，可能希望只使用会话 cookies 来确保每个呼叫在那个时刻都得到授权。根据数据泄露的风险和成本以及更长的延迟可能给客户带来的成本来选择您的解决方案。

**2。你对产品的可扩展性有什么抱负？**

如前所述，使用 JWTs 进行扩展要容易得多，因为不需要调用服务器来重新认证会话。如果您的产品必须处理高流量，那么您需要制定一个计划来解决潜在的延迟问题。

**3。您的应用程序依赖于哪些现代功能？**

对于许多现代特性，如无服务器计算、跨域功能、特定于移动设备或单页面应用程序，jwt 要么是首选的，要么是必需的。了解您的产品使用哪些功能将有助于您了解可用的会话管理工具。

**4。性能和正常运行时间对我的最终用户有多重要？**

我想多快开始运行？对于那些价值主张依赖于快速、流畅的用户体验(比如游戏直播)的公司来说，JWTs 可以提供他们需要的速度和响应时间。对于其他类型的产品，延迟对用户体验的影响较小，或者他们希望以较少的初始投资获得安全性保证，会话令牌可以提供他们所需的稳定性和保证。

### 选择权在你

虽然一些铁杆支持者可能总是坚持在会话令牌和 jwt 之间进行选择，但现代会话管理解决方案要微妙得多，因此公司可以优化其独特产品的性能和安全性要求。由于能够根据需要在 jwt 和会话令牌之间切换，现在有了比以往更多的选择。