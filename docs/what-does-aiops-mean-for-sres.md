# AIOps 对 SREs 意味着什么？

> 原文：<https://devops.com/what-does-aiops-mean-for-sres/>

说到 AIOps，SREs 似乎有两种想法。一方面，AIOps 的潜力非常令人兴奋。通过自动化复杂的工作流程和故障排除过程，AIOps 可以让您作为 SRE 的生活变得更加轻松。

但另一方面，一些 sre 可能会选择用鄙视和不信任的眼光看待 AIOps。他们可能会认为 AIOps 只是另一个时髦的流行语，并不符合宣传，可能会分散对真正重要的 的 [SRE 工具的注意力。](https://rootly.com/blog/7-essential-tools-for-sres)

哪个视角是对的？sre 应该张开双臂拥抱 AIOps，还是应该抵制营销人员将 AIOps 定位为 IT 行业最新、最伟大的工具创新的努力？

这些都是我们无法明确回答的主观问题，但至少让我们通过研究 AIOps 对 sre 意味着什么来获得一些视角。

## 什么是 AIOps？

如果你关注 it 术语，你可能至少听说过 AIOps 这个术语——它是 IT 运营的人工智能[](https://www.appdynamics.com/topics/what-is-ai-ops)的缩写——它指的是使用人工智能和机器学习(ML)来帮助自动化 IT 运营工作流。

AIOps 背后的重要思想是，通过使用 AI 和 ML 对来自 IT 系统的大量数据进行高级分析，IT 和 SRE 团队可以比使用传统的手动方法更有效地解决复杂的问题。

例如，AIOps 有助于在像 [Kubernetes](https://rootly.com/blog/how-kubernetes-can-both-help-and-hinder-incident-management-teams) 这样复杂的多层环境中发现性能问题的根本原因。或者它可以就如何最好地解决事件提出建议。

AIOps 在 2016 年进入 IT 词汇，当时 [Gartner 创造了术语](https://www.eweek.com/big-data-and-analytics/what-is-aiops/) 。现在，六年过去了，它已经是一个相对成熟的工具领域。

## SREs 如何看待 AIOps

尽管 AIOps 已经存在了一段时间，但似乎还没有很多 sre 接受 AIOps 革命。Catchpoint 在 2021 年的一项调查[](https://devops.com/sres-say-aiops-doesnt-live-up-to-the-hype/)中发现，只有 7.5%的 sre 报告称 AIOps 工具为他们的组织带来了高价值。

目前还不清楚为什么人们对 AIOps 的热情如此之低，但我们推测有几个关键因素在起作用:

*   **AIOps 是一个旧概念的新术语**:许多监控和可观察性工具在很长一段时间内都至少包括基本的 AI 和 ML 分析功能，甚至在工具供应商在其产品上贴上 AIOps 标签之前。sre 可能意识到了这一点，并在某种程度上将 AIOps 视为营销人员重塑实际上并不新鲜的功能的努力。
*   **AIOps 很难实现**:设置 AIOps 工具需要将它与不同的数据源集成，并对其进行定制以适应您的工作流和环境。可能有些 sre 认为这种设置需要付出更多的努力，不值得。
*   AIOps 不能取代人类的洞察力:虽然 AIOps 工具在某种程度上可能有用，但盲目信任基于 AIOps 的分析或建议是不明智的。由于这个原因，一些 sre 可能认为 AIOps 鼓励组织过分依赖自动化工具，而牺牲了只有 sre 才能提供的专家分析和观点。(这与 [将人类的直觉和专业知识置于剧本](https://rootly.com/blog/what-sres-can-learn-from-capt-sully-when-to-follow-playbooks) 之上有时是有道理的类似。)

从 SRE 的角度来看，与 SRE 的传统做法相比，AIOps 可能显得过分夸张、过于复杂和表现不佳。

## SREs 能从 AIOps 中获得什么

SREs 对 AIOps 的警惕是有道理的——但只是在一定程度上。重要的是不要让对 AIOps 局限性的怀疑变成根本不使用 AIOps 的借口。AIOps 可以为 SREs 提供一些价值，即使它并不完美。

例如，AIOps 可以起到减少辛劳的作用。在某种程度上，AIOps 工具可以比人类工程师更快地识别复杂的模式或发现相互关联的数据集，AIOps 减少了 sre 手动排除问题或钻研复杂信息所需的时间。

AIOps 还有助于实现更主动的监控和事件管理方法。如果 AIOps 工具可以在 sre 发现新出现的问题之前提醒它们，那么 AIOps 就可以帮助 sre 在问题变成真正的事故之前发现它们。这对 sre 和最终用户都更好。

还有一种观点认为，AIOps 可以帮助 SREs 用更少的工程资源做更多的事情。如果您可以使用人工智能来自动化监控和事件响应的某些方面，您可以用更少的工程师来维持相同级别的可用性和性能。

## 结论:人工智能不会取代 SREs——但它可以有所帮助

以上并不是说 AIOps 可以取代 SREs，或者它神奇地解决了 SREs 面临的每一个问题。任何相信 AIOps 是一颗银弹的人都相信营销炒作已经到了不健康的程度。

尽管如此，AIOps 工具确实为 sre 提供了价值，在某些方面简化了他们的工作，并提高了可靠性。

因此，尽管明智的做法是对 AIOps 的局限性保持健康的观点，但 SREs 不应该排除 AIOps 工具作为改进可靠性工程的一种方法。