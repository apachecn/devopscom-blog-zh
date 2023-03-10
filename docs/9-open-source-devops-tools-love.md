# 我们喜爱的 9 款开源 DevOps 工具

> 原文：<https://devops.com/9-open-source-devops-tools-love/>

在我们建立 SaaS 公司的同时，我们也投入了大量的时间来研究和决定在我们的 DevOps 工具包中包含哪些工具。我们的这些决定是基于我们在 IT 行业多年的经验，主要是处理基础设施。从构建 Pb 级数据分析基础设施开始，我们的架构、工具和流程已经成为我们技术和运营的关键组成部分。我们在选择、基准测试和不断改进我们的工具选择方面非常小心。

作为一家在开源堆栈(ELK)上构建解决方案的公司，我们的团队积极参与开源社区，在定制工具以满足我们需求的同时，为多个项目(如 Camel 和 Kafka)做出贡献。我们内部使用的绝大多数工具都是开源的。通过分享我们随时间推移收集和完善的工具集，我们希望在 DevOps 社区中就可以进一步改进的地方展开讨论。

因此，我们欢迎您浏览我们创建的以下列表。有些工具你可能已经知道很多年了，而有些可能是新的。当然，我们欢迎任何和所有的反馈，尤其是那些使用替代品的人！

## 必备的 DevOps 工具

### 1.[Nagios](https://www.nagios.org/)(&[Icinga](https://www.icinga.org/))****

