# 以 DevOps 的速度保护 API

> 原文：<https://devops.com/securing-apis-at-the-speed-of-devops/>

在 2021 年 DevOps 报告中，83%的 IT 决策者告诉 [傀儡](https://www.globenewswire.com/en/news-release/2021/07/20/2265754/0/en/2021-State-of-DevOps-Report-Finds-It-s-Not-Tech-but-Culture-that-Keeps-Teams-Stuck-in-the-Middle-of-their-DevOps-Evolution.html) 他们的组织正在实施 DevOps 实践，以提高软件质量、交付速度和系统安全性。然而，这些 DevOps 组织在它们的进化阶段上有所不同。例如，处于旅程中间阶段的受访者报告说，不明确的责任和不充分的反馈循环等文化障碍使他们难以继续他们的 DevOps 旅程并加入高度进化的组织行列。这些障碍有助于解释为什么 97%的高进化组织已经将自动化应用到他们的竞争任务中，相比之下只有三分之二的中级团队和四分之一的低进化团队。

### API 对 DevOps 的重要性

对于任何组织的开发运维之旅来说，自动化的普及都与应用编程接口(API)的重要性息息相关。用 [IBM](https://www.ibm.com/cloud/learn/api) 的话说，API“使公司能够向外部第三方开发者、商业伙伴和公司内部部门开放其应用的数据和功能。因此，API 使得不同公司的服务和产品能够以简化和/或增加用户功能的方式相互通信。

也就是说，用户并不是 API 的唯一受益者。DevOps 团队也是如此。许多团队成员在日常工作中处理日益自动化的流程，因此他们需要 API 来帮助他们部署和配置基础设施。[API 还可以帮助 DevOps 团队](https://devops.com/apis-and-devops/)在运行时获得关于应用的详细信息 。 DevOps 员工 可以利用这些洞察力在问题导致中断之前主动解决问题。

### API 和 DevOps 的安全障碍

尽管有这些好处，API 和 DevOps 也面临着安全挑战。当代计算机服务公司(CCSI)确定了组织在开发运维过程中可能遇到的几个安全障碍。这些包括以下:

**快速的开发过程** **:** DevOps 引入了更快的软件交付速度。在努力跟上这种需求的过程中，开发人员可能会犯编码错误，使应用程序容易受到攻击。如果没有及时的安全审查，这些易受攻击的产品和服务可能会投入生产，给攻击者提供了利用这些缺陷并试图访问受影响客户的数字资产的机会。

**协作差** **:** 没有开发和运营的协作，任何 DevOps 之旅都不会成功。当缺乏联合流程时，这些团队可能会固守自己的筒仓。例如，如果开发和运营没有就他们的凭证、令牌、SSH 密钥和其他秘密的管理进行沟通，这种工作方式可能会留下安全漏洞。

这些安全挑战可能会蔓延到 API 中。 [开发的速度](https://devops.com/api-sprawl-a-looming-threat-to-digital-economy/)加上糟糕的团队沟通可能会产生同一个 API 的多个版本。这种冗余造成了所谓的 API 蔓延，这是一种组织的 API 数量和范围呈指数增长的现象。API 蔓延有其自身的障碍，包括维护困难和损坏的客户端，这些问题为攻击者提供了更多渗透组织系统的机会。这个现实有助于解释为什么 2020 年 91%的企业经历了一次 API 安全事件 以及为什么 2021 年中期 恶意 [API 流量增长了 300%](https://securityboulevard.com/2021/07/api-attack-traffic-grew-300-in-the-last-six-months/?__hstc=48761529.fdf74b0d71b4d125f029ed63ce4aa0fd.1644225583555.1644225583555.1644229874714.2&__hssc=48761529.1.1644229874714&__hsfp=2525351468) 。

### 组织如何应对这些安全挑战？

为了回答这个问题，我们回头看看高度发展的 DevOps 组织在做什么。大多数组织都在关注 发展 。在 Puppet 的报告中，51%的受访者表示他们正在将安全性集成到他们的 DevOps 需求中，更多人表示设计(61%)和构建(53%)也是如此。另有 52%的调查参与者表示，他们正在将安全性纳入他们的测试。相比之下，中级和低级的组织主要在准备生产系统审计的过程中，或者当他们了解到影响生产的问题时，从事安全工作。

除了这些关注领域，组织还需要强调运行时保护。Salt Security 同意这种说法， [注意到](https://salt.security/blog/api-security-checklist) 组织如何需要“安全测试您的 API，但要知道，您还需要运行时保护来捕捉没有经过标准构建过程的更改和测试工具没有设计来发现的滥用。”

最后，组织需要将视为文化变革。他们可以通过将安全责任分配给 DevOps 团队中的一个人来做到这一点。这样做将有助于确保团队在工作中不会忽视安全性。同时，组织可以为他们的开发人员进行安全意识培训，并定期邀请开发和运营人员分享他们的故事、优先事项和成功经验。这将有助于促进协作，从而最大限度地减少跨系统的 API 冗余和 API 蔓延。