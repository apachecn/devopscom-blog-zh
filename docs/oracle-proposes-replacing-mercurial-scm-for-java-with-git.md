# Oracle 提议用 Git 取代 Mercurial SCM for Java

> 原文：<https://devops.com/oracle-proposes-replacing-mercurial-scm-for-java-with-git/>

Oracle 今天在其 [Oracle Developer Live—Java](https://developer.oracle.com/developer-live/java/) 活动上提议对 Java 进行一系列更新，包括用 Git 替换 Mercurial 源代码管理(SCM)平台，这是 Oracle 创建的用于向 Java 社区共享更新的存储库，从 Java 16 的初始可用性开始，然后将项目本身迁移到 GitHub。

此外，Oracle 还开发了与 GitHub 和 GitLab 兼容的服务器端工具，以及与 Git 和 Mercurial 兼容的客户端工具，以帮助进行迁移。这项工作基于 Skara 项目，该项目已经为 Mercurial SCM 库提供了所有活动的和统一的开发路线的只读 Git 镜像。

Oracle 还计划在 Java 16 中增加一个矢量应用编程接口(API ),并启用一些 C++特性。

Oracle 今天还宣布了对 Java 15 的增强，包括支持 Edwards-Curve 数字签名算法、隐藏类和重新实现传统数据报套接字应用编程接口(API)。此外，对更高级的垃圾收集工具和文本块的支持已经完成。

在 Java 15 中，其他一些高级但尚未最终确定的功能包括对密封类的支持、增强的模式匹配、记录和访问外部内存的 API。

Java 开发人员关系副总裁 Chad Arimura 说，总体来说，最新的创新显示出古老的编程语言仍然充满活力。尽管有过多的选择，大多数企业 IT 组织仍然主要依赖 Java 来构建应用程序，即使他们正在过渡到基于部署在 Kubernetes 集群上的容器来构建基于微服务的应用程序。Arimura 指出，就这一点而言，Java 没有遭受与 COBOL 编程环境相同命运的危险，COBOL 编程环境在创新的步伐中变得相对陈旧。

这些组织中的许多也在采用围绕 Git 存储库的最佳 DevOps 实践的道路上走得很远。他说，采用 Git 作为 Java 项目的 SCM 库将通过简化已经标准化 Git 库的组织的工作流程来进一步推动这些工作。

虽然 Java 继续主导着企业应用程序的开发，但各种规模的组织都在使用更广泛的编程工具，这也是事实。通过采用 Git 和 GitHub，Java 社区将能够更流畅地与使用各种编程工具创建的各种开源项目共存。企业开发人员显然仍然依赖 Java 来编写他们的大部分服务器端应用程序，但是更多的客户端代码正在使用基于 JavaScript 等框架来开发。

然而，与此同时，希望实现应用程序组合现代化的 IT 组织应该能够相信这样一个事实，即在 Java 最初推出近 30 年后，它仍然具有相关性。现在的挑战是确定在所有年龄段的开发人员现在经常使用的大量其他编程工具中，在哪里最好地依赖 Java。