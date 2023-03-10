# 为什么选择 Salesforce？

> 原文：<https://devops.com/why-salesforce/>

在过去的 20 年里，Salesforce 已经成为发展最快的企业软件平台，并且是销售、服务、营销、集成和定制应用程序开发等领域的市场领导者。尽管公司可能采用或考虑使用 Salesforce 的原因有很多，但最重要的价值主张是它提供了大量现成的功能，以雄心勃勃的速度发布新功能，并允许几乎无止境的定制和创新。

与传统平台不同，无需管理计算、数据、网络或安全基础架构，也无需投资于不会为组织增加价值的通用系统管理。除此之外，围绕 sales force trail head 的可访问的支持性社区和学习文化，可以实现快速入职和技能发展，很容易看出该平台的吸引力。

Salesforce 在 2000 年的口号是“点击而不是代码”，他们的标志是“没有软件”的形象，体现为 Salesforce 的第一个吉祥物 [SaaSy](https://www.salesforce.com/blog/2018/09/dreamforce-18-where-is-saasy.html) 。你可以是一个只使用点击的声明式开发人员，并使用拖放界面构建数据模型、业务流程自动化和用户界面。这为一个全新的工作专业化打开了大门:Salesforce admins 和 app builders——被授权直接定制平台以满足公司需求的公民开发者。

随着 Salesforce 的发展，他们认识到需要在其平台上启用自定义编码，并推出了 Apex 触发器，随后在 2008 年推出了 Apex 类和 Visualforce。管理员继续配置丰富的业务功能，而低代码开发人员和专业开发人员被授权创建超出声明性构建范围的定制。最初，在 Salesforce 上开发的代码是初级的:这里那里有几百行代码来适应不寻常的计算和数据处理。但是渐渐地，公司开始积累成千上万行定制代码，特别是当遗留应用程序从其他系统迁移过来的时候。不用说，“没有软件”的格言不再严格适用。

自 Apex 推出以来的十年中，150，000 家公司采用了 Salesforce，并将数量惊人的遗留系统迁移到 Salesforce 上，sales force 现在每天处理数十亿笔交易。其中许多交易是核心 CRM 和客户服务应用程序的一部分，但大量交易与自定义应用程序相关，这使得 Salesforce 成为最大的平台即服务(PaaS)提供商之一。

## DevOps 对 Salesforce 有何不同？

如前所述，Salesforce 同时提供 SaaS(软件即服务)和 PaaS(平台即服务)。相比之下，DevOps 世界中其他地方的大部分焦点是从内部基础架构转移到使用 IaaS(基础架构即服务)。此图展示了这四种模式之间的差异，以及它们如何代表公司自身必须管理的逐步简化。

![](img/75a7d1c98a72d8f23ebcbfaae1811407.png)

Figure 1: On-premise systems require you to manage all of the resources yourself. IaaS, PaaS and SaaS delegate progressively.

与大多数其他平台相比，管理 Salesforce 开发生命周期需要独特的技能和方法。你可以说 DevOps 运动是由开发人员(使用传统语言，如 Java)和系统管理员或操作员(使用传统基础设施，如服务器和数据库)共同实现的。因此，在 DevOps 世界中有大量成熟的工具和技术用于开发和部署代码，以及管理和更新基础设施。遗憾的是，几乎没有一个可以直接用于 Salesforce。

为了说明这一点，让我们看看团队如何使用 AWS 管理基础设施，或者在 Heroku(sales force 拥有的一个 PaaS 产品)上部署应用程序。AWS 基础设施的每个方面都可以使用 JSON 配置来表示。JSON 可以用来定义使用哪些 AWS 服务，它们在哪些数据中心运行，以及它们是如何配置的。AWS CLI(命令行界面)可以在 GitLab CI 等持续集成工具中使用，以便在每次 JSON 配置发生变化时自动将更新部署到 AWS 基础设施。

类似地，Heroku 提供了一个平台来部署定制的应用程序代码(用 Java、PHP、Ruby 等)。)并指定需要哪些服务(如 Postgres 数据库)来支持该应用程序。Heroku CLI 可用于在代码库发生变化时自动更新应用程序。Heroku 还提供了一个名为 Pipelines 的工具，允许您可视化和管理整个开发生命周期，而不需要第三方 CI 工具。

AWS 的基础设施作为代码的方法让系统管理员很高兴，因为它允许他们跟踪变化和自动更新。类似地，Heroku 消除了开发人员部署应用程序所需的大部分设置和依赖。Heroku 提供了一个真正的 PaaS，可以接受以传统方式构建的定制编码的应用程序:从头开始。

