# 2021 年最佳–2021 年我们喜爱的 11 款开源 DevOps 工具

> 原文：<https://devops.com/11-open-source-devops-tools-we-love-for-2021/>

随着 2021 年的临近，我们 DevOps.com 想要突出今年最受欢迎的文章。以下是我们 2021 年最佳系列的第八部。

DevOps 不仅仅是一种文化转变——它需要伟大的工具来实现。下面，我们列出了一些当今最受欢迎的 DevOps 工具。但是，向花哨的 SaaS 解决方案投入大量资金会很快吞噬掉云预算。这些 DevOps 工具都是开源的，支持从容器构建和编排到微服务网络、配置管理、CI/CD 自动化、全栈监控等一切。以下是 2021 年我们最喜欢的一些开源 DevOps 工具。

## 1. [Kubernetes](https://github.com/kubernetes/kubernetes)

随着微服务和基于容器的软件的普遍存在，Kubernetes 在今年的开源 DevOps 工具列表中名列榜首也就不足为奇了。Kubernetes 用于编排容器，其采用率在 2020 年上升了 48%。Kubernetes 可以在生产中自动部署、维护和扩展容器组，而不是手动发布微服务。 [Kubernetes](https://kubernetes.io/) ，有时写为 K8s，由云原生计算基金会( [CNCF](https://www.cncf.io/) )托管。

## 2.[码头工人](https://docs.docker.com/get-docker/)

软件 Docker 是一个免费的开源平台，用于构建、发布和运行一个轻量级的应用程序。容器打包了程序运行所需的二进制文件、库、配置文件和依赖项。在过去的十年中，容器在敏捷开发中发挥了关键作用，Docker 容器引领了这场革命。其核心是 [Docker 引擎](https://www.docker.com/products/container-runtime)。 [Docker Hub](https://hub.docker.com/) 也是一个寻找和共享作为容器的预打包函数的优秀资源。此外，为了堵塞容器漏洞，使用[开源容器审计工具](https://techbeacon.com/security/17-open-source-container-security-tools)如 Docker Bench 或 [Anchore](https://containerjournal.com/topics/container-security/methods-to-audit-docker-container-security/) 可能会有帮助。

## 3\. [Istio](https://github.com/istio/istio)

微服务是一种方便的开发风格，但是它们带来了新的开发和架构问题。也就是说，我们如何在所有服务中一致地应用安全、加密、可观察性和遥测元素等网络策略？嗯，[服务网格](https://containerjournal.com/features/when-is-service-mesh-worth-it/)是一个答案。服务网格在每个容器旁边放置一个边车代理，并将这些网络功能抽象到一个控制平面。 [Istio](https://containerjournal.com/topics/container-networking/istio-service-mesh-update-arrives/) 就是这样一个被广泛采用的开源服务网格。Istio 基于 Envoy 构建，向插件和[扩展选项](https://containerjournal.com/features/extending-the-envoy-proxy-with-webassembly/)开放。我们还应该提到 [Linkerd](https://containerjournal.com/features/how-linkerd-approaches-extensibility/) 和[库马](https://containerjournal.com/topics/container-networking/introducing-kuma-the-service-mesh-from-kong/)作为可行的开源服务网格替代方案。

## 4. [GitHub 动作](https://github.com/features/actions)

GitHub 可以说是这个星球上最流行的源代码控制和软件协作平台。GitHub 平台本身，基于 Git，在过去几年中有了一些重大的更新。最值得注意的是 [GitHub 动作功能](https://techbeacon.com/app-dev-testing/github-actions-goes-full-stack-how-put-it-work-your-software-team)。GitHub 动作使 GitHub 上托管的软件包能够接受输入并触发其他进程。这可能有助于自动化 GitHub 中一些很酷的 DevOps 工作流，如代码审查、分支管理或 CI/CD 流程——这里的可能性组合是无限的。GitHub 动作本质上是托管在 GitHub 存储库中的 YAML 文件，利用 GitHub webhooks。虽然这与其说是一个开源工具，不如说是一个特性，但是我们觉得在这里包含它是很重要的。Actions 对公共存储库是免费的，限制为 100 个操作。

## 5.詹金斯

DevOps 哲学的很大一部分是寻找更有效地自动化和部署新迭代的方法。这个目标的一部分是创建一个简化的持续集成和持续交付(CI/CD)管道。Jenkins 是一个开源的自动化服务器，拥有数百个插件来自动构建、部署和测试软件项目。虽然 GitHub Actions 理论上可以在未来取代 CI 服务器，但是像 Jenkins、[circle CI](https://circleci.com/docs/)、[TravisCI](https://travis-ci.org/)和[git lab Community Edition](https://about.gitlab.com/blog/2016/07/20/gitlab-is-open-core-github-is-closed-source/)这样的 CI 工具仍然是许多 DevOps 团队的首选。

## 6.[普罗米修斯](https://github.com/prometheus/prometheus)

度量和警报系统对于[站点可靠性工程师](https://devops.com/how-the-sre-role-is-evolving/)可视化应用和对问题做出反应至关重要。 [Prometheus](https://prometheus.io/) ，一个毕业于 CNCF 的项目，是一个广受欢迎的开源监控解决方案。Prometheus 服务器通过抓取 HTTP 端点来收集时间序列指标，并生成一个系统来与这些数据进行交互，提供深度查询、可视化、存储和其他功能。查看这个[令人敬畏的普罗米修斯名单](https://github.com/roaldnefs/awesome-prometheus)，获取普罗米修斯介绍和其他资源。

## 7.[可回答的](https://github.com/ansible/ansible)

Ansible 是关于自动化的。Ansible 是一个由 Red Hat 赞助的开源项目，可用于自动化云供应、联网、部署、配置管理和其他任务。Ansible 有一个简单而有效的架构，相对容易组装——你所需要的只是一个文本编辑器和命令行。您在文本文档中描述您的基础设施，并在行动手册中组织您想要的状态。实践中的例子，请看 [OpenIO 如何使用 Ansible](https://www.openio.io/blog/why-and-how-we-use-ansible) 。“Ansible 不仅是我们部署 OpenIO 核心的标准工具，也是我们的 WebUI、OIO-FS 和所有即将推出的选项的标准工具，”OpenIO 运营部门的 Cédric Delgehier 写道。

## 8.[厨师](https://github.com/chef/chef)

Chef 是另一个用于自动化配置管理的基础设施即代码(IaC)解决方案。Chef 使用 Ruby 来自动化服务器配置，并与所有主要的云服务提供商(CSP)合作良好。这在创建和配置大量机器时非常有用。像这个列表中的其他自动化工具一样，用户以声明的格式描述它们的组件和状态。在 Chef 中，这些被称为“食谱”，可以组合成“食谱”不能因为不切题就 diss 大厨！

## 9.[地形](https://github.com/hashicorp/terraform)

Terraform 是另一个 IaC 工具，可用于使用配置文件启动构建、版本控制和进一步自动化。GitHub 上的描述是“Terraform 是一种安全高效地构建、更改和版本化基础设施的工具”。Terraform 遵循用户用高级语法创建的“执行计划”。Terraform 的一个独特之处在于它强调版本化——这允许您像对软件一样对服务的蓝图进行版本化。

## 10\. [JAMStack](https://jamstack.org/)

正如我之前提到的， [JAMStack](https://devops.com/jamstack-boards-the-enterprise/) 结合了 JavaScript、API 和 markdown 来构建基于 web 的应用程序。虽然更多的是一种“无头开发”方法，而不是单一的开源工具，但 JAMStack 项目通常是使用开源组件构建的。例如，JAMStack 经常利用开源的无头内容管理系统，如 Ghost、Strapi 和/或 Netlify CMS。

## 11.[各堆叠](https://www.elastic.co/elastic-stack)

[ELK Stack](https://www.guru99.com/elk-stack-tutorial.html) 是由 Elastic 维护的三个开源项目的联合:Elasticsearch、Logstash 和 Kibana。有了这三个组件，开发人员可以从任何来源获取和记录数据，并创建有用的可视化效果。这种集中式日志记录是通过 NoSQL 数据库实现的，该数据库通过 Elasticsearch 进行存储，通过 Logstash 进行处理和数据收集，通过 Kibana 进行可视化。提高可见性对于数据分析至关重要，有助于识别错误以缩短平均恢复时间(MTTR)。

## 完善 2021 年开发运维工具链

编程不仅仅是交付高质量的代码，它还关乎高效的执行。这种全面改善运营的驱动力是真正的[将运营融入一切](https://devops.com/could-no-code-enable-everything-ops/)。有了出色的开源 DevOps 工具，这意味着越来越多的架构师可以在他们的部署模型中采用 DevOps 方法。

DevOps 作为一种实践，以及它的底层技术，总是在不断发展。在 2021 年，大量的努力被放在争论引入微服务开发风格的影响上。结果，我们注意到容器编排器和服务网格的成熟。蓝图化基础设施即代码并创建[自动化、可重复的配置](https://devops.com/report-the-state-of-devops-automation/)是实现自动化构建和发布管道的另一个必备条件。更不用说，许多[无代码和低代码平台](https://devops.com/low-code-makes-api-testing-more-accessible/)正在向非程序员开放 DevOps 功能，尽管是从专有的角度。

值得注意的是，一些流行的开源 DevOps 工具已经被收购——如 Docker 和 Chef——模糊了他们的业务和他们的开源根源之间的界限。当谈到开源工具时，采用供应商中立的工具是一个很好的实践，有代表不同利益相关者的[坚实的社区支持](https://containerjournal.com/features/five-values-that-define-kubernetes-culture/)。这将有助于您的项目经得起未来考验。即使开源是“免费”的，用户也必须确保[的好处超过上线时间](https://containerjournal.com/features/when-is-service-mesh-worth-it/)以及自托管的运营开销。

DevOps 工具有利于自动化软件部署。在这里，我们试图列出一些最令人兴奋的工具来帮助自动化这一过程。当然，许多新的工具正在 DevOps 领域出现，我们还没有触及表面。你有没有上面没有提到的最喜欢的 DevOps 工具？请在下面的评论中告诉我们！