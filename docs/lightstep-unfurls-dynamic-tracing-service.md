# LightStep 展开动态追踪服务

> 原文：<https://devops.com/lightstep-unfurls-dynamic-tracing-service/>

LightStep 宣布了一项独立的动态跟踪工具功能，该功能可以基于 100%的可用数据来可视化代码中的模式。

公司首席执行官本·西格曼说 [LightStep Tracing](https://globenewswire.com/news-release/2019/03/04/1745655/0/en/LightStep-Tracing-Shakes-Up-Microservices-and-Serverless-APM-and-Observability.html) 不同于其他追踪方法，因为它不依赖于小样本数据，这些数据通常不会提供多少可操作的见解。相反，LightStep 跟踪可以搜索和可视化软件即服务(SaaS)应用程序提供的 100%数据的分布式跟踪。

![](img/06bf402afe08f1fe4f43e16600fce753.png)在 [QCon London 2019](https://qconlondon.com/) 大会上发布，LightStep Tracing 基于最初在应用性能管理(APM)平台中开发的功能，称为 [LightStep [x]PM](https://devops.com/lightstep-unveils-apm-microservices/) ，针对基于微服务的应用进行了优化。然而，LightStep 跟踪并不要求 DevOps 团队实现 LightStep [x]PM 来利用分布式跟踪。

分布式跟踪正得到越来越广泛的应用，因为这种能力使得可视化潜在性能问题的模式变得更加简单。西格曼在谷歌任职期间创建了第一批分布式追踪实例之一。该项目被称为 Dapper，现在每秒钟可以分析超过 20 亿次交易。Sigelman 随后共同创建了 OpenTracing 应用程序编程接口(API)标准，该标准现在在云本地计算基金会(CNCF)的支持下可用。

根据 Sigelman 的说法，当今许多 DevOps 团队最常犯的一个错误是高估了分布式跟踪作为数据源的价值。Sigelman 补充说，虽然访问分布式迹线是必需的，但真正的价值来自能够以可视化方式动态检查所有可用迹线。Sigelman 警告说，DevOps 团队应该小心他们从基于数据样本的分析中得出的结论，因为可能对应用程序性能产生重大影响的异常值很容易被忽略。

LightStep 跟踪为开发运维团队提供了对动态系统图表的访问，这些图表直观地总结了瓶颈以及实时性能直方图，使组织能够了解是什么定义了其环境中的正常应用行为。Sigelman 表示，DevOps 团队还首次可以捕获可共享的系统行为快照，这些快照基于数千条相关跟踪的统计摘要来解释性能异常。Sigelman 说，在几分钟内，LightStep Tracing 就可以用于检测和可视化 web、移动、微服务、无服务器和单片应用程序之间的服务对服务交互。

DevOps 更令人沮丧的一个方面是，大多数团队将花费更多的时间寻找问题的根源，而不是修复它。但是，在确定问题的根源之前，IT 组织在应用程序所有者眼中的声誉会继续受损。还有一个不幸的趋势是，DevOps 团队在“作战室”花费了过多的时间，试图证明他们管理的 IT 环境的任何元素都不是问题的根本原因。与其以牺牲 IT 组织的声誉为代价浪费所有的时间，也许早在任何应用程序所有者意识到问题的存在之前，就应该发现问题并将其可视化。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)