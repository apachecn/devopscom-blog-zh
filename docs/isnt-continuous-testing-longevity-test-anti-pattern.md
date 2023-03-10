# 持续测试不是寿命测试反模式吗？

> 原文：<https://devops.com/isnt-continuous-testing-longevity-test-anti-pattern/>

根据 Jim Coplien 的说法:“反模式看起来是个好主意，但应用起来却适得其反。”在 DevOps 环境中，连续测试对于快速测试特定软件组件(以分钟或小时计量的周期)的狭窄环境是一种有吸引力的解决方案，但如果软件所在的系统有故障模式(例如，内存泄漏的影响)，并且如果发布之间的时间大于该时间，则可能是“坏的”。换句话说，由连续测试规定的快速测试周期模式似乎是与长期“长寿”测试的基本概念相反的反模式。那么，什么是适用于它的明确的积极模式呢？

在我之前的名为[“从 QA 到持续测试”](https://devops.com/blogs/qa-continuous-testing/)的博客中，我指出“在测试设计的最佳实践中最熟练的 QA 测试专家是有价值的，因为他们会生产出质量最好的产品。”QA 测试专家断言，发布一个没有经过与发布生命周期相当的持续时间测试的软件产品是不明智的。只有与发布节奏相比运行时间非常长的测试才被认为是足够的。多长时间才算够长？这是一个超出这篇短文范围的进一步讨论的主题，但是我自己的观察是，最佳实践测试环境在一个构建候选上运行加速级负载和脉冲负载流量模式至少 48 小时或更长时间，然后才确定一个版本至少为有限的部署进行了充分的测试。甚至 48 小时也比典型的“连续测试”周期长得多。那么“什么样的积极的持续寿命测试模式可以代替它呢？”

持续寿命测试模式听起来像是矛盾的，但事实上，寿命测试在持续测试原则的上下文中是兼容的。下面我描述了三种有时使用的连续寿命测试模式。

**模式一:**寿命测试时间窗口预留如周末。在这种模式中，常规的持续集成/测试周期在周末被中断，寿命测试只在周末时间窗口之前最后创建的构建上运行。这具有除了用于常规 CT 测试的资源之外不需要任何特殊测试资源的优点，并且不需要任何复杂的调度来协调测试环境。缺点是寿命测试结果只能每周获得一次，很难诊断哪个构建导致了寿命失败，并且发布候选的问题会将发布延迟一周，直到下一次寿命测试运行验证了修复。

**模式 2:** 寿命并行测试经常被安排，也许每隔几个构建就频繁一次，或者也许每天一次。这种模式的优点是，常规的连续集成/测试周期在任何时候都不会中断(它们 24/7 运行)，寿命测试结果可用于比模式 1 更多的构建，这降低了诊断的复杂性，并且可以减少发布延迟，但是缺点是，必须为与常规 CT 测试并行的每个寿命测试保留单独的测试资源。对于具有许多测试目标和大量构建的复杂测试系统来说，这可能是非常昂贵的，因此在测试资源成本和延迟成本(如果做得不够频繁)之间有一个折衷。

**模式 3:** 智能寿命测试仅在某些条件触发寿命测试时进行，根据智能规则启动寿命测试，智能规则将软件更改与寿命性能问题相关联。这种模式具有与模式 2 相同的优点，而且如果触发器的规则不太频繁地触发，测试资源的成本通常比模式 2 低得多。缺点是整个方案依赖于规则引擎和规则的创建，这些规则理解长时间测试的变更风险。如果规则太宽松，那么这种模式可能会让太多的寿命失败逃脱，但是如果规则太严格，那么这种模式并不比模式 2 更好，而且实现起来更复杂。

那么，哪种持续寿命测试模式是最好的呢？最佳答案是最符合组织的发布节奏、测试成本和风险目标的答案。

因此，实际上，持续测试是一种寿命测试反模式，但幸运的是，根据最佳实践实现的 DevOps 基础设施有多种互补的持续寿命测试模式可供选择。

在思必驰，我们认为测试在 DevOps 有着光明的未来。你可以在
[Spirent.com/solutions/devops](http://www.spirent.com/solutions/devops)了解更多我们的观点

你对这些模式有什么看法，或者你有其他应该提到的模式吗？