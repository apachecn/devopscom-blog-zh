# DevOps 聊天:与 IBM 的 Kristian Stewart 一起向左转移运营，向右转移开发

> 原文：<https://devops.com/devops-chat-shift-ops-left-shift-dev-right-kristian-stewart-ibm/>

在本次 DevOps 聊天中，我们将采访 IBM 云事件管理团队的 Kristian Stewart 博士。Kristian 对开发人员和运营人员的角色以及他们如何互动有着敏锐的洞察力。克里斯蒂安称之为左移操作，右移开发。看待事物的有趣方式。

像往常一样，下面是流媒体音频，下面是我们的谈话记录。

## 声音的

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/347515572&color=%232d0c66&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/347515572&color=%232d0c66&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

艾伦·希梅尔:大家好，我是 DevOps.com 的艾伦·希梅尔，来这里参加另一个 *DevOps 聊天*。今天有一个非常热门的话题，我的嘉宾是 IBM 云事件管理团队的 Kristian Stewart。克里斯蒂安，欢迎来到 *DevOps 聊天*。

克里斯蒂安·斯图尔特:非常感谢你邀请我，艾伦。

Alan Shimel: 我只是想确定我没弄错——你是 Kristian Stewart，对吗？

克里斯汀·斯图尔特:据我所知。

艾伦·希梅尔:好的。好吧，有时我滑稽的法国口音会让人们感到困惑，但是，不管怎样——Kristian，我提到你正在与 IBM 合作云活动管理，但是请给我们的观众一点支持。那到底是什么意思？

克里斯汀·斯图尔特:好吧，让我给你一点背景，因为这里有一些历史，特别是关于播客的主题，它谈到了操作工具。所以我在 IBM 工作了十年。我是一套 IT 服务管理工具的首席架构师之一，我的专长是事件管理，作为 IBM 的 Netcool 品牌的一部分，好吗？所以我在这个行业做了 18 年。

早在 90 年代末，我曾为一家小型初创公司工作，这家公司名为“Micromoves”，在 90 年代末的网络繁荣时期，我们专注于将用于严格故障管理的工具引入电信公司和通信服务提供商。然后，在 21 世纪初，我们转向并成功销售到企业、金融和零售领域，因为从 IT 运营的角度来看，他们的 IT 基础架构变得越来越大、越来越复杂，也越来越成熟。因此，我们在 2006 年被收购，我们开始致力于应用有趣的数学和分析技术，增加我们的工具提供的价值，并将机器学习和问题应用到这个领域。这就是我三年前的背景。

那么我所说的“云事件管理”是什么意思呢？最近，作为我们所服务的行业发展的一部分，随着他们向云迁移以及他们在云方面的投资增加，我一直在与团队合作，以构建我们之前仅在内部提供的软件即服务产品功能，因此它包括警报通知工具、操作手册自动化工具和云事件管理。所以我们对 DevOps 的兴趣是双重的，对吗？因此，我们的转变本身，从最初部署在内部的收缩包装客户端服务软件，经历了云原生、云规模、公共云驻留产品的开发，我们的员工采用了微服务架构、12 因素应用程序，当然还有开发运维等范例。

我们的团队必须忍受的最大挑战或最大变化之一是，他们现在必须自己操作这些部署，对吗？所以他们从收缩包装，“把它给客户。现在是他们的问题了，”–嗯，可以说是“现在我们为你们主持这个。”因此，我们有从开发和 QA 过渡到运营角色的人员，他们需要应用软件工程技能并与应用程序开发人员合作，以确保我们在私有云方面拥有强大的功能。我们提供 24/7 全天候运营来支持这些产品。

但我们发现自己处于一个相当独特的位置，因为我们在运营，但作为一种服务产品，它们本身旨在帮助负责运营自己的应用和服务的人。因此，这只是我们最终用户的一种新的同理心，特别是当我们开始将我们的产品定位于接受 DevOps 的团队时。这回答了你的问题吗？

艾伦·希梅尔:是的，还有一些。*【笑】*但是好东西，克里斯蒂安。谢谢您们。所以今天我想谈一谈，把这个带回家给 DevOps，对吗？我们最近在 DevOps.com 看到的一个趋势是，真的，将“运营”放在开发运维中，对吗？因为我们现在已经从供应商和从业者两方面与开发运维领域的一些人进行了交谈，他们非常强调运维在开发运维中的作用。不过，Kristian，我有机会与许多像你一样的人交谈，许多人都在大力投资开发运维，但我也有很多机会与许多人交谈，他们不是新开发运维者，也不是新开发运维者，或者刚刚涉足开发运维，正在规划他们的开发运维迁移和转型。

我试图提醒人们的一件事是，“不要把你的常识丢在门口，”在 DevOps 门口，对吗？带上它，一号。此外，虽然您带来了一些东西，但这并不意味着您到目前为止在运营部门所做的一切，以及所有学到的经验教训和积累的最佳实践都会被抛弃，就像婴儿洗澡水一样。有了 DevOps，我们就进化了。我们不一定是革命性的；我们在进化。因此，建立在最佳实践和久经考验的运营实践、方法和流程基础上，可能是一个比全盘否定、从头开始更好的解决方案。谁有机会这么做呢？你对此有什么看法，克里斯蒂安？

