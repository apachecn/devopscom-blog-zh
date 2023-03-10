# DevOps 聊天:Liquibase，开源和数据库，与 Datical

> 原文：<https://devops.com/devops-chats-liquibase-open-source-and-databases-with-datical/>

甚至在数据库开发运维这个术语被使用之前，Datical 就已经是这个领域的领导者了。许多人可能没有意识到的是，开源的 Liquibase 项目是 Datical 成功的主要因素。因此，在填补开放总裁的职位时，他们会选择一位开放源码领域的资深人士，这并不奇怪。

Dion Cornett 从他在 Red Hat 和 MariaDB 的时候就有开源的可信度。在他的新职位上，他负责营销、销售和产品。他决心看到开源商业模式取得同样的成功，他以前也是开源商业模式的一部分，在[datic](https://www.datical.com/)取得成功。

在这次讨论中，我们听听 Dion 对他的计划和观点的看法。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[soundcloud url=”https://api.soundcloud.com/tracks/771223528″ params=”color=#ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true” width=”100%” height=”166″ iframe=”true” /]

## 副本

艾伦·希梅尔:嘿，大家好，我是艾伦·希梅尔，来自 DevOps.com 的[。您正在收听另一个 DevOps 聊天。我们今天有一个很好的 DevOps 聊天，很高兴向你介绍 Datical 的新任总裁，Dion Cornett。迪翁，我没有搞砸吧？](https://devops.com/)

Dion Cornett: 你没有，非常感谢你的介绍，我很高兴今天能上你的播客。

谢谢你，戴恩。所以，我们播客的听众对 Datical 并不陌生。你知道首席技术官 Rob Reeves 是这里的常客，你知道，我们取笑他和他的 Lebowski 大毛衣，但听到 Robert 对 DevOps 和数据库、DevOps 市场的总体看法，以及对 Robert 喜欢发表的任何意见，总是令人耳目一新。

但也很高兴有一个来自 Datical 的新面孔。首先，欢迎加入。

**科内特:**谢谢。

Shimel: 我总是喜欢让我的听众感受到是谁在说话。Dion，你介意吗——我不是让你读你的简历，但你能为观众分享一点你的背景吗？

是的，你知道，我认为更适合 Datical 的是，如果我必须这样描述我自己，我是一个开源的人。我喜欢开源，我相信这是一种更好的软件生产模式，你知道，这种精英思想和透明度的结合会产生更优雅的代码。

所以，你知道，我的背景是有一个符合这种哲学的职业。因此，我在 Red Hat 工作了九年，担任过几个不同的管理职位，负责北美非知名客户销售，然后负责全球战略联盟。我从那里开始接手 MariaDB 的销售工作，这是一家开源数据库公司

**Shimel:** 当然，*【相声】*嗯。

科内特:是的。*【笑声】*它在 2013 年并不那么受欢迎，但我们确实在三年内将这项业务增长了 7 倍。这让我得到了 CEO 的职位。我确实在开源之外做了一些事情，但这是一个大数据挑战，一家名为 ReachForce 的公司，我们成功地将它卖给了这个领域中另一家名为 Leadspace 的公司。

然后，我实际上休息了一段时间，通过一个董事会成员的介绍，花了一些时间和 Datical 在一起，有点爱上了这个概念。所以，你知道，我在 Red Hat 的工作，显然涵盖了所有挑战的基础，因为它与 MariaDB 的数据有关，并真正看到了在构建和维护一个大而强大的数据库方面的斗争，以及这对几乎任何应用程序都是多么重要。你看看我们的一些顶级银行或电信类客户，你知道，数据是这些公司创造的一些价值的核心。

然后，即使在 ReachForce，右，martech 领域的大数据公司，数据也是至高无上的。这些都是在数据库中维护的，在快速变化的应用程序需求的背景下，尝试更新、升级、维护这些数据库是一项非常重要的工作。

因此，当一家公司出现时，它结合了我的 DNA 中的开源，然后解决了数据库变更管理的挑战，这看起来非常合适。

绝对的。Dion，你知道，另一件让我们早点解决的事情是——在当今世界，当我们任命总裁时，你知道，曾经有一段时间，正如我们所说的那样，CEO 和总裁是一个人。然后，从治理的角度来看，这是一个糟糕的模式。在很大程度上，我们将首席执行官和总裁分开了。总统有各种各样的责任。有些更像首席运营官，有些更像 CRO，你知道，意思是负责所有收入类的活动。

只是，你在哪里，你知道，你在 Datical 负责什么？

科内特:是的，所以，正式来说，我的职责是销售、营销和产品。这是公司的起源，我和公司的首席执行官德里克关系很好。我们已经工作了一个月，我认为我们合作得很好，即使是在我的招聘过程中。

但是德里克在这里建立了一种令人惊叹的文化。当你开始一项新工作时，这是你永远不知道的事情之一，你知道，团队之间的协同作用是什么，德里克是一个非常有效的领导者，他建立了一个伟大的文化。就 Datical 解决方案的深度和价值而言，这是无可争议的，对吗？我们有很多六位数的客户，甚至有一个七位数的客户。我的意思是，这些都是解决大企业中的棘手问题，而该公司在这方面做得非常好。

我是为一个非常特殊的章程而来的，对吗？我们如何更好地与我们的社区互动和协作，以更快地将创新推向市场？你的听众可能知道，Alan，Datical 的真正基础是一个名为 Liquibase 的开源项目。Liquibase 是——我在 Red Hat 做过的事情之一是，我在那里管理风险投资组合。我看了上百份开源商业计划，做了十几项投资，并加入了红帽投资的一些公司的董事会。当你看到成千上万的开源项目时，Datical 可以说是前 10 名——或者 Liquibase 可以说是前 10 名。

那么，我们如何与该社区合作，再次以一种协作的方式，我们真的在拉动创新，推动创新，并尽可能地为这个具有挑战性的数据库问题带来更多价值？

绝对的。所以，你说了很多。让我们把他们一个一个挑出来。

首先是 Liquibase。这是我们在过去的播客和过去的内容类型网络研讨会中提到过的，我们用 Datical 做了一些事情。但是——也许你会改变这一切，我希望你会的，迪翁。我知道在我的脑海中，当我想到 Datical 时，我不会想到 Liquibase。虽然 Liquibase 有大量的追随者，但我只是没有——看起来是这样，我没有责怪任何人或任何类似的事情，但我只是，我没有把这两者联系起来。也许这是你使命的一部分。

绝对是。我们希望这种联系不仅存在，而且是牢固的。再说一次，我们这里有一个伟大的团队，伟大的文化，伟大的人。我们想利用这一点成为社区的优秀管理者。

你知道，激励这里的人们的部分原因是，这是一个需要解决的巨大挑战。你之前评论过罗伯特特立独行的风格，我认为这是正确的，对吗？我们在打碎一些玻璃。我们试图创造一个新的模式，一个新的方向，以及一个非常重要的发展。

这就是 Liquibase。您知道，Datical 是建立在此基础上的一组功能。不过，我们需要明确的是，这一核心是我们的基础，而且，你知道，我们希望尽我们所能成为 Liquibase 社区 1500 多万用户的好管家，你会看到这将成为我们更多的身份，体现在我们所做的一切，我们如何行动，行为，我们在哪里投资，以及我们如何努力将价值推向我们的客户。

**希梅尔:**优秀。Dion，让我再给你讲一个开源的东西。你知道，正如我之前跟你说过的，我对市场有自己的看法，你知道，建筑商，我称之为市场的民主化。

我也有一个开源运动的观点，你知道，整个开源社区在哪里。那就是，你知道，我们已经从大教堂和集市发展到我称之为开源的老大哥阶段，看起来，每个开源项目都是由一个供应商赞助或拥有的。这在某种程度上抑制了行业基础上的合作，对吗？这就像是，Oracle 不会为 MS SQL 做出贡献。我的意思是，SQL 女士远没有开放。*【笑声】*

但是假设，一旦甲骨文收购了—

**科内特:** MySQL。

**Shimel:** MySQL。听着，这就是玛丽亚和其他人突然出现的原因，对吗？坦白地说，因为人们不确定甲骨文会不会好好表现。

但那是老的了。这个模型就是我所说的开源的基础时代，我们有 Linux 基金会、Eclipse 基金会或 Cloud Foundry 基金会。你知道，他们是非盈利性的，他们为了社区的利益拥有开源项目。

我不知道像 Liquibase 这样的游戏领域有什么基础。是你，还是那个—

Cornett: 不，你知道，我对基金会的模式非常熟悉。是的，很明显，红帽是 Fedora 的先驱。

希梅尔:当然，是的。

**Cornett:** 我们实际上也在 MariaDB 实现了一个基础模型。所以，即使你今天看，MariaDB.org 是一个独立的法律实体—

**Shimel:** Yep.

Cornett: 将总裁和工程师分开。真正的目的是让用户相信，无论您讨论的供应商收购如何，该项目的功能都将继续发展。

我们没有——再说一次，我在这里工作了一个月——我们现在没有 Liquibase 的基础。

**Shimel:** 好的，我不是让你——不要说任何你不能说的话*【相声】*。*【笑声】*

科内特:是的。*【笑声】*这当然是一个考虑因素。*【相声】*但是你知道，这是有分寸的，对吧？那么，有什么权衡，有什么价值？当你谈到开源的不同阶段时，我认为——很不幸，开源曾经是一种，你用了技术民主化这个词；这也是 Matthew Szulik，Red Hat 的前首席执行官使用的一个短语。

**Shimel:** 嗯嗯。

Cornett: 他还谈到了人们的时尚宣言，开源是成功的。我的意思是，你在互联网上使用的所有东西，今天大部分都是开源的。所以，很明显赢了，对吧？这场战斗算是结束了，人们说，“嘿，我想抓住这个。”

因此，有一群公司试图利用开源品牌，却没有真正理解作为社区管理者和良好合作的细微差别。在某种程度上，我认为这提供了一种扭曲的视角。我们会在 Datical 避免这种情况。你知道，再说一次，我们会成为社区的好管家。我们认识到它必须是参与性的。大多数社区成员都在 IBM、SAP 或其他类似的公司工作。他们花时间成为这个社区的一部分，因为这为他们正在做的事情和他们的职业生活提供了一些价值。

因此，我们必须认识到，我们必须为这种价值做出贡献，试图在某种程度上篡夺他们所做的事情，并在没有工作的情况下将其货币化，因为如果它真的是重要的功能，有人会做一个分叉并将其货币化。

这实际上是提供这些协同作用——我之前用了这个短语，你有一个精英思想，这有点像提升每个人，对吗？因此，我们可以为需要企业产品细节的客户提供更高的价值，或者如您所说，我们拥有品牌 Liquibase Pro。然后是那些人，他们是社区的一部分，为了他们的特殊需要，他们得到了他们试图解决的问题的投资的多倍回报。

确实是这样的，社区是一个完美的词，因为这是让每个人都过得更好的共同努力。

**Shimel:** 太好了。迪翁，我们快没时间了。我想给你更多的东西来咀嚼。我想让你，在你的脑海中，快进 6 个月，12 个月，做出你的选择——你对 Datical 有什么影响？

**Cornett:** 你知道，我认为我们必须看看——所以，我们正在做的一部分是，我们拿着一张白纸，我们说，嘿，如果我们从今天开始，看看市场的趋势，云、微服务、NoSQL、NewSQL，你知道，这些都不一定是 10 年前由 Nathan 创建 Liquibase 时的情况，与我们现在的情况相比，今天会是什么样子？完美的数据库 DevOps 解决方案与我们目前在社区中拥有的解决方案之间的差距在哪里？随着 IT 基础架构的不断发展，我们如何帮助引导和管理这些解决方案，使其真正解决我们面临的和将要面临的问题？

因此，我认为，如果我们可以在几年后回顾并说，“看，这是产品的发展，它更容易使用，更容易实施，实现价值的时间相对较快，”这确实允许，在一天结束时，我们正在努力让数据库跟上围绕应用程序取得的所有 DevOps 进步。如果我们看到数据库没有像今天这样拖累应用程序、及时性、速度和有效性，那么我知道我们已经成功地进行了这种重新灌输，重新参与到社区中，并将这种创新推进到产品中。

是的。我同意你的观点。迪翁，我答应过 15 分钟内带你离开这里。我知道你另有约会。但我想邀请你回来。也许我们下次会做一个视频，我们可以挖得更深一点。而且，你知道，我喜欢谈论开源，你也是，我们的观众也是。

**科内特:** *【笑声】*

Shimel: 所以，我认为这是我们继续讨论的一个很好的话题。不过，我想祝你在这个世界上一切顺利。那里有一群很棒的人，你是团队中很棒的一员。

科内特:哦，非常感谢。我很感激你的好意，艾伦。是的，我期待着未来的对话。那太好了。

这当然很好。好的，戴安·科内特，Datical 的新总裁，加入我们的 DevOps 聊天。我是艾伦·希梅尔，您刚刚听到的是另一个 DevOps 聊天。祝大家愉快。

— [Alan Shimel](https://devops.com/author/ashimmy/)