[![nagios](img/b78525efabbc9c2883cae1e77a4355ae.png)](https://devops.com/wp-content/uploads/2015/08/nagios.png) 基础设施监控是一个拥有众多解决方案的领域…从 Zabbix 到 Nagios，再到数十种其他开源工具。尽管现在有很多新手，Nagios 是一个非常有效的老监控解决方案，因为有大量的贡献者社区为该工具创建插件。Nagios 并没有包含我们想要的自动发现新实例和服务的所有功能，所以我们不得不用社区的插件来解决这些问题。幸运的是，这并不太难，Nagios 工作得很好。

我们还研究了 Icinga T1，它最初是作为 Nagios 的 T2 分支 T3 创建的。它的创造者旨在通过新功能和现代用户体验将 Nagois 带到一个新的水平。在开源社区中，对于 Nagios 及其子代的优点存在争议，但目前我们仍在继续使用 Nagios，并对其规模和性能感到满意。随着我们的进步，将来可能会转而采用更新的技术，如 Icinga。

### 2.[提示](https://mmonit.com/monit/)

[![monit](img/5aade7e3d6e4579d6cd34b0ce4526387.png)](https://devops.com/wp-content/uploads/2015/08/monit.png) 有时候最简单的工具是最有用的，简单的看门狗 Monit 就证明了这一点。它的作用是确保机器上任何给定的进程正常启动和运行。例如，Apache 发生故障，Monit 将帮助重启 Apache 进程。它非常容易设置和配置，对于具有数百个微服务的多服务架构尤其有用。如果您使用 Monit，请确保监视它执行的重启，以便发现问题并实现解决方案(而不是仅仅重启并忽略故障)。您可以通过监视 Monit 的日志文件来做到这一点，并确保每次重新启动时都向您发出警告。

### 3.[elk–弹性搜索、日志塔什、kibana](https://www.elastic.co/webinars/elk-stack-devops-environment)—途径 [Logz.io](http://logz.io/?utm_source=devops.com&utm_medium=referral&utm_content=9_open_source_devops_tools&utm_campaign=contributed_article)

[![logz.io](img/9c00a25a24f9ada1d312c38925c59e13.png)](https://devops.com/wp-content/uploads/2015/08/logzio.png)ELK Stack 是现代 IT 界最常见的日志分析解决方案。它将环境中所有服务、应用程序、网络、工具、服务器等的日志收集到一个集中的位置进行处理和分析。我们将它用于分析目的(例如，解决问题、监控服务以及减少解决运营问题所需的时间)。该工具的另一个用途是用于安全和审计(例如，监视安全组的变化和权限的变化)。收到关于这些问题的警报后，很容易对未经授权的用户和活动采取行动。我们还将 ELK 用于商业智能，例如监控我们的用户及其行为。你可以建立自己的麋鹿或购买它作为一种服务。我们已经为社区[写了一个关于使用 ELK 监控你的应用程序性能的指南](http://logz.io/blog/elk-monitor-platform-performance/?utm_source=devops.com&utm_medium=referral&utm_content=9_open_source_devops_tools&utm_campaign=contributed_article)。

免责声明: [Logz.io](http://logz.io/?utm_source=devops.com&utm_medium=referral&utm_content=9_open_source_devops_tools&utm_campaign=contributed_article) 是我们在自己的环境中使用的 ELK-as-a-service。你可以说我们吃自己的狗粮。

### 4.[领事。我](https://consul.io/intro)

[![consul](img/4a122abc4ed7f0353b574e06bf2e169b.png) ](https://devops.com/wp-content/uploads/2015/08/consul.png) Consul 非常适合基于微服务构建的现代弹性应用中的服务发现和配置。这个开源工具利用最新的技术为服务提供内部 DNS 名称。它充当一种代理来帮助您签名和注册名称，使您能够访问服务名称而不是特定的机器。例如，如果您有一个由多台机器组成的集群，那么您可以简单地将它们注册为 Consul 下的一个实体，并轻松地访问该集群。我们称赞这个工具的效率，尽管我们仍然觉得可以用它做更多的事情。如果您也在使用它，那么听听您自己的使用案例就太好了。

### 5.詹金斯

[![jenkins](img/f3bf66f46354d9da59a372b34f9d0f3f.png)](https://devops.com/wp-content/uploads/2015/08/jenkins.png) 大家都知道詹金斯吧？它不是最快也不是最棒的，但是它很容易上手，而且它有一个很棒的插件和附加组件生态系统。它还经过优化，易于定制。我们已经配置了 Jenkins 来构建代码、创建 Docker 容器(参见下一项)、运行大量测试，并推进到试运行/生产阶段。这是一个很棒的工具，但是有一些关于伸缩性和性能的问题(这并不罕见)。我们已经探索了其他很酷的解决方案，如 [Travis](https://travis-ci.org/) 和 [CircleCI](https://circleci.com/) ，它们都是托管解决方案，不需要我们进行任何维护。然而现在，既然我们已经投资了詹金斯，我们将继续投资。

### 6.[码头工人](https://www.docker.com/)

[![docker](img/2f634bfb31473df15bf60de48525b283.png)](https://devops.com/wp-content/uploads/2015/08/docker.png) 关于 Docker 如何改变 IT 环境，我们已经说了很多。这很棒……甚至改变了生活——(尽管我们仍在经历一些挑战)。我们在大多数服务的生产中使用 Docker。通过允许容器从一个地方移动到另一个地方，它简化了配置管理、控制问题和扩展。

我们开发了 SaaS 解决方案，拥有 12 层数据处理管道。通过与 Jenkins 和 Docker 的合作，我们已经能够在一台 Mac 上运行跨所有层的完整管道。说 Docker 没有任何复杂性是错误的，因为即使是小容器也可能需要大量的时间来构建。然而，我们希望确保我们的开发人员尽可能满意，并使他们能够快速工作。由于存储、安全、网络以及与容器相关的一切都涉及管理，这可能是一个挑战。

我们看到 Docker 的进步，并期待着欢迎该公司的新管理和编排解决方案。对于那些可能对 Docker 有疑问的人，我们也编制了一份迁移到 Docker 时的挑战和解决方案列表。

### 7.[可回答的](https://www.ansible.com)

[![ansible](img/c1ed6aabe7a8204ccd512fea0694247b.png)](https://devops.com/wp-content/uploads/2015/08/ansible.png) 还是那句话，简洁是关键。Ansible 是一个类似于 Puppet 和 Chef 的配置管理工具。就个人而言，我们发现这两个对我们的用例来说有更多的开销和复杂性——所以我们决定用 Ansible 来代替。我们知道 Puppet 和 Chef 可能有更丰富的特性集，但是简单性是我们想要的 KPI。我们在使用 Ansible 的配置管理和使用 Docker 容器简单地删除和旋转新的应用程序实例之间看到了一些折衷。使用 Docker，我们几乎从不升级机器，而是选择旋转新机器，这减少了升级我们的 EC2 云实例的需要。Ansible 主要用于部署配置。我们用它来推动变化和重新配置新部署的机器。此外，它的生态系统非常棒，可以轻松编写定制应用程序。

### 8.收集/收集

Collectd/l 是漂亮的小工具，可以收集和存储关于运行它们的系统的统计数据，比其他工具灵活得多。它们允许用户测量多个系统指标的值，并且与其他旨在测量特定系统参数的日志收集工具不同，Collectd/l 可以并行监视不同的参数。我们使用这两个工具来衡量客户绩效参数，并将它们发送到我们的 ELK 即服务平台。我们专门将一个 Collectl 代理封装在 Docker 容器中，并用 Ansible 将它推送到我们所有的服务器上。它每隔几秒钟收集一次信息，然后将其发送到 ELK，以便我们运行报告和发送警报。如果您想了解我们如何在自己的环境中完成这一过程以及其他人如何做到这一点的具体示例，我们[为每个人](http://logz.io/blog/elk-monitor-platform-performance/?utm_source=devops.com&utm_medium=referral&utm_content=9_open_source_devops_tools&utm_campaign=contributed_article)制作了一份指南。

### 9. [Git (GitHub)](https://github.com/)

[![github](img/6c7f128e6234b15b9da4a27d6372eb11.png)](https://devops.com/wp-content/uploads/2015/08/github.jpg)10 年前，随着 Linux 社区对支持分布式系统的 SCM(源代码控制管理)软件的需求，Git 应运而生。Git 可能是目前最常见的源代码管理工具。在内部运行 Git 一小段时间后，我们意识到我们更适合使用 [GitHub](https://github.com) 。除了其强大的分叉和拉请求功能，GitHub 还具有可以与 Jenkins 连接的插件，以便于集成和部署。我认为向现代 it 团队提及 Git 并不是什么新闻，但是由于它对我们的巨大价值，我决定将它添加到列表中。

## 其他选择？

现代 DevOps 世界充满了杰出和独特的开源工具——这是一个弱肉强食的世界。我们发现这里列出的工具是同类中最好的，并认为它们应该包括在每个 DevOps 工程师的候选名单中。

还是我错了？你的工具包里有哪些开源 DevOps 工具？我很想在下面的评论中听到你自己的推荐和经验。