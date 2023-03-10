# 消除影子操作

> 原文：<https://devops.com/eliminating-shadowops/>

如果你像我一样，你会认为云和计算虚拟化技术正在改变数据中心，但与我们即将面临的情况相比，它们根本不算什么。随着应用程序容器、网络和存储虚拟化、大数据以及集成和超融合基础架构的出现，IT 环境正在加速演变。IT 和业务部门在基础设施和应用程序支持和管理方面的角色也在发生变化；推动对传统 IT 行动手册中没有的解决方案的需求。

竞争激烈的在线市场给企业带来越来越大的压力，要求他们更快地向市场提供服务和应用程序更新。虽然现在越来越多的注意力集中在应用程序本身，但事实是它们依赖于基础架构才能交付给最终用户或客户。传统 IT 运营在交付所需基础设施方面的不灵活性阻碍了开发团队满足服务交付速度的需求，从而导致 ITOps 和开发团队之间的差异。

如今，云服务提供商提供的基础设施资源被应用程序/服务所有者和开发团队视为一种更快速、更灵活的方式来获得应用程序和服务交付的基础设施。当业务单位和开发团队开始规避传统的 IT 运营，以获得满足快速发展的需求所需的敏捷性时，就产生了我所说的影子运营。

ShadowOps 的特点是外包基础架构和服务的秘密扩散，这进一步阻碍了 IT 和开发运营之间的关系，并带来了风险，影响了从治理和合规性到业务连续性灾难恢复、服务质量等方方面面。

**了解影子作战**

应用程序/服务所有者和开发人员运行其应用程序所需的基础架构由 IT 运营部门提供支持和管理。企业认为 IT 运营是一个障碍。他们太慢，太不灵活。这导致企业寻求外部基础设施，于是影子运营战略诞生了。

ITOps 负有满足某些要求的巨大责任，如监管或安全审计，同时还要确保有灾后恢复和业务连续性计划和系统；本质上是为任何事情和任何可能发生的事情做计划。

另一方面，开发人员生活在业务单元中，通常不了解 it 运营部门每天都在做些什么，或者他们的操作如何影响他们的过程和需求。

虽然开发人员通常可以每天交付多个版本，但他们在测试、开发、QA 和预生产过程中几乎不受限制，一旦他们进入生产环境，IT 运营人员通常不会察觉新的或更改的应用程序行为和底层基础架构要求，并且通常会忙于交付新的和更改的应用程序所需的内容。

这导致受影响的开发人员开始寻找能够给他们带来他们渴望的便利和速度的基础设施解决方案。所以他们去 Rackspace，或者亚马逊，或者微软 Azure，简单地购买他们需要的基础设施来支持他们的应用程序，并按月付费。

当开发人员和应用程序所有者开始外包基础架构时，通常很少考虑风险，他们往往会忽略合规性要求、审计等事项，以及简单的更改可能会严重影响 IT 运营这一事实。

IT 运营部门承受着某些法规要求和公司政策的压力，这使得他们在应用程序所有者的眼中显得“缓慢”。外部基础架构对应用程序支持和开发运维团队极具吸引力，因为云服务提供商可以快速调配和交付所需资源。

IT 运营还受到传统监控系统的拖累，这需要大量的手动工作。不仅有单独的工具来监控存储、数据库、网络和中间件，现在有了 ShadowOps，还有单独的基础架构，而且 IT Ops 对外部资源的洞察力或控制力极其有限。他们往往甚至不知道他们的存在，直到有人打电话到服务台无法获得他们的应用程序或无法处理交易。这是事情开始失控的时候。

影子行动的诱惑和后果

ShadowOps 对开发人员很有吸引力，原因有几个:更好的价值实现时间、上市时间、敏捷性、速度、响应能力，这些都是好东西，直到它们开始影响可用性或增加风险，并且没有灾难恢复或业务连续性或 it 运营方面的审计能力。当开发人员购买云服务提供商的产品而不是通过 IT 渠道工作时，您必须与多个提供商打交道——项目管理受到影响，成本失控，并且您无法实现规模经济。

因此，如果每个业务单元或开发团队独立地走这条路，您必须问自己:他们满足业务连续性需求吗？他们有冗余吗？他们是否定期备份？他们记录了所有需要的东西吗？他们是否控制哪些管理员有权访问某些系统？最后，它会通过审核吗？提供商将如何提供访问权限？

ShadowOps 环境的后果不仅是有多个提供商，而且还缺少一个负责协商响应率和 SLA 以满足其业务部门需求的人员，因此当出现安全问题时，没有人在一定时间内做出响应来解决问题。

**统一、自动化和增强 IT 能力**

那么，您如何消除影子操作，为开发人员提供所需的敏捷性，同时增强 IT 能力呢？

首先，让中央 It 部门的开发人员能够利用更好的工具来满足不断变化的 IT 环境的需求，从而实现更好的协调。

为 IT 运营提供统一、自动化的性能和可用性监控工具，采用单一用户界面和单一数据存储，以及针对整个基础架构(无论部署在何处)的事件管理，这是朝着克服导致影子运营的障碍迈出的一大步。

借助自动构建和更新的统一模型，您将始终能够监控整个 IT 环境的最准确视图，控制成本，促进资源共享，并允许不同部门做出更好的采购，以满足不断发展的业务需求。

ShadowOps 环境的一个关键症状是缺乏灵活性的 it 运营组织，在这种组织中，IT 通过严格的服务和 SLA 菜单控制内部的一切，开发人员被迫处理这些服务和 SLA 以满足他们的要求。通过利用统一的监控解决方案，您可以使 IT 能够适应和放弃一些控制，并促进与开发人员的共同基础，使 IT 成为推动者而不是执行者。

如果业务部门希望使用外部提供商，it 运营部门可以帮助他们选择合适的提供商，分配项目负责人，帮助他们设置项目，并使其在正确的控制下工作。

然后，IT 人员可以自由地咨询业务和开发团队，指导他们做出更好的采购，并对其环境有更多的控制，有可能将多个业务部门的需求与一个专门从事他们实际需要的基础架构的特定提供商相结合。

IT 运营，以及 X 即服务(基础架构、平台、软件等。)，允许更大的灵活性，以支持快速原型和交付。它允许 It 成为开发团队的技术推动者，而不是迫使他们仅仅依赖于他们现有的基础设施，并且不可避免地寻求影子操作。

有关如何通过利用统一的监控工具来消除影子运营，从而使 IT 运营更加敏捷并满足开发团队不断发展的需求的更多信息，请点击此处阅读我们关于整合 IT Ops 和 DevOps 的完整报告。