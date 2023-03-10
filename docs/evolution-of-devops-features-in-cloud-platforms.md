# 云平台中内置 DevOps 功能的演变

> 原文：<https://devops.com/evolution-of-devops-features-in-cloud-platforms/>

如今，DevOps 正被许多 IT 组织广泛采用。这样的 IT 组织变得更加敏捷和可靠，更频繁地部署代码，错误和失败更少。DevOps 有助于获得更好的 IT 性能并建立额外的竞争优势，拥有高绩效 IT 组织的公司超越其盈利能力、市场份额和生产力目标的可能性是其他公司的两倍。

DevOps 的采用受到多种因素的推动，如敏捷开发方法、显著提高的产品发布率、公共和私有云平台的广泛选择，以及用于数据中心自动化和配置管理的各种工具。

如今，市场上有许多不同的自动化工具供 DevOps 团队用于供应、编排和配置管理(Puppet、Chef、CFengine、bcfg2、vagger、Fai、Kickstart、Preseed、Cobbler)，用于构建和部署自动化(Jenkins、Maven、ant、Cruisecontrol、Capistrano)，用于基础设施监控(Zabbix、Nagios)和应用性能测量(NewRelic、AppDynamics、DripStat)。

然而，IT 组织仍然难以帮助开发人员和管理员优先考虑两个完全不同的目标——应用程序开发速度和功能完成与生产稳定性和正常运行时间。自动化工具供应商推广他们的产品以解决开发运维团队的挑战，但仍然经常无法面对运营工程师工作流的复杂性，或者开发人员期望的应用发布和部署速度。

另一个问题是，有应用程序发布和部署问题的 IT 组织通常使用某种自动化，但他们希望有更大的灵活性来管理他们的自动化，而不需要在命令行手动调用一切。理想情况下，这种自动化应该在开发环境中对开发人员可用，以便开发人员能够更好地控制环境和理解基础设施的使用。

这些问题推动了 DevOps 工具的发展。如今，云平台供应商将自动化和管理工具直接整合和集成到他们的云平台中。因此，IT 组织可以在同一个全包式云平台中获得更好的自动化功能。我们可以宣称 PaaS 解决方案将成为下一代 DevOps 工具。云平台已经不再需要担心虚拟机/容器的供应和配置管理的许多方面。这些云平台以非常高效的方式解决了这个问题，因为它们对资源和事件有更多的控制权，它们管理整个资源集群，同时考虑不同的指标和状态指标。因此，这些平台提供了更高的资源密度、更好的利用率、跨集群的智能负载分配、新版本部署的自动化、可扩展性和维护的自动化、开箱即用的高可用性和容错功能。

事实上，许多 IT 组织使用 Puppet 和 Chef 等自动化工具来解决模板管理、更新中间件堆栈、应用程序配置管理和新版本零停机部署的挑战。然而，最新的云解决方案包括更多旨在解决相同任务的“原生云”功能。有许多例子表明，云平台正朝着这个新的 DevOps 方向发展，在流行的云平台中提供原生自动化功能。

