# LitmusChaos 增强了开发人员对云原生可靠性的体验

> 原文：<https://devops.com/litmuschaos-enhances-developer-experience-for-cloud-native-reliability/>

在 [云原生计算](https://en.wikipedia.org/wiki/Cloud_native_computing) 中，应用被期望具有弹性、松耦合、可伸缩、可管理和可观察。由于集装箱化，微服务激增，而且运输速度很快。微服务环境更加动态。在这样的环境中，使应用程序具有弹性意味着以容错方式部署应用程序，但也意味着构建应用程序来承受依赖(即上游/下游)服务上发生的故障，并继续采取适当的措施来防止这种故障的发生。同样，质量保证团队应该涵盖 CI 和 CD 流程中要涵盖的所有故障场景。最终，Ops 团队必须通过实践混沌工程来继续测试服务在生产中的弹性。持续验证可以而且应该在产品生命周期的所有阶段进行。

**开发人员的混沌工程**

云原生开发者在开发 [微服务](https://blog.codinghorror.com/curlys-law-do-one-thing/) 时遵循卷毛定律。这实现了模块化和更快的应用交付，但也需要在代码中创建一组定义良好的条件来处理各种微服务故障、API 响应和 Kubernetes 等底层平台。虽然 Kubernetes 在实现微服务架构方面发挥了重要作用，但它也带来了开发人员应该了解的某些假设。例如，pod 被逐出或在节点间移动的频率是 ESX 集群中虚拟机移动频率的数倍。在一个可扩展的环境中，pod 驱逐可能在任何时候发生(取决于负载条件和其他环境因素)，但是服务应该继续正常工作。

在开发过程中可以执行大量的混沌测试，以针对 Kubernetes 故障和常见的云原生基础架构应用程序故障建立弹性。LitmusChaos 是一个云原生应用程序，它提供了实践端到端混沌工程的所有能力。其混沌实验本质上是声明性的，云原生开发者可以以云原生方式添加或执行混沌实验。Litmus 的核心在 Chaos CRDs 的基础上运行，这使得云原生开发者对 Chaos 的实践变得非常自然。

**CI 中的混沌工程**

云原生 CI 渠道对 QA 团队提出了额外的要求。他们需要根据云原生平台功能(如 Kubernetes)的各种特性来测试应用程序。Kubernetes 环境可能会出现各种故障，如 pod、节点和服务级别故障。在 chaos 集成 CI 管道中，chaos 实验旨在涵盖 Kubernetes 和其他云原生堆栈组件的所有故障场景，以及特定的应用程序故障

除了能够针对各种不同的场景轻松执行混沌实验之外，质量保证团队还可以从一个版本到另一个版本测量应用程序的弹性指标的性能。Litmus 就是这样一个工具，它可以很容易地将弹性度量与不同版本的被测系统的混沌运行进行比较。

**LitmusChaos 工作流程或场景**

混沌实验作为 [混沌工作流](https://docs.litmuschaos.io/docs/concepts/chaos-workflow/) 的构建单元，它以任何想要的顺序和序列将多个混沌实验串在一起，将失败注入到多个资源中。这允许简单地使用[chaos center](https://docs.litmuschaos.io/docs/getting-started/resources#chaoscenter)web UI 来创建复杂的、真实的故障场景，这些场景涉及作为单个工作流一部分的整个应用程序的几个不同方面。可以把混沌实验想象成封装了特定目标资源的失败条件的乐高积木。这些乐高积木可以按照任何想要的顺序灵活地排列，以形成混沌工作流——一个为验证您的特定 SLO 需求而定制的失败场景的聚合。

**将混沌测试引入开发者 CI 管道**

[LitmusChaos](https://github.com/litmuschaos/litmus) 提供了通过混沌中心创建工作流并以不同方式使用它们的能力。为了在 CI 管道中使用工作流，最简单的方法是将创建的混沌测试存储在 git 中。如果您在 Litmus 中配置 gitOps，工作流会自动存储在 Git 中，您可以直接在 Git 上或通过 chaos center 编辑测试。一旦测试(YAML 清单)在 Git 中，您就可以通过创建一个 kubernetes shell 环境并执行在您的 CI 管道中调用它

***" kubectl apply-f http://<github.com>/your-repo/your-file . yml "***

上面的命令可以神奇地获得您的混沌实验，设置执行环境，执行混沌测试，并将结果/指标上传到混沌中心。

基本上，开发者可以通过插入“kubectl apply-f<chaos test . YAML>来构造他们的 CI.yaml 文件，并在混沌中心观察结果。Chaos center 提供了对历史工作流执行的分析，这有助于了解您正在开发的应用程序的弹性是在增加还是保持不变(假设您已经提供了良好的 Chaos 覆盖率)。

这里有一个如何在 CI 平台上使用 Litmus chaos 测试的例子，在这个例子中是线束 CI:[https://dev . to/ksatchit/chaos-engineering-with-Harness-cicd-pipelines-1dn 0](https://dev.to/ksatchit/chaos-engineering-with-harness-cicd-pipelines-1dn0)

在其他 CI 平台上，如[【git lab】](https://github.com/litmuschaos/gitlab-remote-templates)【circle CI】等，也可以以同样的方式使用 Litmus 混沌测试。