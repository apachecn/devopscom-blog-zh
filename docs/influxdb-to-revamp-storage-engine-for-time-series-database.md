# InfluxDB 改造时序数据库的存储引擎

> 原文：<https://devops.com/influxdb-to-revamp-storage-engine-for-time-series-database/>

InfluxData 已经启动了一个开源项目 influx db IOx T1，该项目将成为该公司下一代 T2 时序数据库 T3 的基础。

同时，该公司已经使 [InfluxDB 开源 2.0](https://www.influxdata.com/blog/influxdata-advances-possibilities-of-time-series-data-with-general-availability-of-influxdb-2-0/) 普遍可用。该公司数据库的这一版本以单一二进制的形式出现，这使得它更容易保护。

InfluxDB 开源 2.0 还提供了对数据浏览器可视化工具的访问，以及专门为时间序列数据构建的轻量级 Flux 查询语言。

![](img/b2e62ae83f76708a273599c49a95e52b.png)

InfluxData 首席技术官保罗·迪克斯(Paul Dix)表示，虽然现有的数据库产品仍在不断改进，但现在是时候开始通过一个围绕存储引擎的新项目来解决一些问题了，该项目将使跨数千台服务器查询数千兆字节的数据成为可能。他说，InfluxDB IOx 项目将通过消除当前平台固有的基数、数据大小和集群大小的限制来解决这个问题。

InfluxDB IOx 项目是用 Rust 编程语言编写的，并结合了 Apache Arrow，这是一个开源的内存分析引擎，它结合了在 Apache Software Foundation (ASF)的支持下正在发展的柱状数据存储。这种方法还将使 InfluxDB 能够原生支持 SQL 以及 InfluxQL 和 Flux 查询语言。

目前的计划是在未来的点版本中使 InfluxDB IOx 成为可选的存储后端。到明年下半年，InfluxData 计划 InfluxDB Enterprise 客户将拥有一个商业支持版本的 InfluxDB IOx 和 InfluxDB Enterprise。InfluxDB IOx 将有自己的构建，可以单独运行。Dix 指出，实际上，InfluxDB IOx 将使分离计算和存储需求变得更加容易。

Dix 表示，虽然 InfluxDB 已经成为支持各种监控工具实时收集数据的基础，但影响可连接的表数量的当前基数限制需要一种新的方法来添加对分布式跟踪功能的支持，以观察基于微服务的应用程序。他指出，IOx 版本还将采用对象存储平台来降低总拥有成本，同时使解决分布式计算环境的需求成为可能，现在分布式计算环境包括各种边缘计算平台。

他补充说，采用 Apache Arrow 的决定也为喜欢使用 SQL 和其他脚本语言的最终用户打开了平台。

利用 InfluxDB IOx 的可观察性工具进入 DevOps 工具可能还需要一段时间。然而，很明显，时序数据库将会发展以满足云原生应用的需求，这些应用将基于跨越分布式计算环境的大量微服务。唯一的问题是，这些应用程序的当前部署速度可能会在多大程度上超过 InfluxDB 的当前能力。