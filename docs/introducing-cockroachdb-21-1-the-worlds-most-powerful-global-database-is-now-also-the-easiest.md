# CockroachDB 21.1 简介:世界上最强大的全球数据库现在也是最简单的

> 原文：<https://devops.com/introducing-cockroachdb-21-1-the-worlds-most-powerful-global-database-is-now-also-the-easiest/>

*领先的云原生 SQL 数据库让管理世界任何地方的数据变得简单，只需一条 SQL 命令*

**纽约州，2021 年 5 月 18 日 —** 蟑螂实验室今天宣布发布 CockroachDB 21.1，这是业界领先的分布式 SQL 数据库的实质性飞跃。CockroachDB 已经被誉为世界上最强大的全球数据库，随着这个最新版本的发布，它现在也是最容易的。CockroachDB 21.1 使将数据绑定到单个数据库中世界上任何地方的特定位置变得非常简单，从而确保了法规遵从性、减少了延迟并提高了容错能力。CockroachDB 21.1 使任何开发人员——无论他们的专业知识如何——都能从小规模起步，快速扩展，并毫不费力地走向全球。

今天的用户要求无论他们在地球上的什么地方，都能获得始终在线、近乎即时的体验，跨多个地区部署数据库可以满足这些要求。然而，这在历史上成本极高，或者说是一场运营噩梦。凭借其独特的架构和内置的管理数据位置的能力，CockroachDB 消除了在世界任何地方分发数据的大部分挑战。

将数据绑定到一个位置的能力是数百个 CockroachDB 客户使用的功能，现在使用该功能已经减少到几个简单的 SQL 语句。这种新方法使得任何会写 SQL 的开发人员都可以在几秒钟内访问地理定位数据。现在，在全球范围内部署数据也不需要预先考虑——即使您从单个区域开始，您也可以随时将 CockroachDB 节点添加到另一个位置(在云中立即可用)并激活这些功能，而无需停机、模式更改或任何类型的手动分片。现在，您可以通过一条 SQL 语句向世界上的任何人提供快速可靠的用户体验。

“我们的使命一直是让任何开发者都能轻松构建真正突破性的应用。蟑螂实验室的首席执行官兼联合创始人斯潘塞·金博尔说:“太多的开发团队开始于一个仅仅‘足够好’的平台，然后要么在业务增长时受到束缚，要么不得不承受迁移的痛苦。”。“您的抱负不应受到基础设施的限制。有了 CockroachDB 21.1，任何人都可以在一个数据库上从头开始构建他们的应用程序，从一个云区域到一个全球足迹，从车库中的三个人到数百万美元的企业。”

CockroachDB 通过以下方式大幅降低运营复杂性，并轻松提供快速、可靠的客户体验:

*   通过将数据放置在离最终用户很近的地方，
*   通过冗余消除停机，能够在整个区域或云故障中幸存下来，
*   通过在本地边界内存储数据来支持数据隐私合规性，
*   以及交付多云/混合云部署，以消除“一体化”单一云方法的风险和成本

从财富 500 强公司到五人创业公司， [全球各行各业的](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=362673626&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fcustomers%2F&a=companies+across+the+globe) 公司都在使用 CockroachDB 来转变他们的业务。例如，DoorDash 正在使用 CockroachDB 来处理特定区域内的大型活动高峰，同时保持一致的事务。SpaceX 使用 CockroachDB 来管理和存储世界上最大的卫星星座的运行数据。其他客户包括康卡斯特、易贝、南诺福克、LaunchDarkly、Lush、Tokopedia 和神话游戏。

CockroachDB 21.1 中的其他更新使开发人员能够:

*   通过添加一种新的索引类型，存储跨多个云区域的 JSON 和空间数据，分区 [倒排索引](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=2772127062&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv21.1%2Finverted-indexes&a=inverted+indexes)
*   利用 [解释](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=797864199&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv21.1%2Fexplain.html&a=EXPLAIN) 、 [解释分析](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=338982637&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv21.1%2Fexplain-analyze&a=EXPLAIN+ANALYZE) 中的更多详细信息，以及 CockroachDB 本机 [监视 UI](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=943304915&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv20.2%2Fui-overview.html&a=monitoring+UI) 中的更多语句和事务详细信息，包括争用信息，简化 SQL 查询的优化和故障排除
*   [使用更多第三方工具处理日志](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=3067350902&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv20.2%2Fdebug-and-error-logs.html&a=Process+logs) ，提供多种更新，包括更多日志格式化选项
*   将数据从群集传输到更多工具，并为 [【本地变更数据捕获(CDC)](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=700550248&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv21.1%2Fcreate-changefeed&a=native+Change+Data+Capture+(CDC)) 功能提供了一种新的加密类型
*   改进了之前使用 Postgres 的应用程序的测试和 [迁移，并改进了导入功能以忽略不支持的语句](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=2858783935&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv21.1%2Fmigrate-from-postgres&a=migration+of+applications+that+previously+used+Postgres)
*   与开发者工具[active record](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=694997539&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv21.1%2Fbuild-a-ruby-app-with-cockroachdb-activerecord&a=ActiveRecord)[Hibernate](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=3084317756&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv21.1%2Fbuild-a-java-app-with-cockroachdb-hibernate&a=Hibernate)[liqui base](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=395844731&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv21.1%2Fliquibase.html&a=Liquibase)和 [Datagrip](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=2670145117&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fdocs%2Fv21.1%2Fthird-party-database-tools.html%23integrated-development-environments-ides&a=Datagrip) 无缝集成，并更新了 CockroachDB 与这些工具的兼容性

运行 CockroachDB 最简单的方法是使用 CockroachCloud，它是我们的数据库即服务，可在全球多个云提供商处即时获得。今天 [这里](https://c212.net/c/link/?t=0&l=en&o=3166797-1&h=2770286855&u=https%3A%2F%2Fwww.cockroachlabs.com%2Fget-started-cockroachdb%2F&a=here) 免费上手。

**关于蟑螂实验室
帮助各种规模的公司及其开发的应用快速扩展，在任何情况下都能生存下来，并在任何地方蓬勃发展。CockroachDB 在全球各行各业的一些大型企业中广泛使用，包括 Equifax、Bose、Comcast 以及银行、零售和媒体领域的一些大型公司。蟑螂实验室总部位于纽约市，背后有 Altimeter、Benchmark、Greenoaks、GV、Firstmark、Index Ventures、 Lone Pine 、Redpoint Ventures、红杉资本、Tiger Global 和 Workbench 的支持。欲了解更多信息，请访问 cockroachlabs.com**