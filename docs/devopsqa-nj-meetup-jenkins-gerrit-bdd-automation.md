# DevOpsQA NJ Meetup: Jenkins 与 Gerrit 和 BDD Automation

> 原文：<https://devops.com/devopsqa-nj-meetup-jenkins-gerrit-bdd-automation/>

[DevOpsQA NJ](https://www.meetup.com/DevOpsandAutomationNJ/) 最近与 Jenkins 和 BDD 举行了关于自动化的四月会议，来自 CloudBees 的 Kishore Bhatia 和来自 Billtrust 的 Tom Bartolucci 担任演讲人。场地、食物和茶点由 [Audible](http://www.audible.com/) 在纽华克历史名城的一个最先进的大型办公场所提供。

在享受了披萨、葡萄酒和啤酒之后，我们开始了 Tom Bartolucci 关于 BDD 自动化框架的演讲。Tom 从事网络软件开发已经超过 13 年了。他用 Java 编写了应用程序。NET、PHP、Python 和 Javascript，面向出版和移动视频领域的客户。目前，他是位于 SaaS 的支付周期管理公司![TomPresentation1](img/e70b2fa828e2e21aa497685e46668edd.png)bill trust 的开发副总裁。他的 13 名 web 开发人员团队致力于交付 6 个比尔·信托 SaaS 产品，并使用 Codeception，一个基于 PHP 的 BDD 框架进行测试。

根据 Tom(我们都同意)的说法，这个想法不是要找到 bug，而是要阻止它们。他在 Billtrust 的团队选择了 Codeception，因为它允许用 PHP 编写测试，这是其开发团队所使用的；还支持 Selenium WebDriver、PhantomJS 和 BrowserStack 并且有各种工具、平台和内置报告的挂钩。因此，它的进入门槛很低，并使 Codeception 的团队迅速起步。进行跨浏览器测试可以让他们发现 IE 漏洞，这是他们之前由于主要在 Firefox 中测试而错过的。Codeception 允许测试人员创建 BDD 风格的可读测试，类似于 Cucumber spec，但是作为代码编写。简单的语法使 QA 团队能够编写他们能够阅读和理解的代码。开发人员能够添加定制模块，因为框架是用他们熟悉的 PHP 开发的。Codeception 有多种用途，包括编写验收测试、单元测试和 API 测试。

Tom 还描述了 Billtrust 如何将 Codeception 与 Jenkins 集成在一起，以执行测试并发布报告。然后，他进行了该框架的现场演示。在会议结束时，有很多关于 vagger 集成、并行化、失败的测试重新运行以及 Codeception 和 Cucumber 之间的差异的好问题。

接下来，来自 Cloudbees 的 Kishore B ![KishorePresentation1](img/93cbb6b916cb6a2b2383fe5b7d5dcf8a.png) hatia 做了一个关于 Jenkins pipelines 和 Gerrit 代码评审的演讲。[基肖尔·巴蒂亚](https://twitter.com/BhatiaKishore)供职于 [](https://xebialabs.com/) [CloudBees](https://www.cloudbees.com/) ，用开源软件构建定制框架，帮助客户解决持续交付和大规模开发的工程问题。Kishore 是 Jenkins 的专家，在 FinTech 企业软件和云平台方面有开发经验。几个月前，Kishore 和 Issac 做了一个关于 Jenkins Workflow 的演示，展示了 Workflow 如何消除连接多个管道的瓶颈。

这一次，焦点集中在一个非常有效的用例上:一个大的代码库，许多团队为代码做贡献。团队不应该在电子邮件上合作。他们应该得到由他们使用的工具完成的通知和提交后验证。在这种情况下，它是 Gerrit——Google 开源项目，提供自己的 Git 实现。您只是希望这项工作神奇地在幕后运行，为您进行代码审查。这个场景中的主要挑战是您想要快速失败——只要任何步骤失败就报告 CI 结果，并确保没有孤立的构建。

Kishore 随后演示了在 Jenkins 中实现该用例所涉及的步骤，包括将拉请求验证添加到构建步骤中，允许开发人员直接在 VCS 工具中获取构建状态，只有在出现故障时才返回 Jenkins。目前，将每个状态发布到 GitHub 是有限制的。需要设置的关键事项—Gerrit 基础架构、Jenkins 安装、Jenkins 将参考的工作流。虽然一开始看起来很复杂，但是一旦你开始使用这个工作流，使用 Groovy script helper 之类的东西，它就会变得简单。Jenkinsfile 将定义在开发、QA、登台和生产中应该发生的事情的流程。Kishore 接着做了一个很棒的流程演示，并回答了观众提出的问题，包括并行提交和测试数据管理。

在课程结束时，我们进行了抽奖，三名幸运的获奖者获得了 Audible 赞助的奖品，包括一台亚马逊 Echo。期待我们的下一次会面。

如果您想了解更多关于 Jenkins 工作流程的信息，您可以通过 [【电子邮件保护】](/cdn-cgi/l/email-protection#0e656c666f7a676f4e6d62617b6a6c6b6b7d206d6163) 联系 Kishore。要了解 Audible 的更多精彩机会，请访问 http://about.audible.com/或联系 [【电子邮件保护】](/cdn-cgi/l/email-protection#572438393623382532173622333e353b327934383a) 。

![GroupPicture](img/c36be371206ab170d3bac3b6e8958fc7.png)