# 借助 DevOps/CD/CI，GE Capital 每周发布两次移动应用，以 Velocity 速度实现自动化合规

> 原文：<https://devops.com/ge-capital-releases-mobile-app-twice-weekly-automating-compliance-velocity-thanks-devopscdci/>

GE 金融为企业客户提供设备租赁、移动应用和金融产品。通用电气金融公司全球董事总经理马特·麦钱特(Matt Merchant)与 DevOps.com 讨论了这家金融服务巨头的发展计划和流程。

根据 Merchant 的说法，他的团队在驾驶方面领先

(A)整个 IT 部门的 DevOps 文化变革，
(B)devo PS 工具的采用和扩展，以及
(C)管理结构的变化，以便在继续满足法规要求的同时以更高的速度运营。

最后一句话道出了 GE Capital 的 DevOps 流程所要缓解的一个关键痛点:如何在保持合规的同时加快开发。GE Capital 通过自动化安全性和合规性做到了这一点。你很快就会看到，但首先，移动应用程序。

车队司机的移动应用程序

GE Capital 在全球范围内为送货司机、销售人员和其他因公出差的企业提供车队租赁服务。GE Capital 作为租赁平台的一部分提供的移动应用程序很多，并且因国家而异。对于这个讨论，Merchant 以一个部署在瑞典的 app 为例。

这款基于网络的应用程序使司机能够定位附近的加油站、轮胎店、修理店和挡风玻璃更换服务。司机还可以使用该应用程序下载路线，收集加油、里程和机油更换/服务数据，并记录他们的工作时间。这个应用创造了许多效率。

司机过去常常从实体司机手册中获取商店数据，他们必须仔细阅读手册才能找到最近的服务提供商。“你一把目录交给他们，它就过时了。现在，他们可以在手机上获得实时更新，”Merchant 说。他们还习惯于用便笺簿和笔手工记录他们的时间，然后在一天结束时回到办公室将这些数据输入计算机。“现在他们是实时完成的，而且是在一天结束时完成的，”Merchant 说。

开发前后的移动应用开发

在 GE Capital 旧的瀑布式移动应用程序开发流程中，发布需要六到八周。挑战包括不一致的代码存储库、手动脚本和测试，以及每次开发人员开发代码时都要面对变更、架构和安全审查委员会。“因为所有这一切都是如此痛苦，你不想经常重复这个过程，所以你把更多的变化捆绑到一个版本中，这增加了出错的风险，”Merchant 说。

通过 DevOps，GE Capital 增加了 Chef 配置管理，并创建了一个公司称之为 ArchOps 的“总体伞形”开发流程。Merchant 解释说，ArchOps 涵盖 CD/CI 和虚拟化云平台管理，同时利用精益六适马方法进行 swift 敏捷应用程序开发。这实现了快速迭代、一致的代码、自动化测试，并使用 Chef 实现了快速虚拟机加速。并且不再有变更管理评审。

实现“快速合规”

为了实现 Chef 所说的“速度上的合规性”并高速交付合规的、可审计的代码，GE Capital 重新考虑了其收费站流程和工件。“我们将价值流图应用到我们的治理模型中，去除了 60%的关卡和 70%的人工制品，”Merchant 说。这款手机应用的发布时间缩短到了几天。

GE Capital 通过自动化测试输出分析实现自动化合规。当分析表明代码的一部分没有通过测试时，代码就会返回到开发阶段，开发阶段必须在重新测试、进一步分析和最终推广到生产之前修复它。“这样就不需要变更顾问委员会了，”Merchant 说。

当审计员请求测试结果、发布日期或特定代码发布的副本时，Merchant 只需从 Git 存储库中取出给定的代码和所有的测试结果、设计工件以及与之捆绑在一起的治理数据，并将其移交。

请一次通过开发

现在，随着 GE Capital 对 DevOps 思维模式的掌握，所有开发人员都使用 [Eclipse IDE](https://eclipse.org) ，它将代码直接传输到公司的 Git 存储库中。一旦代码进入 Git，开发人员就可以使用 Jenkins 等工具运行作业，进行 Fortify 应用程序扫描，并使用 GE Capital 的自制工具 Rainbow 进行 UI 测试。

一旦代码通过所有测试，系统会将其发送到生产前的试运行环境中。“GE Capital 使用 Chef 构建了登台环境，Chef 调用服务器，旋转环境，并将代码放入其中，”Merchant 说。用户接受和剩余的测试发生在那里。然后，创建内部环境的 Chef 代码创建生产环境，确保发布后应用程序的稳定性。