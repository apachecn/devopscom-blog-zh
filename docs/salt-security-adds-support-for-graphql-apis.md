# Salt Security 增加了对 GraphQL APIs 的支持

> 原文：<https://devops.com/salt-security-adds-support-for-graphql-apis/>

Salt Security 扩展了其保护应用程序编程接口(API)的平台，以包括对使用 GraphQL 构建的 API 的[支持。](https://salt.security/press-releases/salt-security-introduces-api-security-protection-for-graphql-apis?)

GraphQL 是一种用于 API 的开源数据查询和操作语言，最初由脸书开发。与目前广泛使用的 REST APIs 相比，它提供了一种更有效的方法来查询数据。

Salt Security 首席产品官 Elad Koren 表示，在 Salt Security API 保护平台上添加对 GraphQL 的支持以及对 REST APIs 的现有支持，将使安全团队有可能发现这些 API，减少数据泄露，阻止攻击并消除漏洞。Salt 平台解析每个 GraphQL 查询的复杂结构，以识别唯一的对象实体，然后使用这些对象实体来创建所采用的 GraphQL APIs 的完整清单。

Koren 指出，由于独特的调用和响应格式，使用 GraphQL 构建的 API 更难保护。他说，网络犯罪分子还可以利用嵌套查询和查询批处理等 GraphQL 功能来发起分布式拒绝服务(DDoS)攻击。

许多开发人员倾向于认为，由于 GraphQL 相对较新，大多数网络罪犯主要关注利用 REST APIs。然而，随着越来越多的开发人员采用 GraphQL，网络犯罪分子开始找到利用 API 的方法只是时间问题，这些 API 可能不如许多组织已经知道如何保护的 REST APIs 安全。

Salt 安全平台本身基于一个大数据引擎，该引擎采用机器学习算法和其他形式的人工智能(AI)来实时识别攻击。它创建了一个基准来识别合法的系统行为，同时防止网络犯罪分子使用渗透测试工具来执行侦察。

![](img/075ea807a4c1570469f5bb59a79c785c.png)

从 DevOps 的角度来看，Salt Security API Protection Platform 与吉拉和 Slack 等工具相集成，除了帮助跟踪票证以确保实施补救修复之外，还可确保将补救细节发送给正确的开发团队。它还可以与 Splunk 和 Sumo Logic 等供应商提供的安全信息事件管理(SIEM)平台集成，以便为开发人员和安全运营团队提供事件响应。

大多数 IT 团队不会在一夜之间用基于 GraphQL 的 API 替换 REST APIs。然而，很快就会有足够多的基于 GraphQL 的 API 来保证额外的安全措施。不太清楚的是，与安全运营团队相比，DevSecOps 团队将在多大程度上实施这些安全措施。

然而，无论如何，随着组织推出新一代基于微服务的应用来推动任务关键型数字业务转型计划，需要保护的 API 数量正在迅速增加。每个微服务都有自己的 API，需要构建并保护。不幸的是，大多数 API 都是由开发人员开发的，他们并不总是对安全性有最高的评价。因此，当 API 安全的更多责任转移到开发人员身上时，许多安全团队会被建议确保每个被部署的 API 都是完全安全的。