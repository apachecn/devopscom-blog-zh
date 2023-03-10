# DevOps 聊天:使用 MemSQL 的云原生应用的数据库

> 原文：<https://devops.com/devops-chat-database-for-cloud-native-apps-with-memsql/>

数据和数据库技术正在经历颠覆。收集的数据量呈爆炸式增长，为颠覆性服务和新公司创造了新的潜力。数据分布在云和数据中心的不同位置。此外，云技术带来了过多的数据库类型、分布选项、分析能力和 AI/ML 处理。任何不利用数据为客户和业务带来好处的公司都只会成为下一个被破坏的受害者。

Nikita Shamgunov， [MemSQL](https://www.memsql.com/) 联合首席执行官/联合创始人，加入 DevOps Chat，讨论这些破坏性因素如何改变容器化和云原生应用的数据收集和存储方式。速度、大量数据收集、分布式设计和规模都是 Nikita 认为对当前和未来的云原生应用至关重要的挑战。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/680565254&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/680565254&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

米奇·阿什利:大家好，我是米奇·阿什利和 DevOps.com，您正在收听的是另一个 DevOps 聊天播客。今天，MemSQL 的联合首席执行官和联合创始人尼基塔·沙姆古诺夫来到了我的身边。今天的主题实际上是看数据库的状态，市场和技术，就像我们现在考虑数据库一样。尼基塔欢迎加入 DevOps 聊天。

**尼基塔·沙姆古诺夫:**谢谢，谢谢——很高兴来到这里。

阿什莉:很荣幸能请到你。感谢加入我们。你能从自我介绍开始，告诉我们一点你是做什么的，以及一点关于 MemSQL 的信息吗？

沙姆古诺夫:绝对是。我叫尼基塔·沙姆古诺夫，是数据库公司 MemSQL 的联合首席执行官和联合创始人。在 MemSQL 之前，我在脸书工作，在此之前我在微软工作，负责 SQL server 内核。所以，我是经过培训的内核工程师。在此之前，我在俄罗斯圣彼得堡获得博士学位。

**阿什利:**优秀，优秀。好吧，让我们直入主题吧。在开始播客录制之前，我们聊了一会儿。你知道，数据库已经存在很长时间了，你知道，几十年前创建的技术仍然在许多领域生产，但也发生了很多变化。为什么不谈谈正在改变数据库环境的一些市场力量呢？

沙姆古诺夫:绝对是。因此，我认为有几种市场力量和行业力量正在穿透市场和技术。第一个是数据量在增长，对吗？

阿什利:嗯。

Shamgunov: 还有很多公司——举例来说，你不必走得太远，你知道，像优步、网飞、亚马逊和谷歌这样的公司，它们的大部分价值来自数据，对吗？80 年代的人会将这些公司中的任何一家描述为美化了的数据库应用程序——但是，当然，它们远不止于此。

随着数据量和数据种类的增长，区分赢家和输家的标准是人们能够多好地捕捉数据并根据数据采取行动。

阿什利:嗯。

**沙姆古诺夫:**对吧？一个很好的例子是，你知道，当你叫一辆优步时，你知道，你把它放在你的手机里，然后你就知道车在哪里，他们多快到达，你需要多长时间到达目的地。

这真的非常非常强大。我们现在都习惯了这一点，但 10 年前，这不是现实，也不可能。这是第一个力，对吗？人们看到谁是那些在市场上前进的公司，他们想在他们的州，在他们的类别中抓住同样的机会。

他们也害怕被下一个优步、下一个脸书、下一个亚马逊——尤其是亚马逊——所颠覆。

阿什莉:没错。

**Shamgunov:** 因此，正在经历的第二个市场力量是建筑。而且，因为数据量在增长，摩尔定律不再适用，所以我们不能只依赖更好、更便宜的硬件，我们必须构建分布式系统。

而且，在数据库世界中，分布式系统在很大程度上直到最近才变得新奇起来。我们开始看到分布式数据库系统——而现实是，很难建立一个分布式的记录事务系统，并使其为生产做好准备，因为其中包含的技术数量巨大，并且不同的、在市场上成功的其他数据库产品已经有 30 多年的历史了。想想 Oracle，想想 SQL Server。

阿什利:嗯。

**Shamgunov:** 当这种大规模的架构变化出现在需要重新设计这些系统的业务现实中时，供应商实际交付这些系统就变得非常非常困难。这是第二种市场力量。转场*【相声】* —

阿什莉:尼基塔，如果可以的话，我想问你一点关于这个的问题，关于-

Shamgunov:—走向分布式系统—请讲。

**Ashley:** 您认为分布式架构的出现很大程度上是因为内部数据中心与私有云和公共云之间的转移吗？是更多的把内容推到边缘，做缓存？它是否将内容推向某个地理位置？是什么推动了数据库的分布？

**Shamgunov:** 这是一个非常好的问题，首先，因为我要说的是，目前正在发生的第三大市场力量正在转移到云上。

阿什利:嗯。

**沙姆古诺夫:**对，还有云，如果你把它和电平行，对，世界上大部分都在云中消耗电力，你知道吗？你只要把你的东西插到插座上，电就来了。

阿什利:嗯。

**Shamgunov:** 在建筑物中，发电机仍然存在于重要的地方——制造业、医疗保健、医院——但它只占全球电力消耗的很小一部分。

同样，在云中使用 it 也很有意义，在 IT 中，您知道，有应用程序、分析、数据库、机器学习—您知道，通常云提供商现在提供的所有服务。现在，如果我们接受这种世界观——当然，我们看到了电力领域发生的事情，这与 IT 领域发生的事情是一样的——那么您可以将同样的事情划分到不同的工作负载中。一旦你放大数据库工作负载，你会意识到，是的，你想把目前运行在数据中心的工作负载转移到云中。

云是不同的，你知道吗？云中最重要的是软件只是作为服务运行。但是，它也创造了一个机会，为云重建 it 的每一部分。这已经发生了。在我们的空间中，它已经发生在数据仓库中，但由于 Okta，它也发生在身份上。它发生在云存储上，像亚马逊上的 S3 或 Dropbox 这样的服务是更高层次的服务。因此，基本上，随着基础架构 it 向云转移，我们正在为云重建 IT。现在，碰巧的是，通过这种重建，您想要满足下一代工作负载的需求。这就是分布式系统的用武之地。此外，您正在为云进行架构设计，因为云中的成本等式是不同的。

因此，与传统架构相比，可伸缩性和弹性允许您提供更好的成本平衡。所以，如果你有一个 Oracle，是的，你可以在云中运行它，在 EDM 中，没问题。实际上，与专为云设计的系统相比，它的速度太慢、成本太高，而且成本也可伸缩，所以从存储和计算的角度来看，您只能消耗您所需的资源。存储计算网络带宽—运行工作负载所需的一切。但它也将更加高效，因为像 EDM 一样运行数据库，每个人都会告诉你这不是一个好主意，但如果它是一个为云设计的数据库服务，那么你可以针对并绕过限制，针对所有可用于云的服务和资源进行构建。

**Ashley:** 我想问你的是，应用程序的提升和转变与数据库的提升和转变之间似乎有相似之处。如果您只是将应用程序引入云环境，那么它就不是为云而设计的，但是您必须重新设计、重建、利用数据库即服务等优势。对吗？

沙姆古诺夫:绝对是。好的，在应用程序领域，与云不同的是，某些应用程序可能比其他应用程序更受欢迎。如果您只是将这些应用程序放在虚拟机中，那么很有可能会过度调配和调配资源不足。

对于不太受欢迎的应用程序，运行一个应用程序会浪费整个虚拟机，而对于非常受欢迎的应用程序，您没有足够的网络带宽或 CPU 来大规模运行该应用程序。这就是为什么 Kubernetes 真正改变了游戏规则，如果你基于 Kubernetes 构建，你可以预发布可伸缩的、无状态的应用。然后，如果你在云中运行它，当然，你用来驱动这些应用程序的数据库，你作为服务消费。

**Ashley:** 再多说一点，因为我们已经在其他网络研讨会和播客上讨论过数据的状态性与构建软件和重建软件的动态性，后者可能与数据库的状态不匹配。在 Kubernetes 环境中，您如何处理这种情况？

沙姆古诺夫:所以，这里有两个部分。第一个是，您在 Kubernetes 环境中运行您的应用程序，并通过数据库作为服务来消费数据。这是当今云架构的蓝图。假设你在 Amazon 上运行你的 Kubernetes，你的应用程序是用任何语言编写的，但是假设是 Node.js，你启动 DynamoDB，使用 Amazon 示例，作为一个服务，你从应用程序连接到数据库，这就是你的应用程序。

现在，在关系数据库的世界里——顺便说一下，它比对象数据库占有更大的市场份额——

阿什莉:当然，是的。

沙姆古诺夫:而且理由很充分。您可以用类似的方式运行它。你知道，在这种情况下，你可以启动 MemSQL 作为服务，你知道，在 Kubernetes 集群内运行你的应用程序。

您可以做的另一件事是，您可以将 MemSQL 带到 Kubernetes 环境中。这为您提供了控制力和云的可移植性。现在，您不仅可以将您的应用程序部署到 Kubernetes 中，并根据应用程序的需求和受欢迎程度来扩展应用程序，而且存储数据和为应用程序提供支持的数据库也可以部署在同一个 Kubernetes 集群中，它会做同样的事情。它将根据您的应用需求伸缩。

因此，它为您带来了云的可移植性。例如，你可以打包行李，从 AWS 转到 Google，它允许你做的另一件事是把它从云带到本地。今天，这样做的原因通常是双重的。要么是安全性和合规性，要么是成本，对吧？如果工作负载非常静态，并且您无法通过应用程序和数据基础架构的弹性来实现较高的效率，那么内部部署可能仍然更便宜，这将促使您将其付诸实施。

**Ashley:** 当您不仅在一个云内移动，而且跨云移动时，拥有一个单一的工具来执行 ETL 与将它们分离开来相比有多重要？

Shamgunov: 嗯，我认为，归根结底，我们在谈论锁定，我们在谈论开发人员的生产力。那些是完全不同的。现在，锁定是我们这个领域的许多人在使用 Oracle 供应商产品时都会遇到的问题。

阿什莉:当然可以。

Shamgunov: 在那里，他们经历了他们所说的勒索循环。每次 Oracle 续约时，您最终都要与 Oracle 谈判，如果您想减少数据库开销，这将是一次非常困难的对话。您知道，Oracle 会进行审核，他们有权这样做，因此他们会检查并找到所有使用 Oracle 的应用程序。如果您减少了使用量，Oracle 会提高维护费或下一次许可费。

所以，在这个供应商身上花很多钱真的很难摆脱。我们在大型企业中一次又一次地听到这种说法。我与一家大银行的首席信息官交谈过，Oracle 在那里的支出是几年 10 亿美元。

阿什利:不奇怪，是的。

Shamgunov: 如果你仔细想想，这绝对是疯狂的，对吗？原因在于，除了成本之外，Oracle 一直是提供服务的优秀合作伙伴。您知道，银行运行—在他们的银行中，这是一家消费者银行，它运行在 Oracle 上。

但与此同时，竞争对手也在追赶功能，对吗？MemSQL 附带了一个非常强大的记录功能系统，迄今为止，这一直是 Oracle 的强项，您知道，它具有更具吸引力的价格、更灵活的部署模式以及在云中作为数据库即服务运行的能力，我们可以保证 SLA 有足够的时间。随着人工智能和人工智能的集成，我们看到，这个等式正在缓慢但肯定地发生变化。而且，你知道，人们会严肃地提出问题，“为什么我们要在这项技术上花这么多钱，我们能不能不要这样做？在这里，我们将节省数亿美元，提升股东价值。除此之外，我们将让我们的开发团队行动得更快，对吗？

那么，回到你关于跨云和开发人员生产力的问题，对吗？第一个是锁定，我举了一个 Oracle 锁定的例子。但是现在，首席信息官们不想因为与单一的云提供商结婚而陷入同样的陷阱。你知道，感谢上帝，市场上有多家云提供商，其中三家在美国非常非常强大，你知道，在很大程度上，它们的能力相似——GTP、Azure 和 AWS。

所以，一个关键企业选择两三个云供应商是非常典型的。这就防止了锁定。然而，为了真正避免锁定，你必须选择允许在所有云上以相同方式运行软件的服务提供商。

阿什莉:没错。

Shamgunov: 理想情况下，他们以路径服务的形式提供服务，就像数据库服务一样，这种服务在每个云上都可用。如果是这种情况，那么，你知道，你依赖于供应商，但你不依赖于大型供应商，这是云之一。因此，这是我所认识的每个首席信息官最关心的事情。

**Ashley:** 你对甲骨文的看法很有道理，这可以追溯到 2000 年代或者 90 年代。你知道，对 VLDB 来说，这确实是镇上最好的比赛，可以说。也许你也可以去微软。

**沙姆古诺夫:**嗯嗯。

阿什莉:但今天不是这样。当你去找云提供商时，你有很多选择，我可以想象，像你这样的人，生活在所有这些云环境中，或者多个云环境中。因此，您也可以为客户提供服务，当然，这些客户将拥有一个云计算战略。

当然，你知道，我说得再好不过了。

阿什利:好的，太好了。*【笑声】*锁定那个——太好了。当人们从传统的 VLDB 环境迁移到云环境时，我们再来看看 Oracle，他们面临的最大挑战是什么？为了真正考虑如何利用云的灵活性，您必须做出什么样的范式转变？

如果你想离开甲骨文，有一个三步走的策略。任何数据库技术的最大粘性是所有基于数据库构建的应用程序，它们在应用程序之间使用和共享数据。不同的数据库技术可以是应用兼容的，比如 MySQL 和 AWS Aurora，对吧？

阿什利:嗯。

Aurora 是一个新的数据库，但它的计算部分实际上是 MySQL 代码，所以它们是应用兼容的。如果一个应用程序能对抗 MySQL，它也能对抗 Aurora。

所以，这就是为什么在 MySQL 和 Aurora 都参与的低端市场，这可能是一个可行的策略。这是一个非常好的方法，对吧，因为只需将你的应用指向不同的数据库就很容易了。不同的数据库产品很难实现两个数据库之间的应用程序级兼容性。

第二个是工作负载兼容性。因此，我们所有运行在 Oracle 上的工作负载都可以转移到另一个数据库，前提是有足够好的理由。您知道，假设您要将工作负载迁移到的数据库具有所有相同的功能集，并提供强大的记录保证系统等等。

因此，如果您的工作负载兼容，那么您可以从一个数据库转移到另一个数据库，但是您需要做一些工作，对吗？您需要扩充并可能重写应用程序的某些部分。

阿什利:嗯。

**Shamgunov:** 在我们的领域中，有一大块市场被称为第一层工作负载。这些第一层工作负载通常在 Oracle 上运行，它们要么有非常非常强的记录系统要求，要么有性能要求，要么有可用性要求，要么有非常强的并发性要求。

由于我们的体系结构，我们实际上是唯一一个可以将工作负载从 Oracle 转移到 MemSQL 上的游戏，特别是像 Oracle 这样的系统——您知道，在企业存储上运行的大型 Oracle 系统或像 Oracle Rack 或 Oracle Exadata 这样的系统。我们有无数的例子来说明我们是如何将客户从 Oracle 手中解放出来的。

所以，坦白地说，这是我们最大的机会。因此，您将不得不投入一些工作，但是如果您正在经历的痛苦如此之大，以至于您愿意投入这些工作，那么我们是迁移您的 Oracle 工作负载的绝佳目的地。

阿什莉:嗯，很好。你是一位很棒的客人，也是一次迷人的谈话。我希望我们有更多的时间聊天。也许我们可以在另一个播客上这样做。

好了，谢谢大家，我还要感谢我的观众尼基塔·沙姆古诺夫(Nikita Shamgunov)加入我们，他是 MemSQL 的联合首席执行官和联合创始人。

沙姆古诺夫:是的，很高兴来到这里。非常感谢。

阿什莉:没错。感谢我们的听众。我是 DevOps.com[的米奇·阿什利](https://devops.com/)，您已经收听了另一个 DevOps 聊天播客。在外面要小心。

— [米切尔·阿什利](https://devops.com/author/mitchellashley/)