# 影响 Java 内存消耗的核心因素

> 原文：<https://devops.com/core-factors-influencing-java-memory-consumption/>

众所周知，Java 对资源有着贪得无厌的胃口，要求严格控制不超过预算限制。然而，最新的 JDK 更新和其他开发已经帮助 Java 运行时在内存使用方面变得非常灵活。如果配置得当，Java 可以为不同类型的应用带来成本效益——云原生或遗留、微服务或单片。今天，有可能从一开始就把 Java 做得非常小，然后在不消耗不必要的资源的情况下逐渐扩大规模。

在这里，我们将仔细研究影响 JVM 中资源使用的因素，看看哪些工具可以提供帮助，以及如何调整流程以获得更大的弹性和可伸缩性，最终降低 TCO。

# 扩展可能性:虚拟化与容器化

在 JVM 中有几个扩展选项:垂直、水平和两者的组合。为了最大化结果，从垂直扩展配置开始是很重要的，这种配置可以根据当前的负载水平优化每个实例内部的 RAM 和 CPU 使用。下一步，在水平扩展时，这些设置将在所有实例中复制。

### 虚拟机扩展

当开始在一个 VM 中运行一个项目时，选择合适大小的机器是很重要的，因为太小的实例会导致性能问题，甚至在负载高峰期间停机。然而，过度分配将导致在正常负载或空闲期间浪费未使用的资源，这些资源仍然必须付费。这可能是一个艰难的选择。

从较小的虚拟机开始，然后随着项目的增长进行扩展。当只需要多一点资源时，云供应商可以为您提供两倍的规模，因为这是最常用的扩展步骤(例如，请参见下面的 AWS 服务)。

![](img/10eca813e9884f438ab95b3c2928a170.png)

在这种扩展过程中，通常会暂停当前虚拟机来迁移和重新部署应用程序。这不可避免地导致一些停机时间，并需要人工干预。

内存膨胀提供了一种可能的方式(尽管相当复杂)来动态修改虚拟机内部的资源量，而不会导致停机。然而，这一过程不是完全自动化的，需要特殊的工具来监控主机和客户操作系统中的内存压力，然后根据需要激活垂直扩展。因此，内存膨胀在实践中不能很好地工作，因为内存共享应该是自动的，以呈现预期的优势。

不幸的是，在资源使用方面缺乏虚拟机弹性和效率通常会导致超额支付。

### 容器缩放

容器化提供了一种新的应用程序打包方式，通过使用 [cgroups](https://en.wikipedia.org/wiki/Cgroups) 在同一主机上的容器之间自动共享资源，使资源消耗更加精细和灵活。与虚拟机不同，容器的边界可以轻松地扩大和缩小，而无需暂停和重启正在运行的实例。

![](img/facc1968e65b0e22cf2a34cd097d20e9.png)

有两种类型的容器:应用程序容器和系统容器。两者都使用相同的扩展方法，但它们的目的不同。应用程序容器(如 Docker 或 rkt)通常更轻量级，运行单个进程，主要用于创建新项目，因为从预先存在的 Docker 图像模板构建它们很容易。

系统容器(LXD，OpenVZ)的行为就像一个完整的操作系统，可以运行全功能的初始化系统。这种类型的容器更适合于单片和遗留应用程序，因为它可以重用最初创建的设计和重要的“老派”设置。

与虚拟机相比，即使系统容器也要薄得多，因此向上和向下扩展花费的时间要少得多。横向扩展过程非常精细和流畅，因为容器可以轻松地从头开始配置或克隆。

### 垃圾收集器选择

为了在基于 Java 的容器中最大化上述垂直伸缩的效率，选择合适的垃圾收集器(GC)并根据项目需求对其进行调优是非常重要的。

让我们回顾一下五种广泛使用的垃圾收集器解决方案:

*   **G1:** 从 JDK 9 开始，这个现代的收缩垃圾收集器默认是启用的。它的一个主要优点是能够压缩空闲内存空间，而不会有很长的暂停时间和取消对未使用堆的提交。这种 GC 被认为是垂直扩展的最佳生产就绪选项。
*   **Parallel:**JDK 8 中的默认 GC，它是低暂停的好选择，但不是内存收缩的好选择。这使得它不适合灵活的垂直缩放。
*   **Serial，conmarksweep(CMS):**这两个都是收缩式垃圾收集器，能够垂直扩展 JVM 中的内存使用。但是与 G1 相比，它们需要四个完整的 GC 周期来释放所有未使用的资源。JDK 9 中一个新的 JVM 选项( [-XX:-ShrinkHeapInSteps](https://bugs.openjdk.java.net/browse/JDK-8146436) )可以通过在第一个完整的 GC 周期后立即关闭提交的 RAM 来加速内存释放。
*   Shenandoah: Shenandoah 是垃圾收集器中的后起之秀，有望成为 JVM 垂直伸缩的最佳解决方案。与其他方法相比，它的主要优点是能够在实时模式下收缩，而不必调用完全 GC，这有助于消除显著的性能下降。

让我们比较收缩 G1 和非收缩并行的内存行为:

通过并行，未使用的 RAM 不会释放回操作系统。JVM 永远保留它，即使忽略显式的完整 GC 调用。因此，即使您的应用程序具有较低的 RAM 消耗，未使用的资源也不能与其他进程或其他容器共享，因为它完全分配给了 JVM。

![](img/a1131b2f971cb37e53072f28807a05f2.png)

与前面的示例相比，现代收缩 G1 垃圾收集器显著提高了资源利用率。保留的 RAM 会根据实际使用量的增长而缓慢增加。最大堆限制内的所有未使用资源不会因闲置而浪费，而是可供同一主机中运行的其他容器或进程使用。

![](img/7d76be19658f60d927d525072b2f5879.png)

总而言之，使用非收缩 GC 或非最佳 JVM 启动选项的 Java 应用程序持有所有分配的 RAM。为了纵向扩展 Java，垃圾收集器应该在运行时提供内存收缩。换句话说，它必须将所有活动对象打包在一起，删除垃圾对象，取消提交，并将未使用的内存释放回操作系统。

# 云提供商的收费模式

如今，大多数云供应商都提供“按需付费”的计费模式。这意味着可以从较小的机器开始，然后随着项目的增长，添加更多的服务器或迁移到两倍大的实例。但是如上所述，通常您会保留比应用程序实际消耗更多的资源，以避免负载高峰期间停机的风险。因此，许多组织支付了过多的费用，因为帐户是按虚拟机计费的，而不是基于内部消耗的资源。

与此同时，有些提供商提供“按使用量付费”的计费方法，这在容器化、资源粒度和自动垂直扩展的帮助下成为可能。付款基于集装箱内的资源单位。并且根据当前时刻的负载动态地提供和回收所需的容量。因此，您将根据实际用量付费，而无需进行复杂的重新配置来扩大或缩小规模。

考虑所有这些因素并实现正确的设置可以显著降低 Java 托管资源的成本，并从整体上积极影响应用程序的性能。云和容器技术继续消除障碍，并为具有不同架构和预算的项目提供新的机会。

## 关于作者/ Ruslan Synytsky

![](img/73d6e5264f802f706af12f252d38c397.png) Ruslan Synytsky 是 [Jelastic](https://jelastic.com/) 的首席执行官和联合创始人。他设计了多语言云平台的核心技术，该平台在全球范围内的各种数据中心运行数千个容器。Ruslan 致力于构建高度可用的集群解决方案，以及为云中的传统和微服务应用程序增强自动垂直扩展和水平扩展方法。Ruslan 积极参与面向开发者、主机提供商、集成商和企业的各种会议。在推特上关注他。