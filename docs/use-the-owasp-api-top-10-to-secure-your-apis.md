# 使用 OWASP API Top 10 来保护您的 API

> 原文：<https://devops.com/use-the-owasp-api-top-10-to-secure-your-apis/>

在过去的十年中，用于构建应用程序的工具、语言、平台和方法发生了巨大的变化。应用程序安全实践必须随之改变；否则，安全专业人员将不断追赶攻击者和网络罪犯。

## 什么是 OWASP API Top 10？

微服务和应用程序编程接口(API)的增加引发了一系列针对应用程序的新威胁。OWASP API Top 10 记录了与 API 开发相关的风险。

以下是最新 OWASP API Top 10 中突出显示的漏洞:

1.  中断对象级授权(BOLA)
2.  用户身份验证失败
3.  过多的数据暴露
4.  缺乏资源和速率限制
5.  功能级别授权中断
6.  批量分配
7.  安全错误配置
8.  注射
9.  资产管理不当
10.  记录和监控不足

## 为什么 OWASP API Top 10 是必需的？

庞大的整体正在让位于小巧灵活的微服务。Kubernetes、容器、云原生架构和 API 网关是新的热点。这种转变也导致了新的威胁。

让我们来看看传统 web 开发和 API 开发的[区别](https://www.traceable.ai/blog-post/6-new-requirements-for-securing-microservices-versus-monolithic-applications)。

## 认证和授权看起来完全不同

API 十大风险中有十分之三(包括前两个)与身份验证和授权问题有关。这些关键的安全功能在 API 中与在更传统的 web 应用程序中有所不同。

在典型的 web 应用程序中，用户登录，服务器授予一个会话 cookie。浏览器存储 cookie，并在每次请求时将其传递给服务器，这样就不需要重新进行身份验证。用户的所有权限都与会话 ID 相关联。

API 由部署在不同服务器上的几个迷你 web 应用组成，每个应用都有自己的数据存储。在一台服务器上创建一个会话并不重要。接收下一个请求的服务器不知道存储在第一个服务器上的会话的任何信息。

这种复杂性催生了 OAuth 和 OpenID 连接规范。这些规范概述了分布式系统的认证(开放 ID)和授权(OAuth)。正确使用这些技术有助于保持微服务和 API 的安全。

但是即使 API 的认证和授权已经改变，它们的另一个方面引入了 API 风险中的一个新的大玩家:业务逻辑错误。

## API 说得太多了

传统的 web 应用程序公开一个端点，在服务器上运行的一个可执行文件包含所有的业务逻辑。攻击者将很难描绘出应用程序的所有内部业务逻辑。有了这么多的试验和错误，基于输入的漏洞更容易被发现，例如 [XSS](https://devops.com/?s=XSS) 或 SQL 注入。

另一方面，将应用程序分解成微服务，每个微服务都有自己的 API 端点，默认情况下会将大部分业务逻辑暴露给外部世界。您可以观察浏览器的连接，将应用程序的各个部分视为一个整体。而且大多数时候，公共接口揭示了敏感数据对象的基本参数和唯一标识符。

博拉就是这种现象的一个极好的例子。当攻击者更改传递给 API 的资源 ID 以检索其他人的记录时，就会发生 BOLA。

想象一个保存敏感文档的医疗应用程序。您可以查看 PDF 格式的文档。因为 API 用于提供数据，所以客户端应用程序通过 URL 传递一个 ID。你不小心(因为我们知道你不会故意这样做)调换了 URL 中的数字。突然，另一个人的医疗信息回瞪着你。您发现了一个 BOLA 漏洞。

API 说得太多的另一个例子是基于声明的认证。通常，JSON web 令牌(JWT，发音为“jawt”)用于发送当前用户的权限，称为“声明”这些令牌很容易被解码和更新。

想象一下，使用 OAuth 接收一个 JWT 并对其进行解码。您会注意到令牌上的一个属性是“admin: false”现在你知道应用程序是如何决定你的权限的了。您将属性更改为“admin: true ”,并在下一个请求中将其发送回应用程序。如果 API 没有遵循正确的令牌签名和验证过程，那么您现在已经成为一名管理员，可以访问各种好东西。

确保你的 API 没有泄露太多信息。了解 API 的客户看到了什么，并确定每个数据的风险和缓解措施。

“信口开河击沉船只”是二战时期著名的安全警告。在当今世界，松散的数据汇 API。

## 微服务和 API 非常容易创建和部署

新的开发方法伴随着组织内部的文化变革而来。开发人员的自主性和交付速度得到了强调，导致许多开发团队决定如何实现 API 以及何时何地部署它们。

这些方法带来了更大的灵活性、敏捷性和可伸缩性，但也可能导致 API 激增和风险增加。API 前十名中的第九名是资产管理不当。不知道所有 API 在哪里以及它们做什么会导致严重的应用程序漏洞。

例如，在创建和部署 API 的新版本时，运行旧版本的端点可能仍然存在。如果旧版本包含安全漏洞，攻击者可能会在您不知情的情况下利用它。使用 API 发现技术构建清单，使组织能够找到这些端点并正确关闭它们。

企业需要敏捷和反应灵敏。但他们也必须意识到这些策略产生的副作用，并设计一些流程来控制局面。

## 如果您正在构建 API，不要忘记 API Top 10

构建微服务和 API 不同于构建传统的 web 应用程序。环境、框架和开发技术的差异在引入新问题的同时解决了一些问题。

熟悉 OWASP API Top 10 并使用它来检查您的应用程序。将它添加到您已有的常规安全检查点。那么您就可以确信您的 API 是安全可靠的。

可追踪的防御人工智能有助于防范 OWASP API Top 10。观看[录制的演示](https://www.traceable.ai/view-traceable-demo),了解它的运行情况。