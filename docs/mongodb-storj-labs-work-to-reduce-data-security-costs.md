# MongoDB 和 Storj 实验室致力于降低数据安全成本

> 原文：<https://devops.com/mongodb-storj-labs-work-to-reduce-data-security-costs/>

MongoDB Inc .和 Storj Labs 今天宣布，他们已经联合为开源 MongoDB 数据库创建了一个备份服务，该服务利用全球网络提供额外的存储容量。

Storj Labs 创建了一个基于[的 Tardigrade 分散式云存储服务，这是一个开源对象存储系统，与亚马逊网络服务(AWS)定义的 S3 应用编程接口](https://devops.com/storj-labs-unfurls-decentralized-storage-service/) (API)兼容。该对象存储系统将文件的 80 个切片分布在成千上万个节点的子集上，每个节点仅包含在需要时重建该文件所需的数据切片。重建一个文件只需要其中的 29 个切片，这使 IT 团队能够保护数据，而不必管理加密密钥。

通过 Storj Labs 的连接器，现在可以通过 MongoDB DevOps Manager 调用 Tardigrade 分散式云存储服务，该服务在 MongoDB Inc .提供的开源数据库的商业支持企业版中提供。

![](img/3853c6aaf4bbecf645bc19e9db923705.png)

Storj Labs 首席执行官 Ben Golub 表示，Tardigrade 分散式云存储服务为基于云的备份和恢复平台提供了一种更便宜的替代方案，因为从服务器到个人台式机等设备上的过剩容量随时可用，他说，挑战在于找到一种方法来集中所有过剩容量，使 it 组织能够轻松使用。

Golub 说，IT 组织应该期待 Storj 实验室为数据库和其他平台建立更多的连接器，这些平台需要更便宜的数据保护方法。他指出，随着新冠肺炎疫情带来的经济衰退，越来越多的组织开始接受创新方法来降低存储成本。

当然，大多数 IT 团队都习惯于采用一系列数据保护平台来备份和恢复数据。在整个企业中部署的数据库的数量和类型持续快速增长的时候，Tardigrade 分散云存储服务可能会被视为另一种选择。开发人员特别喜欢采用开源文档数据库，这种数据库不需要数据库管理员(DBA)从中央采购组织获得许可。然而，通常不需要太长时间，开发人员就会寻求中央 It 部门的帮助来管理所有这些数据库，尤其是在生产环境中部署了应用程序之后。

当然，并非所有这些应用程序都具有同等价值，因此考虑到当前的经济环境，人们可能更愿意尝试至少替代性的数据保护方法。

然而，不管平台如何，有一点是明确的，即数据保护和 IT 基础架构的其余部分越来越多地由 API 驱动。因此，数据保护的责任也进一步推给了开发运维团队，他们拥有使用 API 持续自动化备份和恢复所需的专业知识。这可能并不总能让传统的 it 管理员满意，他们已经使用基于图形用户界面(GUI)的工具几十年了。然而，信息技术时代显然正在发生变化。