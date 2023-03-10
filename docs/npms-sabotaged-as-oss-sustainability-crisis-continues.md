# 随着开放源码软件可持续性危机的继续，国家预防机制遭到破坏

> 原文：<https://devops.com/npms-sabotaged-as-oss-sustainability-crisis-continues/>

当[两个广泛使用的开源节点打包模块(npm)本周被蓄意破坏](https://securityboulevard.com/2022/01/npm-libraries-colors-and-faker-sabotaged-in-protest-by-their-maintainer-what-to-do-now/)时，一场关于小型开源项目可持续性的长期酝酿的辩论超越了理论。

Colors.js 是一个下载量超过 33 亿次的 npm，有超过 19，000 个项目依赖于它。与此同时，Faker 已经被检索了 2.72 亿次，有超过 2500 个项目依赖于它。Colors.js 使组织能够在控制台上打印彩色的文本消息，而 faker 用于生成测试应用程序的假数据。下载了最近发布的 Colors.js 版本的开发人员发现他们的应用程序陷入了一个无限循环，打印出“LIBERTY”“LIBERTY”“LIBERTY”，后面跟着一系列无意义的非 ASCII 字符。与此同时，Faker 也删除了功能代码。

开源软件安全平台提供商 Sonatype 的高级安全研究员 Ax Sharma 指出，这些行为发生在一系列零日漏洞之后，这些漏洞影响了广泛使用的 Java 应用程序日志工具 [Log4j](https://devops.com/?s=Log4j) 。Sharma 首先报告了 Color.js 和 Faker 的更新问题。

从事 Log4j 项目的贡献者小组发现他们自己[创建了多个包更新，以解决常见漏洞和暴露(CVE)列表中不同严重性的漏洞](https://securityboulevard.com/2022/01/ftc-warning-in-wake-of-log4j-secure-your-software-supply-chain/)。夏尔马说，然而，鉴于这些漏洞的严重性，有多少漏洞值得列入 CVE 名单，这是有争议的。

对于较小的开源项目的贡献者来说，这个问题已经成为一个爆发点。这些贡献者认为，较大的组织正在利用他们的努力，而没有对项目做出任何实质性的贡献作为回报，更不用说补偿任何贡献者的时间和努力了。Sharma 解释说，国家预防机制最近的更新基本上是一份抗议声明。

尚不清楚小型开源项目的其他贡献者是否会效仿，但关于这些项目可持续性的辩论已经变得激烈。许多开源软件的贡献者认为使用他们创造的自由软件的组织应该承担保护它的责任。这种“用户小心”的安全方法对于那些没有为他们的努力得到补偿的贡献者来说是可以理解的。然而，当被要求修补被价值数十亿美元的组织使用的开源项目时——并且是在紧急、紧急的基础上这样做——那些志愿贡献者的怨恨会急剧上升。

幸运的是，人们正在努力解决这些问题。开源安全基金会(OpenSSF)是 Linux 基金会的一个分支，[筹集了 1000 万美元](https://securityboulevard.com/2021/10/new-openssf-gm-sets-open-source-security-course/)来帮助维护者采用最佳实践，并更好地保护开源项目免受恶意代码的攻击。[谷歌承诺 100 万美元帮助开源开发者](https://securityboulevard.com/2021/10/google-contributes-1m-to-reward-developers-for-oss-security/)遵守国家标准与技术研究所(NIST)的指导方针，以回应拜登政府最近关于网络安全的行政命令。作为一个由 Linux 基金会管理的试点项目，这项工作是谷歌之前对开源安全做出的 100 亿美元承诺的一部分。

白宫国家安全顾问杰克·沙利文最近也给主要的软件公司和开发者发了一封信，邀请他们讨论提高开源软件安全性的计划。第一步是本月由主管网络和新兴技术的副国家安全顾问安妮·纽伯格主持的为期一天的讨论。在信中，Sullivan 特别指出，虽然开源软件加快了创新的步伐，但其中的大部分是由志愿者维护的。他指出，这现在是一个关键的国家安全问题。

目前还不清楚这场正在出现的开源可持续性危机将如何发展。然而，DevOps 团队可能想要考虑他们对开源项目的依赖程度，开源项目的贡献者可能对他们的工作如何被利用有问题。