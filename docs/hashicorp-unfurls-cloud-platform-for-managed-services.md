# 哈希公司推出托管服务云平台

> 原文：<https://devops.com/hashicorp-unfurls-cloud-platform-for-managed-services/>

HashiCorp 今天在其在线 [HashiConf Digital](https://hashiconf.com/digital-june/) 活动上发布了 [HashiCorp 云平台](https://www.globenewswire.com/news-release/2020/06/22/2051130/0/en/HashiCorp-Launches-Multi-Cloud-Infrastructure-Automation-as-a-Service-with-HashiCorp-Cloud-Platform.html) (HCP)，通过该平台，HashiCorp 打算将其所有软件作为完全托管的服务提供。

与此同时，HashiCorp 宣布了对 HashiCorp Terraform 的更新[的公开测试，这是一个开源工具的策划实例，用于配置 IT 基础设施，增加了额外的工作流功能。](https://www.hashicorp.com/blog/announcing-the-terraform-0-13-beta)

最后，对 Nomad 的[更新，一个用于容器化应用环境的集群管理器和调度器，增加了对多个集群以及由云本地计算基金会(CNCF)定义的容器网络接口(CNI)规范的支持。](https://www.hashicorp.com/blog/announcing-hashicorp-nomad-0-12-beta)

HashiCorp 云服务产品营销总监罗布·吉诺瓦(Rob Genova)表示，尽管该公司以前将一些产品作为托管服务提供，但 HCP 将作为 HashiCorp 代表最终客户管理其软件更新的基础。

HCP 上的第一个托管服务，现在在私人测试中可用，是部署在亚马逊网络服务(AWS)上的 Consul service mesh 的实例，接下来是由 HashiCorp 开发的秘密管理软件 Vault 的实例，也将部署在 AWS 上。

HCP 的核心是 HashiCorp 虚拟网络(HVN)，它围绕一个孤立的单租户网络提供跨云提供商的通用抽象。每个 HVN 中可以部署多个服务。HashiCorp 承诺，未来 HVN 将实现跨云提供商的对等和跨提供商的软件集群。Genova 补充说，将根据客户需求增加对其他云服务的支持。

![](img/12fc5267e77944c15a7e5f4240411cb3.png)

HCP 将以现收现付的定价模式提供，以最大限度地降低前期成本，Genova 表示，这将使较小的团队和组织更容易获得 Consul 和其他 HCP 服务。只有当工作负载扩大时，成本才会增加。他说，开发和生产定价选项都将可用。

Genova 补充说，HashiCorp 已经提供了对 Consul 和 Terraform 托管实例的访问，它将继续与 HCP 一起提供这些实例。

Genova 表示，越来越多的组织倾向于让 HashiCorp 代表他们管理领事、金库、地形和游牧。Genova 表示，在许多组织的 IT 资源有限的时候，许多组织希望将有限的内部资源投入到构建和部署应用程序上，而不是维护应用程序所需的基础架构上。

尚不清楚在新冠肺炎疫情引发的经济衰退之后，有多少组织会选择更多地依赖托管服务。在许多组织裁员或冻结员工人数的时候，所有的选择都在考虑之中。许多内部 IT 团队可能偶尔会采用托管服务来扩展他们自己的能力。在其他情况下，开发人员可能会完全绕过 IT 运营团队。

在疫情之后，Genova 注意到更多的组织只是希望在云中部署资源，以确保可用性，同时获得更高的灵活性。

不管选择哪条路，IT 团队觉得更有必要自己做所有事情的日子，不管是好是坏，都在彻底改变。