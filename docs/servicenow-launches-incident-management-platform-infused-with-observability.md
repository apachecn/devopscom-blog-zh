# ServiceNow 推出注入可观察性的事件管理平台

> 原文：<https://devops.com/servicenow-launches-incident-management-platform-infused-with-observability/>

ServiceNow 在其软件即服务(SaaS)产品组合中添加了一个基于去年收购的 Lightstep observability 平台的事件管理平台。

ServiceNow 的 Lightstep 总经理本·西格曼(Ben Sigelman)表示, [Lightstep](https://lightstep.com/) 事件响应使开发运维团队能够使用[可观察性](https://devops.com/?s=observability)工具，通过自助服务门户，使他们能够更快地确定任何事件的根本原因。它将协调电话呼叫上报、警报分组、事件分析和补救的能力与一套协作和事件管理工具相结合。

Sigelman 指出，这种方法将使 Lightstep observability 平台更易于通过云服务访问。Lightstep observability 平台本身基于一个时间序列数据库，每天能够处理一万亿个事件。

Lightstep Incident Response 通过共享日历同步日程安排来管理组织的随叫随到服务，并根据事件的性质和受影响的服务使用特定的标签来指示谁需要参与。团队成员被邀请到基于预构建协作集成的专用渠道进行快速补救。随着时间的推移，他们可以创建自动流程，在问题再次出现时进行自我分类和自我修复。该平台还集成了 LogicMonitor、Postman、Slack、Sumo Logic 和 Zoom 等监控、观察和协作工具。

Lightstep 事件响应现已推出免费版和付费版。定价基于被管理的活动服务的使用，而不是基于席位许可。

Lightstep 事件响应还与 ServiceNow 为 IT 服务管理(ITSM)创建的 Now 平台进行了本机集成。Sigelman 指出，这种集成将使组织能够更容易地融合 ITSM 和 DevOps 工作流。

可观察性平台聚集了日志、指标和跟踪的集合，使得开发运维团队能够查询这些数据。目标是让 DevOps 团队更容易识别可能破坏应用程序环境的异常。然而，这些相同的工具也允许开发运维团队更快地确定 IT 事件的根本原因。今天，许多组织定期召开“作战室”,要求 IT 团队通过排除过程费力地确定问题的根本原因；这可能需要几天——有时甚至几周——才能完成。

Sigelman 说，随着越来越多的应用变得仪器化，部分由于开源代理软件的可用性，可观察性平台将在帮助自动化事故管理过程中发挥关键作用。在被 ServiceNow 收购之前，Lightstep 团队成员在 OpenTracing 和 OpenTelemetry 开源项目的创建过程中发挥了作用，用于收集跟踪、指标和日志。今天，OpenTelemetry 是一个沙盒级别的项目，由云本地计算基金会(CNCF)管理。

随着更多基于微服务的应用程序的部署，应用程序被检测的百分比将很快大幅增加。如果没有某种程度的工具，管理这些高度分布式的应用程序是不可行的。当然，现在的问题是，确定在多大程度上也对已经在相同环境中运行的许多单片应用程序进行检测。