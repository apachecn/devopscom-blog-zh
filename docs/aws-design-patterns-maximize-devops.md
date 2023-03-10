# 3 个 AWS 设计模式，最大化 DevOps 价值

> 原文：<https://devops.com/aws-design-patterns-maximize-devops/>

许多企业领导正计划将 DevOps 作为其 IT 转型战略的基石。但是，尽管听起来可能令人惊讶，但对于主要供应商如何解决 DevOps 转型挑战的怀疑态度比比皆是，他们将 DevOps 与连续交付(CD)基础架构混为一谈。

“我们想要 DevOps，在长达九个月的实施后，我们得到了一个连续交付平台，它在没有显著商业价值的情况下加快了 IT 运营。你能提供怎样不同的帮助？”三个月前的一次谈话中，纽约一家大型金融机构的高级业务主管讽刺地问我。

业务主管是对的:DevOps 不是我一直在实施的一项技术，它主要是一种加速的应用交付方法，以技术支持的应用交付运营模型的形式实施。Chef 的首席技术官亚当·雅各布(Adam Jacob)在“[DevOps 的秘密:它总是关于人，而不是技术](http://readwrite.com/2015/07/29/devops-people-not-technology/)”中证实了这一事实，他说，“devo PS 是关于将你需要建立和有效运营你的业务的所有人聚集在一起，并授权他们尽快朝着他们的目标前进。”

敏捷管理的 Ernest Mueller 在“ [DevOps:这不是厨师和木偶](https://theagileadmin.com/2012/04/02/devops-its-not-chef-and-puppet/)”中证实了 Adam 的观点:“厨师和木偶是单独的工具，如果你想使用它们，你可以用来实现整体 DevOps 策略的特定部分——但仅此而已。它们是很好的工具，但不能为您解决开发工作。”

我们如何实现 DevOps 以符合业务领导者的期望？我开发的三个亚马逊 Web 服务(AWS)设计模式可以帮助在 AWS 云上获得最好的 devo PS:**软件组织工厂**、**数字组织工厂**和 **CD 基础设施工厂**。本文讨论了软件组织工厂。

## DevOps 价值的基础:对 IT 服务交付的影响

在深入研究这些 AWS 设计模式之前，快速提醒一下 DevOps 是什么，它的价值主张，更重要的是，IT 服务交付方式需要哪些改变。

### 我们都必须考虑的被忽略的 DevOps 业务逻辑

云的采用和不断增长的数字经济的综合效应正在改变竞争环境；它迫使企业领导者将创新和市场响应能力作为竞争优势。

事实是，通过促进技术的获取，云加速了数千家科技初创公司的进入，这些公司利用最新的技术创新将传统产品和服务替代为数字产品和服务。这创造了一个新进入者越来越多地与老牌品牌竞争的环境，迫使企业领导者寻求价值范式而不是 IT 效率。

这位业务主管认为，“在这些新市场中，我们关心的是通过在正确的时间向正确的细分市场提供正确的服务来增加客户价值。你们需要改变 IT 范式；它本身并不能创造这种价值。”

那么，今天的 IT 方法应该改变什么？

### 现代 IT 的两个维度:操作模型和持续交付基础设施

在我最近的一本书《用 DevOps 重新思考你的 IT:使你的 IT 与 DevOps 保持一致的完整指南》中，新的 IT 范式主张商业价值来自两个维度:组织灵活性和技术效率。换句话说，它将现代 it 定义为二维资产，包括运营模型和持续交付基础设施。

创新的及时交付超越了 IT 问题；它不仅贯穿您的销售、市场营销、售后服务、应用程序开发和 it 运营，还要求您就如何加快业务优先级划分、决策和问题解决给出具体答案。在运营模式中，业务和 IT 人员、流程、实践和工具相结合，以创建灵活的跨职能环境。下图展示了典型的 DevOps 运营模式:

![Typical DevOps Operational Model](img/6cd9b896eea974e8e05df8e63847f13f.png)

Typical DevOps Operational Model

除非利用技术来加速过程，否则为了灵活性而组织灵活性是没有意义的。这就是裁谈会基础设施发挥作用的地方；在整个交付过程中，他们基于 ide 来加速编码和测试，基于版本化工具来将软件版本转换为版本，基于持续集成(CI)工具来构建版本，以及基于交付管道来确保持续交付。

那么，DevOps 是什么？

### DevOps 是一种基于技术的应用交付模式

DevOps 是价值、原则、流程和实践的组合，不仅由开发人员和 IT 运营部门共享，也由业务部门共享。目标是帮助组织在正确的时间向正确的细分市场提供正确的服务。

![DevOps from the Business Perspective](img/9f94e7b699eeba6795129f5303cac562.png)

DevOps from the Business Perspective

正如我一直在实施的那样，它是一个跨职能的应用交付模型，涉及业务和 it，并由持续交付基础架构支持。

通过启用和自动化敏捷实践，持续交付基础架构使运营模式变得敏捷，并为企业提供应对竞争挑战所需的灵活性和速度。

## 作为 DevOps 实现工程框架的设计模式

正如业务主管所建议的，今天的 DevOps 实现很难实现承诺的业务优势。原因是，操作模型维度被忽略，而支持工具和基础设施。

另一个原因是，DevOps 年轻，还处于技术成熟度模型的早期阶段；缺乏专业知识和工程方法来实现 it，即一种技术支持的应用交付模式。这就是 DevOps 转换设计模式的帮助所在。

### 什么是 DevOps 转换设计模式？

在本文中，术语 DevOps 转换设计模式指的是解决特定 DevOps 策略的通用可重用架构。它们不一定是可实施的解决方案，它们的主要目标有两个:

*   为设计和实现技术支持的运营模型提供一种中性语言
*   提供一种减少设计和实施持续时间和工作量的工程方法

它们是开发运维及平台即服务(PaaS)服务的正式架构设计和实施最佳实践。

### 作为 DevOps 实现工程方法论的设计模式

为了实现它的目标——技术支持的应用交付模型——设计模式围绕四个项目构建，包括目的、原则、一般解决方案和实现技术。

**目的:**阐明设计模式的目的以及 DevOps 策略，以解决。

**原则:**制定为规则和信念的最佳实践是否应该保证预期的 DevOps 策略收益？它们是实施 DevOps 战略的解决方案的决定因素。

**通解:**蓝图是原理应用的结果吗？他们总结了要实施的 DevOps 平台的功能和技术架构。

**实施技术:**实施通用解决方案的推荐技术方法、解决方案和工具有哪些？

为什么是 AWS？为什么它会成为 DevOps 价值的催化剂？

## AWS-一些将改变 DevOps 实现的设计模式

AWS 提供了如此丰富、多样且易于实施的服务组合，如果不利用它来实现现代化，那将是非常不幸的。下图总结了企业通过 AWS 从 DevOps 转型体验中获得价值的基本原理:

![Rationale of the DevOps Design Pattern](img/316ff6298b9514c0451c03889fa670c8.png)

Rationale of the DevOps Design Pattern

这是一种信念:

*   某些原则决定了交付保证价值的应用交付模型(ADM)架构所需的 AWS 服务。
*   使用这些 AWS 服务实现 ADM 会产生基于 AWS 的 DevOps 平台，这些平台可以切实地提供预期的好处。

### 产生 AWS 价值的四项 DevOps 原则

让我们来探讨一下我一直用来让首席信息官对其 AWS 云满意的原则:

1.  **全面思考，不仅仅是 IT:** 提醒转型不仅仅是 IT，而是整个组织的价值流，从营销和销售到开发和 IT 运营。
2.  **考虑跨职能部门，而不仅仅是 IT 部门**:提醒您，最重要的是建立一个跨职能部门的应用程序开发环境，以加快业务优先级划分、问题解决和决策制定，并实现价值实现目标。它们将成为 DevOps 平台的核心价值主张。
3.  **让 it 变得敏捷、灵活和快速**:提醒您敏捷、灵活和快速是竞争力和商业价值的催化剂。它们将成为 DevOps 平台的一部分。
4.  **Think PaaS** :提醒 AWS 为实施最先进的 CD 基础架构提供各种服务。

让我们举例说明三种将改变 AWS 开发人员体验的设计模式！

### 用软件组织工厂实现一种启动思维

目的是实施专注于上市时间和价值实现时间的 DevOps 战略。它适用于科技创业公司。

为了实现创业思维，devo PS AWS 的四个原则实现如下:

*   **考虑整体的和跨职能的，而不仅仅是 IT** :相关的业务和 IT 资源被放在一个单一的和专门的服务开发团队中，由适当的 Scrum 和 XP 敏捷实践支持。
*   **让 it 变得敏捷、灵活和快速**:基于敏捷实践和 AWS 基础设施即代码的 PaaS 服务旨在让应用交付流程变得敏捷、灵活和快速。
*   **想想 PaaS** : AWS 基础设施 as code 和 DevOps 工具相结合，以 PaaS 平台的形式实现 CD 基础设施。

原则应用产生的 DevOps 平台如下图所示:

![Software Organization Factory](img/b288386f4bc43df1871c35f142eeb7c9.png)

Software Organization Factory

“创业思维”平台围绕三个组件构建，包括支持云的运营模式、PaaS 和 CD 基础设施。

运营模式建立在三阶段应用交付生命周期的基础上:

*   **计划&度量**:它利用敏捷实践，如 Scrum 产品积压计划或 XP 的用户故事，动员业务用户、开发、QA 和运营人员处理业务优先级问题。
*   **开发&测试**:使用敏捷技术，如 Scrum 迭代、XP 的测试驱动开发(TDD)和行为驱动开发(BDD)，在开发生命周期中动员业务用户、开发、QA 和运营人员。
*   **发布&部署**:在部署到生产之前，它利用持续集成实践来构建和测试发布。
*   **监控&改进**:外包是为了让服务开发团队专注于核心业务:开发软件。

CD 基础架构结合了以下服务:

*   AWS CodePipeline 和 CodeDeploy 来设置交付管道。
*   AWS 基础设施作为代码，包括 CloudFormation、OpsWorks 和 Elastic Beanstalk，以生成 CD 基础设施。

## 总结一下

DevOps 的业务优势是真实的，然而，它还很年轻，仍处于技术成熟度模型的早期阶段。缺乏实现 it 现状(一个技术支持的应用交付环境)所需的专业知识和工程方法。

DevOps 设计模式(如软件组织工厂)填补了当今转换实践的空白:

*   它们为架构师团队和执行团队提供了一种中性的语言来讨论业务、技术和技术挑战以及解决方案。
*   通过指出可以利用的敏捷实践，他们简化并加速了运营模型的设计和部署。
*   通过指出要利用的 AWS 服务和功能，它们促进了 CD 基础架构的设计和实现。

本文中描述的 DevOps 实现过程在我最近的书《用 DevOps 重塑您的 IT:使您的 IT 与 DevOps 保持一致的完整指南》中有完整的记录。

在我的下一篇文章中，我将讨论数字组织和 CD 基础设施设计模式。

——[菲利普·阿卜杜拉耶](https://devops.com/author/pabdoulaye/)