# SDN 和 NFV 的持续测试和监控要点

> 原文：<https://devops.com/continuous-test-monitoring-essentials-sdn-nfv/>

之前的博客[持续测试监控 DevOps Healthbeat](https://devops.com/2015/09/11/continuous-test-monitoring-devops-health-beat) 讨论了测试和监控测试趋势的重要性和建议做法。当被测试和监控的系统是诸如下一代软件定义网络(SDN)和网络功能虚拟化(NFV)系统的联网组件的协作应用、基础设施和设备的网络时，这种需求被放大。在网络系统中，任何网络组件(如最终用户应用程序、网络接口设备、网络控制平面、网络数据平面、负载平衡器、防火墙、网络管理、协调和网络虚拟基础设施)的问题都会严重影响用户和网络服务性能。组件的数量、种类、拓扑和版本及其主机环境为 DevOps 持续测试和监控带来了特殊挑战。

In an SDN and NFV world all production topologies and network variations must be tested and results must be monitored or the results will be uncertain. Despite the complexity, or perhaps because of it, continuous testing and monitoring must be optimized to ensure that testing and results analysis for each CI/CT cycle keep pace with accelerated continuous testing and longer term continuous test monitoring is necessary to assure overall delivery confidence for each release and longer term product performance trend in a positive direction. Individual test results or a fixed number of test campaigns can only tell you so much.

除非对所有网络节点和所有拓扑的测试和测试分析结果进行持续监控，并在多个测试和发布周期内汇总结果，否则无法对 SDN 网络和 NFV 组件的长期健康状况建立足够的可持续信心。拓扑感知的连续测试解决方案与可以在整个网络资源集合上聚集结果的连续测试监控工具的组合可以提供测试结果的长期战略视图，这是收集、聚集和组织测试结果数据以获得对每个版本和多个版本的演进的网络组件和服务的信心所必需的。

以下是清单格式的一些建议，已被证明对持续测试和监控可持续高性能 SDN 和 NFV 系统和服务非常有用。

1.  确定持续测试和监控的优先级:持续测试和监控可以帮助解决的一些问题包括由虚拟网络基础架构、虚拟网络功能、网络管理、协调和管理、第三方网络和最终用户系统兼容性、网络性能、网络容错功能引起的间歇性故障。持续测试和监控的最佳实践表明，将测试与特定网络系统或服务最相关的问题，并监控结果趋势。
2.  回归测试网络系统和服务，即使没有预期的变化:间接变化的意外后果可能会影响性能，因此自动回归套件应该偶尔审核所有生产网络测试拓扑和版本变化区域，以确保万无一失。这种情况下经常出现的典型例子是对审计功能很重要的功能、系统向后兼容性功能和升级/降级管理功能。

3.  选择收集和报告趋势的连续测试和监控工具:
    可以关联和报告多个网络节点和拓扑变化的测试结果的工具可以发现间歇性的错误或问题趋势。从长期结果视图中突出显示短期结果视图的阈值、电子邮件警报和控制面板尤其有价值。

4.  使用连续测试监控结果来诊断和解决问题:
    间歇性故障和问题只有在测试结果以长期趋势的形式呈现时才变得明显，当积累了大量数据集并通过最可能原因标签进行过滤时，这些故障和问题更容易诊断。一旦确定了诊断，就可以通过有针对性的重新测试案例来验证根本原因，这些案例根据诊断设置了所有条件。一旦得到确认，就可以重构有问题的设计来处理或避免失败的情况。

以上是持续测试监控的部分建议，已被证明可支持可持续 SDN 和 NFV 网络系统和服务。在思必驰和泽法，我们认为持续的测试和监控对于成功的开发至关重要。您可以通过查看我们的联合网络研讨会来了解我们对这一主题的更多看法:
[克服 DevOps 挑战](http://go.getzephyr.com/l/77632/2015-07-13/3zt2m?referer=Zephyr)

你对这些建议有什么看法，你还有其他应该提到的建议吗？

### 关于作者马克·霍恩比克 &桑杰·扎拉瓦迪亚

Marc Hornbeek 是思必驰通信基础设施测试优化(ITO)部门 DevOps 持续测试解决方案的高级解决方案架构师。他最近在 Spirent 管理 DevOps。他是测试自动化工具的主要架构师，也是从初创公司到大型跨国公司的测试自动化的倡导者。他发表了 30 多篇文章，并在许多会议和用户论坛上发表演讲，主要是关于持续自动化测试和 DevOps 的主题。

[![sanjay](img/b5ce2fae27edeebee282108976c4a987.png)](https://devops.com/wp-content/uploads/2015/10/sanjay-e1446002257337.png) 桑杰扎拉瓦迪亚负责在[【泽法】](http://www.getzephyr.com)驾驶定制成功。这包括培训、咨询、客户支持和客户管理。最近，作为 Patni Computers Telecoms IT Managed Services Practice 的助理副总裁，他建立了支持移动内容提供商的 IT 运营团队。Sanjay 在大型和小型公司的多个地区的 IT 和技术支持服务团队中拥有超过 15 年的领导经验。桑杰拥有印度马尼帕尔理工学院的研究生学位