# DevOps 聊天:DevSecOps 和 OpenShift，带红帽

> 原文：<https://devops.com/devops-chats-devsecops-and-openshift-with-red-hat/>

在本次 DevOps 聊天中，我们与 Red Hat 的高级首席产品经理 Kirsten Newman 进行了交谈。这是一个关于 DevSecOps 的状态以及 Red Hat OpenShift 团队如何努力使开发者、开发者和网络人员更容易合作来创建更安全的应用程序的大讨论。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/785410855&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/785410855&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

**艾伦·希梅尔:**大家好，我是艾伦·希梅尔，DevOps.com，集装箱杂志，安全大道——您正在收听的是另一个 DevOps 聊天。欢迎，我想欢迎我们的 DevOps 聊天 Kirsten 红帽新人。柯尔斯顿，欢迎你。

克里斯汀新人:谢谢你，艾伦。很高兴来到这里。所以，我是你说的柯尔斯顿新人，红帽子。我在 Red Hat 的重点是针对云原生应用的 DevSecOps，现在已经在 Red Hat 工作了大约四年。这真的很有趣。这些年来，我设法利用了我的各种不同的背景元素。我在 Rational Software 工作了九年，从事开发工具的工作。

Shimel: 当然可以。

**新人:**对。我在 BMC BladeLogic 的运营部门工作了一段时间，在 Black Duck Software 工作了七年，专注于帮助公司管理开源软件中的漏洞的解决方案，这让我转到了 Red Hat，在那里我开始专注于 OpenShift security 和 DevSecOps 等所有方面。所以，DevOps—

Shimel: 确实如此。

**新人:**对。

**Shimel:** 我的意思是，在你的职业生涯中，我想我非常了解所有这些公司，也认识很多人——我确信我们甚至有很多共同工作过的人。

新来的人:我想是的。

**Shimel:** 很搞笑。所以，你在 Rational，离开 Rational 只是为了回到 IBM Rational。

**新人:**我知道！*【笑声】*确实如此。

你知道，这就是生活的循环，伙计。*【笑声】*

**新人:**这就是生命的轮回，没错。

**希梅尔:**欢迎光临。所以，Kirsten，听着，DevSecOps 对我们来说当然是很亲近的东西。我们每年都会在 RSA 大会上展示我们的 DevSecOps Days 或 DevOps Connect/DevSecOps Days。

**新人:**嗯嗯。

**Shimel:** 我们实际上在周四有现场直播的虚拟活动，我想是 3 月 26 日，也就是 26 日。

**新人:**好听。

**Shimel:** 所以，你知道，坦率地说，这整个安全问题是我进入 DevOps 的原因，我认为这是一个安全治愈许多原罪的好机会。

**新人:**绝对。*【笑声】*

但是无论如何，你知道，当我们看到 DevSecOps 和 DevOps 世界时，Kirsten，你不能不注意到 Kubernetes 和整个云原生运动对此的影响。

**新人:**好的。

**Shimel:** 和一个伟大的—

新人:绝对没有——变化很大，是的。

**Shimel:** 你知道，从基础设施的角度来看，这确实是目前正在进行的许多工作的核心。很多时候，我不知道人们是否喜欢其他的东西，对吗？我记得当云出现时，我们从客户端-服务器和所有这一切。安全性，总是有滞后，对吧，“哦，是的，我们必须用这个做安全性。”

新人:没错。

**Shimel:** 我想，我们和 Kubernetes 也有一点这样的合作

新人:不，我认为这很公平。

Shimel: 是吗？你知道，人们争先恐后地做 Kubernetes，试验它，部署它，然后有人开始说，“等等，这里的安全性怎么样？合规呢？这个或者那个呢？”

**新人:**对。

现在，我将告诉你，我对你的意见很感兴趣——我认为这次的滞后时间比我们过去看到的要短得多。

**新人:**哦，我绝对这么认为。我认为这很有趣。我观察到的一些事情。一个是，我真的认为容器和 Kubernetes 创造了一个极好的机会，将安全性向左转移，我会在几个方面更明确地说明这一点。但事实上，我曾与公共部门的一位网络防御主管共事过，他相信并宣扬容器可以提高安全性，我剽窃了他的观点，因为我真的认为那是正确的。

