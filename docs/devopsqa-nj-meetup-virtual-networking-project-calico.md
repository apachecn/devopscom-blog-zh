# DevOpsQA NJ Meetup–与 Calico 项目的虚拟网络

> 原文：<https://devops.com/devopsqa-nj-meetup-virtual-networking-project-calico/>

[![devopsqa1](img/9d79f4f173d1a7d76c13504cdd146888.png) ](https://devops.com/wp-content/uploads/2015/04/devopsqa1.jpeg) [DevOpsQA NJ](https://www.meetup.com/DevOpsandAutomationNJ/) 在虚拟网络上举行了我们四月份的聚会，Christopher Lijenstolpe 是演讲人。meetup 在新的地点举行，这是一个俯瞰纽约市的最先进的办公场所，由 [Ishi Systems](http://www.ishisystems.com/) 提供。

Christopher 是 Metaswitch Networks 的解决方案架构总监，也是 Project Calico 的原始架构师。在加入 Metaswitch 之前，Chris 负责包括南极洲在内的全球网络。

我们详细了解了 Project Calico，它是 Apache 许可的纯第 3 层网络解决方案，适用于容器、虚拟机和混合环境。它的座右铭是可扩展、简单、开放，从表面上看，它符合所有这三个标准。

Chris 首先向我们介绍了标准虚拟网络模型，并展示了当今网络系统不必要的复杂性。虽然所有这些系统都试图解决大量假设的需求，但唯一真正的需求是建立通信。这种复杂性导致了各种问题，例如脆弱的连接、较差的性能、低效的资源利用以及故障排除的困难。当涉及到容器时，这些问题被显著放大。

那么什么是卡利科计划？正如 Christopher 简单解释的那样，它建议利用 3 个关键组件(BGP、IP 和策略)构建像互联网一样的数据中心。用克里斯托弗的话说，“印花布项目如此简单，很难相信以前没有人想到它”。这是真正创新解决方案的真正标志。如果你想在 OpenStack 或 Docker 上试用 Project Calico，你可以在[http://projectcalico.org](http://projectcalico.org)阅读更多信息，或者直接通过 [【电子邮件保护】](/cdn-cgi/l/email-protection#1e7d766c776d6a716e767b6c5e6e6c71747b7d6a7d7f72777d7130716c79)[![Project-Calico-logo-456x456-no-text](img/404e34bbd648f5b5174dfcc59c08a724.png)](https://devops.com/wp-content/uploads/2015/04/Project-Calico-logo-456x456-no-text.png) 联系克里斯多佛