# 使用网飞的 HubCommander 自动化 GitHub 组织

> 原文：<https://devops.com/using-netflixs-hubcommander-to-automate-github-organizations/>

网飞的指数级增长在很大程度上归功于其惊人的科技积累。通过单一内部 API 限制其内容，该公司能够提供与设备类型无关的内容，并迅速击败消费娱乐行业中的当代竞争对手。

那么，当网飞公开一些内部架构供他人使用时，我们很感兴趣。HubCommander 只是网飞不断增加的[开源工具](https://github.com/Netflix)中的一员。这是一个用于 GitHub 管理的 ChatOps 工具。

我们之前报道过 ChatOps 的[开源方法，跟踪如何将免费的操作工具引入对话，以提高透明度和效率。在本文中，我们将通过了解网飞如何利用 HubCommander 来继续这项研究，并深入研究其开源迭代，看看其他人如何利用它来自动化其 GitHub 组织。](https://devops.com/implementing-chatops-using-open-source-tooling/)

## 问题

在大型组织中工作时管理许多 GitHub 存储库可能会令人沮丧；尤其困难的是管理不同用户子集之间的权限级别。不仅各种用户权限级别难以跟踪，而且还有一个固有的安全问题需要解决，尤其是在与外部团队合作时。

> “使用 GitHub 组织的最大挑战之一是用户管理。” —网飞

项目经理需要管理不同的组织，GitHub 需要 admin 权限来管理这样的库设置；如果有成千上万的员工入职，手动编辑这个可能是一项极其乏味的工作。

## 好处！

在网飞， [HubCommander](https://github.com/Netflix/hubcommander) 将其用户管理方法标准化，实现了跨开发团队 GitHub repo 权限的自动化。

> *“在没有工具的情况下，管理 GitHub 上的许多用户可能是一个挑战。我们需要提供增强的安全功能，同时保持开发人员的灵活性。因此，我们创建了 HubCommander，以针对网飞优化的方式提供这些功能。”*

HubCommander 提供了这一缺失的环节，让管理员能够快速授予权限。HubCommander 设计时考虑到了 ChatOps，因此很容易嵌入到聊天中。因此，特权 GitHub 组织管理任务可以从 Slack 通道执行，“而无需向您的 GitHub 组织成员授予管理或所有者特权。”

## 使用中枢命令器

要使用 HubCommander，首先要有 **Python 3.5+** 、 **Slack** 、一个 **GitHub 组织**和一个**拥有所有权级别权限的 GitHub bot 用户**。

接下来，安装了 HubCommander **的 Slack channels】可以调用`!help`来返回一个机器人命令列表:**

![](img/4f9503b24142f10bf9925ee1ab33014a.png)

Source: Netflix

例如，要创建一个 repo，只需使用命令`!CreateRepo`:

![](img/16262dd93957aba2f72562fef0530e12.png)

Source: Netflix

使用 HubCommander 还具有安全优势，因为它减少了授予每个用户的 GitHub API 权限数量——减少攻击媒介本质上增加了安全性。关于安全性的另一点是 HubCommander 与用于额外认证的 **Duo** 的集成:

![](img/7f0bf1dc0d2be87c7c3ff9884d01a1e6.png)

Source: Netflix

[HubCommander 功能](https://github.com/Netflix/hubcommander#features)的总列表包括:

*   知识库创建
*   知识库删除
*   知识库描述和网站修改
*   授予外部协作者对存储库的特定权限
*   存储库默认分支修改
*   存储库 PR 列表
*   存储库部署密钥列表/创建/删除
*   存储库主题创建/删除
*   存储库分支保护启用/禁用
*   在 GitHub repo 上启用 Travis CI
*   通过 Duo 使用 2FA 保护命令

## 使用 ChatOps 自动化 GitHub

如果您的代码驻留在多个 Git 存储库中，比如网飞，那么有一种方便的方法来配置所有实体的权限就变得非常必要。有了在 GitHub 存储库上执行操作任务的机器人，网飞受益于自动操作和更广泛的团队访问，增加了其敏捷目标:

> “管理开销的减少极大地简化了我们的开源工作。”

网飞有三个开发渠道(一个核心的网飞 OSS，Spinnmaker 和一个新想法的 skunkworks 项目)。因此，跨组织拥有一致的权限模型可以减少摩擦。此外，由于网飞与第三方合作，如承包商或其他开源贡献者，HubCommander 也是维护安全的有效方式。

## 最后的想法

网飞认识到 ChatOps 方法越来越受欢迎，并引用了其他好处，如团队透明度、每个事件的时间戳和自助服务性质——所有这些都是在其开发工具中采用 ChatOps 策略的原因。

HubCommander 似乎是 GitHub 库管理的一个很好的 ChatOps 工具。然而， [GitHub Actions](https://github.com/features/actions) (在撰写本文时仍处于测试阶段)是一项新功能，它将帮助开发工作流，为 GitHub 操作职责本身提供自动化。这可能会引发替代机器人的开发，特别是在响应事件的工作流方面。

目前，有了 HubCommander 这样的开源工具，某些 GitHub 的任务可以加快，刺激了一种更有效的管理文化，以减少多余的任务。虽然乍一看，GitHub 存储库管理的简写似乎不是一个优先事项，但它可以极大地减少操作上的麻烦。

— [比尔·多菲尔德](https://devops.com/author/bill-doerrfeld/)