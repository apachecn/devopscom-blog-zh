# DevOps 如何培育物联网棕色地带以取得成果

> 原文：<https://devops.com/how-devops-can-nurture-the-iot-brownfield-for-results/>

您最新的物联网项目顺利通过了概念验证，但在推广过程中开始遇到问题。幸运的是，你的 DevOps 超人让事情运转起来。现在，也许一年或更久以后，随着项目的发展，你会看到越来越多的问题出现。如果这种情况听起来有点熟悉，或者你担心你可能会去那里，你并不孤单。欢迎来到物联网棕色地带。

“不，不可能。在概念验证期间，我们选择并评估了全新的硬件和软件。这从一开始就是一个全新的项目。”小心这个陷阱。许多物联网项目确实是从绿地项目开始的，没有集成遗留硬件和软件的限制。您的团队在 IT 和业务线人员的协作下开发了需求。您引入了这些新工具，并在小范围内取得了成效。根据思科 2017 年对 1，845 名 IT 和业务线决策者的物联网调查，60%的物联网项目停滞在概念验证阶段，因此您处于领先地位。

或者看起来是这样。现在是不断升级的承诺。管理层认为，如果它在小范围内有效，那么当它在整个企业范围内推广时就应该有效。数据和洞察力将源源不断地涌入，每个人都可以实时看到任何地方发生的事情。他们给首次展示开了一张大支票，然后你就走了。

## 麻烦的第一个迹象

在第一次展示项目评审时，人们开始对“完全成功”的定义吹毛求疵你推广了 X 个地点，其中 Y 个在工作，X-Y 个处于不同的分流状态。这怎么可能呢？您采用了“相同”的配置并对其进行了扩展。随着团队对非工作人口的调查，你会发现一些不一样的小事情，需要到处调整。

抛开琐碎的、过度的规模和时间，物联网绿地项目是不存在的。每一个生命周期延长的物联网项目都变成了棕色地带，新旧硬件和软件混杂在一起。对于大多数物联网应用来说，严格控制配置(国防或医疗应用)是极其昂贵且不必要的。两年后、五年后、十年后，你的供应商不会卖给你完全相同的硬件或软件。除非你向他们支付终身购买电子元件或冻结开源代码发布的费用。

理想情况下，我们应该将 DevOps 团队派往物联网项目。有了一个获取数据的大型工具堆栈，随着形势的发展，业务线类型可以想出更多的事情来做。重点是获得洞察力，并为优化结果进行调整。循环学习和安全增强是游戏的一部分。

## **应对物联网棕色地带**

这里有一个悖论:你的物联网应用存活的时间越长，这种情况就变得越复杂。如何应用物联网棕地思维来提高自己的成功几率？技术要求各不相同，但一些核心哲学原则会有所帮助。

***卷着变化*。**您的团队已经能够熟练地快速发布应用软件。更加积极地应对固件和网络级别的持续变化。整合空中下载(OTA)技术，用于更新任何无线设备上的代码。随着物联网规范的不断发展，部署能够处理修订后的协议栈(或全新协议栈)的多协议网关。无情地更新安全漏洞。

***抽象一切。*** 你会读到很多关于物联网互操作性的文章，人们通常指的是协议的有线级互操作性。这些多协议网关只有一个任务——将实时数据传输到 IP 网络和云中。让我夜不能寐的是数据级的互操作性。使用 edge 或 fog 计算对数据流进行预处理，这样云就不会被困在整理同一类数据的各种格式中。使用 JSON 或其他轻量级技术抽象您的数据，以便如果下一代传感器以稍微不同的格式输出数据，可以在接近源的地方修改预处理。考虑发布-订阅协议，以便在节点之间更容易地进行路由。

***优化云端。*** 鳞能在云梯队中狠狠咬一口。异构的分布式架构通常会胜出。在有实时数据的地方部署混合云解决方案。让公共云做它擅长的事情:演示、商业智能和归档。在用于繁重分析的私有云实例中，使用 Apache Spark 等框架来最大限度地减少数据移动，为关键算法添加更快的节点。尝试为每个数据流分配一个小型处理内核，以实现可预测的截止日期，或者在工作流优化节点中使用 FPGAs 来提升计算性能。

## **毕竟只是生意**

最终，评估物联网应用的完全成功将取决于编写大规模部署检查的业务线决策者。DevOps 模式是随着时间的推移培育物联网棕色地带的理想模式，其特点是技术专家和业务线类型之间持续的强大协作。在项目早期，接触一些外部物联网专业知识，直到你有几个学习周期。

正如思科 2017 年物联网调查提到的那样，61%的从业者认为我们对企业的物联网转型只是皮毛。避免绿地陷阱并结合这些物联网棕色地带应对策略，从长远来看，将为您提供最佳的成功机会。

— [唐·迪丹吉](https://devops.com/author/don-dingee/)