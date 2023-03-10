# 虚拟机支持的并行测试环境

> 原文：<https://devops.com/boomtown-no-bust-vm-supported-parallel-testing-environment/>

## 新兴城市开发流程简介

[BoomTown](http://boomtownroi.com/) 使用一套特定的 DevOps 流程，为房地产专业人士提供最新的房地产列表和房屋数据以及 CRM 解决方案和分析工具。“我们的开发、运营和质量保证团队可以自动完成一切，同时将云提供商和其他服务最适合的任务转移给这些提供商，”BoomTown 质量保证经理布莱恩·鲍姆加特纳说。

仅举一个例子，BoomTown 最近采用了亚马逊网络服务(AWS)来托管其基础设施的各个方面。“它使我们能够提供高可用性和弹性服务，同时允许我们的开发团队专注于改革房地产软件行业，”鲍姆加特纳说。

鲍姆加特纳解释说: [Docker](https://www.docker.com/) containers 支持 BoomTown 的常规部署流程，将环境设置容器化，以获得更可靠、有序的部署体验，无论公司是将代码推向 QA 还是生产。 [TeamCity](https://www.jetbrains.com/teamcity/) ，JetBrains 提供的构建管理工具和 CI 服务器中日益流行和频繁出现的名字是 BoomTown 的 go to build 平台。 [New Relic](https://newrelic.com/) 是 BoomTown 的首选性能管理解决方案，支持生产应用和服务器性能的实时透明，让 BoomTown 市民(客户)满意。

## 使用 Sauce Labs 虚拟机进行规模测试之前和之后的新兴城市

在应用[酱实验室](https://saucelabs.com/)之前，BoomTown 的 QA 分析师团队专门以手动方式处理所有软件测试。每次试运行都要经过他们的圈/机器/笔记本电脑。在新功能发布之前，分析师通常会通过几种不同的浏览器和版本对产品或功能执行一整套回归测试，以验证新版本及其功能。鲍姆加特纳说:“对于大型项目来说，仅这个过程就需要两周时间。”。

BoomTown 现在使用一个测试自动化框架，该框架是用几种流行的 DevOps 工具构建的。BoomTown 的测试高级软件工程师 Joey Gryder 说，定制的测试自动化利用了 [Ruby](https://www.ruby-lang.org/en/) 、 [Selenium WebDriver](http://www.seleniumhq.org/projects/webdriver/) 、 [Cucumber](https://cucumber.io/) 、 [MySQL](https://www.mysql.com/) 、 [Sinatra](https://github.com/sinatra/sinatra) 和 [Angular JS](https://angularjs.org/) 。该框架提供了历史和实时测试结果的 BoomTown 视图，以及通过仪表板前端软件连接到后端系统来运行手动测试的能力。

BoomTown 应用单个 web 服务来断言测试系统自动化特性的控制和操作。一个“测试运行器”库使 QA 能够以并行执行的方式运行 Cucumber 特性。BoomTown 使用 MySQL 存储测试结果。“当我们将所有这些与 Sauce Labs 的虚拟机结合起来时，我们可以使用我们的完整测试套件在各种浏览器配置上安排夜间测试运行，”鲍姆加特纳说。这使得 BoomTown 每晚可以对软件进行多达 100 次测试。

## 并行化

就节省时间、资源和工时而言，BoomTown 软件测试框架中的秘密是使用 Sauce Labs 虚拟机来支持许多并行的自动化测试。这使得 BoomTown 最长的一个半小时的试运行时间缩短到不到 15 分钟。

“使用 Sauce Labs，可以轻松启动任意数量的并行虚拟机，针对您想要的浏览器进行配置，以运行一组 Selenium WebDriver 测试步骤。鲍姆加特纳解释说:“如果没有这样的解决方案，BoomTown 的测试团队将不得不通过一台机器和一个浏览器在本地执行整个测试套件，或者建立一个内部测试实验室来实现并行浏览器测试。”。(酱实验室显然不是唯一一个竞争对手包括 [BrowserStack](https://www.browserstack.com/) 和 [TestingBot](https://testingbot.com/) 的玩家；让您的尽职调查成为您选择最适合您需求的服务的指南。)

BoomTown 认为卸载工作是最好的选择，这样可以加速耗时的测试任务，防止 QA 成为 CD 上与时间相关的瓶颈。“我们只是通过增加虚拟机数量和并行运行更多测试来做到这一点，”鲍姆加特纳说。

添加虚拟机和增加并行测试实例的数量是一种易于扩展的方法，即使 BoomTown 添加了测试并延长了总测试运行时间，它也能继续提高测试速度和驱动 CD。

鲍姆加特纳说，使用由 Sauce Labs VMs 支持的自动化并行测试可以解放 QA 分析师，让他们在测试中更有创造力，找到越来越多有趣的方法来打破测试负载下的应用程序；同时，自动化测试“机器”验证团队已经建立的平凡且重复的测试。

“我们最近将自动化作为质量关纳入了我们的 CI 流程。在一个拉取请求被接受之前，它必须通过一组在 Sauce Labs 中运行的关键路径 UI 测试。这在我们的日常开发过程中设定了一定水平的质量期望，从而节省了我们的测试时间，”Gryder 解释道。