# 美国运通使用 DevOps 来更好地应对违约

> 原文：<https://devops.com/american-express-uses-devops-for-better-breach-response/>

周六早上 6 点，电话铃响了，吵醒了美国运通的首席信息官。当电话在早上 6 点响起时，从来都不是好消息。从来没有。这个例子没有什么不同:在这种情况下，第三方供应商刚刚遭受了一次违规，而这次违规将影响美国运通持卡人。

在接到电话后，首席信息官立即启动了公司的网络危机应对团队。网络危机响应团队的工作是帮助识别受影响的持卡人，并准备联系和帮助任何有问题或需要帮助的人。

如今，快速响应客户并向他们提供正确信息的需求至关重要，这不仅是为了与监管机构保持一致，也是为了帮助客户避免欺诈性交易和身份盗窃。谈到如此有效的数据泄露事件响应，DevOps 很少发挥作用，但美国运通在最近的 DevOps 企业峰会上分享的经验揭示了 DevOps 组织在有效的泄露响应方面可以做得多好。

在首席信息官和网络危机响应团队首次通话的几个小时内，主要的违规响应被分成三个团队。第一个团队关注数据缺口桥接团队通常关注的内容:如何识别受影响的客户。第二个小组由业务和产品负责人以及客户服务人员组成，他们的目标是从回应调查中获得发现，并将其传达给美国运通的客户。

第三个团队由理解所有系统的 DBA 和系统专家以及企业架构师组成，他们可能能够快速解决出现的任何技术挑战。

## **获取正确的违规信息**

到了那个周六下午 3 点，第一小组决定可以收集所有需要的信息来识别受影响的持卡人。这是好消息。坏消息是将会有数以千万计的生产记录需要被评估以做出最终决定。

如果团队要在生产中拉动数千万张唱片，这种需求将会降低生产系统的速度。“我们如何在不影响可用性的情况下将这些记录从生产中提取出来？这就是挑战，”美国运通消费品开发工程副总裁 Aimee Cardwell 说。

随着时间的推移，团队努力寻找一种在不影响可用性的情况下访问这些生产记录的方法，团队中的一名工程师提出了一个在大多数组织中都会遭到嘲笑的想法:*我们为什么不克隆生产？但是这个新奇的想法并没有立即被否决。参加电话会议的团队开始权衡克隆产品的利弊，并得出结论:事实上，它可以快速克隆产品，并且所有受影响的卡数据都可以聚合，而不会对美国运通的服务器和相关可用性产生负面影响。*

Cardwell 解释说，在团队成功克隆生产系统后，他们通宵工作以确定受影响的卡成员，这需要交叉引用克隆的生产系统和其他数据存储。

“在这里，真正重要的是每个人在提出一个真正出格的想法时的舒适程度。最终，他们齐心协力实现了这一目标，因为各个团队对成功所需的人员、技术和流程有着深入的了解，”美国运通 DevOps 实施总监 Chad Avery 说道。

现在是周日早上 6 点，自从 CIO 的电话在周六早上响起以来，团队一直在不停地工作。该团队设法评估了来自各种系统的相关数据，并收集了一份潜在受影响卡会员的列表。经过仔细分析，他们能够确定谁受到了违规的影响，谁没有受到影响。

是什么使这一成功成为可能？Avery 和 Cardwell 都认为这是业务、产品和技术团队的整合。“事实上，我们的业务、产品和技术团队在此次事件中通力合作，这对我们来说是一个巨大的胜利，”Cardwell 说。

Avery 认为，一个组织成功整合其技术、业务和产品团队的能力至关重要。他说，如果这些团队没有从一开始就合作，他们可能无法找到解决方案，即使找到了，也需要花费更多的时间。

## **披露日，也是最后的大赢家**

还好很快就解决了。到周一早上，遭到破坏的第三方准备公开其数据泄露。这一声明不仅会立即影响美国运通卡会员，还会影响大多数其他信用卡提供商。许多客户迫切想知道他们的帐户是否受到影响，如果受到影响，该怎么办。

客户服务热线必须准备好。

这被证明是需要解决的最后一个挑战:客户服务代表如何知道哪些打电话的客户受到了影响？紧密的团队整合和协作再次被证明是决定性因素。

产品团队的工程师花了 24 小时开发了一个工具，并与美国运通的客户服务专家分享。当个人呼叫客户服务团队时，该工具可以提醒团队某个客户是否在受影响的群体中。

该工具还配备了数据收集功能，使每个人都能从事件中学习，甚至为下一次做更好的准备。“我们希望每个人都变得更好。我们希望自己变得更好，”卡德韦尔说。“我们想知道打电话的客户中有多大比例受到影响，打电话的客户中有多大比例没有受到影响。我们想知道我们对这些客户的响应时间。我们想知道任何其他有助于我们下次做得更好的数据。”

正是这种对技术团队、业务部门、开发人员、运营和安全团队之间协作的专注，使他们能够快速成功地管理第三方数据泄露，并为下次做得更好做好准备。“他们都能够快速开发出解决方案。他们能够识别客户影响、设计解决方案、构建解决方案、测试解决方案并部署解决方案。顺便说一下，这些团队在一个周末就完成了，”埃弗里说。

— [乔治·v·休默](https://devops.com/author/george-hulme/)