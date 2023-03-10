# Chef 在 AWS Cloud 上增加了对 Arm Graviton 2 处理器的支持

> 原文：<https://devops.com/chef-adds-support-for-arm-graviton-2-processors-on-aws-cloud/>

Chef 本周宣布，其作为代码管理和测试基础设施的产品现在支持亚马逊网络服务(AWS)云上 Arm 的 Graviton 2 处理器。

AWS 本周宣布在其公共云上推出 M6g 处理器实例[。M6g 处理器基于 64 位 Arm Neoverse N1 架构，由 Arm 和亚马逊旗下的 Annapurna Labs 联合设计。](https://aws.amazon.com/blogs/aws/new-m6g-ec2-instances-powered-by-arm-based-aws-graviton2/)

据 AWS 称，在一次预览程序中，Honeycomb 等平台在 M6g 上消耗的实例比广泛使用的 AWS C5 实例少 30%。数据分析软件提供商 Treasure Data 报告称，与同等规模的 M5 实例相比，性能提高了 30%，而成本降低了 20%。Amazon ElastiCache 服务团队发现，在 Redis 上，M6g 实例的吞吐量比 M5 实例提高了 50%。

此外，AWS 本周透露，它还计划基于 64 位 Arm 处理器添加计算优化的 C6g 实例和内存优化的 R6g 实例。

云中的 Arm 处理器有望为构建跨 AWS 云服务的混合物联网(IoT)应用和嵌入式系统中广泛使用的 Arm 处理器实例提供基础。此前，AWS 推出了一项 AWS Greengrass 计划，通过该计划鼓励开发人员在[边缘计算平台](https://devops.com/aws-adds-gui-to-snow-edge-computing-family/)上构建和部署支持云的物联网应用。

Chef 业务开发副总裁 Vikram Ghosh 表示，DevOps 团队现在可以使用他们用来在 AWS 云上运行的其他类型的处理器上供应实例的相同 Chef 工具来自动供应 Arm 处理器。

![](img/48bd13793195e02b665b2f844e0dd43a.png)

Ghosh 指出，用不了多久，Arm 处理器的 64 位实例就会出现在其他云计算平台上。事实上，随着 Arm 处理器和图形处理器单元(GPU)的兴起，云中可用的处理器类型从未如此多样化，Ghosh 表示，这推动了对以代码形式管理基础设施的工具的需求增加。

就采用最佳 DevOps 实践来构建和部署物联网应用而言，现在仍处于早期阶段。然而，物联网应用的高度分布式特性(在许多情况下需要频繁更新)有助于使用 DevOps 流程更有效地管理它们。在大多数情况下，这些物联网应用程序代表“绿地”应用程序，其中没有可能造成文化冲突的遗留流程。

预测新冠肺炎疫情之后对边缘计算应用的需求是很困难的。然而，普遍的预期仍然是，更多的应用程序代码将更接近它被消费的点，特别是当 5G 无线网络服务变得更加可用时。事实上，许多这些应用程序现在正在构建，预计这些网络服务能够将边缘计算应用程序与后端云资源连接起来。

一旦构建了这些应用程序，下一个巨大的挑战将是找到一种方法来保护它们并持续更新它们。然而，与此同时，今天在云中为基于 Arm 处理器的边缘计算平台构建的边缘计算应用程序的数量将大幅增加。