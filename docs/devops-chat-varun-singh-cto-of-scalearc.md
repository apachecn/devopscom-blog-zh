# DevOps Chat: Varun Singh，ScaleArc 首席技术官

> 原文：<https://devops.com/devops-chat-varun-singh-cto-of-scalearc/>

[![singh](img/5add174f1d53791986ab65c3e2ec0760.png)](https://devops.com/wp-content/uploads/2015/09/singh.jpg) 最近，我有机会与 ScaleArc 的创始人兼首席技术官瓦伦·辛格(Varun Singh)坐在一起。ScaleArc 最近被 Gartner 评为酷派供应商，是数据库负载平衡软件的领先提供商。

Varun 和我谈到了为什么 IT 领导者需要确保他们的数据库以最佳方式运行。最重要的是，作为互联网的先驱，辛格在印度有着丰富多彩的职业生涯。你可以听听我们的对话，然后跟着抄本走。尽情享受吧！

[soundcloud url=”https://api.soundcloud.com/tracks/224505149″ params=”auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&visual=true” width=”100%” height=”450″ iframe=”true” /]

艾伦·希梅尔:大家好，我是《Devops.com》的主编艾伦·希梅尔。很高兴今天我们的嘉宾 ScaleArc 的创始人兼首席技术官 Varun Singh 先生能够加入我们。凡荣，欢迎收看我们的网络直播。

谢谢你，艾伦。谢谢你今天邀请我，会很有趣的。

艾伦·希梅尔:我想是的。所以，凡荣，我们在现场直播或录制之前聊了一会儿，你给了我一些你的背景。你曾在印度从事 OS/2 Warp 和 BBS 方面的工作，在印度运行了第一个基于 Linux 的 BBS，还主持了一个电视节目，这是一个非常有趣的职业。

是的，是的。在我的职业生涯中，如果你想这么说的话，我的目标是多元化。我什么都试过了。当过作家。做记者，做一些评论和其他事情。我建立了一个名为 TechTree.com 的网站，这个网站现在是印度第一的科技网站，还有一大堆其他的东西。我在美国消费者新闻与商业频道公司发展的巅峰时期加入了他们，最初是作为一名技术编辑加入的，但他们希望我成为首席技术官，所以我有时会这样做。用他们建立了很多网站，当我们这样做的时候，基本上了解了如何扩展数据库的价值。由此产生了 ScaleArc 的想法。

*艾伦·希梅尔:*优秀。所以，瓦伦，对于不熟悉 ScaleArc 的观众来说，你能给我们一个简短的背景介绍吗？

当然可以。ScaleArc 是数据库负载平衡软件。我们实际上为您提供了一个虚拟机，该虚拟机包含数据库负载平衡软件，可让您进行扩展，提供零宕机环境，并使您的事务性应用程序完全零宕机。这是一种谷歌、脸书和其他所有人都拥有的技术，因为他们是为自己打造的。我们所做的是为世界其他地方建造它。

Alan Shimel: 正如其他人常说的，CoreOS 人，你们给大众带来了类似谷歌的体验。

*Varun Singh:* 是的，在数据库层，是的。因此，CoreOS 本质上是在操作系统层做这件事，容器领域正在发生很多事情，这非常非常令人兴奋，我们也在某种程度上参与其中。但本质上我们所做的是坐在交易箱前。因此，应用程序和网站通过一个抽象层连接到我们，一旦它们连接到我们，我们就可以在后台与多个数据库服务器建立连接，并确保无论发生什么情况，应用程序都能顺利完成交易。

*艾伦·希梅尔:*优秀。还有凡荣，ScaleArc 算是一夜成名六年了吧？你们从 2009 年开始就存在了？

*Varun Singh:* 是的，我们花了大约 2.5 到 3 年的时间来建立技术本身，因为建立我们已经建立的东西非常复杂，因为我们已经建立了世界上第一个透明的数据库引擎。如果你看看我们在 2010 年申请的四项专利，它们都是关于透明度，以及我们如何基本上为任何一个应用程序实现这一点。因此，应用程序所要做的只是将其连接转移给我们，他们就可以立即访问整个集群，获得零停机时间，获得深入的 SQL 分析，所有这些都是我们提供的单一软件包的一部分。

*艾伦·希梅尔:*优秀。所以，Varun，我们今天的谈话实际上是针对 C 级，副总裁经理级的人。为什么应该——在不深入了解技术或功能集的情况下，高管们为什么应该关心 ScaleArc 正在做什么以及您正在解决高管们关心的什么问题？

当然可以。因此，在这个时间点上，我相信很多高管都在考虑如何迁移到云。当您转向云时，您实际上是在运行更小的机器，您正在运行不可预测的安排窗口，并且您还必须担心如何在多台机器上聚合容量才能达到您的性能数字。

许多在本地的超大型服务器上运行的应用程序现在都没有办法进入云环境。因此，就大型任务关键型数据库密集型应用程序而言，ScaleArc 基本上是能够迁移到云的最后一步。这是我们做的第一件事。

我们让您的应用程序开发人员开发这些应用程序变得更加容易，不必担心高可用性，不必担心故障转移和所有这些事情。这使得开发人员的工作变得更加容易。我们为您提供了许多 API，所有这些 API 都可以让您自动完成几乎所有这些功能。您可以继续进行滚动升级。你可以做一个滚动补丁。所有这些都可以自动化，您可以使用我们提供的 API 来完成所有这些工作。

*艾伦·希梅尔:*优秀。那么，Varun，当你们这些人通常——首先，是大多数大型企业都在寻找这种东西，还是所有企业都在寻找这种东西？

*Varun Singh:* 这是一个全面的计划，但我们目前专门针对较大的企业。所以我们的一些最大客户是 Dell.com。因此，Dell.com 的每一笔交易都与我们合作，我们已经与他们一起度过了前两个黑色星期五，现在正准备与他们一起度过第三个黑色星期五。我们与纳斯达克合作，所以纳斯达克目前几乎所有的价格信息都来自我们的系统。我们在 Microsoft.com 与答案合作，所以所有通过 Microsoft.com 答案的用户查询都会通过我们。这是我们的大规模部署之一，涵盖四个区域、多个数据中心、主动/主动。非常复杂的应用程序和部署。

*艾伦·希梅尔:*优秀。还有凡荣，当你与这种规模的客户互动时，互动来自哪里？是高管主导的，还是有一些技术冠军将 ScaleArc 技术带入高管团队？

*Varun Singh:* 有时是行政领导，有时是架构领导。有时甚至是 DBA 或应用程序开发人员主导的。它是全面的。我们看过各种各样的，但我们见过的最一致的是建筑，我认为这也非常适合你的展览。

艾伦·希梅尔:是的，是的，我想是的。所以，凡荣，我想我们之前说过，我们生活在一个有趣的时代。当我们进入一个由开发运维、自动化和持续交付集成、持续集成、持续一切等运动主导的世界时，这就像是一个边界层。这对你的生活和 ScaleArc 有什么影响？

*Varun Singh:* 这对我们帮助很大。这正是人们想要的。他们希望应用程序基础架构持续可用。因此，从这个角度来看，事实上数据库是堆栈中最后一个难以管理的东西，我们在这个时间点上有点像在飞。

艾伦·希梅尔:没错。因此，数据库是最后一部分，可以更快地做更多的事情，并获得某种 DevOps 方法或敏捷。

*Varun Singh:* 是的，从本质上说，客户现在的目标是能够真正了解他们的数据库堆栈，并完全控制他们的数据库堆栈。我们正在成为他们每天都要查看的控制面板，从本质上了解正在发生的事情，无论是新用户登录到他们的数据库堆栈，还是正在执行以前从未执行过的新查询。我们为他们提供的是整个堆栈以及零停机维护的能力，能够在一天当中将服务器标记为离线，为其安装补丁程序，对其进行升级，然后使其恢复在线。在过去，您从未能够做到这一点，因为您总是会有大量的应用程序错误，而我们正在做的基本上是消除所有这些应用程序错误，并提供一个几乎可以与任何应用程序引擎配合使用的事务引擎，并允许该应用程序引擎成为零宕机应用程序。

*艾伦·希梅尔:*优秀。Varun，对于在这里收听的高管，您认为首席技术官、首席信息官、副总裁和经理在数据库管理、数据库性能、数据库负载等方面应该寻找的下一个前沿或下一件事是什么？

*Varun Singh:* 我认为在这个时候，他们必须想办法向外扩展，向外扩展，达到我们所说的“无共享”。无共享本质上是一种在服务器上存储数据库信息的方式，这种方式使您不必担心相互依赖的问题。因此，每台服务器都是一个独立的隔离区域，即使您有五台服务器，也可以让其中四台停机，第五台仍然运行。这就是我认为现在每个人都在朝着的架构。这就是 MySQL 出名的架构，现在几乎所有的数据库都朝着这个架构前进。数据库变得越来越复杂。但是应用程序真的不能使用它，因为现在的问题是这些应用程序中有很多是写在旧版本的 SQL 数据库上的。因此，我们所做的是将新数据库中的所有新功能提供给应用程序，而无需对应用程序进行任何更改。

*艾伦·希梅尔:*优秀。凡荣，我们快没时间了，信不信由你。我们尽量让这些聊天相对简短。但我最后总是问人们的一个问题是，对于听众来说，无论他们是经理、高管还是想成为经理或高管的人。如果你必须选择一本书来阅读，这本书将帮助他们推进他们的职业生涯，并了解正在发生的事情和他们需要去哪里，那本书会是什么？

*Varun Singh:* 我现在可以给你两三个，但是如果你真的想要一个，就企业家而言，我认为*关于硬东西的硬东西*仍然是这个月的特色。它仍然进行得很好，我已经重读了两遍，有时如果你重读它，它会赋予你新的意义，因为你是从一个完全不同的角度分析一个情况，这是一本非常有趣的书。

艾伦·希梅尔:所以*关于硬的东西的硬的东西。*

*Varun Singh:* 是的，这是 Jason Horowitz 的合伙人之一，Ben Horowitz。

艾伦·希梅尔:本·霍洛维茨，当然，我很了解这本书。凡荣，当然如果人们想了解更多关于 ScaleArc 的信息，是 ScaleArc.com 吗？

*Varun Singh:*ScaleArc.com，我们有一大堆视频，我们有一些网络研讨会，我们还有许多其他可用的资料以及客户案例研究。

*艾伦·希梅尔:*优秀。varun Singh——ScaleArc 的创始人/首席技术官——非常感谢您今天参加 DEVOPS 聊天，感谢您让 scale arc 继续取得成功。

*瓦伦·辛格:*谢谢。谢谢你邀请我。