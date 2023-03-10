# ScyllaDB 为其 NoSQL 数据库展示了“巨大的”新功能

> 原文：<https://devops.com/scylladb-unveils-monstrous-new-capabilities-for-its-nosql-database/>

*在 2021 年 Scylla 峰会上，ScyllaDB 首席执行官概述了在性能、灵活性和规模方面达到新水平* *的计划*

加利福尼亚州 PALO 阿尔托，2021 年 1 月 12 日(环球新闻网)——在 2021 年举行的 [Scylla 峰会上，ScyllaDB 揭开了新的云原生功能、更广泛的平台支持以及为期一年的项目，以缓冲其高性能 NoSQL 数据库的各个方面。](https://www.globenewswire.com/Tracker?data=kHtUz8k0I9XFPplhLEWbz_YocfWxKAAOzydAR72MfBC9Op-eG_kESS8Uid3xZEjcm-fRzoqcSayMtPzb7mlO3PvT_BMLtGKetYFltKal240q6F_utV8q14YCYeQgkFPM)

在上一次峰会上，ScyllaDB [宣布](https://www.globenewswire.com/Tracker?data=Xd47Rrcq_PGckeSbaXJ8gF4-i4AMgyy-hGsNdOsOPqt5w7Igp9ClOw14rNym4NLElmiriuUNd8LIYHbSaxI1a0UlZsYCGuCgQA5ROR_0vovCvCwRn8MMPViBLezEciYHaRpzsrNRnDBfH5DXrWJP1YGkRl4OoQ9j5lzs17yEAXgro3JyZrN_5lKYwh8DYgir_rCF9Ent75oIDZd4cb2-0Q==)已经与 Apache Cassandra 的功能完全匹配。它还推出了交流发电机 API，为亚马逊 DynamoDB 用户提供了一个开源替代方案，具有更大的部署选择、更好的性能和更低的总拥有成本。

那么，世界上最快、最具成本效益的 NoSQL 数据库下一步会是什么呢？ScyllaDB 联合创始人兼首席执行官 Dor Laor 在 Scylla Summit 2021 的开场主题演讲中提供了答案。

**介绍喀尔刻项目**

该公告以喀尔刻项目开始，这是一项为期 12 个月的计划，旨在为“锡拉”已经强大的数据库带来更大的一致性、更好的弹性和易用性。每个月，ScyllaDB 都会发布一个新的特性或升级到一个现有的功能，同时还会有许多较小的生活质量改进。

Laor 说，今年计划的重大变化是迁移到 Raft 共识协议，在两个方面带来重大改进。首先是灵活性和可管理性。所有内部元数据操作都将变成事务性的，使 Scylla 能够在一次操作中弹性地将其大小翻倍。第二个需要改进的地方是一致性。以前，NoSQL 数据库依赖最终一致性来避免性能开销。有了 Raft，Scylla 将以常规操作同样低的处理开销支持交易——这对 NoSQL 开发者来说是一个游戏规则的改变者。

喀尔刻项目下的其他开发将提高吞吐量，减少延迟，并简化大规模运行分布式数据库的操作复杂性。有关喀尔刻项目的更多详情和跟踪其里程碑，请访问 ScyllaDB 的[喀尔刻项目](https://www.globenewswire.com/Tracker?data=BM2-PgEre40K1X9Aghmzk3p3V56jMKl2xizBtRcCxDTx1PG84V_iZtIoGZeQ12CNbyfGq5lvKWyWFH7vuAPF-uoYbiIsvYBqPo9pFxqAMz0=)页面。

“Scylla 是以 Apache Cassandra 为模型的高度分布式数据库，”Laor 说。“我们彻底改造了 Cassandra，用 C++重写了代码，并优化了其性能的方方面面。喀尔刻项目将再次改变锡拉，提供速度、可靠性和云原生功能，远远超过任何其他同类数据库。”

**GCP 上的锡拉云**

Laor 还宣布，Scylla 的托管解决方案 Scylla Cloud 于去年在 AWS 上推出，现在运行在谷歌云平台上(目前处于测试阶段)。这是 Scylla Cloud 一系列声明中的最新一个，最近[选择](https://www.globenewswire.com/Tracker?data=M7QtjcCVy-nS392UCirR2ApjXSEU65oZWKsn3M44BUKn131oksOSbhDiR3TC0WBVYDwhUTA9wgfagD1N-aIGBeFWyUs8-HGRu4k-fZLWrLQCs2BqEWEQ7Xcf1e8KUR3zixNCaRjsUj6MZkz3d892eAMn4klaOwyoR2DbtmtVaZM=)作为唯一一个在 AWS Outposts 平台上认证的 NoSQL 数据库，用于内部托管服务。

【Kubernetes 的 Scylla 运营商现已推出

Laor 接下来宣布了 Scylla Operator T1 的正式发布，这是一个 Kubernetes 扩展，使得在云原生环境中运行 Scylla 集群变得容易。Scylla Operator 支持 Kubernetes 的广泛采用，使用户能够用一个命令创建多个 Scylla 集群，跨多个可用性区域自动部署，扩展操作，进行滚动更改、修复和升级，从自动修复中受益，并执行备份、恢复等。

有关 GCP 支持的详细信息以及将应用程序集成和连接到 ScyllaDB 的 AWS 和 GCP 托管解决方案的提示，请务必参加 Scylla Cloud 上的 Scylla Summit [会议](https://www.globenewswire.com/Tracker?data=e030VdaEbD8AWZ_MGZzpkS3IXO1SwMb5efzjS-GVO90QJiGOe-bgg-w4VN7n0iv1fSOfMYSo0e35AL-Mk_uDQV2K4glA62RILVF0rqKv2dc9nHvIloUrNUN1RgtTj7JInyLysJT4AHVG8MAvvLl0HA==)。要深入了解 Scylla 的 Kubernetes 操作员，请不要错过[会议](https://www.globenewswire.com/Tracker?data=e030VdaEbD8AWZ_MGZzpkT1E3RNXdEFvFkNs0JEriYUtX-wCVTzSCvngR41iY-EL1SEGTkXiCIq5QTjZrwxNVIWmAlPy-6bXdddJU-c2LqH8_fT0R1kKI27fdbRvk-1vVtcEd0RRqCuaV6iSgUCVSw==)，其中涵盖了横向扩展、滚动升级、自动配置更改等等。

要查看 2021 年 Scylla 峰会的完整议程并注册参加现场活动或为期半天的免费讲师指导培训，请访问 2021 年 Scylla 峰会网站[此处](https://www.globenewswire.com/Tracker?data=oMPw4x_hVVLx6QVoA3eiIgEFAFotiMaa0lbS9CMYl4vKYGCW2_I-MotJJkM7rnMH-nvyMDpIBjrnuXoqzDqZPwl5_c1SVI7JvhetrK31kqc=)。

**关于 ScyllaDB**
[Scylla](https://www.globenewswire.com/Tracker?data=kHtUz8k0I9XFPplhLEWbz1QO1lShnBxKzAkM7wCKjNTsjtU7jLjjX-I-4xxx84_AlHbGHnH4mMB_x1KBoCF4EA==) 是实时大数据数据库。API 兼容 Apache Cassandra 和 Amazon DynamoDB，Scylla 采用无共享方法，将吞吐量和存储容量提高了 10 倍。Comcast、Discord、Grab、Hotstar、Medium、Starbucks、Ola Cabs、Samsung、IBM、Investing.com 和[更多领先公司](https://www.globenewswire.com/Tracker?data=jpZ3VT-Pe-e5ooubLTMBWYZ6N3Ozr1NEgE13L-mZqQXn4tpd-Dc9AiF5cmCEVssd-M5f-3MbriyFVhOA7JM2ucUCTrAhJjIkedqjksLTzQZecj5X6fdOmoK_PaP2XCUg)采用 Scylla 实现了数量级的性能提升并降低了硬件成本。ScyllaDB 由负责 KVM 虚拟机管理程序的团队创建，并得到 Bessemer Venture Partners、Eight Roads Ventures、Innovation destinations、Wing Venture Capital、Qualcomm Ventures、TLV Partners、Magma Venture Partners、Western Digital Capital 和 Samsung Ventures 等公司的支持。更多信息:[ScyllaDB.com](https://www.globenewswire.com/Tracker?data=kHtUz8k0I9XFPplhLEWbz4O20PDKV_VUd-jBrStsItMaCG0YG5BcOXmqhFlNLKCSpYGBo_IrmqdWmoUFApAjfQ==)。