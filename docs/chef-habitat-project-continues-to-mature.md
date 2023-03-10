# DevOps 聊天:厨师栖息地项目继续成熟

> 原文：<https://devops.com/chef-habitat-project-continues-to-mature/>

两年多前, [Chef Habitat](https://www.habitat.sh/) 发布时(DevOps.com 关于 Habitat 的好故事[在这里](https://devops.com/chef-potential-game-changer-habitat/)以及 [DevOps 关于 Habitat 的好聊天在这里](https://devops.com/devops-chat-habitat-chef-julian-dunn/)), devo PS 社区中的许多人都想知道 Chef 和 Habitat 将何去何从。这确实是一个雄心勃勃的愿景，但它能实现其崇高的目标吗？

Habitat 现在由许多提供不同功能的不同包组成。当然，大厨栖息地还有更多。这个 DevOps 的聊天会告诉你这一切。

《Habitat》的合著者海梅·温瑟(Jaime Winsor)和《Habitat》的高级产品经理塔莎·德鲁(Andrew Drew)以及《Habitat》的用户、SmartB 的布雷克·欧文(Blake Irvin)加入了我们的 DevOps 聊天。在他们三个之间，有大量的信息。如果你对 Chef Habitat 感兴趣或者想了解更多，这是一个很好的起点！

像往常一样，下面是我们谈话的音频流，后面是我们谈话的文字记录。尽情享受吧！

# 音频:厨师栖息地

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/359426717&color=%238cae9a&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/359426717&color=%238cae9a&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

# 文字记录:主厨栖息地

**Blake Irvin**
Blake has spent over a decade working in systems and software engineering automation, on platforms ranging from on-premise metal to containers-as-a-service, BSD and Solaris systems to embedded Linux sensor platforms. He lives and works in Berlin, Germany, where he’s Senior Operations Engineer at smartB, GmbH, an energy-efficiency and sustainability startup.

Alan Shimel: 大家好，我是来自 DevOps.com 的 Alan Shimel，我在这里参加 DevOps 聊天，我们为这一集准备了一个非常棒的聊天节目。这都是关于主厨栖息地的，我们有一些真的-我们今天有三位嘉宾，所以我们要让它继续下去。

首先让我介绍一下我的两位主厨嘉宾或者来自主厨。一个是塔莎·德鲁，他是“大厨栖息地”的产品经理，另一个是杰米·温索尔，他是“大厨”的工程师，也是《栖息地》的合著者之一。杰米，塔莎-欢迎来到 DevOps 聊天。

塔莎·德鲁:非常感谢。很高兴来到这里。

**Shimel:** 谢谢。

杰米·温瑟:是的，谢谢你邀请我们，伙计。

Shimel: 嘿，这是我的荣幸。然后，今天加入杰米、塔莎和我的，是从柏林远道而来的布雷克——我希望我不会搞砸了——欧文。布雷克，你在吗？

布莱克·欧文:是的。

希梅尔:好的。谢了。嘿，布雷克，我很感激你能抽出时间来加入我们。布雷克，你和 BusyBee 在一起，那是公司的名字吗？

欧文:这叫 smartB。

Shimel: smartB。

**Irvin:** 是的，B 实际上代表商业，因为我们正在建设，因为我们专注于为企业提供能效分析，无论是小型企业还是超大型企业，以及它们运营的建筑。

**Tasha Drew**
Tasha Drew is the Product Manager for Habitat. She previously launched Chef Automate’s analytics capabilities, was Head of Product at Rentlytics, was responsible for product for Engine Yard Cloud, and spent several years in various data center endeavors on behalf of Lockheed Martin. Tasha holds an M.S. in Management from RPI and a B.S. in Computer Science from USC. When not in front of a computer, Tasha prefers to be cruising around Napa or at the beach with her dogs—all while having intensely deep thoughts about how to save application developers from tedious rework via the wonders of application automation with Habitat.
**Jamie Winsor**
Jamie Winsor is a lead engineer at Chef Software and the coauthor of Habitat, an open source project built upon distributed system protocol Butterfly to provide a self-healing, self-configuring, stack-agnostic, frictionless abstraction for running applications—regardless of their complexity—to software developers. Jamie has been a software engineer in the video game industry for 10 years, focusing on networked application servers on such titles as League of Legends, Lord of the Rings Online, and Dungeons and Dragons Online. One of Jamie’s responsibilities in his game development tenure was to bring what we today know as DevOps into the daily lives of the other developers on his team, which Jamie accomplished by building, evangelizing, and teaching methods to his peers. He draws on that experience today in building Habitat, as he helps enable all software developers, regardless of their experience, bring their ideas to life without investing in the details of operationalizing an application.

哇，那真是好东西。杰米和塔莎，你们都为厨师工作，不需要向我们的观众介绍厨师是谁，但布莱克-欢迎。我们今天请你来是因为我们要谈一点关于栖息地的问题，布莱克，如果你不介意，我想从塔莎和杰米开始，谈一点——只是一点背景。也许我们这里有些人不熟悉栖息地。

杰米，你是合著者。你为什么不拿那个，对吗？对于不熟悉的人来说，栖息地是什么？

温瑟:是的，当然。所以，Habitat 项目是一系列软件，我希望它的总体目标是通过关注应用程序而不是基础设施来重新定义应用程序自动化的含义。过去，我们一直在构建服务中的计算机来托管我们的应用程序，而 Habitat 所做的是它说，“让我们专注于运行我们的应用程序所需的应用程序，我们需要最少的软件，然后围绕它配置机器，”Habitat 运行的正是您需要的东西。

它通过一个打包系统和一个构建系统以及一个流程管理器来实现。流程主管运行软件包，流程主管使用 gossip 协议与其他主管通信，以共享和传播关于他们正在运行的软件的信息，这使我们能够免费实现一些东西，只需将您的软件与 Habitat 打包，例如服务发现、主-从故障转移、滚动配置更新、滚动软件更新，所有这些都使用 gossip 环进行协调。

最后，我们建造的这一块，最后一块栖息地简称为 Builder，我们今天也可以聊聊，它是我们大约一个月前刚刚推出的。Builder 是一个托管的软件即服务构建服务，目前处于预览模式。它是免费的，它构建了与 Habitat 打包在一起的软件，并在发布渠道中托管它，这允许您让主管订阅，然后使用不稳定分支到稳定分支等之间的完整 CI/CD 升级过程接收自动更新。基本就是这样。

**Shimel:** 是的，不，不仅仅是基本上——这是一个很好的描述和很棒的东西，Jamie。

塔莎，现在，Habitat 是由 Chef 作为开源项目发布的，现在大概是两年前了，对吗？

德鲁:是啊，是啊。

塔莎，告诉我们 Habitat 最近有什么进展。

**德鲁:**当然可以。所以，基本上，自从两年前 Habitat 首次亮相以来，我们一直在不停地工作，只是在 Jamie 一直在谈论的建筑系统和过程监督系统之间添加功能和能力。

我们还一直致力于这两者之间的整体集成的部署部分，在 Habitat 的世界中，这是高度不可知的。因此，这个想法是，使用您需要的任何工具来部署您在 Habitat 中使用的那些工件和管理器。因此，我们一直在与合作伙伴合作，以实现一个真正伟大的云铸造生态系统故事，Kubernetes 生态系统故事，AWS 和 Azure 故事，然后还有 Terraform。

因此，我们的想法是，我们一直在使人们越来越容易开始使用 Builder，这就是为什么我们在免费预览模式下发布 Builder，因为我们只是想让人们以这种非常低摩擦的方式开始使用 Habitat 并开始重建他们的所有工作负载，然后使用您最喜欢的技术进行部署，然后开始看到 Builder 中的管理程序的好处，在两者之间进行交流。

绝对的。正如你提到的，Builder 现在是免费预览版。你知道，有些人看着像 Habitat 和其他一些伟大的开源项目 Chef 有点像牧羊人，他们说，“这一切都很好，很好，很好，但是如何——你知道，他们在哪里，如何保持业务？他们在哪里赚钱？”

那么，塔莎，你能不能谈一谈大厨是如何看待 Habitat 的商机的？

德鲁:是的，绝对是。因此，对于我们的企业客户来说，为了拥有真正强大的控制平面管理层，拥有与我们所有开源产品集成的内部解决方案是非常重要的。因此，有了 Chef Automate，我们将继续投资，并取得令人难以置信的成功。

然后，有了 Habitat，当企业希望快速将应用程序交付到大规模生产时，Habitat 成为继续支持企业的技术。因此，让我们的核心企业客户采用这部分技术套件将继续是我们战略的一部分，但我们也有 Builder，使较小的商店能够开始使用—非常低的摩擦点，非常易于使用。随着时间的推移，当我们看到人们如何采用和使用这项技术时，我们将调查如何将 Builder 本身货币化。

**Shimel:** 精彩回答。太好了，塔莎。所以，布雷克，我不想让你待太久。现在让我们带你进入这个。首先，Blake，我想我没有问你，我也不知道我们的观众是否理解，但你在 smartB 的角色到底是什么？

Irvin: 所以，我——我们在 smartB 有一个多学科、多语言的工程师团队。我们做各种各样的事情，因为我们仍然是一家小商店和小公司。但是我的关注点——这也是我的关注点和兴趣点，实际上已经有 10 年多一点了，是关于各种运营工程。

所以，我过去做的更像是传统的系统管理，现在我可以说我更像是一个软件工程运营专家。换句话说，我正专注于改进和简化软件工程的过程，而不是像服务器这样的事情。

听起来你好像在对我做亏心事，伙计。[笑声]但是布莱克-

欧文:是的，可以这么说。

是的。那么，布莱克，smartB 用的是 Habitat？

欧文:对，没错。

**Shimel:** 我们来说说为什么。

欧文:我会说，就目前而言，什么？

Shimel: 我想说——为什么？你用它做什么？

欧文:嗯，我们几乎在任何事情上都使用它。我们有一个——是的，我们有一个生产服务，它还没有被我称为“习惯化”或包装在“栖息地”包中，我们只是在等待社区中的一些工作完成，然后才能这样做。但是，我们 85%到 90%的服务都在 Habitat 下运行，使用 Habitat supervisor，我们正在尽可能多地使用杰米和塔莎描述的工作流程。

我认为，对我们来说，这实际上是一个很好的过程，因为栖息地的设计方式，采用过程可以是渐进的。因此，当塔莎提到让 Habitat 用户自由选择他们希望如何部署或如何采用时，这绝对是我们利用了很多来让我们的故事对自己有利的事情。

**Shimel:** 明白了。那么，布雷克，我是说，你们什么时候收养的，从栖息地开始？

**Irvin:** 所以，当我看到发布视频时，我想是 Adam 在西雅图的发言——Adam Jacob，厨师首席技术官。我看着它，最初只是出于好奇，然后，随着演讲的进行，我的嘴开始张得越来越大。不是因为我认为这是我见过的最具突破性的东西，而是因为我不能-我很惊讶地看到，10 年前我脑海中有多少关于这种东西的复选框，所有这种操作都有效，有多少复选框在描述工具的架构和行为时被项目选中。

所以，我想，在发布视频的几周内，我们就开始考虑采用的可行性。

**Shimel:** 哇。

Irvin: 大概几个月后就开始做推广了。因此，我们一直像一个非常缓慢的、渐进的展示那样做，以确保我们不会中断我们当前的任何软件开发流程或我们当前的生产环境。这就是一直以来的情况。我想说，这是一个持续的过程，到现在已经有八个月了，但是进展非常缓慢。

非常酷。所以，Blake，你知道，我在开源相关项目和材料方面有很长的工作历史，我总是很好奇，你知道，作为一个消费者，如果你愿意，或者这个开源项目的用户，你们有没有——你们回报了什么？你有没有贡献任何代码，错误发现，新功能的建议？在这里，你如何回馈社区？

欧文:是的，当然。我认为事情是这样的，因为我们是一个非常小的团队，我们真正关注的是试图按照设计的方式使用工具，然后每当我们发现错误或我们希望看到改进的地方时，向社区和/或核心维护者提供反馈，并保持对话真正开放和流畅，这很好。这是我继续使用 Chef 软件的原因之一——不完全是我的整个职业生涯，但相当大一部分是我的职业生涯。只是，我认为，作为一个组织，Chef 认为社区非常重要，事实上，也许是建立一个公司最重要的事情之一。与我在其他开源团队的经历相比，我认为这对每个参与者来说都是一个真正的胜利。

因此，就代码贡献而言，我认为我们所做的主要是制定了许多计划，这是 Habitat 在为您的应用程序设置一组依赖关系时使用的包的蓝图。因此，我们肯定已经在社区中发布了很多这样的内容。我想你可以找到它们，如果你在 smartB origin 下的 Builder 站点上查找，你会看到我们已经发布的所有包。我们也发布了一些东西回到核心计划方面，仅仅是人居团队维护的那些。

**Shimel:** 明白了，明白了。杰米和塔莎，布雷克和斯玛特布是不是代表了典型的栖息地使用者？

温瑟:我会这么说。你知道，有了 Habitat，你可以挑选你想要的东西，看着 Blake 和 smartB 从包装经理和主管成长起来，并逐渐走向采用 Builder，这真是太棒了。在社区中与他们共事非常愉快。他们给了我们很多很好的反馈。你知道，他们是用户，所以真正重要的事情之一是，你建立一个功能或者你建立——你知道，你修复一个错误，然后你立即从社区获得反馈，与他们一起工作令人难以置信。

不过，我认为 Habitat 可以为任何发布软件的团队工作。所以，他们绝对是一个典型的用户，因为他们运送软件，对不对？

**Shimel:** 嗯嗯。酷豆。伙计们，我们快结束了，不幸的是，领先超过 15 分钟。但是塔莎，对于那些想自己探索栖息地的人来说，他们可以去哪里获取信息呢？

德鲁:是的，我们希望他们访问我们的网站 Habitat.sh。在那里，你可以看到，我们有一个快速的，你知道，只是踢踢轮胎，10 分钟的演示。如果你想开始玩 Habitat 的运行和构建时功能，我们有更深入的教程，我们的社区在我们的 Slack 频道上非常活跃，你可以在那里找到加入的链接，但它只是在 Slack.Habitat.sh。所以，当你开始时，如果你想进入那个 Slack 频道，整个核心团队都在那里，我们的社区也在那里，我们寻求对新人的超级欢迎。总频道非常欢迎新问题。因此，您可以直接加入并获得支持，然后提出您的任何问题。

**Shimel:** 所以，是 Habitat.sh？

德鲁:是啊，是啊。

**Shimel:** 优秀，优秀。伙计们，听着。非常感谢你们三位，布雷克·欧文、杰米·温瑟、塔莎·德鲁，非常感谢你们成为我们本期 DevOps Chat 的嘉宾。继续取得成功，布莱克，你们在更大的业务中使用 Habitat，杰米和塔莎，你们继续开发并使 Habitat 成为世界各地公司不可或缺的工具。好吗？

德鲁:非常感谢。

**温瑟:**谢谢。

Shimel: 好了，各位，祝你们今天愉快。我是 DevOps 聊天室的 Alan Shimel。我们希望在下一次聊天中尽快见到您。在那之前，保重，各位。

— [Alan Shimel](https://devops.com/author/ashimmy/)