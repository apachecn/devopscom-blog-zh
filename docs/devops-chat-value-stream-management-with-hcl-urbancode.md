# DevOps 聊天:使用 HCL UrbanCode 进行价值流管理

> 原文：<https://devops.com/devops-chat-value-stream-management-with-hcl-urbancode/>

价值流管理(VSM)是我们听到频率较高的一个术语。DevOps、敏捷、精益和当代应用程序开发是非常动态的。这些快速、动态的方法会使软件开发过程对更广泛的组织不透明。它在这部分市场还处于早期，但是它需要量化来自我们软件开发投资的商业价值。

HCL [UrbanCode](https://info.urbancodelabs.com/about) 的产品管理负责人史蒂夫·布恩(Steve Boone)加入我们这一期的 DevOps Chat，谈论这个新兴市场的状况。Steve 分享了关于组织如何合作的宝贵见解，DevOps 和敏捷在哪些方面产生了可衡量的差异，以及管理层可以做些什么来为团队提供管理 VSM 的工具。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/686224849&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/686224849&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

米奇·阿什利:大家好。我是 DevOps.com 的米奇·阿什利，您正在收听的是另一个 DevOps 聊天播客。今天，我和 HCL 城市代码的产品管理负责人 Steve Boone 在一起。我们今天的主题是从您现有的 DevOps 文化中提取价值流管理。史蒂夫，欢迎来到 DevOps 聊天。

史蒂夫·布恩:嘿，米奇！非常感谢你今天邀请我。很荣幸。

阿什莉:很荣幸能请到你。我们感谢你加入我们。你能从自我介绍开始，告诉我们一点你在 HCL 城市代码做什么和一点关于公司的情况吗？

是的，绝对是。我加入 UrbanCode 品牌已经有 13 年多了。如果你对 UrbanCode 不太熟悉，回到 2013 年，我们被 IBM 收购，然后就在最近，大约两年前，我们与 HCL 达成了知识产权合作关系。这太棒了，因为我们有 IBM 和 HCL 这样的公司投资我们的整个 UrbanCode 产品组合。你知道，从持续集成、持续交付、发布流程编排到最近，我们一直将目光转向价值流管理，并试图专注于如何帮助企业采取下一步措施，挑战并解决我们认为是第二天的开发运维挑战。现在我们已经实现了所有这些自动化，我们如何将它提升到下一个级别，我如何识别我的组织中正在出现的新瓶颈并变得更加成功？我认为，归根结底，这就是我们都在努力做的事情。

阿什莉:绝对是。我们应该从一点点定义开始。你如何定义价值流管理？

男孩，这是一个很好的问题。我认为这在很大程度上是一个新兴市场。当我们从 UrbanCode 的角度考虑价值流管理时，我们真的希望确保我们的开发团队正在做的工作是一个整体，与整体业务目标一致，对吗？其次，我们希望能够提供数据和信息，这些数据和信息不仅对开发团队很重要，对测试团队和设计团队也很重要，让他们负责我们认为是他们自己的价值流。

当我们思考这个问题时，它实际上是关于我如何从创意中获得一些东西，并把它一路带到，比如说，生产或我的客户手中？但是在这个过程中有哪些不同的步骤，对吗？这就是我们所认为的价值流。

所以，有个想法。最终，这个想法变成了我的开发人员的待办事项中的某个项目，然后我想推进这几组等同于某种商业价值的想法。而且，你知道，几年前，在 DevOps 革命的阵痛中，如果你愿意，你知道，人们会说很多话——“嗯，你的瓶颈显然在部署自动化”或“显然在测试自动化。”

现在情况已经不同了。我的意思是，许多这些公司已经在人员、流程和工具上投资了数百万美元，对吗？现在，他们开始回来说，“太好了，我们正在做所有这些事情。我们如何变得更好？我的新瓶颈在哪里？”

价值流管理真的能揭示这个领域，并帮助人们了解他们组织中新的瓶颈出现在哪里。

**阿什利:**出色的清晰度。我完全同意你的设计。验证你是否认为这是正确的，或者帮助我稍微推进一下这个想法——看起来价值流管理已经出现了，因为像敏捷、精益、开发运维这样非常动态的过程正在创建软件，以小得多的增量工作，在如何以敏捷的方式转向、调整、承担下一个故事方面有更大的灵活性，无论它可能是什么。但是对于组织来说，这也可能是非常混乱和不透明的，试图理解如果我们在这里投入资金，在这里投入产品需求，我们会得到什么？价值流管理可能是一种反应，或者是一种对整个过程中发生的事情进行系统观察的方式，这样我们就可以了解我们在哪里获得了价值，我们是否获得了我们需要推向市场的东西，以及持续改进和如何变得更好。

那是在轨道上吗？你认为这个想法需要在不同的方向上推进吗？你有什么想法？

不，我认为市场真的很早，我认为你所说的反映了这一点，对吗？我认为这是价值流管理试图传达的一个非常重要的信息。

我把它看做几件事，对吗？我想你是对的。一个组织中有许多不同的开发团队。我想现在，如果你说，“嘿，你是一个敏捷团队吗？”你知道，拥有许多敏捷团队并不一定能造就一个敏捷企业，对吗？

因此，问题变成了，我们在这些团队中做了什么不同的事情？我们如何展现最佳实践？我如何了解这些团队正在做的工作？这是怎么回事？

因此，如果我是一名 C 级高管，我们说，“嘿，你知道，我们想投资这些新的特性和功能”——那么，什么是正确的技术，我们应该把它交给什么样的团队？那些团队目前在做什么？

所有这些都成为非常重要的问题。我认为，更重要的是，当你看到这些组织在过去 10 年中在 DevOps 上所做的投资时，你知道，有一种越来越大的压力要展示 ROI。在我们投资的人员和我们一直在努力的过程中，在我们获得的工具中，它有回报吗？如果没有，为什么没有？我们需要调整什么？

阿什莉:是的，非常好。我认为你是对的，我很感激你事先这么说。它正在出现，还在形成中，我们还处在这个过程的早期。

企业组织倾向于做的一件事是，他们不总是喜欢在某件事情上成为第一。他们喜欢事情被证实。不总是这样，但你不想事事都处于风口浪尖。在早期，企业组织是如何处理价值流管理的？他们中有很多人加入吗？有几个人带头，还有其他人跟随吗？你如何看待这一发展？

布恩:是的，你知道，这有点像突然发生的事情。我认为任何组织都不会对价值流管理的概念感到陌生。我们看到的是，他们通常每年都会经历一次或两次某种价值流流程，他们会从一个 1000 英尺的大画面来看组织是如何合作的，对吗？工作如何在这个巨大的曲柄中转动，我们如何改进它？

但是 DevOps 的理论，对，我们想要快速的反馈，一年一次或两次查看你的整个组织，以及想法是如何通过它的——这不是真正有效的，它肯定不是对做这项工作的人的反馈。

因此，我们开始看到的是，管理层试图给团队提供他们需要的工具来控制他们自己的价值流，并对该价值流负责，对吗？在大公司，他们会说，“嘿，我们到处都有价值流。”人力资源可以是它自己的价值流——我们如何雇用和培训新员工进入我们的组织会影响我们能够交付的工作类型。

从 UrbanCode 的角度来看，我们专注于我们最了解的价值流，即持续集成和持续交付。因此，我们专注于我们领域中的工具，无论是部署工具、构建工具、测试工具、源代码工具，然后我们开始寻找，“那么，在一个典型的开发团队中，谁是推进这些想法的所有参与者？”对吗？你知道，我们的开发团队依赖于设计团队。他们依赖于测试团队。

所有这些都会对交付时间、周期时间和平均恢复时间等产生影响。一些主要的事情，如果我们去询问某人，比如说朵拉，他们关心的指标类型，你知道，识别高绩效团队，并能够看着其他团队说，“嘿，看，这些是我们希望看到你改进的指标。”

因此，对我们来说，我们在某种应用开发/运营级别上看待价值流，但在如何将价值流推广到业务、证明正在完成的工作、证明正在进行的投资以及继续认识开发运维文化中需要改进的领域方面具有巨大的商业价值。

**Ashley:** 看起来随着组织的发展，他们对开发运维的采用最终会遇到传统的关卡，也许你可以将它们视为障碍和停止点，因为组织的其余部分并不是为在那种动态流程中运营而建立的，它具有传统的瀑布式流程。看起来，你使用 UrbanCode 所做的，不仅仅是在整个 CI/CD 流程中自动化和集成，而且你还提供了信息，这些信息与沟通一些事情联系起来，帮助团队更容易地通过，或者如果是一个停止，它是最小的，因为你已经获得了所有你需要说的信息，“我们准备好进入生产了吗？”或者，“这些东西在发布中吗？”

这就是你将价值流与开发流程联系起来的方式吗？

布恩:对，没错。我的意思是，我们关注的一个关键问题是，你知道，开发人员正在研究的这些想法在哪里？嗯，你知道，通常，他们在类似 JIRA，对吧，或者 RTC 的地方——但是有一些积压管理保存着这些非常优秀的想法，它们以史诗和工作项目的形式存在，它们与 sprints 和 releases 联系在一起。

所以，你有了所有这些想法，它们都在运动中。他们都在工作的某个阶段。它们要么被搁置，要么正在设计，要么正在进行，要么正在评审，要么正在被合并，要么正在被构建。这个想法有一个旅程。它有历史和生命，如果我们可以开始浮现那段旅程，那么人们可以开始看到想法是如何在不同的团队之间流动的，对吗？

每个人都在努力为他们的团队、应用程序和项目做到最好。这绝不是指着手指说，“哦，好吧，我们被这个版本或这个特定的值耽误了，因为它没有足够快地从测试中出来”或“我们没有足够快地得到设计。”

但它是关于这些不同团队之间的关系，以便我们可以开始与正确的人进行有意义的对话，以改善这些在我们自己的内部流程中不时出现的小瓶颈。你知道，就像我们谈论人、流程和工具一样，其核心是文化，对吗？我认为价值流管理真正酷的事情之一是，正确执行，我们真的可以开始执行 DevOps 文化，并有点火上浇油，对不对？重新点燃创造力，真正让人们相信，这不是一个单独的团队或应用程序，而是企业共同努力，以最有效的方式为客户提供价值。

阿什莉:我喜欢你的想法。这似乎是 DevOps 团队或开发组织的潜在自然反应之一，因为组织还没有在那种环境中工作，价值流管理可以被视为获得控制的一种方式，这是这种方式的黑暗或消极的一面。另一种看待它的方式是带来透明度，你知道，真正从系统的角度看待这个问题，就像我前面提到的那样。

你见过那种有点反对价值流管理的反应吗，因为这种感觉有点像老大哥进来并试图夺取控制权，或者 DevOps 团队很快看到价值在哪里并开始接受它？

**Boone:** 是的，我想这是一对夫妇——我的意思是，我肯定，我想回到早期的持续集成，对吗？我们有这样的东西，如果你破坏了建筑，你会看到大红灯在开发坑闪烁，人们会看起来像，“哦，他一定是破坏了那边的建筑”，然后—

阿什莉:耻辱之墙。*【笑声】*

布恩:你知道，你必须——是的，这就像，你必须戴上傻瓜帽。我想我们离那些日子已经很远了，但还是有些犹豫，对吧？我的意思是，现实情况是，如果你去很多组织问:“你的 DevOps 之旅进展如何？”他们会说，“哦，很好。我们增加了很多自动化。我们投资了大量的培训。我们对自己的现状非常有信心。”

所以，任何时候你走进一个黑暗的房间，打开手电筒，第一次看到真实的数据，那里可能会有一些令人担忧的事情，一些人们现在不一定知道的事情。你知道，也许可以说是一些不为人知的秘密。

但是我学到的是，开发团队，他们真的想尽可能做到最好，对吗？他们想提供高质量的产品，他们想以最快的方式做到这一点。

因此，如果我们给他们工作进展的反馈，如果他们能看到哪里出了问题，他们会倾向于做正确的事情。他们进行了有意义的对话，他们改进了自己的价值流并为之负责。总体而言，这将大大提高业务效率，对吗？

所以，我认为这是它真正积极的一面，它给了人们承担责任所需的工具。当然，当我们积累这些数据时，你知道，你为开发团队提供了价值，这些数据和价值会积累到更高的管理层，这样他们就可以有效地运营业务，对吗？我的意思是，归根结底，这些组织中仍然有大量资金被套牢。因此，如果我们想制定一个新的计划，一套新的功能，如果我们想第一个上市，我们想确保我们有正确的团队，我们有正确的技术和平台，并且我们投入的努力符合业务目标。

所以，对房子的双方来说都是双赢的。你知道，AppDev 团队赢了，业务也赢了。我们真正认为我们可以产生很大影响的地方是，一些团队在过去几年中可能没有在 DevOps 领域感受到太多的爱——我说的更多是我们在运营、安全、测试领域的员工，也许是一些更关注我们的敏捷成功的员工。

你知道，我们越来越多地看到组织内开发人员和管理层的高流动率。你知道，当你从一家公司转到另一家公司时，敏捷最佳实践的定义或实现可能会有一点不同，甚至可能会改变，对吗？

阿什利:嗯。

**Boone:** 那么，我们如何确保每个人都了解我们的业务是如何运作的，这里的事情是如何运作的，这样我们就可以不断地改进流程？

Ashley: 你知道，我经常被问及的一个问题是，无论是个人技术专家、开发人员，甚至是技术组织的领导者，我们如何才能更好地与 C 套件沟通。通常，归结起来就是，你必须用商业术语说话。你知道，这种投资或资金，无论是流程改进还是技术，如何帮助我们增加收入，带来新的收入流，改善客户体验，减少客户流失—这一直是一个著名的问题，抓住一切。

但是你必须从商业角度来看，如果你相信你正在做的事情，如果你相信 devo PS——我们知道它并不完美，我们都是一个学习的组织——透明度可以帮助你很快地说，“为什么投资另一个测试工具，或者投资一些时间在重新设计上，是一个值得花钱的过程？”因为我们可以看到它的结果，我们也可以有一种方式来传达我们正在做的事情和这样做的价值。

布恩:完全正确。我可以给你两个经典的例子。你知道，现在，我们看到许多公司试图重新构建或更新他们的应用程序以加快交付，对吗？因此，我们采用分布式应用，我们将它们构建成微服务，并认为从配置和交付的角度来看，它们更易于管理。

阿什利:嗯。

**Boone:** 但是让一个开发团队说，“嘿，你需要重新设计这个东西”是有成本的

阿什莉:绝对是。

**Boone:** 所以，你基本上需要从头开始构建 it，但你也需要管理维持运营的现有业务价值。

所以，如果你要进行投资，你知道，六个月、七个月、八个月之后，甚至在你进行投资的时候，你会想知道我们实际上要花多长时间才能做到这一点？这是我们可以在我们组织的其他地方重复的吗？这样做是否有很好的商业意义，或者我应该只专注于构建新的微服务和新的应用程序，而不是专注于重新架构？

阿什利:嗯。

**Boone:** 你知道，我们看到这份清单的其他地方是，你知道，我们所说的不断拖累团队速度的事情之一是像计划外的工作或可能突然出现的事件，客户支持。管理人员很容易说，“嗯，我们没有从这个开发团队得到我们需要的东西。我们需要雇用更多的开发人员。显然，如果我们投入更多的人力，就能解决我们的任何问题。”

但是什么样的人，你知道吗？可能我们需要更多的支持工程师，我们需要更多的设计师，我们需要更多的测试人员。因此，了解资源、人员在哪里，他们正在做的工作类型，工作在哪里被耽搁，对于了解我们应该雇用什么样的人，我们需要什么样的培训来改善我们试图建立的文化是极其重要的。

**Ashley:** 既然你已经参与了价值流管理这一部分，那么我们是否已经有了一些最佳实践，“如果你正在实施这一点，是否已经开始了这一旅程，是否吸取了一些经验教训，或者确保你做了这一点”之类的事情，试图让你有最好的机会实现全垒打，或者至少是首次体验价值流管理？

布恩:是的。你知道，当我们第一次开始与客户交谈时，他们会说，“那么，我们如何更好地了解我们的价值流？”我们喜欢做小作坊，对吧？很多都是从白板开始，通过一些开放和诚实的对话，对吗？同样，整个想法是，我们不是真的在这里指指点点，而是在这里了解我们如何变得更好。

我们坐下来开始思考——好吧，如果我们从业务中获得一个全新的想法，它的旅程是什么？我认为，如果你让五六个不同的人在房间里，他们会完成 80%的旅程，然后，通过更多的对话，你会开始理解——是的，有时，我们必须吸引这些不同的股东。或者有时它被某种批准和签署的政治繁文缛节所阻碍，我们一次得不到几个星期。

所以，你开始展示一些要洗的衣服，但与此同时，你真正开始了解价值流的每一个单独的步骤以及它所经历的旅程。

一旦我们有了端到端的计划和设想，我们就可以开始寻找改进的地方，对吗？我认为这些是我看到的公司现在做的基本事情。

那些更积极的人开始想象这些不同的过程，当它们改变状态的时候。因此，他们已经到了我们可以开始映射和跟踪一个工作项目的实际旅程的地方，从提交到拉取请求，到实际的代码合并，再到构建、部署，应有尽有。

作为其中的一部分，他们开始关注一些现有的工具。你知道，UrbanCode Velocity 非常适合两个人，或者我应该说是两个人的团队。你知道，把它拉下来，社区版是免费入门，开始集成你的工具。您可以开始看到这些工作项目变得栩栩如生，并看到它们是如何从您的积压日志开始一路传播的，有希望传播到您的客户手中。

我要说，对于许多团队来说，这是一次令人大开眼界的经历，因为他们正在了解自己的流程，然后与其他团队进行真正有意义的对话，有点像“哦，你知道吗？嘿，你们是否在自己的组织中发现了同样类型的流程瓶颈？”看着它很有趣。

**Ashley:** 这非常有帮助，我很欣赏你的想法，让我们从基础开始，规划流程，就我们的现状达成一致，然后从那里开始，你们都用 UrbanCode 做了一些很好的工作，拥有社区版确实是一种低障碍、低阻力的方法。你可以把它拿下来，下载下来，开始使用它，并了解如何将它应用到你的工作中。这是一个非常非常好的工具。

是的，谢谢你。我们对此感到非常兴奋，因为这是一个非常新的领域，但我们也看到了摆在我们面前的大量机会，不仅可以改善人们的日常工作方式，还可以改善他们对周围人的文化。构建软件是令人兴奋的，有时，它可能相当有压力，对吗？我认为，当人们每天去上班时，他们想做的事情之一就是成为一种文化的一部分，这种文化是支持性的，是创造性的，可以帮助他们成为最好的人。

我认为价值流真正融入了 DevOps 的文化，对吗？我们如何确保我们作为一个组织所做的事情是为了企业的最佳利益？并确保我们为人们提供成功所需的工具。

阿什利:嗯，当然。好的，Steve，非常感谢你参加 DevOps 和我们的聊天——Steve Boone，HCL UrbanCode 的产品管理负责人。史蒂夫，谢谢你。

米奇，再次感谢你。这真是一种享受。

阿什利:当然，我们要感谢你——你，我们的听众，今天加入我们。我是 DevOps.com[的米奇·阿什利](https://devops.com/)，您已经听到了另一个 DevOps 聊天。在外面要小心。

— [米切尔·阿什利](https://devops.com/author/mitchellashley/)