# 子树应对微服务数据管理挑战

> 原文：<https://devops.com/subtree-rises-to-microservices-data-management-challenge/>

刚刚筹集了 1000 万美元的资金，Subtree 已经从 stealth 中脱颖而出，推出了一项基于 dotmesh 开源实用程序的微服务服务，使 DevOps 团队能够捕获应用程序的整个状态。

Subtree 首席执行官卢克·马斯登(Luke Marsden)表示，Dotmesh 以一系列被称为数据点的单元形式捕获应用程序状态，并基于微服务架构捕获和跟踪任何应用程序中所有数据库、文件和其他数据的所有版本。该实用程序公开了一个命令行界面(CLI ),通过它可以收集由 dotmesh 捕获的有关应用程序的数据，并且 dotmesh 服务器组件存储所有的数据点。

Marsden 说，dotmesh 实用程序可以应用于任何微服务，不管使用什么运行时或容器类别。

一旦捕获，这些信息就可以通过 dothub 存储库共享，由 Subtree 作为服务来管理。马斯登说，不需要使用 dothub 作为存储库，因为 dotmesh 实用程序是开源代码。但马斯登说，dothub 旨在成为共享分布在整个企业的微服务应用程序状态数据的最有效方式。

他说，目标是提供相当于 Github 提供的源代码服务，专门用于共享生产环境中部署的微服务应用程序的状态信息。

* * *

**相关内容:**

[Red Hat 调查发现微服务被广泛采用](https://devops.com/red-hat-survey-sees-broad-adoption-of-microservices/)

[Flexera 扩展了开源扫描工具的范围](https://devops.com/flexera-extends-scope-of-open-source-scanning-tools/)

* * *

马斯登说，实际上，dotmesh 和 dothub 的结合创造了一种用于跟踪和管理数据的新型服务网络。

他指出，微服务带来了巨大的数据管理挑战，因为最佳实践要求每个微服务都能够访问自己的数据库。马斯登说，管理由绑定到大量数据库的微服务组成的应用程序，很难确定建立在多个微服务之上的应用程序的状态。例如，如果一个微服务出现故障，DevOps 团队通常不得不停止应用程序，因为它们之间存在所有的依赖关系。然而，dotmesh 实用程序通过应用编程接口(API)绑定到 dothub 服务，使得确定所有这些微服务及其数据源之间的关系变得更容易，他说。

Subtree 设想 DevOps 团队同时使用 dotmesh 和 dothub 来创建工作流，专门解决微服务环境中的数据管理问题。根据 IT 组织试图管理的微服务数量的不同，他们目前面临的数据管理挑战的程度也不同。然而，在某种程度上，几乎每个采用微服务的 IT 组织都需要解决如何管理连接到每个微服务的数据，尤其是在更大的有状态应用程序的环境中。

缺乏专为微服务设计的数据管理的影响已经显现。许多组织不能有效地测试基于微服务的应用，因为测试不能准确地反映应用的真实规模和范围。

dothub 服务的定价是每月 10 美元，存储容量为 5GB。还有一个免费存储层，可提供高达 1GB 的存储空间。

现在还不太清楚 It 组织内部的谁将管理由不可避免地将成为数以千计的微服务访问的数据。但很明显，目前管理所有这些数据的工具在很大程度上是不存在的。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)