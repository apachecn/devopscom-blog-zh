# DevOps 聊天:lumi go Aviad Mor 的无服务器智能

> 原文：<https://devops.com/devops-chat-serverless-intelligence-with-lumigos-aviad-mor/>

Lumigo 发现自己正处于当今基础设施部署的最大浪潮之一——无服务器时代。这并非偶然，该公司成立于大约一年前，其使命是提供一个无服务器的智能平台。

创始人是前检查点的人，他们看到了基于最佳实践的平台的需求，以帮助在不同的公共云提供商(包括 AWS Lamdba、Azure 和 Google Cloud)之间部署无服务器有效负载(应用程序)。

在这次 DevOps 聊天中，我们与首席技术官兼联合创始人 Aviad Mor 就该公司和无服务器市场进行了交谈。像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/623133621&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/623133621&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

**艾伦·希梅尔:**大家好，我是艾伦·希梅尔，DevOps.com，安全大道，集装箱杂志，您正在收听的是另一个 DevOps 聊天*。*今天 DevOps Chat 的嘉宾是 Aviad Mor，他是一家名为 Lumigo 的公司的首席技术官/联合创始人。

**Aviad Mor:** 对，对。

希梅尔:好的。阿维亚德，欢迎你！

早上:嗨，艾伦。我很高兴今天能参加你的播客。

Shimel: 我们很高兴你能来。Aviad，让我们从这个开始。我不认为很多人——也许我错了，但我不认为我们的观众中有很多人对 Lumigo 非常熟悉。告诉我们背景。公司是关于什么的？

![Lumigo Aviad Mor](img/0cb620d6554f42d295487b563a743be7.png)

**Aviad Mor, Lumigo**

早上:好的，当然。我很乐意。所以，Lumigo 是一家创业公司。我们成立于大约一年前，我们在无服务器领域。我们是一家专注于无服务器监控和故障排除的公司，我们正在做的是，我们让客户能够看到他们的系统，了解发生了什么，并在总体上允许他们采用无服务器。

绝对的。当然，你知道，无服务器确实是热门技术之一，我的意思是，它是一个时髦的词，被夸大了，但它确实是下一代基础架构的热门技术之一，因为我们继续从单纯的基础架构即服务转向平台即服务，现在无服务器可以托管您的分布式应用程序。

我认为——你知道，Aviad，我们生活在一个泡沫中，我们说没有服务器，人们知道我们在说什么，对吗？

**Mor:** *【笑声】*

但是我们有时需要记住这一点——忘掉非 IT 人士。他们认为没有服务器，他们一定认为这是某种黑魔法。但是，即使人们可能不了解云架构和一些最新的容器化和应用程序托管，他们也不能百分之百确定什么是无服务器。

对于许多人来说，它几乎是 Lambda 的同义词，对，是 AWS 的 Lambda 平台。

**Mor:** 对，对。

Shimel: 你知道，我确定——说吧。

**Mor:** 对。所以，我认为 Lambda 是——它是无服务器的核心。AWS 在大约四五年前宣布 Lambda 时，那是无服务器运动的开始。Lambda 是什么，是一种功能即服务。它很快。这让我们看到——它允许用户运行他们的计算，运行他们代码的特定部分，而不必关心任何服务器、任何容器。他们只需编写代码，上传到云提供商，然后决定代码的触发因素。

希梅尔:是啊。

Mor: 因此，他们可以毫无问题地运行它，不需要安装任何东西，也不需要在出现任何安全问题时进行更新。但我想说的是，我认为 Lambda 和功能是一种服务，这更多的是技术部分。我认为，在许多方面，无服务器是一种思维方式。因为无服务器伴随着它周围的整个生态系统。您有一个无服务器的数据库和 API 网关，例如，文件存储也是无服务器的。这很重要，因为当你想在云端建立一个完整的架构，一个完整的应用，你不能只使用函数。你需要一起使用所有这些不同的部分，你现在可以有一个完整的架构，它只由你没有安装的东西组成，好吗？

**Shimel:** Mm-hmm.

Mor: 所以，我认为无服务器的主要部分是服务器是别人的问题。例如，AWS 或谷歌或微软，无论你在哪个云上运行。

Shimel: 当然可以。当然，这就是其中的一部分，对吗？在云环境下，基础设施是别人的——所以，你在和一个在互联网时代从事托管和基础设施业务的人交谈，对吗？我们过去销售我们称之为电源、ping 和管道的产品，对吗？然后，有了云，您不必—您不必销售电源、ping 和管道。你提供了，人们并不真正关心，他们只是建立在管理程序之上。

现在，我们看到，他们甚至不关心整个过程，甚至在某些时候通过操作系统，对吗？他们只是把它放上去——他们只是上传他们的应用程序。

你知道，我们提到了 AWS Lambda，但你也提到了微软和谷歌云，虽然我认为 AWS 像在许多云领域一样，可能是领先的参与者，但不一定是无服务器领域的领先参与者，你知道，微软和谷歌也有一些非常好的产品。

