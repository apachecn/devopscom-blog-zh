# 一整天 DevOps:将 Lambda 发挥到极致

> 原文：<https://devops.com/all-day-devops-taking-lambda-max/>

Lambda 是希腊字母表中的第 11 个字母，它也是 Amazon Web Services (AWS)服务的名称，该服务允许您在不实际配置服务器的情况下运行代码。亚马逊选择 Lambda 这个名字是因为——好吧，我不知道。知道的在这里评论。

幸运的是，你不需要知道这些来理解如何利用 Lambda。[马特·威廉姆斯](https://www.linkedin.com/in/technovangelist/)，在[Datadog](https://datadoghq.com/)([@ technovangelist](https://twitter.com/technovangelist))的 DevOps 布道者，在他题为“[抓住基础设施:充分利用 Lambda](https://www.youtube.com/watch?v=sex96wDvJo8&__hstc=31049440.6325613bfa5f684c3c47d140220f1453.1496940254734.1498655858390.1499708756946.25&__hssc=31049440.1.1499708756946&__hsfp=2042285363) ”的演讲中，概述了如何在 [2016 全天 DevOps 大会](https://www.alldaydevops.com/)上建立 AWS Lambda

首先，要理解 Lambda 是什么，我们必须看看服务器的演变。

![williams1.png](img/bbf8d05f43b9650b0d62c224711a60e8.png)

我们从物理盒子开始——我们必须购买和维护这些盒子，无论我们使用了多少，我们都必须支付所有的费用。然后，我们发展到一台物理服务器上有多个虚拟机，这样我们就可以最大限度地利用物理机的资源。现在，AWS 和类似的云服务很常见。我们创建我们需要的虚拟机，服务提供商维护物理服务器。我们也有容器来保持不同机器上的环境相同，最后，我们到达 Lambda，它是运行代码的服务，但是不需要你设置服务器。它会自动处理所有这些，您只需为该功能实际运行的时间付费。所以，如果你的函数运行需要 500 毫秒，你需要支付 500 毫秒来运行一次。

λ是基于触发器的。当接收到触发时，它执行指定的功能。触发事件可以是 AWS 服务的各种动作，比如当一个文件出现在 S3 上或者一个 Alexa 技能被请求时。

**Lambda 是无服务器的，**就你而言。

**λ是无状态的。这意味着你不能依赖本地状态，所以，如果你需要在函数调用之间保留信息，你必须把数据保存在别的地方。**

**λ执行函数。**各功能:

*   是 AMZN Linux 上 LXC 的一个容器中的代码
*   对它能做什么没有限制
*   根据执行时间、数量和内存定价

**Lambda 链接到各种 AWS 服务，**例如:

*   文件(S3)
*   数据库更新(DynamoDB)
*   溪流(运动)
*   消息(SNS、SES)
*   物联网(Echo，API 网关)

Matt 提到了几个很好的用例，例如 bootstrapping(每月前 100 万个请求是免费的)、cron jobs、文件操作、API 翻译、社交媒体流处理、扩展基础设施、移动/物联网后端和 Alexa 技能等等。

他还提到了三个具体的例子来探讨:

*   [Bittorrent 追踪器](https://blog.zappa.io/posts/zappa-bittorrent-tracker)
*   [S3 数据加载](https://www.trek10.com/blog/serverless-architectures-s3-data-loading/)
*   [聊天机器人](http://claudiajs.com/claudia-bot-builder.html)

Matt 随后概述了如何开始，并指出只要您认为应用程序开发简单(编写代码、在 AWS 上设置和调试)，设置就很简单。他演示了一个在 S3 上添加图片时自动调整图片大小的例子。你可以在这里用截图[观看他的完整演示。](https://youtu.be/sex96wDvJo8)

Matt 还提供了一些 AWS Lambda 工具的列表:

*   [顶点](http://apex.run/)
*   [无服务器框架](http://serverless.com/)
*   [戈斯帕塔](http://gosparta.io/)
*   [Go-lambda](https://github.com/xlab/go-lamdba)
*   [AWS 圣杯](https://github.com/awslabs/chalice)

Matt 讨论了监控的必要性以及如何使用 Lambda 进行监控，结束了他 30 分钟的演讲。

你可以[在这里](https://youtu.be/zNPsHMuk1v0)在线[观看](https://youtu.be/sex96wDvJo8)马特的全部演讲，在这里你可以更深入地探讨这个话题。如果你错过了其他任何一个 30 分钟的全天 DevOps 演示，它们很容易找到并且免费提供[在这里](https://www.sonatype.com/all-day-devops-on-demand?__hstc=160429922.6e550c6bb5ab39a60b15e9b7c028fd0a.1493638577119.1501169189385.1502212281637.6&__hssc=160429922.2.1502212281637&__hsfp=1674733363)。最后，请务必在此为您和您团队的其他成员注册 2017 年全天 DevOps 会议[。今年的活动将提供 96 场由从业者主导的会议(不允许供应商推介)。10 月 24 日，这一切都是免费在线的。](https://www.alldaydevops.com/)

— [德里克·威克斯](https://devops.com/author/derek-e-weeks/)