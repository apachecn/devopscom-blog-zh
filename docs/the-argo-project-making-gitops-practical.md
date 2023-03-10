# Argo 项目:使 GitOps 实用化

> 原文：<https://devops.com/the-argo-project-making-gitops-practical/>

如果你是一名 DevOps 工程师，你可能至少听说过" [Argo](https://argoproj.github.io/cd/) "这个名字，见过这个友好的 squid 标志，并且想知道:每个人都在谈论的这个工具到底是什么？

简而言之，Argo 是一个流行的开源工具，它使得 GitOps 对于任何使用 Kubernetes 的人来说都是实用的。但远不止这些，因为通过启用 GitOps，Argo 还将使 Kubernetes 环境比以往任何时候都更加健壮、安全和可靠。

让我们来看看为什么 Argo、GitOps 和优秀的 DevOps 工程师的组合是生产灵丹妙药。

## 什么是 GitOps，它会取代 DevOps 吗？

GitOps 是开发团队用来管理基础设施和部署应用程序的新(更)流程和范例。GitOps 中的“Git”指的是流行的开源版本控制系统。GitOps 使用 Git 作为声明性配置的单一信息源。基于这种声明式配置，它发挥了它的魔力。

GitOps 使用 Git pull 请求自动管理基础设施的配置和部署。当开发团队对 Git 配置进行更改时，部署在环境中的 GitOps 代理会自动将更改与实时状态进行协调。对活动环境的每一个更改都在 Git 存储库中被捕获，因此团队对系统更改拥有前所未有的可见性和可审计性。最重要的是，如果生产中出现问题，回滚到以前的工作版本是很容易的。

GitOps 建立在开发人员经验的基础上，使团队能够使用与开发软件相同的工具和流程来管理他们的基础设施，并将这些工具扩展到软件部署和基础设施管理领域。

虽然有些人将 GitOps 吹捧为“DevOps 2.0”，但许多专家不同意，他们说 GitOps 不是 DevOps 的更好版本，也不是完全取代 DevOps 的东西。GitOps 是一种技术实践，对 DevOps 团队非常有益。DevOps 工程师不会像一些人担心的那样被 Git 触发的机器人取代。但是 GitOps 会让她和她支持的开发者更快乐，更有效率。

## Argo 项目是什么？

