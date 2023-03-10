# SQL 与 NoSQL——未解决的争论和开发陷阱

> 原文：<https://devops.com/sql-vs-nosql-unsettled-debate-devops-pitfalls/>

大数据是一种相对较新的现象，它推动着行业炒作周期，是数据库业务的中流砥柱。IT 公司对利用大数据(或大小数据)带来的运营洞察力的无尽价值主张深信不疑，以至于很容易忽视它对传统数据库技术和实践的影响。

为了驯服不断膨胀的数据洪流，组织正在将 NoSQL 数据库管理系统(DBMS)引向不再重视古老的关系数据库管理系统(RDBMS)的道路，RDBMS 最初曾孕育了大数据。许多组织的目标是复制 Google 和 Amazon 在后端数据库投资中发现最佳点性能和生产力的 NoSQL 运动，以至于他们完全忽略了以下数据库最佳实践，而偏爱一个数据库管理系统而不是另一个:

*   预先设计数据库，关注永久的公司数据，而不是临时的应用程序。
*   数据库不是黑匣子。整合可重用的设计特性和功能，以免为每个新应用程序单独重新构建验证和后端逻辑。
*   将设计阶段的板载数据库管理员作为开发运维策略的一部分。
*   在编写应用程序代码之前，构建记录良好的数据模型。
*   设计适当的数据交互策略。
*   从多个角度建模，因为一个用例的最佳结构可能不适合另一个用例。
*   使用多个数据库管理系统。使用 NoSQL 数据库存储用户数据和会话数据，或者使用 SQL 数据库来聚合非结构化数据并关联不同的数据类型。
*   [为所有类型的应用构建最佳后端](https://devops.com/blogs/like-backend/)。

这些最佳实践鼓励使用 NoSQL DBMS 来实现高可伸缩性，绕过数据存储容量的限制，降低运营支出，集成缓存并限制数据库模式变化时的应用程序中断。然而，企业不能忽视传统 RDBMS 在处理、存储和保护敏感业务信息方面的重要性，以便在枯燥的后台事务应用程序中安全、可靠和高效地使用。

IT 部门可以利用大量的解决方案来缩小 SQL 和 NoSQL 之间的差距，例如 [Splice Machine](http://www.splicemachine.com/) ，而不是考虑 RDBMS 和 DBMS 之间没有结果的争论。诸如 [MongoDB](https://www.mongodb.org/) 之类的工具支持 NoSQL DBMS 的高性能、可用性和可伸缩性，而 [RedGate](https://www.red-gate.com/) 和 [Datical](http://www.datical.com/) 支持安全高效地执行数据库更改，以确保 DevOps 方法的关键战略优势:持续集成、持续交付、高效开发和对后端数据库系统的快速反馈。

然而，在现代开发商店中，这不是一个或另一个。至少在近期内，对于像离散事务、用户会话和用户信息这样的事情，总是需要关系数据库。我们不再处于它只是工作的一个工具的情况，今天它是最好的工具。

这些高级数据库更易于安装和管理，减少了对复杂、资源密集型和耗时的后端数据库管理流程的担忧，如管理故障切换、优化性能和负载平衡。

**数据库自动化和开发运维差距**

即使在 DevOps 环境中，数据库交付也让位于源代码，在这种环境中，开发人员和运营人员专注于他们各自领域的敏捷性，让数据库自动化在 DevOps 团队陷入手动数据库交付的炼狱时迎头赶上。对数据库自动化的不信任是高效和持续的数据库交付的主要障碍。为了弥合这一差距，DevOps 团队必须遵循适用于开发和运营流程的后端数据库管理的自动化、协作和敏捷性原则。

对于 DevOps 而言，良好的数据库设计意味着对数据库进行更少的更改，以实现高效的测试和服务虚拟化。渐进式开发运维团队必须专注于配置管理、应用部署、监控、版本控制和测试等核心工具类别。与此同时，诸如将数据库管理视为事后想法，以及在软件开发生命周期的早期阶段没有选择正确的数据库管理系统等弊端会阻碍真正的 DevOps 运动的成功采用。