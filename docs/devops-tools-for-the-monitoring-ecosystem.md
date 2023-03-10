# 用于监控生态系统的 DevOps 工具

> 原文：<https://devops.com/devops-tools-for-the-monitoring-ecosystem/>

DevOps 是一种文化和过程的转变——它的目标是实现更高的软件变更率和质量。有多种工具可以通过自动化和增强的度量和可见性来帮助促进这种转变。没有度量，你就无法拥有或观察到进展，在整个转变过程中，你需要保持高度的可见性，以便快速、安全地前进。对于许多组织来说，不仅文化和过程转换的想法令人生畏，采用工具来帮助您完成这一旅程更是如此，因为它需要大量的学习。

一套集成的 DevOps 监控工具能够提高可见性和工作效率，实现更高性能的系统，并建立跨职能协作。正确的工具集不仅仅是工具本身——它是关于发展定义你的产品/服务和工作场所的文化、规则和实践。

本文将概述一些关于监控生态系统的最佳 DevOps 工具和实践，帮助开发人员和运营团队有效地合作。

## **监控工具**

一个好的监控平台可以让您监控基础设施和应用程序的性能，无论是在本地、云中还是在集装箱化的环境中，因此您可以随时全面了解每个系统。无论您想要监控 Kubernetes、物联网设备还是裸机，合适的监控工具都有助于实现这一目标。

有效的监控工具可以提高系统性能和工作效率，并帮助您减少停机时间。您可以充分规划升级和新项目，更好地分配时间和资源。您可以在问题影响用户之前发现并解决它们。

有很多很棒的监控工具；这里就不一一赘述了，重点说一下人气排名前三的。

不管你喜不喜欢，Nagios 仍然是一个被广泛使用的工具，并为我们今天所知的监控奠定了基础。再加上，[Nagios 的服务检查其实是牛逼的](https://blog.sensu.io/the-story-of-nagios-plugin-support-in-sensu) (而且不被重视)。然而，Nagios 的不足之处在于大规模监控短暂的环境，比如 Kubernetes 和 Docker。事实上，Nagios 在任何环境中的大规模监控方面都有所欠缺，无论环境是否是虚拟化的。进入 Prometheus，一个开源监控工具(和 Kubernetes 一样，是 CNCF 的一部分),它使用基于拉的架构。它不是将指标推送到监控工具，而是从服务中提取指标。由于 Kubernetes 内置的导出器，Prometheus 通常是监控 Kubernetes 的首选，但在监控较旧的基础设施时，它就显得力不从心了(更多关于 Prometheus [的优缺点，请参见这里的](https://blog.sensu.io/monitoring-kubernetes-docker-part-2-prometheus) )。

这让我想到了 [Sensu](https://sensu.io/) ，它提供了两全其美的功能:在 Sensu 中，您可以重用 Nagios 服务检查，并大规模监控短暂的环境。如果你有一个严格基于容器的环境，那么 Prometheus 是一个不错的选择；如果您有多代基础架构的组合(我们在客户那里经常发现这种情况)，那么 Sensu 就是合适的选择。

## **配置管理工具**

配置管理工具允许您自动配置和部署系统，强制执行所需的配置，并纠正配置偏差。通过将您的 [基础设施建模为代码](https://blog.sensu.io/infrastructure-as-code-testing-and-monitoring) ，您可以将版本控制、自动化测试和持续交付等软件交付实践应用于基础设施和应用程序。

将过去手动、重复且容易出错的工作自动化，可提高速度、可预测性和可扩展性，并确保跨测试、开发和生产环境的标准化配置。消除雪花服务器减少了时间(和麻烦),让您更快、更可靠地部署软件。

流行的配置管理工具包括:Ansible，它是用 Python 编写的，无代理，利用命令式(与声明式相反)方法。Puppet 是另一个流行的选择——它依赖于声明式配置管理方法，并使用特定于领域的语言和代理/主架构。最后，还有 Chef，它是用 Ruby 和 Erlang 编写的，建模类似于 Puppet。

## **报警工具**

警报工具提供可操作的和信息性的系统警报，并且可以定制以适应系统的复杂性。例如，您的警报系统需要足够敏感，以覆盖停机，但又不能太敏感，以至于您捕捉到用户不会看到的频繁、间歇性的问题，而这些问题会让您收到大量不必要的警报。

警报工具有助于为您的警报策略奠定基础，因此您可以确定通知谁、如何跟踪问题和结果以及如何确定补救的优先顺序。流行的工具包括 PagerDuty，它提供了一个随叫随到的管理平台，带有用于分析、事件智能和自动化事件响应的插件。还有 ServiceNow，它利用自动化的 ITSM 工作流以及客户服务和业务流程。您可以 [将您的警报发送到 Slack](https://docs.sensu.io/sensu-go/latest/guides/send-slack-alerts/) 以将警报整合到您用于与团队协作的同一个平台中。

## **指标存储**

一旦您实现了配置管理、警报和监控的自动化，您将拥有大量可供学习的数据。挑战:如何安全地存储和分析它？您需要一个存储系统，让您能够从系统容量、用户行为、服务级别、安全风险等方面进行汇总和学习。

您从指标中获得的洞察力为您业务所有层面的决策提供了信息，提高了您满足服务级别协议、满足客户期望以及进行新战略投资的能力。数据驱动的决策促进了持续学习和改进的文化。

用于存储指标的流行工具包括 InfluxDB 和 TimescaleDB、非常适合长期存储的时序数据库(TSDBs)以及 Splunk，后者使用搜索引擎数据库模型来存储和查询您的数据。Amazon Web Services (AWS)支持广泛的存储用途，包括关系和非关系数据库、用于分析的数据仓库、TSDB、用于存储事务的 leger 数据库等等。

## **可视化工具**

可视化工具可以被视为 DevOps 工具链中用于监控的支柱:您可以组合所有数据，对其进行排序和可视化，并将其显示在可定制的仪表盘上。

可视化工具提供了背景和意义，使您能够跟踪一段时间内的变化和改进，并为管理层提供有助于指导战略决策的实时视图。定制选项使团队成员可以轻松设计和共享他们自己的仪表板。

Grafana 是一款流行的开源可视化工具，可用于各种不同的数据存储之上，包括 Graphite、InfluxDB 和 Elasticsearch。有关 Grafana 如何与您的监控和 TSDB、 [集成的更多信息，请查看此用例](https://blog.sensu.io/how-to-measure-every-api-call-in-your-go-app) 。

## **评估您的 DevOps 工具**

无论您处于开发运维之旅的哪个阶段，明智的做法是重新评估您正在使用的工具，并找出可以微调的地方。考虑监控生态系统中的 DevOps 工具，不仅仅是它们的功能。你如何使用它们开始定义你的习惯、价值观和工作文化——相应地，你的产品或服务的质量以及你给用户带来的价值。

— [Sean Porter](https://devops.com/author/sean-porter/)