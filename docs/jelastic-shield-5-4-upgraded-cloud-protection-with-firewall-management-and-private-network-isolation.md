# Jelastic Shield 5.4 升级了云保护，具有防火墙管理和专用网络隔离功能

> 原文：<https://devops.com/jelastic-shield-5-4-upgraded-cloud-protection-with-firewall-management-and-private-network-isolation/>

获得更高的云安全性，管理对应用程序的访问，改善用户体验

**加州帕洛阿尔托，2018 年 3 月 24 日**–[je lastic](https://jelastic.com/)，公司，多云 DevOps PaaS，宣布了一个名为 Shield 5.4 的新产品发布，强调了其在安全增强方面的主要目标。在此版本中，该平台升级了新的防火墙管理系统、专用网络隔离和客户要求的一系列其他功能。

Jelastic 首席执行官 Ruslan Synytsky 表示:“安全性保证被视为我们的云客户的主要要求之一，这也是我们不断改进 Jelastic platform 的原因，我们为此增加了专用网络隔离和增强的防火墙管理功能。

Jelastic 5.4 版本的主要特性之一是新实现的通过一个方便的图形界面在容器级别管理入站和出站防火墙规则的可能性。许多默认规则被自动添加到入站部分，以使节点可操作。

“5.4 版本为我们带来了在安全级别和访问管理方面更充分地满足客户(尤其是金融行业)需求的可能性。此外，值得一提的是，使用可简化开发运维流程的部署后和部署前脚本增加了容量。Jelastic 成为开发人员更加完整和强大的解决方案！我们喜欢它，”首席执行官马修·罗宾说。

此外，还实现了自动网络隔离，以禁止不同环境之间的任何不允许的连接。这导致了另一个重要的新增可能性，即创建安全的[环境组](https://docs.jelastic.com/environment-groups)，旨在将单个帐户的环境相互隔离。Platform 自动为每个隔离组创建一个专用的 IP 集，该 IP 集由适当的容器内部地址组成。这允许控制每个环境的节点之间的[访问。](https://docs.jelastic.com/environment-isolation)

“作为一家云托管公司，安全性是我们主要关注的问题之一。我们希望为我们的用户提供最好的安全功能，这也是我们很高兴在加拿大市场推出这款全新 Jelastic 平台的原因，”Alexandre Barfuhok， [Sphere48](https://jelastic.cloud/details/sphere48) 首席执行官

在 Jelastic Shield 版本的范围内，增加了许多其他所需的功能和改进，其中包括:

*   所有支持的中间件堆栈的额外环境层
*   通过专门打包的中间件容器支持 Go 语言
*   应用程序构建和部署操作的 Webhooks
*   内置 Web SSH 控制台
*   HTTP 2.0 支持 Jelastic 共享和专用负载平衡器
*   UI/UX 改进
*   部署改进
*   云脚本引擎优化，改善无服务器用户体验

“发布的功能提供了将适当的安全策略应用于容器环境的功能。因此，现在公司和用户可以阻止所有类型的访问，以更有效地保护他们的应用程序。我们对新平台版本的发布和达到最高客户满意度的可能性感到兴奋，”Sidimar Carniel， [Saphir](https://jelastic.cloud/details/saphir) 首席执行官。

Jelastic 5.4 的完整列表。详细描述的版本特性、改进和错误修复可以在[发行说明](https://docs.jelastic.com/release-notes-54)中查看。一个新推出的产品版本已经可以通过在[的一个升级的 Jelastic 服务提供商](https://jelastic.cloud/?versions=5.4-b2)注册来试用。

**关于 je elastic**

Jelastic 是托管提供商、企业和开发者的强大解决方案，将 PaaS 和 CaaS 的优势结合在一个完整的包中。其丰富的界面通过自动化微服务或整体应用程序的创建、扩展、集群和安全更新，简化了复杂的云部署。Jelastic 拥有独特的按使用量付费定价模式，在全球 60 多个数据中心提供公共云、私有云、混合云和多种云。该平台支持 Java、PHP、Ruby、Node.js、Python、.NET、Go 环境和自定义 Docker 容器。更多信息在[https://jelastic.com](https://jelastic.com)