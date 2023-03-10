# 1Password 推出开发人员工具来提升体验和工作效率

> 原文：<https://devops.com/1password-launches-developer-tools-to-enhance-experience-and-productivity/>

*新特性将帮助开发人员以更少的摩擦编码和部署更安全的软件到生产中*

**多伦多，2022 年 3 月 15 日—**[1 密码](https://c212.net/c/link/?t=0&l=en&o=3422412-1&h=527337044&u=https%3A%2F%2F1password.com%2F&a=1Password)，以人为中心的安全和隐私领域的领导者，今天推出了开发者工具，这是一套旨在帮助开发者在开发工作流程中轻松、安全地生成、管理和访问机密的功能，从 Git 开始。开发人员工具将有助于简化复杂的流程并改进安全实践，以确保数据受到保护，而不会减慢开发进度。它还将为开发人员提供安全访问所需秘密的途径，无论他们身在何处，也不管他们使用的是什么设备。

“开发人员在构建和部署安全软件时会遇到很多复杂性，安全性和便利性似乎是不可调和的，”1Password 的首席产品官兼新兴解决方案总经理阿克谢·巴尔加瓦说。1Password Developer Tools 旨在通过让复杂的安全流程变得更加方便，让安全的事情变得更加简单，从而让他们的生活变得更加轻松

我们的“[隐藏在众目睽睽之下](https://1password.com/resources/risks-of-mismanaging-corporate-secrets/)”研究报告发现，在 IT/DevOps 公司中，四分之一(25%)的员工在十个或更多不同的地方拥有秘密，并通过电子邮件和 Slack 等不安全的渠道与同事分享。此外，61%的项目因机密管理不善而延期，三分之一(36%)的 IT/DevOps 员工表示，他们将通过不安全的渠道共享机密，以提高工作效率和速度。

为了效率而偷工减料可能很诱人，但这样做会使个人和企业面临潜在的安全漏洞。除了保护个人密码和信息之外，开发人员工具还将提高开发人员的工作效率，在一个应用程序中实现 SSH 密钥的快速生成、通过命令行界面(CLI)使用生物认证和安全机密管理无缝访问数据。1 在测试期间测试这些功能的 Password 客户有积极的反馈可以分享:

*   “所有在不同机器上交换密钥、从代理添加和删除密钥、从密钥输入密码短语的麻烦，现在都变成了一次生物认证。这才是宋承宪应该有的样子，牛逼！”–Marcel kers ten，ComLine GmbH 的软件开发人员

*   “新的 1Password CLI 使我们的 web 开发团队能够以比以前更安全的方式节省同步密码和 API 密钥的时间。我强烈建议任何 web 开发团队考虑使用 1Password CLI 工具来提高安全性和效率。”–Craig Haseler，TechSource 的项目经理

*   “SSH 密钥管理是我多年来一直要求的 1 密码功能！谢谢团队！”–克里斯蒂娜·沃伦，高级云倡导者

**SSH 密钥管理**

开发者只需点击几下鼠标就可以生成、存储和使用 SSH 密钥。为了帮助避免错误，1 浏览器的密码将自动将其公钥填充到热门网站，包括 GitHub、GitLab、BitBucket 和 Digital Ocean。然后，通过内置的 SSH 代理，用户可以将代码推送到 GitHub，并通过简单地扫描他们的指纹来验证终端中的其他 SSH 工作流，从而事半功倍地提高安全性。开发人员不再需要记住或键入密钥密码、手动将密钥复制到新设备或在磁盘上存储文件，从而避免了 SSH 密钥的弱加密和其他安全风险。

**带生物识别解锁功能的 CLI 2.0**

借助改进的 CLI(包括改进的语法)和新的生物识别解锁功能，开发人员可以在终端中快速管理机密、配置用户或自动化工作流，而无需切换开发工具或手动输入密码。Developer Tools 还通过 CLI inject 和 run 命令简化了密钥管理，允许开发人员使用秘密引用进行编码，这些秘密引用在运行时替换他们 vault 中的实际 API 密钥。

**机密管理**

开发人员无需硬编码机密或将它们存储在不安全的明文、配置文件或电子表格中，而是可以在他们首选的工具和工作流程中的一个位置管理和访问他们的机密。将机密存储在加密的保险库中，并作为几种默认项目类型之一(包括 API 凭据、AWS 帐户、数据库、服务器或 SSH 密钥)将有助于防止机密泄露造成的破坏。Developer Tools 还通过在整个团队中提供对秘密的安全访问来促进协作。对于希望自动化基础架构机密的组织来说，这些工具继续建立在[机密自动化](https://www.prnewswire.com/news-releases/1password-launches-secrets-automation-and-makes-acquisition-to-protect-infrastructure-secrets-301267859.html)之上。

要了解更多关于开发者工具和包含的特性集的信息，请访问我们的网站。您也可以访问我们新的[开发者文档门户](https://developer.1password.com/)了解更多信息。

**关于 1 密码**

1Password 以人为本的安全方法确保人们在工作和家庭中的安全。这是唯一从头开始构建的解决方案，使任何人——无论技术熟练程度如何——都能够在数字世界中无所畏惧、无所摩擦。该公司的密码管理和凭证安全平台受到超过 100，000 家企业的信任，包括 IBM、Slack、Snowflake、Shopify 和安德玛。1Password 保护全球数百万个人和家庭的最敏感信息，帮助消费者和企业在更短的时间内完成更多工作，同时确保安全性和隐私。在 1Password.com 了解更多信息。