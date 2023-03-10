# TOC 投票决定将 OPA 移入 CNCF 孵化器

> 原文：<https://devops.com/toc-votes-to-move-opa-into-cncf-incubator/>

今天，云计算原生计算基金会(CNCF)技术监督委员会(TOC)投票接受开放策略代理(OPA)作为孵化级托管项目。

OPA, which entered the CNCF Sandbox in March 2018, is an open source, general-purpose policy engine that enables unified, context-aware policy enforcement across the entire stack. It
provides greater flexibility and expressiveness than hard-coded service logic or ad-hoc domainspecific languages and comes with powerful tooling to help anyone get started.

Styra 软件工程师兼 OPA 技术主管 Torin Sandall 表示:“随着企业采用云原生技术的范围扩大，基于策略的控制是必要的。“OPA 在 CNCF 找到了一个理想的家。其他 CNCF 项目可以有选择地集成一致的策略表达和实施机制，以及围绕它的公共工具集。随着我们进入孵化器，我们期待着继续这项工作。”每个组织都有影响整个体系的独特政策。这些政策对长期成功至关重要，因为它们围绕成本、性能、安全性、法律法规等方面编纂了重要的要求。同时，组织通常依赖部落知识和文档来确保策略被正确执行。虽然这些方法容易出错，但它们的存在是因为系统经常缺乏自动化策略实施所需的灵活性和表达能力。
通过 OPA，服务通过执行查询来卸载策略决策，OPA 评估策略和数据以产生查询结果(这些结果被发送回客户端)。策略是用
高级声明性语言减压阀编写的，可以通过文件系统或定义良好的 API 加载到 OPA 中。

“云原生生态系统必须提供灵活的解决方案来控制谁可以在现代微服务部署中做什么，因为传统的策略管理方法无法满足现代环境的要求，”云原生计算基金会首席技术官/首席运营官 Chris Aniszczyk 说。“OPA 通过集成了策略管理的 Gatekeeper 项目，在与 Kubernetes
的集成方面取得了长足的进步。将 OPA 转移到 CNCF 孵化器将提高人们的认识，并鼓励在云原生生态系统内外
开发 OPA 扩展。”OPA 已被用于跨堆栈的几个层在几个不同的域中启用策略的软件:容器管理(Kubernetes)、服务器(Linux)、公共云基础设施(Terraform)和微服务 API(Istio、Linkerd、CloudFoundry)。从 2019 年 1 月开始，Styra、谷歌、微软和其他公司开始联合开发和贡献 OPA Gatekeeper 子项目。Gatekeeper 将 OPA 与 Kubernetes 集成在一起，帮助管理员实施准入控制策略，并审核集群中是否存在违反策略的情况。
Gatekeeper 还包括针对常见使用情形的标准策略库(例如，注册管理机构白名单、入口冲突、标签管理等)。).

网飞使用 OPA 作为一种方法，在云基础设施的数千个实例中跨各种语言和框架的微服务中实施访问控制。在 KubeCon
Austin 2017 上，网飞描述了他们如何围绕 OPA 构建访问控制。OPA 也被 Intuit、Medallia、Chef 等公司用于生产。“在多样化的生态系统中应用访问控制是一项大规模的挑战。如果没有合适的工具，要确保分布在许多应用程序和框架中的所有应用程序都正确且一致地应用授权是不可能的。OPA 使我们能够以一致的方式定义策略，利用这些定义中的复杂数据源，在我们的环境中随处应用它们，并轻松测试它们的正确性。”网飞公司的高级安全工程师伊恩·哈肯说。
OPA 的主要特性:
●分离——管理员可以动态管理策略，而无需对服务进行更改
。
●兼容——RESTful API 使用 JSON over HTTP，因此无论您使用哪种编程语言，您都可以将 OPA 与您的
服务集成。
●响应式——从零开始设计，考虑到延迟敏感型应用，
以最小的性能影响实施策略。
●交互式——任何人都可以使用 OPA 的交互式 shell 快速试验查询
和数据集。
●易于部署——零部署依赖性。它作为守护进程与您的服务并行运行
,并为了高可用性的目的共享它的命运。
●可嵌入——用 Go 编写的服务可以使用 OPA 作为库，不需要运行
单独的守护进程。
显著的里程碑:
● 45 个贡献者
● 1，847 个 GitHub stars
● 52 个发布
● 1，545 个提交
● 151 个分叉
作为 CNCF 主持的项目，加入了 OpenTracing、Fluentd、gRPC、rkt、CNI、Jaeger、公证人、TUF、Vitess、NATS、Linkerd、Helm、Rook、Harbor 等孵化技术，OPA 是与其结盟的中立基金会
的一部分每个 CNCF 项目都有一个相关的成熟度等级:沙盒、孵化或毕业项目。有关每一级技术资格的更多信息，请访问 CNCF 毕业标准 v.1.1

更多关于 OPA 的信息，请访问 https://github.com/open-policy-agent.