[Argo](https://www.cncf.io/projects/argo/) 是一个由云计算本地计算基金会(CNCF)托管的开源项目，用于以 Kubernetes、GitOps 风格构建和管理连续交付工作流。Argo 的独特之处在于它是 Kubernetes-native——完全为现代集装箱化环境而设计。

阿尔戈项目由四个主要的次级项目组成:

*   **Argo CD**—具有强大 GUI 和 CLI 的 GitOps 连续交付引擎。
*   **Argo Workflows**—支持工作流和有向无环图(Dag)的工作流引擎，其中每个流程阶段都是一个容器。
*   **Argo Rollouts**—一种先进的 Kubernetes 部署引擎，支持渐进式交付策略，如 canary 和 blue/green 部署，这在普通的 Kubernetes 中很难实现。
*   **Argo Events**—Kubernetes 基于事件的依赖管理系统，可用于触发 CI/CD 管道中的自动化工作流。

## 生产中对 Kubernetes 的要求

Kubernetes 是一个编排平台，可以帮助部署、扩展和管理容器化的应用程序。它可以管理容器和底层基础设施—调度容器并管理其工作负载。这种能力集成了软件开发和平台管理，以改进应用程序管理和可移植性。

生产中的 Kubernetes 可以提供许多优势。例如，它使发布对高可用性应用程序的频繁更改同时保持它们在线成为可能，并使您能够将应用程序从一个集群移动到另一个集群。然而，您需要正确地配置 Kubernetes 来实现它的潜力。

为生产配置 Kubernetes 包括根据每个用例实现需求。因此，在一个 Kubernetes 项目中，什么是“生产就绪”在不同的用例之间可能会有很大的不同。然而，仍然有适用于大多数用例的最低要求。以下是 Kubernetes 在生产中的关键要求:

*   **安全**——当 [为生产](http://www.tigera.io/learn/guides/kubernetes-security/) 保障 Kubernetes 时，你需要最小化攻击面。这意味着锁定 Kubernetes 控制平面、应用程序及其相关数据。您需要保证机密的安全，强化节点，使用基于角色的访问控制(RBAC)，并使用最新的安全更新保持 Kubernetes 版本的更新。
*   **可移植性和可扩展性**—您可以通过保持可移植性和可扩展性来最大限度地提高集群性能。Kubernetes 有许多功能可以帮助您实现这一目标，包括自我修复节点和自动扩展基础设施。
*   **部署速度** —Kubernetes 通过自动化相关流程加快了基础设施和应用程序的管理。您可以将 Kubernetes 的自动化特性与 GitOps 结合使用，以提高 CI/CD 管道的部署速度。
*   **灾难恢复**—通过结合使用 Kubernetes 和 GitOps，您可以显著缩短平均恢复时间(MTTR)。GitOps 可以帮助您将 MTTR 缩短到几分钟，并在集群完全崩溃的情况下快速轻松地重建您的容器基础架构。
*   **持久性**—为了支持有状态的生产应用程序，您需要配置 [Kubernetes 持久性卷](https://cloud.netapp.com/blog/kubernetes-persistent-storage-why-where-and-how) ，为存储设备提供多个存储层，并确保它们得到有效利用。
*   **可观察性**—可观察性使您能够获得运行服务的高级视图，帮助您在部署前做出明智的决策以降低风险。GitOps 可以帮助您持续监控 Kubernetes 部署，确保您可以在出现问题时立即采取行动。

## Argo 工具对生产环境的好处

### 阿尔戈光盘

[Argo CD](https://argoproj.github.io/cd/) 是 Kubernetes 原生的持续交付(CD)工具。虽然大多数 CD 工具只支持基于推的部署，但 Argo CD 以拉模式工作，从 Git 存储库中检索更新的代码，并将其直接部署到 Kubernetes 资源。这使得开发人员可以在一个系统中管理基础架构配置和应用程序更新。

Argo 光盘的主要特点包括:

*   将 Kubernetes 集群中的应用程序状态与 Git 存储库中声明性配置的当前版本自动同步(==GitOps)。
*   能够可视化部署问题并检测和修复错误配置。
*   方便的基于 web 的 GUI 和 CLI。
*   基于角色的访问控制(RBAC)和单点登录(SSO)，包括通过 GitHub、LinkedIn、微软等登录。
*   支持 webhooks 触发 GitLab、GitHub 和 BitBucket 中的动作。

【Argo CD 如何让 Kubernetes 制作就绪？

GitOps 可以帮助您在 Kubernetes 中实现真正的 GitOps 工作流，这在生产环境中提供了以下好处:

*   **最大限度地减少失败的部署并快速从停机中恢复**—如果生产中出现任何问题，Argo CD 可让您立即恢复并轻松回滚，将恢复时间缩短到几秒钟。
*   **内置审计历史** —Argo CD 确保对 Kubernetes 集群的每一次更改都以 Git 配置更改日志的形式进行审计。这提供了一个完整的审计线索，可以跟踪谁在集群中更改了什么，从而实现一致的操作并支持法规遵从性要求。
*   **提高已开发功能生命周期的可见性** —Argo CD 提供了从基础设施或应用程序的每次变更到导致这些变更的代码提交的可追溯性。
*   **增强的安全性** —Argo CD 提供了强大的安全保证，利用强大的加密技术来管理变更和验证作者身份，并在 CI 环境和生产系统之间建立了完全的隔离，消除了许多类型的供应链攻击。

### 阿尔戈推出

[Argo Rollouts](https://codefresh.io/learn/argo-rollouts/) 是一组 Kubernetes 控制器和 CRDs，提供高级部署功能，如在 Kubernetes 环境中的蓝/绿和金丝雀部署、实验和渐进交付。它可以与输入控制器和服务网格集成，以便在更新期间逐渐将流量转移到新版本。

Argo 部署的一个关键功能是，它可以查询和解释来自许多来源的指标，以验证部署是否正常工作，并执行自动升级或回滚。

**Argo 的推出如何为 Kubernetes 的生产做好准备？**

默认情况下，Kubernetes 提供使用“滚动更新”策略更新应用程序的部署对象。在大型生产环境中，滚动更新被认为风险太大，因为无法控制部署速度，也无法在出现故障时自动回滚。

另一个限制是，Kubernetes 部署不能查询外部指标来确定部署是否成功，例如真实的用户性能或参与度测量。

Argo 的推出可以解决所有这些挑战，并在 Kubernetes 环境中实现完全渐进式交付，而不需要复杂的配置。

### Argo 工作流

Argo Workflows 是一个开源的本地容器工作流引擎，用于在 Kubernetes 上编排并行任务。Argo 工作流作为 Kubernetes 自定义资源定义(CRD)来实现。

阿尔戈工作流程的主要特点包括:

*   定义工作流，其中工作流中的每个步骤都是一个容器。
*   将多步骤工作流建模为一组操作或 Dag，以捕获依赖关系。
*   在 Kubernetes 上本地运行 CI/CD 管道，无需配置复杂的软件开发产品。

**Argo 工作流程如何使 Kubernetes 生产就绪？**

Argo Workflows 允许您在任何 Kubernetes 环境中自动执行生产工作流，无论是内部部署、混合云还是多云环境。它消除了手动流程，并确保自动化被表示为声明性配置，使其一致、可重复、易于回滚和易于故障排除。

### 阿尔戈事件

Argo Events 是一个基于 Kubernetes 事件的依赖项管理器，它为不同的事件源定义了多个依赖项(例如 webhook、S3、时间表、流等)。)和 Kubernetes 对象。帮忙扣扳机。

阿尔戈事件本身不是很有用。为了交付价值，您需要与能够执行工作流步骤的系统集成。因此，您可以使用 Argo 工作流来设置 Argo 事件。这有助于协调平行的 Kubernetes 工作。

**Argo 事件如何让 Kubernetes 做好生产准备？**

Argo Events 提供了多种功能，可在 Kubernetes 生产环境中实现依赖性管理:

*   管理各种事件源的依赖关系。
*   定制业务级约束逻辑以解决事件依赖性的能力。
*   管理从简单的线性实时依赖关系到复杂的多源批处理作业依赖关系的一切。
*   符合 CloudEvents 标准。
*   能够在运行时管理事件源。

## 结论

在本文中，我介绍了 GitOps 和 Argo 项目的基础知识，并展示了 Argo 项目的每个关键模块如何帮助开发人员和 DevOps 工程师以最少的工作量使 Kubernetes 产品化。Argo 的神奇之处在于它的简单性，以及它与现有 Kubernetes 工作流程无缝结合的方式。我希望这将鼓励您尝试它，看看它是否能对您组织的生产问题有所帮助。