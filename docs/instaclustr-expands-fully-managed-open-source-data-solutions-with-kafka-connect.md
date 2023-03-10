# Instaclustr 通过 Kafka Connect 扩展了完全托管的开源数据解决方案

> 原文：<https://devops.com/instaclustr-expands-fully-managed-open-source-data-solutions-with-kafka-connect/>

*The addition of managed Kafka Connect provides enterprises with the most efficient, scalable, cost-effective, and reliable way to stream data between Kafka and myriad data systems*

**加利福尼亚州雷德伍德城——2020 年 6 月 8 日——**[insta clustr](https://www.instaclustr.com/)，通过完全托管的开源数据技术提供大规模可靠性，今天宣布 [Instaclustr 托管的 Kafka Connect](https://www.instaclustr.com/solutions/managed-kafka-connect/) 全面上市。Instaclustr 托管平台的最新成员支持 [Apache Kafka](https://www.instaclustr.com/solutions/managed-apache-kafka/) 和其他大规模数据系统之间的无缝数据移动。Kafka Connect 是继 Apache Kafka、 [Apache Cassandra](https://www.instaclustr.com/solutions/managed-apache-cassandra/) 、 [Apache Spark](https://www.instaclustr.com/solutions/managed-apache-spark/) 和 [Elasticsearch](https://www.instaclustr.com/solutions/managed-elasticsearch/) 之后，又一项由 Instaclustr 专业管理和支持的快速、成熟、有弹性且高度灵活的开源数据技术。

Kafka Connect——Apache Kafka 项目的开源组件——促进了 Kafka 集群与外部数据源和接收器之间的集成。该解决方案利用了可重用的开源 Kafka 连接器，作为 Kafka 和其他系统之间的插件。通过这样做，Kafka Connect 解决了在 Kafka 和所有其他系统之间开发线性可扩展的流数据集成器所固有的核心挑战。

Instaclustr 现在将 Kafka Connect 作为一项完全托管的服务提供，因为该解决方案通常需要相当高的操作能力，才能大规模高效部署和优化。Instaclustr 管理的 Kafka Connect 提供了这种深厚的专业知识，使客户能够快速构建 Kafka 集成到必要的数据源，并可靠地扩展其流数据功能。在 Instaclustr 亲力亲为的管理的支持下，企业可以将资源集中在构建他们的应用程序上，而 Instaclustr 则处理 Kafka Connect 定制和部署的复杂性。Kafka Connect 增加了 Instaclustr 在其[纯开源版本](https://www.instaclustr.com/company/open-source-2/)中提供的数据层技术，为 Instaclustr 客户提供了“开放核心”解决方案的有利替代方案，这些解决方案增加了许可成本，并促进了供应商锁定。

Instaclustr 首席产品官 Ben Slater 表示:“人们对 Kafka Connect 的兴趣一直在快速增长，这是理所应当的。“通过我们广泛的托管 Kafka Connect 预览版，我们继续看到这项技术可以为寻求最可靠和可扩展的方式将 Kafka 集群连接到外部数据源和接收器的企业提供多大的价值。我们很高兴现在推出 Instaclustr 管理的 Kafka Connect，并期待帮助新老客户更加高效地利用 Kafka。”

使用 Instaclustr，可以在几分钟内创建 Kafka Connect 集群，并开始构建 Kafka 集成。Instaclustr 包括一系列用于流行数据存储的预建连接器，包括 AWS S3。还提供自带 Kafka 连接器(BYO 连接器)选项，使企业能够更快速地部署定制 Kafka 连接器。这允许企业构建定制的集成和/或试验尚未创建的新集成。客户可以将任何 Kafka 连接器(包括任何开源、专有或第三方连接器(具有适当的使用许可))直接部署到他们专用的 Kafka Connect 集群上。

Instaclustr 管理的 Kafka Connect 提供了企业充分利用 Kafka 和其他数据源之间的实时数据集成所需的一切:

*   **自动化供应和部署:** Instaclustr 通过 Instaclustr 管理控制台、REST APIs 或 Instaclustr Terraform 提供程序提供托管 Kafka Connect 的自动化供应。
*   **灵活部署:**客户可以选择部署 Kafka Connect 集群并将其链接到 Instaclustr 管理的 Kafka 集群，或者部署到在 Instaclustr 平台之外运行的 Kafka 集群。并且可以选择将 Kafka Connect 集群部署在其自己的专用 VPC 中，或者部署在关联的 Kafka 集群的 VPC 中。
*   **在您的提供商帐户或我们的帐户中运行:**在 AWS、Azure 和 GCP(在正式发布后的后续版本中提供)上支持 Instaclustr 托管的 Kafka Connect，或者在客户自己的本地数据中心中支持。客户可以在 Instaclustr 的云提供商账户中以固定的、包含基础设施的成本运行它，或者使用他们自己的云提供商账户并支付每个节点的管理费。
*   **可用性 SLA:**使用 Instaclustr 管理的 Kafka 集群时，Instaclustr 提供 99.99%的可用性 SLA。
*   **监控和警报:**客户可以通过 Instaclustr 的管理控制台和 REST APIs 访问关键指标，还可以检索与 Prometheus 监控系统兼容的格式的监控指标。警报到位，使 Instaclustr 的团队能够主动识别任何违规行为。
*   **安全性:** Instaclustr 管理的 Kafka Connect 通过 SOC 2 认证，具有通过 TLS 的客户端到集群安全连接、节点到节点加密、防火墙配置和其他企业级安全功能。
*   **24×7 专家支持:** Instaclustr 客户可以 24×7 访问技术支持，拥有管理大规模分布式系统的实际专业知识。【T2

*   **预建连接器:**一个 AWS S3 连接器(在 GA 版本中可用)和一个 Cassandra 连接器和一个 Elasticsearch 连接器(将在后续版本中添加)。
*   **自定义连接器:**客户可以将任何连接器部署到他们专用的 Kafka 集群上(需要相应的使用许可证)。
*   **访问连接器日志:**连接器生成的访问日志可用于简化调试。

要开始试用 Instaclustr 管理的 Kafka Connect，请访问此处的，或联系 Instaclustr [销售](https://www.instaclustr.com/company/contact/)或[客户成功](https://support.instaclustr.com/hc/en-us/requests/new)团队。

**关于 Instaclustr**

Instaclustr 通过我们的开源技术集成数据平台提供大规模可靠性，如 Apache Cassandra、Apache Kafka、Apache Spark、Redis 和 Elasticsearch。我们使公司能够将内部开发和运营资源集中在构建面向客户的尖端应用程序上。Instaclustr 现在通过其开源技术套件管理着超过 7000 万个节点小时和 6 PB 的数据。