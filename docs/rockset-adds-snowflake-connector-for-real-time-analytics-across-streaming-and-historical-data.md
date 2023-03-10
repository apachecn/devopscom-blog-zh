# Rockset 增加了雪花连接器，用于跨流和历史数据进行实时分析

> 原文：<https://devops.com/rockset-adds-snowflake-connector-for-real-time-analytics-across-streaming-and-historical-data/>

*新的集成为开发人员提供了跨实时和历史数据的高效亚秒级搜索、聚合和连接。*

**加利福尼亚州圣马特奥，2022 年 6 月 15 日—** [专为云构建的实时分析平台 Rockset](https://rockset.com/) 今天宣布推出一款新的雪花连接器，可对来自 Apache Kafka、Amazon DynamoDB 或 MongoDB 等来源的流数据以及来自雪花的历史数据进行低延迟、高并发性分析。

像雪花这样的数据仓库被分析师和数据科学家用来存储和分析历史业务数据，通常是 Pb 级的，数据以不频繁的批次加载以节省成本。相比之下，开发人员使用 Rockset 等实时分析平台将来自雪花的历史数据与来自 Apache Kafka 等来源的实时事件流相结合，并为面向用户的应用程序和运营分析用例提供服务。

Rockset 在一个[聚合索引](https://rockset.com/blog/converged-indexing-the-secret-sauce-behind-rocksets-fast-queries/)中高效地组织数据，该索引针对实时数据接收和低延迟分析查询进行了优化。Rockset 的摄取汇总使开发人员能够使用 SQL 预聚合实时数据，而无需复杂的实时数据管道。因此，客户可以将存储和查询实时数据的成本减少到原来的 1/10 到 1/100。此外，Rockset 专为云构建，可独立扩展计算和存储，从而最大限度地提高资源效率，而不会产生任何运营开销。

Rockset 首席执行官兼联合创始人 Venkat Venkataramani 表示:“世界正从静态仪表盘转向实时、交互式的面向用户的分析，如客户推荐、物流跟踪和风险分析，这些都需要高效的性能。“Rockset 与 Snowflake 的集成使用户能够搜索、聚合和连接历史数据与实时事件流，以支持亚秒级查询。另一种常见的使用模式是在雪花中的历史数据上建立和训练您的机器学习模型，并在模型服务期间使用 Rockset 提供实时功能和信号。”

此版本使使用雪花的组织能够:

*   搜索、聚合和连接来自雪花和实时事件流的历史数据或来自 Apache Kafka、Amazon Kinesis、Amazon DynamoDB、MongoDB、PostgreSQL、MySQL、Oracle、SQL Server 等的更改数据捕获流。

*   使用 Rockset 的聚合索引以更低的成本实现更好的性能，实现低延迟、高并发性查询，以对来自雪花的历史数据进行面向用户的分析。

*   将 Rockset 用于实时模型，作为雪花的机器学习管道的一部分。

Rockset 拥有丰富的数据连接器库，可从现有事件流、数据库和湖泊中进行无模式摄取，并与数据源保持同步，从而在生成新数据的 1-2 秒内实现快速分析。Rockset 由支持脸书新闻订阅和搜索的在线数据基础设施背后的团队构建，其灵感来自支持云级实时分析的相同索引系统。

要了解更多有关 Rockset 最新集成的信息，请访问 Rockset 在拉斯维加斯雪花峰会上的 1113a 号展位，查看 [Rockset 的雪花文档](https://rockset.com/docs/snowflake/)，或安排在 https://rockset.com/[进行演示](https://rockset.com/)。

**支持资源**

*   [Rockset 网站](https://rockset.com/)

*   [Rockset 博客](https://rockset.com/blog/)

*   [Rockset 最新消息](https://rockset.com/company/)

*   [在 Twitter 上关注我们](https://twitter.com/rocksetcloud)

*   [在 LinkedIn 上加入我们](https://www.linkedin.com/company/rocksetcloud/)

**关于 Rockset**

Rockset 是专为云构建的实时分析平台，能够以惊人的效率对实时数据进行快速分析。以亚秒级响应搜索、连接和聚合任何大规模数据。利用 Rockset 的云原生聚合索引和内置连接器高效扩展。无论数据的形状如何，只需几周而不是几个月就能构建数据应用程序。欲了解更多信息，请访问[rockset.com](https://rockset.com/)。