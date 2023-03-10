# 数据库瓶颈:App 变慢的隐藏原因？

> 原文：<https://devops.com/database-bottlenecks-hidden-cause-app-slow-downs/>

性能问题会削弱任务关键型业务应用。如果您足够幸运，您的解决方案可能很简单，只需增加更多的广域网带宽、几台额外的服务器或一个内容交付网络，但是当您的数据库成为您最大的瓶颈时，真正的问题就出现了。当性能问题对保持业务运营和收入的应用程序产生负面影响时，挑战就更加难以克服。

检查架构缺陷、深入代码寻找缓慢性能的线索以及搜索日志文件寻找关联事件可能是一项艰苦、乏味的工作。在要检查的所有方面中，以下三个问题点应该在排除性能问题的故障排除优先级列表中处于较高位置:

1.  连接池问题
2.  低于标准的查询性能
3.  处理繁忙流量的并发能力不足

当数据库管理员(DBA)未能及时发现并修复瓶颈时，企业会失去眼球和收入，有时会终生失去客户。每个事务性应用都访问关系数据库，它们最大的问题是横向扩展的挑战。虽然现代数据库支持横向扩展，但今天的应用程序并没有利用这种额外的容量。

一个中间软件层，数据库负载平衡软件，解决了这一挑战；它使应用程序能够使用额外的服务器，而无需任何代码更改。它通常还包括缓存，这可以显著提高性能—同样，无需更改代码。数据库负载平衡不仅使水平扩展变得容易，还能帮助您识别其他瓶颈，并在几分钟内缓解它们。

## 数据库负载平衡:银弹？

数据库负载平衡软件配有分析工具，可以实时精确定位数据库问题。它监控一切，从每个读写查询到连接、服务器性能和整体数据库负载。详细的分析让您深入了解需要解决的问题，以及应该关注哪些方面以确保更好的性能。负载平衡器拥有及时解决性能问题所需的所有必要工具。它有效地解决了前面提到的三个主要性能问题，并通过以下方式显著提高了应用性能和可用性:

1.  **连接池和多路复用:**通过应用连接池和多路复用，数据库负载平衡软件可以显著减少到您的服务器的连接数量。与基于客户端的连接池不同，这种方法确保了更高的操作效率，并有助于轻松处理额外的连接高峰。

2.  **内存中的查询响应缓存:**软件的分析可以识别要缓存的潜在查询，并让您在不改变应用程序的情况下缓存它们。例如，您可以将一篇文章在内容管理系统(CMS)中缓存一天，让评论部分从数据库中取出以保持最新。您可以将邮政编码表缓存几个月。寻找设置生存时间过期或自动缓存失效的能力，以便您可以确保原子性、一致性、隔离性、持久性( ACID)合规性和事务安全性。

3.  **动态负载平衡:**数据库负载平衡软件以安全和一致的方式将应用程序中的查询路由到多个服务器。它的自动化读/写拆分通过将所有读取查询转移到可用的读取副本和写入主服务器来确保高性能。这种负载分布增加了容量，有利于即时横向扩展。负载平衡器就像一个控制点，提供对性能需求的深入了解。通过实时洞察问题的根本原因，整个查找和修复过程变得快速、高效和有效。

数据库管理员背负着识别数据库瓶颈这一最困难的任务，他们可以利用功能丰富的数据库负载平衡器来自动诊断瓶颈并让数据无缝流动，从而简化工作并提高工作效率。

## **关于作者/托尼·布兰森**

![](img/bcbc1aee23946d0362b88827966cce85.png)

托尼·布兰森是 ScaleArc 公司的数据库负载平衡高级分析师。Tony 热衷于剖析技术主题，如透明故障转移、集中控制、ACID 合规性、数据库可伸缩性和停机影响。在他休息的日子里，可以发现他在看科幻电影、攀岩或做志愿者。在[推特](https://twitter.com/IamTonyBranson)上关注他。