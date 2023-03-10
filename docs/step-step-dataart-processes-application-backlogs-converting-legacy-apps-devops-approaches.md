# 循序渐进:DataArt 如何处理应用程序积压，使用 DevOps 转换传统应用程序

> 原文：<https://devops.com/step-step-dataart-processes-application-backlogs-converting-legacy-apps-devops-approaches/>

[DataArt](http://www.dataart.com/software-development-company) 为旅游&酒店、媒体、物联网、金融服务和医疗保健等行业设计和定制软件。DataArt 项目经理 Anton Krasikov 表示:“我们开发新产品和服务，改进现有解决方案，改造传统系统，并提供技术和工业领域的专业知识。

## DataArt 如何使用 DevOps

DataArt 快速交付高质量软件以支持运营绩效。DataArt 的 DevOps 流程招募了 Git 等版本控制系统和 Ant、Maven 和 Gradle 等构建系统。“几乎每个项目都依赖于在像詹金斯、团队城市或 TFS 这样的 CI 服务器中使用这些构建系统，”Krasikov 说。

DataArt 的开发过程也需要使用 TestNG 和 Junit 这样的框架进行大量的单元和集成测试。Krasikov 说:“也有一些项目，我们更喜欢 TDD 或 BDD 方法，使用特定的框架，如用于 UI 测试的 Selenium。通过使用 Puppet、vagger 和 Chef，DataArt 可以在 CD 管道中快速部署开发环境。DataArt 使用方法论应用这些精选的 DevOps 开发工具，其中可能包括看板或 Scrum (Scrum 是 DataArt 在这个故事中最常提到的)。

以前，DataArt 依赖手工过程或脚本工具来构建系统、源代码和单元测试。Krasikov 说:“将包括开发、质量保证和运营在内的一切联系在一起需要大量的管理工作。

**将积压的应用添加到您使用 DevOps 方法开发的应用中的挑战**

在 DataArt 返回到包含一些遗留应用程序的现有系统上工作的情况下，可以使用敏捷开发来维护这些遗留应用程序，但是过多的软件依赖性可能会使软件发布/发布周期难以保持一致。

“遗留软件可能没有良好的测试覆盖或适当的构建系统，所以我们通常在 DevOps 方向采取措施，如果不能实现连续交付，至少要实现适当的连续集成，”Krasikov 说。

将积压的应用程序添加到 DevOps 开发流程中存在挑战。Krasikov 说:“这类非 DevOps 应用程序通常会遇到几个问题，或者在最坏的情况下会遇到所有这些问题。根据 Krasikov 的说法，处于预开发运维状态并渴望转型的积压应用可能具有以下任何或所有症状:

*系统模块之间的许多依赖关系
*没有自动化环境
*没有持续集成
*没有测试自动化
*没有构建系统或低效使用

**逐步转变应用程序**

Krasikov 说，要将应用程序添加到 DevOps 方法中，首先要分析现有的源代码、系统依赖性和系统环境。接下来的步骤来自于一个最近的 Java 项目的例子，DataArt 就是这样做的。

a)选择一个源代码控制系统，如 Git。

b)进行重构并执行单元测试。“这些是齐头并进的，所以测试覆盖了主要的业务逻辑。急于达到 100%的测试覆盖率是没有意义的，但是我们测试了主要的部分。这也使我们能够降低系统复杂性，并分离系统组件，”Krasikov 说。

c)构建系统——“最初的应用程序使用庞大而混乱的 Ant 脚本来生成可部署的包。Krasikov 说:“在我们完成重构后，我们用 Maven 作为构建和依赖管理系统，将应用程序拆分成多个模块。

d)集成测试——“我们将这些作为独立的测试自动化套件引入，以确保应用程序模块作为一个整体正确工作，”Krasikov 说。

e)持续集成——data art 为多个构建任务设置了一个 Jenkins 服务器，通过每一次提交进行构建，并通过夜间集成测试将部署定位到目标环境。Krasikov 说:“CI 使我们能够尽早识别不工作的构建，从而节省调查时间。

f)环境设置–最后，DataArt 以代码形式实施基础设施。根据 Krasikov 的说法，新的开发环境使用 Puppet with vagger 来检查源代码，旋转 VM 盒/模板，并快速部署。

根据 Krasikov 的说法，DataArt 并行运行一些步骤以节省更多时间，例如随着源代码迁移移动到虚拟化配置的环境。

DevOps 帮助 DataArt 加快项目进度，让客户满意

通过越来越多地将积压的应用程序转换为 DevOps 开发方法，企业通过实现项目目标和交付每次通过 DevOps 过程的工作软件迭代而受益。“高度自动化降低了人为错误的风险，有助于我们在开发周期的早期失败。通过持续交付，我们的客户更容易看到他们想法的直接影响，”Krasikov 说。