# DevOps 的消费者网络自动化？

> 原文：<https://devops.com/consumer-web-automation-devops/>

如今，基于事件的自动化无处不在，从非技术人员使用的 IFTTT 菜谱，到 Twitter、Google+和脸书的自动交叉发布，再到免费 iTunes 下载的电子邮件提醒。不要忘了从 Zapier 和现在的 Stamplay 创建更复杂序列的技术知识，以跟踪工作负载和简单的业务流程或自动化开发工具。

但这种自动化不仅限于消费者使用，它也可以解决 DevOps 的挑战。通过 IFTTT 和 Zapier 等服务实施的简单 DevOps 流程改善了工作流程，提高了工作绩效。

让我们来看一些具体的例子

在大型企业中，有一些应用程序拓扑超出了典型的需求。这些对于金融服务、军事、应急服务和警察行动，或者对于确保自动出纳机和销售点系统的快速响应时间，都是必不可少的。

通过 Zapier 集成基于 web 的平台 RequirementOne 和 Microsoft Azure 网站，IT 网络资源规划成为开发和运营的共同基础。双方都可以访问软件架构，允许他们评估新触发的需求，并立即决定是否需要更改应用程序设计或代码。

**将 DevOps 自动化引入物联网**

IFTTT 有一些连接硬件设备的方法。Belkin 的 We-Mo 开关通过 Wi-Fi 从任何地方控制设备，芬兰初创公司 The Button Corporation 使用“bttn”——一种物理互联网连接按钮——按下它可以触发结合互联网技术的特定可配置操作，如脸书、HTTP、Twitter、短信或电子邮件。

Samanage 是一个基于云的硬件库存解决方案，可以保存网络中所有硬件的详细配置和物理位置，通过 Zappier 可以将其提升到一个新的水平。它可用于通知团队成员硬件库存的变化，确定需要关注的问题并触发新的解决方案。

但不仅仅是独特的场景，交付管道的标准组件也可以自动化。

**连续部署**

连续部署可以通过标准化变更来防止倒退或失败，从而提高软件质量。为了实现这些标准，一些 zaps 可以提供帮助。例如，新的 Relic 应用程序可以检测新的部署并运行 Runscope Radar 中定义的测试。Runscope Radar 是一个框架，它构建测试来验证您的服务是否返回预期的数据，并在出现故障时接收通知。当 Jenkins 上的部署作业完成时，它会记录在 New Relic 中，让您可以看到部署对性能和操作的影响。新的遗迹部署通知可以通过 Pushover Push 发送到手机，发送到 Twilio Call Phone，并可以自动添加到 Google Calendar 作为一个新的事件，并提供详细信息。它还可以向 HipChat 发送消息，或者创建 Zenddesk 票证或 FogBugz Bug 来创建案例。

对于没有 SQL DB 部署的系统，MMS (MongoDB 管理服务)是一个免费的基于云的服务，用于监控 MongoDB 部署的健康状况，可以跟踪关键的性能指标，使用户能够更好地优化部署。通过 PagerDuty IFTTT 集成，MMS 还可以在某些指标超出正常范围时自动发送触发警报，从而提供任何潜在部署问题的即时通知。

**监控**

DevOps 监控方法的目标是找出应用程序何时结束运行或服务何时不可用，以便预测故障或显示事后原因。

Scout 是一个托管服务器监控解决方案，收集各种服务器和应用程序指标，如内存使用、服务器负载、网络吞吐量等。然后，它会根据指定的阈值和趋势发出警报。与 Zapier 结合，Scout 可以向 Campfire 聊天室发送通知或向 HipChat 发送警报，同时将这些警报记录在整个团队都可以访问的共享 Dropbox 文件中。

Monitis 是一个基于云的监控解决方案，它使用一个仪表板界面来显示网站服务器和应用程序的健康状况。当出现问题时，它使用 Zapier 触发器发送警报。

OpsGenie 的心跳监控软件和应用程序 Pingdom 也使用频道切换警报。OpsGenie 的 Heartbeat 确保系统受到端到端的审计，并实时报告问题。Pingdom 提供关于网站网络和服务器的正常运行时间、停机时间和性能的网站报告。

IFTTT 监控更加有限。它仅提供围绕发送和接收 SMS 构建的方案，例如在网络基础设施故障、服务器故障或性能下降的情况下。为了使用 IFTTT PagerDuty 响应 DevOps 事件，它应该与聊天应用程序相关联。无论您使用桌面还是 Android 或 iOS 移动设备，都可以将触发、解决、确认、升级和分配发布到 HipChat 聊天室。

**促进团队协作**

Zapier 和 IFTTT 实现了 DevOps 的另一个目标——通过工具促进团队协作。GitHub 存储库可以以这样的方式配置，即推送到它将自动触发 Jenkins(一个开源的持续集成服务器)中的构建。这允许开发人员接收即时反馈。Basecamp 是一个受欢迎的项目管理工具，它通过以下方式显著增强团队沟通:根据新的 Gmail 电子邮件或 Pivotal Tracker 故事创建待办事项，将事件添加到 Google 日历，在 HipChat 中发送新事件的消息，根据 Basecamp 待办事项创建新的 GitHub 或 JIRA 问题，将 Basecamp 附件同步到 Dropbox 或 Google Drive，或根据 GitHub commits 创建消息。

聊天是向整个团队广播问题或疑问或在调试时共享堆栈跟踪的快捷方式，另外还可以将整个讨论存档以供将来参考。习惯上是以每个产品或每个项目为基础建立聊天室。这方面的一个例子是 Salesforce Chatter，这是一款聊天软件，它通过在其上添加 IFTTT，将脸书、Twitter 或 Dropbox 等消费者互联网应用程序引入企业。为了提高工作效率，Toodledo 等基于网络的待办事项列表软件使用了功能强大的 IFTTT 菜谱，允许用户通过语音创建待办事项，或者在任务管理平台(如 Asana)上整合聊天室。使用 Zapier 触发器可以围绕单个任务进行实时讨论，或者跟进一个问题。
与 Zapier 集成的关系数据库(mySQL、PostgreSQL、SQL Server、Firebird)可以轻松保存或插入行，只需向给定的 Zapier 地址发送电子邮件即可。此外，可以永久监控数据库活动，如插入、更新和删除。亚马逊的 DynamoDB 和 MongoDB 等 NoSQL 数据库也可以与 Zapier 建立连接，并将数据导出到谷歌文档，从新表格向 WordPress 发布帖子，或者从新项目创建 ActiveCampaign 联系人。

如你所见，有很多例子。现在 Stamplay 采用了相同的 web 自动化概念，并特别关注开发人员。我相信这是一个很好的方式，让小团队接受 DevOps 概念，而不需要专门为 it 人员招聘，让企业用一个易于使用的工具卸载一些简单的任务，只需几天而不是几个月。

我唯一的问题是这对企业总线工具 MuleSoft 和 TIBCO 意味着什么。

分享您的 web 自动化方案，并让我们知道您如何使用基于消费者的酷工具来简化您的 DevOps 流程。