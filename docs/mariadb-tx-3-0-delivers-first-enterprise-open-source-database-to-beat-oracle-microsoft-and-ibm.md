# MariaDB TX 3.0 推出首个企业开源数据库，击败甲骨文、微软和 IBM

> 原文：<https://devops.com/mariadb-tx-3-0-delivers-first-enterprise-open-source-database-to-beat-oracle-microsoft-and-ibm/>

*提供开源数据库从未提供的高级数据保护、专用存储引擎、时态处理和 Oracle 兼容性功能*

**加利福尼亚州门洛帕克和赫尔辛基——2018 年 5 月** **24 日——**[*Maria db Corporation*](https://mariadb.com/)今天宣布发布 [MariaDB TX 3.0](https://mariadb.com/products/solutions/oltp-database-tx) ，这是第一个提供高级功能的企业开源数据库解决方案，到目前为止，这些功能需要昂贵、专有和复杂的数据库。应用程序开发人员和数据库管理员(DBA)现在可以突破传统的数据库模式，快速响应当今快速变化的需求。MariaDB TX 3.0 使用专门构建的存储引擎来同时支持具有不同特征的多种工作负载—事务性、分析性、写入密集型或超大规模。MariaDB 还引入了时态处理、Oracle 兼容性和针对敏感个人和个人可识别信息的高级数据保护(SPI/PII)，从而扩大了支持的用例数量。借助 MariaDB TX 3.0，客户可以轻松、快速、安全、经济地在企业开源数据库上运行其关键业务。

“多年来，企业一直受到在专有数据库产品上运行核心业务的高成本的挤压，没有简单的出路。MariaDB 公司服务器产品管理负责人 Max Mether 表示:“以 MariaDB TX 3.0 和 MariaDB Server 10.3 GA 为核心，我们不仅创造了一种将应用迁移到 MariaDB 的简化方法，我们还开创了企业开源数据库的新标准。“MariaDB 用户现在可以混合搭配多个专门构建的存储引擎，以最佳性能支持一系列使用情形——所有这一切都在同一时间和同一熟悉的数据库中完成。”

**MariaDB:甲骨文的替代品**

长期以来，专有数据库供应商用层层复杂性和高成本限制了 IT，阻碍了创新和业务增长。迁移到更灵活、更现代的解决方案的过程一直非常耗时、复杂且耗费大量资源，并且缺少只有在昂贵的专有数据库中才能找到的关键功能。

MariaDB TX 3.0 是第一个提供 Oracle 兼容性的企业开源数据库，包括与 Oracle 兼容的序列和与 Oracle PL/SQL 兼容的存储过程语言，使 Oracle 数据库用户能够在迁移应用程序或部署新应用程序时重用现有代码和已建立的技能集。新加坡开发银行(DBS)通过与 MariaDB 在 Oracle 兼容性方面的合作，仅在 12 个月内就将其 50%以上的任务关键型应用程序从 Oracle 数据库迁移到了 MariaDB。这种兼容性与新的 [MariaDB Red Rover 迁移实践](https://mariadb.com/services/migration-practice)相结合，帮助客户充满信心地迁移到 MariaDB。

**简易时态数据处理**

MariaDB TX 3.0 引入了内置的系统版本化表，使开发人员能够轻松优雅地将时态要素构建到应用程序中。这消除了为维护行历史而手动创建列、表和触发器的需要，解放了 DBA，使他们只需创建具有系统版本控制的新表或修改现有表来添加它，从而大大简化了流程。开发人员可以使用标准 SQL 查询一个表，以查看数据在之前的某个时间点是什么样的，例如查看客户的配置文件历史，以了解偏好如何随着时间的推移而变化。

**每次都完美的数据库**

MariaDB 受益于一种独特的体系结构，可以通过部署在商用硬件上的单个数据库中的可插拔专用存储引擎进行配置。客户可以通过在同一模式中混合搭配用于事务查询的 InnoDB、用于分析查询的 ColumnStore、用于写密集型工作负载的 MyRocks 或用于极端规模的 Spider，同时支持各种不同的工作负载。不管是什么用例，MariaDB 每次都能完美剪裁。

MariaDB TX 3.0 包括 MyRocks 和 Spider 存储引擎的正式上市。

*   **MyRocks** :固态硬盘(SSD)的写入和空间优化存储引擎，支持 IoT 和 M2M 等写入密集型工作负载。其他使用案例包括电子商务点击流和购买应用程序，这些应用程序需要连续的写入流，而不会影响用户体验。
*   **Spider** :用于读取、写入和存储扩展的分布式存储引擎，其中数据、设备或用户的数量大于单个数据库实例，需要分布在多个数据库实例中。用例包括面向数百万网站访问者的 web 购物车和 cookies，它们需要高性能、可伸缩性和并发性。

**高级数据保护**

没有其他企业开源数据库具有内置的数据保护来保护敏感的个人身份信息不被暴露，无论是意外还是恶意的。MariaDB TX 3.0 增加了通过完全数据混淆匿名化数据或通过完全或部分数据屏蔽伪匿名化数据的能力。高级数据保护和安全性永远不会作为一个昂贵的附加组件分离出来。

**可用性**

MariaDB TX 3.0 将于明天开始正式提供[下载](https://mariadb.com/downloads/mariadb-tx)。

**附加资源**

*   网络研讨会:[注册了解 MariaDB TX 3.0 的新特性](http://go.mariadb.com/mariadbtx3.0_webinar_registration-LP.html?utm_medium=release&utm_campaign=2018-mariadbtx3.0-webinar)
*   博客:[Maria db TX 3.0——率先兑现企业开源的承诺](https://mariadb.com/resources/blog/mariadb-tx-30-first-deliver-promise-enterprise-open-source)
*   [MariaDB TX 3.0 数据表](https://mariadb.com/sites/default/files/content/assets/ds/mariadb_tx_3_ds.pdf)
*   参观[mariadb.com](https://www.mariadb.com/)
*   在推特上关注 [@mariadb](https://twitter.com/mariadb)
*   阅读 MariaDB 的[博客](https://mariadb.com/resources/blog)

**关于 MariaDB 公司**

MariaDB Corporation 是 MariaDB(增长最快的开源数据库)背后的公司。MariaDB 在社区创新和企业采用方面有着悠久的历史，它提供了功能最全的开源数据库。MariaDB 为谷歌、维基百科、腾讯、威瑞森、星展银行、德意志银行、西班牙电信、华泰证券等公司的应用提供支持。

MariaDB 解决方案旨在运行在任何基础设施上，包括裸机服务器、虚拟机、容器、公共云和私有云，可用于所有领先的 Linux 发行版，包括 Ubuntu，并且是 openSUSE、Manjaro、Red Hat Enterprise Linux(RHEL)/CentOS/Fedora、Arch Linux、SUSE Linux Enterprise 和 Debian 的默认数据库，覆盖全球超过 6000 万开发人员。

###

 ****