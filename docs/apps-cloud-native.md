# 你的应用应该是云原生的吗？

> 原文：<https://devops.com/apps-cloud-native/>

公司多年来一直依赖并从中获利的大量应用程序还有很多生命力。未来可能属于能够提供微服务和容器的性能和效率优势的云原生应用，但此时此刻，组织正在寻找将旧的优势与新的承诺相结合的方法。

随着不断的发展，你可能会说软件行业已经完全消除了产品生命周期的概念。然而，IT 经理知道，他们的组织目前使用的一些应用程序可能会在挂起编译器后很长时间内运行。

这些遗留应用程序已经多次证明了它们的价值。有些是一次性的，很容易适应新系统，并在实施时被新系统所适应。有些人非常擅长他们所做的事情，他们总结道，“如果它没有坏，就不要去修理它。”在应用程序和数据向云的大规模迁移中，很自然地，如此庞大的旧应用程序会受到审查，成为云原生应用程序的替代品。

在 2015 年 12 月 8 日的一篇关于堆栈的文章中，Red Hat 的 Gordon Haff 研究了 IDC 最近对企业开发运维团队的调查结果，发现 83%的人预计在 2019 年之前必须支持传统应用和基础架构。

[![DevOps_Cloud_Native](img/941b2edc7c64d67d1af7706b074b8e9d.png)](http://www.morpheusdata.com)

他指出，这似乎违反直觉，但在采用分布式、横向扩展、基于微服务的应用程序方面走得最远的组织，推迟将现有应用程序转换为云架构的可能性是其他组织的两倍。

## 什么特征使得应用成为云原生的？

TechTarget 的 Sean M. Kerner 在 2015 年 12 月的一篇文章中写道，云原生应用的最简单定义是“与物理基础设施分离”。除了从头开始设计为在云中运行(无论是私有还是公共),该应用还必须按需扩展，包括向上和向下扩展以及跨节点扩展。

Munish Kumar Gupta 通过 [Slideshare](http://www.slideshare.net/write2munish/building-cloud-native-applications-cdc-april-2013-v0-2) 表示，云原生应用具有容错性，可扩展，旨在异步处理请求，使用队列来分离功能。

另一个正在迅速成为云原生应用标准的功能是使用 Docker 容器，这有助于在公共亚马逊 Web 服务(AWS)云和私有 OpenStack 云以及其他选项上的部署。由 Linux 基金会和其他组织发起的云本地计算基金会(CNCF)可能很快会给出“云本地”的更正式的定义。

容器是 CNCF 提出的应用和服务标准的关键组成部分，这些应用和服务在公共云和私有云上本地运行，并在两种环境之间无缝移动。CNCF 将为其参考实现创建代码，而不是先在纸上写规格，然后基于规格实现代码。CNCF 成员谷歌捐赠了其 Kubernetes 容器编排系统，并将受益于该基金会对私有云和混合云的支持，这是该公司目前缺乏的技术。

## 云原生的持续发展

人们很容易将云原生应用的定义局限于这两个主要特征:与基础设施分离，以及可在节点间上下扩展。如果这种方法让你觉得过于简单，你并不孤单。《信息周刊》的 Charles Babcock 在 2015 年 7 月 30 日的一篇文章中解释说，云原生的关键是微服务——他称之为“离散应用服务”——在自己的容器中运行，并通过网络连接以创建定制应用。结果是一个“用户驱动的系统”的环境，它由标准化的部分组成，并由“标准化的部署和操作过程”管理。

根据 engineered via[slide share](http://www.slideshare.net/RichardHarvey7/micro-services-and-containers)的理查德·哈维所说，微服务和容器的结合推动了应用堆栈，简化了所有类型计算环境中的部署。

巴布科克表示，公司的回报还很遥远，但最终云原生应用将使公司专注于他们的客户，因为软件景观正在改变。这通过持续部署和交付“全新”软件转化为竞争优势。