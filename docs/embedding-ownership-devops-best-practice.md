# 嵌入所有权:DevOps 最佳实践

> 原文：<https://devops.com/embedding-ownership-devops-best-practice/>

从我所在的 DevOps 社区来看，开发往往比运营更受关注。 [SimplifyOps](https://www.rundeck.com/) 的 Damon Edwards([@ damone Edwards](https://www.twitter.com/damonedwards))试图通过他在[全天 DevOps 会议](http://www.alldaydevops.com/?__hstc=31049440.5c975bf4c2f7d75bed4a82ecdebc1a21.1488814769496.1496252475941.1496404639141.41&__hssc=31049440.3.1496404639141&__hsfp=20068296)上的演讲“Ops Happens:devo PS Beyond Deployment”来改变这种情况。

达蒙直接切入了大多数 DevOps 问题背后的主要系统性力量:筒仓。产品开发流程是这样的:规划—>开发—>发布—>运营。问题在于许多企业倾向于将相似的功能放在一起。每个人都会被关进地窖。然后在筒仓之间建立墙壁。最终，人们只知道在他们的筒仓里生活，使得移交更加困难。

我们经常发现应用程序知识和业务意图在开发方面被强调得很重，而在操作方面却很轻。同样，运营知识在运营方面很重要，但在开发方面却很少。此外，开发有所有权，但责任有限，而运营有责任，但没有所有权。

![](img/9d595d735e27533e540cee676333578d.png)

虽然许多企业都在努力建立跨职能团队，但现实是，这种转变往往达不到真正的集成运营。结果呢？筒仓依然存在。

所以，有人会问，为什么这么难？

![](img/1732d32133a54f3bb5dc8c8e9a99fe98.png)

现实是企业运营压力巨大。一面是告诉他们要走得更快，打开它，另一面是告诉他们要更安全，更可靠。这些通常被视为相互竞争的优先事项。

为了解决这一问题，企业需要在产品开发周期的运营活动中尽可能地“左移”。他们需要在开发过程中尽可能多地做。对于部署功能，企业应该:

1.  编写/运行自动化测试
2.  编写/练习部署自动化
3.  运行安全扫描工具

对于运营职能，企业应该:

1.  编写/练习自动化操作手册
2.  编写/实施监控/指标
3.  操作控制(安全！)

然而，向左移动操作要困难得多。你是怎么做到的？嵌入所有权。

我再重复一遍:*嵌入所有权*。

首先，那些构建东西的人定义修复它的过程，而那些构建东西的人在它崩溃时修复它。

这听起来很简单，但会引发问题:

1.  您如何安全可靠地提供访问权限？
2.  您如何让专家参与补救？
3.  您如何让专家了解运营情况？
4.  你如何在几天/几周/几个月后进行尸检？

达蒙推荐了四个步骤。

**步骤 1:** 建立安全的运营门户

![](img/3a6cdbac437512a005db819b6b67beb0.png)
**第二步:**建立 ops 流程的软件开发生命周期(SDLC)

![](img/319660cb050d1383140917e333cdf4d1.png)

**第三步:**连接企业管理系统

![](img/7bec6d2af8c2519b9f1a62acce55bd0b.png)

**第四步**:让合规真正快乐

![](img/5265f873dae98be38d83736283fcc1f6.png)

Ticketmaster 是一个现实生活中的例子，它在一个大的、显著的规模上工作。Ticketmaster 将其系统称为“边缘支持”，它包括:

*   交付团队编写/审核的自动化运营程序
*   运营部仍然完全控制可以运行的内容和安全策略
*   授权支持团队执行自助式运营任务
*   为开发人员提供有限的自助操作
*   结合新的事件响应模型

Ticketmaster 已经看到了变革性的成果。在边缘支持之前，平均响应时间为 47 分钟。现在，边缘支持已将这一时间缩短至仅 3.8 分钟，此外还将上报减少了 50%，总体支持成本降低了 55%。Ticketmaster 已经看到了真正的成果。

![](img/2992a7b9531b4570470867e19e70d0af.png)

达蒙在他的演讲中有更多的细节，你可以点击这里在线观看。如果你错过了其他任何 30 分钟长的全天 DevOps 演示，它们很容易找到并免费提供[在这里](http://www.sonatype.com/all-day-devops-on-demand?__hstc=31049440.fff56b041308a66b74cf93c40ea2030a.1456347809383.1485535294436.1485539851201.581&__hssc=31049440.3.1485539851201&__hsfp=1394008546)。

最后，请务必在此为您和您团队的其他成员注册 2017 年全天 DevOps 大会[。今年的活动将提供 96 场由从业者主导的会议(不允许供应商推介)。这一切都是免费的，10 月 24 日在线。](http://www.alldaydevops.com/?__hstc=31049440.5c975bf4c2f7d75bed4a82ecdebc1a21.1488814769496.1496252475941.1496404639141.41&__hssc=31049440.3.1496404639141&__hsfp=20068296)

— [德里克·威克斯](https://devops.com/author/derek-e-weeks/)