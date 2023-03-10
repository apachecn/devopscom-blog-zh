# 持续交付基金会增加互操作性项目

> 原文：<https://devops.com/continuous-delivery-foundation-adds-interoperability-project/>

在本周的一次 [CDEventscon](https://events.linuxfoundation.org/cdeventscon/) 活动中，连续交付基金会(CDF)宣布它正在主持一个 [CDEvents 项目](https://cd.foundation/announcement/2022/05/17/cd-foundation-announces-cdevents-a-vendor-neutral-specification-for-defining-the-format-of-event-data/)，它希望通过该项目创建一个供应商中立的规范，用于定义跨多种服务、平台和系统的事件数据格式。

IBM 的开源开发者倡导者、CDEvents 项目的共同创建者和 CDF 技术监督委员会的成员 Andrea Frittoli 表示，开源联盟正在发起这项倡议，以促进跨连续交付(CD)平台的互操作性。在 CDF 的上下文中，这个任务跨越了持续集成和持续部署平台，它们是 CD 的子集。

CDEvents 本身是基于云本地计算基金会(CNCF)内的无服务器工作组创建的现有 CloudEvent 规范。作为这项工作的一部分，CDF 已经建立了一个概念验证实现，使 Tekton pipelines 和 Keptn orchestration 工具能够管理应用程序生命周期，通过一个公共事件协议进行通信。

从多个 DevOps 平台收集指标是一项挑战，因为没有共享事件数据的标准。收集指标的分析提供商和价值流管理平台需要为他们支持的每个平台创建连接器。CDEvents 将为从任何开发工具或平台收集指标提供一个标准接口。他补充说，这些数据也将使描述工件及其元数据的工作流更容易可视化。

缺乏描述事件的通用方法意味着开发人员不仅必须不断地重新学习如何消费事件，还限制了库、工具和基础设施在从路由器和跟踪系统到软件开发工具包(SDK)的环境中促进事件数据交付的潜力。

当然，这种持续交付规范可能还需要一段时间才能提高跨 DevOps 环境的互操作性，但是跨已经成为碎片化工具和平台的拼凑物的需求是不言而喻的。许多组织已经在投资各种分析工具，希望提高应用程序的开发和部署速度。在太多的例子中，DevOps 团队无意中制造了瓶颈，减缓了开发的速度。挑战在于，随着新的工具和平台被添加到 DevOps 工作流中，在创建连接器之前，它们不太可能能够与这些应用程序共享数据。

当然，并不是每个人都喜欢更多的[指标](https://devops.com/?s=metrics)。目标应该是指导团队如何变得更有效率，而不是执行一套苛刻的命令。可以说，这样的命令只会赶走那些试图在作为艺术形式的编码和作为手艺的应用程序开发之间取得平衡的开发人员。

然而，随着组织更好地理解软件在驱动业务过程中所扮演的关键角色，就越希望衡量他们的应用程序开发工作的速度和效率——以证明他们在软件开发上的投资水平。