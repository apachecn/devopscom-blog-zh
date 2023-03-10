# 为应用程序设计认证系统

> 原文：<https://devops.com/architecting-an-auth-system-for-applications/>

当今的应用程序使用许多登录和身份验证方法以及工作流。在这里，我将分享最相关和最成熟的身份验证工作流，您可以使用它作为架构和设计传统 web 应用程序、单页面应用程序和本机移动应用程序的身份验证系统的基础。

## 传统 Web 应用程序的身份验证工作流

传统的 web 应用程序使用基于消息的模型加载网页并提供用户功能，在这种模型中，浏览器根据地址栏中的 URL 向 web 服务器发出 HTTP 请求。服务器用 HTML、CSS 和 JavaScript 响应这个请求，然后在浏览器中显示一个资源。除了传统的 web 应用程序，新的 web 应用程序通常仍然以这种方式提供功能。

当用户提交表单或单击链接或按钮时，浏览器会向 web 服务器发送新的 HTTP 请求，并更改地址栏中的 URL。服务器再次响应，返回 HTML、CSS 和 JavaScript，然后在浏览器中显示一个资源。

对于传统的 web 应用程序，浏览器只支持两种 HTTP 方法:GET 和 POST。GET 用于从指定的资源请求数据，POST 用于向服务器发送数据以创建或更新资源。

![](img/7620cf27097b006c652a0d5f60a406d0.png)

以下是您可以用于传统 web 应用程序登录和验证的几个工作流。请注意，*应用程序后端*是应用程序的后端(不是身份提供者或 IdP ),而*本地登录表单*是直接内置到应用程序中的表单，而不是外部登录表单。

