# Log4j 如何成为严重的 DevOps 问题

> 原文：<https://devops.com/how-log4j-becomes-a-serious-devops-problem/>

最近发现的[Apache Log4j](https://logging.apache.org/log4j/)漏洞对任何开发软件的人都有广泛的影响，尤其是对 DevOps 领域的人。该漏洞([CVE-2021-44228](https://nvd.nist.gov/vuln/detail/CVE-2021-44228))最令人担忧的是 Log4j 的使用有多普遍。该漏洞在大量应用程序中报告，并直接影响众多[Apache](https://www.apache.org/)项目，包括 Druid、Dubbo、Flink、Flume、Hadoop、Kafka、Solr、Spark 和 Struts。还有无数的[思科程序](https://tools.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-apache-log4j-qRuKNEbd)受到漏洞 的影响。受影响的应用程序和库的列表似乎几乎是无限的，扩展到了 Elastic LogStash、GrayLog2、Neo4J、Steam、Twitter 甚至是[VMware Tanzu](https://tanzu.vmware.com/?utm_content=inline-mention)系列程序。

简而言之，任何使用 Log4J 进行日志记录和跟踪的应用程序都会受到被称为[log 4 shell](https://www.lunasec.io/docs/blog/log4j-zero-day/)的攻击。事实证明，这些攻击很容易被利用，可以用来控制易受攻击的服务器。

## 为什么 DevOps 从业者应该关注

DevOps 的世界是一个不断重复的世界，应用程序的特性和改进被整合到生产环境中。为了加速开发，QA 过程通常局限于最近的变更。

换句话说，开发人员通过他们的[管道](https://devops.com/bridging-the-appsec-and-devops-disconnect/)，通常可以建立一个质量基线，然后通过只测试自应用程序最后一次迭代以来有什么变化来加速他们的 CI/CD 管道。该过程确保了可接受的质量水平，而没有引入被认为是不必要的步骤。

然而，这些流程并没有考虑旧 API 和库中新发现的缺陷，这意味着这些缺陷可能会传到已部署的应用程序中，并使开发运维团队完全意识不到影响和可能的中断。在应用程序部署后检测缺陷就像是本末倒置。

使情况更加复杂的是，许多开发人员缺乏定义明确且维护良好的软件材料清单([【SBOM】](https://www.ntia.gov/SBOM))，这意味着开发人员可能不知道在部署的应用程序中正在使用的组件和/或库。

没有 SBOM，修复应用程序的问题变得越来越困难——尤其是当开发人员一开始就不知道这个问题的时候。

## 责任应该在哪里？

应用程序中引入的漏洞往往成为相互指责的游戏，开发者指责库供应商或 infosec 员工，infosec 指责开发者没有对他们选择纳入应用程序的组件进行尽职调查。

当然，相互指责只会增加焦虑，推迟补救过程，并且无助于确定检测和补救漏洞的责任。DevOps 团队需要将这些争论放在一边，并建立一个处理无意引入的漏洞的流程。更重要的是，DevOps 团队需要在 DevSecOps 上投资，以确保尽快检测和修复漏洞。

为了避免像[log 4 shell](https://www.lunasec.io/docs/blog/log4j-zero-day/)这样的漏洞可能导致的大规模破坏，那些运行 DevOps 的人应该考虑:

*   创建和维护 SBOM
*   部署扫描已发现漏洞的自动化工具
*   自动比较 SBOM 和漏洞
*   将 DevSecOps 流程纳入其 CI/CD 管道
*   频繁测试应用程序的缺陷
*   发现漏洞时与网络安全人员协调
*   频繁打补丁

随着几乎每天都有越来越多的漏洞被发现，DevOps 团队必须时刻警惕他们的应用中整合了哪些组件。此外，随着低代码/无代码工具和集成开发环境(ide)的使用越来越多，DevOps 还需要考虑这些工具是否使用了其他可能受到威胁的库。