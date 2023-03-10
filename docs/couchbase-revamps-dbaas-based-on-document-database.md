# Couchbase 基于文档数据库改进 DBaaS

> 原文：<https://devops.com/couchbase-revamps-dbaas-based-on-document-database/>

Couchbase Inc .推出了一个经过改进的数据库即服务(DBaaS)平台，名为 [Couchbase 五车二](https://www.prnewswire.com/news-releases/couchbase-introduces-couchbase-capella-hosted-database-as-a-service-on-aws-making-it-faster-easier-and-more-affordable-for-developers-to-build-enterprise-applications-301403318.html)，托管在亚马逊网络服务(AWS)云上。

Couchbase 产品管理高级副总裁斯科特·安德森表示，随着应用程序开发的不断发展，越来越多的组织倾向于让数据库提供商代表他们管理这些平台。他指出，这种方法将数据库管理员(DBA)解放出来，让他们可以花更多的时间来构建和部署应用程序。

Couchbase 五车二基于 Couchbase Server 7，该服务器基于 JavaScript 对象表示法(JSON)格式，向文档数据库添加了多语句 SQL 事务功能，使其能够在几微秒内运行事务处理应用程序，而以前这些应用程序需要关系数据库来处理 SQL ACID 事务。

Couchbase Server 7 的这个版本还在无模式数据库中添加了模式和类似表的组织结构，称为“作用域和集合”，使得在事务运行时添加表成为可能。

![](img/94d2509abbc4bb40399bacd0abbbf668.png)

作为一个文档数据库，Couchbase 获得了广泛的关注，这主要是因为开发人员选择使用一个他们可以下载并部署的数据库来构建应用程序，而不是要求 DBA 建立一个关系数据库。然而，随着文档数据库实例数量的激增，出现了跨服务器和云服务管理它们的需求。

接下来的挑战是决定是雇用专门的管理员，还是雇用由供应商管理的 DBaaS。许多组织选择 DBaaS 方法，因为它消除了雇用全职管理员的需要。然而，一旦组织选择了 DBaaS 方法，它接下来需要将该服务集成到其 DevOps 工作流中来构建这些应用程序。

当然，对于 DBaaS 平台来说，并不缺少选择。根据 Adroit Market Research 的一份报告,到 2025 年，全球云数据库和 DBaaS 市场规模预计将达到 260 亿美元。根据信息服务集团(ISG)发布的[报告](https://www.businesswire.com/news/home/20211012005672/en/Global-Market-for-IT-and-Business-Services-Growing-at-Fastest-Pace-Ever-ISG-Index%E2%84%A2-Finds)，总体而言，第三季度服务市场达到创纪录的 134 亿美元，同比增长 55%。

尚不清楚组织最终会在多大程度上依赖于“即服务”平台，但自从新冠肺炎疫情开始以来，向这种消耗 It 资源的方法的转变已经显著增加。因此，内部 IT 团队的组织方式正在发生转变，因为较低级别的任务要么是自动化的，要么是由为供应商工作的外部 IT 团队处理的。

无论采用哪种方法，组织内创建和分析的数据量只会越来越多。组织将需要确定相对于依赖外部服务提供商来说，管理这些数据在多大程度上是合理的。当然，当依赖外部服务提供商时，挑战不仅仅是技术上的；它引入了一种新的文化动态，许多 it 团队需要一段时间才能完全理解。