虽然我们可以说 Salesforce 的 Lightning 平台是一个 PaaS，但它实际上与 Heroku 等真正的 PaaS 系统的工作方式截然不同。Lightning 平台允许您编写自定义服务器端或客户端代码，但该代码只能在 Salesforce 上运行。尽管它允许您定义自定义数据库表和字段，但该模式不能加载到除 Salesforce 之外的任何数据库中。这些自定义实际上只是对一个 Salesforce 实例的配置的更改。因此，更准确地说，您对 Salesforce 进行的每个定制基本上都是 Salesforce 配置更改。

Salesforce 实际上只是一个允许无限定制的大型应用程序。但这意味着用于管理其他 IaaS 和 PaaS 产品的工具不能用于定制 Salesforce。然而，幸运的是，Salesforce DX 的发布意味着与其他技术一起使用的技术和原则现在可以移植到 Salesforce。这是我最近发布的《掌握 Salesforce DevOps》一书的重点。

## 销售队伍中的开发人员

从内部 CRM 软件迁移到 Salesforce 消除了对服务器和手动软件升级的需求。将客户支持和在线社区管理整合到 CRM 平台上，消除了集成销售、支持和社区应用程序的需要。将传统应用程序迁移到 Salesforce 平台允许这些应用程序与业务的其余部分共享数据和流程。

由于迁移到云极大地简化了交付 IT 功能的许多挑战，许多 Salesforce 客户已经能够在没有开发运维实践的情况下快速创新。但是，即使没有管理服务器和从零开始构建软件的麻烦，不可避免的复杂性增长最终会导致公司努力解决诸如组织不同步和部署功能延迟等问题。

Salesforce 解决了如此多的 IT 难题，几乎很容易忽略它创造了一些新难题的事实。

Salesforce 让公司能够专注于核心竞争力，而不是努力提供基本的 IT 服务。Salesforce 管理员和开发人员有权将他们的时间直接用于创造业务价值。但是随着多个 Salesforce 管理员和开发人员年复一年地在公司工作，越来越多的 [Salesforce 客户](https://devops.com/report-more-salesforce-customers-adopting-devops/)发现自己淹没在所有这些商业价值中。

如果您有成千上万个组件，每个组件都提供业务价值，但没有系统的方法来跟踪、管理或部署它们，那么您现在就面临一种新形式的业务困难和混乱。过犹不及。

## 什么是 Salesforce DX？

Salesforce DX(开发体验)是由 Salesforce 于 2016 年开始的一项倡议，并在 Dreamforce 2017 上公开推出。该计划的目标是重新设想 Salesforce 上的开发体验，重点关注如何为他们的开发社区提供安全有效开发所需的工具和流程。

Salesforce DX 是一个非常广泛的计划，包括 Salesforce 的几个主要团队，专注于环境管理、自定义编码、开发人员工具、API 等。尽管 Salesforce DX 团队处理非常多样化的需求，但他们的主要关注点(至少在最初)是改进开发人员工具和开发生命周期。

Salesforce DX 中包含的工具和功能免费提供给所有 Salesforce 客户。从这个意义上说，Salesforce DX 是对 Trailhead 的重要补充，trail head 是 Salesforce 的免费、自定进度、游戏化、交互式学习平台。Trailhead 也是公司的一项主要投资。这些都旨在支持熟练销售人员的成长，并使这些员工更容易在平台上构建和创新。这些多年战略计划有助于确保人才短缺和员工效率低下不会成为该公司每年 30%快速增长的限制因素。

## 摘要

Salesforce 是一个极其强大和多功能的平台。但是它在很多方面都是独一无二的，对于专业开发人员来说，让他们的工具和技术适应这个平台并不容易。

Salesforce DX 是一项重大战略举措，旨在确保 DevOps 和模块化架构等行业最佳实践在该平台上得以实现。但是让事情成为可能并不意味着过程是简单的。对于大多数致力于为 Salesforce 启用 DevOps 的团队来说，这仍处于早期阶段。幸运的是，有大量的研究和经验可以从更广泛的 IT 行业借鉴。将 Salesforce 等灵活、强大的平台与 DevOps 流程的速度和可靠性相结合，可以为团队带来全新水平的效率和效果。

— [安德鲁·戴维斯](https://devops.com/author/andrew-davis/)