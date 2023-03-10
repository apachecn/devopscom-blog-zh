# 如何使用詹金斯管道

> 原文：<https://devops.com/how-to-use-the-jenkins-pipelines/>

随着管道的引入，Jenkins 添加了一个嵌入式 Groovy 引擎，使 Groovy 成为管道 DSL 中的脚本语言。

以下是建立 Jenkins 管道需要采取的步骤。

1.  首先，登录到 Jenkins 服务器，从左侧面板中选择“新项目”:

![](img/00649d8b8c3b0d547ba893f2b73f1918.png)

2.  接下来，输入管道的名称，并从选项中选择“**管道**”。点击**确定**进入下一步:

![](img/8d7f30759e0c5d29e59140894270cd5b.png)

3.  现在，您可以开始使用管道脚本了:

![](img/b394f04d99bfa8870f463c6ceddce530.png)

中间的红框是你开始写剧本的地方。

## 创建 Jenkins 管道脚本

Pipelines 有特定的句子或元素来定义脚本部分，它们遵循 **Groovy** 语法。

### 节点块

要定义的第一个块是“节点”:

![](img/7ddd44dfd6c819bce769f346be1621cf.png)

一个“**节点**是 Jenkins 分布式模式架构的一部分，其中工作负载可以委托给多个“**代理**节点。

“主”节点处理您环境中的所有任务。Jenkins 代理节点从主节点卸载构建，从而执行节点块中指定的所有管道工作。有关更多细节，请阅读关于 [Jenkins 分布式构建](https://wiki.jenkins.io/display/JENKINS/Distributed+builds)的内容。

*   这个块是可选的，可以认为是一个好的实践，因为代码包含在这个块中。
*   一旦任何节点可用，Jenkins 将安排并运行所有步骤，并创建一个特定的工作区目录。

### 詹金斯管道建造阶段

需要“阶段”部分来隔离工作类别，如内嵌所列:

![](img/286d4252ecbf8a62eed4a8e6989e2383.png)

一个指定的管道将由几个步骤组成，这些步骤可以分成几个阶段。例如:

| 第一阶段 | 从存储库中提取代码 | 拉代码签入 |
| 第二阶段 | 构建您的项目和工件 | 构建项目/项目的工件 |
| 第 3 阶段 | 部署应用程序 | 从集中式存储库部署到指定的环境 |
| 第四阶段 | 执行功能测试 | QA 性能会发生 |
| 第五阶段 | 执行性能测试 | (UI 和性能可以测试。 |

注意:每一个都可以包含多个动作。

例如，部署应用程序的阶段可以包括将文件复制到定义的环境中进行功能测试，以及复制到专用服务器中进行性能测试/QA，一旦文件复制成功，交付流程将开始在任何指定的环境中部署。

每个阶段块指定要执行的任务:

![](img/8ce7bd84cc98d050f54f552573fa08ea.png)

Stage 块也是可选的，但是推荐使用它们，因为它们提供了一种有组织的方式来指定要在脚本中执行的任务。

## **管道语法**

本节基于[Pipeline](https://jenkins.io/doc/book/pipeline/getting-started)入门中介绍的信息，应仅作为参考。有关如何在实际示例中使用管道语法的更多信息，请参考 Jenkins 章节的[使用 Jenkinsfile](https://jenkins.io/doc/book/pipeline/jenkinsfile) 部分。

*   从 Pipeline 插件的 2.5 版本开始，Pipeline 支持两种不同的语法，下面将详细介绍。关于各自的优缺点，请参见[语法对比](https://jenkins.io/doc/book/pipeline/syntax/#compare)。

"**管道语法**访问以下页面:

![](img/ff0a9929fdf5843d47da1c511d74a1b8.png)

![](img/d2b93478a1a092061a48ef1102c3e750.png)
**“生成管道脚本**”将创建可立即添加到您的脚本中的所需句子。

## **Jenkins file**

管道支持[两种语法](https://jenkins.io/doc/book/pipeline/syntax)，声明式(在管道 2.5 中引入)和脚本式管道。两者都支持构建连续的输送管道。这两者都可以用于在 web UI 中或者用 Jenkinsfile 定义管道，尽管通常认为创建一个 Jenkinsfile 并将该文件签入源代码控制存储库是一种最佳实践

![](img/f5075a37e720885d4c29f1d88fa8a655.png)

### 詹金斯脚本管道:

*   对于更高级的使用**脚本化管道**的情况，上面的例子**节点**是关键的第一步，因为它为管道分配了一个执行器和工作空间。因为 **Jenkinsfile** 是直接从源代码控制中提取的，所以 Pipeline 提供了一种快速简单的方法来访问源代码的正确修订:

checkout 步骤将从源代码控制中签出代码；scm 是一个特殊变量，它指示检出步骤克隆触发此管道运行的特定修订。

## **詹金斯的沙盒安全**

Jenkins 通过提供沙箱来限制任何 Groovy 脚本的执行。下面显示的选项“**使用 Groovy 沙箱，**”在 Pipeline 选项卡中可用，它允许任何用户运行脚本，而不需要管理员权限。在这种情况下，脚本只能通过使用内部可访问的 API(允许您使用 Groovy 开发脚本)来运行。

![](img/5fde31f74a22471f1a42df0e6e02dfc2.png)

取消选中时，如果脚本有需要批准的操作，管理员必须提供这些操作。这种方法被称为**脚本审批。**“默认情况下，所有 Jenkins 管道都运行在 Groovy 沙箱中。

如果选中该选项并使用未经授权的操作，脚本将在运行时失败。函数的白名单和黑名单都可以在[脚本安全的内置列表](https://github.com/jenkinsci/script-security-plugin/tree/master/src/main/resources/org/jenkinsci/plugins/scriptsecurity/sandbox/whitelists)中查看。

— [Pramod Vishwakarma](https://devops.com/author/pramod-vishwakarma/)