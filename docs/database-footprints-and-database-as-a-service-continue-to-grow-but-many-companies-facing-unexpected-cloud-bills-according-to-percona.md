# 据 Percona 称，数据库占用空间和数据库即服务继续增长，但许多公司面临意想不到的云账单

> 原文：<https://devops.com/database-footprints-and-database-as-a-service-continue-to-grow-but-many-companies-facing-unexpected-cloud-bills-according-to-percona/>

*   *根据 2020 年的调查受访者，超过 20%的公司面临超过预算的云成本，45%的公司正在运行 DBaaS*
*   *Percona 扩展了面向开源数据库和 DBaaS 的产品和服务目录，包括支持 PostgreSQL 版本 13、PostgreSQL 托管服务的测试版发布以及 Percona 企业平台。*

**北卡罗来纳州罗利——2020 年 10 月 20 日——**[开源数据库软件和服务的领导者 Percona](https://www.percona.com/) 今天在 [Percona 在线直播](https://www.percona.com/live/conferences)大会上宣布了其 2020 年[开源数据管理软件调查](https://www.percona.com/open-source-data-management-software-survey)的结果。根据调查结果，云计算的成本被认为是许多公司面临的一个问题，22%的组织面临来自云提供商的额外计划外成本。

使用数据库即服务(DBaaS)的公司比例从上一年的 40%上升到 45%。超过一半的大型公司(56%)表示他们使用 DBaaS。与寻求降低风险的公司的趋势一致，大约一半的公司(大型公司类别中的 28%)使用了不止一种 DBaaS 服务。

Percona 的 2020 年开源数据管理软件调查还包括以下主要发现:

*   开源数据库选择的决策正在集中化
    *   41%的受访者表示，架构师现在是负责制定数据库部署决策的主要群体。
    *   下一组是开发者，占 26%。这表明，尽管许多开发人员仍然对他们组织的技术选择负责，但这已经开始基于管理支持和管理开销的需要进行整合。
*   数据库继续快速增长
    *   82%的组织发现他们的数据库空间每年增长超过 5%。
    *   对于 12%的组织，他们持有的数据量在 12 个月内翻了一番或更多。
*   对于许多组织来说，升级云实例是常事
    *   大约 28%的人需要两到三次升级，而 21%的人需要十次以上的升级，相当于每个实例的潜在成本翻倍。
    *   相反，只有 12%的组织没有对其实例进行任何更改。
*   云支出和规划喜忧参半
    *   大约 22%的人发现他们的云支出超出预期，而 60%的人发现他们的云支出大致合适。17%的受访者的云支出低于预期。
*   许多公司继续将 Kubernetes 用于应用程序部署和数据库环境
    *   47%的受访者在内部使用 Kubernetes 进行应用程序的开发和测试(高于 44%)，36%的受访者将其用于生产应用程序(高于 32%)。
    *   使用 Kubernetes 运行数据库的受访者比例今年也有所增加，36%的人将其用于开发和测试(高于 33%)，23%的人将其用于生产(高于 17%)。

*“对于许多组织来说，围绕云和数据的增长超出了他们的预期。随着时间的推移，保持对数据和成本的控制对每个人来说都至关重要——使用开源数据库是实现这一点的最佳方式之一。然而，DBaaS 在今年的结果中日益流行，这表明许多组织可能没有意识到围绕云和锁定存在的所有问题。Percona 首席执行官彼得·扎依采夫表示:“*将 Kubernetes 和开源数据库结合起来，有助于在数据方面实现控制、自由和灵活性的正确组合。

*新产品路线图和更新*

作为 Percona Live 的一部分，Percona 宣布了几项新产品和服务，扩展了其开源数据库产品的范围。Percona 使用 PostgreSQL 的最新版本(版本 13)更新了 PostgreSQL 的[发行版，通过更高效地使用索引和排序功能以及减少资源使用来提高性能。还包括一个由 Percona 编写的自定义扩展](http://percona.com/software/postgresql-distribution) [pg_stat_monitor](https://www.percona.com/blog/2020/10/14/announcing-pg_stat_monitor-tech-preview-get-better-insights-into-query-performance-in-postgresql/) 的技术预览。这个扩展收集和聚合查询性能数据，从而实现更好、更快的查询分析。它可以单独使用，但当与最新发布的[Percona Monitoring and Management 2.11 结合使用时，它的功能才能得到最好的发挥，使用户](https://www.percona.com/software/database-tools/percona-monitoring-and-management)能够轻松地分析他们的 PostgreSQL 查询。

“在 Percona，我们感谢整个社区为最新版本的 PostgreSQL 所付出的努力。我们希望继续支持该社区，因此很高兴将我们的 PostgreSQL 发行版更新到最新版本。这使我们能够帮助企业公司确保他们所需的工具、插件和扩展能够协同工作，易于部署，经过认证，并由值得信赖的供应商提供支持，”Percona 产品总监特里·施洛瑟说道。

在 Percona Live 活动上，该公司还宣布 PostgreSQL 的托管服务将于明年初推出，而 Percona Enterprise Platform Beta 将于年底前推出。

Percona 企业平台将是一个真正的开源平台，不会将用户锁定在特定的云服务或平台上。它将提供单一平台来轻松管理开源数据库基础架构，并提供自助服务体验来实现快速、一致的开源数据库部署。

*“我们期待分享 Percona 企业平台，作为我们测试计划的一部分，因为这将为我们提供宝贵的早期反馈，以塑造平台的未来方向。这个项目将采取分阶段的方法，所以我们可以专注于不同的领域，并与尽可能多的测试人员合作。“我们最初的重点将是 MySQL 和 MongoDB 技术，PostgreSQL 将在稍后的过程中加入，”*施洛瑟评论道。

*佩尔科纳在线直播*

本期[Percona 在线直播](https://www.percona.com/live/conferences)将于 10 月 20 日和 21 日播出，时长超过 28 小时。它提供了围绕开源数据库和软件开发主题的混合内容，包括 MySQL、PostgreSQL 和 MongoDB，以及其他开源数据项目，如 ClickHouse、TiDB、MariaDB 和 Kunlun。

活动期间的主题发言人包括:

*   Percona 首席执行官彼得·扎依采夫—*为什么公共数据库即服务是开源中断的主要原因*
*   EnterpriseDB 高级企业架构师 Bruce mom Jian—*数据库的民主化*
*   Francis Crick Institute 研究数据服务/数据库团队负责人 Karen Ambrose—**全球疫情的技术响应 Francis Crick Institute COVID19 联盟诊断管道**
*   *Honeycomb 的首席开发顾问 Liz Fong-Jones 和 Thoughtworks 德国公司的数据主管 Emily Gorcenski—*为您的道德原则组织起来**
*   *Percona 的 MongoDB 技术主管 Kimberly Wilkins—*MongoDB 的现状，它的开源社区，以及 Percona 的发展方向**
*   *甲骨文 MySQL 社区负责人 Frederic Descamps-*海豚的状态**

*所有内容将在活动结束后提供。如需了解完整议程和注册信息，请访问[https://www.percona.com/live/agenda](https://www.percona.com/live/agenda)*

***链接***

*   *Percona Open 年开源数据管理调查—[https://www . per ConA . com/Open-Source-Data-Management-software-Survey](https://www.percona.com/open-source-data-management-software-survey)*
*   *PostgreSQL 的 Percona 分布-[https://www.percona.com/software/postgresql-distribution](https://www.percona.com/software/postgresql-distribution)*
*   *佩尔科纳企业平台测试版-[https://www.percona.com/software/enterprise-platform](https://www.percona.com/software/enterprise-platform)*