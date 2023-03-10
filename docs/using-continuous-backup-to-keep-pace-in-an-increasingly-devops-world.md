# 使用连续备份跟上日益发展的全球化步伐

> 原文：<https://devops.com/using-continuous-backup-to-keep-pace-in-an-increasingly-devops-world/>

***连续备份如何帮助开发团队使用正确的数据继续工作***

软件工程的世界已经改变；事实上它一直在变化。我们正在从瀑布时代前进，那时每个版本都有多个特性的大预算版本是常态。现在，为了竞争，组织必须实现敏捷开发，缩短发布周期，并且每次改进或新增的功能更少。现代软件开发已经演变成一种持续开发的实践，以至于每个新版本都像是一个简单的补丁，而不是一次戏剧性的大修。

这完全颠覆了测试过程。发布周期是过去的一小部分，以前的 QA 方法没有机会跟上。最新的模式将开发人员、运营人员、测试人员和安全人员结合成一个紧密团结的团队。开发周期缩短，测试和部署从源头开始自动化。所有这些团队和过程的混合被称为 DevOps。

虚拟化带来的灵活性和可用于时间点回切的快照使这种新的运营和开发模式成为可能。然而，仍然存在一些限制，使得技术无法支持开发运维团队的高级需求。仍然需要更多来保持环境的最新状态，因为一旦删除快照，它所代表的数据就消失了。

包括 Docker、Kubernetes 和 Puppet 在内的新工具已经出现，可以在运营方面提供帮助，但如果没有高效和有效地使用它们，开发团队仍然会很昂贵。等待数据库从生产中刷新或等待任何类型的回归测试环境被实例化的任何停机时间或空闲时间都是在烧钱。DevOps 过程可以做到这一点，但是如果没有连续的恢复点流，它们就不会有效。

## **代码的质量**

开发只能和开发人员必须使用的生产数据副本一样好。难题是在合理的时间内获得生产数据的最新拷贝。如果它使用模拟测试数据来模仿生产，结果可能是劣质的，缺陷可能会更频繁地出现。

具有跨任意时间点的数据、文件或虚拟机的搜索和恢复的连续备份解决方案可以简化开发和测试。如果您在一对多配置中的不同位置有多个数据拷贝，那么构建生产环境的克隆就很简单。然后，可以将生产数据复制到灾难恢复设施进行保护，也可以复制到开发、测试和 QA 环境，以确保开发人员和测试人员使用相同的最新版本的生产数据。

生产副本与适当 API 的同时使用可以允许在没有人工干预的情况下编排测试构建和部署。这是非常重要的，因为能够在良好、可靠的数据上执行测试可以显著减少部署到产品中的代码缺陷的数量。

## **对变化的信心**

因为您可以轻松地创建生产工作负载的实时副本，所以开发人员不必猜测当他们将新的代码更新推向生产时会发生什么。相反，可以将具有最新数据的生产的精确副本复制到一个隔离的区域，在那里它不会影响生产用户。在这种环境下，他们可以毫无风险地观察结果。

[刺中的吉卜赛人杨森](https://devops.com/author/gijsbert-janssen-van-doorn/)