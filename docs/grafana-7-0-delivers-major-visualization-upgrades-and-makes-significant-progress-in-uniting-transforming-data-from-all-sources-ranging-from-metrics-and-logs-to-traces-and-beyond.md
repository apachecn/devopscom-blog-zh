# Grafana 7.0 提供了主要的可视化升级，并在统一和转换来自所有来源的数据方面取得了重大进展，从指标和日志到跟踪等等

> 原文：<https://devops.com/grafana-7-0-delivers-major-visualization-upgrades-and-makes-significant-progress-in-uniting-transforming-data-from-all-sources-ranging-from-metrics-and-logs-to-traces-and-beyond/>

今天，Grafana Labs 宣布 Grafana 7.0 的正式上市，它具有显著的增强功能，可以简化定制插件的开发，并大幅提高可视化的能力、速度和灵活性。最新版本帮助组织更快地实现他们的监控、可视化和可观察性目标。开源 Grafana 是世界上最受欢迎的仪表板解决方案之一，拥有超过 500，000 个活跃安装和全球使用的数百万个仪表板。Grafana 7.0 是从 6.0 开始的努力的积累，跨越了来自全球 362 个贡献者的近 18，000 个提交和 3，699 个拉取请求。此外，还有数百个公司、商业和社区数据源插件以及数千个示例/入门仪表板，支持用户在内部和云中的需求。

Grafana 7.0 增强功能非常注重在以下关键领域为用户和组织提供帮助:

*   **(更容易)连接和统一您的所有数据**
    *   谷歌(Stackdriver/Cloud Monitor)、微软(Azure Monitor)和亚马逊(Cloudwatch)之间的合作带来了新的插件，加上开源 Loki 的日志支持以及 Zipkin 和 Jaeger 的跟踪输入。这些扩展了 Grafana 现有的社区和企业商业插件，从 Prometheus、Graphite 和 Elasticsearch 等流行的开源项目到 Splunk、Datadog、New Relic、Zabbix、Oracle、ServiceNow 等专有资源，还包括您自己的定制数据源/API。
    *   基于 Apache Arrow 的新组件库、工具、数据结构和完全重建的通用统一数据和插件框架提供了一致的数据结构，并显著减少了开发插件所需的工作量。

*   **(更强大的能力和控制力)处理和转换您的数据**
    *   以前在许多面板或数据源中作为自定义功能复制的一组共享的公共数据操作现在是 Grafana 数据处理管道的一个组成部分，所有数据源和面板都可以利用。
    *   转换包括重命名、汇总、组合和执行不同面板中的计算，将时间序列标签放入列中，在其他面板中重用和细化查询结果，等等。
    *   新的数据检查功能允许用户查看、导出(CSV)面板的基础源数据，并对其执行简单的转换。他们还可以深入查询执行细节，以便更快地进行故障排除。

*   **(更快的方式)可视化您的数据…甚至跟踪**
    *   一个新的跟踪查看器补充了对度量和日志的现有支持，使用户能够通过分布式系统跟踪单个请求的路径。
    *   一系列自动化且易于使用的渲染选项极大地简化了工作，并以各种格式生成仪表板面板，包括表格、非时间序列图表等。这扩大了现有面板插件的重要库，包括地图、饼状图和仪表。
    *   新的面板选项，新的编辑体验，新的表格面板以及更容易调整大小。

*   **使用新的企业功能搜索、发现和保护您的仪表板**
    *   Okta 和 SAML 团队同步。
    *   针对使用趋势的现成搜索和仪表板报告，可更轻松地识别非活动和受欢迎的仪表板。
    *   能够识别并发仪表板用户，以实现更快的协作。

“我迫不及待地想把它交到我们用户的手中。对我们来说，这是一个真正的重大发布——不仅仅是一个. 0 或一系列功能，而是一个根本性的、系统范围的进步。在这个版本中，用户将体验到可视化速度的提高，以及大量的功能，这些功能将为他们提供一个位置，在用户级别上对他们的数据执行简单和复杂的功能和转换。例如，通过链接一组简单的点击转换，用户将能够连接、过滤、重命名和计算以获得他们需要的结果。Grafana 正在成为一个理想的工具，可以加速和简化基本的数据转换，并减少通过仪表板外的各种查询语言执行脱节转换的需要。”—to rkel dega ard，Grafana 的创始人，Grafana Labs 的联合创始人和 CGO

“我们认为供应商不应该拥有可观察性策略；用户和组织需要。我们专注于帮助他们通过一个开放的可组合框架来统一组织的复杂环境，从他们自己的自定义 API 和开源指标(如 Prometheus 或 Graphite 和 Loki for logs)到合并开源和专有系统(如 Elasticsearch、Datadog、Splunk、Oracle 和 ServiceNow)。”— Raj Dutt，Grafana Labs 联合创始人兼首席执行官。

Grafana 云客户可以立即获得 Grafana 7.0，或者通过 30 天免费的[云试用](https://grafana.com/signup/cloud/select-org)和[下载](https://grafana.com/get)获得。

来自几个 7.0 预览博客/推文的参考链接:

**新历史探索者:**【https://twitter.com/grafana/status/1255891305525362689】https://grafana . com/blog/2020/04/30/grafana-7.0-先睹为快-查询-历史探索/ (推文:)

**新的表格面板**

[https://grafana . com/blog/2020/04/28/grafana-7.0-sneak-peek-new-table-panel-for-dashboards/](https://grafana.com/blog/2020/04/28/grafana-7.0-sneak-peek-new-table-panel-for-dashboards/)推文:【https://twitter.com/torkelo/status/1254027987323965441】T2

**新的自动网格布局**

[https://grafana . com/blog/2020/04/23/grafana-v 7.0-is-coming-soon-check-out-this-snow-peek-of-the-auto-grid-layout/](https://grafana.com/blog/2020/04/23/grafana-v7.0-is-coming-soon-check-out-this-sneak-peek-of-the-auto-grid-layout/)(推特:【https://twitter.com/grafana/status/1253370370914242560】T2

**新图标:**

[https://twitter.com/grafana/status/1256317203214991362](https://twitter.com/grafana/status/1256317203214991362)