# 补充技术:Amazon RDS 和 PostgreSQL

> 原文：<https://devops.com/complementary-technologies-amazon-rds-and-postgresql/>

对于那些正在寻找一种关系数据库服务来有效且持续地满足他们需求的企业来说， [Amazon RDS](https://aws.amazon.com/rds/) 可能值得一试。通过使基于云的关系数据库易于设置、操作和扩展，Amazon RDS 将企业从内部数据库管理职责的时间陷阱中解放出来，从而允许更明确地专注于产品和业务开发。在选择数据库引擎时，亚马逊 RDS 上的组织有多种选择，从亚马逊自己的 Aurora 到 MySQL、MariaDB、Oracle、Microsoft SQL Server 和 PostgreSQL。

虽然这些 Amazon RDS 数据库选项各有利弊，但我是 PostgreSQL 的粉丝，原因有很多。PostgreSQL 提供了一个功能丰富的[开源对象关系数据库引擎](https://www.postgresql.org/)，该引擎由 15 年的专门社区开发、经过验证的架构以及在可靠性和数据完整性方面的良好声誉提供支持。PostgreSQL 比 MySQL 的速度和特性集更匹配，为数据库表带来了比标准的选择、插入、更新功能。在特别强大的社区和第三方支持的推动下，PostgreSQL 定期发布稳定的更新，以增强其性能并扩展其功能——现在包括原生 JSON 存储、原生数组以及创建自定义数据类型、函数和深度可定制扩展的能力，以满足特定的应用需求。

串联使用 Amazon RDS 和 PostgreSQL 提供了协同优势，这在很大程度上归功于许多旨在提供简单性的设计特性。Amazon Web Services 包括一个一键式界面，用于在云中创建 PostgreSQL 实例。亚马逊还提供其集成在亚马逊 RDS 服务中的 [AWS 数据库迁移服务](https://www.reliam.com/migration/2017/03/27/amazon-dms-database-migration-made-easy.html) (DMS)，这使得将现有数据库迁移到 PostgreSQL 并将其作为亚马逊 RDS 实例导入变得非常容易，并且不需要停机(并且可以将迁移安排在企业认为最方便的时间)。Amazon RDS 还允许您在几分钟之内在云中上下扩展 PostgreSQL 数据库；使用 Amazon 可用性区域提供高可用性和冗余的自动复制；与亚马逊虚拟私有云等其他 AWS 服务轻松集成；并使使用自动快照设置和还原数据库备份变得简单。

## 快速扩展

Amazon RDS 和 PostgreSQL 的组合非常适合随着组织应用程序需求的增加而平稳增长，因为 Amazon RDS 平台允许您根据需要纵向和横向扩展实例。

Amazon RDS 中的垂直扩展可以通过以下方式实现:

在 RDS 仪表板中，从数据库实例的选项列表中选择“修改”:

![](img/bec625440ab3bdadc83e466062ff0f44.png)

然后，选择一个新的数据库实例类:

![](img/958bd8e475ca227d22a3d6f743c5babb.png)

该过程现已完成。Amazon RDS 中的垂直扩展就是这么简单。当使用多个可用性区域运行数据库时，垂直扩展也可以在很少或没有停机的情况下发生，因为备用数据库将首先升级，然后故障转移到这个升级的数据库。

此外，Amazon RDS 提供了一种简单的方法来提高读取性能，方法是增加水平伸缩，将读取副本用作与主数据库同步的只读副本。

从控制面板中，为实例选择“创建读取复制副本”:

![](img/469992c78f662b630c2673ff6735bd9b.png)

在下一个屏幕上，选择实例大小和数据库实例名称。还可以将读取副本部署到任何区域和可用性分区:

![](img/c740d248cad5d80ff13d60d2f0f9ee4b.png)

在短短几分钟内，将实现水平规模的扩大:

![](img/51b2fb857edb062d6d665feedf4920f5.png)

在我看来，通过联合 Amazon RDS 和 PostgreSQL，企业可以实现简单、经济、多功能的全面管理的数据库即服务解决方案的所有优势，这种解决方案可以在几分钟内完成设置，并可以扩展到成长中的组织可能需要的任何规模。

— [法布里西奥·马里亚尼](https://devops.com/author/fabricio-mariani/)