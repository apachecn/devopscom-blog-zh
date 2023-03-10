# Kubernetes Jenkins 主从式:扩展可伸缩性问题

> 原文：<https://devops.com/kubernetes-jenkins-master-slave-scaling-the-scalability-issue/>

LinkedIn、索尼、戴尔和许多其他公司都使用 Jenkins 作为 CI/CD 工具，并使用并行运行 365 天的大量代码库进行构建。通常，您可能没有太多的代码要构建，但是在构建过程中创建的从属对象即使在构建完成后也处于 upstate 状态。这可能导致更高的成本、更高的不必要资源利用率和更复杂的交付渠道。

有没有克服这种情况的流程？是的。解决方案是*可扩展性*。

# Jenkins 可扩展性

Jenkins 拥有的最强大的功能之一是扩展—超越其正常的生产力极限。在本文中，我们将了解 Jenkins 主/从模型，其中有一个中心 Jenkins 实例，称为主实例，以及几个可执行的从实例，称为从实例，主实例负责在从实例之间调度作业。奴隶的一些特征是:

*   并行运行多个生成任务。
*   自动替换伪造的詹金斯实例。
*   根据要求和需要启动和终止从设备，从而降低成本。

有几种方法来实现詹金斯缩放；也许最容易实现的是 Kubernetes 上的 Jenkins scaling。

本文将回答关于 Kuberenetes 上的缩放过程的某些问题，包括:

*   当主模块生成一个构建时，从模块是如何创建的？
*   如何将构建分配给新创建的从属服务器？
*   在构建期间和之后，从机如何与主机通信？

# 詹金斯主安装

先决条件:

*   詹金斯档案
*   kubernetes-Jenkins-deployment . YAML 文件
*   忽必烈詹金斯服务 yaml file
*   立方结构永久磁碟区
*   Kubernetes 持续量索赔参考:blazer.com

在 Kubernetes 上安装 Jenkins 的首选方式是基于 Jenkins 基础映像创建一个定制的 Docker 映像。现在，您需要生成一个 Docker 文件，该文件包含来自 Docker public repo 的基本映像，在该文件上，您可以通过添加插件、安装 Maven (RUN 命令)以及您的构建和 Jenkins 部署的替代依赖项来微调您的 Jenkins 应用程序。

![](img/7db41adcfcc01cddb3b525e7a7ef06d5.png)

![](img/b03e0ac715ee7bee82939672ed98638f.png)

Docker 文件将准备映像，这样您就不需要在 Jenkins 部署后安装任何插件——所有这些都是在创建 Jenkins Docker 映像时完成的。

创建一个 **Jenkins-deployment.yaml** 文件，其中包含部署名称、Docker 自定义 Jenkins 映像、持久卷和其他输入，然后部署应用程序。

![](img/325575260c34e1477a4dcab95ef4e6d9.png)由于每次部署都会创建一个 pod，所以让我们检查一下 pod 的状态以及 Jenkins 是如何在 Kubernetes 集群上部署的。

![](img/5972bec26f3d38e61444eefdcc685eba.png)

![](img/8f24a5a50f170fc7de5f3576686856aa.png)现在，让我们为 Jenkins 部署创建服务文件以访问仪表板。

![](img/5f2cb81e8b984ea3ea085c66f7ff3cda.png)

从上图中，我们可以访问 Jenkins 仪表板，其中包含由服务文件(32683)生成的节点 ip 和端口号。

# Jenkins 上的从机配置

Jenkins 仪表板打开时，检查以确保安装了 Kubernetes 插件。如果插件安装完成，将会在**管理 Jenkins->****配置系统****–>Kubernetes****–>添加云**中提供配置 slave 细节的选项

遵循以下步骤:

![](img/b4fc0f1be8f89bc11da34238f1e3cbc7.png)

![](img/321200704ee1ef535adf41cf7d22a1eb.png)

![](img/f1c4a781d82378babfcc422e30c93e72.png)

![](img/5c8c292c647adabc514f53c209081369.png)

然后进入管理詹金斯**–>**配置全局安全**–>**代理**–>**检查 JNLP 代理修复的协议:50000 和(Java Web Start 代理协议/1)如下图所示。

![](img/c92750d7184397f1d6af6863842470eb.png)

![](img/e4a3a00df7a73702c017e7d14ed4c870.png)

现在，创建一个自由式作业，并在“常规”选项卡中选中“限制该项目的运行位置”,并给出我们在设置中配置的从属名称:

![](img/d990637d987719200a0e39c5c19abe8b.png)

## 工作流程

*   当作业从主服务器触发时，它将查找从服务器配置详细信息。
*   基于在使用 JNLP Jenkins 从映像的主中给出的配置，从 pod 被创建并被分配给从主生成的构建，直到构建完成。
*   在一个成功的构建中，从属服务器将在一段时间内检查其他构建调度器。如果主服务器没有响应，从服务器将向主服务器发送现有的构建结果并终止。

— [幸运的库马尔·萨巴](https://devops.com/author/lucky-kumar-sappa/)