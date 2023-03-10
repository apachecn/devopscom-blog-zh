# 哈希公司为 Azure 云更新 Terraform 工具

> 原文：<https://devops.com/hashicorp-updates-terraform-tool-for-azure-cloud/>

HashiCorp 今天宣布，它已经更新了它创建的 Terraform 实例，以自动配置 Microsoft Azure 云上的虚拟机，从而为 it 团队提供更精细的控制。

2.0 版。的 Terraform (TF) AzureRM Provider 将允许 IT 团队按类型分别配置虚拟机，例如 Windows 和 Linux。

此外，TF azure RM Provider 2.0 版将允许用户为资源指定自定义超时。以前，默认情况下超时设置为一小时。

最后，TF AzureRM Provider 2.0 移除了已弃用的资源、数据源和字段。TF AzureRM Provider 目前提供对 374 个资源和 119 个数据源的访问。

HashiCorp 的产品营销副总裁 Amith Nair 表示，目标是为 IT 团队提供一套工具，用于自动化 Azure 上虚拟机的配置，比微软目前提供的工具更容易访问。

Nair 说，HashiCorp 看到越来越多的人采用微软 Azure，这反过来创造了对更容易大规模部署虚拟机的工具的需求。事实上，Nair 指出，随着越来越多的工作负载转移到公共云中，IT 自动化面临的阻力就越小，因为管理员正在寻找以目前前所未有的规模管理 IT 的方法。当然，许多组织在首次采用一套最佳 DevOps 实践时，获得了使用 Terraform 等工具的第一次经验。

不太清楚的是，与 Linux 相比，在 Windows 实例上配置了多少虚拟机。毫无疑问，微软已经成为亚马逊网络服务(AWS)在公共云中统治地位的最强有力的挑战者。然而，这一成功很大程度上是因为微软支持在 Azure cloud 上同时发布 Linux 和 Windows Server。当然，有许多组织，比如沃尔玛，更喜欢在 Azure 上标准化，只是因为他们认为亚马逊是一个竞争对手。然而与此同时，也有很多公司同时雇佣了 AWS 和 Azure。

Nair 说，大多数采用多种云的组织倾向于孤立地管理它们。然而，随着云计算的总成本随着部署的每一个额外工作负载而持续上升，预计有一天会有更多的组织寻求在真正的混合云计算环境中统一多个云的管理。自然地，许多这样的组织最终会倾向于可以跨多个云使用的工具。

与此同时，无论是 it 管理员还是开发人员自己在云中配置虚拟机，多亏了 Terraform 等工具，在云中设置虚拟机所需的时间和精力现在可以忽略不计。现在的挑战与其说是找到自动化工具，不如说是驾驭所有自然发生的文化变革。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)