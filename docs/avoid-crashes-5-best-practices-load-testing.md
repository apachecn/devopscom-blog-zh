# 避免崩溃:负载测试的 5 个最佳实践

> 原文：<https://devops.com/avoid-crashes-5-best-practices-load-testing/>

苛刻的客户期望和社交媒体上信息的快速传播使得网站和应用程序崩溃成为当今公司和组织的禁区。

交通高峰导致的撞车事故会造成即时和长期的销售损失，也会损害品牌形象。当服务器或网站在备受期待的活动期间(如黑色星期五、大型游戏或大型音乐会前)宕机时，影响可能是永久性的。

然而，避免“网站暂时不可用”屏幕也比以往任何时候都容易。通过持续和主动地对你的网站进行性能测试，你可以很容易地发现错误、瓶颈和 bug，然后修复它们，以确保你的网站能够处理任何数量的流量。

以下是对你的网站或应用进行负载测试的五个最佳实践:

## **定义你的负荷目标**

在开始测试之前，您需要弄清楚您需要测试什么。

这包括并发用户的数量、流量模式和用户可以访问的区域。例如，如果您的网站在高峰时有 10，000 个并发用户，但上午有 3，000 个用户，下午总数慢慢攀升到 10，000 个——这些访问者大多只是浏览您的主页——您需要运行一个不同的测试，而不是如果您的网站上有 10，000 个并发用户整天不停地浏览多个页面。

为了确定您的负载目标，您需要直接与您的业务同事联系。例如，让你的产品经理设置系统的预期功能，让营销团队通知你任何可能增加网站流量的特别活动，然后查看服务器日志和谷歌分析等工具来确定以前的客户模式。

## **选择你的负载测试工具**

有多种开源负载测试工具可以用来运行测试。

JMeter 是最受欢迎的工具，但是你也可以使用 Gatling，Locust，Tsung，The Grinder 或 Selenium。[点击这里了解更多关于这些工具集之间的差异](https://www.blazemeter.com/blog/open-source-load-testing-tools-which-one-should-you-use?utm_source=devopscom&utm_medium=external_article&utm_campaign=five-best-practices-load-testing-website-app)。

这看起来复杂吗？Taurus 是一个开源的自动化测试框架，通过使用一个简单的 YAML 脚本来简化这些工具的运行。如果你需要从云中运行测试，利用丰富的分析或者需要用户协作，你可以考虑使用 [BlazeMeter](https://a.blazemeter.com/app/sign-up?utm_source=devopscom&utm_medium=external_article&utm_campaign=five-best-practices-load-testing-website-app) 。

## **将您的系统发挥到极限**

为了确保达到负载目标，您需要一个缓冲区；具体来说，您需要确保您的系统能够处理更重的负载。

这可以确保 CPU 保持在低水平，并且您不会遇到内存泄漏。但是，我们也建议您将您的系统发挥到极限，看看它何时以及如何出现故障。这确保您确切地知道您的系统的弱点是什么，让您有更好的能力来修复任何可能发生的错误。

如果你遇到意想不到的流量高峰，这一点尤其重要——比如说，如果你的竞争对手的网站崩溃了，他们的所有客户都跑来找你。你不想为此做好准备吗？

## **监控测试结果**

留出查看测试结果的资源。

检查 KPI，包括响应时间和命中次数，以及它们之间的相关性，以了解您的系统的能力和瓶颈是什么。这些信息将帮助您了解哪些地方需要修复。

随着测试时间的推移，您将能够识别 KPI 趋势，这将有助于您监控系统健康状况。我们还建议您使用 APM 工具监控后端 KPI，如数据库查询。

## **再次测试**

所以，你已经测试，你已经分析，你已经修复。

现在，您还有最后一件事要做 *:* 再次运行您的测试，以确保在提交更改后一切顺利。这确保了没有任何东西被忽略。如果因为一个小小的疏忽，你所有的努力都付之东流，那将是一个遗憾。

现在，让我们开始测试吧！

要获得更多负载测试技巧，请查看这份免费白皮书“[如何确保您的网站或应用在高峰时间不会失败](http://info.blazemeter.com/holiday_load_testing_wp?utm_source=devopscom&utm_medium=external_article&utm_campaign=five-best-practices-load-testing-website-app)”为了了解更多关于 BlazeMeter 的信息，[请求演示](http://info.blazemeter.com/live-request-a-demo?utm_source=devopscom&utm_medium=external_article&utm_campaign=five-best-practices-load-testing-website-app)。

-[科恩的脚](https://devops.com/author/noga-cohen/)