由于模型中的变化，以及操作系统依赖性和运行时间，所有东西都打包在一起，而且您总是从不可变的容器映像进行部署，您真的可以用一种新的方式来管理事情，但不是每个团队都准备好了，也不是每个团队、每个安全供应商都准备好了。

所以，我认为机会是双重的。一种是调整对安全性的思考，使它不再成为最终发生的事情，但这仍是一个过程，仍有大量工作要做。另一件事是，安全工具领域本身在历史上是相当孤立的，对吗？你知道，有操作系统层安全、网络层，还有我正在使用的 SIEM 和 SOC，以及我的证书管理和保险库。

它们中没有一个真正被设计为与 Kubernetes 和 containers 支持的自动化水平一起工作，这导致了对较小公司的这种非常有趣的开放，实际上，许多现在已经存在一段时间的初创公司开始打破这些孤岛，并以一种真正符合 DevSecOps 模型的新方式提供安全功能，因为你会看到一个供应商带来了一系列功能，从 CI/CD 集成到运行时安全到网络安全，这是一个非常有趣的空间，可以看到它是如何发展的。

Shimel: 真的有。Kirsten，我要告诉你的另一件事是，当我第一次看到人们通过容器和 Kubernetes 谈论安全性时，我再次受到鼓舞，这真的就像——让我扫描一下您的容器的漏洞，对吗？

**新人:**对。*【笑声】*

我对自己说——我不在乎我的代码是在容器中，还是在管理程序中，还是在裸机上。漏洞扫描就是漏洞扫描。这肯定不仅仅是一个漏洞扫描之类的东西。

**新人:**绝对。我认为，正如你之前提到的，Kubernetes 在这一领域已经取得了长足的进步。所以，有些事情就像，如果我们思考——所以，绝对是这样。漏洞扫描是基本的，人们总是能理解。他们倾向于——从历史上看，他们在生命周期中发生得有点太晚了，给 AppDev 团队等带来了挑战。

我们看到这种转变发生了很大的变化，但是为了将安全性构建到平台中，您应该做和可以做的事情还有很多。例如，当我们在 Kubernetes 中看到 pod 安全策略时，Kube 管理员可以通过这种方式利用 Linux 特性，在 Kubernetes 层实现容器隔离，并执行诸如确保容器不会以不必要的权限运行之类的操作。

Shimel: 当然可以。

**新人:**因此，我们看到了更多的功能——现在，这仍然是测试版，所以社区仍然有一些工作要做。但正如你所说，我们看到了更多的重视，你知道，由 CNCF 赞助的开源 Kubernetes 安全审计就是一个很好的例子。

哦，当然可以。看，CNCF 已经完成了约曼的工作。他们在整个 Kubernetes 项目中做得非常非常好，特别是在安全性方面。

你知道，但是其中一个原因，比如—我们昨天做了一个网上研讨会，它是关于，你知道，不同云提供商版本的 Kubernetes 和—

**新人:**嗯嗯。

**Shimel:** *【相声】*环境。你知道——太棒了，我们有 700 多人注册了这个网络研讨会。

**新人:**太好了。

**Shimel:** 很多很棒的问题，甚至后来在 YouTube 上，很多很棒的问题。在听人们谈话的过程中，我明白了一件事——你知道吗？无论是 AWS、Azure 还是 GCP 或其他什么，设置我的 Kube 环境对我来说可能不是最好的事情，因为我更希望获得一个软件包发行版，或者更完整的解决方案，Kubernetes 是其中的一部分，像 OpenShift，但也提到了其他一些——Rancher 等等。

**新人:**当然。

Shimel: 但是 OpenShift 是最受欢迎的一个。我认为其中一个原因是，人们想知道安全性已经被纳入其中。

**新人:**对。

**Shimel:** 除了 Kube 版本之外，无论是 1.4、1.5、1.6，你知道，K8 还推出了什么

**新人:**对。

**Shimel:——**为了让它更简单？

