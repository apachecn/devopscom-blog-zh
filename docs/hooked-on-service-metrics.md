# 迷上了服务指标

> 原文：<https://devops.com/hooked-on-service-metrics/>

我们生活在一个日益“即服务”的世界。从软件即服务(SaaS)和平台即服务(PaaS)到功能即服务(FaaS)和 SaaS 交付的应用程序，服务交付已经成为业务目标和实践的重中之重。

在当今的 DevOps 环境中，微服务(设计可扩展、独立交付的服务的云原生方法)允许团队优先考虑每个单独的服务，而不是同时考虑许多服务，从而实现敏捷性和连续交付。然而，即使有这些好处，微服务也带来了相当大的挑战，特别是在可观察性、监控和安全性方面。因此，服务指标现在比以往任何时候都更加重要，因为减轻挑战和抓住微服务带来的机遇有助于开发运维团队创造高质量的终端用户体验。

随着服务交付如此融入整体业务和客户体验，确保服务性能始终保持最佳状态至关重要。技术专家如何确保满足服务级别协议、服务顺利运行以及满足并超越最终用户的期望？答案很简单:沉迷于服务指标。

## **上瘾**

在这篇文章中，我们将探讨与微服务相关的服务指标。由于微服务可能带来的可观察性、监控和安全挑战，管理和控制微服务及其流量需要一个额外的工具层:服务网格。实施服务网状架构有助于促进流量管理、服务身份和安全性、策略实施等，最终为容器和微服务管理带来可靠性、安全性和可管理性。请求量、请求持续时间、延迟和请求大小等重要指标可以跨服务网格自动收集，这有助于促进成功的微服务部署。

然而，尽管服务网格工具有助于降低风险，但是诸如 RPC 超时和异常传播之类的故障还是会发生。微服务领域的故障通常发生在服务之间的交互过程中，因此清晰地了解这些事务有助于 DevOps 团队更好地管理架构并避免所述故障。服务网格提供了可观察性，这使 DevOps 团队能够轻松地看到服务相互交互时发生的情况，从而更容易构建更具弹性、更安全和更高效的微服务系统。此外，服务网格提供了一个开发人员驱动的、服务优先的网络，这种网络的运行无需应用程序开发人员将网络问题构建到他们的应用程序代码中。服务网格创建了一个网络，使运营商能够通过策略定义网络行为、节点身份和流量。

## **成功秘诀:你需要知道的事情**

那么，DevOps 团队如何实现服务度量的服务网格架构呢？遵循一些最佳实践有助于确保成功:

*   **知道何时实施**:如果 DevOps 团队不打算运行过多的微服务，服务网格可能就没有必要了；现有工具和安全工具可能只能管理不到 10 个微服务。但是一旦一个团队开始运行超过 10 个，服务网络就变得至关重要。
*   **了解您的用例**:在确认服务网格架构的必要性之后，您必须了解它将如何与您正在运行的其他类型的基础设施进行交互，因为这将有助于确定利用什么服务网格。例如，有些与 Kubernetes 或 Docker Swarm 配合得很好，但是如果您不在容器内运行服务，您将只能从服务网格的安全性或可观察性方面受益。根据您的用例，您可能希望实现一个功能强大的服务网格，比如 Istio，或者一个更简单的工具，比如 Linkerd 2.0。
*   **关注网络:**使用服务网状架构，您有几个通过新网络进行通信的微服务。因此，了解网络的重要性非常重要:您希望从连接您的微服务的网络中获得什么？您希望您的网络尽可能智能和有弹性；避开故障路由流量，以提高群集的总体可靠性；并避免不必要的开销，例如高延迟路由或具有冷缓存的服务器。您希望您的网络能够确保服务之间的流量不会受到微不足道的攻击。并且您希望您的网络通过突出服务通信失败的意外依赖性和根本原因来提供洞察力。

## **结论**

沉迷于服务指标是确保成功交付服务和满足最终用户体验的关键。鉴于服务为企业带来的价值，确保服务始终以最佳状态运行至关重要。对于微服务，实施服务网状架构并遵循相应的最佳实践有助于确保成功的服务交付。

— [亚当·赫特](https://devops.com/author/adam-hert/)