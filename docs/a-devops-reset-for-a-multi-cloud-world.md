# 面向多云世界的 DevOps 重置

> 原文：<https://devops.com/a-devops-reset-for-a-multi-cloud-world/>

在 DevOps 的世界里，只有两件事真正重要:

*   尽快发布应用程序和更新
*   尽可能经济高效地访问能够运行这些应用的资源(处理、存储、网络)。

用来实现这两个目标的措施应该无缝地协同工作——否则，你的效率会很低。但是软件开发和 IT 运营一直处于不同的旅程，现在需要多层工具、专业知识和大量宝贵的时间来分发和管理需要运行的应用程序。组织容忍所有这些复杂性(以及随之而来的延迟和成本),因为他们看不到其他选择。但是如果有更简单的方法呢？我将研究驱动软件开发和 IT 运营的两个基本转变，并看看为什么当前的过程如此繁琐。

### 转变一:从单片应用到微服务

一开始，应用程序是单一的，所有的功能和代码都打包在一起。当应用程序一年更新一次或两次时，这种方法是可管理的，但当每天都要更新多次时，这种方法就不可管理了。*最后*有人意识到，如果将应用程序划分为称为微服务的更小单元，那么构建、改进和维护起来会容易得多。微服务是独立的、松散耦合的、可单独部署的服务，每个服务处理一个特定的功能。

为了支持微服务，出现了一个技术堆栈，类似于梯子上的台阶:

*   为了使它们具有可移植性，微服务被封装在容器中——这是一种轻量级的标准方法，应用程序可以在环境之间移动并独立运行。运行微服务所需的一切，如设置、系统工具、库和依赖项，都打包在容器中。
*   一个应用程序可能有数百个相关联的容器。你是如何管理它们的？随之而来的是 Kubernetes(又名 K8s)，这是一款用于在虚拟机集群中部署和编排容器的开源软件。(注意“集群”这个词——其意义将在稍后讨论。)
*   由于微服务不断更新，如何确保运行的是正确的版本？随着 GitOps 的出现，它为所有这些微服务的所有更新提供了版本控制。Git 存储库为期望的应用程序状态提供了单一的事实来源，以及每一次代码更改的记录。

最后，我们需要建立持续集成/持续交付(CI/CD ),以推出应用程序改进和新特性。随之而来的是 ArgoCD，这是一个用于 Kubernetes 的 GitOps 连续交付工具，它可以连续监控正在运行的应用程序，将当前的实时状态与 Git 存储库中指定的目标状态进行比较，并解决差异。

### 转移二:  从内部部署转移到多云

不久前，IT 部门还在热烈讨论这个被称为公共云的奇怪新概念，以及它是否可能在他们的运营中发挥作用。但是一旦他们发现增加资源是多么容易，闸门就打开了。

第一个试验性步骤通常涉及混合云，将现场私有云与溢出到公共云中相结合，以应对工作负载高峰。这些最初的尝试迅速发展到数十或数百个云，分布在不同的位置，由不同的提供商提供。这是全球企业正在发生的思维转变——他们曾经拥有少量的云，现在他们的云运营规模庞大，不断增长，无止境。企业还发现，云不仅仅是一种更简单、更具成本效益的应用运行方式，它还开启了新的机遇。

现在有了核心云、面向超本地应用的边缘云、区域云、面向高可用性和弹性的云等等。边缘计算是另一种选择，在面向客户的前端云中运行需要低延迟，而后端处理在主云中进行。但这仅仅是开始。

### 持续交付现在太复杂了

今天，一个应用程序可能有几十个微服务分布在不同的云中，需要协同工作——可能一些在云 1 中，一些在云 2 中，其他在云 40 中，等等。规模很快变大。例如，如果将 100 个微服务交付给 100 个云，则有 10，000 个突变需要配置和管理。

这是新常态，DevOps 需要适应。流程应该是透明的，但是跨多个云和云实例连接微服务需要集群间的通信，而 Kubernetes(及其之上的 GitOps/ArgoCD)本身并不支持这种通信。

要完成所有这些工作，需要专业的技能组合，因此组织雇佣在连续交付、多云、网络、安全和自动化方面具有专业知识的团队。第一步包括将 K8s 容器分发到微服务将要运行的云中。一些企业创建自己的分发系统，另一些企业选择下载、安装和管理第三方软件，如开源 ArgoCD。

第二步更复杂:跨不同云和 K8s 集群安全地连接那些微服务。这包括集成复杂的服务网格、负载平衡器、API 网关和网络/防火墙自动化工具，所有这些都集成到一个集中的控制台中进行配置和监控。

结果是不可避免的:大量的额外成本、低效率、潜在的安全风险和上市时间的延迟，从而给业务带来风险。开发团队每天更新微服务，但依赖 CloudOps、NetOps、SecOps 和其他类型的 Ops 来将它们交付到需要运行的不同云和集群。

尽管这些不同的利益相关者尽了最大努力，但每次改变都可能需要几天或几周的时间来更新云网络和安全性。

### 通过覆盖网络简化多云操作

当数百个微服务分布在越来越多的云中并不断更新时，您需要一种替代方案—一种能够简化当前操作而不牺牲安全性或应用程序性能的方案。让我们抛开传统的方法，想想应该怎么做。

首先，解决方案应该易于使用，因此 DevOps 人员不必精通底层技术，也不必依赖于精通的 NetOps、SecOps 和/或 CloudOps 人员。相反，只需提供一些关于 Git 存储库和您希望微服务运行的云的基本信息，其余的由覆盖网络处理。

它应该是全面的—集成 ArgoCD、服务网格、K8s 入口网关、零信任安全性、弹性/故障转移、负载平衡和多云网络—所有这些通常需要组装和配置单个工具的元素。

它应该使[多云](https://devops.com/?s=multi-cloud) Kubernetes 应用程序操作易于管理，通过单一仪表板，您可以在所有云和集群中安全地部署、连接和监控微服务。

最后，解决方案应该以服务的形式提供，而不是必须安装 ArgoCD 服务器并试图自己管理它(或雇佣团队来支持它)。如果你有问题或者需要帮助，有能力的人会帮你的忙。

## 颠覆性——以好的方式

准备好迎接与底层网络和安全细节相分离的自助式多云 Kubernetes。这是一种即将颠覆微服务部署和管理方式的方法，因此 DevOps 可以回到真正重要的事情上: D 在应用需要运行的资源上尽可能快地交付应用。在大幅降低成本且不影响安全性的情况下，以以前的一小部分时间提供新功能的能力将意味着竞争优势和更强的底线。