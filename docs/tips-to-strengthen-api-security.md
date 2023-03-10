# 使用这些技巧和模式增强 API 安全性

> 原文：<https://devops.com/tips-to-strengthen-api-security/>

如果你没有注意到，数字组织正在构建越来越多的[API](https://devops.com/?s=APIs)。在撰写本文时，ProgrammableWeb 跟踪了超过 23，000 个公共 web APIs，到 2023 年，API 市场估计价值[51 亿美元。使用 API 进行构建增加了内部互操作性，减少了开发时间，并且可以极大地扩展产品功能。简而言之，API 的价值在上升。然而，开放 API 带来了安全警告，如果不解决，可能会导致严重的违规，抵消这些好处。](https://www.prnewswire.com/news-releases/api-management-market-worth-5-1-billion-by-2023---exclusive-report-by-marketsandmarkets-300810744.html)

我最近与 Salt Security 的 Roey Eliyahu 进行了交谈，以了解他对支持 API 的公司的主要安全问题的看法，以及组织如何保护他们的服务。简而言之，他建议彻底编目和理解你的 API 清单，为法律挑战而设计，并减轻 OWASP 的 10 大 API 安全漏洞。

## API 安全性面临的挑战

API 被称为“网络犯罪的下一个前沿”的确如此，因为 API 漏洞几乎每天都在出现。以最近发生在[思科系统](https://tools.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-ios-webui-priv-esc-K8zvEWM)、 [Shopify](https://techcrunch.com/2020/09/23/shopify-data-merchant-breach/) 、[脸书](https://apisecurity.io/issue-102-vulnerabilities-facebook-campaign-apps-creating-defensible-apis/)、[美国总统竞选应用](https://www.websiteplanet.com/blog/trump-app-vulnerability-report/)、 [GCP](https://www.ezequiel.tech/2020/08/leaking-google-cloud-projects.html) 的 API 漏洞为例。最臭名昭著的可能是 Equifax 违规——没有对传入的 API 调用强制执行格式导致了大规模的数据违规，使该公司付出了[7 亿美元的诉讼费用](https://www.cbsnews.com/news/equifax-data-breach-settlement-equifax-will-pay-700-million-to-settle-data-breach-lawsuits/)。

那么，为什么最近 API 违规事件增加了呢？嗯，几年前，API 很少。而且，这些旧的服务暴露了不太敏感的数据。如今，公司通常有更多的 API。例如，银行应用程序可能会暴露数百个极具价值的端点，这对黑客来说非常有吸引力。

公司也为不同的受众开发 API:smart bear 在 2020 年进行的一项研究发现，72%的公司同时开发内部*和*面向外部的 API。这些 API 可以轻松保存数百个参数，并且随着每一个新方法的加入，公司的潜在攻击面会大大增加。

## 保护 API 的 3 个步骤

为了缓解上述 API 安全问题，Eliyahu 建议采取三个主要步骤:了解您的 API 库存，根据隐私政策和数据隐私法规进行审计，并像老鹰一样跟踪最紧迫的 API 漏洞。

### 了解您的 API 库存

“你需要大量的 API 来了解你的攻击面，”Eliyahu 说。许多 API 提供者用 OpenAPI 定义记录他们的 API。但是，这些文件并不总是与生产现实相匹配——它们可能是手动生成的或者省略了某些方法。“在每一个组织中，实际部署的 API 与库存的 API 之间存在高达 40%的差距，”他说。通过维护更清晰的 API 清单，组织可以避免未受保护的[影子 IT](https://devops.com/5-steps-to-avoid-shadow-it-around-low-code/)。

### 包括法律审计

对 API 的更改可能会导致收集用户信息的方式发生变化。涉及敏感数据的更新可能违反隐私政策或法规，如 GDPR。Eliyahu 说:“有了清单后，你需要手动映射所有参数。他建议对你的 API 清单进行一次法律审计，并建立一个可重复的测试过程，插入一个连续的交付管道。

当 API 团队发布新的更新时，他们必须在开发流程的早期考虑安全性和法律含义。“现在，有了 CI/CD，这些变化必须非常频繁地发生，”他指出。

### 观看 OWASP API 安全性前 10 名

有许多已知的 API 安全漏洞。例如，可能没有适当的授权，密钥可能被暴露，未到期的令牌可能被劫持等等。值得庆幸的是，OWASP 汇编了一个顶级 API 安全漏洞资源，Eliyahu 和 API 经济中的许多其他人都支持这个资源。“世界应该采取行动来解决 OWASP 问题，”他说。这些漏洞如下:

1.  破坏对象级授权
2.  用户身份验证失败
3.  过多的数据暴露
4.  缺乏资源和速率限制
5.  功能级别授权中断
6.  批量分配
7.  安全错误配置
8.  注射
9.  资产管理不当
10.  记录和监控不足

## 利用人工智能超越“打地鼠”

堵住上面这些洞，就是一个好的开始。然而，这些只是针对已知模式的防御措施；它们不能帮助您防范细微的攻击类型。理想情况下，安全系统应该在网络攻击开始之前就阻止它们。

然而，Eliyahu 认识到在如何监控 API 方面存在很大的差距。他说，组织“没有适当的工具来知道谁在寻找漏洞”。“工具通常没有那么先进。他们主要寻找注射和已知模式。”

想象一个黑客在探测一个 API。他们可能会通过反复试验、测试未记录的端点、发送格式错误的请求等方式来实现这一点。“他们需要探测几个小时或几天才能找到东西，”Eliyahu 说。如果人工智能可以在几分钟或几秒钟内检测到这些奇怪的尝试，它可以大大降低风险。

因此，安全解决方案应该利用大数据和人工智能来创建典型行为的基线，然后在任何恶意探测开始的那一毫秒阻止恶意活动。Eliyahu 说，这样的安全人工智能必须考虑几十种行为，例如，API 是如何被访问的？使用了哪些参数？参数之间有什么关系？API 调用的流程是怎样的？可以公开什么类型的数据？

人工智能支持的 API 安全监控可以通过参考使用机器学习不断完善的知识库，立即暂停被视为“异常”的行为，而不是等待违规行为发生。因为，如果你只是阻止恶意行为者，而不知道如何提高 API 的安全性，“你只是在玩打地鼠游戏，”Eliyahu 说。

## DevSecOps 需要预先考虑 API 安全性

Gartner 的分析师 Mark O'Neil 预测，到 2021 年，[25%拥有公共 API 的组织将停止或重启其公共 API 战略](https://www.linkedin.com/pulse/end-beginning-api-economy-mark-o-neill/)，称安全问题是一个常见的突破点。API 现在是许多应用程序开发的核心。然而，如果没有适当的 DevSec 提案，团队将面临浪费精力和代价高昂的违规风险。

总而言之，下面是我们关于 API 安全性的提示:

*   **确保一切都有据可查**:如果没有记录，就不能审核原料药库存。影子 API 增加了攻击的可能性。
*   **观看 10 大 OWASP 漏洞**:这些是 API 安全的基础。虽然不是万灵药，但它们提供了一个起点。
*   **建立安全和法律审查流程**:确保未经适当的安全审查不得部署 API。创建插入持续开发过程的验证系统，这样新版本就不会违反隐私政策。
*   每个 API 都是独一无二的:另一件需要记住的事情是每个 API 都是独一无二的。因此，API 安全监控还需要将更多的上下文融入到独特的业务逻辑中。
*   **持续监控你的 API**:持续搜索任何人*寻找*漏洞。
*   **删除不推荐使用的 API**:删除旧的 API 版本。"你需要一种机制来识别和删除旧的 API 版本."否则“僵尸 API 会咬你的！”
*   从你阻挡的攻击中学习:不要只是玩打地鼠游戏。"你需要一种机制来从你阻止的攻击中学习."