# Hazelcast 展示了云效率，每秒 10 亿个事件的实时流处理

> 原文：<https://devops.com/hazelcast-demonstrates-cloud-efficiency-real-time-stream-processing-of-one-billion-events-per-second/>

使用 45 个节点实现基准测试，从流数据中获得非凡的总拥有成本和业务洞察力

加利福尼亚州圣马特奥2021 年 3 月 17 日/美通社/ — [快速云应用平台 Hazelcast](https://c212.net/c/link/?t=0&l=en&o=3097925-1&h=2794280622&u=https%3A%2F%2Fhazelcast.com%2F&a=Hazelcast) 今天宣布，它在公共云部署中的 720 个虚拟 CPU(vcpu)上成功实现了每秒 10 亿个事件的流处理性能里程碑，延迟为 26 毫秒。Hazelcast 内存计算平台提供与内存存储集成的高速、云原生、分布式有状态流处理功能，以支持具有最高吞吐量和最低延迟要求的软件应用。除了其性能之外，Hazelcast 还设计为以最高效率运行，以最小化硬件占用空间，提供同类最佳的总拥有成本。

如今，除了在任何数据驱动的组织中常见的大型数据集上进行传统的批量计算之外，高性能软件系统也是必不可少的。这些系统还提供了交易处理和流分析方面的扩展空间，以便在经济高效的部署中以更少的时间完成更多的工作。这些信息让企业有更多的自由去试验和发现竞争优势的新机会。

该基准测试中展示的性能水平对于改进机器学习(ML)训练以及增强人工智能(AI)驱动的应用程序的决策制定尤其有价值，例如欺诈检测和其他需要自动、实时决策的用例。在追求更高精度的过程中，这种算法变得更加复杂，资源更加密集，因此经济高效的处理能力对于实现持续发展和改进，同时控制支出至关重要。

“我多年来一直在研究流处理系统和开源开发，看到这些基准测试结果给我留下了深刻的印象，”荷兰代尔夫特理工大学助理教授 Asterios Katsifodimos 说。“直到现在，在基于 JVM 的流处理世界中，每秒 10 亿个事件需要痛苦的参数化、数千个 CPU 内核，并且仍然只能以几秒钟的延迟运行。尽管大多数实际部署所需的吞吐量远低于每秒 10 亿次事件，但该基准测试表明，Hazelcast Jet 可以以毫秒级延迟处理大量数据流，而只需对云节点进行很少的投资，因此可以将大量预算用于高可用性部署。”

基准测试工作始于对 c 5.4x 大型 Amazon Web Services 实例的小型集群的测试，每个集群提供 16 个 vCPUs，使用每秒一百万个事件的数据流来确定第 99.99 ^个百分点的延迟，这是一种比第 99 ^个个百分点的报告更为严格的测量方法。该测试对 20 毫秒的更新使用了快速时间分辨率，这比 NEXMark 定义中指定的 1 分钟窗口产生了更密集的工作负载。来自模拟在线拍卖的 NEXMark 基准测试套件的查询在 5、10、15 和 20 个节点的集群规模上运行，以获得指定百分比的基准延迟。在 20 个节点的集群中，NEXMark 基准测试的查询 5 是最复杂的，它询问“在最近一段时间内，哪些拍卖获得了最高的价格”，99.99 ^(th) 百分点的延迟为 16 毫秒。

然后，该基准侧重于寻找 Hazelcast 在相同的低延迟下可以提供的最大吞吐量，因为它可以从一个节点扩展到每秒查询 10 亿个事件所需的数量。更新时间分辨率放宽到 500 毫秒，仍然比 NEXMark 基准测试定义的时间窗口快两个数量级。延迟百分比也放宽到标准的 99 ^(th) 百分比，以保持基准运行可管理的短。

Query 5 首先在单个节点上运行，达到了令人印象深刻的每秒 2500 万个事件。针对不断增加的集群规模重复测试，Hazelcast 展示了吞吐量近乎线性的增长，并展示了实现每秒 10 亿个事件目标的最少实例数为 45 个节点，同时仍然实现了 26 毫秒的第 99 个百分位数的延迟。

Hazelcast 的首席技术官 John DesJardins 表示:“虽然每秒 10 亿次事件在今天看来似乎有些过分，但随着更多应用程序迁移到云并最终迁移到边缘，数据正处于下一次爆炸的风口浪尖，5G 的推出加速了这一趋势。”。“通过将 Hazelcast 平台与我们的合作伙伴(包括 IBM 和英特尔)的协作努力相结合，客户可以更轻松地知道他们的应用程序可以实时处理和计算大量数据，同时控制硬件成本。”

有关基准测试及其结果的更多详细信息，请访问 Hazelcast 博客，“ [每秒十亿次事件，毫秒级延迟:千兆级的流分析”。](https://c212.net/c/link/?t=0&l=en&o=3097925-1&h=1717642623&u=https%3A%2F%2Fhazelcast.com%2Fblog%2Fbillion-events-per-second-with-millisecond-latency-streaming-analytics-at-giga-scale&a=Billion+Events+Per+Second+with+Millisecond+Latency%3A+Streaming+Analytics+at+Giga-Scale.)

**附加资源**

*   [Hazelcast Jet 4.4 发布](https://c212.net/c/link/?t=0&l=en&o=3097925-1&h=2644335783&u=https%3A%2F%2Fhazelcast.com%2Fblog%2Fhazelcast-jet-4-4-is-released&a=Hazelcast+Jet+4.4+is+Released) 【博客】
*   [Hazelcast Jet 产品页面](https://c212.net/c/link/?t=0&l=en&o=3097925-1&h=3493130225&u=https%3A%2F%2Fhazelcast.com%2Fproducts%2Fjet%2F&a=Hazelcast+Jet+Product+Page) 【网页】
*   [NEXMark 基准信息](https://c212.net/c/link/?t=0&l=en&o=3097925-1&h=1607659438&u=http%3A%2F%2Fdatalab.cs.pdx.edu%2Fniagara%2FNEXMark%2F&a=NEXMark+Benchmark+Information) 【网页】

**关于 Hazelcast 公司**

Hazelcast 是全球 2000 强企业信赖的快速云应用平台，可提供超低延迟、有状态和数据密集型应用。Hazelcast 平台采用实时流和内存优先数据库技术，简化了本地、边缘或云中分布式应用的开发和部署，成为一项完全托管的服务。

Hazelcast 的总部设在加利福尼亚州圣马特奥市，在全球设有办事处。要了解更多关于 Hazelcast 的信息，请访问 https://hazelcast.com。

SOURCE Hazelcast 公司。