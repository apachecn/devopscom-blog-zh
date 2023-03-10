# gitlab 与宗教联盟合作添加工作负载分析工具

> 原文：<https://devops.com/gitlab-allies-with-rezilion-to-add-workload-analysis-tool/>

rezi lion[将其工作负载分析工具与 GitLab](https://www.rezilion.com/blog/rezilion-announces-integration-with-gitlab-that-helps-organizations-reduce-vulnerability-backlog-by-70/) 提供的持续集成(CI)框架相集成。此举是为了让开发人员在将代码上传到存储库之前更容易发现漏洞等问题。

GitLab 的高级产品经理 Sam White 表示，这种集成将为开发人员提供一个即时反馈循环，使他们能够在代码被审查之前解决广泛的问题。他补充说，Rezilion 平台使开发人员能够快速编写代码，同时依靠代码分析工具来发现常见错误，并在他们认为合适的时候进行补救，而不是经历例如遗漏漏洞的耻辱。

Rezilion 首席执行官 Liran Tancman 补充说，Rezilion 平台所基于的专有工作负载组成分析引擎 Unison 使得将更多的应用程序安全责任进一步转移到左边变得可行，而不需要开发人员成为网络安全专家。

Unison 自动创建所有应用程序的模型，包括底层基础设施和运行时环境。它在内存中进行逆向工程和映射，以动态跟踪库存、出处、运行时执行、暴露和每段代码之间的相互依赖，并可以生成软件材料清单(SBOM)。

塔克曼说，最需要立即关注的代码也直接出现在 GitLab 用户界面上。他补充说，随着时间的推移，这种能力可以将组织可能经历的漏洞积压的补救时间减少多达 70%。Rezilion 使组织能够实现这一目标，因为不可利用的漏洞被标记为“误报”，不应该阻止发布。

Tancman 说[如果没有这种程度的自动化，组织实施一套 DevSecOps 最佳实践](https://digitalanarchist.com/videos/featured-guests/automating-devsecops-rezilion)将极具挑战性。他指出，在没有 Unison 引擎实现自动化的情况下，开发人员可能需要数年时间才能达到网络安全培训的水平。

![](img/f97cad6d3e05d57562a570c2bb9616bc.png)

从历史上看，应用程序开发人员和网络安全团队之间的关系一直很紧张。网络安全团队倾向于推迟代码审查，直到它即将被部署到生产环境中。由于网络安全团队发现的漏洞，某个应用程序在最后一刻被删除的情况并不罕见。在某些情况下，该漏洞是一个合理的关注点，但在其他情况下，它被证明是一个误报，因为标记的代码段实际上并不包含在应用程序中。

通过为开发人员提供 CI 框架环境下的工作负载组合分析工具，GitLab 试图减少开发人员和网络安全团队之间的摩擦。

大多数组织完全掌握 [DevSecOps](https://devops.com/?s=DevSecOps) 可能还需要一段时间，但很明显，仅仅告诉开发人员他们将对应用程序的安全性负责，而不提供适当的工具，并不会使应用程序更加安全。