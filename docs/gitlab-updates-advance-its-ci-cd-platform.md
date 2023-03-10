# GitLab 更新推进其 CI/CD 平台

> 原文：<https://devops.com/gitlab-updates-advance-its-ci-cd-platform/>

GitLab 已经扩展了其持续集成/持续开发(CI/CD)平台的功能，以包括与 Slack 和 Mattermost 的协作平台的更紧密集成，以及支持在 Windows 上运行的 Docker 容器的能力。

[GitLab 11.11 版本](https://about.gitlab.com/2019/05/22/gitlab-11-11-released/)为 GitLab 高级版添加了 Docker 映像的缓存依赖代理，以及使用由内部 DevOps 团队管理的 git lab 实例提供实例级 Kubernetes 集群的能力。这些功能是在 [GitLab 上个月宣布最初支持 Kubernetes](https://containerjournal.com/2019/04/19/gitlab-embraces-kubernetes/) 作为一个平台，现在可以在其上部署其 CI/CD 环境之后推出的。

GitLab 的最新版本还为合并请求功能添加了对多个受分配者的支持，这允许 DevOps 团队的多个成员管理 DevOps 管道中的合并请求。

最后，GitLab 11.11 还提供了对发布的访客访问，将附加 CI runner 分钟数扩展到 GitLab 免费版，支持 OpenID Connect 身份验证协议，包括序列化提交图，并通过在应用建议时自动解决讨论来简化审核。

GitLab 的技术宣传员 Priyanka Sharma 表示，GitLab 开始对使用 Docker 容器在 Windows 上构建应用程序感兴趣。GitLab Runners 的 Windows 容器执行器功能使得编排包含将在 Windows 上部署的 Docker 容器的管道变得更加容易。以前，DevOps 团队需要依赖 shell 执行器来编排 Docker 命令。这个更新使得在 Windows 上使用 Docker 容器成为可能，就像在 Linux 平台上部署 Docker 容器一样。GitLab 还改进了对 PowerShell 的支持，此外还为各种版本的 Windows 容器提供了帮助映像。

![](img/98003d01869de6e1b7725cfeab315209.png)

Sharma 说，GitLab 开始看到已经接受 Windows 的 IT 组织开始在 Docker 容器的热情方面赶上来。此外，同时采用 Linux 和 Windows 平台的 DevOps 团队正在寻求将最佳 DevOps 实践应用于这两个平台。

微软已经表示，它打算继续投资，使 Docker 容器成为其整体战略的核心要素。随着与 Docker Inc .合作的进展，对支持 Windows 环境的 CI/CD 平台的需求将变得更加迫切。

Sharma 说，与此同时，GitLab 继续致力于使大规模实施最佳 DevOps 实践变得更加容易。随着企业 IT 组织继续采用 DevOps，他们中的许多人很快发现需要从头开始设计的 CI/CD 平台，以支持许多并发用户正在访问的管道。

许多企业 IT 组织将不得不做出的决定是，他们希望在多大程度上依赖于开源平台还是闭源平台。GitLab 的企业版是一个闭源平台，但该公司确实提供了一个开源社区版。虽然开源 Jenkins 平台目前在 CI/CD 平台中占主导地位，但已采用 DevOps 的企业 IT 组织已表现出愿意采用专有 DevOps 平台，以解决从部署规模到安全性和合规性等一系列挑战。

现在预测下一场涉及向微服务转变的 CI/CD 大战将如何收场还为时过早。然而，如果历史可以作为指导，那么开源和专有 CI/CD 平台都应该有足够的空间。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)