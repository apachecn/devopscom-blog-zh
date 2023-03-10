# 为期两个月的 Hello World

> 原文：<https://devops.com/two-month-hello-world/>

*项目启动如何破坏大型组织的开发工作*

“hello world”应用程序是开发人员(通常是初学者)为学习一门新语言而编写的最基本的程序。这是一种“一切正常”——一个堆栈检查应用程序，可以快速启动一个项目并查看其结果。

生成的 hello world 程序通常是打印到屏幕上的一条消息:“Hello world。”就是这样。没有微服务，REST API 或者类工厂，但是非常令人满意。堆栈工作；你白手起家建立并经营它。

程序员编写 hello world 应用程序代码的平均时间可能是几分钟，甚至几秒钟。设置开发人员的计算机或工作站和服务器以编译/构建和运行 hello world 应用程序的平均时间可能会更长，可能需要几个小时来设置。我在考虑云服务器或容器。将 hello world 应用发布到 Google Play，包括设置、构建和部署，对于第一次使用的人来说需要几个小时。那还不算太糟。但是情况是这样的:运行第一个程序只需要几分钟，而第一次部署需要几个小时。

这是 60:1 的比例。

让我们把标准提高一点:以一家拥有 1200 多名员工的 IT 部门的大公司为例。在这种环境下，发布一个全新的 hello world 应用程序的平均时间至少会增加一个数量级——如果开发人员不仅要使用应用程序，还要将自己或她的团队加入到组织中，时间会增加更多。

随着史诗、用户故事和客户需求的堆积，减少 IT 部门的繁文缛节是一个很大的干扰。这些任务可能简单也可能复杂，比如设置您的代码库和开发栈；身份、安全、磁盘、网络和其他堆栈配置；样板工件和后续测试和发布策略。这是一个相当长的请求链和等待期——足以让 hello world 程序在投入生产之前循环几个月。

## Hello World 的 DevOps

企业应对市场变化的能力始于新项目的快速增加。在微服务领域，这是常有的事。但这主要是在架构层面。除微服务之外，调配和管理外部环境有多容易？或者，在您的组织中调配和管理整个开发到运营体系有多容易？

解决这个问题的一个好方法是通过类似帮助台的设置提供一个自动化任务的菜单，如果可以的话，提供一个配置目录。配置目录针对开发运维周期中的每一项需求，按菜单保存任务。称之为团队向组织请求或交付变更的 it 用户界面。

这不是什么新鲜事。ITIL 到处都在谈论它。它叫做服务台。然而，在 DevOps 文化中，传统的服务目录无法很好地应对持续部署和基础架构即代码的方法。反之亦然。原因是有许多需求往往超出了公共服务台和配置管理自动化领域，因此它们最终会出现在问题跟踪器、服务单中，或者在最糟糕的情况下，出现在普通的电子邮件、聊天和电话请求中。

## 从零到部署

配置服务的目录可以是面向应用程序或项目的，并且应该保持状态，知道过去已经请求和交付了什么，以支持未来的交互。目录提供的每个任务都有一个或多个相关联的规则。这些规则或配方完成了繁重的工作，并自动化了配置、电子邮件、样板文件设置和其他任务，这些任务先于或围绕着大多数核心 DevOps 交付自动化。

可以将它视为经典服务台目录和配置管理工具集的组合。

构建配置管理前端可以极大地减轻和简化应用程序的工作。以下是一些需要考虑的功能和策略:

*   **基线模板**:为团队提供一组基线配置、任务和服务，可以根据项目类型进行配置，如“移动应用”、“Python-Django-Postgres”或“Java-Spring-AngularJS-Oracle DB”这意味着在第一天，开发人员只需选择预先批准的应用程序类型即可开始。按钮式入职应该包括简单的指导方针，保证项目以正确的方式开始，包括将样板源代码提交给存储库和目录验证。
*   **增量服务**:使目录提供增量，只为开发团队提供他们在给定阶段的每个项目在给定时间应该拥有的选项。一个好的配置系统将跟踪每个应用程序在每个环境中的给定点安装了什么，因此将提供渐进的选项。
*   **拓宽您的视野**:自动化*所有可见的*配置任务。仅仅因为你的应用是容器化的或者配置管理是自动化的，并不意味着它从头到尾都是一个按钮。规模合理的应用程序有许多依赖关系、审批和设置步骤，这些在典型的脚本式方法中是没有用武之地的。
*   **手动任务**:将每一个手动流程纳入入职流程，避免使用电子邮件，从而提高工作效率。确保迎合非标准的要求，因为这将有助于保持一切在一个地方。
*   **草案和版本化供应**:允许供应计划与代码一起构建，无论是基础设施即代码还是目录请求。随着新要求的出现，相应地修改条款草案。
*   **适应环境**:对于入职链中的每一个新环境，只需重新应用之前的请求和配置，但要根据特定阶段进行调整。例如，生产前环境模板可能需要扩展 CPU、网络和内存，以接近生产环境。
*   **即时**:确保在代码交付之前*供应发生。如果之前的意思是及时，很好。也许只是在自动化管道中把供应放在部署之前的问题。或者可能是一个需要人工干预的非标准请求，并在短时间内推迟了一个发布。资源调配看起来越像连续部署，就越好。*

下一代配置管理工具必须处理 onboarding 应用程序和服务的许多不同方面，以成为有效的 DevOps 前端。这不仅仅是给开发人员一个“请求云虚拟机”按钮，而是一个完整的“如何、为什么和在哪里”链，帮助团队编写样板应用程序和基础架构代码，正确地通过第一次构建或扩展环境。展望未来，ChatOps 和机器学习正在取代传统的请求工作流，增加了从零到部署管理项目交付所需的洞察力和远见。

DevOps 实践应该在周期的早期开始，并一直提供良好的用户体验。一个好的交付链需要处理新来者的工作流，就像今天的应用程序界面倾向于针对第一次使用的用户。一个友好和有能力的 DevOps 前端是将成熟的组织从其他组织中分离出来的东西，帮助他们优雅地从 hello-world 到 deploy 测试套件。

## 关于作者/罗德里戈·冈萨雷斯

![roddy](img/4e08836d245ed7367939c8f90d3a225f.png)罗德里戈·冈萨雷斯是 [Clarive](http://clarive.com/) 的首席执行官和联合创始人。除了管理日常运营，Rodrigo 还负责公司的整体战略。Rodrigo 来自巴西，拥有德克萨斯理工大学的计算机科学学士学位，在美国、巴西和整个欧洲的科技公司工作了近 20 年，包括朗讯科技和 CA Inc。