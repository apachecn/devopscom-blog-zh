# 在生产中运行 Kubernetes:确保您的路由策略有效

> 原文：<https://devops.com/running-kubernetes-in-production-make-sure-your-routing-strategy-works/>

管理 Kubernetes 在生产中的部署带来了一些相当复杂的挑战。集装箱化环境中网络通信的动态特性产生了独特的操作问题——即使是经验丰富的 DevOps 团队也会感到困惑。为了缓解这些问题，基于软件的路由组件在许多领域提供了关键优势。

这里有一些在任何生产级 Kubernetes 环境中都要考虑的特别重要的路由策略。

## **利用跟踪和监控**

无论你在开发过程中如何彻底地测试应用程序，新一轮的问题 将会在生产中 出现。为了帮助理解(并应对)这些新的障碍，跟踪和监控工具为开发人员提供了对他们的运行时 Kubernetes 环境的关键可见性。选择与已建立的监控和跟踪后端紧密集成的路由技术也将有助于使事情变得更容易。

所有服务间流量都通过软件路由组件。这使得有目的地收集微服务跟踪和监控数据的战略应用设计成为可能。例如，跟踪工具可以识别微服务调用的源和调用流(假设应用程序被设计为支持可跟踪性)。因此，团队可以决定如何充分利用任何可用的微服务，甚至是由不同团队开发的微服务。通过设计应用程序来提供指标，DevOps 团队还可以使用软件路由和监控工具来了解生产问题。例如，跟踪微服务的资源使用指标可以揭示其子组件是否准备好处理更大规模的负载。这些数据可以同时指出性能限制，并帮助排除新功能实现的故障。

## **安全通信和许可**

在 Kubernetes 的任何生产部署中，安全性都必须是首要考虑的焦点。需要严格控制管理内部网络通信的权限，以抵御攻击。必须对内部和外部流量中传输的敏感数据进行加密和保护。许多企业要求数据加密，这不仅是一种最佳实践，也是一种法规遵从性问题。不幸的是，这些安全措施在许多 Kubernetes 环境中并不存在。

路由技术使得使用网络分段来实施安全策略成为可能。 例如，只有具有合理业务需求的客户服务才能访问处理敏感数据的微服务。路由工具也可以提供加密。服务网格可以通过安全 TLS 加密保护内部东西向流量。边缘路由器可以利用提供的证书来加密所有外部南北流量。为了完全自动化可信证书的生命周期管理，DevOps 团队还可以将路由技术与服务配对，如 [让我们加密](https://letsencrypt.org/) 。这种自动化使连续加密和保护敏感数据的传输成为可能，无需人工干预。

## **吸收意外负载峰值**

突然流行、DDoS 攻击和其他意外事件可能会触发意外的负载高峰。作为一种技术，速率限制使运营商能够控制对前端服务的请求速率。这使得应用程序能够吸收意外的负载峰值并避免故障。这样，利用路由工具来实现速率限制技术有效地限制了由于负载事件导致的停机时间。

## **解决沟通问题**

由于容器、主机、网络分区的错误或短期微服务中断，微服务可能变得不可访问。因此，实施缓解策略以防止这些通信故障影响用户是绝对重要的。

例如，负载平衡器可以通过将请求定向到可行的实例(并在实例可用时恢复正常流量)来响应实例故障。在微服务中断期间，停止重复的重试请求以节省资源和避免级联故障至关重要。团队应该使用客户服务来使用电路中断来停止请求、发送错误和回退到替代过程。

虽然可以在每个客户端中使用网络层逻辑来实现这些缓解技术，但这种方法极具挑战性且容易出错。团队最好利用路由技术来控制他们的应用程序的缓解响应。

## **实现高可用性**

与传统的硬件故障转移解决方案相比，当今的软件路由技术为 Kubernetes 环境引入高可用性提供了更有效、更经济的方法。

软件路由技术使 DevOps 团队能够通过独立的、可水平扩展的数据平面和容错控制平面来利用架构。数据平面使得添加所有必要的实例以实现必要的容量和弹性成为可能。同时，控制平面有效地容忍故障，以保持正常运行时间并保障应用用户群的无缝体验。因此，智能路由策略确保了生产 Kubernetes 部署的高可用性和难以置信的弹性。

## **跨多云和其他异构环境部署**

DevOps 团队可以在多个云环境、本地环境甚至其他容器编排解决方案中利用 Kubernetes。路由策略应该满足有效支持跨这些不同环境和解决方案的部署所需的可移植性。通过这样做，开发人员可以在所有部署中部署通用的路由层模型。这减少了关键挑战，因为它使我们能够专注于一个单一且熟悉的解决方案。

选择一种合适的有利软件路由技术可以改变将 Kubernetes 部署到生产中的体验。路由工具提供的功能可以简化甚至完全消除许多常见的挑战(以及一些不常见的挑战)。通过这种方式，DevOps 团队可以更容易、更成功地利用 Kubernetes 提供的一切，同时实现更健壮、更可靠的应用程序。

*要了解更多关于集装箱化基础设施和云原生技术的信息，请考虑来阿姆斯特丹的 [KubeCon + CloudNativeCon EU](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/) 。CNCF 已决定推迟该活动(原定于 2020 年 3 月 30 日至 4 月 2 日)，改为在 2020 年 7 月或 8 月举行。*

曼努埃尔·扎普夫