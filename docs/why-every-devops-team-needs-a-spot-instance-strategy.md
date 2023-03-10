# 为什么每个 DevOps 团队都需要一个现场实例策略

> 原文：<https://devops.com/why-every-devops-team-needs-a-spot-instance-strategy/>

大多数 DevOps 团队广泛使用公共云，并将大量精力放在降低云成本上。根据[一项估计](https://devops.com/cloud-waste-to-hit-over-14-billion-in-2019/)，2019 年美国企业仅在浪费、未使用的云资源上就花费了 141 亿美元。 [Spot instances](https://devops.com/?s=spot%20instance) 是降低公共云服务成本的最重要方式之一。

Spot 实例并不是新的发展。2009 年，亚马逊是第一个宣布这种定价方式的公司，将云计算变成了一个受供求关系影响的市场。微软 Azure [花了十多年时间](https://azure.microsoft.com/en-us/blog/announcing-the-general-availability-of-azure-spot-virtual-machines/)跟进，于 2020 年 5 月宣布其 [spot 虚拟机服务](https://spot.io/what-are-azure-spot-virtual-machines/)。

现货定价模式表面上很简单，但实施起来可能很复杂。Spot 实例是云提供商出售其未使用容量的方式。当没有人通过常规的按需定价模式订购计算实例时，云提供商会以非常优惠的价格将其拍卖，通常比按需成本低 10%至 20%左右。

但是，想要拿到这个八折到九折，并不是那么简单。当另一个云客户请求 spot 实例时，云提供商会发送一个通知，您需要在实例终止之前立即转移您的工作负载。这使得很难将 spot 实例用于有状态的、数据库驱动的应用程序，或者那些需要高可用性的应用程序。

这不是唯一的挑战。市场价格是波动的，比按需定价更不稳定。这意味着随着时间的推移可以实现的折扣水平相对不可预测。

然而，精明的 DevOps 团队至少可以通过三种方式充分利用 spot 实例:

1.  **自动化** —DevOps 团队精通一系列自动化工具，包括配置管理、基础设施即代码(IaC)和云提供商自动扩展工具。这些可以用来管理集群中的工作负载，并在 spot 实例终止时自动进行故障转移。
2.  **开发/测试环境** —DevOps 团队负责建立开发和测试环境，这些环境非常适合于 spot 实例，因为它们通常可以容忍短暂的中断，并且在许多情况下不是有状态的。
3.  **CI/CD 作业**—在 Jenkins、GitLab 和类似工具上运行作业可以很容易地在 spot 实例上扩展。这些作业是无状态的，如果一个实例被删除，很容易在另一个实例上重新运行作业。

## AWS Spot 实例

AWS Spot 实例可以让你以非常优惠的价格购买未使用的 Amazon EC2 计算能力。您可以指定一个价格，当以这个价格提供一个 spot 实例时，它将与您选择的 Amazon 机器映像(AMI)一起启动。

### Spot 实例如何在 AWS 上工作

现货实例以可变现货价格定价，该价格根据供求状况进行调整。要查看当前费率，请使用 [AWS Spot 实例顾问](https://aws.amazon.com/ec2/spot/instance-advisor/)。

您创建一个 spot 实例请求，指定您感兴趣的实例类型，以及它们应该运行的可用性区域(AZ)。如果容量可用，并且它们的当前价格低于您的最高出价，则实例被启动。

Spot 实例将继续运行，直到:

*   容量不再可用(因为实例是由按需客户请求的)。
*   价格已经超过了你的最高出价。
*   您请求终止实例，或者它被自动缩放自动终止。

您还可以订购具有预定义持续时间的 spot 实例，然后在整个持续时间内支付固定的小时费率(即使市场价格在此期间发生变化)。

### 自动化选项

您可以在 Amazon EC2 上自动缩放实例，包括单个自动缩放组中的按需实例和即时实例。如果在向上扩展时 spot 实例不可用，则该组可以使用常规的按需实例。

Amazon 还支持混合使用保留实例和节省计划(通过承诺特定时间段或总容量来节省按需实例的其他方法)。因此，您可以在同一个自动缩放组中组合多种保存方法。

您可以通过跨运行在多个 az 中的多个实例类型部署应用程序来提高可用性。通过允许多种实例类型，您可以利用多个池，并增加在需要时获得 spot 实例的机会。

## Azure Spot 实例(Spot 虚拟机)

Azure 提供 Spot 虚拟机，让您可以访问未使用的计算容量。您可以请求单个 spot 虚拟机，或者使用 Azure 虚拟机规模集(VMSS)启动多个 spot 虚拟机。Spot 虚拟机取代了以前的低优先级虚拟机功能，该功能允许您以较低的价格购买 Azure 上需求较少的虚拟机。

Azure 上虚拟机的现货价格取决于 Azure 区域中特定实例大小和 SKU(实例类型)的可用总容量。Azure 承诺缓慢地改变价格，避免突然上涨，以保持价格稳定，并使预算管理更容易。

像在亚马逊上一样，折扣波动很大，现货虚拟机可以比相同虚拟机的基础价格便宜 90%。

## Spot 虚拟机如何在 Azure 上工作

Azure 门户提供对 Azure spot 虚拟机的访问。创建 spot 虚拟机时，您可以看到所选区域、映像和虚拟机大小的当前价格。为了保持一致，价格始终以美元为单位，即使您使用不同的记账本位币。

逐出 spot 虚拟机有两个选项，您可以选择逐出 spot 虚拟机的条件:

*   **最高限价驱逐**—你设定一个最高竞价，当现货 VM 超过这个价格时，它就会被驱逐。
*   **容量驱逐**—您总是支付虚拟机的当前价格(没有设置最高价格)，当 Azure 没有足够的请求虚拟机类型的容量时，您的虚拟机将被驱逐。

当一个虚拟机被驱逐时，Azure 会应用一个被称为停止/解除分配的驱逐策略。这意味着实例被暂停，但连接的磁盘仍然存在，您仍然需要为它们付费。当价格下降或容量变得可用时，实例会重新启动并继续处理相同的磁盘数据。

### 自动化选项

Azure 提供虚拟机规模集(VMSS)，可以自动增加或减少运行应用程序的虚拟机数量。您可以创建一个包括 spot 虚拟机的扩展集，随着应用程序的扩展，将会添加更多可用的 spot 虚拟机。点规模集在单个故障域中运行，不保证高可用性。与 AWS 不同，Azure 目前不允许混合按需虚拟机和定点虚拟机。

Amazon 和 Azure 都使用 spot 实例提供了强大的成本节约功能。Azure 的产品较新，提供不太先进的竞价和自动缩放功能，但随着服务的成熟，这些功能有望增加。

无论 DevOps 团队选择在 AWS、Azure 或两者中运行，他们都不能忽视 spot 实例，特别是对于低关键性工作负载，如开发/测试和 CI/CD 作业执行。