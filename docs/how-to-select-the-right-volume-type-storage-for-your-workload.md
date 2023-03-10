# 如何为您的工作负载选择正确的卷类型/存储

> 原文：<https://devops.com/how-to-select-the-right-volume-type-storage-for-your-workload/>

AWS 服务处于云服务食物链的顶端，几乎是每个考虑迁移到云的企业的热门话题。在任何云迁移的旅程中，许多隐藏的陷阱等待着毫无准备的人。您已经调配的卷看似完美匹配，但您确定它们适合您的工作负载并具有最佳的性价比吗？今天，我们将让为您的工作负载选择存储类别这一困难任务变得不那么复杂。

### 在 EBS 的世界里

AWS EBS 目前提供三类可观的存储:硬盘驱动器、通用 SSD、预配置 IOPS，以及一种您很可能永远不需要使用的存储——磁性存储。尽管我将对每种类型进行简要描述，但我将重点关注最广泛使用的卷类型—通用卷。

### GP 存储–共同的选择

这是几乎所有 AWS 用户的主要存储。从驾驶角度来看，它为您提供了最佳性价比，通常用于不需要起重的任务。GP 存储的范围从 1gb(GiB)到 16tb(TiB ),提供每秒 128 到 1，000 兆字节(MiB/s)的吞吐量，这很可能适合您的使用情形，除非工作负载非常特殊。

GP 存储有多种类型，每种都有不同的定价和特征，我将在下面提供一些细节。

### GP2–面向大众的老一代固态硬盘

GP2 是 EC2 实例、开发环境和较轻/不太重要的数据库的引导卷的典型解决方案。这是最受欢迎的选项之一，尽管它的流行来自旧习惯，而不是实际上是一个完美的拍摄。GP2 卷的性能与其大小成比例——它们越大，速度越快。尽管如此，这些似乎是一个不错的选择，但老实说，它们并不完美。房间里最大的大象是你必须记住的术语——“突发学分”。

### 突发学分——你商业工作的数学作业

配置一个 GP2 卷，您将获得 540 万突发信用的一次性授权，您可以使用它在需求高峰期间更好地处理输入/输出。更多的令牌意味着您将能够更长时间地维持更大的性能需求，将您的存储提升至 3000 IOPS，只要您口袋里有足够的令牌。
当您进行“turbo”时，它们会被耗尽，而当您没有全速使用磁盘时，它们会累积起来，将未使用的性能保存起来，以备您最需要时使用。将它们全部烧掉，您的 IOPS 性能会降至基础值，吞吐量会降至基准 IOPS 乘以最大 I/O 大小。

