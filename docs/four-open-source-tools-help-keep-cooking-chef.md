# 四个开源工具帮助你与厨师一起烹饪

> 原文：<https://devops.com/four-open-source-tools-help-keep-cooking-chef/>

如果你对 DevOps 概念有一点熟悉，你可能听说过 Chef。如果您已经开始尝试或实现 DevOps，那么您很有可能正在使用 Chef。Chef 是管理 DevOps 环境的一个很棒的平台，但它并不完美。

值得庆幸的是，像 Chef 这样的平台缺少的功能或功能上的差距正好给了其他开发人员介入并扭转局面的机会。对于一些组织来说，这可能是一把双刃剑。调查无数的选项，选择增加价值的工具，而不增加更多的复杂性和麻烦，这可能是压倒性的。

让我们仔细看看四个最流行的开源工具，您可以将它们与 Chef 结合使用，使您的生活更加轻松。

**1。美食评论家**

关于 Chef 最酷的事情之一——至少从极客幽默的角度来看——是各种工具和功能似乎都有与食物相关的名称，模仿 Chef。比如[美食评论家](https://acrmp.github.io/foodcritic/)。

Foodcritic 的目标是让它自动检查你的厨师食谱中的常见问题。这个想法是为了能够分析代码质量，并确定如果您尝试部署它们会导致 Chef 心力衰竭的问题。Foodcritic 确保您的食谱代码是干净的，并在您部署它们并导致 Chef 崩溃之前标记问题。

Foodcritic 也可以配置为与 Travis 和 Jenkins 等持续集成工具一起工作。这样做使您能够将 Foodcritic 的自动检查与 Travis 或 Jenkins 的自动部署管道结合起来，以保持一切顺利运行。

**2。测试厨房**

继续厨师/食物相关的命名惯例，接下来我们有[测试厨房](http://kitchen.ci/)。正如餐馆和食品公司有测试厨房，厨师可以在不中断食品生产或影响菜单的情况下试验新的口味和食谱，测试厨房为 DevOps 开发人员提供了一种执行厨师食谱的方法，而无需在厨师服务器上实际运行代码。

Test Kitchen 拥有驱动程序和插件，允许它与大多数云平台和虚拟化技术一起工作，包括亚马逊 EC2、Blue Box、CloudStack、数字海洋、Rackspace、OpenStack、vagger、Docker、LXC 容器等。它还被设计为支持测试框架，如 Bats、shUnit2、RSpec 和 Serverspec。

**3。伯克希尔哈撒韦**

食物/厨师的联系在这一点上有点夸张，但是一旦你理解了它的作用，它就更有意义了。厨师通常有烹饪书，这些烹饪书存放在书架上。一个 Chef 部署也使用 cookbook，这些 cookbook 可以使用 [Berkshelf](http://berkshelf.com/) 来管理。你看到他们在那里做了什么吗？

Berkshelf 通过管理如何获取 cookbook 并将其部署到 Chef 服务器来确保运行 Chef cookbooks 的正确版本。虽然每本厨师烹饪书都有一些独特的元素(完全相同的烹饪书没有意义)，但仍然有一些共同的元素。每次想要使用这些公共元素时，都需要手动复制，这很繁琐，因此 Berkshelf 简化了这一过程。

**4。纳吉奥斯**

你可能想知道 Nagios 是不是某种异国风味的食物，或者是你从未听说过的美食厨师使用的一种工具。不是的。可悲的是， [Nagios](http://www.nagios.org/) 打破了烹饪或食物相关命名的趋势。Nagios 这个名字实际上是一个递归的首字母缩写词，代表“Nagios 不会坚持圣徒”——这是对其原始名称 NetSaint 的引用，该名称在法律/商标纠纷后被更改。

Nagios 也不像这里列出的其他工具那样以厨师为中心。它是一个 It 基础设施监控工具，是持续监控领域的先驱，现在越来越受欢迎。Nagios 监控您的 IT 基础设施的变化，以便在问题发生之前发现问题，并向适当的人员发出警报。

持续监控有许多潜在的好处。从 Nagios 收集的数据可以帮助减少停机时间和业务损失，或者帮助组织规划和预算 IT 升级。它还是检测安全事件的有效工具，因为持续监控可以识别异常活动或未经授权的更改，并实时发出警报。

如果您在 DevOps 环境中使用 Chef，请查看这四个工具。尽管 Chef 很棒，但您可能会发现这些工具在帮助简化和维护稳定的基础设施方面很有价值。

## [在 9 月 4 日的 DevOps.com 特别网络研讨会上，了解 Rally Software 如何使用 Chef 实现业务敏捷性！](https://devops.com/features/using-devops-achieve-business-agility-webinar-rally-software-chef/)