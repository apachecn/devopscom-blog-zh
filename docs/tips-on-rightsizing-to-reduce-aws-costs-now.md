# 关于合理调整以降低 AWS 成本的提示

> 原文：<https://devops.com/tips-on-rightsizing-to-reduce-aws-costs-now/>

在这种商业环境下，每个人都希望降低成本。首席财务官正在重新评估他们的软件和基础设施支出，自然，公司也在寻找优化 AWS 成本的方法。事实上，我们现在正在利用云之所以如此引人注目的一个主要原因:您可以根据业务需求更加灵活地控制成本。

## **您如何在保持性能的同时降低成本？**

一个好的起点是确定 AWS 的大部分支出来自哪里。一旦知道了这一点，您就可以关注导致最多费用的因素，并确定哪些服务可以缩减，哪些服务需要最多资源。根据服务的不同，有许多选项，如 Amazon EC2 保留实例(RI)、Amazon EC2 Spot 实例和资源合理调整。在这篇博文中，我将讨论合理调整。

有一些很棒的 AWS 和第三方工具(我倾向于 nOps)可以帮助您了解和分析当前的使用模式，并为合理调整 RI 和 Spot 实例提供建议。根据我的经验，亚马逊弹性计算云(亚马逊 EC2)、亚马逊关系数据库服务(亚马逊 RDS)和亚马逊简单存储服务(亚马逊 S3)一直出现在 AWS 账单的前五名。因此，在本文中，我将重点关注这三种服务的合理调整策略。

合理调整不仅仅意味着从旧实例迁移到新一代实例。用这种方法你可能不会省很多钱。合理调整有助于识别明显过度调配的资源。此外，许多资源都是使用 HashiCorp Terraform、AWS CloudFormation 或 AWS 上的自动扩展组进行配置的，因此为短暂的资源寻找合适的机会，并更新自动化不仅可以降低现在的成本，还可以降低未来的 AWS 成本。

## **优化亚马逊 EC2 和亚马逊 RDS 实例**

毫无疑问，亚马逊 EC2 支出是你 AWS 账单上最贵的项目。Amazon EC2 提供了一套强大的 CPU、内存和网络 I/O 选项，内存范围从 0.5GB 到 1TB。有这么多选择可能是一把双刃剑——你如何选择？

您可以根据您的使用案例选择合适的实例类型:计算优化(针对 CPU 密集型工作负载)、内存优化(针对内存密集型工作负载)或网络优化(针对增强的网络吞吐量)。

在为您的工作负载选择最佳实例时，需要考虑一些参数。无论是 HPC 工作负载，还是简单的 Python Flask 应用程序或数据管道项目，都有最适合这些工作负载的 Amazon EC2 实例类型。

为了明智地选择实例，根据当前运行实例的网络 I/O 和 CPU 利用率，应用最具成本效益的 Amazon EC2 实例类型。例如，如果为 Python Flask 应用程序配置了 t3.xlarge，并且使用了不到一半的内存，则该实例类型已经为该工作负载过度调配了。在这种情况下，较小的实例可能更合适，比如 t3.small。    同样值得注意的是，尽管大多数 EC2 实例都考虑了性能，但随着时间的推移，程序的利用率可能会降低，从而导致实例根据当前的 CPU/内存使用情况过度调配。我通常会查看 Amazon CloudWatch 中没有消耗每个实例当前可用的所有资源的实例，并根据历史使用情况，提供适当调整它们的建议。而且，我可以看到与建议的更改相关的成本节约。

这种方法也适用于亚马逊 RDS。Amazon RDS 实例的底层架构与 Amazon EC2 实例非常相似。两者都需要一个亚马逊虚拟私有云(亚马逊 VPC)、安全组和一个磁盘来运行托管数据库实例。

## **优化亚马逊 S3 存储类**

亚马逊 S3 提供了一系列为不同使用案例设计的存储类别:

*   S3 常用数据通用存储标准。
*   S3 智能分层，适用于访问模式未知或不断变化的数据。
*   S3 标准-不频繁访问(S3 标准-IA)和 S3 One Zone-不频繁访问(S3 One Zone-IA ),用于长期但不太频繁访问的数据。
*   亚马逊 S3 冰川(S3 冰川)和亚马逊 S3 冰川深层档案馆(S3 冰川深层档案馆)进行长期存档和数字化保存。

您可以根据存储桶中对象的使用情况来确定最合适的存储类别。因此，您可以削减存储桶中对象的成本，以及从亚马逊 S3 下载或传输文件到任何其他位置所需的 GET 请求的成本。

## **快速获得结果**

与许多快速增长的公司一样，优步也在寻找在不影响其高速团队的情况下优化 AWS 成本的方法。使用上述一些策略以及其他策略，他们能够在短短 30 天内节省 15%的 AWS 成本。优步的关键之一是他们持续监控和优化成本——而不是一劳永逸的方法——因为他们的 AWS 环境变化速度如此之快。他们为此使用 [nOps](https://www.nops.io/) 云管理。

优步高级技术集团基础设施平台高级工程经理 Nick Cobb 报告说，他能够“将成本操作化并直接提交给工程师，在实施的第一个月节省了 15%。除了为领导层和预算流程提供报告之外，我们的效率团队还可以为研发工程师制定行为改变，这些工程师通常习惯于向具有挑战性的问题投入资金。”

如果你对优步使用的战略的更多细节感兴趣，以及你的组织现在可以使用的其他成本优化战略，尼克将于 4 月 21 日与我和 AWS 一起参加 DevOps.com[关于持续成本优化的网络研讨会](https://webinars.devops.com/how-uber-reduced-aws-costs-15-in-30-days) 。这是目前许多组织的热门话题，所以请加入我们。