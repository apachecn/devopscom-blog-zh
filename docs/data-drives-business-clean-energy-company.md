# 数据如何推动清洁能源公司的业务

> 原文：<https://devops.com/data-drives-business-clean-energy-company/>

想象一下，用煤油灯照亮夜晚的道路，在家里你可以做饭、阅读、淋浴，孩子们可以做作业，或者在外面保持商业或医疗中心的营业，或者在公园或田野里玩夜间游戏。这就是不发达国家的生活。不仅光源不足，而且烧煤油对个人健康有害，污染空气。

这些问题对 BBOXX 的团队非常重要，BBO xx 是一家为发展中国家开发清洁可再生太阳能产品的新一代公用事业公司。其团队开发了自己的“电池盒”，这是一种太阳能电池盒，为非洲农村的灯和电器供电——为众多产品和电器提供清洁能源，包括电视、灯和手机以及任何其他点亮或需要供电的物品。

BBOXX 将自己描述为一家服务公司，而不是一家技术公司，因此专注于成为一家数据驱动的公司，捕捉客户数据，分析和处理这些数据，以提供更好的服务，并继续改进电池盒。客户数据对其整体成功至关重要:了解客户购买和使用电池的方式和原因，他们使用电池的时间，时间长度…有许多数据点有助于 BBOXX 了解客户。此外，BBOXX 需要监控电池以确保它们正常工作，帮助保持连接，并在需要时禁用单元。

BBOXX 的开发团队通过远程监控设备来获取数据。他们能够访问传感器通过 2G 网络和亚马逊网络服务基础设施发送到云中的数据。一旦原始传感器数据进入 AWS，它就被存储在为度量和事件设计的数据库中。从这里，他们能够分析 it，提供业务仪表板，生成预测性维护警报和通知，并预测和发现有趣的业务趋势，例如足球比赛期间的能耗高峰。

此外，BBOXX 的团队还可以关联和汇总使用信息，这有助于他们根据即将到来的事件追加销售额外的电源容量。例如，肯尼亚和赞比亚之间的足球比赛增加了对更多能源的需求，以支持更长的观看时间。

成为数据驱动型企业意味着 BBOXX 需要访问其核心的实时数据，这带来了另一系列挑战:

*   安全监控低带宽 2G 网络中的一组分布式设备
*   为希望数据始终正确且可用的分布式团队提供 24 小时不间断的实时监控
*   提供对高速时序数据进行监控和反应的能力
*   远程监控和管理分布式设备的能力
*   能够跟踪使用统计数据，并根据这些统计数据进行计费
*   主动监控设备，以便在客户断电前进行维修
*   提供对客户使用模式的洞察，以制定有吸引力的定价计划
*   收集、协调和使用来自不同组件的三组不同数据:
    *   原始遥测数据(电压、电流、温度)
    *   来自机器固件的日志
    *   衍生数据(电力、日常能源使用、充电状态)
*   缺少管理其他解决方案的员工
*   将系统延迟保持在最低水平——他们的系统已经托管在 AWS 中，性能满足了公司的需求

BBOXX 现在能够洞察其数据，并应用从分析过去的数据中学到的经验来开发新的和令人兴奋的产品。该公司现在使用一种全新的方式存储数据:

*   开发人员分析数据，寻找创建新数据流的方法
*   分析师寻找使用中的异常情况，并编写算法来检测警报
*   业务经理寻找客户使用模式
*   技术人员分析用于远程诊断的时序电压和电流模式
*   集中式呼叫中心操作员通过查看停机原因(硬件故障、过度使用、不付款)来为客户解决更多的技术问题

此外，他们的投资者对他们的数据收集和分析非常感兴趣，将其作为竞争优势、减少拖欠、增长潜力和降低风险的标志。

BBOXX 使用 Amazon Web Services (AWS)来接收商店并分析其稳步增长的产品组合。通过在设计软件架构时考虑到可扩展性，BBOXX 利用了广泛的 AWS 集成功能，包括负载平衡、自动扩展组和代码部署，以保持快速、可靠和一致的内部和外部访问。

如果无法访问用户数据，BBOXX 将无法提供它今天所提供的独特服务，这是一种完全垂直集成的服务，控制着客户体验的每个部分。

## 关于作者/马克·海岭

Mark 是一名热情的营销人员，他相信营销成功之路总是由开发商引领。在加入 InfluxData 之前，Mark 曾在 Hortonworks 担任企业营销和开发者营销副总裁，在 Software AG 担任产品副总裁 s VP，在 Sun Microsystems 担任中间件、Java 和 MySQL 营销副总裁，在 Forte Software 担任营销副总裁。在职业生涯的早期，Mark 是 Oracle 的开发人员和技术支持工程师。Mark 拥有南非威特沃特斯兰德大学的理学学士学位。在 [LinkedIn](https://www.linkedin.com/in/herringmark) 上与他联系，在 [Twitter](https://twitter.com/markrherring?lang=en) 上关注他。