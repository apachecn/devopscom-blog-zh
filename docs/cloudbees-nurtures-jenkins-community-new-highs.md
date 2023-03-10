# CloudBees 将 Jenkins 社区培养到新的高度

> 原文：<https://devops.com/cloudbees-nurtures-jenkins-community-new-highs/>

DevOps 工具箱中的关键人物之一是 Jenkins。几乎每个人都认识詹金斯。对于那些不熟悉詹金斯的人来说，下面是“什么是詹金斯”页面的摘录:

**詹金斯是什么？**

Jenkins 是一个[获奖的](https://wiki.jenkins-ci.org/display/JENKINS/Awards)应用程序，它监控重复作业的执行，例如构建一个软件项目或由 cron 运行的作业。其中，当前的 Jenkins 专注于以下两项工作:

*   **持续构建/测试软件项目**，就像 CruiseControl 或 DamageControl。简而言之，Jenkins 提供了一个易于使用的所谓持续集成系统，让开发人员更容易集成对项目的更改，让用户更容易获得一个新鲜的构建。自动化、连续的构建提高了生产率。
*   **监控外部运行作业**的执行，例如 cron 作业和 procmail 作业，甚至是那些在远程机器上运行的作业。例如，使用 cron，您接收到的只是捕获输出的常规电子邮件，您可以仔细查看这些邮件，并注意邮件何时中断。Jenkins 保留这些输出，让您很容易注意到什么时候有问题。

Jenkins 提供以下功能:

1.  **易安装**:只需 java -jar jenkins.war，或者部署在 servlet 容器中。没有额外的安装，没有数据库。
2.  **轻松配置** : Jenkins 完全可以通过其友好的 web GUI 进行配置，具有广泛的实时错误检查和在线帮助。没有必要再手动调整 XML，尽管如果您想这样做，也可以这样做。
3.  **变更集支持** : Jenkins 可以从 Subversion/CVS 生成一个变更列表。这也是以一种相当有效的方式完成的，以减少存储库的负载。
4.  永久链接:Jenkins 为你提供了大部分页面清晰可读的 URL，包括一些永久链接，比如“最新版本”/“最新成功版本”，这样你就可以很容易地从其他地方链接到它们。
5.  **RSS/E-mail/IM 集成**:通过 RSS 或 E-mail 监控构建结果，获得关于失败的实时通知。
6.  **事后标记**:构建可以在构建完成后很久才被标记。
7.  **JUnit/TestNG 测试报告** : JUnit 测试报告可以列表、汇总，并显示历史信息，如它何时开始中断等。历史趋势被绘制成图表。
8.  **分布式构建** : Jenkins 可以将构建/测试负载分布到多台计算机上。这可以让你最大限度地利用开发人员办公桌下的闲置工作站。
9.  文件指纹 : Jenkins 可以跟踪哪个构建产生了哪个 jar，哪个构建使用了哪个版本的 jar，等等。这甚至适用于在 Jenkins 之外生产的 jar，并且对于跟踪依赖性的项目来说是理想的。
10.  **插件支持** : Jenkins 可以通过第三方插件进行扩展。你可以编写插件来让 Jenkins 支持你的团队使用的工具/过程。

但是在维基之外，Jenkins 是如何成为有史以来最成功的开源项目之一的呢？答案与 CloudBees 有很大关系，与 Oracle 关系不大，甚至与支持生态系统的架构关系更大，该生态系统允许为核心项目开发近千个插件。

首先，让我们先解决一下 Oracle 的一些小问题。詹金斯原名哈德森。哈德森是由太阳微系统公司创办的。当 Oracle 收购 Sun 时，它继承了许多开源项目(OpenOffice 和 Java 就是其中之一)。开源社区中的许多人质疑 Oracle 关于开源的意图。没过多久，许多 Hudson 开发人员和 Oracle 之间就出现了争议。甲骨文声称他们拥有术语 Hudson，这有一个简单的答案。进行了投票，哈德森成了詹金斯。甲骨文一反对，詹金斯就成了哈德森的一个分叉(或者哈德森成了詹金斯的一个分叉)。甲骨文还维护着哈德森，相比詹金斯就是个空壳。

与此同时，JBoss 前首席技术官 Sacha Labourey 在 2010 年创办了 CloudBees。这是在 JBoss 被红帽收购之后。CloudBees 创建了 PaaS，这是首批支持从开发到部署的整个应用生命周期的 PaaS 之一。CloudBees 产品的一个关键部分是 Jenkins 持续集成(CI)引擎。Labourey 引入了 Kohsuke Kawaguchi，他是 Jenkins 的创始人和主要贡献者。除了 Kawaguchi，其他几位主要的 Jenkins 贡献者也来到了 CloudBees。

CloudBees 及其员工为 Jenkins 贡献了超过 80%的代码。詹金斯和支持它的社区正在蓬勃发展。我有机会和川口谈论这个问题。他很自豪现在 Jenkins 有超过 1000 个插件。我被詹金斯网站每月 50 万的下载量惊呆了。

当然，一个繁荣的开源社区不一定会转化为繁荣的商业。有许多公司从未破解开源成功的模式。

这就是 CloudBees 看起来会赢的地方。我和 Kwaguchi 谈到了 CloudBees 的商业成功。CloudBees 在世界各地设有办事处，能够将一个标志性的开源项目转化为蓬勃发展的业务。他们有一套企业(准备付费)插件，以多种方式增强詹金斯。此外，提供托管版本的詹金斯，CI-a-a-S 如果你愿意。他们呼叫詹金斯行动中心。他们还提供[【电子邮件保护】](/cdn-cgi/l/email-protection)，这是其他服务和软件的保护伞，这些服务和软件增强并使 Jenkins 在不同平台上更容易使用，具有不同的语言和其他选项。当然，他们也为您的 Jenkins 安装提供支持。

总而言之，Labourey 和 Kawaguchi 在 Jenkins 的基础上建立了一个繁荣的商业实体，同时保持 Jenkins 作为一个健康、不断增长的开源项目。他们工作出色，值得称赞。

这并不是说詹金斯没有竞争对手。有一些开源项目，也有一些商业项目，声称可以更好更快的做 CI。当然，他们中的许多人受益于已经有 Jenkins 作为模板，并在此基础上逐步改进。您可以在以下网址查看 Jenkins 竞争对手的完整列表:[https://www . G2 crowd . com/products/Jenkins/competitors/alternatives](https://www.g2crowd.com/products/jenkins/competitors/alternatives)

虽然这些竞争对手中的一些在这里或那里提供了改进，但总的来说，詹金斯仍然是衡量他们的标准。在 CloudBees 指导和管理 Jenkins 的情况下，在可预见的未来，它可能会保持这种状态。