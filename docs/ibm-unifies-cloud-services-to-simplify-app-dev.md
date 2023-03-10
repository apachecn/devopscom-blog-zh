# IBM 统一云服务以简化应用程序开发

> 原文：<https://devops.com/ibm-unifies-cloud-services-to-simplify-app-dev/>

IBM 今天宣布，一项统一构建和部署应用程序的云平台的 [IBM 云代码引擎](https://developer.ibm.com/blogs/cloud-made-easy/)服务现已正式推出。

IBM Cloud Code Engine 构建在无服务器计算平台之上，是一项托管服务，它将运行在传统虚拟机上的平台即服务(PaaS)环境、容器即服务(CaaS)环境和批处理工作负载统一到一个平台上。

该托管服务的核心是 Kubernetes 的一个实例，该实例运行 Knative 中间件来调用开源无服务器计算框架、Istio 服务网格和 Tekton 管道来构建 DevOps 工作流。

IBM 云平台首席技术官兼副总裁杰森·麦基(Jason McGee)表示，目标是消除开发人员今天被迫在云中导航的人工构造，每个构造都可以追溯到不同的软件开发时代。McGee 说，IBM 云代码引擎统一了开发人员的体验，使得在对特定应用程序工作负载最有意义的云服务类型上构建和部署应用程序更加简单。开发人员不再需要为特定类型的基础设施配置代码；他们可以简单地描述他们希望源代码或容器映像如何运行，IBM Cloud Code Engine 会相应地自动化部署。

McGee 补充说，IBM Cloud Code Engine 所基于的无服务器计算框架也使 IBM 有可能只在代码实际运行时向组织收费，而不是要求他们承诺特定数量的基础设施来运行一组虚拟机。费用基于消耗的内存和 vCPU 以及传入的 HTTP 调用。McGee 说，随着时间的推移，这种方法将大大降低云计算的总成本。

McGee 补充说，它还应该加快应用程序向云迁移的速度。如今，大约 20%的应用程序工作负载运行在云中。McGee 指出，将接下来 40%的工作负载转移到云中需要提供简化的应用程序开发人员体验。

组织目前面临的挑战是，他们正在云中部署基于单片和微服务的混合应用程序，这些应用程序在不同程度上依赖于面向批处理的实时平台。IBM Cloud Code Engine 致力于在广泛的云服务上提供一个抽象层，他们可以根据需要通过事件驱动的平台灵活地调用这些服务。

IBM Cloud Code Engine 的 DevOps 含义具有潜在的深远意义。如今，开发运维团队代表开发人员花费了大量时间来调配云基础架构。IBM 现在正在为一个能在几秒钟内自动完成这一过程的平台做准备。实际上，对云基础设施的控制将进一步转移到应用程序开发人员手中。理论上，DevOps 团队在部署应用程序后会花更多的时间来优化云环境。

尚不清楚 IBM Cloud Code Engine 等平台可能会在多大程度上迫使云服务提供商根据正在构建的应用程序类型整合他们今天向开发人员提供的不同云服务。然而，已经很明显的是，墙上预示着巩固的文字现在已经被不可磨灭地铭刻。