**Mor:** 对，对。

Shimel: 我想知道你在市场上看到了什么。所以，你比我处理得多。

**Mor:** 对。所以，你知道，当我们看我们的客户时，我们看到 AWS 是明显的领导者。我认为这个数字在无服务器中大约是 60%或 70%。但是谷歌和微软 Azure，他们正在进行一场真正的战斗。他们不断提出创新，有时甚至提供 AWS 中没有的东西。

I think that, in many ways, serverless is a way of thinking.So, I think that, as we progress over time, we’ll see more and more users in Microsoft and in Google. Although today, as you said, most of the people you talk to, they’re using AWS and a lot of times the people who are using Microsoft and Google are people who are already using it for other things in the cloud.

**Shimel:** 对。

Mor: 因此，他们更容易在同一个云中添加无服务器。

**Shimel:** 让我问你一个问题——不在云中的无服务器怎么样？如果您想称之为“提供无服务器、本地无服务器”,您看到了什么吗？

Mor: 对，是的。所以，我们看到了。很少，我必须说。通常，它是开源的——例如，你有 OpenWhisk 和其他。我们通常在他们不能在公共云中运行的地方看到这种情况。

举个简单的例子，国防部队不想在公共云上运行，而是自己运行。但通常是在公共场合，因为我认为无服务器最重要的是让别人为你打理一切。

因此，在一天结束时，如果您仍在构建基础架构并运行开源，这很好，但您仍然非常清楚您有多少台服务器，如何扩展它们，以及需要手动更新的任何问题。

所以，我认为这里的公共云是一个明显的领导者。

Shimel: 当然可以。好了，不用服务器了。好吧，我们将更多地讨论无服务器，但现在让我们来谈谈 Lumigo，对了，以及你们为在无服务器环境中托管应用程序的人做了什么。

我看着它，对我来说，有点 APN 的无服务器，如果你愿意的话。但是还有一种部署前最佳实践方法，以便您可以在部署前进行检查。您是否使用了最佳实践？这是做这件事的正确方法吗？此外，还有部署后监控和警报。公平吗？

Mor: 是的。所以，我认为总的来说，你明白了。我认为 APN 不会完全错。但是，在无服务器领域，我们确实面临着新的挑战，对吗？这是一项新技术，它提供了令人惊叹的东西，但归根结底，它是新的，它有自己的挑战。

其中一个主要的挑战是无服务器的本质是分布式的。因此，当您实现无服务器时，您会有许多不同的部分、微服务，其中的每一个都非常容易部署，并查看它的确切运行情况。但是如果你是，比如说，负责这次行动的 DevOps，你会想看看整个系统是如何协同工作的。你想看看它们是如何联系在一起的。

这在无服务器的世界中变得非常困难，这就是为什么你需要像 Lumigo 这样的东西来为你绘制一切，向你展示你的环境的可视化，这样你可以看到你在哪里有问题，你在哪里花了很多钱，也许，这是我们将要谈论的一点。就像你说的，你是完全正确的——有时你可以在部署它们之前捕捉到这些东西。无服务器附带了许多小东西，我认为开发人员随着时间的推移会具备这些技能。但是现在，我们可以帮助他们节省资金和时间，只需在他们部署 Lambdas 之前查看它们，并告诉他们如何做得更好。

很公平。那么，你知道，我不禁会想，不是每个人都会将其整个基础架构迁移到无服务器的，对吗？因此，在可预见的未来，坦率地说，你将拥有一种混合，就像我们对云一样，对吗？这是一个混合云环境，您拥有混合应用程序环境。我的一些应用程序可能在无服务器环境中，一些不在无服务器环境中，等等。

你知道，现实世界的例子，公司都有，他们有什么，他们怎么做，Lumigo 能全面帮助他们吗，或者 Lumigo 他们集成到其他东西，或者我们只是需要不同的工具和不同的观点来托管我们的应用程序。

艾伦，我认为这是一个很好的问题。我们开始关注无服务器，因为我们发现这是最大的难点。但是，我们越来越多地看到客户使用无服务器，他们中的一些人，姑且称之为纯无服务器环境。但也很常见的是两者都有，在混合环境中两者都有，例如 Kubernetes 和 serverless。

We started out focusing on serverless because we saw that’s where the greatest pain point is.And it does make sense, because it’s not one size fits all. Some tasks are better run by containers. For example, long running tasks that take hours, and some tasks are much better with the serverless; for example, event based or answering quick APIs. So, we see hybrid solutions, and that’s why we’re now starting to give our own solution for distributed tracing. Because when you’re looking at your environment, it just makes sense that you want to see them all in one tool. You want to see how they’re all interconnected.