克里斯汀·斯图尔特:哦，我完全同意。你知道，在我们的客户中，我们有一系列的客户，从电信、金融到零售，对吗？你说吧。在这些客户中，我们有处于成熟度曲线不同点的人，他们采用 DevOps。但是我要对那些客户说的是，当他们看到这些范例时，运营团队的业务目标并没有实质性的改变，当然是自从我进入这个行业以来。虽然发生了很多变化，但是业务目标仍然由 KPI 来衡量，比如平均修复时间、平均故障间隔时间和成本压力，对吗？

纪律–比如说，在一家在 ITIL 进行了大量投资的成熟企业中，他们采用事件和事故管理等纪律，并依赖于一组关键的功能，这些功能在您过渡到 DevOps 时同样适用。你知道，你的开发人员与你的操作的接近程度，流程的顺畅以及这些组织之间的交互，如果有的话，都被一些传统的方法和工具增强了。所以，你知道，要列出其中的一些，你需要工具，这些工具可以从高度异构的环境中消费事件；你需要最小化管理噪音的数量，这些噪音呈现给必须响应事件的人；你需要能够与其他系统集成；您需要能够帮助查明可能的原因，提高运营效率，应用机器学习和高级分析等方法从事件和事故数据中获得洞察力。

所以，如果你看看这些实践的演变，从历史上看，ITIL 是与事件事故管理的实践并行出现的。它没有支配它。你知道，这些标准是——抱歉，事件和事故管理是作为事实上的实践出现的，是由解决实际问题的实用工具的可用性推动的，它们仍然能解决这些问题。你知道，如果你看看运营发展的方式，看看 80 年代末和 90 年代初的电信，对吗？

因此，在当时的电信网络运营中心，您可能有几十名技术非常高的人员，网络工程师，他们接受了几十种不同管理工具的培训，这些人的费用很高，对吗？我的意思是，他们的时间花费了大量金钱，然后事件和事故管理工具的引入帮助他们从这种情况过渡到拥有相同数量甚至更多技能较低的操作人员。因此，事件管理和事故管理做的第一件事就是努力降低运营高效运营团队的成本。

但是现在，如果你看看现在 IT 管理中的变化，我前几天和一家大型企业聊天，十年前，他们这些人总是被相同的指标驱动，如 MTTR、MTBF、成本，对吗？几年前，他们的工作是供应物理硬件、静态中间件，以及从运营角度管理这些东西。现在，这些人不得不提供平台即服务工具、分布式运行时容器和编排系统，并且他们仍然负责现有的基础设施，包括网络、物理服务器和遗留的整体应用程序。所有这些仍然需要管理。因此，主要来说，他们面临着管理混合云的挑战，以及开发运维及敏捷软件开发等工作实践对上市时间的严格要求。

因此，我要说，事件和事故管理工具现在是相对的，如果不是比以前更相对的话，因为当您转向 DevOps 和站点可靠性工程等实践时，您知道，回到过去，您的运营部门雇用数百名您知道的低技能操作员，最佳实践正在转变为您拥有数量少得多的高技能运营员工。对吗？所以这些小伙子和姑娘技术高超，但他们时间有限。你知道，在采用 DevOps 的组织中，典型的操作专业人员希望专注于自动化，在发布生命周期的早期与开发人员联系，为新的推出做准备。他们不希望通过查看日志文件和筛选性能指标来找出发生了什么，这样他们就可以恢复中断的服务。

我认为我们提供的这类工具的最终目标——事件和事故管理——不仅仅是帮助运营商大海捞针；我认为是给他们注射。这是有用的，无论你是一个老派操作的低技能初级操作员，还是一个时间紧迫、拥有 20 年经验的超技术站点可靠性工程师。艾伦，你还在吗？

艾伦·希梅尔:是的。克里斯蒂安，我很抱歉。我有点网络问题。这一切都很好，但是，你知道，我想谈的一件事，克里斯蒂安，是移情的主题，作为你的 DevOps 咒语的一部分，对吗？有时候，人们对文化的东西漠不关心，但是移情在 DevOps 中是很重要的。我想问的是“我们如何找到开发者？”对吗？

长期以来，作为 DevOps 的一部分，运营人员不得不同情开发人员正在做的事情以及他们在开发方面正在做的事情，以帮助部署等，但现在，从另一方面来说，让开发人员同情运营人员正在处理的事情，这是 DevOps 等式的一部分。我的意思是，我听说过一些组织，他们实际上会将开发人员短期嵌入到运营团队中，以便他们通过艰苦的方式获得同理心，如果你愿意，对吗？

*克里斯琴·斯图尔特*是的。

艾伦·希梅尔:他们必须活下去。你觉得这样的事情怎么样？

