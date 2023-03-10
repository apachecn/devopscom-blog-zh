# 军械库提供了扩展 Spinnaker 的框架

> 原文：<https://devops.com/armory-offers-framework-to-extend-spinnaker/>

Armory 是开源 Spinnaker [连续交付](https://devops.com/?s=continuous%20delivery) (CD)软件的策划实例提供商，它正在为 Spinnaker 的任何实例提供一个[开源插件框架](https://www.newswire.com/news/armory-brings-streamlined-extensibility-and-an-expanded-devops-21278304)。

该框架于本周在其在线[开放核心峰会](https://2020.opencoresummit.com/)上宣布，已经被用于为 Spinnaker 创建 15 个插件，包括 Armory 的一个可观察性工具和 Pulumi 的一个供应工具。插件框架创建扩展点，这些扩展点为创建调用 Spinnaker CD 平台内各种微服务的插件提供标准化接口。

Armory 首席技术官 Isaac Mosquera 表示，目标是使正在持续交付(CD)基金会赞助下开发的 Spinnaker 平台更容易扩展。框架和 Spinnaker 之间的关系自然是共生的；需要更多的扩展来增加平台的吸引力。除非 Spinnaker 获得足够多的采用，否则组织不太可能构建这些扩展。

Spinnaker 最初由网飞开发，现在由 CD 基金会与 Jenkins 和 Jenkins X 持续集成/持续交付(CI/CD)平台一起推进。Mosquera 指出，组织将在不同的情况下采用不同的平台，但 Spinnaker 平台确实能够与 DevOps 团队已经部署的多个 CI 平台集成。

他说，随着 IT 环境变得更加混合，混合和匹配 DevOps 平台的能力变得越来越重要。预期对 Tekton 管道的支持将被添加到各种 CI/CD 平台，以便更容易集成 DevOps 管道，tek ton 管道最初由 Google 开发，现在是 CD 基金会产品组合的一部分。

与此同时，一场围绕如何实现最佳 GitOps 实践的辩论正在展开。由于 Kubernetes 的兴起，使用 GitOps 过程来自动将代码从 Git 仓库拉到任何平台上变得越来越容易。在某些情况下，这种方法可能会减少或消除依赖专用 CI/CD 平台来管理该流程的需要。相反，Mosquera 指出，像 Spinnaker 这样的 CD 平台也提供了一系列功能，从自动化审计过程到在出现重大部署问题时回滚应用程序代码。

与此同时，通过 DevOps 管道的代码量持续增加。与此同时，代码以微服务的形式出现，虽然微服务相对更容易构建，但部署、更新和管理往往更具挑战性。

尚不清楚有多少组织可能会考虑替换现有的 DevOps 平台，以便更有效地管理这些流程。然而，更多的组织正在更广泛地采用 DevOps 过程来处理不断增长的代码量。因此，以这种或那种形式采用开源 DevOps 平台的组织数量将会继续增加。然而，这些组织中的大多数不太可能想自己下载构成这些项目的原始数据。