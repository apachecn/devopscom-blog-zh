# 介绍 IBM Cloud ant on Transaction Engine:Cloud Native by Design

> 原文：<https://devops.com/introducing-ibm-cloudant-on-transaction-engine-cloud-native-by-design/>

**作者:****IBM 云数据服务部副总裁兼首席技术官 Adam Kocoloski**

IBM 公共云建立在开源创新、安全和企业级基础设施的领导地位的基础上，所有这些都是为了让我们的客户能够快速构建新的应用程序，同时降低管理这些扩展的应用程序的复杂性。今天，随着 Cloudant on Transaction Engine 的到来，我们宣布了这方面的一项重大新功能。

[IBM Cloudant](https://www.ibm.com/cloud/cloudant?lnk=STW_US_STESCH&lnk2=trial_Cloudant&pexp=def&psrc=none&mhsrc=ibmsearch_a&mhq=cloudant) 是一个可弹性伸缩的、无服务器的数据存储，旨在满足云原生应用程序开发人员的需求。自 2014 年以来，它已经为 IBM Cloud 中的各种内部和外部应用提供了支持。像许多原始的“NoSQL”解决方案一样，Cloudant 通过牺牲传统关系数据库系统的一些隔离和一致性保证来提供可伸缩性和可用性。当我们进入云的第 2 章时，我们给自己的任务是恢复那些任务关键的属性，同时保留和增强 Cloudant 的云原生特性。Cloudant on Transaction Engine 代表着我们朝着实现这些目标迈出的第一大步。

**扩展到新的高度**

新的事务引擎架构高效地组织数据，以便大规模快速检索，我们正在将这些效率传递给我们的客户。运行在事务引擎上的 Cloudant 实例可以支持高达 **100TB** 的数据库，我们已经将这些新实例的每 GB 存储价格降低了 4 倍。我们一直在努力优化硬件配置，以降低成本并利用存储技术的新创新来支持这一新定价。数据仍然以一式三份的形式存储，并在 IBM Cloud Availability Zones 之间复制，您只需为您使用的存储付费。

事务引擎设计也极大地促进了查询处理。在二级索引中更智能地组织数据使我们能够有效地扩展查询吞吐量，而不会对应用程序的数据模型施加分区限制。在整个数据库上创建视图和辅助索引，并在扩展时以可预测的、一致的性能查询它们。在发布时，我们将调配的读取吞吐量上限提高了 5 倍，如果您需要更多的吞吐量。Cloudant on Transaction Engine 还消除了将全局查询作为一个单独的供应吞吐量类别，从而为某些类型的查询节省了高达 20 倍的成本。

**强一致性**

在事务引擎上向 Cloudant 发出的 API 调用针对数据库的*一致、隔离的*快照进行操作。文档操作完全 [线性化](https://jepsen.io/consistency/models/linearizable) ，二级索引与主数据库保持事务一致。为每个 Cloudant 数据库导出的原生变更捕获提要也是完全有序的，除非客户端要求，否则服务永远不会重放以前观察到的事件。

虽然我们已经成为设计应用程序的专家，能够最好地利用最终一致的系统，并乐意与我们的客户分享这一专业知识，但不受最终一致性影响的数据服务只是消除了开发人员否则必须考虑的一整类问题。我们很高兴在 IBM Cloudant 中提供这一功能，并期待扩展能够利用 IBM Cloud 的关键任务应用程序集。

**原生安全**

将他们的数据委托给云数据库的组织需要知道数据被安全地存储并且防止不正当的使用。Cloudant on Transaction Engine 实现了本地数据库加密，因此用户数据甚至在到达磁盘之前就被表示为密文。每个数据库都使用一个唯一的数据加密密钥进行加密，无需额外费用，这些加密密钥的信任根源总是可以追溯到 IBM Cloud 的标准密钥管理服务，该服务利用了一些业界最安全的商用加密技术。

**按设计打开**

Cloudant on Transaction Engine 强化了 IBM 对开放式创新的承诺:支持事务引擎实例的核心数据库特性正在作为 Apache CouchDB 下一个主要版本的一部分进行开发。虽然我们坚信 Cloudant 为客户提供了从这些创新中受益的最佳工具，但我们致力于数据归您所有的原则，我们将始终支持开放 API 和与开源社区的复制互操作性。此外，我们的 Apache CouchDB 扩展产品确保您可以获得在自己的数据中心或其他混合云环境中部署和管理 CouchDB 所需的支持。将 CouchDB 和 Cloudant 结合在一起，您可以获得一种独特的能力，将您的数据准确地带到全球任何需要的地方。

客户正在认识到今天宣布的更新带来的好处。PayRange 首席技术官 Prashant Kanhere 表示:“作为 IBM Cloudant 的长期客户，我们很高兴能够将新的 Cloudant on Transaction Engine 优势纳入 PayRange 移动支付架构。“PayRange 为成千上万台机器上的客户提供非接触式支付方式，这一功能如今比以往任何时候都更加重要。我们是 Cloudant 全局查询的大用户，有很高的吞吐量要求，并一直在寻找优化性能、可伸缩性和成本的方法。Cloudant on Transaction Engine 提供了在所有这些方面将我们的应用引向正确方向的能力。”

除了宣布 IBM 的 Cloudant on Transaction Engine 的新功能，我们还庆祝了结构化查询语言(SQL)背后的关系模型 50 周年。1970 年 6 月，IBM 研究员和计算先驱[埃德加·弗兰克·科德](https://slack-redir.net/link?url=https%3A%2F%2Fwww.ibm.com%2Fibm%2Fhistory%2Fexhibits%2Fbuilders%2Fbuilders_codd.html)发表了开创性的论文“[大型共享数据库的数据关系模型](https://slack-redir.net/link?url=https%3A%2F%2Fwww.seas.upenn.edu%2F~zives%2F03f%2Fcis550%2Fcodd.pdf)”，描述了成为 SQL 基础的著名关系模型。

**##**