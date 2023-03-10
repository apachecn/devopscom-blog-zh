# 在 Go 中创建自动化 GitHub 机器人

> 原文：<https://devops.com/creating-automated-github-bots-in-go/>

事件管理需要快速响应，这是一项挑战，因为通常每天都会发生大量的事件。因此，依靠人类来快速响应这些事件是容易出错、混乱且经常令人沮丧的。这些事件有容易重现的步骤，可以被编码，是机器人存在的完美理由。

创造一个机器人可以减少日常事件的噪音，这样重要的人就可以专注于重要的人类活动——比如编程、创新，或者最重要的，睡觉。 已经有很多机器人存在，可以解决无数问题。例如，[dependent bot](https://github.blog/2020-06-01-keep-all-your-packages-up-to-date-with-dependabot/)有助于保持您的 [GitHub](https://devops.com/migrating-to-github/) 依赖项随着自动拉取请求而更新。 [谷歌日历](https://influxdata.slack.com/apps/ADZ494LHY-google-calendar?tab=more_info) 有一个 Slack bot，可以在会议即将开始时提醒你。当然，也有还没有预制 bot 的情况，这为开发人员提供了创建自己的 bot 的完美机会！

我的首选编程语言是 [Go](https://go.dev/) ，我已经用它创建了多个机器人。我创建的一个最喜欢的机器人有助于管理一个名为 Telegraf 的大型开源项目，我将在本文末尾详细讨论这个项目。机器人并不局限于开源项目；当我在一家大型企业公司工作时，我创建的另一个机器人被证明是有价值的。这是一个 Slack 机器人，可以在 Amazon EC2 Windows 实例上运行命令，并帮助团队快速为客户执行操作，例如在几秒钟内重置密码，而不是几天。

### 为 GitHub 创建自己的机器人

让我们看看如何开始创建一个用 Go 编写的可以与 GitHub 交互的机器人。包[Google/go-github](https://github.com/google/go-github)让你与 GitHub API 交互，让为 GitHub 创建一个机器人变得容易。像这样的工具是你开发自己的机器人的第一步。使用这个包，您可以创建类似于 Dependabot 的东西。为了开始接收 GitHub 事件供您做出反应(比如有人创建了一个 pull 请求)，您需要创建一个[GitHub App](https://docs.github.com/en/developers/apps/getting-started-with-apps/about-apps)。

![GitHub App 1](img/5a3759f4a034fc8d72d4ca24f72ed795.png)

GitHub 文档很好地描述了如何做到这一点，但是需要注意的重要一点是回调 URL。回调 URL 将是一个与您的 Go 程序相关联的公开地址，这样 GitHub 就可以将事件路由到它。我使用[AWS Lambda](https://aws.amazon.com/lambda/)函数来托管我通过使用 [无服务器框架](https://www.serverless.com/) 创建和管理的机器人，但是只要你有一个公共 URL，你可以使用任何你想要的东西。如果您也对使用 lambda 函数感兴趣，您的“main.go”可以简单到只需调用“Lambda”。开始”并传入保存业务逻辑的函数。

![GitHub App 2](img/ca14fde6ef6f5d417a3fd71a582862c0.png)

因为您使用的是公共 URL，所以安全性很重要。一旦您创建了 GitHub 应用程序，您将获得一个秘密令牌，您可以使用它来帮助验证传入的请求。google/go-github 包让这一切变得简单；你要做的就是调用 [github。验证有效负载](https://pkg.go.dev/github.com/google/go-github/v43/github#ValidatePayload) 并向其传递您的秘密令牌和传入的 HTTP 请求，以确保有效负载有效。如果验证成功，该函数将返回定义您刚刚收到的事件的 JSON 有效负载。您可以使用函数 [github 解析有效载荷。ParseWebhook](https://pkg.go.dev/github.com/google/go-github/v43/github#ParseWebHook) ，其中会返回给你一个空的接口，可以容纳任何值。因此，您需要使用类型断言来访问底层类型，以查看您收到了什么事件。

![GitHub app 3](img/c7f7b3c00fc3d94616d846a38e473c0c.png)

根据事件类型，您可能需要采取不同的措施。也许如果有人发行了新的一期，你会收到类型为 的 github。issue event，这将有利于执行初始分类，例如添加适当的标签。也可以接收事件类型 github。CommitcommentEvent ，这表明有人刚刚发表了一个评论，您可以检查特殊命令，比如自动重启构建系统。例如，您还可以在有人创建新问题时创建欢迎评论，如下面的代码片段所示。

![Picture 4](img/ded60ebe173ae3136c1fd8ff21abac2a.png)

### 创建一个松弛机器人

这些例子集中在与 GitHub 的交互上，但是可以被复制来创建一个类似于 Google 日历机器人的 Slack 机器人。软件包[Slack-go/Slack](https://github.com/slack-go/slack)允许您与 Slack API 进行交互，您可以使用该 API 发布消息或创建允许用户与定制按钮和列表进行交互的“模态”。

创建一个 [Slack bot](https://api.slack.com/bot-users) 与创建 GitHub App 的过程类似。Slack 提供了一个用户界面来注册一个 bot，与 GitHub 类似，它需要你提供一个公共 URL，这样它就可以发送你的 bot 事件。然后，您还可以使用函数 [slack 来验证传入的事件。newsecretsverifer](https://pkg.go.dev/github.com/slack-go/slack#NewSecretsVerifier)使用 Slack 提供的秘密令牌。例如，一旦完成这些步骤，您的机器人就可以开始向通道发送消息来帮助您回答问题。

![SlackBot](img/dd939580d84b7e908dec220262fce07a.png)

### 赋予它生命

在 [Telegraf](https://github.com/influxdata/telegraf) 项目中可以找到一个 bot 的例子，它是 InfluxData 的开源数据收集代理。我们有一个用 Go 编写的机器人帮助我们维护名为“telegraf-tiger”的知识库用户与机器人的第一次交互是当他们提交一个新的拉请求时。当请求被发出时，机器人会友好地提醒你签署我们的贡献者许可协议(CLA)。

![reminder](img/0ab9e0ebd4c1c4ba07acce9269d9b90d.png)

一旦签名，机器人可以通过添加注释“ 来验证 CLA 是否已被签名！signed-cla ”并给拉请求一个闪亮的绿色对号，让维护人员知道一切准备就绪。

我们的 Tiger bot 支持的另一个领域是共享我们的持续集成(CI)系统为每个拉请求构建的工件，并提供链接到每种类型的有用注释。这有助于传播对工件的认识，这样任何人都可以轻松地帮助测试新特性或错误修复，而不必自己建立本地开发人员环境。

![CI pull request](img/4e048860bd3ea5928456a66c1dd91661.png)

### 大外卖

机器人是一种令人兴奋的开发工具，它可以自动完成平凡的任务，让工程师专注于更大、更有吸引力的任务。GitHub 等资源也使得以各种方式使用 Go 开发 bot 变得容易。机器人通常出现在不同的界面上，有些只是提醒我们即将到来的会议，有些则确保签署重要的许可协议。

机器人的使用案例是无止境的，通过正确的工具，机器人可以帮助工程师专注于手头更重要的任务。开发人员可以高枕无忧，因为他们知道他们的机器人正在自动执行任务，并对他们不想处理的无休止的警报做出响应。相反，他们能够专注于重要的人类活动，如睡眠，这样他们就可以梦想下一件大事。