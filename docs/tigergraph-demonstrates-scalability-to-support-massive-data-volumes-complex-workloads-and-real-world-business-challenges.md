# TigerGraph 展示了支持海量数据、复杂工作负载和现实业务挑战的可扩展性

> 原文：<https://devops.com/tigergraph-demonstrates-scalability-to-support-massive-data-volumes-complex-workloads-and-real-world-business-challenges/>

*公司在新的图形数据库性能指标评测中取得“行业第一”的成绩*

**加利福尼亚州雷德伍德城，2020 年 10 月 19 日—**[tiger Graph](https://www.tigergraph.com/)，企业唯一可扩展的图形数据库，今天宣布了第一个全面的图形数据管理基准研究的结果，该研究使用了一个机器集群上近 5TB 的原始数据，性能数据证明 graph 可以实时地随真实数据扩展。该公司使用了[链接数据基准理事会社交网络基准(LDBC·SNB)](http://ldbcouncil.org/developer/snb)，这是一种公认的参考标准，用于评估具有密集分析和事务性工作负载的图形技术性能。TigerGraph 是业内第一家以此规模报告 LDBC 基准测试结果的供应商。TigerGraph 能够在一个包含近 90 亿个顶点(实体)和 600 多亿条边(关系)的图上运行深度链接 OLAP 查询，在不到一分钟的时间内返回结果。

“这项基准测试和这些结果对 TigerGraph 和整个市场都意义重大。虽然 TigerGraph 在生产中有多个客户，数据大小和实体/关系数量为 10 倍，但这是第一个公开的基准测试报告，任何人都可以下载数据、查询和执行基准测试。TigerGraph 首席执行官兼创始人徐雨博士说:“没有其他图形数据库供应商或关系数据库供应商展示了同等的分析能力或性能数字。“如果对 graph 在创纪录的时间内容纳大量数据的能力仍有不确定性，这些结果应该会消除这些疑虑。Graph 是一个引擎，它使我们能够用复杂的真实数据实时、大规模地回答高价值的业务问题。TigerGraph 在高级图形分析方面的持续工作已经得到了市场认可、创新的客户应用和持续的产品发展的验证，这些基准测试结果证实了该公司作为明显的市场领导者的地位，在其他供应商失败的地方取得了成功。”

从历史上看，从金融服务到医疗保健等多个行业的企业在努力从互联数据中释放真正价值的过程中，一直在努力应对众多与图形相关的挑战。这些挑战包括无法支持大量数据、查询性能缓慢以及现有 BI 工具缺乏灵活性。TigerGraph 通过世界上最快、最具可扩展性的图形平台解决了这些棘手问题，提供了数据量的巨大可扩展性、针对实时性能的快速深度链接分析，以及作为服务和内部交付的产品。TigerGraph 成熟的技术将数据孤岛连接起来，以进行更深入、更广泛和可操作的大规模分析。

对于这个最新的基准测试，TigerGraph 的性能是使用 LDBC SNB 测量的

分布式集群上的基准比例因子 10K 数据集(4.8TB 原始数据，8.86B 顶点，61.77B 边)。该实现使用 GSQL，一种由 TigerGraph 开发的查询语言。查询被编译并作为存储过程加载到数据库中。

我们用三种类型的查询测试了 TigerGraph 的性能:IS 工作负载(所有查询在 1 到 3 秒内得到回答)、IC 工作负载(所有查询在 3 到 9 秒内得到回答)和 BI 工作负载(大多数 OLAP 式迭代和/或深度链接图查询在 1 分钟内得到回答)。每个查询执行三次，运行时间的中间值表示为最终的等待时间。每个查询分别在 24 台机器、18 台机器和 12 台机器的集群上执行。

LDBC·SNB 基准测试是一项备受业界推崇的测试，用于确认图形平台在执行复杂的商业智能和高级分析任务时的性能。

要获得完整的报告以及如何执行/重复基准测试的详细分步说明，请访问:[https://www.tigergraph.com/benchmark/](https://www.tigergraph.com/benchmark/)

**有用链接**

*   **[图形+ AI 世界](https://www.tigergraph.com/graphaiworld/)**
*   **[TigerGraph 云](https://www.tigergraph.com/cloud/)**
*   **[TigerGraph 开发者社区](https://community.tigergraph.com/)**
*   **[TigerGraph 认证](https://www.tigergraph.com/certification/)**
*   **[TigerGraph 网站](https://www.tigergraph.com/)**
*   **[TigerGraph 博客](https://www.tigergraph.com/blog/)**
*   **[Twitter 上的 tiger graph](https://twitter.com/tigergraphdb)**
*   **[LinkedIn 上的 tiger graph](https://www.linkedin.com/company/3693966/)**

****关于 TigerGraph****

**TigerGraph 是企业唯一可扩展的图形数据库。TigerGraph 成熟的技术将数据孤岛连接起来，以进行更深入、更广泛和可操作的大规模分析。全球五大银行中有四家使用 TigerGraph 进行实时欺诈检测。超过 5000 万名患者收到护理路径建议，以帮助他们踏上健康之旅。3 亿消费者通过由 TigerGraph 支持的推荐引擎接收个性化报价。TigerGraph 优化了 10 亿人的能源基础设施，以减少停电。TigerGraph 成熟的技术支持欺诈检测、客户 360、MDM、物联网、人工智能和机器学习等应用。该公司总部位于美国加利福尼亚州红木城。在 Twitter 上通过 [@TigerGraphDB](https://twitter.com/tigergraphdb) 关注 TigerGraph，或者从【tigergraph.com/cloud】的[免费开始，或者下载 TigerGraph 企业免费许可证。](https://www.tigergraph.com/cloud/)**