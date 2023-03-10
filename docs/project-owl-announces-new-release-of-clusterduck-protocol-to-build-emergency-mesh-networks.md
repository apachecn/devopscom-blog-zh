# OWL 项目宣布新发布的 ClusterDuck 协议用于构建应急网状网络

> 原文：<https://devops.com/project-owl-announces-new-release-of-clusterduck-protocol-to-build-emergency-mesh-networks/>

***开发者使用、测试和贡献开源通信系统的机会*** ***，该系统在灾难发生后提供连接***

**布莱恩·克努斯，首席执行官&猫头鹰项目联合创始人**

尽管有疫情，在过去的一年里，开源社区的开发者在世界各地共同努力，帮助 [猫头鹰项目](https://www.project-owl.com/%5Ch) (组织、行踪和后勤)推进了 ClusterDuck 协议 (CDP)无线技术。

CDP 项目提供了一个系统来管理基于 LoRa(远程无线电)的物联网设备(Ducks)的自组织网状网络，该网络可以快速、廉价地部署。猫头鹰计划发明了这项技术，作为 2018 年首届 [代号](https://developer.ibm.com/callforcode/%5Ch) 全球挑战赛的一部分。

2020 年 3 月， [Project OWL](https://developer.ibm.com/callforcode/solutions/owl/) 与 IBM、[Linux 基金会](https://www.linuxfoundation.org/) 共同启动了开源 ClusterDuck Protocolproject，为社区提供一个家园，并将生态系统扩展到全球其他利益相关方。

今天，我们很高兴地宣布为我们的用户提供四项技术更新，我们邀请开发人员帮助我们改进驱动它们的硬件、软件和分析，以便在灾难发生后随时随地提供连接。

**我们今天宣布的内容**

**DMS Lite****Dashboard GitHub 1.0 发布**:DMS(Duck Management System)Lite Dashboard 是 Project OWL 针对 ClusterDuck 协议的离线数据收集平台。这是一个开源仪表板，用于在浏览器中查看网状网络。我们已经发布了 1.0 版本，并呼吁开发者改进和扩展该架构。DMS Lite 可以收集通过 ClusterDuck 网络发送的所有数据，以可视化网络活动和数据，为远程和离线区域提供分析。

**重构的面向对象代码库**:更新后的库支持很多额外的硬件平台，所以你可以使用各种新类型的设备。开发人员可以扩展和添加他们自己的硬件，根据他们所拥有的或喜欢使用的东西来扮演网状网络中的角色。

**新的** **安卓应用:**地方当局、急救人员和受灾个人可以下载的移动应用。ClusterDuck 应用程序为附近的 Duck 设备提供蓝牙连接，而不是连接到其本地 WiFi 点。蓝牙连接将有助于提供更强的安全性，并显著降低能耗，同时为紧急响应通信提供另一种渠道。开发者可以帮助我们改进 Android 应用程序，并从 iOS 版本开始。

**更具弹性的通信格式和协议:**我们将发布一种新的消息格式，以及一种用于连接设备和转发消息的更新协议。这使得平台在不利条件下更加高效、可靠和高性能。它还加强了对其他运输选择的支持，包括卫星连接。
我们的发行说明包括消息格式、新设备支持的细节，以及这些和其他新特性的更新文档。

**开源社区参与度**

自从去年在 Linux 基金会的管理下开源了cluster duck 协议以来，看到来自开源社区的回应是非常鼓舞人心的。开源社区已经发展到数百名来自世界各地的贡献者，人们总是有机会在我们的 Slack 工作空间和 GitHub 资源库中加入讨论。

通过社区与我们联系的三位开发人员是纽约的 Zachary Neuhaus、波特兰的 Amir Nathoo 和达拉斯的 David Mandala。它们是开发附加连接选项、面向对象重构以及更好的消息格式和协议的组成部分。

由于增加了新的功能，刚接触该项目的开发人员将获得更加无缝的体验。随着对开源技术的更快更容易的访问，我们希望世界上更多的人可以参与进来，建立他们自己的网络，并继续与我们一起建立协议，因为我们试图将连接带给最需要它的人和地方。

**IBM 的持续指导**

自从 [赢得](https://developer.ibm.com/blogs/with-project-owl-a-smart-network-of-rubber-ducks-can-save-lives/)2018 年代码全球挑战赛以来，IBM 继续指导我们的团队实施开源最佳实践，例如，通过帮助我们在开源上游 ClusterDuck 协议中进行创新，并将下游集成到我们自己的 OWL 项目包中，类似于成功的 Red Hat 模型。

他们也有助于扩大我们的合作伙伴网络。例如，在 2021 年初，OWL 项目通过世界银行的 tech emerge Resilience India Challenge 赢得了一笔 [赠款](https://www.worldbank.org/en/news/press-release/2021/01/12/world-bank-group-and-ces-announce-global-tech-challenge-winners) ，并且正在与喜马拉雅山脉地区喜马偕尔邦灾害管理当局(SDMA)讨论测试我们的技术。这对我们来说将是一个令人振奋的工程挑战，因为该地区的地形不同于我们在 [波多黎各](https://developer.ibm.com/callforcode/solutions/owl/%5Ch) 和多个北美地点与 IBM 服务团队合作时遇到的广阔而多样的部署地点。

OWL 期待着在 2021 年与当地利益相关者一起重返世界各地的实地测试。我们也愿意与新的合作伙伴一起测试和改进我们的开源代码库，以确保它能够在 OWL 项目或其他项目部署的任何地方产生影响。

**今天如何参与**

对于开源社区的开发者来说，这是一个参与的好时机，不管你在世界的哪个角落，也不管你的专业技术水平如何。OWL 看到了来自地方政府以及公共和私营部门组织的需求，这推动了创新并帮助我们扩展到更多行业。我们邀请您立即加入该社区:

请访问该网站，了解更多关于如何为 ClusterDuck 协议开源工作做出贡献的信息:[www.clusterduckprotocol.org](http://www.clusterduckprotocol.org/%5Ch)
在 GitHub 上找到代码库:https://github.com/Call-for-<wbr>代码/cluster duck-协议
加入与全球开发者的对话:www.clusterduckprotocol.org/<wbr>slack