# LightStep 推出面向微服务的 APM

> 原文：<https://devops.com/lightstep-unveils-apm-microservices/>

各种形式的应用性能管理(APM)平台已经存在了一段时间。但是随着微服务的兴起，许多 IT 组织发现传统 APM 平台的设计无法处理软件模块的数量或这些模块的更新速度。但是 LightStep 是一家由前谷歌员工创办的初创公司，拥有 2900 万美元的额外资金，它将自己定位为第一个从头开始为微服务环境编写的 APM。

LightStep 首席执行官 Ben Sigelman 表示，无论软件模块和组件部署在哪里， [LightStep [x]PM](http://www.marketwired.com/press-release/founded-ex-googlers-lightstep-emerges-from-stealth-redefines-application-performance-2240535.htm) 都能够监控和排除所有网络和移动客户端、单片和微服务的性能问题。

他说，对 LightStep [x]PM 的大部分需求主要是由基于 Docker 等容器的微服务驱动的。但是 APM 平台本身可以支持微服务和传统的单片应用程序。Sigelman 说，随着组织转向微服务，同时继续需要支持在生产环境中运行的现有遗留应用程序，这为合理化 APM 平台创造了机会。

Twilio、Lyft、Yext、GitHub 和 DigitalOcean 已经在使用 LightStep [x]PM，这可以追溯到 Dapper，这是一个始终在线的分布式跟踪系统，由 Sigelman 在谷歌的生产环境中开发。分散式架构使 LightStep [x]PM 能够持续分析所有服务的 100%事务。然后使用统计引擎来检测异常，APM 可以记录并重放这些异常，作为基于 OpenTracing 的端到端跟踪功能的一部分，open tracing 是 Sigelman 和其他人共同创建的开放式 API 标准，现已成为由云本地计算基金会(CNCF)管理的项目。

LightStep [x]PM 中嵌入的其他功能包括支持服务网格和负载平衡技术，如 Envoy、linkerd、nginx 和 haproxy。

随着企业计算的每一个新时代，LightStep 等初创公司和现有技术平台提供商之间都会展开一场竞赛。LightStep 显然试图在 APM 平台的现有提供商能够添加对微服务的支持之前填补空白。现任者偶尔会依靠他们自己的有机努力来升级他们的平台，但更多的时候他们会收购一家初创公司，然后花几年时间试图统一不同的代码基础。

当然，有许多组织才刚刚开始他们的 DevOps 之旅。他们中的许多人可能没有任何类型的 APM 平台。大多数产品对成本也很敏感，所以基于开源代码的产品更有吸引力。

无论 APM 战争如何发展，很明显他们即将进入一个新的阶段。这些战争的赢家和输家将由 DevOps 团队决定，而不是试图强加一个自上而下的框架的 C 级 IT 高管。毕竟，如果说 IT 组织在过去几年中学到了什么，那就是 DevOps 在自下而上时往往会产生更持久的影响。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)