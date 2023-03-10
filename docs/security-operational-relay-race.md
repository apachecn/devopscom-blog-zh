# 运行接力赛中的安全性

> 原文：<https://devops.com/security-operational-relay-race/>

如果你曾经看过人们跑接力赛，你会注意到大部分的风险发生在接力棒从一个人传给下一个人的时候。在 IT 流程中，移交过程中的风险也急剧增加。无论您是从一个流程阶段转移到另一个阶段，从一个“所有者”转移到另一个阶段，还是从一个环境转移到另一个环境，在阶段转换期间风险都是最大的。

无论您是否使用 DevOps，安全性在这些移交过程中都扮演着重要的角色。这里有一些原则，可以帮助保护移交和减少风险的运作接力赛。

## 减少访问

他们说厨师太多会破坏汤，这也适用于 IT 流程。限制可以直接在生产中进行更改的人数，您就有机会通过减少部署的随机行为，以及生产中出现的更改冲突和神秘更改来提高安全性和保护可用性。这是创造可预测性和减少变更冲突的关键。

## 创建可防御的“瓶颈”

减少将事物部署到生产环境中的方式将有助于保护生产环境的完整性。这并不一定意味着*阻止*变化，更多的是控制变化如何进入环境。专注于创建可信任的存储库、部署源、自动化工具和服务帐户，以减少如何进行部署的选项。当您定义了清晰的泳道并且知道预期的部署路径时，就更容易检测到意外的活动和动作。

使用瓶颈来加强验收标准，以确保您准备好对交付给您的代码、系统和应用程序负责。

这种方法允许自治团队在如何完成工作方面有很大的自由度，同时通过生命周期的发布管理和到 Ops 阶段的过渡来加强一致性。

## 像空中交通管制员一样思考

当处理需要在生产中聚集和互操作的多个工作流时，我认为空中交通管制员的心智模型工作得很好。机场允许一群独立的运营商以有序的方式聚集在一个共享的环境中，以最小的冲突和可预测的吞吐量，而空中交通管制员在实现这一目标方面发挥着关键作用。在 IT 环境中，这意味着依靠那些比任何单个团队都有更广阔视角的人，这样他们就可以放眼全局并整体协调活动。

这种“缩小”视角对于识别风险活动和差距、理解可能破坏您的安全模型的依赖关系以及介入以帮助缓解危险情况至关重要。这种方法也使得与第三方提供商合作更加容易，因为您可以专注于他们的*结果*(输出和移交)，而不是陷入他们日常活动的细枝末节。

## 持续监控以识别“信任差距”和异常值

DevOps 对连续监控和仪器仪表并不陌生。从安全角度来看，持续监控就是建立一套控制措施，让您能够快速识别增加风险的条件，上述要素有助于您更有效地完成这项工作。例如:

*   当有人绕过您的流程并直接在生产环境中进行更改时，访问限制和瓶颈使您能够快速检测到。
*   这些元素还允许你密切关注第三方承包商和提供商，以确保他们遵守你的规则，并且你知道他们一直在做什么。
*   可防御的瓶颈使您能够在有人篡改您的源代码库、自动化脚本或安全监控组件(比如禁用日志记录)时发出警报。
*   研究您的指标，找出您的遥测数据中与移交相关的黑点，并询问攻击者(内部或外部)如何利用您的移交中的任何弱点。

这些只是如何应用这些概念的几个例子。当您认识到移交是有风险的时，您可以很快看到安全性如何在减轻这些风险和帮助维护您的生产环境的可靠性、安全性和可信度方面发挥作用。