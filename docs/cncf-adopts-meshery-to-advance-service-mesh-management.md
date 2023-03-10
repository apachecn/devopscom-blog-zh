# cncf 采用 mashery 推进业务网格管理

> 原文：<https://devops.com/cncf-adopts-meshery-to-advance-service-mesh-management/>

云本地计算基金会(CNCF)本周在[ServiceMeshCon/kube con+CloudNativeCon](https://events.linuxfoundation.org/servicemeshcon-north-america/)会议期间宣布，由第 5 层[创建的服务网格管理平面 Meshery 已经成为沙盒级项目](https://www.prweb.com/releases/2021/10/prweb18259869.htm)。

此外， [Layer5 还向 CNCF 捐赠了服务网格性能](https://layer5.io/company/news/cncf-adopts-service-mesh-performance-standard-established-by-layer5) (SMP)，这是一套用于测量服务网格效率的工具。SMP 提供了一个开源框架来定义标准化的基准测试实践、性能测试配置和测量，作为创建 MeshMark 指数以对服务网格进行评级的工作的一部分。IEEE 还将在本月晚些时候发布一套服务网格性能方法，该方法是与 Layer5、Intel、Red Hat 和 HashiCorp 的工程师合作开发的。

Layer5 首席执行官 Lee Calcote 表示，目标是让 it 团队更容易根据他们特定的用例需求来确定使用哪个服务网格。

几个服务网格平台开始获得牵引力，作为管理应用程序编程接口([API](https://devops.com/?s=APIs))和在较低层网络和安全 API 之间提供一个抽象层的手段，使这些服务更容易被开发人员以编程方式访问。

Meshery 本身是 SMP 的一个实现，也是为服务网格接口(SMI)创建的一致性工具，SMI 是一个独立的 CNCF 项目，旨在促进服务网格之间的互操作性。Meshery 基于一组微服务，旨在使平台易于扩展。

这种方法使得使用 Meshery 项目中的一系列管理工具来管理可能部署在虚拟机和 Kubernetes 集群上的服务网格的多个实例成为可能。

Meshery 支持 AWS App Mesh、Citrix Service Mesh、HashiCorp Consul、Istio、库马、Linkerd、网络服务 Mesh、NGINX 服务 Mesh、开放服务 Mesh 和 Traefik Mesh。Meshery 还以模板的形式为 IT 团队提供了 60 多种最佳实践，可用于部署服务网格。

![](img/113314af6ed21d20df30b6beb6f47987.png)

就在企业中采用服务网格而言，现在还为时尚早。大多数 IT 团队仍然依赖代理软件或网关来管理 API。然而，随着需要管理的 API 数量的稳步增长，用不了多久，许多 it 团队就会开始至少评估一个服务网格。

从长远来看，这些服务网格可能会对 IT 管理产生深远的影响。很明显，服务网格还为调用网络和安全服务提供了更高层次的抽象。事实上，服务网格最终可能会在推动网络和安全运营与 DevOps 最佳实践的融合方面发挥关键作用。

与此同时，IT 团队将需要决定他们希望在单个服务网格上实现多大程度的标准化，而不是让各个团队实现他们自己的首选平台，将来有一天可以通过 Mashery 进行集中管理。无论如何，管理和调用 API 的方式将很快彻底改变。