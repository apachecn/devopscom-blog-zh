# 2021 年最佳——将传统 Java 应用转变为微服务

> 原文：<https://devops.com/transform-legacy-java-apps-to-microservices/>

随着 2021 年的临近，我们 DevOps.com 想要突出今年最受欢迎的文章。以下是我们 2021 年最佳系列的第十六期。

速度是 DevOps 的主要原则之一，任何保持或提高速度的事情都有利于整个过程。然而，在 DevOps 过程中仍然有许多减速带，这些减速带威胁着进展并使 DevOps 过程慢如蜗牛。当将遗留的单片应用程序转变为对云更友好的东西时，最大的障碍之一就是微服务。

微服务显然是为云开发的应用的未来；研究巨头 [IDC 预测，到 2022 年部署的所有新应用中，90%](https://www.idc.com/getdoc.jsp?containerId=US44403818) 将采用微服务架构。IDC 还指出，微服务的主要好处是提高了开发人员设计、调试、更新和利用第三方代码的能力。虽然 DevOps 倾向于开发内部代码，但是微服务架构提供的好处仍然是一样的。

## 微服务:实现目标

向微服务架构的迁移可能简单，也可能复杂，这取决于组织所走的道路和他们的起点。例如，如果目标是将遗留应用程序转变为微服务，那么过程可能会非常复杂和乏味。遗留应用程序的转换通常意味着手动分解遗留代码，并将其分解为将作为微服务运行的独立代码元素。这对 DevOps 管道来说非常复杂，现有代码的快速迭代是常态，而不是例外。

然而，市场上有一些工具可以简化这个过程。一个这样的工具是 [vFunction，它最近从 stealth](https://devops.com/vfunction-automates-conversion-of-java-apps-to-microservices/) 出来，任务是将单片 Java 应用程序转换成微服务。

![microservices](img/9854fb93b336e47d342ef93ceb4eb570.png)

vFunction 有一个有趣的方法来处理这个过程。 [vFunction 平台](https://vfunction.com/newsroom/vfunction-unveils-the-first-and-only-platform-purpose-built-for-automated-intelligent-and-scalable-cloud-native-modernization/) 部署在本地，其中 vFunction Java 虚拟机(JVM)代理检查遗留应用并收集数据，然后将这些数据收集到 vFunction 服务器上。从那里，软件架构师可以进一步调查收集到的关于遗留应用程序的信息，并开始设计微服务架构来更新代码库。“一旦开发人员对设计感到满意，vFunction 就会生成一个服务规范文件，其中包含创建微服务所需的所有信息，”vFunction 首席执行官兼联合创始人默蒂·拉法林说。“该文件由我们的自动化引擎使用，该引擎扫描原始代码并复制相关工件以创建新服务。”

Rafalin 表示，vFunction 利用监督学习技术、图论和聚类算法来识别死代码和代码异常，从而防止遗留应用程序的彻底崩溃或“分解”。 最终，vFunction 有望实现许多手动步骤的自动化，DevOps 工程师过去常常执行这些步骤来将单片应用程序分解为微服务。根据 Rafalin 的说法，vFunction 使该过程的速度提高了 15 倍，并可以实现 80%至 95%的自动化。目前，vFunction 只专注于 Java，它认为这是当今最大的机会。然而，该公司计划在未来支持用其他语言编写的应用程序。

除了新人 vFunction，还有其他方法来处理将遗留 Java 应用程序迁移到云中的问题。一个例子是 [Anthos](https://cloud.google.com/anthos) ，这是一个将谷歌云服务扩展到 DevOps 环境中的托管应用平台。另一个是 IBM 的[mono 2 micro](https://developer.ibm.com/languages/java/tutorials/transform-monolithic-java-applications-into-microservices-with-the-power-of-ai/)，这是一个基于人工智能的半自动工具集，用于协助重构单片 Java 应用程序。

对于那些希望从零开始构建基于微服务的应用的人来说，有许多工具可供选择。最有趣的是使用快速应用程序开发(RAD)技术和利用低代码模型的开发环境。有几十个可用的 RAD 平台；主要例子有 [造波者](https://www.wavemaker.com/)[外部系统](https://www.outsystems.com/) 和 [敏捷点](https://agilepoint.com/) 。

在大多数情况下，那些将遗留应用迁移到微服务模型的人通常会根据特定的用例选择许多工具。对一些人来说，重写较小的遗留应用程序可能更容易；对于其他人来说，重构可能是获取遗留应用程序中知识产权的唯一方式。无论哪种方式，仔细选择合适的工具都有助于保持 DevOps 领域的速度。事实证明，保持这样的速度对于在预算内按时构建云友好型应用至关重要。

Rafalin 说:“除非人们将这些单一的应用程序现代化，使之成为云原生的，否则它们最终需要非常大的机器，并且最终往往要向云提供商支付更多的费用。”“组织现在明白，如果他们想要获得云的真正优势，他们需要对这些应用进行现代化。这从采用包含微服务、API 和现代设计原则的架构开始。”

教训是要明智地选择，选择支持规模和增长的工具集，以及能够支持微服务需求的工具集。