GP2 存储卷的性能可以通过以下公式计算:
以 MiB/s 为单位的吞吐量=((以 GiB 为单位的卷大小)×(每 GiB 3 个 IOPS)×(KiB 的 I/O 大小)

直到你的音量变得如此之大，以至于它的基本性能超过了突发的程度，你都必须把它们背下来。这个点在哪里？相当高，大约为 1.1 TB(1024 GiB)—即使对于中型企业来说，这也是一个很大的磁盘空间，尤其是因为这些卷不能装载到多个目标上。

![](img/da4aa44d8b78b0129994b1d72e008b75.png)

图 1:特定卷大小的最大 IOPS 图(来源: [AWS 文档](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html)

除非您正在为数十或数百个 Docker 容器部署一个像 EC2 主机实例这样的吞噬磁盘的庞然大物，或者您计划在未来几年运行一个巨大的 Elasticsearch 节点，而没有清理例程，否则您不太可能需要这么大的空间。此外，在提到的两种情况下，您可能会先用完 CPU 和 RAM 对于这些情况也有更好的替代方案，更不用说缺乏维护绝对不是一个好的做法。

此外，对于几乎所有的用例——web 服务、web 应用程序、数据库、与 Docker 一起使用的 EC2 实例等等——几乎任何东西都比 GP2 好。

幸运的是，在 2014 年，GP3 的引入带来了一些巨大的改进。

### GP3——新来者

虽然不是一个真正的“新”玩家，但在体验了 GP2 的内部运作后，GP3 卷是一个受欢迎的改进。相比之下，它们的性能更好，成本更低，使您能够更轻松地根据自己的需求扩展运营。信用余额激增的日子已经一去不复返了。

这种存储类的黄金法则是“混合搭配”。“这里的基准性能是 GP2 卷、3，000 IOPS 和 125 MiB/s 的最大突发性能。如果您的业务需要更多，您可以额外购买其中任何一种，只需为您感兴趣的内容支付额外费用。

限制相当宽松。您可以购买每 GiB 高达 500 IOPS(对于至少 32 GiB 卷，上限为 16，000 IOPS)，或者每 GiB 高达 0.25 MiB/s(对于至少 8 GiB、4，000 IOPS 或更多的卷，上限为 1，000 MiB/s)。

如果你以前对你的 GP2 卷很满意，那么几乎可以保证你的公司也会对 GP3 同样满意，而且你会节省相当比例的存储成本，甚至高达 20%。

假设你不需要比 GP2 提供给你的更多的东西，进行转换。为了更容易地降低这些成本，AWS 现在会自动将您的新 GP3 卷的 IOPS 和吞吐量设置为与 GP2 完全相同。少猜测，少胡闹，多点好东西。只需点击几个按钮，节省一些现金，没有任何附加条件。

这是我为每个“一般”或“典型”工作负载推荐的存储类别。对于几乎所有不期望大量磁盘操作的业务用例来说，这是一个很好的起点，但是当对磁盘能力的可怕需求到来时，它已经准备好进行扩展。

GP3 可以轻松处理 EC2 实例的引导卷角色。它既可以托管简单的应用程序，也可以托管稍微复杂一点的应用程序、数据库(如 MySQL 和 PostgreSQL ),或者托管容器化环境中的混合应用程序，尤其是在多节点配置中或者作为 Kubernetes 集群的一部分。如果您安装了 CSI 驱动程序，Kubernetes 的 Zesty Disk 会自动处理此开关

到时候，它可以根据需求进行扩展。在某些情况下，使用 GP3 提供高速存储甚至可能比 IO1/IO2 类型更便宜，IO1/IO2 类型专用于速度和我们列表中的下一个。

### IO 存储级别—对速度的需求

IO 存储类的推出是为了满足基于极高耐用性、高读/写速度和最低可用延迟的业务需求。它需要达到一定的标准才能显示其真正的潜力，而且成本要高得多。但是，反过来，它提供了无与伦比的速度和可靠性，以及一些您在任何其他存储类型中都找不到的功能。

例如，如果您希望为基于磁盘的高速数据库配置一个卷，或者为多个大规模电子商务实例创建一个 MySQL 数据库主机，那么这种卷类型非常有用，尽管从 RDS 到多实例数据库(例如 MySQL Galera)都有多种选择。如果您需要快速接受大量数据以便用 ML 算法进行处理，这也是合适的。

### IO1/IO2 与 IO2 Block Express 您需要哪种“最快”的？

IO2 Block Express 相当于强效类固醇上的 IO2。您可以获得四倍的 IOPS 和吞吐量限制，不到毫秒的延迟，而且令人惊讶的是，没有额外费用。是的，你没看错，它们的价格是一样的。此外，调配超出标准 IO2 实例限制的额外 IOPS/吞吐量实际上成本更低。

如果您决定使用 IO2 并满足需求(一个[特定类型的 EC2 实例](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/provisioned-iops.html#io2-block-express))，您肯定应该考虑 Block Express——如果默认情况下它还没有运行的话。

你什么时候运行 IO2？嗯，凭借其强大的功能和高昂的价格，这个类致力于最依赖磁盘、吞吐量大和 IOPS 依赖的怪物。例如，用于证券交易所的数据处理机器、全球日志接收大型机，或者为非常苛刻的工作负载准备的多 pod Kubernetes 节点—毫无疑问是存储巨头。当你需要一台能尽可能多出拳的机器时，这是你的不二选择。

那 IO1 呢？这是低延迟、高 IOPS 和价格之间的折衷。当您需要的不仅仅是一般用途，但仍不足以获得最快的存储时，这是一个不错的选择。请记住还有一个额外的缺点——耐用性较差。每年 0.2%的故障率听起来并不多，但如果您考虑到几十或几百个驱动器、绝对关键的工作负载或两者，这绝对会产生巨大的影响。

### 那么，我应该为我的工作负载选择哪一个呢？

如您所见，退一步说，EBS 的世界相当复杂。因此，我制作了一个图表，可以简化您的用例的选择过程:

![](img/0e1207b396025c96d6795a1e1798a979.png)

### 奇异的磁盘和如何驯服它们

选择正确的存储类别是一个艰难的决定，但好处是值得的。只需一次操作，您就可以提高实例的性能，并在下一次开具发票时节省成本。