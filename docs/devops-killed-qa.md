# DevOps 是如何杀死 QA 的

> 原文：<https://devops.com/devops-killed-qa/>

如果你从事软件质量保证(QA)工作，是时候找份新工作了。

整个软件开发过程总是由以下核心活动组成:

*   创建需求分析；
*   产生软件人工制品的规范；
*   构建软件；
*   调查产品或服务的质量；
*   发现并修复缺陷；然后
*   部署到生产环境。

在大多数组织中，这一过程通常发生在一种或多种方法中，如瀑布或敏捷。在瀑布中，测试过程发生得相对较晚。软件被生产出来，QA 团队发现缺陷，然后软件被修复。这最后两个实践在一个循环中重复，直到管理层认为可以向公众发布为止。

在敏捷中，个人和团队——包括 QA——紧密合作，在持续的基础上发布并更新软件，而不是一次性部署整个平台。DevOps，正如我们在我们的“[中所写的，什么是 DevOps？](http://logz.io/learn/what-is-devops/)"指南，是敏捷开发的下一代。敏捷是软件开发中的一种思维方式；DevOps 更进了一步，它是一种具体的文化变革，在一个组织内实施这一理念。

这种实现消除了 QA 作为组织中一个独立实体的需要，并将质量责任分散到不同的团队，尽管许多人认为仍然需要这种形式的规程。

## DevOps 中 QA 的过去解释

![devops qa](img/916530b45d168a968dd64c9864d8f26c.png)一个常见的说法是，DevOps 位于开发、运营和质量保证维恩图的[中心:](https://www.soapui.org/testing-dojo/world-of-api-testing/dev-ops-trends.html)

> 一方面，QA 与开发一起工作，试图将更多的测试推入持续集成系统。测试必须零人为干预，并生成自己的测试数据。
> 
> 另一方面，QA 与运营部门合作开发监控工具；也许是为了在生产中连续进行冒烟测试。运营部门可能正在开发用于生产系统备份和恢复、部署回滚的脚本，或者用于灾难恢复的脚本。

NeoTYS 的 Tim Hinds 对这个问题有不同的看法，他说“DevOps QA”是为了防止缺陷，而不是发现缺陷。

> QA 在这个组织结构中起着关键的作用，因为他们有可见性和指导方针，在代码工作时推出代码，在代码不工作时退回代码。这与 10 年前的 QA 组织有很大的不同，QA 组织的主要职责是发现 bug。今天，QA 团队负责防止缺陷到达公共场所。

恕我直言，两者都是错的。

## **为什么 DevOps 不需要 QA**

DevOps 经常使用持续集成(CI)和持续交付(CD)。在 CI 中，开发人员使用各种[持续集成工具](http://logz.io/blog/continuous-integration-tools/)每天多次将代码集成到共享存储库中，DevOps 依靠自动化来确定版本的质量。如果您想要运行 CD，您不能有任何人工交互，这确保了存储库中一批代码的任何版本都可以在任何给定的时间发布。

本质上，传统的 QA 无法在完整的 CI/CD 环境中工作。在旧的结构中，软件质量的责任在 QA 手中。今天，它是 DevOps 文化和方法的一部分——开发人员现在拥有责任，而不是组织内的一个独立实体。

具体来说，DevOps 需要使用供应商和工具，如 [BUGtrack](http://www.bugtrack.net/) 、 [JIRA](https://www.atlassian.com/software/jira) 和 [GitHub](https://github.com/) 来汇总和报告软件错误和缺陷。测试自动化工具包括 [Selenium](http://www.seleniumhq.org/) 、[cumber](https://cucumber.io/)、 [JUnit](http://junit.org/) 、 [TestNG](http://testng.org/) 和 [JMeter](https://jmeter.apache.org/) 管理、执行和测量功能测试和循环。

最后，如果在开发和运营之间有一层人员，那么您就无法无缝地执行 CI 和 CD，因此也就无法执行 DevOps。要运行一个合适的 DevOps 操作，你根本不能有 QA。

## **质量保证的未来**

那么，所有从事质量保证工作的人会怎么样呢？随着越来越多的组织转移到 DevOps，他们变得越来越多余，美国最快乐的工作之一可能不会快乐太久。

根据美国劳工统计局(BLS)的数据，软件质量工程是高科技职业之一，其增长率预计比平均增长率低[:](http://www.bls.gov/ooh/about/data-for-occupations-not-covered-in-detail.htm)

![qa job outlook](img/f34c221b3971d59610ffb9814f1d15f5.png)

然而，BLS 的数字可能太大了，因为该局根本没有将“DevOps”视为一个独立的职业:

![image02](img/6b4b07e645d080dc6127d7726a70456d.png)

作为证据，只要看看谷歌趋势中“sqa 工作”的相对谷歌搜索数如何缓慢下降，而“devops 工作”的相对谷歌搜索数如何迅速增加:

![qa jobs vs devops jobs](img/20a59f28a63ed75f751c49e197c6802f.png)

对于 QA 来说，趋势肯定不好看。