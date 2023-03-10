# 运营报告平台的数据保护

> 原文：<https://devops.com/data-protection-operational-reporting-platforms/>

根据来自社交、移动和云平台的数据做出实时业务决策是当今世界的一项要求。这就是为什么 Spark、Apache Cassandra、Kafka、Docker、Mesos、Marathon 等新一代运营报告平台的生态系统应运而生。企业正在使用这些技术来重新设计其数据存储和处理框架，以实现更低的成本、可扩展性和更快的响应时间。然而，随着企业在这种下一代技术堆栈上部署业务关键型应用程序，他们需要为可能会中断面向客户的应用程序的故障或错误做好准备。

运营报告平台提供的主要优势之一是实时可见性，这使企业能够根据可操作的见解做出战略决策。但是，新的应用程序会产生大量数据，而陈旧的运营报告平台(基于传统数据仓库、数据集市和 ETL 逻辑的平台)无法跟上，因此:

*   业务决策基于陈旧的数据
*   碎片化的数据增加了出错的风险
*   数据的多份拷贝增加了存储成本

这些问题促使许多进步的、以数据为中心的企业重新构建他们的运营报告平台。在这个新的架构中，Kafka 充当一个持久的消息总线，它从关系存储中获取数据并提供故障恢复和消息缓冲。火花或火花流可用于转换、聚合和其他轻量级流处理。这些处理节点可以部署在 Docker 容器中。最后，Apache Cassandra 充当分布式数据存储层，提供线性可伸缩性和高可用性。Kafka 还支持通过 [Flafka](http://blog.cloudera.com/blog/2014/11/flafka-apache-flume-meets-apache-kafka-for-event-processing/) 添加多个数据消费者，如 Hadoop/HBase。

![Datos IO - operational reporting platforms](img/348e76862a1f85de69f9cbae9eab3b5f.png)

然而，随着企业采用运营报告平台，他们希望确保[不良数据馈送和人为错误](http://datos.io/to-err-is-human/)不会导致数据丢失。Apache Cassandra 本机复制数据，但不提供及时恢复数据的能力。

随着企业采用其关键应用程序来实现开发灵活性、可扩展性和更低的运营成本，他们还必须探索专门针对横向扩展数据库的数据保护解决方案。