所以，现在，我们开始研究容器和 Kubernetes，看看它们是如何协同工作的。所以，现在如果，例如，你有一个 Lambda，其中有一个故障，你可以看到导致该故障的确切事件链，不管调用该 Lambda 的是另一个 Lambda 还是一个容器，都没关系。您可以查看和浏览所有这些不同的呼叫，并尽快修复和找到根本原因。

**希梅尔:**优秀。Aviad，正如我向你提到的，时间过得很快。这是我想探讨的另一个领域，也是你的个人旅程。你知道，每当我足够幸运地在节目中有一位联合创始人或首席技术官这样的人时，我总是喜欢——因为有人在听，他们刚刚开始他们的职业生涯，或者他们想进入这个行业，或者他们可能已经在公司工作过，但他们渴望或梦想开始自己的，建立一个公司。

给你的听众介绍一下你的个人背景，以及你是如何来到这里的。

Mor: *【笑声】*嗯，当然，当然。我职业生涯的大部分时间都在 Checkpoint 工作，这是一家大公司，实际上在以色列，它是最大的网络安全公司之一——实际上，在全世界，它是最大的网络安全公司之一。

在那里呆了很多年后，我决定搬家。我不得不承认，一方面，做这件事一直是我的梦想，一直是我做自己的事情的梦想，一些小事。另一方面，这并不容易，我有机会和 ________ 一起工作，他不仅是我的同事，也是我非常非常好的朋友，我们知道我们必须一起工作。

但是我会给你们举一个例子。人们，你知道，走过来对我说，“祝你好运，但是你知道，你太老了。你已经 38 岁了，有妻子和三个女儿。你不能这么做。这只是年轻玩家的游戏。”

**Shimel:** Mm-hmm.

Mor: 但是，你知道，这就像——这是一种强烈的欲望。你知道你必须这样做，而在我进入之后，首先，当然，我得到了我家人的祝福，因为没有那，没有我妻子那样做，这是不可能的。

然后我也很高兴看到我已经获得的经验确实有一些意义。不仅仅是因为你已经*【笑声】*了，我说的是老了，就像他们对我的称呼一样，但这确实意味着你有经验，你知道如何与客户打交道，以及如何在大企业工作。最终，这是一个伟大的组合。

所以，现在，当我看它的时候，它是非常艰苦的工作。我看我女儿的次数没有我想的那么多，但我知道这是我一生中做的最好的决定之一。我可以告诉你，最令人兴奋的事情之一是在生产中，在客户的生产中，看到 Erez 和我自己设想的东西，它出现在一年前的一个 PowerPoint 上。现在它正在运行并帮助实际的客户？那是一种很棒的感觉，真的。

席梅尔:我知道，这很有成就感——听着，我去过那里。你想知道真相吗，38 岁对于一个初创公司来说并不算老。因为，从一个创业到另一个创业，我都在努力回想。我创办了我的第一家公司——我大概 33 岁，实际上是 34 岁。但我认为你需要一定的经验，对吗？

现在，有些人会告诉你，在像 Checkpoint 这样的文化中工作，尽管它很大，但与在 IBM 或这些真正的大公司中工作相比，仍然具有相当的企业家精神。所以——还有，整个以色列科技界。这是一个新兴国家，我认为这也有所帮助。

但是，你知道，你提到了一些我认为人们没有给予创始人足够信任的事情，那就是——这并不容易，你要花很多时间远离家人，度过很多艰难的时光，周末和商务旅行，你知道，做你必须做的事情。在那里，很多人在工作的时候，在一天结束的时候，他们带着清醒的头脑回家，对吗？所以，事情就是这样。

在我们——因为我们，我们现在可能超时了，Aviad，但我想让你谈谈 Kubernetes 在无服务器中的作用。我要在我们结束这个播客后去 KubeCon，你知道，他们看起来有联系，但没有联系，对不对？你对此有什么看法？

**Mor:** 嗯嗯。我认为，最终，它们以两种方式联系在一起。我认为我们必须记住，虽然是云提供商在做，但无服务器功能是在容器上运行的，对吗？所以，他们可能在 Kubernetes 或类似的东西上运行。这是在基础设施层面上，尽管作为开发人员，您并不关心这些。

但另一方面，我认为随着无服务器的增长，我们看到它在增长，它不会取代 Kubernetes。它将与它并列，我认为未来的技术栈将是像 Kubernetes 和 SaaS 这样的无服务器事物的组合，对吗？所有这些将为每一家公司提供他们所能得到的最佳解决方案。

**希梅尔:**优秀。Aviad Mor，首席技术官，Lumigo 联合创始人——感谢您成为本次 DevOps 聊天的嘉宾。

艾伦，非常感谢你。这真是一种享受。

好的。我是艾伦·希梅尔，来自 DevOps.com media ops、安全大道、集装箱杂志——您刚刚听到了另一个 DevOps 聊天*。*祝大家今天愉快。

— [Alan Shimel](https://devops.com/author/ashimmy/)