# 新遗迹报告日志数据量激增

> 原文：<https://devops.com/new-relic-reports-major-spike-in-volume-of-log-data/>

新遗迹今天分享了一份基于其收集的匿名数据的[报告](https://newrelic.com/resources/report/2022-state-of-logs)，该报告显示其[可观察性](https://devops.com/?s=observability)平台收集的日志数据量增加了 35%。

该报告还指出，NGINX 代理软件生成的日志(38%)是最常见的日志类型，其次是 Syslog (25%)和 Amazon 负载平衡器(20%)。

此外，在已经采用 New Relic 平台的 it 团队中，Fluent Bit 是最常用的开源处理器和转发器工具(38%)。另外 16%使用 New Relic 基础设施代理，14%通过 HTTP 端点直接向 New Relic 发送日志数据。

该报告还发现，语言代理摄取的所有日志中有 50%来自 Java 应用程序，其次是。Net (26%)、Ruby (22%)和 Node.js (2%)。

New Relic 的开发人员关系总监 Jemiah Sius 表示，随着越来越多的云原生应用程序被部署，随着开源 OpenTelemetry 工具被更广泛地采用，收集的日志数据量只会增加。此外，IT 团队还将收集指标、痕迹和事件，以使用 New Relic One 等可观察性平台更好地查明问题的根本原因，他补充说。

当然，Amazon Web Services (AWS)现在是日志数据的最大来源之一。New Relic 报告指出，在使用 New Relic One 平台的 AWS 客户中，无服务器 AWS Lambda 服务是最广泛使用的日志数据源。然而，Sius 指出，AWS Firehose 服务在提取、转换和加载(ETL)数据方面的使用在去年急剧增长。

New Relic 报告发现，虽然只有 32%使用 AWS 的 New Relic 帐户采用了 Firehose，但采用率同比增长了 62%。

每当出现问题时，日志数据通常是任何 it 团队首先要参考的，但是随着日志数据量的增加，将日志数据与特定的 IT 事件相关联变得越来越困难。每个 IT 团队必须解决的问题是，要存储多少日志数据以及指标、跟踪和其他数据格式，以帮助他们主动识别 IT 问题的根本原因。

与此同时，可观察性平台承诺可以查询日志数据来识别事件之间的关系。Sius 表示，其目标是使 IT 团队能够在中断 IT 服务之前调查问题，而不仅仅是在事件发生后做出反应。

当然，希望是机器学习算法将很快在大多数 IT 团队知道有问题之前自动识别问题。鉴于现代 it 环境的整体复杂性，大多数 IT 团队甚至不太可能知道启动什么查询来确定问题的根本原因。相反，随着机器学习算法越来越熟悉构成正常 it 事件的因素，这些算法将更容易发现实际上值得 IT 关注的问题。