# Red Hat 通过 OpenShift GitOps 和 OpenShift Pipelines 实现了 DevOps

> 原文：<https://devops.com/red-hat-makes-devops-a-reality-with-openshift-gitops-and-openshift-pipelines/>

新的 Red Hat OpenShift 特性为组织提供了完全集成的 CI/CD 管道，以便在整个开放式混合云中更加一致地交付应用程序，并具有更高的可预测性

RALEIGH, N.C. — May 3, 2021 —

全球领先的开源解决方案提供商 Red Hat，Inc .今天宣布 OpenShift GitOps 和 OpenShift Pipelines 正式上市，这是 Red Hat OpenShift 的新功能，[行业领先的企业 Kubernetes 平台](https://www.redhat.com/en/resources/forrester-wave-multicloud-container-platform-analyst-material)。这些功能通过简化混合云中的应用程序开发和部署，帮助组织进一步减少开发和运营团队之间的摩擦。

DevOps 方法通过将开发和运营团队的工作联系到一个更加统一的方法而不是单独的孤岛来促进文化转变，有助于更快地将应用程序投入生产。但是许多组织仍然在努力完全转换到 DevOps，特别是因为许多相关的工具是特定于工作流或软件的，导致了跨团队的完全不同的方法。OpenShift GitOps 和 OpenShift Pipelines 有助于更好地统一应用开发和 IT 运营，使团队能够在开发过程的早期合作，同时有助于在整个应用生命周期中提供更高的安全性、可预测性和可见性。

> 通过 OpenShift GitOps 和 OpenShift Pipelines，我们正在努力消除开发人员和 IT 运营之间的假墙，使团队能够在应用开发流程的早期合作。这不仅有助于在软件交付过程中更快地发现和防止缺陷，而且通过在整个生命周期中提供更高的可见性和安全性，从整体上简化了过程。
> 
> Ashesh Badanisenior vice president, Cloud Platforms, Red Hat

### 更快、更可扩展的开发

DevOps 是大多数 IT 组织努力追求的文化，CI/CD 是一种可以帮助他们实现这一目标的工具，但两者之间仍然需要一座桥梁。OpenShift GitOps 有助于提供这一桥梁。

GitOps 采用以开发人员为中心的方法来构建应用程序，使用 Git 存储库作为开发人员和运营团队的唯一来源。OpenShift GitOps 基于[开源 Argo CD 项目](https://www.redhat.com/en/about/press-releases/red-hat-and-intuit-join-forces-argo-project-extending-gitops-community-innovation-better-manage-multi-cluster-cloud-native-applications-scale)构建，支持 IT 团队实施 GitOps 工作流进行集群配置和应用交付。通过实施 GitOps 框架，通过声明性代码、自动化基础设施和部署要求以及 CI/CD 来推动更新和更改，从而帮助组织实现更快、更安全、可扩展的软件开发。

此外，OpenShift GitOps 增加了对集群和应用状态的可见性，并在需要时纠正与期望状态的偏差。该功能使团队能够对集群中的变更拥有完全的可见性和可追溯性，因为每个变更都在 Git 存储库中表示。这使得跨越开放混合云的 Kuberenetes 集群之间更容易实现一致性。

### 完全控制管道

基于 Tekton 开源项目，OpenShift Pipelines 被设计为在其自己的容器中运行 CI/CD 管道的每个步骤，并允许每个步骤独立扩展以满足管道的需求。对于试图优化其基础设施资源的运营团队来说，限制在静默期支持管道所需的资源有助于降低开发人员运行管道所需的成本和开销。

OpenShift Pipelines 提供了一种简化的体验，能够完全控制团队的交付管道、插件和访问控制，无需管理中央 CI/CD 服务器。

**可用性**
OpenShift GitOps 和 OpenShift Pipelines 现已通过 OperatorHub 向所有托管 OpenShift 服务和自管理 OpenShift 容器平台以及运行 Red Hat OpenShift 4.7 及更高版本的 OpenShift 平台的订户提供。

**支持语录**
*红帽*云平台高级副总裁 Ashesh Badani
“通过 OpenShift GitOps 和 OpenShift Pipelines，我们正在努力消除开发人员和 IT 运营部门之间的壁垒，使团队能够在应用开发过程中更早地合作。这不仅有助于在软件交付过程中更快地发现和防止缺陷，而且通过在整个生命周期中提供更高的可见性和安全性，从整体上简化了过程。”

*Baloise Group*
devo PS 工程师 Nikolas Philips 说:“我们是 Argo CD 开源项目的长期用户，该项目使我们能够采用 GitOps 方法进行应用开发，并更加一致地交付应用。我们期待着使用 OpenShift GitOps，这样我们就有了一个我们已经利用的工具的企业版，帮助我们进一步扩展我们的应用程序开发。”

*Stefan Luthardt，tribe lead，Container Services，Fiducia & GAD IT AG*
“我们有大约 500 名活跃的开发人员独自开发我们的 Vertriebsplattform 应用程序套件，因此利用 Git 存储库作为单一的事实来源对于我们的应用程序开发流程来说是必不可少的。作为 OpenShift 的长期用户，我们期待利用 OpenShift GitOps 提供的功能。”

*Tobias Denzler，DevOps 解决方案架构师，Helvetia*
“随着我们在生产中继续扩大 Kubernetes 和容器的使用，我们需要确保我们的开发人员和 IT 运营团队在每一步都保持同步。我们对 OpenShift GitOps 和 OpenShift Pipelines 的发布感到兴奋，这有助于我们的团队在流程的早期调整，以简化我们的应用程序开发流程。”

**附加资源**

*   了解关于 [OpenShift GitOps](https://openshift.com/gitops) 的更多信息
*   了解关于 [OpenShift 管道](https://www.openshift.com/learn/topics/pipelines)的更多信息
*   了解更多关于 [Red Hat OpenShift](https://openshift.com)

**连接红帽**

*   了解更多关于[红帽](https://red.ht/IOS5vm)的信息
*   在[红帽编辑部](https://red.ht/1qeXuma)获取更多新闻
*   阅读[红帽博客](https://red.ht/1zzgkXp)
*   在 Twitter 上关注[红帽](https://bit.ly/2FVq6ik)
*   加入脸书的红帽
*   在 YouTube 上观看[红帽视频](https://bit.ly/JEkzvc)
*   在 LinkedIn 上关注[红帽](https://linkd.in/1AlOAXq)

## 关于红帽

[Red Hat](https://www.redhat.com) 是世界领先的企业开源软件解决方案提供商，使用社区驱动的方法来提供可靠和高性能的 Linux、混合云、容器和 Kubernetes 技术。Red Hat 帮助客户集成新的和现有的 IT 应用程序，开发云原生应用程序，基于我们业界领先的操作系统实现标准化，以及自动化、保护和管理复杂的环境。[屡获殊荣的](https://access.redhat.com/recognition)支持、培训和咨询服务使 Red Hat 成为[财富 500 强](https://www.redhat.com/en/about/trusted?sc_cid=70160000000e5syAAA)值得信赖的顾问。作为云提供商、系统集成商、应用程序供应商、客户和开源社区的战略合作伙伴，Red Hat 可以帮助组织为数字未来做好准备。

## 前瞻性声明

本新闻稿中包含的某些声明可能构成《1995 年私人证券诉讼改革法案》意义上的“前瞻性声明”。前瞻性陈述提供基于某些假设的对未来事件的当前预期，包括与任何历史或当前事实没有直接关系的任何陈述。实际结果可能与此类前瞻性陈述所表明的结果有重大差异。本新闻稿中包含的前瞻性声明代表截至本新闻稿发布之日的公司观点，这些观点可能会发生变化。然而，虽然公司或其母公司国际商业机器公司(纽约证券交易所代码:IBM)可能会选择在未来的某个时间点更新这些前瞻性声明，但公司明确否认有任何义务这样做。这些前瞻性声明不应被视为代表本新闻稿发布日期之后的任何日期的公司观点。

###

*Red Hat、Red Hat Enterprise Linux、Red Hat 徽标、JBoss、Ansible、Ceph、CloudForms、Gluster 和 OpenShift 是 Red Hat，Inc .或其子公司在美国和其他国家的商标或注册商标。Linux 是 Linus Torvalds 在美国和其他国家的注册商标。OpenStack 文字标记是 OpenStack 基金会在美国和其他国家的注册商标/服务标记或商标/服务标记，经 OpenStack 基金会许可使用。Red Hat 不隶属于 OpenStack 基金会或 OpenStack 社区，也不受其支持或赞助。*