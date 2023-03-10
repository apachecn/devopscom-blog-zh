# GrammaTech 为 CodeSentry 增加了 SBOM 分析功能

> 原文：<https://devops.com/grammatech-adds-sbom-analysis-capability-to-codesentry/>

GrammaTech today [更新了其 CodeSentry 代码检查平台](https://www.businesswire.com/news/home/20220118005071/en/GrammaTech-CodeSentry-Enhances-Software-Bill-of-Materials-Capabilities-to-Improve-Software-Supply-Chain-Security),增加了通过分析应用程序二进制文件来创建软件材料清单(SBOM)的功能。

GrammaTech 的技术产品管理总监 Walter Capitani 表示，CodeSentry 的 3.0 版本利用了该公司用于二进制软件组成分析的算法，使组织能够在一系列备受瞩目的漏洞出现后，更好地解决软件供应链问题。

该工具可以通过与基于风险的安全性的 [VulnDB 数据库](https://www.riskbasedsecurity.com/)集成，应用于商业软件和开源组件，该数据库是为跟踪安全问题而创建的。

![GrammaTech](img/e1601caf79320dbbfc803dc2012f6219.png)

在拜登政府最近发布行政命令，要求联邦机构只能使用 SBOM 附带的软件之后，人们比以往任何时候都更加关注创建 sbom。然而，大多数组织无法访问他们所使用的应用程序中使用的源代码。GrammaTech 使组织能够通过分析应用程序中的二进制代码来生成 SBOM，从而解决这个问题。

Capitani 说，该报告不仅确定了应用程序中的所有组件，还列出了与正在使用的组件版本相关的所有已知漏洞。CodeSentry 还将列出其他常见软件产品和可能受相同漏洞影响的版本，以及已修复问题的软件版本或未受这些漏洞影响的组件版本。

几乎所有的软件应用程序都包含第三方和开源组件，这些组件在软件供应链中产生了盲点。事实上，正是这个问题使得修复零日应用程序漏洞如此具有挑战性；尤其是当它们出现在诸如广泛用于 Java 应用程序的 Log4j 这样的日志管理工具中时。

GrammaTech 正在为二进制软件组合分析(SCA)工具提供案例，该工具使 DevOps 团队能够在应用程序部署到生产环境之前解决漏洞问题。然而，与此同时，安全和法规遵从性团队现在可以使用相同的工具来确定应用程序部署到生产环境后组织可能面临的风险级别。Capitani 指出，后一种能力尤其重要，因为零日漏洞通常在应用程序部署到生产环境中很久之后才会被发现。

无论采用何种方法，更好地保护[软件供应链](https://devops.com/?s=supply+chain)的需求现在是一个主要的 IT 问题，最终将鼓励更多的组织采用 DevSecOps 最佳实践来更好地保护应用程序。当然，挑战不仅仅是支持那些实践的需要，还要为开发人员提供他们将实际用来实现那些实践的工具。这些努力的成败不仅取决于工具的功效，还取决于它在整体开发人员体验中的适合程度。毕竟，如果对于一般开发人员来说太难使用，世界上最伟大的工具仍然会受到冷落。