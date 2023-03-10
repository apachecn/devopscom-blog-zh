# 问答:Sematext 关于 Docker 监控的提斯，第 1 部分

> 原文：<https://devops.com/qa-stefan-thies-sematext-group-inc-docker-monitoring-support-part-one/>

斯蒂芬·提斯是 DevOps 福音传道者。我最近和他谈到了 Docker 对 Sematext Logsene 日志记录、异常检测和警报软件以及 SPM 监控软件的使用。请继续阅读我们对话的第一部分。

**David Geer:** 从技术上讲，就本文而言，什么是日志记录？

**提斯:**日志记录是指存储运行在计算机上的程序(应用程序、服务器)的输出。通常，软件应用程序生成的日志消息存储在日志文件中。然而，运行在 [Docker](https://docker.com) 容器中的软件将其日志信息写入虚拟终端(控制台)。Docker 守护进程(管理容器的服务器进程)有几个工具可以通过日志驱动程序或 Docker API 将日志消息转发给负责存储日志消息的外部应用程序。这不是处理日志数据的传统方式。这改变了日志收集和存储机制，并迫使许多组织通过引入新工具来改变其日志管理工作流。

通常，您会使用一个名为 syslog 的服务来接收日志消息并将其存储在服务器上，但是这需要对所有 Docker 容器进行特殊配置。虽然 Docker 使部署应用程序变得更加容易，但新技术使日志记录和监控变得更加困难，因为除了与 Docker 集成之外，您无法使用传统工具。

这正是 Sematext 等公司提供附加值的地方，它们通过实现:

*   融入 Docker 生态系统
*   日志文件的云存储
*   针对日志数据的全文搜索、分析、可视化和警报的索引

从技术上讲，语义日志对日志记录有什么贡献？

**提斯:**日志日志管理包括处理日志数据所需的所有工作流程和安全程序。Logsene 为访问日志数据提供基于角色的访问控制。日志被收集并发送到 Logsene 服务器(运行在云中或本地),在那里数据被存储和分析。

其他重要特性包括:

全文搜索
分析
警报
异常检测

对于那些寻求捕获日志以监控其 Dockerized 分布式应用程序的解决方案的用户和组织来说，Logsene/Sematext 以什么方式可用？

**提斯:** Logsene 在本地可用，在云中作为 SaaS 使用。它也适用于混合环境，例如在裸机上运行内部的 Dockerized 应用程序，同时将日志运送到 Logsene SaaS。在这种情况下，只有 Docker 的 Sematext 代理在本地运行。

Sematext Docker 代理自动检测正在运行的 Docker 容器，并自动从容器中收集日志。Sematext Docker 代理可以将非结构化日志消息转换为结构化数据进行分析。我们使用集成的解析器和模式库来实现这一点，模式库检测日志格式来构造日志。Sematext Docker 代理的最终任务是将所有容器中的结构化日志安全地发送到 Logsene，在那里进行全文搜索和分析查询的索引。Logsene 用户界面提供了用于搜索、可视化、异常检测和日志数据警报的所有工具。

**Geer:**Docker 的 SPM 是什么？起到什么作用？

**提斯:**logs ene 和 SPM 都通过 Sematext Docker 代理收集数据。SPM 是许多服务器应用程序的性能监控、异常检测和警报解决方案，如 Web 服务器(如 [Apache](https://www.apache.org) 、 [Nginx](https://www.nginx.org) )、数据库(如 [Cassandra](https://cassandra.apache.org) 、 [MongoDB](https://www.mongodb.org) 、 [HBase](https://hbase.apache.org) 、 [MySQL](https://www.mysql.com) 等)。)、大数据引擎(如 [Spark](https://spark.apache.org/) 、 [Storm](https://www.storm.incubator.apache.org) 、 [Hadoop](https://hadoop.apache.org) 等。)和全文搜索引擎(如 [Elasticsearch](https://www.elastic.co/) 、 [Solr](https://lucene.apache.org/solr) )。Docker 的 Sematext 代理不仅收集容器日志，还同时收集所有容器的性能指标，以及 Docker 事件。

面向 Docker 的 SPM 提供了对 Docker 平台上应用性能的运营洞察。它不仅限于性能监控—它与 Logsene 集成，在单个用户界面中进行日志管理。DevOps 团队可以找到与潜在性能瓶颈相关的日志消息。大多数组织使用不同的工具进行性能监控和日志记录。Sematext 已经认识到，指标和日志必须在单个平台中可用，以提供详细的运营见解，而不必在不同工具之间切换，并且没有多种工具集成、多用户界面、管理多种工具访问权限的登录以及来自多个供应商(如 [NewRelic](https://www.newrelic.com) 或 [Splunk](http://www.splunk.com) )的计费或许可等开销。

观看我与 Sematext 的斯特凡·提斯对话的第二部分。