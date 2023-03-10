# 使用 glu 实现部署和监控自动化

> 原文：<https://devops.com/deployment-and-monitoring-automation-glu/>

glu 是一个免费/开源的部署和监控自动化平台。glu 是 LinkedIn 在 2009 年中期启动的一个项目，旨在解决部署构成 LinkedIn 体验的一系列应用程序和服务的指数级增长的需求。虽然当时存在一些像 Chef 和 Puppet 这样的项目，但他们大多擅长配置基础设施(创建用户、安装 java 等……)。glu 生活在一个更高的空间:在一群机器上提供动态应用程序(经常改变，实时故障检测等等)。

## glu 在应用部署领域

首先，让我们从一些定义开始:当我说*应用程序*时，我指的是一段通常需要运行的代码，并且通常提供某种形式的 api 来与之对话(在较低的级别上，它是一个监听端口的套接字)。对等的术语是*服务*或者*服务器*。例如，webapp 服务器就是一个应用程序。虽然 glu 也可以处理一次性的程序(运行，进行一些计算，然后停止)或基础设施(perl，java 等)，但它并没有优化来处理这些用例，其他项目更擅长这项任务(Chef/Puppet)。

一般来说，应用程序的特别之处在于，它们往往比基础架构更频繁地发生变化。在持续部署的时代，有时同一个应用程序一天要更新和部署几次并不罕见！

glu 被设计来处理这种用例:将应用程序部署到任意大的节点集:

*   高效地
*   最少/没有人类互动
*   安全地
*   以可重复的方式

[![glu executes a deployment](img/d55bceb4174e00b1d2698f8383a11d39.png)](https://devops.com/wp-content/uploads/2014/03/executeplan.jpg)

simply click “OK”!

## glu 在应用程序监控领域

一旦应用程序启动并运行，从底层硬件崩溃到应用程序本身的不当行为，许多故障都可能发生。这是它的本质，没有什么是完美的，事情会以这样或那样的方式崩溃。因此，为了能够做出适当的反应，监控系统的总体状态非常重要。glu 被设计为提供一个完整的视图，显示您已经部署了应用程序的节点集。当出现问题时，您可以近乎实时地知道。然后，您可以决定适当的操作过程，比如在崩溃的节点上重新启动失败的应用程序，或者将其降级到以前的版本，并将以前的版本重新部署到所有适当的节点。顺便提一句，你也可以在 glu 之上构建一个完整的监控解决方案，正如这篇[博文](http://www.pongasoft.com/blog/yan/glu/2011/03/18/building-monitoring-solution-with-glu/ "blog post")中所解释的。

![](img/3327bdc088b6dd172d2bad9d879dd2f7.png)

glu detects failure

## glu 是一个平台

很难建立一个一刀切的解决方案。这就是为什么 glu 被设计成一个平台，以便您在 glu 之上构建适合您的环境和工作流程的解决方案:

*   glu 提供了一个 REST api，这样你就可以通过一个简单的[文档化的 api](https://pongasoft.github.io/glu/docs/latest/html/orchestration-engine.html#rest-api "api") 来控制 glu。例如，glu 在设计上不是自动反应的(这意味着如果某个东西失败了，glu 会告诉你失败的情况，但它不会自己采取行动)，但是使用 REST api，在它的基础上构建一个反应式解决方案是相当容易的。
*   控制台(它是主要的 UI / REST api)，是高度可定制的(改变一些特性的行为的插件，让你改变它的外观的 css 调整，等等)
*   glu 自带了自己的包/发行版构建器，可以让你定制每一个组件来满足自己的需求(简单到改变端口号，复杂到提供你自己的专门化 )。
*   glu 没有规定部署对您意味着什么，也没有规定如何对您自己的系统建模(集群、组等)，也没有规定如何对您的工作流建模(在 glu 的术语中称为状态机)。你在控制，你决定。

## 实践中的 glu

glu 不是一项学术活动。glu 在 2010 年初作为开源发布之前，已经在 LinkedIn 上构建并成功部署。glu 帮助 LinkedIn 管理在 1000+节点环境中发布数百个应用程序/服务的复杂性(2010 年的数字)。其他知名公司如 Orbitz 和 Outbrain 也在使用 glu 来满足他们的部署需求。

多年来，为了支持更多的用例，glu 已经得到了[改进和增强](https://pongasoft.github.io/glu/docs/latest/html/RELEASE.html "release notes"),但是 glu 最初基于的核心和基本概念以及我在这篇文章中简要介绍的仍然是 glu 的本质！

## 如何从 glu 入手？

如果你想看一看 glu，最好是前往[主文档](https://pongasoft.github.io/glu/docs/latest/html/index.html "documentation")页面。我还建议[下载 glu](https://bintray.com/pongasoft/glu/releases/ "download") 并尝试[教程](https://pongasoft.github.io/glu/docs/latest/html/tutorial.html "tutorial")，它会让你感受到 glu 的能力。