**新人:**当然，这是我们 Red Hat 的一大关注点，真的，从一开始就是。您知道，企业解决方案—这是一个我们已经讨论过需要根据技术进行调整的安全工具变化的地方，但总的来说，原则仍然适用。你知道，你仍然需要审计日志，对不对？您知道，您仍然需要从集群本身记录数据。您需要来自应用程序的日志数据。你需要监控工具。所以——你还需要考虑主机逮捕的安全性。

因此，我们实际上已经将堆栈视为跨越所有这些东西的堆栈，我们希望尽可能轻松地将该解决方案作为一个解决方案来管理，对吗？所以，如果你——很多人都这样做，你知道，并从中获得价值。但是，如果您有能力自己动手做 Kubernetes，添加日志堆栈，添加企业解决方案真正需要的所有不同部分，那么您必须单独维护它们，也要单独维护主机操作系统。

因此，我们最近真正关注的是自动化一切，包括主机操作系统，尤其是 OpenShift 4。所以，Rel CoreOS，Fedora CoreOS 作为开源项目提供。这是一个容器优化的操作系统，我们将其作为完整平台的一部分进行管理。这使得在集群中应用操作系统更新变得更加容易。你可以用一种让你表现良好的应用程序零停机的方式来做到这一点。你可以让一个节点停止服务，就像 Kubernetes 管理它一样。用 OpenShift 或其组件或操作系统本身的补丁更新它，让它重新投入使用。

因此，从整体上看整个堆栈，企业需要什么来确保他们有一个安全、稳定、高度可用的环境，并确保我们在整个堆栈中利用 Kubernetes 出色的声明性和自动化功能。

绝对的。你知道，我真的没有意识到——你知道，直到你刚才说了，我从来没有把你们正在做的事情拼凑起来。很神奇，不是吗？

**新人:**真的很酷。我们要做的另一件有趣的事情是，我们实际上——回到主机操作系统层，好吗？如果您需要扩展您的集群，这意味着添加一个新的主机，您需要确保部署该基础架构，并根据您的标准保护该基础架构，然后在其上放置 Kubernetes，并将其添加到集群中，您就可以在其上放置工作负载了。

我们正在使用 Kubernetes 操作符的概念来自动化 OpenShift 的组件，包括主机操作系统。我们有一个 machine config 操作符，所以如果你在云中部署 OpenShift，在那里你可以很容易地自动添加基础设施，你可以使用 machine config 操作符和 Kubernetes 的声明性质，对吗？它是一个容器优化的操作系统，主要以容器映像的形式提供，用户空间是只读的，您已经声明了主机应该是什么样子，您只需使用 machine config 操作符即可启动新主机并将它们添加到您的集群中。

**希梅尔:**优秀。你知道，我想，如果我们不提及整个新冠肺炎以及它对事情的影响，我们将会玩忽职守。

新人:很公平，是的。

**Shimel:** 在我看来，首先，我不认为我们现在看到的很多情况及其影响必然是三周或六周，或者，你知道，很多事情会持续下去。

**新人:**对。

**Shimel:** 我认为有一件事会一直持续下去，那就是人们想要更多的自动化，对吗？

**新人:**绝对。

**Shimel:** 在部署、运营和基础设施方面。

新人:没错。

**Shimel:** 从安全的角度来看，自动化是一把双刃剑，对吗？至少我们，从—从安全角度来看，当事情自动化时，我们认为我们确切地知道会发生什么，所以我们可以围绕它进行计划。另一方面，安保人员会变得有点神经质，你知道，当事情从我们冰冷的手里出来的时候。

**新人:**对。

**Shimel:** 你怎么看？怎么样——你觉得怎么样？

**新人:**我知道；我同意你的观点。我认为 Kubernetes 的一个方面是，它在某种程度上突破了安全团队的界限。随着时间的推移，我与许多不同的安全团队交谈过。所以，这有点像——你知道，在这一点上，他们对应用程序层的开发运维的想法更适应一些，对吗？对于那些将要部署的容器化应用程序，这就像—好吧，他们有一种想法，“是的，安全静态分析工具，集成的漏洞扫描器集成。”我在市场上看到了一些很酷的新东西，它们是开始评估配置和 docker 文件的工具，这真的很棒。

