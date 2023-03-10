# 如何协调您的开发运维与云计划

> 原文：<https://devops.com/align-devops-cloud-initiatives/>

基础设施即代码(IaC)实践通过基础设施或平台云(IaaS 或 PaaS)成为可能，解决了许多与持续交付和开发运维相关的重要问题。因此，在私有云、混合云或公共云模式中实施 IaaS 和 PaaS 应始终与您的开发运维计划保持一致。在之前的一篇文章中，我认为 OpenStack 是 DevOps 的理想栖息地。毕竟，OpenStack 是由软件开发和托管领域的一些最大的公司以及数以千计的个人社区成员支持的。事实上，许多人认为 OpenStack 是云计算的真正未来。但是，云环境也可能基于专有的 VMware 技术、混合 Amazon Web Services (AWS)或类似技术。无论您最终选择哪一种，对于寻求在敏捷环境中持续交付的公司来说，云都是一个重要的促成因素。

为什么？为什么 IaaS 是成功开发运维战略的一个组成部分？通过 IaaS 和最终的 PaaS，基础设施供应的瓶颈得到了解决；不再依赖于工作繁忙、任务积压时间长、能够编写脚本和实现自动化的人员不足的运营团队。需要基础设施供应来按需创建各种环境，包括开发、测试和集成环境，在连续交付链或发布管道的不同阶段或步骤中都需要这些环境。这些环境可以在隔离中创建，并且与其他项目的依赖关系消失了，而这些项目是导致发布延迟的原因。

测试自动化对于连续交付是至关重要的，但是如果提供必要的测试环境需要几天或者几周的时间，那么好处就会减少。

**devo PS-云对齐技巧**

因此，我们将云作为发展战略的一部分。您现在如何协调开发运维与云计划？当您的开发人员随时快速启动环境时，您需要考虑哪些因素？

首先，从 IaaS 开始。与 PaaS 相比，IaaS 更容易实现，也更普遍适用。为了快速取胜，使用公共的 IaaS，比如通过 AWS 或者微软 Azure。解决开发或测试环境所需的合规性和安全性问题，并在这些服务的基础上创建几个部署脚本。要么准备带有中间件、应用服务器和数据库的现成映像，要么让开发人员自己安装这些组件。或者，ops 也可以准备必要的安装脚本并提供给开发人员。

第二，基于 OpenStack 或其他技术构建自己的 IaaS。敏捷开发团队和负责 IaaS 基础设施的团队使用的工具集和界面需要同步。例如，如果您在云环境中使用 OpenStack，那么可以使用 Chef 或 Puppet 来调整您的配置工具。好消息是，这些技术中的许多确实可以很好地协同工作。

第三，一旦您的 IaaS 实现成熟并被采用，转向 PaaS。PaaS 是私有云领域的冠军联赛，通常要求组织致力于数据库、中间件、应用服务器、部署架构等的特定标准。它不仅可以轻松快速地供应服务器，还可以供应应用程序的完整运行时环境，并在其上部署应用程序。

在所有阶段，各部门之间都需要紧密合作。负责交付私有云的敏捷开发、IT 运营和基础架构团队都需要围绕一个共同目标保持一致:更快地向市场交付优质应用和更新。这意味着要齐心协力构建可靠、快速且适应性强的云基础设施，以支持敏捷服务交付。理解和跟踪个人发展里程碑是必要的。依赖“大爆炸”方法没有意义:云基础设施需要与所有开发时间表同步。

事实证明，在构建基础设施团队时使用敏捷方法特别有用:每个平台都有一个产品负责人，他与开发团队一起工作，管理开发人员对平台的所有请求，即所需的 API 及其签名或公共 backlog 中特定技术的支持版本。这与开发部门的产品负责人管理他们的业务积压是一样的。,

最后，确保你有合适的技能。开发运维及私有云基础架构需要新的技能组合，例如运营工程师，来准备、管理和开发您的私有云及应用平台。在敏捷开发过程的中途购买技能是没有意义的:它们需要从一开始就被构建到业务计划中。

DevOps、IaaS 和 PaaS 就像 PC 和键盘一样走在一起；应用程序和 iPhoneWindows 和 Word。总之，IaaS 基础架构中的 DevOps 使您能够驾驭更快的开发并转向[连续交付。](http://automic.com/continuous-delivery)