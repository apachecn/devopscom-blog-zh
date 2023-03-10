# 云部署的最佳实践

> 原文：<https://devops.com/best-practices-cloud-deployment/>

当谈到在云中部署应用程序时，传统观点认为，如果您是一家中小型公司，就不需要 DevOps。云旨在使几乎任何人都能够快速、轻松地建立他们需要的基础架构，而无需在管理复杂的数据中心运营或硬件方面有太多经验。但是，当公司意识到需要开发运维时，几乎已经太晚了——云基础架构已经变得复杂，成本已经超出预期，宝贵的时间正在被浪费。

为了确保您能够优化云或混合云部署，并避免其他公司遇到的许多问题，您必须在公司内部采用许多最佳实践。

### 最佳实践 1:从一开始就意识到你需要 DevOps

当您管理自己的硬件时，您确切地知道部署成本是多少，有哪些资源可用，并且清楚地了解它们是如何相互关联的。云的抽象使得初始设置变得轻而易举。但是通常不涉及正式的结构:个体开发人员可以在他们需要的任何时候启动新的实例，而不用考虑已经在使用的资源的更大图景，它们是如何使用的，或者组织正在计划什么。

增加不必要的云资源不仅会增加公司的长期成本，还会导致云蔓延，需要耗时的手动流程来维护。想象一下，如果您的公司有数千台由不同流程创建的机器，但您不知道是谁创建了它们，它们的用途是什么，甚至不知道是否仍然需要它们，那么您的公司将会面临哪些挑战。

通过从一开始就使用 DevOps，您将能够平衡开发人员的需求和云中资源的可用性，以确保费用不会失控，并且您确切了解云基础架构现在和未来的使用情况。

### 最佳实践 2:有一个过程和目的

在创建云基础架构时，您需要有一个明确定义的目的，以及一个用于部署和持续管理的流程。您需要跟踪正在使用的资源及其指定用途。一些云供应商，如 AWS，提供标记功能，帮助您跟踪每台机器是为什么服务而创建的，以及它们是否用于生产、备份、负载平衡或测试。

无论您是使用标记功能还是维护单独的云资源数据库，了解您购买了什么以及如何使用将提供所需的可见性、易管理性和更好的成本控制。

### 最佳实践 3:利用自动化

无论是在云中还是在内部，自动化对于简化日常实践都非常重要，确保它们得到一致应用，并消除手动流程中常见的潜在错误。

当部署在多个云上或混合环境中时，理解用于一个云提供商的标签在另一个云提供商上不起作用是很重要的。该流程通常分为三个步骤:库存创建、系统准备和自动部署。许多云系统允许您直接从服务器创建动态清单，消除了手动创建或维护的需要。然而，跨多个云的部署需要对该清单进行抽象；通常从各种动态库存中创建统一格式的静态库存。

### 最佳实践 4:在设计网络时考虑安全性

设计不良的网络几乎不可能安全。当公司允许他们的网络有机增长而不是提前规划时，问题经常出现。许多公司已经采用了隔离服务网络和管理网络的最佳实践。服务网络包括向您的客户和用户提供服务所需的所有组件，而管理网络则由您内部管理网络所需的组件组成。隔离这些网络可以更好地确保未经授权的用户无法通过互联网访问您的系统。

安全性的另一部分是密钥管理。根据云提供商的不同，密钥可以广泛使用，或者有一个对全世界开放的根密码。事实上，许多黑客会定期扫描 Github 的,寻找开发者不小心签入的密钥。由于必须管理如此多的密钥，您可能很难确保它们不被暴露。DevOps 在保持密钥锁定方面起着重要的作用，然后将它们提供给一组精选的个人，这些人只能在生产中使用它们。

### 最佳实践 5:战略性地进行监控

当您在内部部署硬件时，通常的做法是预先定义要监控的内容。但是云中的监控完全不同，基本的默认设置会产生大量数据，其中大部分可能与您的组织无关。

根据您处理内部监控的方式，您将希望设计云监控来满足您公司的独特需求，并过滤掉与您的网络或运营无关的信息。

### 最佳实践大有帮助

牢记这些最佳实践并从一开始就采用 DevOps 模型将使您的公司无论规模大小都能从云部署中获得最大收益，并避免在没有适当的预先规划和对网络设计和流程的高度关注的情况下出现的成本高昂且耗时的挑战。

## 关于作者/罗杰·富尔顿

*![roger-headshot](img/f8796e61921f2d7c56f2ef8605e30461.png)*

罗杰·富尔顿是 Iron.io 的基础设施和运营总监。他的背景包括在软件架构和运营规划方面的丰富经验。他管理国际团队，为最终用户提供高度可用的产品和高性能的内部基础设施。在加入 Iron.io 之前，Roger 曾在 Kaybus 担任应用和基础设施工程主管。他还曾在 JRV 咨询集团、Cybrata、隐形 IT 和 Clarus Systems 担任技术领导职务。罗杰拥有贝尔法斯特皇后大学的硕士学位，并以最高荣誉毕业。