让我们以云计算行业的远见者之一——亚马逊网络服务为例。他们的云服务之一 cloud formation([http://aws.amazon.com/cloudformation/](https://aws.amazon.com/cloudformation/))允许开发者和管理员创建和管理资源、中间件堆栈和应用程序模板。它有助于管理已配置资源和应用程序的配置和更新。从字面上看，它的设计是为了解决与木偶和厨师相同的任务。您可以找到许多与 CloudFormation 与 Puppet/Chef 的比较相关的线程讨论。ops works(【http://aws.amazon.com/opsworks/】T2)是另一项应用管理服务，简化了应用部署和生命周期管理。它有助于定义应用程序拓扑、软件包安装规范以及软件和资源配置。此外，该服务包括基于时间或负载的自动化扩展，并允许编写这些任务的脚本。

DevOps 进化的另一个好例子是 Google 云平台发布的新云服务。最近，这个公共云平台发布了几个不同的功能，帮助解决与上述类似的任务——副本池([https://developers.google.com/compute/docs/replica-pool/](https://developers.google.com/compute/docs/replica-pool/))、启动脚本[https://developers . Google . com/compute/docs/how tos/Startup script](https://developers.google.com/compute/docs/howtos/startupscript)和云部署管理器[https://developers.google.com/deployment-manager/](https://developers.google.com/deployment-manager/)。这些本机集成的云工具提供了从通用模板创建和管理虚拟机(VM)集、调整其大小、更新或删除它们、定义不同的配置属性(如基本映像、连接的磁盘详细信息、连接的网络对象和启动后要执行的脚本)、安装新软件和更新、定义虚拟机启动时持续可用的环境/操作系统变量的能力。此外，它还提供了使用简单的模板机制轻松声明、部署和维护复杂应用程序的能力。它调配、扩展和监控虚拟机和应用程序。此外，它还可以执行定期运行状况检查，并可以重启或重建无法正常响应的虚拟机集。最近公布的云调试器和云跟踪([http://Google Cloud platform . blogspot . com/2014/06/enabled-developers-to-tame-production-systems-in-the-Cloud . html？UTM _ source = feedburner&UTM _ medium = Feed&UTM _ campaign = Feed % 3A+CLP LBL+% 28 cloud+Platform+Blog % 29](https://googlecloudplatform.blogspot.com/2014/06/enabling-developers-to-tame-production-systems-in-the-cloud.html?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+ClPlBl+%28Cloud+Platform+Blog%29))允许开发人员只需在一行代码上设置一个观察点，就可以获得所有局部变量、参数、实例变量和完整堆栈跟踪的快照。它有助于快速识别和修复性能瓶颈，并使工程师能够通过详细的报告比较不同版本的性能。它的运行时间为零，没有复杂的配置，适合在生产中使用。上述工具涵盖了大量的 DevOps 任务。

docker([http://www.docker.com/](https://www.docker.com/))是紧密集成的云自动化机制的另一个好例子，也是 DevOps 发展的又一个例子。该自动化解决方案的承诺和重点是消除不同环境中配置和部署的复杂性。许多云供应商已经宣布与 Docker 集成。许多观察家认为，Docker 仍处于早期阶段，尚未准备好投入生产，但该产品已经引起了业界的广泛关注，该技术似乎意义重大。

此外，在 DevOps 发展中还有更大的事情——统一云自动化的开放计划，即云应用的拓扑和编排规范(https://www.oasis-open.org/committees/tc_home.php?，TOSCA)wg_abbrev=tosca 。TOSCA 的目标是增强云应用和服务的可移植性，实现云服务的可互操作描述以及云服务各部分和操作行为之间的关系。例如模板配置和供应、应用程序部署、软件补丁和更新、应用程序扩展和维护等。换句话说，它推动了独立云平台供应商或云托管服务提供商的统一标准。因此，it 应该通过创建一个供应商中立的生态系统来简化开发运维团队的工作和任务，从而支持向任何兼容云平台的可移植部署、现有应用向云的平滑迁移以及构建和运行多云提供商应用的能力。

总之，未来将会带来更多针对 DevOps 需求的不同自动化特性的云原生吸收。云平台向 DevOps 方向的演进对 IT 组织极为有利，因为他们不需要管理和学习不同的自动化工具和方法。这种不必要的复杂性将被同一云平台内不同自动化功能的无缝集成所取代。这意味着在不久的将来，Puppet 和 Chef 等非常受欢迎的 DevOps 工具将与云平台的内置功能相竞争。

但是，在演进期，选择合适的云平台至关重要。它应该允许 It 组织使用多种方法-旧的遗留自动化方法和新的本机功能，以通过内置自动化和已收集的知识库提供最大的灵活性。选择的灵活性是 IT 组织发展 DevOps 的关键点，即同时使用两个领域的能力:旧的自动化工具和云平台的下一代功能。

此外，提到 PaaS 和 IaaS 之间的无缝集成对于 DevOps 发展的重要性也是有意义的。上面讨论的公共云平台(AWS 和 Google Cloud)今天提供了合并的解决方案。这两层的集成对于大量使用私有云和混合云的企业非常重要，因为它取代了两种不同解决方案不必要的维护复杂性，并消除了集成不同供应商产品的额外开销。换句话说，合并 PaaS 和 IaaS 在同一个解决方案中提供了极大的自动化灵活性和易用性。无缝云平台在同一个全包式云解决方案中提供了自动化功能的最佳组合，有助于推动创新和维护传统应用。

下一代云平台将在开发部门和运营部门之间建立双赢关系，当开发部门和运营部门互动的结果是双赢时，IT 组织的绩效也是双赢。

[![ruslan4](img/a33270b7c4c0d21244cc155b9f53b848.png)](https://devops.com/wp-content/uploads/2014/07/ruslan4.jpg)

**关于作者**

Ruslan Synyntsky 是 Jelastic 的创始人兼首席技术官。Ruslan 在 IT 行业从业超过 15 年，是大规模分布式 Java 应用程序和企业平台方面的专家。在建立 [Jelastic](http://www.jelastic.com) 之前，他领导了工程团队 a 和在太空总署、Ukrainet iQueLab、SolovatSoft、Datamesh。