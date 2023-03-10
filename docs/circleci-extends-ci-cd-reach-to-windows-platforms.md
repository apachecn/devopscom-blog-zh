# CircleCI 将 CI/CD 扩展到 Windows 平台

> 原文：<https://devops.com/circleci-extends-ci-cd-reach-to-windows-platforms/>

CircleCI 今天宣布，它将在各种 Windows 平台上提供其持续集成和持续部署(CI/CD)平台。

CircleCI 产品副总裁马特·怀曼(Matt Wyman)表示，支持 Windows 的决定源于微软最近的 DevOps 举措，最引人注目的是其收购 GitHub 的举措。Wyman 表示，随着微软投入更多时间和精力推广最佳 DevOps 实践，对在内部或微软 Azure 公共云中运行的 CI/CD 平台的需求将急剧上升。

CircleCI 上的 Windows 环境还支持 Docker Engine–Enterprise for Windows 工作流，并且所有 Windows 作业都在虚拟机上独立运行。每个新作业使用的环境都是及时创建的，一旦作业结束运行，环境就会被破坏。该方法旨在确保构建的可再现性以及存储在 CI 环境中的代码、数据和秘密的安全性。所有 CircleCI 功能，如缓存、工作区、批准作业和上下文，现在都可以用于 Windows 作业。

![](img/1a98f10ab1daf20e2dad799cbc946aaa.png)

Wyman 说，CircleCI 现在希望组织扩展相同的软件开发生命周期过程，以构建和部署基于 Windows 和 Linux 的应用程序。他补充说，在跨两种环境的通用 CI/CD 平台的上下文中利用相同管道的能力将有助于减少今天构建 Windows 应用程序所需的时间和精力。

目前，尚不清楚在 Windows 和 Linux 环境中构建和部署应用程序的一套通用流程是否会促进 it 组织内部的协作。Linux 和 Windows 团队往往不怎么互动。然而，随着越来越多的组织寻求应用可重复的过程，使他们能够更快地构建更可靠的软件，[标准化 DevOps 过程的需求](https://devops.com/doing-devops-in-an-interconnected-world/)变得显而易见。当然，Circle CI 并不是唯一一家希望利用新兴混合云计算机会的 CI/CD 平台提供商。

同样值得注意的是，像微软和 Red Hat 这样的平台提供商也在推广他们自己的软件开发生命周期管理方法。组织需要决定他们希望在多大程度上依赖平台供应商提供的工具和流程，而不是集成跨多个平台的 DevOps 流程的 CI/CD 平台。为了打这场仗，CircleCI 上个月透露，它又筹集了 5300 万美元的资金。当时，该公司指出，其平台上的月度工作总数为 3000 万，高于 2018 年 1 月的 700 万。

不管选择哪条道路，组织越来越需要在多个平台上构建和部署软件。与管理这些流程相关的挑战是巨大的。IT 领导者首先需要确定的问题是，他们有多希望自上而下地推动软件开发的统一，而不是简单地提供一套他们的团队(希望)会倾向于使用的工具和平台。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)