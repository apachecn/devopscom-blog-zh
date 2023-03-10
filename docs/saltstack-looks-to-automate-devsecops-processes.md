# SaltStack 希望自动化 DevSecOps 流程

> 原文：<https://devops.com/saltstack-looks-to-automate-devsecops-processes/>

SaltStack 今天宣布，它已经[将其自动化框架](https://www.prnewswire.com/news-releases/saltstack-enterprise-6-3-improves-it-monitoring-capabilities-vulnerability-management-workflows-and-risk-based-vulnerability-remediation-301083578.html)与各种第三方安全平台集成，以进一步采用最佳 DevSecOps 流程。

SaltStack 产品管理总监 Mehul Revankar 表示，SaltStack Enterprise 的 6.3 版本提供了与 Splunk、Tenable、Qualys、Rapid7 和 Kenna Security 产品的集成。使用 Tenable、Qualys 和 Rapid7 的工具进行漏洞扫描所生成的数据可以直接导入 salt stack Enterprise[以通知自动化的 DevSecOps 流程](https://devops.com/survey-surfaces-root-causes-of-devsecops-tension/)，而与 Kenna Security 的集成使得基于风险级别的漏洞修复自动化和优先级排序变得更加容易。

Revankar 表示，后一种能力至关重要，因为不应仅根据漏洞的严重性来确定补救工作的优先顺序。他说，例如，可能会在位于防火墙后的应用程序中发现漏洞，但如果该应用程序不提供对 web 的访问，则组织可能会决定不立即修补该漏洞，不管其严重性如何，因为违规的风险仍然相对较低。

他补充说，这些功能将使 SaltStack Enterprise 成为在 DevSecOps 流程环境中提供安全编排、自动化和响应(SOAR)功能的基础，使其更容易将网络安全纳入更大的剧本环境中，以实现 it 管理的自动化。

Revankar 指出，大多数行动手册将由 DevOps 团队与网络安全专业人员合作开发。

除了改进 DevSecOps 流程，SaltStack 还希望通过提供与 Prometheus 的兼容性，使 Splunk 和 Datadog 等外部应用程序更容易使用其框架生成的数据，Prometheus 是在云本地计算基金会(CNCF)的支持下开发的开源 it 监控工具。SaltStack Enterprise Splunk 附加工具已添加到 Splunkbase 存储库中。

SaltStack 还提供了一个性能和健康仪表板，使 DevOps 团队能够跟踪使用 Prometheus 数据格式显示的 25 个 SaltStack 企业指标。

![](img/5608e0a5d055a42c3106b372ca0882e5.png)

SaltStack Enterprise 所基于的开源 Salt 框架已经成为自动化 IT 流程的热门选择。因为它是基于 Python 的，就编程专业知识而言，采用 Salt 的障碍比其他编程语言要低。因此，越来越多的 IT 运营团队倾向于学习 Python 来利用 Salt 实现流程自动化。

像大多数采用开源商业模式的供应商一样，SaltStack 通过企业版扩展了 Salt 的功能，它既扩展了 Salt 的功能，又提供了商业支持。

随着各种规模的组织寻求最大限度地利用其有限的网络安全资源并削减成本，对 IT 自动化的兴趣正在上升。SOAR 形式的 IT 自动化提供了一个机会，可以在不增加 IT 组织规模的情况下更广泛地应用网络安全策略。

当然，挑战在于拥有构建剧本所需的专业知识。在开源框架的情况下，许多剧本在像 Salt 这样的社区成员之间共享。不管这些行动手册是如何获得的，很明显，随着 it 变得越来越复杂，大多数 IT 组织都不会没有它们。