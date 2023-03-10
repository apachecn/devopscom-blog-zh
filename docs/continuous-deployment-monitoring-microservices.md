# 微服务的持续部署和监控

> 原文：<https://devops.com/continuous-deployment-monitoring-microservices/>

持续部署和持续监控在 DevOps 中成长起来，微服务成长为交付平台。虽然目前所有这些都是相对稳定的概念，但是仍然有相当多的从业者在努力融合这些概念，以创建一个允许深入理解和轻松部署的整体环境。

所以我想我们可以看看外面有什么，进展如何，甚至为你提到一两个资源。

## 持续部署

虽然持续交付(CD)和持续集成(CI)已经很好地掌握了，但是持续部署已经有点落后了。这是有原因的——有好的也有坏的——为什么这是真的，但这是真的。持续部署是实际部署 CI/CD 周期结果的行为。持续部署的全部目的是通过在新特性通过 CI/CD 测试时，或者在测试后不久，或者对于某些行业来说，在需要时发布它们，来加速新特性向市场的发布。连续交付与 CI/CD 略有不同，因为组织的其余部分—销售、支持、营销、会计等。—必须为发布做好准备，所以在最慢的情况下，关键是它不是在持续部署模式下发布新功能的阻碍。

## 微服务

简单地说，微服务是将应用程序分解成可以独立运行的更小的部分。对于“更小的部分”的含义有许多不同的想法，一些商店将其应用程序分解到类似于无服务器功能的功能级别，因此一个名为 calculateSalesTax 的 API 会在给定位置和美元信息的情况下做到这一点，而其他人则喜欢更广泛的定义，包括 API 的整个分组。在这个场景中，一家公司将所有数据库工作拆分到一个可扩展的微服务中。无论哪种方式，您都将拥有比以往更多的实例(通常是容器，但有时是虚拟机甚至是物理服务器)来构建应用程序。

## 为什么是集装箱

如上所述，微服务架构通常构建在容器上。容器定义的可移植性是公司倾向于这个方向的主要原因之一。能够说“这个容器可以在我们的硬件、我们的私有云、公共云、公共云 VPC 或虚拟机上运行”，这是一种确保您可以将系统定位到最适合组织需求的环境的方法。

容器也比虚拟机轻得多，这意味着启动时间更快，更容易扩展微服务架构以满足不断变化的用户需求。

## 集装箱管理

说到容器，容器管理系统用于确保容器是活动的和响应的。在高级情况下，可以让它们检查容器是否也在做它应该做的事情。虽然我是阿帕奇 Mesos T1 的粉丝，但这个世界似乎已经转向了 T2 Kubernetes T3，所以我们将把重点放在它上面，不再进一步提及其他人。

除了确保正确数量的给定容器正在运行，并在一个容器消失时采取措施增加新的容器之外，Kubernetes 还做了一些事情，例如管理容器的秘密，在一个组中的实例之间执行负载平衡(这些组在容器管理中通常称为服务)，根据指示按比例增加/减少实例，并为服务提供滚动更新，以便服务在更新时不会关闭。

这使得容器管理工具成为任何连续交付和连续监控工作的重要部分。

## 合起来

这为我们提供了包括用于 CI 和 CD 的 [Jenkins](https://jenkins.io/) 在内的工具，并且通常用于发布管理，尽管其他工具也专门用于发布部分。将 Jenkins 与基础设施即代码解决方案结合起来，例如 [Teraform](https://www.terraform.io/) 或我们过去讨论过的任何其他解决方案。添加像 [Prometheus](https://prometheus.io/) 这样用于收集监控数据的工具，以及像 [Grafana](https://grafana.com/) 这样用于可视化数据的工具，您就踏上了持续交付和持续监控的道路。

当然，事情没那么简单，我在这里概述一下。在研究这个博客的时候， [Infostretch](https://www.infostretch.com/) 的人和我分享了一些信息，他们也认为这是一个 5 万英尺的视角。但这是我们的起点。为了更全面地了解情况，下面是 Infostretch 与我分享的一个简单的持续部署图:

![](img/d679b2165f5667f72591106c59f55c28.png)

既然我们在讨论 Infostretch 与我分享的信息，我们也来看一下该公司监控的内容。您将会看到，它不是“阳光下的一切”，而是为他们提供可操作情报的重点。应用程序内部的一些特定于应用程序的监控点，这就变成了应用程序性能的金矿。

| **分类** | **指标** |
| 聚类指标 | 总体集群内存利用率 |
| 总体集群 CPU 利用率 |
| 总体集群文件系统利用率 |
| 单个服务 CPU 利用率的多系列图 |
| 单个服务内存利用率的多系列图 |
| 单个服务 FS 利用率的多系列图 |
| Application Metrics | 服务请求率 |
| 服务错误率 |
| 服务延迟 |

## 还有很多

在一个单独的博客中，实在没有足够的空间来涵盖持续交付和持续监控中所有需要和可能的内容。我会继续尝试连续写博客来帮助你，DevOps.com 的其他作者也有好东西可以分享。

唐·麦克维蒂