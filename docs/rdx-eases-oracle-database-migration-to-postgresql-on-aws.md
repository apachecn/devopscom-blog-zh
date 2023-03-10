# RDX 简化了将 Oracle 数据库迁移到 AWS 上的 PostgreSQL 的过程

> 原文：<https://devops.com/rdx-eases-oracle-database-migration-to-postgresql-on-aws/>

RDX 本周推出了一套工具，旨在更容易地将运行在 Oracle 数据库上的应用程序转换为 Amazon Aurora，这是一个运行在 Amazon Web Service (AWS)云上的开源 PostgreSQL 数据库实例，与 Oracle 数据库兼容。

在华盛顿特区举行的 AWS 峰会上宣布的[clckwrk Oracle 重构服务](https://www.prnewswire.com/news-releases/rdx-announces-clckwrk-refactoring-service-that-enables-customers-to-migrate-applications-off-oracle-and-onto-amazon-aurora-300864910.html)承诺通过自动化多达 60%的数据库模式转换过程，减少与亚马逊 Aurora 平台重构应用程序相关的人工工作量。

RDX 的首席战略官 James Ball 说，除了降低成本，许多组织希望将应用程序转移到云中的开源数据库，以进一步实现他们的 DevOps 雄心。每次应用程序需要扩展时，组织都会产生额外的 Oracle 许可费用。他说，相比之下，开源数据库使 DevOps 团队能够根据需要自动扩展数据库实例。

AWS 一直在努力说服客户放弃专有数据库，转而使用在其云平台上运行的开源数据库。这种竞争压力是新联盟背后的驱动力，这在以前被认为是不可想象的。例如，甲骨文最近与微软合作，推动甲骨文云平台与微软 Azure 云的集成。甲骨文更希望其数据库运行在其云上，但通过联盟，它表示愿意与微软合作，在 Azure 上部署甲骨文数据库，Azure 是 AWS 的领先行业替代平台。当然，微软有其专有的数据库，以微软 SQL Server 的形式采用。

Ball 表示，RDX 不仅提供工具来加速向亚马逊 Aurora 的转换，还为希望将亚马逊 Aurora 的管理外包给 RDX 的客户提供托管服务。

大多数组织需要几个月的时间将传统应用迁移到公共云。AWS 有兴趣尽可能帮助加速这一进程。但是许多采用最佳 DevOps 实践的组织发现他们的努力受到了对专有数据库的依赖的阻碍。事实上，如此多的开发人员倾向于开源数据库的原因之一是为了避免所有与获得新数据库许可相关的麻烦。

目前还不清楚 DevOps 在企业中的兴起最终会在多大程度上改变数据库的忠诚度。Oracle 试图通过将其数据库作为托管服务来保持尽可能多的控制，从而消除一些与构建新实例相关的采购开销。但是，Oracle 数据库许可证的成本仍然隐藏在托管服务的成本中。

并非每个组织都在寻求从专有数据库过渡，但是现在围绕“开源优先”运动有足够的势头，值得开发工具来自动重构遗留数据库，这不仅是为了降低成本，也是为了使其更加敏捷。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)