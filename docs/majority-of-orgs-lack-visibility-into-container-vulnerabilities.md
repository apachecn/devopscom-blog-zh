# 大多数组织缺乏对容器漏洞的可见性

> 原文：<https://devops.com/majority-of-orgs-lack-visibility-into-container-vulnerabilities/>

今天，第三方应用程序依赖性和多语言软件开发的混合经常使评估风险变得困难。随着许多新的云原生部署模型的出现，发现潜在漏洞可能会变得很棘手。这些威胁表现为 Kubernetes 中的[不安全默认设置](https://containerjournal.com/features/insecure-defaults-remain-a-threat-for-kubernetes/)、威胁容器完整性的、[CVEs](https://containerjournal.com/topics/container-security/methods-to-audit-docker-container-security/)以及其他易受攻击的条件。

填补整个云原生层的空白现在至关重要，以避免暴露数据和违反隐私法规。然而，获得对这些资产的可见性具有挑战性，传统的应用程序安全实践可能无法在云原生环境中实现。

Dynatrace 发布的一份新的 [2021 年 CISO 报告](https://www.dynatrace.com/info/cloud-application-security-ciso-research-1/)“精确、自动的风险和影响评估是 DevSecOps 的关键”，表明全球企业 IT 部门的误报率增加，并且普遍缺乏实时容器运行时漏洞扫描。在接受调查的 700 名 CISOs 中，大多数报告称微服务、容器和 Kubernetes 在其组织中造成了安全盲点。

下面，我们将讨论该研究的主要收获，以了解为什么新的云原生开发模型会留下安全漏洞。我们将考虑 CISOs 如何提高整个云原生 IT 堆栈的安全性，同时仍然获得基于容器的交付模式的回报。

## 云原生安全盲点

采用新的基于容器的技术可能会引入多种微妙的安全隐患。在接受调查的技术领导者中，89%的人报告说微服务、容器和 Kubernetes 在其组织内制造了新的漏洞。

工程师正在发布代码，以保持发布速度，并满足数字创新的需求。在此过程中，28%的 CISOs 表示，应用团队有时会绕过漏洞扫描来加快软件交付。由于这些现实，毫不奇怪，71%的 CISOs 承认他们在投入生产之前不能完全确信代码没有漏洞。

随着一些团队绕过安全预生产，随之而来的是更多的团队在生产期间不应用整体安全扫描*。结果，报告发现，几乎所有组织(97%)都缺乏对运行时漏洞的实时可见性。*

信息过载增加了云原生盲点的数量。该报告计算出，一个组织平均每月收到 2，169 个关于潜在应用程序安全漏洞的新警报。在如此大量的警报中，77%的 CISOs 表示它们大多是误报，而不是实际暴露。

由于极少的测试和大量的误报，组织可能会留下许多未修补的漏洞。更糟糕的是，时间紧迫的开发人员可能缺乏解决已知问题的带宽。

## 交货更快，检测更难

漏洞检测中的许多挫折可能在于向新的工作方式和更快的交付周期的普遍转变。例如，63%的 CISOs 报告称开发运维及敏捷方法使得检测和管理漏洞变得更加困难。

此外，74%的 ciso 表示，漏洞扫描器等传统安全控制不再适合今天的云原生世界，77%的 ciso 同意[自动化](https://devops.com/report-the-state-of-devops-automation/)可能有所帮助。这可能涉及到用更加自动化的方法取代手动部署、配置和管理。其他人同意[安全代码](https://containerjournal.com/features/leveling-up-container-security-with-security-as-code/)是确保高集装箱安全最佳实践所必需的。

更频繁交付的另一个结果是增加了多报。在每月收到的所有安全漏洞警报中，CISOs 报告称只有 42%的警报需要采取措施。更快的发布周期可能会加剧已经拥挤不堪的漏洞检测系统。

## 谁负责漏洞管理？

研究发现，只有 3%的组织能够实时了解集装箱化生产环境中的运行时漏洞。事实上，在 68%的组织中，生产中的漏洞扫描每月只发生一次或更少。

为了弥补这一差距，大多数 ciso 认为管理和响应漏洞的责任不在安全团队，而在应用程序和开发运维团队——85%的 ciso 认为这些团队应该负责漏洞管理。当其他利益相关者提倡增加[全周期开发控制](https://containerjournal.com/features/can-great-dx-enable-full-cycle-development/)并鼓励[跨角色开发思维](https://devops.com/seven-reasons-you-shouldnt-hire-a-devops-engineer/)时，这些发现浮出水面。

将更多的控制权交给开发人员听起来不错，然而，64%的受访者表示，开发人员并不总是有时间在代码投入生产之前解决漏洞。结果，超过四分之一的应用程序团队完全绕过了漏洞扫描。通常，工程团队可能不会经常与安全组同步，并且 [DevSecOps](https://devops.com/6-traits-that-define-devsecops/) 原则还没有在所有组织中普及。

该报告还强调了一个事实，即现有的安全工具往往是无效的；69%的 CISOs 表示安全工具会降低开发速度，因为它们只关注软件交付周期的一个状态。

## 云使用需要安全重新定位

随着云架构的崛起，组织正在采用云原生工具，如微服务、容器和 Kubernetes。还有可能[多工具条件](https://containerjournal.com/editorial-calendar/could-nomad-reignite-orchestrator-wars/)进一步使漏洞扫描过程复杂化。由于要保护的系统比以往任何时候都多，团队可能需要重新定位他们的漏洞检测方法。

Dynatrace 创始人兼首席技术官 Bernd Greifeneder 表示:“云原生架构的使用越来越多，从根本上打破了传统的应用程序安全方法。“这项研究证实了我们长期以来的预期:手动漏洞扫描和影响评估不再能够跟上当今动态云环境和快速创新周期的变化步伐。”

来自 Dynatrace 的全球 CISO 报告“精确、自动的风险和影响评估是 DevSecOps 的关键”调查了 700 名首席信息安全官(ciso)有关漏洞的监控实践。要查看该报告的全部调查结果，您可以在这里下载。