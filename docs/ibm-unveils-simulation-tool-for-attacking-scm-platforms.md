# IBM 推出攻击 SCM 平台的模拟工具

> 原文：<https://devops.com/ibm-unveils-simulation-tool-for-attacking-scm-platforms/>

在[黑帽美国 2022](https://www.blackhat.com/us-22/) 大会上，IBM 今天透露，它正在提供一个工具包，用于对源代码管理(SCM)平台发起模拟攻击。该工具包是作为概念验证而推出的。

IBM Security 的 X-Force Red arm 的对手模拟负责人布雷特·霍金斯(Brett Hawkins)表示， [SCMKit](https://securityintelligence.com/posts/abusing-source-code-management-systems/) 利用大多数 SCM 平台中的 REST 应用程序编程接口(API)功能，使用经过验证的 SCM 平台证书来启动各种类型的攻击模块。IBM 还描述了一系列[攻击场景](https://securityboulevard.com/2022/08/github-zero-day-from-35k-repos-compromised-to-false-alarm/)，模拟工具可用于启动这些场景。

SCMKit 目前可以对 GitHub Enterprise、GitLab Enterprise 和 Bitbucket Server 发起模拟攻击。该套件可以支持侦察、权限提升和持久性攻击模块功能，用于创建个人访问令牌或安全套接字外壳(SSH)密钥。Hawkins 补充说，SCMKit 基于一个模块化框架，使得将来添加额外的模块成为可能。

Hawkins 说，IBM 创建 SCMKit 是为了将更多的注意力集中在一种攻击媒介上，这种攻击媒介可以被用来危害软件供应链。在一系列高调的安全违规事件发生后，拜登政府发布了一项行政命令，要求联邦机构审查其软件供应链的安全性。虽然人们对这个问题的认识比以往任何时候都多，但 Hawkins 指出，人们对识别网络罪犯能够利用的针对 SCM 平台的特定攻击媒介的关注度几乎没有这么高。

目前还不清楚组织在何种程度上对他们首选的 SCM 平台进行渗透测试，因为他们致力于保护软件供应链。然而，用不了多久，测试这些平台的安全性完整性就会变得更加普遍。在某些情况下，组织将自己启动这些测试。在其他情况下，第三方 IT 服务公司将负责启动这些测试。

当然，挑战在于渗透测试技术也经常被网络犯罪分子用来进行侦察。SCMKit 没有发现任何新技术，但它[确实为网络罪犯提供了针对 SCM 平台发起攻击的指南](https://securityboulevard.com/2022/07/are-proof-of-concepts-benefiting-cybercriminals/)。因此，IT 组织应该假设这些类型的攻击在未来几个月会越来越频繁。

无论使用何种工具，网络犯罪分子显然已经意识到软件供应链是 it 的软肋。如今，组织通常将大部分安全工作集中在生产环境上。然而，插入到软件仓库中的恶意软件可以很容易地进入多个下游应用程序。在未来的某一天，恶意软件会接触到一个命令和控制系统，从而使网络犯罪分子能够发起勒索软件攻击或只是窃取数据。该恶意软件还可以在应用程序环境中横向移动，造成额外的破坏。

对应用程序安全性威胁的全面了解可能还需要一段时间，但是随着越来越多的组织采用 DevSecOps 最佳实践来保护其软件供应链，几乎可以肯定的是，渗透测试将在 DevOps 环境中变得更加普遍。