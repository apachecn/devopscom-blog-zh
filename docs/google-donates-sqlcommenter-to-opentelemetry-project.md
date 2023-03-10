# Google 向 OpenTelemetry 项目捐赠 Sqlcommenter

> 原文：<https://devops.com/google-donates-sqlcommenter-to-opentelemetry-project/>

谷歌今天宣布 [Sqlcommenter](https://github.com/google/sqlcommenter) ，一个提供访问对象关系映射(ORM)自动工具库的开源项目，将与 OpenTelemetry 合并，open telemetry 是一个用于构建代理软件以工具应用的开源项目。

谷歌的产品经理 Nimesh Bhagat 说，Sqlcommenter 旨在简化应用程序和数据库遥测之间的关联。OpenTelemetry 提供了一种收集日志、指标和跟踪的机制，该机制是在云本地计算基金会(CNCF)的支持下开发的。

Bhagat 指出，使用 OpenTelemetry 收集数据的组织将面临的挑战是，无论数据最终驻留在什么平台上，都需要工具来查询这些数据。OpenTelemetry 以前缺乏一个通用标准，通过该标准可以将应用程序标签和跟踪发送到数据库并与应用程序堆栈相关联。Google 设想 IT 团队要么使用 Sqlcommenter 来探索数据，要么通过云 SQL Insights 或第三方应用性能管理(APM)平台等平台进行访问。

今年早些时候，Google 将 Sqlcommenter 作为开源软件发布。它旨在通过提供对包含导致 SQL 语句执行的应用程序代码信息的注释的访问，使对象关系映射(ORM)能够在 SQL 语句执行前对其进行扩充。

Sqlcommenter 还允许将 OpenTelemetry 跟踪上下文信息传播到数据库，从而实现应用程序跟踪和数据库查询计划之间的关联，这最终将使确定性能问题的根本原因变得更加容易，例如，涉及基于微服务的应用程序调用数据库。Bhagat 指出，Sqlcommenter 主要是为全栈开发人员设计的，这些开发人员对如何使用 SQL 查询驻留在可观测性平台中的数据有所了解。

具体来说，Sqlcommenter 旨在通过简化将慢速查询与源代码相关联的过程来提供对后端数据库性能的更深入的了解。它目前支持 Python、Java、Node.js 和 Ruby 语言以及诸如 Django、Sqlalchemy、Hibernate、Knex、Sequelize 和 Rails 等 ORM。

![](img/e88828934fd81b47e714804470f43d69.png)

随着使用开源软件的应用程序的数量持续稳步增长，DevOps 团队可能查询的数据量也将稳步增长。云存储平台使得以可承受的成本存储这些数据变得更加容易，但下一个挑战显然是找到一种方法，从所有这些数据中挖掘出有意义的见解。毫无疑问，实现这一目标将需要从查询工具到机器学习算法的一切，这些算法能够在一定规模上识别模式，否则这是不可能的。

与此同时，DevOps 团队可以期待能够达到一定程度的可观察性，而这在以前只能以限制组织将检测的应用程序数量的成本来实现。当应用程序之间的依赖性与日俱增时，这种程度的可观察性将很快被证明是不可或缺的。