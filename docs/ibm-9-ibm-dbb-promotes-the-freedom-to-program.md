# 基于依赖的构建促进了编程的自由

> 原文：<https://devops.com/ibm-9-ibm-dbb-promotes-the-freedom-to-program/>

每当我想感到惊讶时，我所需要做的就是思考这样一个事实:Linux 操作系统的持续开发基本上是由一群志愿者完成的。没错！最流行和最重要的操作系统之一是通过捐赠的劳动力来更新和维护的。世界上任何地方的任何程序员都可以为改进 Linux 内核做出贡献。

如此艰巨的任务是通过志愿者劳动完成的，这令人难以置信。更神奇的是，创造出来的软件质量水平格外高。让我们面对现实吧，开发 Linux 内核不是一个有着一年 C 编程经验的高中生能做的事情。但是，只要代码符合要求，任何一个高中生都可以为 Linux 代码库做出贡献。在某种程度上，这种事情的发生几乎是不可思议的。但是每天都是这样。

是什么促成了这种自由？在我看来，这是拉请求的概念。

## 拉请求的强大优雅

“拉”请求是开源开发过程中一个简单而重要的部分。开发人员从 Linux 存储库的主分支中创建一个特性分支，然后在该特性分支中添加或修改代码。当然，开发人员编写测试来验证新代码是否有效。代码完成后，开发人员向项目发送一个 pull 请求，这个项目通常托管在 GitHub 或另一个流行的 Git 存储平台上。项目维护人员是一群对代码库有专业知识的人，他们使用嵌入 Git 存储库平台的工具来审查 pull 请求。每个维护者检查代码，如果代码通过检查，评审者投票批准。如果代码有缺点，评审者可以使用 Pull Request Commenting 特性直接在代码中提出改进建议，这些特性在几乎所有的 Git 仓库平台中都可用，包括[【GitHub】](https://help.github.com/articles/about-pull-requests/)[Git lab](https://about.gitlab.com/2015/07/29/feature-highlight-merge-request-approvals/)和 [Bitbucket](https://www.atlassian.com/git/tutorials/making-a-pull-request) 。

这是一个简单而强大的过程，并且改变了企业级软件的创建方式。任何开发人员都可以以他们想要的任何方式实现一个想法，只要实现与代码库兼容。由开发人员决定如何去做他们想要的事情；没有人发号施令。这个过程很简单:弄清楚如何对代码做出贡献。创建特征分支。做你的工作。做一个拉取请求。如果你的贡献是有用的，并且编码良好，你就被录取了。如果没有，我们将尽力帮助您做得更好。

## 使用 DBB 将 Git 引入大型机开发

拉请求是一种令人信服的软件开发方法——以至于 IBM 已经把它作为大型机上软件开发的核心部分。此外，其产品 [基于依赖关系的构建](https://developer.ibm.com/mainframe/products/ibm-dependency-based-build/) (DBB)，通过减少审查人员在代码审查过程中需要做的工作，简化了大型机拉请求过程。

A [Dependency Based Build trial](https://www.ibm.com/account/reg/us-en/signup?formid=urx-31400&cm_mmc=OSocial_Blog-_-Systems_Systems+-+IBM+Z-_-WW_WW-_-Link+from+Devopsdotcom+DBB+trial_ov63620&cm_mmca1=000020YJ&cm_mmca2=10003064) is available in the IBM Z Trial Program at zero cost, and with no installation required. The trial environment includes hands-on tutorials.

几乎所有的现代 ide 都支持 Git 版本控制。例如，开发人员可以配置 [Visual Studio 代码](https://code.visualstudio.com/Docs/editor/versioncontrol)、 [JetBrains](https://www.jetbrains.com/help/idea/using-git-integration.html) 产品和 [Eclipse](https://www.eclipse.org/egit/) 来自动与远程 Git 库一起工作。一旦集成，Git 在后台运行，允许开发人员在版本控制下工作，而不必直接发出 Git 命令。IBM 的大型机集成开发环境 [IDz EE](https://www.ibm.com/blogs/systems/7-things-ibms-ide-provides-for-developer-empowerment/) 也提供了 Git 集成。这是一件大事，因为 Git 现在是大型机生态系统的一部分。习惯于在独立的 x86 Java 应用程序上使用 Git 版本控制的开发人员现在可以转向为大型机开发，而不必学习新的源代码控制管理(SCM)系统。但是更令人印象深刻的是，Git 被用作更传统的大型机工件的 SCM 比如 COBOL 源代码。

此外，Git 集成超越了开发人员对源代码的工作；Git 被用于整个大型机构建过程——顺便说一下，这可以由 Jenkins 控制。而且，Git 是 IBM [DBB](https://developer.ibm.com/mainframe/2018/04/19/dbb-serve-wider-vision-supporting-open-source-devops-pipeline-including-traditional-z-os-artifacts/) 使用的一项基础技术，它是一个依赖关系控制代理，与 Git 一起确保大型机构建过程中的所有文件——源代码和依赖关系——都是最新的。同样，这也是一件大事:拥有大型机部署流程中的所有活动部分，从编程到构建再到发布，使用 Git 作为公共代码存储库允许 z/OS 大型机组件成为平台无关的部署流程的一部分。DBB 的使用克服了大型机和分布式世界之间的一个重大障碍。

那么，这与拉请求的能力有什么关系呢？

## 将拉请求和代码审查添加到大型机体验中

拉式请求评审过程不仅仅是“查看代码”当你有一个可能有数百万行代码的项目时，比如 Linux 内核，没有开发人员会仔细研究每一行代码。他们将阅读文档，运行单元测试，查看添加或删除的代码行，并查找明显的问题和低效之处。现在，在 PC 上，编译像 Linux 内核这样的东西很简单——所有的代码都在一个库中。然而，在大型机上，情况有所不同:代码更加分散，依赖性管理可能变得棘手。DBB 负责跟踪各种 Git 存储库中的依赖性变化，因此当需要执行 pull 请求时，评审者不必浪费时间解决依赖性问题来编译大型机代码。DBB 会处理的。对于 pull 请求，评审人员可以做他们应该做的事情:确保代码能够工作，并且其质量能够被合并回一个主分支。

这可能看起来不多，但是任何熬夜到凌晨 3 点试图解决依赖性问题的人都明白，任何时候都要有一直在构建的代码的重要性。这就是 DBB 带来的力量。

## 编程的自由

编程是一种特殊的职业。它需要艺术、科学、创造力和工程学科的不同寻常的结合。此外，这不是一个适合处方的职业。每个编程项目都是特殊的，需要新的想法。当开发人员可以自由运用他们的想象力以不同的方式思考时，新的想法就会产生。pull 请求是确保开发人员能够自由地以生成有用的高质量代码的方式进行编程的最佳方式之一。DBB 将编程的自由扩展到了大型机社区。

历史已经表明，当一个开发人员被给予编码的自由和编码的社区时，结果是伟大的软件。问问莱纳斯·托沃兹就知道了。

鲍勃·雷瑟曼