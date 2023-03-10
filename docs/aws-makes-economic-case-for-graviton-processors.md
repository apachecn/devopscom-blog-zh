# AWS 为 Graviton 处理器提供经济支持

> 原文：<https://devops.com/aws-makes-economic-case-for-graviton-processors/>

亚马逊网络服务(AWS)正在基于 AWS Graviton 处理器的亚马逊弹性计算云(Amazon EC2)上提供预览版 [C7gn 实例](https://aws.amazon.com/about-aws/whats-new/2022/11/announcing-amazon-ec2-c7gn-instances-preview/)。与上一代 C6gn 实例相比，C7gn 实例提供高达 200 Gbps 的网络带宽和高达 50%的数据包处理性能。

在 [AWS re:Invent 2022](https://reinvent.awsevents.com/?) 大会上宣布，这些实例基于 AWS 提供的 Arm 处理器架构，作为 x86 处理器的替代方案。

亚马逊 EC2 产品管理总监 Rahul Kulkarni 表示，随着整体经济前景走软，人们对更高效的 AWS Graviton 处理器的兴趣急剧上升。他补充说，随着部署在云中的应用程序总数持续增长，越来越多的 IT 团队正在寻找降低成本的方法。

虽然还不清楚有多少应用程序正在开发中，以在 Arm 处理器上运行，但 Kulkarni 指出，对于大多数应用程序来说，重构现有应用程序以在 Arm 处理器上运行的过程不像以前将应用程序从一种处理器转移到另一种处理器时那样密集。

总体而言，AWS 现在在其云平台上提供了超过 600 种类型的虚拟机实例，包括一组在 preview 中提供的 [Inf2 实例](https://aws.amazon.com/about-aws/whats-new/2022/11/aws-announces-amazon-ec2-inf2-instances-preview/)，这些实例基于定制的 AWS 处理器，这些处理器针对处理工作负载进行了优化，包括驱动人工智能(AI)模型的机器学习算法。

Kulkarni 指出，每个 AWS 实例都利用了一组 AWS Nitro 卡，这些卡卸载了虚拟化产生的开销，因此 IT 组织可以充分利用计算资源，而不必分配任何资源来运行虚拟化软件。他补充说，虚拟化税反而被 AWS 吸收，以降低客户的总云成本。

此外，越来越多的客户正在利用 AWS Cost Optimizer 和 AWS Karpenter for Kubernetes 集群等工具，这些工具采用机器学习算法来识别降低云基础设施成本的机会，例如通过将工作负载转移到不同的服务类别。

当然，有多种控制云成本的策略，从承诺以折扣率每年消耗指定数量的计算资源，到更多地依赖在有限时间内可用的现场实例。将工作负载从一个云提供商转移到另一个云提供商的效率较低，因为迁移工作负载的总成本可能很高，具体取决于调用的专有应用编程接口(API)的数量。

不管采用哪种方法，允许开发人员随意调用云资源的日子似乎已经结束了。在云时代，企业 IT 组织更加关注 IT 的总成本。因此，他们中的许多人正在采用财务运营(FinOps)最佳实践来最大限度地利用云基础架构资源。

目前还不清楚 It 组织将如何欣然接受 AWS Graviton 以及其他类别的 Arm 处理器来实现这一目标，但随着经济前景继续保持不确定性，毫无疑问，所有选项现在都摆在桌面上。