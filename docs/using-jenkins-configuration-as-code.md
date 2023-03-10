# 使用 Jenkins 配置作为代码

> 原文：<https://devops.com/using-jenkins-configuration-as-code/>

使用以下代码，我们可以配置 Jenkins Master 来集成 Sonar、Nexus 和吉拉，并将它们作为一个代码进行管理。Code as configuration 是 Jenkins 中的一个插件，非常流行，使用起来也很简单。

首先，我们需要安装来自詹金斯市场的插件。

## **管理詹金斯>管理插件>前进**

![](img/d357d03e2eaa21499a6ef09d05fb7e83.png)

安装后，管理詹金斯，你会发现代码设置配置。

![](img/bb749f40b0d9e1a76e2a5f2241ba4963.png)

打开此链接后，它会将 Jenkins 配置显示为代码屏幕。

**![](img/295653da7011182f4edc65983fffefc7.png)** 在这里，你有两步:

1.  URL 或路径。
2.  导出现有配置。

## **提供 URL 或路径**

我们有两个存储 Jenkins.yaml 文件的选项:

1.  詹金斯正在运行的任何目录
2.  版本控制(比如 Git)

如果我们选择第一个选项，那么我们需要将 Jenkins.yaml 文件放在 JENKINS_HOME 目录中，放置该目录路径并单击“Apply new configuration”

![](img/d64dbbd596f4dd23067be853e998e7c1.png)

如果我们要进行版本控制，我们需要一个位置来存放 Jenkins.yaml 文件，然后我们需要在 GitLab 中以 raw 格式打开该文件，如下所示:

**![](img/5dfad44aeade915841af0e3fe9f81356.png)**

现在，放置链接并点击应用新配置。

![](img/fbca42d71efd7fad20915012644a0a49.png)

## **导出现有配置**

将当前配置导出到 Jenkins.yaml，单击导出配置按钮下载 Jenkins.yaml 文件。

![](img/a24c5cdd01f19163c0099c7e7e702ae6.png)

打开此文件后，您可能会看到一些错误。请记住，这仍在开发中，因此导出功能现在工作正常。

![](img/5d1a9289ec4a77396c422cbcb052844a.png)

我们可以用简单的 yaml 格式编写 Jenkins.yaml 文件。

## **插件**

这是 YAML 格式的样子:

![](img/698d8a70ee28f216f15e5a83a48773b2.png)

让我们转到下一步工具的安装。

## **工具安装**

这是工具安装过程中的样子:

![](img/be3f1f13b13862581cda7642481ecd14.png)

## **工具集成**

![](img/20f394afc7516fe3334e60c25aa694d9.png)

下一步是管道作业配置。

## **使用 JCasC 设置作业**

![](img/7fdbf7548453994daaff3cf2996aa03b.png)

现在，让我们把所有的东西放在一起，看看在詹金斯发生了什么:

![](img/97eea09d5d8adecbc3735b6fce2115ae.png)

应用新配置后，它将显示配置的日期、时间和路径。

**![](img/d9e270330c9b1d258bb6a5d69e98ab12.png)**

如果语法格式有错误，它将抛出如下所示的错误:

**![](img/8bf8a4dc59bd06b72982a44c39bc8db2.png)**

## **Rest API 方法提交配置**

在这里，我们正式拥有 JCasC。有一种方法可以通过 CURL 应用更改。

这里我们有两个 CURL 命令:

1.  确认
2.  应用新的

## **验证**

在这里，我使用詹金斯 YAML 存储在版本控制工具与公共回购:

![](img/e1104aee0b771b8665b270cac3ae82bc.png)

响应将如下所示:

![](img/868746f345b249dfaecfc978cf390fdb.png)

## **应用新配置**

![](img/225ff6f76851b021adf3a1cac544a9f0.png)

——[【Santosh Rahul goru】](https://devops.com/author/santosh-rahul-goru/)