但是，随着我们继续进入运营领域，Kubernetes 和 SDN 是任何 Kubernetes 集群都需要的，现在我们已经将服务网格添加到组合中，或称为 Istio，用于基于微服务的通信。网络安全团队对谁来管理 Kubernetes 层的网络策略感到不安，现在，我也有了服务网格或 Istio 策略，谁来负责这些策略？

最后，这真的是关于可见性。因此，如果我们回到自动化，我们实际上是将基础设施视为代码，GitHub 的模型同样适用于 Kubernetes 层，也适用于 Kube 集群的配置，我们需要到位，您需要自动化来获得最佳结果，但您需要以一种方式让安全团队能够看到他们习惯看到的各种事情。

因此，我认为这是我们开始以新的方式向左转变的另一种方式，我还看到了一些解决方案，它们有助于根据对环境的评估自动生成网络策略，或者根据对应用配置的评估自动生成服务网格策略。

但所有这些，你知道，网络安全人员不一定会登录到集群中查看。那么，他们如何获得他们需要的视图，以及他们如何帮助 AppDev 团队理解整个风险管理和他们的安全视角？所以，这不仅仅是关于工具，而是关于人和过程，对吗？我认为这里有如此多的丰富性，但你是完全正确的——没有自动化我们就做不到。因此，我们必须帮助这些人适应这种转变，同时确保他们获得所需的可见性，知道事情正在以符合他们的风险指导原则、监管要求和他们想要的安全态势的方式进行。

**Shimel:** 所以，对我来说，DevSecOps 的一个根本问题，DevSecOps 的一个根本转变是，首先，安全人员认识到他们不是唯一关心安全的人。

**新人:**嗯嗯。

**Shimel:** 信不信由你，开发人员和 DevOps 人员确实关心安全性。他们可能没有受过安全培训，但他们关心安全。

我认为第二件事是，开发人员必须认识到，DevOps 团队必须认识到，安全人员不仅仅是路障。

**新人:**对。

Shimel: 他们不会总是说不的人。

**新人:**对。

**Shimel:** 我们是什么——所以，这本质上与技术无关。这是人与人之间的问题。

**新人:**绝对。

**Shimel:** 我认为我们在这方面取得了真正的进展，因此，我们看到的是安全人员为开发运维团队的开发人员正在使用的安全工具付费并给予认可——

**新人:**对。

**Shimel: —** 在 Kubernetes 平台上—

新人:没错。

**Shimel:——**你知道，因为这是现在的首选平台，对我来说，这让我对此保持乐观。

**新人:**对。不，我同意，而且，当我们考虑更广阔的前景时，我的意思是，安全威胁一直在不断发展，不断变化。而且没有足够的受过安全训练的专业人员，对吗？没有足够的网络安全人员，等等。

因此，我们必须弄清楚，我们如何帮助团队扩展，协作是实现这一目标的途径。你说得对，我看到了和你一样的东西，对，安全团队正在批准那些容器原生的工具，Kube 原生工具有助于确保。在某种程度上，我并不是说这是一种消极的方式，但在某种程度上，他们是被迫这样做的，因为他们是传统的工具，过去在后端使用，在容器和 Kubernetes 的世界中并不有效。

因此，他们真的必须顺应我们在供应商领域看到的这种转变，这只是为协作和共享知识开辟了一个极好的机会，你知道，有时这对人们来说是一种调整。

**Shimel:** 是啊，同意，同意。Kirsten，当我们第一次开始时，我说，你知道，时间过得很快，我只会让你在这里呆 15 分钟——嗯，那是 21 分钟前。

**新人:** *【笑声】*好了。

席梅尔:我们——是的，我们做到了。好吧。我们得结束这个案子了。也许我们会让你下次再来，我们—

**新人:**是计划！

**Shimel:——**可以在那里继续对话，好吗？

**新人:**太好了。非常有趣——非常感谢你，艾伦。

**Shimel:** 谢谢。

**新人:**好的。

Kirsten 新人，红帽子，我们的客人。我是《集装箱日报》和《安全大道》的艾伦·希梅尔，在 DevOps.com 的[。您刚刚听到了另一个 DevOps 聊天。大家保重。](https://devops.com/)

— [Alan Shimel](https://devops.com/author/ashimmy/)