# JFrog 启动区块链项目以保护开源软件

> 原文：<https://devops.com/jfrog-launches-blockchain-project-to-secure-open-source-software/>

在其 [swampUP](https://swampup.jfrog.com/) 活动上，JFrog 今天发布了 Project Pyrsia，这是一个开源项目，使用区块链平台和 [Sigstore](https://containerjournal.com/?s=Sigstore) Cosign 和公证人 V2 加密签名软件来保护软件包。除了 JFrog，该项目的其他贡献者包括 Docker，Inc .、DeployHub、Futureway 和[甲骨文](https://devops.com/?s=Oracle)。

JFrog 的开发者关系副总裁 Stephen Chin 表示, [Project Pyrsia](https://swampup.jfrog.com/) 将使组织能够为存储在安全的存储网络中的开源软件组件建立一个出处链。

Chin 指出，实际上，Pyrsia 项目正在利用分散的 Web3 技术来保护开源供应链。他补充说，使用区块链平台验证软件组件完整性的方法将确保开发者使用的任何软件组件都不会受到损害。

最终，我们的目标是将 Pyrsia 项目贡献给开源安全基金会(OpenSSF)，OpenSSF 是 Linux 基金会的一个分支，作为一个联盟，它正在寻求协调努力，以更好地保护开源软件。JFrog 自己的研究发现了 20 多种不同的开源软件供应链攻击，其中两种涉及零日威胁，没有即时可用的软件补丁。网络犯罪分子正在瞄准开源项目，因为任何被包括在内的恶意软件稍后都会出现在任何数量的下游应用程序中。他们的最终目标是在他们选择的时间激活恶意软件。

在去年发现影响 Java 应用程序的零日 [Log4Shell](https://devops.com/?s=Log4Shell) 漏洞后，保护开源软件成为一个更紧迫的问题。许多开发人员经常重用开源软件，但是这些项目中有许多是由少数程序员维护的，这些程序员自愿贡献他们的时间和精力来构建其他人可以免费使用的组件。像任何其他开发人员一样，这些人拥有的安全专业知识是有限的；确保软件安全的责任落在决定部署软件的组织身上。问题是，许多开发人员认为软件比实际更安全。像 Project Pyrsia 这样的项目是[的一部分，它是一个更大的努力，使维护者更容易保护开源软件](https://securityboulevard.com/2022/05/openssf-seeks-150m-to-address-open-source-software-security/)。

尚不清楚安全问题是否会促使组织审查他们使用的开源软件的数量。大多数组织比他们意识到的更依赖于开源软件，因为大多数打包的应用程序将包括开源组件。每当发现零日漏洞时，组织可能会花费数月时间来寻找可能易受攻击的开源组件的所有实例。

从理论上讲，对开放源码软件的日益关注应该会导致更多地采用 DevSecOps 最佳实践，从而减少生产环境中的漏洞数量。与此同时，考虑到几乎每个组织都在使用开源软件组件，对它们进行更多的审查是必要的。