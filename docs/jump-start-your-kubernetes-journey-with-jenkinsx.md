# 与 JenkinsX 一起开始您的 Kubernetes 之旅

> 原文：<https://devops.com/jump-start-your-kubernetes-journey-with-jenkinsx/>

容器很快被采纳为部署服务的稳定方式。越来越多的组织正在采用不可变的架构，容器提供了一种很好的方式来实现这一点。

但是，伴随稳定性而来的是部署的复杂性，以及管理工作负载、扩展和更新的复杂性。除此之外，还必须创建一个可靠且可重复的流程来持续构建和运输这些容器，以达到生产就绪状态。Kubernetes 是一个选择:它提供了可靠地管理服务生产工作负载的特性。

因此，现在开发人员必须学习 Kubernetes，以及如何为 Kubernetes 准备他们的应用程序，并为持续集成和持续部署(CI/CD)创建管道。开发人员还必须确定完成这项工作的最佳方法以及从哪里开始。

## jenkinx:ci/CD for kublers

JenkinsX 是现代云平台的开源 CI/CD 解决方案，用于在 Kubernetes 上开发和管理应用程序。正是自动化帮助应用程序迁移到 Kubernetes，在 Kubernetes 上部署各种服务来管理应用程序的 CI/CD 之旅。

![](img/4ae54fe4b5a4e1bad9d1930ca8bcfaa2.png)

开发人员只需关注他们的产品及其特性，JenkinsX 将管理 Kubernetes 的部署。它固执而灵活，并提供广泛的定制。用户可以在 AWS、Azure、Google 上使用 JenkinsX 创建 Kubernetes 集群，甚至可以在 minikube 或 minishift 上本地创建。已经拥有自己的 Kubernetes 集群并启用了 RBAC(基于角色的访问控制)的开发人员可以简单地在其上安装 JenkinsX。

![](img/fe6589f0fe33dcd13900cb3847daf5cb.png)

JenkinsX 提供了各种模板，而且，由于它是开源的，每天都会添加更多的模板。开发人员可以使用 spring boot 应用程序的模板版本、golang 项目、node、open-liberty、python-http 等快速入门。它将为模板应用程序创建一个 git repo，然后连接到开发人员的 github 帐户，将此模板推送到 repo。此外，它还设置了与 Jenkins 对话所需的 webhooks，这是作为 JenkinsX 设置的一部分安装在 Kubernetes 上的。

JenkinsX 还在 Kubernetes 中创建名称空间环境。默认情况下，它将创建一个可以修改的试运行和生产环境。

![](img/8b3bc45760823545af5e1854c9d02c79.png)

一旦对一个模板化的 quickstart 应用程序进行了更改，并且创建了一个 pull 请求，该流程就会启动，并使用 webhooks 将有效负载推送给 jenkins。然后管道作业开始启动构建过程。

![](img/c85c6aa86c83cf6e3afadf0642394da5.png)

在应用程序在自己的容器中构建之后，下一个阶段开始创建 docker 映像并将其推送到内部 docker 注册中心。舵图是为应用程序生成的，并存储在内部托管的海图博物馆中。然后将它部署到预览环境中，开发人员甚至可以在合并拉取请求之前查看或运行应用程序测试。

随着拉请求被审查并合并到主分支，一个任务开始将该应用程序部署到环境中。JenkinX 实现了 GitOps，所以任何更改都是从 github 存储库中触发的。它创建一个对环境存储库的 pull 请求，并添加一个变更，以便在这个环境中部署这个应用程序。，验证拉请求并自动合并它，开始最后的部署阶段。

![](img/9354b4d77a0f9e03e30d00f2874a74ec.png)

将一个环境映射到一个特定的名称空间，然后在该名称空间中部署应用程序容器，创建一个服务，并配置所有需要的映射。此外，还提供了一个 URL 供开发人员访问他们的应用程序。

![](img/8a8e2cbca18d5be2b413c97bda9f46ce.png)

然后，开发人员推出他们的更改，喝杯咖啡(这一步是可选的)，几分钟后，他们就可以获得在该环境中访问应用程序的 URL。

![](img/f0c798afac8802f03328445734ed839a.png)

这是标准的工作流程。您可能已经注意到，JenkinsX 与传统的 Jenkins 方法非常不同。Jenkins 提供了完全的灵活性，而 JenkinsX 提供了固执己见的方法。假设它创建的模板 repo 中包含所有内容，您可以随时根据自己的需求对其进行修改。

将为管道作业创建一个 Jenkinsfile，可以对其进行编辑以添加另一个阶段。如果需要，可以创建和更新舵图。用户可以禁用它第一次创建的默认环境，并拥有自己的一组持久或可任意使用的环境。

这是一个很好的方法，可以让我们今天用来在 Kubernetes 上构建和部署应用程序的各种不同工具实现自动化。我希望增加一些功能，比如不同的部署策略、对内部 docker 注册表的支持以及清理过时映像的维护功能。也就是说，JenkinsX 消除了大部分学习曲线，并开始了您的 Kubernetes 和容器之旅。

— [绍拉夫森](https://devops.com/author/saurav-sen/)