*Kristian Stewart:* 我认为，就让开发专业人员参与进来而言，你提到了角色轮换，对吗？我认为这是一种策略。你知道，我更喜欢把它想成“左移右移的开发”，而不是“左移操作”，对吗？

艾伦·希梅尔:是的。

艾伦·希梅尔:很好。很好。

Kristian Stewart: 实际上，你知道，这让我想起了 20 或 25 年前收缩包装软件开发的情况，在开发、谁是编码员和 QA 之间。对吗？因此，在敏捷软件开发之前，有一堵砖墙，在那堵墙上扔了一堆代码。我认为敏捷，通过左移测试，真的有助于弥补这一点，就我所见，今天，开发人员和质量保证工程师真的，真的紧密合作，而不是依赖，你知道，大量的文档来相互交流。

因此，我认为，对于 DevOps，我认为类似的事情正在发生，我认为您需要左移右移的开发，以及左移左移的操作。因此，我认为，运营应用程序或服务必须是一项共同的责任，我确实认为开发人员需要参与其中。因此，当事故发生时，dev 将成为上报点。也可以包括角色轮换。但是，为了双方的利益，我认为他们都需要使用相同的操作工具，这样，当环境中发生事故或关键事件时，他们可以看到彼此在做什么。然后他们会被激励去改进这些工具的使用，为了他们自己，也为了运营。

我认为，你知道，凌晨 3 点的事故通知，你知道，就像凌晨 3 点的传呼，是一个很大的动力。因此，对于运营人员来说，编写操作手册和自动事件响应是一种激励，这样服务恢复会尽可能快，最好是自动的。对于开发人员来说，让他们的服务或应用程序可操作是一种激励，对吧，所以他们需要在应用程序中加入适量的工具，以便运营部门可以管理事件，或者更好的是，一些脚本可以管理事件，这样他们都不会在凌晨 3:00 上报。因此，我认为这是一种软硬兼施的方法，恕我直言。

*艾伦·希梅尔:*嗯嗯。是啊，很有道理。克里斯蒂安，我要你重复你之前说过的话。我们需要将运营向左移动，将开发向右移动，或者我是不是弄错了？

克里斯汀·斯图尔特:是的，不，是的，我就是这么说的。右移 dev 和左移 ops，对吗？

*艾伦·希梅尔:*明白了。

克里斯汀·斯图尔特:所以让他们在职责上有一定程度的重叠。当然，他们对这些责任的反应可能会大不相同。你知道，让我看看我是否能想到一个例子。因此，对于开发人员来说，在这种情况下，当他们参与响应事件时，在他们的应用程序日志中非常清楚就可以了。

所以，如果你考虑由 Kubernetes 上部署的基于容器的应用程序生成的事件，那么事件和事故管理系统将显示来自应用程序代码的日志；他们会收到中间件的日志。来自 Kubernetes 本身的日志；可能来自外部技术和整体的日志——NFS 安装、数据库、传统应用、网络；他们还可能从监视系统获得警报，这些系统正在监视运行容器的性能指标，例如微服务之间的事务请求率、CPU 利用率、响应时间。

因此，如果开发人员能够确保日志中包含像关键程度或严重程度这样简单的概念，这确实有助于过滤 _____ 操作人员判断某个问题是否真的存在。例如，这个事件被归类为跟踪消息吗？调试信息？一个警告？一个错误？是否知道这会影响服务？对吗？

艾伦·希梅尔:是的。

Kristian Stewart: 而且，你知道，有什么比让开发人员使用完全无法理解的日志消息更好的方法来激励他们实现这些实践呢，对吗？

*艾伦·希梅尔:*同意。同意。嘿，克里斯蒂安，我们已经超时了，但是，正如我在开始前告诉你的，这里的时间过得很快。但是，你知道，在最后的 18 分钟里，我想说的是，我很喜欢你说的运营左移、开发右移，我们的运营和开发可以合作。正如您所说，他们每个人都有不同的反应，扮演不同的角色，对给定的事件或刺激做出不同的反应，但他们可以一起工作，我们可以在 ops 在 IT 行业过去 50 年中所建立的基础上再接再厉。并且–

*克里斯琴·斯图尔特*毫米。

*艾伦·希梅尔:*对吧？我们不会把它留在 DevOps 的门口；这是它的一部分。我想要的是——你知道，如果我们能让人们带着它。你同意这是他们的主要收获吗？

克里斯汀·斯图尔特:当然。完全同意。

艾伦·希梅尔:太棒了。嘿，IBM 的 Kristian Stewart，感谢你加入我们这一集的 *DevOps 聊天*。希望将来能听到更多关于您和 IBM 团队围绕云和混合云以及其他一些东西所做的事情。我们很快就会让你回来，但是现在，谢谢你成为我们这一集的嘉宾。

克里斯汀·斯图尔特:艾伦，这绝对是我的荣幸。

艾伦·希梅尔:太好了。嘿，这是艾伦·希梅尔，各位，为 DevOps.com， *DevOps 聊天*。感谢您的加入，我们下次聊天再见。

— [Alan Shimel](https://devops.com/author/ashimmy/)