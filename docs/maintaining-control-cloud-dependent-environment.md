# 在依赖云的环境中保持控制

> 原文：<https://devops.com/maintaining-control-cloud-dependent-environment/>

随着数字化转型改变着全球企业的面貌，我们越来越依赖公共云提供商及其服务。当我们托管并向客户交付软件应用和服务时，像最近亚马逊 S3 存储子系统这样的故障会使全国乃至全世界大大小小无数公司的运营陷入瘫痪。

亚马逊可能也有自己的内部运营陷入停滞，因为它的平台和交付基础设施很可能是使用自己的服务构建的。以至于从美国东部时间下午 12:37 到下午 3:37，亚马逊由于对 S3 的依赖而无法更新其 SHD(服务健康仪表板)，不得不求助于 [Twitter](https://twitter.com/awscloud) 来让客户了解正在发生的事情！

中断的根本原因是其简单存储服务(S3)出现故障，如下所述:[https://aws.amazon.com/message/41926/](https://aws.amazon.com/message/41926/)。然而，大多数人最可能忽略的是它对依赖其 S3 服务可用性的其他 AWS 服务的影响。

在大修期间被中断的多个 AWS 服务包括:

*   Amazon Athena——用于使用 SQL 分析 S3 的数据
*   Amazon Elastic MapReduce(EMR)-用于大数据处理的弹性 MapReduce
*   Amazon Inspector——用于检测部署在 AWS 上的应用程序的漏洞
*   亚马逊 Kinesis fire hose——用于向 S3、红移或弹性搜索提供实时流数据
*   亚马逊简单电子邮件服务(Amazon SES)——用于为运行在 AWS 上的应用程序提供电子邮件服务
*   亚马逊工作邮件——亚马逊为企业提供的电子邮件和日历服务
*   Amazon Auto Scaling——允许您根据条件增减 EC2 容量
*   Amazon cloud formation–允许创建和管理相关 AWS 资源的集合

在停机窗口期间，多项服务出现了性能严重下降的情况，包括:

*   Amazon AppStream——Windows 应用程序的云端流媒体服务
*   亚马逊云搜索——托管搜索服务
*   亚马逊认知——移动和网络应用的身份服务
*   Amazon EC2 容器注册中心(ECR)-托管 Docker 容器注册中心
*   亚马逊弹性计算云(EC2)，亚马逊弹性代码转换器-媒体代码转换
*   亚马逊冰川–数据归档和备份
*   Amazon light sail–易于管理的 VPS
*   亚马逊移动分析–分析和跟踪移动使用数据
*   Amazon Pinpoint–推送通知
*   亚马逊红移-数据仓库服务
*   Amazon Simple Workflow(Amazon SWF)-面向开发人员的工作流服务
*   亚马逊工作文档–文档协作
*   AWS 批处理–批处理计算作业
*   AWS code build–编译代码、测试和生成软件包的托管服务
*   AWS 代码提交–托管源代码管理服务
*   AWS code deploy–托管代码部署服务
*   AWS 数据管道-数据工作流服务
*   AWS Electric Beanstalk–自动部署、负载平衡和扩展
*   AWS 密钥管理服务–加密密钥的集中控制
*   AWS Lambda–无服务器计算
*   AWS ops works–自动化 AWS 配置管理
*   堆栈——作为一个单元的 AWS 资源集合
*   AWS 存储网关—混合云存储

## 我们能从这次停电中吸取什么教训？

这次宕机不仅仅是云服务提供商独有的现象。即使托管在您自己的数据中心，一项或一组服务中断也很容易发生。当众多企业的主要服务提供商在他们提供的主要服务中遇到中断时，像这样的中断最终会产生广泛的影响。

对停机的巨大影响的另一个考虑是我们构建软件的方式。我们不再自己建造一切。我们构建基本组件，并尽可能使用第三方功能。鉴于亚马逊提供的服务和产品的广度，有一些公司的软件产品完全是在 AWS 上构建和运行的，这并非不可能。

[我们的客户](https://smartbear.com/product/alertsite/resources/case-studies/)在亚马逊的基础设施上运行应用程序，我们立即感受到了宕机的影响。下图显示了在我们的系统上被监控的应用程序中发现故障的时间与亚马逊中断的[时间之间的相互关系。](http://blog.smartbear.com/performance-monitoring/the-cloud-just-had-a-thunderstorm-now-what/)

这次中断可能是由硬件故障引起的。这可能是由一个软件更新没有准备好的黄金时间。或者像亚马逊在这种情况下向我们指出的那样，[这是由于人为错误](https://aws.amazon.com/message/41926/)。我们都经历过人为错误给客户带来困难的经历。可以想象的是，亚马逊正在收紧测试实时服务的流程，可以做什么，谁可以做，以及所使用的工具中内置了什么类型的故障保险，以便可以避免这些大规模的意外中断。

即使严重依赖云提供商，你又能做些什么来帮助自己呢？

1.  在开发/测试、试运行和生产的早期经常进行测试，以确保通过您的应用程序和服务(您自己的和来自第三方的)的所有关键路径都正常工作。
2.  在把你的软件推向生产之前，要做性能验收，因为在生产中发现问题比在开发/测试或试运行中发现问题要昂贵得多。
3.  监控云提供商提供的服务，以便在出现问题时立即知道。
4.  了解您的云提供商在处理生产系统变更时遵循的政策和程序。他们的流程和控制及其恢复机制的成熟度应该让您高枕无忧，这种程度的停机将导致快速恢复。

## 关于作者/ Anand Sundaram

![](img/890e205313acefcca1233a2468b90c6b.png)Anand Sundaram 拥有近 25 年建立和发展多项技术业务的经验，是 smart bear Software[alert site](https://smartbear.com/product/alertsite/overview/)的产品副总裁。他是三家初创公司的联合创始人，其中包括估值超过 2.4 亿美元、拥有 160 多名员工的 RSW 软件公司。他在软件质量、安全性和部署后监控方面拥有丰富的背景知识，构建了两个负载测试产品，并发明了第一个部署后深度事务监控产品。