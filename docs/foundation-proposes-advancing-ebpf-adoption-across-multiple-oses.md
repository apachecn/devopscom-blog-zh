# 基金会提议跨多个操作系统推进 eBPF 的采用

> 原文：<https://devops.com/foundation-proposes-advancing-ebpf-adoption-across-multiple-oses/>

eBPF 基金会计划推进一种方法的采用，使沙盒程序在内核级运行得更快，今天它作为 Linux 基金会的一个分支被推出。

被称为 [eBPF](https://devops.com/?s=eBPF) 的技术最初是为 Linux 开发的。eBPF 基金会现在致力于在所有操作系统中扩展 eBPF 的使用。eBPF 基金会的成员包括脸书、谷歌、等价、微软和网飞。

利用 eBPF 的网络和安全工具提供商 Isovalent[的首席技术官兼联合创始人托马斯·格拉夫(Thomas Graf)表示，随着核心技术在更广泛的平台上得到测试和验证，IT 组织应该会看到该技术与其他操作系统一起成为 Windows 的一部分。](https://containerjournal.com/topics/container-networking/isovalent-container-networking-in-2021-using-ebpf/)

实际上，eBPF 改变了操作系统的设计方式。它在内核和用户空间之间架起了一座桥梁，使开发人员能够跨多个子系统组合和应用逻辑，而这些子系统在历史上是完全相互独立的。例如，这种方法使安全工具能够扩展到能够以更高的吞吐量识别威胁的程度，从而在同时发起的网络安全攻击数量不断增加的情况下提高整体规模。

![](img/1e3c51f75c51ced926bdeeeb73b0c435.png)

目前，eBPF 被云服务提供商等网络规模的公司广泛采用。脸书在其数据中心使用它作为主要的软件定义的负载平衡器，而谷歌在其托管的 Kubernetes 产品中使用开源的 Cilium 网络软件。

然而，在部署了 Linux 的内部 IT 环境中的采用更为有限，这仅仅是因为已经优化了网络、安全性和存储产品以利用 eBPF 的供应商数量仍然相当有限。

例如，Sysdig 最近发布了一个使用 eBPF 的开源 Falco 容器安全平台实例。Tigera 还提供了[其容器网络平台的一个实例，该平台在 Linux 内核层利用 eBPF](https://containerjournal.com/topics/container-networking/tigera-embraces-ebpf-to-advance-container-networking/) 。

最后，Graf 指出 eBPF 最大的好处是效率。随着越来越多的供应商利用有朝一日将广泛应用于多个操作系统的功能，安全、网络和存储平台的总处理成本将会下降。

同时，IT 组织最好询问他们的供应商他们计划何时支持 eBPF。云服务提供商通常要求 it 更高效地交付他们自己的托管服务，因此任何希望向这些提供商销售平台的供应商都需要支持 eBPF，以大规模提升性能。接下来的问题是确定哪些采用了该技术的平台也可用于内部 IT 环境中，以寻求类似的优势。

不管采用哪种方法，很明显，很快就有理由不仅升级网络、存储和安全平台，还升级尚不支持 eBPF 的操作系统实例。DevOps 团队最好做相应的计划，因为最终受益于 eBPF 的平台数量遍布整个企业。