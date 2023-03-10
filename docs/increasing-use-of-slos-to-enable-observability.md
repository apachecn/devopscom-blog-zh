# 增加 SLO 的使用，以实现可观察性

> 原文：<https://devops.com/increasing-use-of-slos-to-enable-observability/>

在大多数 IT 和运营部门中，可观察性是一个不断发展的学科。为了更快地发布稳定的软件，运营商需要持续了解性能、正常运行时间和可用性等指标。因此，工程师们正在全面增加对[服务级别目标](https://devops.com/whats-the-difference-between-sli-sla-and-slo/)(SLO)的使用——最近的一项研究发现，82%的公司正在增加对 SLO 的使用。

SLO 支持深入了解特定应用的性能，通常由[现场可靠性工程师](https://devops.com/day-in-the-life-of-a-site-reliability-engineer-sre/) (SREs)使用，以确保质量并避免服务中断。不仅如此，各个团队还将 SLO 与业务的各个方面联系起来，以降低成本并帮助直接决策。但是，尽管许多环境都具有可见性，但仍然存在差距。

Nobl9 最近发布了一项针对 IT 专业人士和高管的[全球调查](https://www.nobl9.com/the-state-of-service-level-objectives)，该调查跟踪了 2022 年服务水平目标的状态。下面，我们将看看报告中的关键发现，并考虑它们对 SLO 状态和总体可观测性的意义。

## 可观测状态和 SRE

总的来说，跨组织的站点可靠性工程仍然是成熟的。虽然只有 31%的公司采用了 SRE，但它预计未来会有很大的增长，因为 46%的公司表示他们计划在未来采用 SRE。

这些运营商现在面临许多[云原生可观察性工具](https://containerjournal.com/features/the-state-of-cloud-native-observability-tools/)，这些工具以指标、日志和跟踪的形式产生了[数据海](https://containerjournal.com/features/how-to-avoid-drowning-in-cloud-native-observability-data/)。整整 39%的公司使用 6 到 10 种观察和监控工具，35%的公司使用 11 种以上。

现在部署了这么多工具，谁在使用这种可观察性和监控数据呢？也就是说，在 74%的公司中，可观测性数据支持运营需求。运营团队最有可能使用 SLO 来监控正常运行时间、性能和整体效率。在运营团队之后，安全团队也使用这种可观察性数据(71%)，这是有意义的，因为 SLO 可以通知事件响应。接下来的其他领域是客户支持、合规性和容量规划。

一个有趣的发现是，只有 42%的公司使用 SLO 来遵守服务级别协议(SLA)。这表明 SLO 最常用于内部优化和决策制定。

## 混合环境使可见性复杂化

公司大多跟踪 SLO，以提高他们对网络(83%)、数据库(76%)和应用程序(75%)的可见性。其他主要领域包括私有云环境和传统计算安排。但是，尽管可观察性是一种趋势，组织仍然缺乏对整个体系的完全可见性。

值得注意的是，近一半(46%)的受访者表示，他们的监控和可观察性工具无法提供对公司所有 IT 资产的*全面*可见性。例如，只有 45%的公司能够看到他们的容器，只有 35%的公司能够看到他们的微服务架构。

缺乏[全栈可见性](https://devops.com/could-full-stack-observability-help-lessen-its-burden/)可能会因为混合云和多云条件的增加而变得复杂，因为 78%的人表示混合云环境会使监控基础架构变得更加困难。

## 跟踪 SLO 的好处

该报告将 SLO 定义为“随着时间的推移，为给定系统、应用程序或服务设定的性能和可用性目标。”对于遵循这些目标的组织来说，好处是显而易见的-它们可以帮助提高性能、指导决策并帮助避免停机。

因此， *70%的公司目前正在以某种方式使用 SLOs】。以下是跟踪 SLO 的一些好处:*

*   **提高微服务性能** : 87%的受访者表示对微服务架构使用 SLO 可以提高服务性能。
*   **实现全栈可观察性** : 58%的人表示他们公司的一些 SLO 被映射到业务运营。
*   **改善业务决策** : 91%的人认为使用 SLO 有助于推动更好的业务决策。
*   **防止服务中断** : 67%的受访者表示他们的公司借助 SLO 阈值警报防止了业务中断。
*   **减少开支** : 90%的受访者表示 SLO 为他们的公司节省了资金。

## 最后的想法

比以往任何时候都有更多的团队在跟踪服务级别目标。大多数没有使用 SLO 的公司(71%)现在计划很快采用它们。数据表明,[可观察性市场](https://containerjournal.com/features/7-open-source-cloud-native-tools-for-observability-and-analysis/)是一个不断发展的领域，有发展的空间。同样的道理也适用于 [SRE 的角色](https://devops.com/site-reliability-engineering-sre-comes-of-age-in-2022/)。

然而，值得指出的是，并非所有的公司都会采取完全相同的角色或监控程序。因此，在*谁在使用 SLO 以及如何应用 SLO 方面，可能会继续存在差异。无论如何，这项研究表明，调查 SLO 有可能在许多方面有益于软件生命周期。*

这项名为“采用 SLO 增长以提高可见性并推动业务改善”的研究调查了全球不同行业的 309 名参与者。这项研究由 Nobl9 赞助，由 Dimensional Research 进行。如需了解更多信息，您可以点击下载[报告。](https://www.nobl9.com/the-state-of-service-level-objectives)