| **原生登录表单到应用后端使用……** |
|  | [jwt 并刷新存储在 cookies 中的令牌](https://fusionauth.io/learn/expert-advice/authentication/webapp/native-login-form-to-application-backend-jwts-refresh-tokens-cookies) |
|  | [刘宇](https://fusionauth.io/learn/expert-advice/authentication/webapp/native-login-form-to-application-backend-sessions) |
|  | [会话加上存储在 cookies 中的刷新令牌](https://fusionauth.io/learn/expert-advice/authentication/webapp/native-login-form-to-application-backend-sessions-refresh-tokens-cookies) |
| **OAuth 2 授权码授予使用…** |
|  | [【jwt】并刷新存储在 cookies 中的令牌](https://fusionauth.io/learn/expert-advice/authentication/webapp/oauth-authorization-code-grant-jwts-refresh-tokens-cookies) ( **推荐** ) |
|  | (**推荐** ) |
|  | [会话加上存储在 cookies 中的刷新令牌](https://fusionauth.io/learn/expert-advice/authentication/webapp/oauth-authorization-code-grant-sessions-refresh-tokens-cookies) |
| **OAuth 2 资源所有者密码凭证授予使用…** |
|  | [jwt 并刷新存储在 cookies 中的令牌](https://fusionauth.io/learn/expert-advice/authentication/webapp/oauth-resource-owner-password-credentials-grant-jwts-refresh-tokens-cookies) |
|  | [刘宇](https://fusionauth.io/learn/expert-advice/authentication/webapp/oauth-resource-owner-password-credentials-grant-sessions) |
|  | [会话加上存储在 cookies 中的刷新令牌](https://fusionauth.io/learn/expert-advice/authentication/webapp/oauth-resource-owner-password-credentials-grant-sessions-refresh-tokens-cookies) |

## 单页应用程序的身份验证工作流

从网页加载 HTML、CSS 和 JavaScript 源代码后，单页 web 应用程序(spa，发音为“SPA”或“S-P-A”)完全在浏览器中运行。在检索组成应用程序的 HTML、CSS 和 JavaScript 之后，浏览器调用 JavaScript 框架，该框架引导并呈现应用程序。

spa 调用[API](https://devops.com/?s=APIs)来处理用户交互和输入。例如，如果用户单击链接或提交表单，SPA 可能会呈现不同的页面或表单。

API 是使用 XMLHttpRequest 调用的，XMLHttpRequest 是一个内置的浏览器对象，可以用 JavaScript 发出 HTTP 请求。当服务器响应时，浏览器中运行的 JavaScript 动态更新数据，而不执行  全页面刷新。

![](img/018528f81a382e1b259c735e1ae2b2e9.png)

spa 使用单一的请求和响应模型。由于浏览器使用 XMLHttpRequest，它可以支持 GET 和 POST，以及其他标准的 HTTP 方法，如 PUT 和 DELETE。(PUT 用于替换指定资源的所有当前表示，DELETE 用于删除指定资源。)选择的 HTTP 方法告诉服务器如何处理请求。

以下是一些可用于 SPA 登录和身份验证的工作流。

| **原生登录表单到应用后端使用……** |
|  | [jwt 并刷新存储在 cookies 中的令牌](https://fusionauth.io/learn/expert-advice/authentication/spa/native-login-form-to-application-backend-jwts-refresh-tokens-cookies) |
|  | [刘宇](https://fusionauth.io/learn/expert-advice/authentication/spa/native-login-form-to-application-backend-sessions) |
|  | [会话加上存储在 cookies 中的刷新令牌](https://fusionauth.io/learn/expert-advice/authentication/spa/native-login-form-to-application-backend-sessions-refresh-tokens-cookies) |
| **原生登录表单到 FusionAuth 使用…** |
| [jwt 存储在本地存储，刷新令牌存储在 cookie](https://fusionauth.io/learn/expert-advice/authentication/spa/native-login-form-to-fusionauth-jwts-local-storage-refresh-tokens-cookies) |
| [JWTs 并刷新存储在 cookies 中的令牌](https://fusionauth.io/learn/expert-advice/authentication/spa/native-login-form-to-fusionauth-jwts-refresh-tokens-cookies) |
| [jwt 并刷新存储在 cookies 中的令牌](https://fusionauth.io/learn/expert-advice/authentication/spa/native-login-form-to-fusionauth-jwts-refresh-tokens-cookies) |
| **OAuth 2 授权码授予使用…** |
|  | [【jwt】并刷新存储在 cookies 中的令牌(**推荐** )](https://fusionauth.io/learn/expert-advice/authentication/spa/oauth-authorization-code-grant-jwts-refresh-tokens-cookies) |
|  | [刘宇( **推荐** )](https://fusionauth.io/learn/expert-advice/authentication/spa/oauth-authorization-code-grant-sessions) |
|  | [会话加上存储在 cookies 中的刷新令牌](https://fusionauth.io/learn/expert-advice/authentication/spa/oauth-authorization-code-grant-sessions-refresh-tokens-cookies) |
| **【OAuth 2】隐式授予使用…** |
|  | [存储在 cookies 中的 jwt](https://fusionauth.io/learn/expert-advice/authentication/spa/oauth-implicit-grant-jwts-cookies) |
|  | [jwt 存储在本地存储器](https://fusionauth.io/learn/expert-advice/authentication/spa/oauth-implicit-grant-jwts-local-storage) |
|  | [刘宇](https://fusionauth.io/learn/expert-advice/authentication/spa/oauth-implicit-grant-sessions) |
| **OAuth 2 资源所有者密码凭证授予使用…** |
|  | [jwt 并刷新存储在 cookies 中的令牌](https://fusionauth.io/learn/expert-advice/authentication/spa/oauth-resource-owner-password-credentials-grant-jwts-refresh-tokens-cookies) |
|  | [刘宇](https://fusionauth.io/learn/expert-advice/authentication/spa/oauth-resource-owner-password-credentials-grant-sessions) |
|  | [会话加上存储在 cookies 中的刷新令牌](https://fusionauth.io/learn/expert-advice/authentication/spa/oauth-resource-owner-password-credentials-grant-sessions-refresh-tokens-cookies) |

将 OAuth 用于 SPA 时，请注意浏览器会从 SPA 导航到 OAuth 提供者。OAuth 工作流完成后，浏览器将被发送回 SPA 页面，在这里它将使用缓存的资产快速重启 SPA。

## 本地移动应用的身份验证工作流

原生移动应用通常通过 App Store 和谷歌 Play 商店等在线市场安装在移动设备或任何智能设备上。单击设备上的应用程序图标会启动设备操作系统，从而启动应用程序及其用户界面。

几乎所有本机应用程序都调用服务器上的 API 来处理用户交互和输入，比如按钮点击和表单提交。本机应用程序通常使用被设计为直接访问源代码的所有类、对象、函数和方法的库来与 API 快速通信并简化 API 调用。

![auth mobile](img/eeba83e0389b91d5dd23696672ec6989.png)

以下是一些可用于本地移动应用程序登录和验证的工作流:

| [**原生登录表单到应用后端使用 JWTs 并刷新令牌**](https://fusionauth.io/learn/expert-advice/authentication/mobile/native-login-form-to-application-backend-jwts-refresh-tokens)[**原生登录表单使用 JWTs 进行 FusionAuth 并刷新令牌**](https://fusionauth.io/learn/expert-advice/authentication/mobile/native-login-form-to-fusionauth-jwts-refresh-tokens) **(推荐)**[**OAuth 2 资源所有者密码凭证授予使用 jwt 和刷新令牌**](https://fusionauth.io/learn/expert-advice/authentication/mobile/oauth-resource-owner-password-credentials-grant-jwts-refresh-tokens) |

注意，本地移动应用程序也可以使用 OAuth 授权码授权来交换访问令牌的授权码。此工作流适用于许多 IDP，与前面的传统 web 应用程序和单页应用程序部分中描述的基本相同。主要区别在于，本机应用程序在 OAuth 工作流结束时从 web 视图中提取 JWT 和刷新令牌。

## 认证系统最佳实践

上面列出的工作流应该为您提供了遵循身份验证系统最佳实践以及为您的应用程序设计可靠的登录和身份验证系统的基准。虽然这些示例使用 FusionAuth 作为 IdP，但是可以使用任何 IdP。大多数 IDP 能够进行各种各样的登录和身份验证工作流，此处的示例并不详尽。

当您为传统 web 应用程序、单页应用程序或原生移动应用程序设计身份验证系统时，请记住一些 IdP 登录工作流可能会带来严重的安全风险。正如所有与数字身份、用户和数据安全有关的事情一样，明智地选择 IdP 和身份验证工作流程非常重要。