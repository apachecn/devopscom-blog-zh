# CNCF 将 LitmusChaos 的平台提升到孵化水平

> 原文：<https://devops.com/cncf-takes-litmuschaos-platform-to-the-incubation-level/>

云计算本地计算基金会(CNCF)的技术监督委员会(TOC)今天宣布将开源 LitmusChaos 应用测试平台提升到孵化级别。

LitmusChaos 是 2020 年由 ChaosNative 捐赠给 CNCF 的一个[混沌工程](https://devops.com/?s=chaos+engineering)平台。从那以后，它已经被超过 25 个组织在生产环境中采用，包括 Intuit、Lenskart、Orange、Red Hat 和 VMware。

ChaosNative 首席执行官 Uma Mukkara 表示，LitmusChaos 的开发旨在为 DevOps 团队提供一个使用容器构建的混沌工程平台，与现有的整体替代方案相比，该平台更容易扩展和缩小。然而，平台本身可以用来测试单片和基于微服务的应用。

该平台包括基于软件开发工具包(SDK)的混沌算子；一个用于托管和共享实验的 ChaosHubLitmus 工作流声明性地链接实验(顺序或并行)以构建混沌场景；一个被称为 ChaosCenter 的集中控制平面，用于设计、调度和监控 Litmus 工作流；Litmus Probes 用于创建混沌场景，自动执行稳态验证和补救措施，并提供混沌可观测性工具来导出普罗米修斯指标。

![](img/18ab81155858af8b518fd3be4170e558.png)

LitmusChaos 项目现在总共有 400 多个贡献者，提出了 4000 多个拉取请求。Mukkara 说，自今年年初以来，Litmus operator 的安装量已经增长到每天 2000 多台。Mukkara 补充说，展望未来，2022 年的目标是大幅增加 LitmusChaos 集成的数量，用于更广泛的 DevOps 平台。还计划为 Kubernetes 和非 Kubernetes 目标进行更多组实验，通过 CNCF 正在推进的开源 OpenTelemetry agent 软件提高可观测性并与其他平台集成。

总的来说，在 DevOps 工作流中采用混沌工程还为时尚早。然而，Mukkara 说，随着越来越多的组织采用可观察性来更好地理解 IT 过程，使用混沌工程来测试 IT 弹性的组织的数量也应该增加。Mukkara 指出，事实上，随着 IT 环境变得越来越复杂——这主要归功于基于微服务的应用程序的兴起——有一天可能需要混沌工程方法来进行测试。

与此同时，仍然有许多 IT 专业人员对测试的混沌工程方法感到不安，这些方法故意破坏底层服务来测试应用程序的弹性。然而，核心思想是任何应用程序都不应该有可能导致其不可用的单点故障。理论上，基于微服务的应用不会失败，因为当一项服务变得不可用时，呼叫会自动被重新路由到另一项服务。该应用程序的性能会下降，但不会脱机。挑战在于，使用微服务构建实现这种弹性水平的应用程序需要大量的 DevOps 专业知识。

不管应用程序是如何构建的，有一点是清楚的，那就是组织对应用程序的依赖程度。因此，对应用程序故障或性能下降的容忍度从未如此之低。