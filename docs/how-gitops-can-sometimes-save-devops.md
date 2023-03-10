# GitOps 如何(有时)拯救 DevOps

> 原文：<https://devops.com/how-gitops-can-sometimes-save-devops/>

自从一年多前 Weaveworks 发布 GitOps 以来，已经有很多关于 GitOps[的文章，作为“整个系统的单一事实来源”,用于在云上使用 Git 进行 Kubernetes 部署。](https://www.weave.works/technologies/gitops/)

被[Alexis Richardson](https://uk.linkedin.com/in/richardsonalexis)，[weave works](https://www.weave.works/)联合创始人兼首席执行官恰当地描述为“90%的最佳实践和 10%的酷新东西”，GitOps 在很大程度上为 Kubernetes 上的 DevOps CI/CD 部署提供了一个框架。这是许多 Kubernetes 管理发行版中经常被忽略的东西——因此，它很受欢迎。

该工具对于没有采用 Kubernetes 的组织来说显然没有用，但在许多方面，它使组织的 [DevOps](https://en.wikipedia.org/wiki/DevOps) 通过以一种更有纪律和更专注的方式运行 Git，更有效地利用 [Kubernetes](https://kubernetes.io/) 。

[企业管理协会(EMA)](https://www.enterprisemanagement.com/) 的分析师 [Torsten Volk](https://www.linkedin.com/in/torstenvolk) 说:“GitOps 背后的想法是最大化开发人员花在高效编码上的时间，而不是担心如何使用最新的源代码，将他们保存的代码合并回库中，并持续支持应用程序构建过程中出现的问题。

GitOps 为 DevOps 提供了一种使用其版本控制功能来归档应用程序部署变更的方法，这种方法允许在以后调用这些变更。当体系结构出现故障，并且需要访问和恢复事故发生前的应用程序部署或更新的先前版本时，这就很方便了。所有的变更都被标记和存档，使得每个开发人员都知道他们对应用程序的变更是何时以及如何被更改的。

Volk 说:“理想情况下，每个开发人员都会签入他们的代码，并收到一个链接，链接指向正在运行的应用程序，其中包含他或她最新应用的更改，以及所有其他已签入存储库的更改。
![](img/ca795cfa02a684fd6e35d2966d921d09.png)

## 领养清单

Volk 提出了他认为 DevOps 在采用 GitOps 之前应该具备的以下要素:

Volk 说，所有的基础设施和应用程序配置，包括数据库、中间件和机器学习模型，都需要定义为代码。

他说:“每个人都必须接受一个基本概念，即只有当成功构建的所有组件都被签入 Git 时，代码才是完整的。”CLI 驱动的临时部署不再被接受

—devo PS 组必须能够检测到应用程序代码的变化，这些变化以前可能绕过 Git。沃尔克说，因此，必须有一个适当的程序，使这些变化回到 GitOps 的控制之下。

他说:“IT 运营/开发团队需要专门通过更改登记到 Git 中的代码来对应用程序进行操作更改。”。“这意味着诸如扩展、故障切换、创建维护窗口等任务。以及紧急故障排除任务都必须通过 Git 运行。后者尤其棘手，因为企业不会因为 GitOps 而接受更长的[【MTTD】](http://kpilibrary.com/kpis/mean-time-to-detect-mttd-2)[平均检测时间和【MTTR】](https://en.wikipedia.org/wiki/Mean_time_to_repair)

在开发和运营中必须使用声明性管理实践。“这已被证明是一个关键的路障，”沃尔克说。“Kubernetes 开发人员，作为开发和运营的一部分，仍然经常更喜欢命令式管理的控制，而不是定义他们想要的最终状态并让软件处理如何实现的承诺。”

对于具备上述先决条件的 DevOps 团队来说，使用 Git 在云上运行 Kubernetes 部署至少值得一看。然而，对于那些出于正当理由采用 GitOps 的组织来说，它并不是一个通用的解决方案，组织需要对其进行修改以满足他们的需求。例如，在使用它在云平台上运行 Kubernetes 和 Prometheus 遥测数据库两年后，与 Weaveworks 描述的功能相比，它的实现几乎肯定会有所不同。

因此，DevOps 需要积极参与 GitOps 的部署和维护，以确保其满足组织的个性化需求。当第一次描述 GitOps 时，Weaveworks 的 [Richardson](https://uk.linkedin.com/in/richardsonalexis) 写道:“公平的警告:这是对我们有用的，亲爱的读者，你可能不同意。”

— [B .卡梅伦增益](https://devops.com/author/b-cameron-gain/)