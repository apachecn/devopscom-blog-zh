# Istio 1.7 提供混合云特性

> 原文：<https://devops.com/istio-1-7-delivers-hybrid-cloud-features/>

**由大可，** **开源领袖，云原生，IBM**

今天的 Istio 1.7 版本对 Istio 的操作体验进行了重大改进。一些新的功能改进，包括控制平面升级、虚拟机集成和集中 Istio 体验，使 Istio 更易于操作，并扩展了其在混合云环境中的功能。这篇博客文章向您介绍了该版本中的新特性，讨论了 IBM 对 Istio 的投资，并解释了 Istio 对于开发开放的混合云环境是如何至关重要。

**功能改进**

**多个控制平面升级**。一个有价值的可用性改进是将 [金丝雀升级](https://istio.io/latest/docs/setup/upgrade/) 功能整合到操作器中。随着这一变化，Istio 的 canary 升级将全面推出，并成为 Istio 的首选升级途径。通过 canary 升级，您可以使用持续集成和 Istio 的遥测功能来验证新的控制平面。一旦一部分工作负载得到验证，就可以转移更多的工作负载，直到所有工作负载都使用新的 Istio 控制平面运行。

为了快速了解这一特性，请观看下面的[视频](https://www.youtube.com/watch?v=POlpwBdXfbE&feature=emb_logo)。
iv>T3**虚拟机集成**。尽管存在一些可用性问题，Istio 从其早期版本开始就已经有了虚拟机集成。有了 Istio 1.7，虚拟机集成接近 [beta 质量](https://github.com/istio/community/blob/master/FEATURE-LIFECYCLE-CHECKLIST.md#beta) 。虚拟机集成的目标是将虚拟机工作负载连接到服务网格，这样虚拟机就像 Istio 中的另一个工作负载一样工作。Istio 1.7 中新的 WorkloadEntry API 将虚拟机视为 Kubernetes pods，因此您可以使用 API 管理您的基础架构。此外，我们实现了许多安全增强，包括令牌引导和证书轮换。我们仍在开发虚拟机集成，但您可以使用[alpha](https://github.com/istio/community/blob/master/FEATURE-LIFECYCLE-CHECKLIST.md#alpha)quality[documentation](https://istio.io/latest/docs/setup/install/virtual-machine/)将虚拟机连接到服务网格。这项工作在一大批感兴趣的开发人员的帮助下进展迅速。

**中央情报局**。由 IBM 开发的 central Istiod 在 Istio 1.6 中得到了部分实现，现在是 Istio 1.7 中的 alpha quality。中央 Istio 的好处是，现在可以将 Istio 控制平面与数据平面分离，以改进操作支持。此外，Central Istiod 满足了多租户的要求，是 Istio 迈向多租户之旅的第一步。

由 IBMers 和丁领导的工作为 Istio 引入了一种新的部署模型，使网格运营商能够在专用集群上安装和管理网格控制平面，与数据平面集群分开。在下面的视频中，丁向您介绍了中央研究院。

**其他改进**

您应该了解的 Istio 1.7 中的其他一些改进包括:

*   测试和资格改进。我们的 Istio 社区对测试 变得越来越严格，这使得每个版本都有更好的项目交付。根据最近的统计，Istio 有 20k+的功能测试和 45k+的单元测试。
*   移动到特使 xDSv3。xDS 是底层 API，它提供了 Istio 管理的数据平面协议。这个主要的版本变化提供了 [改进的性能和可伸缩性](https://mattklein123.dev/2020/03/15/on-the-state-of-envoy-proxy-control-planes/) 。
*   集装箱网络接口。Istio 的 [CNI](https://istio.io/latest/docs/setup/additional-setup/cni/) 支持 Istio 工作负载在 Kubernetes 中无需提升权限即可运行。

**Istio 支持工作负载可移植性，这是混合云的一个关键因素**

交付混合云环境的最大挑战之一是需要使用网络技术将不同的环境连接在一起。如果没有连接，工作负载的可移植性将成为交付真正的混合云体验的一大挑战。

IBM Cloud Satellite 使您能够在最有意义的地方运行工作负载—无论是公共云、您的数据中心还是边缘位置。Istio 服务网格驱动 [IBM Cloud Satellite 分布式云网络连接](https://developer.ibm.com/articles/overview-of-the-new-ibm-cloud-satellite-distributed-cloud/) ，提供工作负载可移植性和互操作性。

**IBM 的 Istio 投资**

**引领创新**。在 Istio 项目中，我们的开发人员专注于构建我们认为对创建和实现开放混合云环境最重要的技术。具体来说，我们领导了启用 central Istiod 的工作，这是 Kubernetes 内部多租户之旅的第一步。IBM 积极参与将虚拟机集成到 Istio 中，在 Istio 1.5、1.6 和 1.7 中开发了许多初始技术。最后，IBM 关注重叠技术支持，这样支持一种技术就支持另一种技术。

**支持社区**。虽然有些 [争议围绕着 Istio 的治理](https://developer.ibm.com/blogs/istio-google-open-usage-commons/) ，但社区成员的奉献精神赋予了 Istio 项目生命，并使其不断向前发展。任何项目的优势都取决于这些贡献者，IBM 坚信支持社区，我们希望所有人都为 Istio 1.7 版本感到自豪。

**参与 Istio**

以下是一些参与 Istio 社区和项目的方法:

*   [在您的 Kubernetes 集群上开始使用 Istio](https://istio.io/latest/docs/setup/getting-started/) 。
*   了解 [对 Istio](https://github.com/istio/community/blob/master/CONTRIBUTING.md) 的贡献。
*   加入 Istio 的 [Slack 开发者交流](https://slack.istio.io/) 。

史蒂文·大可是 IBM 的开源领导者。他是 Istio 项目的维护者，也是环境工作组的工作组领导。