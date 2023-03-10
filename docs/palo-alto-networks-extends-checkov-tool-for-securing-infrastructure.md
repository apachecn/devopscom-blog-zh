# Palo Alto Networks 扩展 Checkov 工具以保护基础设施

> 原文：<https://devops.com/palo-alto-networks-extends-checkov-tool-for-securing-infrastructure/>

Palo Alto Networks】向 Checkov 添加了对 GitHub Actions、GitLab Runners、CircleCI 和 Argo 工作流的支持，Checkov 是一种开源工具，可以扫描以编程方式提供的基础架构以查找错误配置。

帕洛阿尔托网络公司 Prisma Cloud 的 Bridgecrew 产品高级总监盖伊·艾森科特(Guy Eisenkot)表示，目标是更容易保护使用 Terraform 等[基础设施即代码](https://devops.com/?s=infrastructure+as+code) (IaC)工具创建的配置。

他指出，这些新增功能现已成为 Checkov 策略库的一部分，包括基于图形的检查，它提供了一种上下文感知的方法，可以使用一种工具来识别 DevSecOps 工作流中基础架构和应用程序代码内的风险，该工具使 IT 团队能够管理策略即代码。

![](img/e67eb43225dba2a6125814d02d0ebaff.png)

云基础设施的错误配置已经成为一个主要问题。通常，这种基础设施是由很少或没有网络安全专业知识的开发人员以编程方式提供的。因此，网络犯罪分子现在更加积极地扫描错误配置，例如，他们可以利用这些错误配置通过应用程序编程接口(API)泄漏数据或非法访问服务。Eisenkot 指出，Checkov 使得在云基础设施被供应之前，在 DevOps 工作流的上下文中识别那些潜在的安全问题变得更加容易。

在一系列引人注目的违规事件之后，人们更加关注保护软件供应链。拜登政府去年甚至发布了一项行政命令，要求联邦机构审查其软件供应链的安全性。Eisenkot 说，挑战在于大多数组织还没有实现真正以开发人员为中心的方法来确保应用程序的安全性。

一般来说，云平台比内部 IT 环境更安全；然而，如今用于构建和部署云应用的流程显然存在问题。网络安全人员的长期短缺进一步加剧了这一问题，因为大多数组织无法跟上工作负载在云中部署的速度。

随着越来越多的组织也开始采用 DevSecOps 最佳实践，网络安全的整体状况应该会有所改善。挑战在于，无论花费多少时间和精力来教育开发人员，总会有错误被网络罪犯利用。像 Chekhov 这样的策略代码工具使得这些错误不太可能延续到生产环境中。

与此同时，组织需要致力于弥合应用程序开发和网络安全团队之间的长期分歧。历史上，网络安全团队会在电子表格中汇总他们发现的漏洞，然后要求开发人员进行补救。问题不仅在于没有时间解决这些脆弱性，还在于缺乏提供的背景。这些漏洞中的许多往往并不适用于应用程序的部署方式。随着时间的推移，应用程序开发人员开始忽略许多这样的请求，而将精力集中在编写额外的代码上。当然，编写的代码越多，理论上需要补救的漏洞就越多[，直到形成恶性循环](https://devops.com/poor-app-remediation-creates-a-vicious-vulnerability-cycle/)。

当然，一个漏洞最终成为一个关键的漏洞，并成为该规则的例外，这只是时间问题。