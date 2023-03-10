# 学习微体系结构中的产品故障排除技术

> 原文：<https://devops.com/learning-production-troubleshooting-techniques-in-microarchitectures/>

我们行业的一个伟大之处是任何人都可以用最少的工具开始开发。任何人都可以通过某种计算机、文本编辑器、教程和他们的大脑来学习开发。

事实上，如何思考开发问题的最初基础根本不需要计算机，从而进一步降低了入门成本。拥有这样一种不需要很多工具的简单入门方式降低了入门门槛，使更多的人能够加入开发团队并贡献新的想法和观点，从而丰富了整个行业。

进入容器化和构建现代微体系结构是一个稍微高一点的门槛，但只是稍微高一点。有很多精彩的教程可以帮助你开始使用 Kubernetes、Docker、OpenShift Origin 和其他免费的开源工具。

一般软件开发和微体系结构之间入门的唯一区别是:需要一台具有运行容器的处理能力和内存的计算机，并对开发语言有足够的了解，能够使用基本的应用程序。即使是最后一个差异也不是那么重要，因为人们已经构建了如此多的示例应用程序，其明确的目的是教导新人将微服务部署到各种系统上。

然而，当谈到从管理 [Kubernetes](https://devops.com/identifying-and-abstracting-business-intelligence-from-kubernetes-workloads/) 部署或其他现代架构的 DevOps、SRE 或 Ops 方面学习时，我找不到任何可靠的免费教程可以在学生面前倾倒一堆破碎的沙箱，以明确构建他们的故障排除知识。

要深入了解如何让微架构从故障或崩溃中恢复过来，需要接触更大的应用和集群，以及更资深或更有经验的导师——除非你足够幸运，能够构建大型互联应用，并定期向它们发送足以导致故障的流量。

如果没有人愿意在一个缺乏经验的候选人身上冒险，那么缺乏强大的教程和对更多资源的需求使得闯入微体系结构的 DevOps 或 SRE 工作变得特别困难。我想看到这种改变。我们错过了倾听新声音的机会，这些人可能从不同的角度看待问题，或者可能对我们面临的问题有独特的解决方案。

我决定创建一个存储库，里面装满了故意破坏的 Kubernetes 构建，以便新的从业者逐步构建更高级的故障排除技能。基本的想法是建立一个环境金字塔。基础水平应该容易理解和理解。这些环境非常简单，只有一个失败的原因。

我们需要孤立地建立对共同原因的基本认知。我们中许多调试过生产系统的人几乎无意识地掌握了一个共同原因何时出现，这仅仅是因为我们认识到了我们正在分析的数据模式中的微弱特征。但是，如果您从未见过该信号，并且在这些调试挑战中没有导师陪伴，那么学习在数据的大海中找到该信号就要困难得多。这些初始环境应该更容易了解这些信号是什么样子的。

下一级环境会有一些与实际问题无关的附加因素，导致附加日志、附加流量峰值或附加活动。简而言之，这些环境会有噪音。我们可以通过添加另一个在同一集群上运行良好的服务或应用程序，为其中一些环境增加另一层复杂性。这个级别将训练排除系统中未损坏部分的能力，识别未互连的系统，并在不干扰环境其余部分的情况下在一个系统上工作。

金字塔上更高的环境会有多种起作用的因素、转移注意力的东西或复杂的结构。此时，一些环境需要在本地系统之外托管。我仍然在争论如何做这些环境，以便教程仍然是免费的，容易让新手使用——我愿意接受建议。

理想情况下，还会有一个书面的指导，上面有学生在自己解决问题之前不会看的答案和提示，但他们肯定可以查找和学习，不管他们是否解决了问题。毕竟，无论如何想象，故障诊断都不是闭卷考试。

那么如何开始呢？在 [GitHub](https://github.com/nimbinatus/broken-k8s) 找到回购。它是免费的——有麻省理工学院许可的开源软件——并且开放给人们投稿。自述文件中有一个关于 repo 的贡献部分，解释了如果您想要发送提交，应该如何开始。如果您想自己尝试使用这些环境并练习或学习故障排除技巧，初始环境构建在 Minikube 上，Minikube 是一个在本地机器上运行小型 Kubernetes 集群的工具。遵循众多优秀教程中的一个，在您的本地机器上启动并运行 Mikube，然后遵循 GitHub 关于克隆一个 repo 的教程。

或者，你可以直接下载回购。一旦启动并运行了 Minikube，并且在本地机器上有了 repo 的副本，请按照每个环境的目录中的说明将环境部署到本地集群，并开始尝试找出到底哪里出了问题。

想帮助实现这个项目吗？我希望有更多的贡献者！除了可以在线寻求帮助，我还将参加在圣地亚哥举行的 KubeCon 北美 2019。在大会上，我会在 LogDNA 的展位上设立一个黑客角，在大会的大部分时间里，我会坐在那里做这个项目，和其他人一起，等着你。带来你的想法、你的故事、你的破碎环境、你的笔记本电脑、你写文档的意愿、你的 Kubernetes 知识、你自己——任何有助于丰富这个项目的东西都是受欢迎的。

要了解更多关于集装箱化基础设施和云原生技术的信息，请考虑参加 11 月 18 日至 21 日在圣地亚哥举办的 [KubeCon + CloudNativeCon NA](https://events.linuxfoundation.org/events/kubecon-cloudnativecon-north-america-2019/) 。

劳拉·圣马利亚