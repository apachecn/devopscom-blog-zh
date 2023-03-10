# CDF 正式毕业詹金斯 CI/CD 平台

> 原文：<https://devops.com/cdf-officially-graduates-jenkins-ci-cd-platform/>

持续交付基金会(CDF)今天宣布[开源的 Jenkins 持续集成/持续交付(CI/CD)已经正式毕业](https://cd.foundation/announcement/2020/08/04/cd-foundation-announces-jenkins-graduation/)。

Jenkins 去年被捐赠给了 CDF(Linux 基金会的一个分支),还有 Jenkins X(Kubernetes 的 CI/CD 平台);Spinnaker，一个 CD 平台；Tekton 是一个构建管道的框架，将作为下一代 CI/CD 平台的基础。

CDF 董事会主席兼 CloudBees 开源社区总监 Tracy Miranda 表示，尽管 Jenkins 的血统可以追溯到 2004 年，但 CDF 希望确保适用于其他项目的相同要求也适用于 Jenkins，尽管它显然已经成熟。CDF 对项目毕业的要求是:展示出不断增长的采用率、具有开放的管理流程、成熟的特征以及对社区、可持续性和包容性的坚定承诺。

CDF 今天也公布了詹金斯的公开路线图。主要特性包括改善用户/管理员体验以及与云平台更紧密的集成。简化在 Kubernetes 集群上部署 Jenkins 的操作工具的工作也已经开始。

从长远来看，CDF 致力于在 Jenkins 和 [Spinnaker](https://devops.com/cd-foundation-touts-spinnaker-cd-progress/) 之间扩大基于 Tekton 的触发管道的采用。Tekton 管道更容易创建，并且可以跨多个平台重用。Jenkins X 已经采用了最初由谷歌开发的基于 Tekton 的管道。

CDF 的创始成员有 CloudBees、Google、CapitalOne、CircleCI。富士通、华为、IBM、JFrog、网飞和销售力量。

在近期内，Miranda 说 CDF 也试图标准化应用于 DevOps 过程的术语表。我们的目标是提供一种类似于“罗塞塔石碑”的东西，这将有助于刚开始他们的旅程的 IT 专业人员更容易访问 DevOps。

至少在理论上，Jenkins X 等平台加速了在 Kubernetes 集群上运行的基于微服务的应用程序的开发。然而，在实践中，许多 IT 团队继续使用 Jenkins 和其他 CI/CD 平台来构建单片和基于微服务的应用程序。

然而，随着 Kubernetes 的发展，应用程序的部署方式也可能会发生变化。今天，大多数 DevOps 团队将应用程序代码从 CI/CD 平台推送到目标系统上。但是，如果 Kubernetes 部署在多个平台上，那么通过使 Kubernetes 集群能够按需从 CI/CD 平台提取代码，自动化代码交付可能会变得更加容易。

随着组织过渡到构建和部署基于微服务的应用程序，显然将更加需要依靠最佳开发运维实践来管理每个微服务之间存在的所有依赖关系。传统应用程序开发流程将无法跟上基于容器的微服务被淘汰和替换的速度。

当然，与采用 Jenkins X 或 Spinnaker 之类的 CD 平台相比，组织在多大程度上更喜欢使用基于 Java 虚拟机的 Jenkins 还不清楚。然而，随着这些平台之间的互操作性不断提高，有一天发现 DevOps 团队在不同的应用程序开发项目中混合使用所有这些平台也就不足为奇了。