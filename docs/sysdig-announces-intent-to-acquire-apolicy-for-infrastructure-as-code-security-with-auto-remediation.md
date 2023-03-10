# Sysdig 宣布有意收购一项基础设施政策，作为具有自动补救功能的代码安全政策

> 原文：<https://devops.com/sysdig-announces-intent-to-acquire-apolicy-for-infrastructure-as-code-security-with-auto-remediation/>

*基于开放策略代理(OPA)的策略代码增强了 Sysdig Secure DevOps 平台中现有云和 Kubernetes 的安全性*

**加利福尼亚州三藩市，2021 年 7 月 20 日— [Sysdig，Inc.](https://sysdig.com/) ，**安全开发运维领导者宣布有意收购一家策略公司，以进一步左移安全性，并扩展 Sysdig 产品，以包括基础设施即代码(IaC)安全性。Sysdig 客户确保开发运维周期从构建到生产的安全。策略补充了这些功能，通过策略即代码、自动纠正偏差以关闭从生产到源头的循环，以及基于风险的优先级排序来更快地解决问题，以合规性和治理实施来增强云和 Kubernetes 的安全性。

**云团队采用安全的 DevOps 来管理安全风险**
疫情引发了在线工作的巨大转变，这给在云端交付应用的团队带来了压力。现代应用构建为容器化的微服务，使用 DevOps 方法来加速交付。随着安全流程的转变，团队正在采用安全开发运维。这包括云配置风险管理、在构建时扫描映像、在运行时检测和响应威胁，以及持续验证是否符合监管标准。

**借助 IaC security 实现云和 Kubernetes 安全性的自动化**基础设施即代码(IaC)和 GitOps 的趋势继续获得云平台团队的广泛认同，成为实现基础设施完全运营控制的一种方式。当团队使用诸如 Terraform、CloudFormation 等 IaC 工具编写基础设施时，很容易忽略安全性。云中的错误配置很常见，许多引人注目的云违规事件就证明了这一点。采用 IaC 原则构建基础设施可以通过提高一致性和减少人为错误来提高可靠性。在定义配置时检查安全性'将安全性进一步左移'，允许团队在部署基础架构之前发现并解决问题。

IaC security 的目标是自动化组织的云和 Kubernetes 安全控制。借助 IaC security，团队可以通过将策略应用为代码来验证配置文件和生产环境并确保它们完全相同，从而始终如一地实施法规遵从性和治理。当出现运行时偏差时，可以直接在源头发现并自动补救，以确保它们不会再次发生。通过将 IaC 安全性集成到安全的 DevOps 工作流中，团队可以将安全性进一步左移，从而提高安全性并减少安全团队的警报疲劳。

**首席执行官 Suresh Vasudevan 的博客:** [Sysdig 和 policy 联手帮助客户保护基础设施代码并自动修复](https://sysdig.com/blog/sysdig-and-apolicy-join-forces-to-help-customer-secure-infrastructure-as-code/)。

**为 Sysdig 的客户收购政策带来的 IaC 安全优势:**

*   **通过从源代码到生产代码的策略实施合规性和治理:**策略能够在多个 IaC、云和 Kubernetes 环境中应用一致的策略和最佳实践。现在，客户可以通过将策略作为代码来统一安全需求，从而在开发人员、开发人员和安全团队之间架起一座桥梁。通过 Kubernetes admission controller 强制执行基于 OPA 的策略来实现合规性自动化，从而将控制权交还给用户。
*   **自动修复漂移并关闭从生产到源的循环:**通过添加策略，客户现在可以检测运行时漂移，并立即将其映射回 IaC 配置(源)文件。这极大地提高了开发人员的工作效率，因为只需简单的拉式请求就可以自动修复 IaC 配置源，并允许在团队间一致地实施策略。
*   **通过基于风险的优先级排序更快地修复问题:**通过识别受 IaC 错误影响的生产实例并根据应用程序上下文对 IaC 修复进行优先级排序来整合警报，允许用户对补救工作进行优先级排序。丰富的应用程序上下文使得识别能够修复错误配置的所有者变得容易。

政策团队，包括创始人 Maor Goldberg，首席执行官，Eran Leib，副总裁产品管理和 Shlomi Wexler，副总裁 R&D 将加入 Sysdig 团队。策略产品将作为 Sysdig Secure DevOps 平台的一部分。

Sysdig Secure DevOps 平台独特地解决了保护容器、Kubernetes 和公共云基础架构的挑战。Sysdig 得到了数百家领先企业的信任，包括 FIS 的 Worldpay、Yahoo Japan、IBM 和 JW Player，可以放心地运行现代云应用程序，同时管理安全风险并满足合规性要求。

“大多数违规都是由配置错误引起的。Sysdig 首席执行官 Suresh Vasudevan 表示:“我们的客户需要一个能够在部署前检测配置错误并识别生产偏差的单一平台。借助策略，只有 Sysdig 能够为基础架构和工作负载提供安全的 DevOps 工作流，并通过修复运行时发现的问题，自动关闭从生产到资源的循环

“我们成立了 Apolicy，目的是通过风险识别、补救和政策执行来确保 Kubernetes 从源头到生产的安全，”Apolicy 首席执行官 Maor Goldberg 说。“我们很高兴与 Sysdig 联手，将市场上最好的云和容器安全功能与我们的基础设施和态势安全相结合。我们将共同为客户带来一个基于开源的端到端云原生安全平台。”

“我们非常高兴能够在 2019 年底率先支持 Maor 和 policy 团队，因为他们开始颠覆云原生应用程序保护领域。StageOne Ventures 管理合伙人 Tal Slobodkin 表示:“今天，我们同样兴奋地看到 policy 与 Sysdig 合并后的下一步发展，并期待合并后的公司未来取得成功。