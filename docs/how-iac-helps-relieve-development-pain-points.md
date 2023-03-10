# IaC 如何帮助缓解开发难点

> 原文：<https://devops.com/how-iac-helps-relieve-development-pain-points/>

开发人员每天花大量时间挖掘系统内部，为应用程序分配存储，将安全系统连接到用户界面，以及跟踪应用程序的版本在开发周期中的位置，等等。

这就是为什么出现了一种新的软件类别， [基础设施即代码](https://devops.com/infrastructure-as-code-iac-why-collaboration-is-key/) (IaC)，它承诺自动化系统基础设施供应和集成。它释放了时间，因此开发人员可以将更多精力放在前端解决方案上，而不是后端配置管理上。不过，首先让我们了解一下什么是 IaC，以及它如何帮助你的组织。

## 什么是基础设施即代码(IaC)？

IaC 通过使用成套工具、协议、语言和流程，减少了系统基础设施的创建和配置时间。在传统的数据中心系统管理中，每个配置条目和更改都需要手动操作。现在，技术团队可以以智能、自动化的方式管理一切。

借助 IaC，基础设施配置管理数据存储在标准化文件中。这些工具监控和维护基础设施的状态，并确保在应用程序运行时有合适的资源可用。这将 DevOps 团队从过多的手工劳动中解放出来。本质上，大规模配置和管理变得非常简单。

## 开发痛点

目前，发展是一个繁琐的过程，因为摩擦在许多地方出现。在加速应用程序开发的前端——构建特性集——方面已经取得了很大的进步。尽管如此，当软件组件被绑定到计算机基础设施时，这个过程在后端会变慢。

从历史上看，软件是作为一个大型的整体代码块来部署的。更新是乏味的，因为应用程序的所有代码都必须运行，即使它不涉及更新或错误修复。容器和微服务的出现使开发人员能够设计模块化的应用程序，因此更容易更新、添加或调试。

但是，该应用程序仍然必须绑定到现有的计算基础架构中。云解决方案——例如 AWS、谷歌云平台或微软 Azure——为公司提供了快速获得大量计算处理能力的途径。但应用软件必须被告知如何访问网络、提供安全信息、分配存储空间以及在中央服务器上运行代码。

因此，开发人员花费大量时间构建和维护基础设施代码。为此，他们使用 Python 等语言和 Chef、GitHub 等解决方案。他们希望使用自动化来简化和加快流程，但在这里，他们再次遇到了一些障碍。

### 工作流程瓶颈

随着应用程序变得越来越大，组件变得越来越小，开发人员发现他们自己混合和匹配来自各种各样地方的软件。跟踪流程中的内容是一项常见的挑战。当前的工作流通常不直观，并且严重依赖于拉取请求。一些解决方案试图解决多个工作空间的问题，但最终结果是脆弱和不确定的代码。

如果没有将项目映射到分支或标签，对批准的拉请求进行评论的人就可以将未批准的代码推向生产。在今天快节奏的 DevOps 工作环境中，一个本来是用于短期测试运行的批准变成了当前的版本，产生了意想不到的后果的连锁反应，产生了混乱和有缺陷的代码，大大减慢了开发速度。

### 访问控制

大多数工具不提供访问控制模型。例如，开发人员可以跟踪单个存储库和单个 Terraform 项目，但是随着存储库和项目数量的增长，确保适当的访问控制功能变得更加困难。

### 工作空间挑战

遗留瀑布和静态开发项目允许 IT 团队建立一次他们的系统基础设施，然后忘记它。但在动态环境中，微服务转瞬即逝。新环境激增，产品团队必须不断地配置他们自己的工作区，这消耗了时间和资源。

### 漂移检测

通用的 IaC 平台不提供检测基础设施是否处于[](https://spacelift.io/blog/drift-detection)漂移的机制。因为如此多的配置是在运行时完成的，所以基础设施的期望状态和实际状态之间会出现差异。

漂移有许多原因，例如开发人员或机器脚本意外事件或系统资源的缺乏。太大的漂移会导致应用不稳定。在开发周期的早期发现这样的问题比试图修复生产系统更有效。但是通常缺乏必要的可见性，只有当系统完全投入使用时，缺点才会变得明显。

### 资源可视化

鉴于当今的动态环境，开发人员需要清晰的可见性。他们必须能够仔细检查作业运行时发生的情况。尽管 CI/CD 平台提供了许多优势，但它们很少从实时或历史的角度提供对资源使用情况的洞察。

因此，每当出现性能问题时，这些平台很少提供关于问题来源或如何解决问题的见解。因此，开发人员的注意力从应用程序增强转移到故障排除上。

### 缺乏可重用性

遗留基础设施无法让团队跨多个环境重用可靠的系统映像。为了解决这个问题，团队经常为每个应用程序的每个版本创建一个新的映像，从而减慢开发时间。

### 高价

手动设置每个 IT 环境需要时间和人力，这增加了成本。公司必须有专门的工程师团队负责创建基础设施。但他们也需要主管和数据中心资源，这最终会增加技术支出。IaC 工具集中管理流程并创建合适的环境。这样，组织只需为他们真正需要的系统资源付费。

## IaC 如何改进业务？

[传统 IT 实践](https://devops.com/saying-goodbye-to-legacy-systems/) 昂贵、缓慢且不一致，因为它们严重依赖手动输入。基础设施即代码自动化了大部分基础设施管理流程，带来了一系列好处。

### 速度

借助 IaC，资源调配和管理比手动系统更快、更高效。环境的基础设施是用代码定义的。基于代码的基础设施极大地加速了软件开发和交付周期的每个阶段。因此，DevOps 团队在提高软件质量的同时，更快、更大规模地交付应用。

### 一致性

IaC 持续部署一致的配置，没有任何差异。因此，它能够快速交付一致的基础架构和环境。这减少了错误和开销，同时提高了生产率。

### 消除管理开销

基础设施自动化有助于减少参与软件开发过程路由部分的人员数量。这是因为网络和存储管理不需要人力资源。公司将员工解放出来，从事更具战略性的计划。

### 减少风险和错误

IaC 有助于降低风险和避免人为错误。它还可以防止运行时问题和由于缺少依赖关系或配置偏差而导致的安全缺陷。

### 能见度

开发人员对 IaC 配置文件的版本控制方式与他们对任何其他源代码文件的版本控制方式相同。这给了他们任何变化的完全可追溯性。通过这种方式，IaC 确保了高效、异常透明的工作流程，并加快了开发过程。

## 寻找 IaC 解决方案

维护传统基础架构是一个耗时、复杂的过程。 [IaC 正在成为](https://spacelift.io/blog/business-benefits-of-iac) 的解决方案，它减轻了开发团队日常感受到的压力和痛苦。现在，他们可以加快系统资源到应用程序的部署和连接。开发人员可以变得更加高效，并使公司能够以更快、更可靠和更具成本效益的方式响应业务需求。开发过程不再拖业务的后腿。