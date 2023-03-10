# 问答:Sematext 关于 Docker 监控的提斯，第 2 部分

> 原文：<https://devops.com/qa-sematext-thies-docker-monitoring-part-two/>

在我与斯蒂芬·提斯对话的第一部分， [Sematext](http://www.sematext.com) DevOps 专家。我们谈到了[码头工人](https://www.docker.com)对 Sematext Logsene 日志记录、异常检测和警报软件以及 SPM 监控软件的使用。让我们继续谈话。

**David Geer:** 是什么让 Logsene 集中化？典型部署集中在哪里？it 集中化的优势是什么？

**提斯:**传统上，系统会在每台服务器上存储来自多个应用程序的日志。这使得出于故障排除或审计目的而搜索日志变得困难。为了找到相关的日志条目，操作员必须登录到每个服务器，在该服务器上找到正确的文件，并在该文件中搜索相关的消息。

这可能需要几分钟的时间。由于系统将日志存储在多个服务器上，很难关联数据，因此几分钟的时间可能会变成令人沮丧的数小时根本原因查找会议，通常涉及多个团队成员。Logsene 为来自多个服务器和应用程序的所有日志数据提供了一个中央全文索引。不需要登录到多个服务器并搜索/grep 多个日志文件。所有团队成员同时看到所有数据，可以更有效地协作。

有了一个集中的搜索位置，可以更轻松地快速查找日志、运行分析查询或将警报规则集中在一个位置。

Logsene 为 Docker 日志做了什么？

**提斯:**Docker 的 Sematext 代理与 Docker API 交互，以自动收集、解析和处理日志、指标和事件。它会自动检测容器(无需设置或配置新容器！)并支持 [Docker Hub](https://hub.docker.com/) 上应用的多种日志格式，如 [Nginx](https://www.nginx.com/) 、 [Apache](https://www.apache.org) 、 [Elasticsearch](https://www.elastic.co/) 、 [Solr](https://lucene.apache.org/solr) 、 [MongoDB](https://www.mongodb.org) 、 [MySQL](https://www.mysql.com) 等等。

**Geer:** 你的说法是什么意思，“一些 DevOps 工程师甚至认为 Logsene 是‘类固醇上的麋鹿栈’”？

**提斯:**ELK Stack 是开源工具的组合:Elasticsearch、 [Logstash](https://www.elastic.co/products/logstash) 和 [Kibana](https://www.elastic.co/products/kibana) 。这些工具在日志传送(Logstash)、索引和搜索(Elasticsearch)以及可视化(Kibana dashboards)方面非常流行。但是，这些工具缺少许多企业功能，如多用户用户界面、基于角色的访问控制、日志的安全传输或开箱即用的配置，以及用于搜索日志的简单查询语言。这就是 Sematext Logsene 将相关的企业特性添加到这些开源工具中的地方，以使它们易于使用并安全地集成到企业信息技术基础架构中。

对许多人来说，维护 Elasticsearch 集群是另一个问题。这需要很多专业知识。使用 Logsene 不需要这种专业知识。Logsene SaaS 提供了一个管理解决方案，用户不需要知道任何关于维护弹性搜索集群或所需的基础设施。Sematext 会帮他们处理的。Sematext 客户可以从这些托管服务中受益，并且只需支付自托管 ELK 堆栈成本的一小部分，在自托管 ELK 堆栈中，存储、计算和网络基础设施以及高技能员工的人力都很重要。

**Geer:**Tutum 是什么？在 Tutum 上轻松启动 SPM 和 Logsene Docker 有什么重要的？

**提斯:**[Docker 2015 年收购 Tutum](http://blog.tutum.co/2015/10/21/dockertutum/)。Tutum 以云服务的形式提供 Docker 容器的管理。Tutum 是一个操作“Dockerized”应用程序堆栈的平台。对于 Docker 的 Sematext 代理，Tutum 集成会在几秒钟内将 Sematext Docker 代理自动部署到所有集群节点。这些节点可以运行在不同的云平台上，如亚马逊、[、数字海洋](https://www.digitalocean.com/)、 [Rackspace](http://www.rackspace.com) 或本地。对于运行大型基础架构或混合云的人来说，这又是一个巨大的时间节省器。支持 Docker 产品并与 Docker 产品进行出色的集成对于 Sematext 来说非常重要。

Sematext Docker 代理运行在 Docker 提供的所有解决方案上，例如 Docker Swarm 和其他解决方案，如 Google [Kubernetes](https://kubernetes.io/) ，Google [Container Engine](https://cloud.google.com/container-engine/) ， [RancherOS](http://rancher.com/rancher-os/) ， [CoreOS](https://coreos.com/) ，Amazon [ECS](https://aws.amazon.com/ecs/) 或 Hashicorp [Nomad](https://www.hashicorp.com/blog/nomad.html) 。

**Geer:** 请讨论一下 Sematext Docker 和 Docker image？

**提斯:** Sematext Docker 映像在 Docker Hub 上可用，我们在 Stackfiles.io 上为 Sematext Docker 共享了 Tutum Stackfile，最简单的获取方式就是使用 Sematext，它会为你生成 Stackfiles，包括令牌。

Docker Hub 是公共应用程序映像(包括相关安装说明)的中央注册表。Docker 用户可以借助 Docker Hub 中的指令快速找到如何运行“Docker 化”的应用程序。通常，这需要在使用正确的设置启动容器之前做一些配置工作。

Stackfile.io 是人们共享预配置的应用程序堆栈(例如，web 服务和所需的数据库)的地方。Sematext 为 Sematext Docker 代理提供了一个预配置的设置，用于监控 Tutum Cloud 中的所有容器。这意味着只需单击所选的堆栈文件，并输入应用程序的唯一标识符(令牌)，就可以启动 Sematext Docker 代理并监控 Tutum Cloud 中运行的所有容器。这就是全部的代价。

当您登录 Sematext SPM 或 Logsene 时，一般安装说明会显示所有必需的配置。Sematext 用户可以简单地复制/粘贴相关命令，包括其应用程序的唯一标识符(令牌),以部署 Sematext Docker 代理。这也为我们的用户节省了大量时间，他们只需几分钟就可以启动并运行。