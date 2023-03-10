# 9 个我们喜爱的开源 DevOps 工具

> 原文：<https://devops.com/9-more-open-source-devops-tools-we-love/>

不久前，我们发表了 Logz.io 的 Tomer Levy 写的一篇关于 9 个我们喜爱的开源 DevOps 工具的文章。当然，你怎么能在这么多有价值的选择中挑出 9 个呢？因此，我们想重新访问开源 DevOps 工具空间，并在列表中添加另外 9 个工具。几个月后，我们还会在列表中添加更多的开源 DevOps 工具。同时，这里还有 9 个我们喜爱的开源 DevOps 工具:

**[![Kubernetes](img/6141fea32fa7c30b7805ba30fa82dc6c.png) ](https://devops.com/wp-content/uploads/2015/11/Kubernetes.png) 1。Kubernetes** 是一个用于 Docker 容器的开源编排系统。它处理计算集群中节点的调度，并主动管理工作负载，以确保它们的状态与用户声明的意图相匹配。使用“标签”和“容器”的概念，它将组成应用程序的容器分组到逻辑单元中，以便于管理和发现。Kubernetes 最初由谷歌开发和拥有，被提供给[云原生计算基金会](https://cncf.io/)来播种其他补充技术，以实现一组通用容器技术。它是 CoreOS 构造产品的一个组成部分，此外还与 Mesos 和中间层 DCOS 紧密相连。Kubernetes 承诺为每个人提供类似 Google 的容器使用。似乎无论我们使用什么样的基本容器技术，它都被今天许多基于容器的 PaaS 栈所使用

[![Chef_HORl_CCan_Reg](img/04e5f8349e9679873a2326f256d0d417.png) ](https://devops.com/wp-content/uploads/2015/11/Chef_HORl_CCan_Reg.png) ** 2。Chef**–来自官方的内容:“Chef 是一个系统和云基础架构自动化框架，可以轻松地将服务器和应用部署到任何物理、虚拟或云位置，无论基础架构的规模如何。每个组织由一个(或多个)工作站、一台服务器和每个将由 chef-client 配置和维护的节点组成。Cookbooks(和 recipes)用于告诉 chef-client 应该如何配置组织中的每个节点。chef-client(安装在每个节点上)执行实际的配置。

不仅如此，对许多厨师来说，Puppet Labs 和 Jenkins 是 DevOps 工具的核心和灵魂。今天，Chef 超越了其最初的配置管理使命，代表着向“一切如代码”的转变，同时仍然保持其开源承诺。Chef 交付、Chef 合规将 Chef 带入整个 DevOps 工作流程中涉及的工具领域。

**[![PL_logo_horizontal_RGB_lg](img/d04ee968a7bb984cedbdca4056083ac3.png) ](https://devops.com/wp-content/uploads/2015/11/PL_logo_horizontal_RGB_lg.png) ** ** 3。木偶**–从罗穆卢斯到大厨莱姆斯，木偶实验室是 DevOps 运动的创始成员之一。Puppet like Chef 建立在开源基础上，并且仍然完全支持其开源遗产，它已经超越了配置管理和单个机器或实例自动化的最初使命，转而协调您的整个堆栈。

来自 Puppet 的开源文档，为什么是 Puppet

Puppet 的开发是为了帮助系统管理员社区构建和共享成熟的工具，避免每个人重复解决相同的问题。它通过两种方式做到这一点:

*   它提供了一个强大的框架来简化系统管理员需要执行的大部分技术任务
*   sysadmin 工作是用 Puppet 的定制语言编写的代码，就像其他代码一样可以共享。

这意味着您作为一名系统管理员可以更快地完成工作，因为您可以让 Puppet 处理大部分或所有的细节，并且您可以从其他系统管理员那里下载代码来帮助您更快地完成工作。大多数 Puppet 实现至少使用一个或两个由其他人开发的模块，并且社区已经开发和共享了数百个模块。

**[![Maven_logo.svg](img/5a6297dd9d0ad64be64826a2a748ae6f.png) ](https://devops.com/wp-content/uploads/2015/11/Maven_logo.svg_.png) 4。Maven**——意第绪语单词的意思是*知识的积累者*，Maven 最初是为了简化 Jakarta 涡轮机项目的建造过程而创立的。有几个项目，每个项目都有自己的 Ant 构建文件，这些文件略有不同，jar 被签入 CVS。我们想要一个标准的方法来构建项目，一个清晰的项目组成定义，一个发布项目信息的简单方法，以及一个在几个项目间共享 jar 的方法。

结果是一个工具，现在可以用于构建和管理任何基于 Java 的项目。我们希望我们已经创造了一些东西，使 Java 开发人员的日常工作变得更容易，并且通常有助于理解任何基于 Java 的项目。

Maven 的主要目标是让开发人员在最短的时间内理解开发工作的完整状态。为了实现这一目标，Maven 试图解决几个方面的问题:

*   使构建过程变得简单
*   提供统一的构建系统
*   提供高质量的项目信息
*   为最佳实践开发提供指南
*   允许透明迁移到新功能

**[![gradle_logo](img/32c6eb85a7f10d167b62f9aeb05a91fb.png) ](https://devops.com/wp-content/uploads/2015/11/gradle_logo.png) 5。Gradle-**阴对美文的阳，grad le 和美文很像木偶和厨师。在这种情况下，虽然 Gradle 是出于对 Maven 和其他工具的不满而诞生的。来自 Gradle，Inc .网站:

Gradle 是由 Hans Dockter 创建的，他当时在企业软件开发部门工作，遇到了一个棘手的构建问题。当时他正在使用 Apache Maven。经过三天三夜的彻底研究，他发现这个问题根本不能用这个工具来解决。Hans 发誓要为他自己，为他的团队，为他的公司，为世界各地的开发者解决这个问题。创始人兼首席技术官亚当·默多克也加入了这项任务。在 2008 年 4 月将 Gradle 开源项目发布到野外之后，Hans 和 Adam 雇佣了他们一路上遇到的所有关键贡献者。其中包括来自 Thoughtworks、Typesafe 和 Pivotal 等公司的世界知名的毕业生专家。

如今，许多开发人员和商店都使用这样或那样的开源工具。

**6。Mattermost ( & Zulip)** 今天是聊天日。在许多组织中，它正在取代电子邮件，成为团队甚至外部成员之间的主要沟通方式。虽然这个领域有很多商业解决方案，比如 HipChat 和 Slack，但是也有一些有价值的开源工具。这些开源解决方案的最大优势之一是，如果您担心控制、治理或安全问题，您不必使用托管版本。你可以在你自己的服务器上安装这些软件，如果你愿意的话，你可以自己维护。以下是两个领先的开源 ChatOps 工具:

[![mattermost](img/75139895d2ad24599b7668c6280165b3.png)](https://devops.com/wp-content/uploads/2015/11/mattermost.png)[matter most](http://www.mattermost.org/)——是一个开源的 Slack 替代方案。背后的公司是由 Y Combinator 资助的初创公司，创始人来自微软 Office engineering。沮丧的是，在使用 SaaS 托管的聊天程序时，他们被锁在自己的数据之外，除非他们付费使用该应用程序，他们开始创建自己的自托管应用程序，因此 Mattermost 诞生了。不确定商业元素将加入其中，也许是开放核心类型的高级功能？支持？时间会证明一切。

[![zulip-icon-512x512](img/4d74f37c71e897c963a1585e59f7917a.png)](https://devops.com/wp-content/uploads/2015/11/zulip-icon-512x512.png) 不基于 IRC 和 XMPP，Zulip 功能: ***线程群组对话、一对一和群组私人对话、持续、历史、完整历史搜索、团队状态和好友列表、内嵌图像、视频和推文预览、拖放文件上传、流范围通知、重要错过消息的电子邮件、桌面通知、声音通知、热键、表情符号、代码、轻量级标记、消息编辑、仅邀请流、带星号的消息、集成、API、移动应用、桌面应用***

**7。OWASP**–开发人员和 DevOps 最好的安全朋友，OWASP 已经成为 web 应用程序安全的地方。他们的使命是使软件安全可见，以便世界各地的个人和组织能够对真正的软件安全风险做出明智的决定。OWASP 实际上是许多不同项目的总称，包括工具、列表(OWASP 前 10 名)和组。他们的网站说得最好:

[![OWASP](img/d1a6616db6af20e5d47791766f2f682f.png)](https://devops.com/wp-content/uploads/2015/11/OWASP.png)OWASP 基金会于【2001 年 12 月 1 日上线它于 2004 年 4 月 21 日在美国成立，是一个非营利性慈善组织，旨在确保我们在 [OWASP](https://www.owasp.org/index.php/Main_Page "Main Page") 的工作能够持续获得支持。OWASP 是一个国际组织，OWASP 基金会支持 OWASP 在世界各地的努力。OWASP 是一个开放社区，致力于使组织能够构思、开发、获取、操作和维护可信任的应用程序。所有 OWASP 工具、文档、论坛和章节都是免费的，对任何对提高应用程序安全性感兴趣的人开放。我们提倡将应用程序安全作为人员、流程和技术问题来处理，因为最有效的应用程序安全方法包括所有这些方面的改进。我们可以在 www.owasp.org 找到。

OWASP 是一种新型组织。我们没有商业压力，这使我们能够提供公正、实用、经济的应用安全信息。OWASP 不隶属于任何技术公司，尽管我们支持商业安全技术的明智使用。与许多开源软件项目类似，OWASP 以协作和开放的方式制作许多类型的材料。OWASP 基金会是一个非营利实体，确保项目的长期成功。

**8。zabbix(&Observium)**–好吧，很多人已经开始讨厌 Nagios 了。仍然有很多人使用 Nagios。也就是说，我们想强调网络和应用程序监控领域的一些开源选项。我们喜欢的两个是 Zabbix 和 Observium。

[![zabbix_logo_500x131](img/d195fbc97da00ef9c205254aefd890bf.png)](https://devops.com/wp-content/uploads/2015/11/zabbix_logo_500x131.png)[Zabbix](https://www.zabbix.com/)——Zabbix LLC 的基本工作范围是开发用于监控网络和应用的开源软件。除此之外，该公司还提供广泛的专业服务，旨在满足每个客户独特的业务需求，包括实施、集成、定制开发和咨询服务以及各种培训计划。

Zabbix 团队的使命是为所有人提供一个卓越的监控解决方案。

该公司的旗舰产品是 Zabbix，这是世界上最受欢迎的开源监控软件之一。它已经被许多公司使用，这些公司选择它是因为它具有真正的可扩展性、高性能、易用性和极低的拥有成本。

 [](https://www.observium.org/) [![observiumlogo](img/8856c6b79b880d123ab0e1a741ff73e9.png)](https://devops.com/wp-content/uploads/2015/11/observiumlogo.png)[observer vium](https://www.observium.org/)–是一款低维护的自动发现网络监控平台，支持多种设备类型、平台和操作系统，包括 Cisco、Windows、Linux、HP、Juniper、Dell、FreeBSD、Brocade、Netscaler、NetApp 等等。Observium 致力于为您的网络健康和状态提供一个美观、强大、简单而直观的界面。

Observium 由一组经验丰富的网络工程师和系统管理员专业开发和维护，是一个由其用户设计和构建的平台。 *Observium 社区*对每个人都是免费的，并且每年接收两次更新和功能。 *Observium Professional* 增加了每日更新和新功能的优先访问权，只需支付少量年费。

**[![cucumber](img/97668f356c86e2d979ca85b727e2031e.png) ](https://devops.com/wp-content/uploads/2015/11/cucumber.png) [ 9。黄瓜](https://cucumber.io/)–**好的，用黄瓜的请举手。这是业内保守得最好的秘密之一。我经常惊讶于有多少开发人员和 DevOps 人员提到这个开源工具。它实际上是几个工具，因为它们是不同语言的不同版本，每个版本都有稍微不同的特性集。

对于那些不知道的人来说，“Cucumber 通过将*需求、自动化测试和文档*融合成一个内聚的整体，彻底改变了软件开发的生命周期:验证软件的纯文本可执行规范。”

这些是我们最新的 9 款开源 DevOps 工具，我们非常喜欢。我们知道还有更多。为我们的下一篇文章留下有价值的选择的评论。