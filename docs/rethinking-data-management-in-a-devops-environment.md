# 重新思考 DevOps 环境中的数据管理

> 原文：<https://devops.com/rethinking-data-management-in-a-devops-environment/>

你经常听到数据是新的石油。这种有价值的、不断变化的商品已经开始在许多云原生应用程序中扮演主角。然而，根据许多 DevOps 团队的说法，数据问题继续困扰着他们持续集成、测试和部署频繁软件版本的工作。更具体地说，持久数据(及其底层数据库引擎)的问题通常是罪魁祸首。

您的组织可能正在追求新兴的物联网应用，这些应用整合并分析来自多个来源的传感器数据。或者，您的 DevOps 团队可能正在尝试开发应用程序，以提取关于客户的进一步可操作的洞察力。不管是什么用例，毫无疑问，后端数据库架构对于这类项目的成功越来越重要。然而，在许多情况下，这样的数据库系统似乎很难跟上当今 DevOps 管道的步伐。

根据一份关于 2019 年数据库部署状态的[报告](https://www.devopsdigest.com/the-state-of-database-deployments-in-application-delivery-2019), 46%的加速发布计划(每周甚至每天发布)的开发运维团队发现相应地加快他们的数据库发布周期“极其或非常困难”。在相关的 Redgate [关于 2019 年数据库开发状况的报告](https://www.devopsdigest.com/2019-state-of-database-devops-report)中，20%的受访者认为缓慢的开发和发布周期是“传统孤岛式数据库开发实践”的最大缺点之一另有 23%的受访者认为，在传统数据库环境中引入数据库更改时，部署失败和额外停机的风险更高。

## 触及数据问题的核心

这样的数据库问题是否是错误选择底层数据库技术的结果——例如使用 RDBMS、NoSQL 甚至是 NewSQL 系统？可能吧。

也许数据库问题也是由于数据库专家和他们的开发人员之间缺乏交流造成的？毫无疑问，这也是事实。

当你得知这两种情况(错误的技术和糟糕的沟通)都是罪魁祸首时，你会感到惊讶吗？此外，还应归咎于用组织处理早期遗留用例的老方法来解决新数据问题的冲动。

最终，与许多与开发运维相关的事情一样，数据问题的答案可能需要在三个独立的方面进行变革:人员、流程和技术。还需要从根本上改变一开始处理这些问题的方式。

## 从人员和流程开始

与其担心数据库变慢，不如从 DevOps 团队如何首先处理底层数据层的许多方面开始。这意味着:

1.  从项目一开始，就让数据库管理员成为跨职能开发团队的一员。这将有助于促进健康的交叉交流。它们还将积极影响支持您的新兴用例的适当底层数据层和基础设施的开发。在管理许多数据集的大型组织中，这些人可能是专门的数据库管理员(DBA)。在较小的公司，这些可能是更多的全栈工程师，他们在数据库操作方面也有高质量的专业知识。
2.  **尽早识别与您的数据相关的不同数据类型、域、边界和最佳云原生模式。**一旦建立了这些，团队就可以更好地理解为每个新用例开发应用程序和数据架构的不同方法。

实际上，组织需要齐心协力，将他们的总体数据架构讨论向左转移。这种转变允许更多关于数据的正确问题被询问、回答，并在整个应用程序的设计早期被合并。

## 询问关于数据的正确问题

这种早期协作工作的一部分可能涉及询问关于数据的关键问题。其中包括应用程序及其用户与底层数据交互的最佳方式，例如:

*   如何获取数据，从哪里获取？
*   我们将如何访问数据？
*   我们将如何以及在哪里存储它？
*   当我们为新的用例构建时，我们如何更新和/或维护遗留数据库？
*   我们将拥有哪些类型的数据？随着时间的推移，类型会如何变化或增加？
*   我们将如何从中查询？用户希望运行的最常见的查询是什么？
*   我们将如何管理和扩展使用中的数据？
*   我们将如何保护数据免遭数据丢失、灾难或损坏？
*   我们将如何保护数据？

如果这些问题听起来很像数据生命周期中的特性，那么你是对的。但是，在匆忙交付、集成、测试和部署应用程序代码的过程中，这些关于数据的基本问题经常被忽略。因此，经常发生的情况是，应用程序团队创建一个设计，然后说，“好了，现在创建一个数据架构来支持应用程序。”

这种在开始时对数据和协作的根本性缺失通常会导致后来糟糕的数据库架构决策。这也可能导致开发运维团队求助于变通方法来适应一开始就做出的错误架构选择——这可能导致一些开发团队选择完全避开 DBA 的参与。在这种情况下，他们甚至可能会选择使用公共云服务(或其他类型的数据管理)来支持他们的应用程序。

相反，应用程序团队应该选择开发人员和 IT 所有职能部门(包括 DBA)之间早期协作的方式。这种方法可以提供更好的 DevOps 结果。它还帮助组织走向这样一个未来:数据架构师在对应用程序的成功至关重要的各方之间提供了一座有效的桥梁:从开发人员的需求到数据库管理员提供的平台以及支持这些平台所需的底层基础设施。

## 改变技能组合，改变思维模式

与大多数 DevOps 相关的事情一样，数据层的成功不仅与 DevOps 管道中的具体步骤有关，还与改变数据库架构和数据库部署方法的教育、思维和文化有关。

例如，如果您组织中的大多数 DBA(如 Oracle DBA 或 SQL Server admins)只专注于一个领域，那么您的组织可能会从教育投资中受益，从而缩小技能差距。这种投资有助于扩大员工对开发运维实践或新兴的云原生应用模式数据库方法的了解和认识。

它还可以帮助一些组织首先确定组织中想要变革、创新和学习新工具、方法和实践的个人。

另一个选择是雇佣那些已经具备这方面专业知识的人。然而，当你雇佣新的技能组合时，答案可能不仅仅是雇佣几个 NoSQL 管理员。这种策略也不一定能解决您的数据问题。雇佣一个不具备多少 NoSQL 技能，但擅长以不同方式思考数据的人，可能同样有益(或者更有益)。

## 商业第一，技术第二

在我们的实践中，我们经常被要求权衡技术选择，以支持 DevOps 在物联网、大数据和高级分析等新兴领域的工作。组织向我们询问使用传统关系数据库(SQL Server、Oracle 等)的情况。)与 NoSQL 数据库(MongoDB、Cassandra 等)的对比。).他们询问一个 NoSQL 迭代相对于另一个迭代的优点。他们询问如何在容器环境中管理持久数据。当他们做出的数据选择导致其他意想不到的问题时，他们甚至会询问解决方法。

我们尽力回答这些问题。但是，只要有可能，我们也会告诉组织后退几步，从他们的业务目标开始:

*   你想完成什么？
*   你的业务驱动力是什么？
*   你希望在这些情况下如何使用数据？

这些问题的答案可以帮助您更好地选择最佳数据架构，以支持不断增长的应用程序。

最终，新的工具和技术可以实现许多令人印象深刻的数据架构。但是，仅仅用工具来解决数据问题是不够的。对任何项目来说，在人员、流程和跨部门沟通方面的早期努力和投资对于成功的数据结果同样重要。

我们现在进行的许多讨论都试图让每个人回到他们跳过的步骤。这又回到了软件工程的基本原则:尽早解决问题，这样以后就不会有问题了。

不幸的是，数据是技术堆栈中的一个组件，一旦您选择了应用程序数据架构的特定路径，就不能轻易撤消。当谈到数据规划时，它实际上是一个现在支付或以后支付的等式。

花时间明智地选择您的数据路径，而不是以后再为部署和性能的降低或其他问题买单，这难道不是最好的选择吗？

——[杰夫·博济奇](https://devops.com/author/jeff-bozic/)