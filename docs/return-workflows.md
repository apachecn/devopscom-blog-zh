# 工作流的回归

> 原文：<https://devops.com/return-workflows/>

最近，工作流已经成为 AWS、脸书、惠普、LinkedIn、Spotify 和 Pinterest 等公司运营线路的基本组成部分，这些公司刚刚[开放了弹球游戏](https://engineering.pinterest.com/post/113376157699/open-sourcing-pinball)。我们已经见证了对基于工作流的自动化的兴趣激增，在过去一两年中，开源世界出现了一些有趣的实现:OpenStack 生态系统的 [Mistral](//wiki.openstack.org/wiki/Mistral) 和 [TaskFlow](https://wiki.openstack.org/wiki/TaskFlow) ，惠普的 [Score](//www.openscore.io/#/) ，LinkedIn 的 [Azkaban](http://data.linkedin.com/opensource/azkaban) ，Spotify 的 [Luigi](https://github.com/spotify/luigi) ，以及 Docker 生态系统的 CenturyLink 的 [dray.it](http://dray.it/ "http://dray.it/") 等等。

工作流用于协调基础架构和应用程序中的操作，自动化复杂的 CI/CD 流程，协调 map/reduce 作业，并将作业处理到容器中。

当谈到更高级别的自动化和编排时，工作流被广泛使用并不奇怪。引用 Pinterest 博客:“在现实环境中，遇到由数百个节点组成的工作流并不罕见。构建、运行和维护如此复杂的工作流需要专门的工具。Bash 脚本是不行的。”工作流在概念上和实用性上都优于脚本。

从概念上来说，工作流将“配方”从底层细节中分离出来，提供了额外的灵活性和移动性。通过修改工作流“蓝图”来根据您的喜好修改流程，而无需修改硬连线代码，例如为业务流程一致性的关键步骤添加标签更新。或者采用为 Rackspace cloud 构建的自动扩展工作流，并使用它来扩展 AWS 集群。

**实用**，工作流在运营上更胜一筹。

1)工作流是一个执行计划，以任务的有向图表示，易于定义、推理和可视化。

2)工作流引擎充当“消息传递结构”，在不同的应用程序域之间传送结构化数据。

3)工作流执行的状态清晰且易于跟踪:查看哪些步骤正在运行，哪些步骤已完成，以及哪些步骤失败了。

4)可以提供可靠性和崩溃恢复[^(【1】)](#_ftn1)，好的工作流引擎做到了。

5)还有其他方便的装饰。在你的脚本中登录有多好？i18n，有人吗？

什么是好的工作流引擎？答案是“看情况。”这取决于工作流设计要做的工作的细节，以及功能范围的宽或窄。下面，我将重点介绍一些架构选择、特性、功能和属性，我认为它们与在自动化和编排中使用工作流最相关。

### 1.功能

核心工作流功能是按照正确的顺序执行任务，并传递数据。在[工作流行话](http://www.workflowpatterns.com/)中，它们被称为流程控制模式和数据模式。

**1.1 流量控制**

已知工作流有超过 [40 个控制模式](http://www.workflowpatterns.com/patterns/control/)。但是在系统自动化中使用工作流的 15 年表明，实践中很少使用模式。最基本的要素是“有条件的顺序执行，一路传递数据。”通常需要并行执行。但是，一旦你分开并行运行任务，你需要加入他们，有 16 种不同的方式来做到这一点。在实现和可用性方面，处理连接是一个高度复杂的步骤。不同的工作流引擎以不同的方式平衡能力和复杂性。

[Spiff 工作流](https://github.com/knipknap/SpiffWorkflow/wiki)实现所有(！)控制模式。[顾名思义，ActionChain](http://docs.stackstorm.com/actionchain.html) 选择了顺序执行的简单性。 [Dray.it](http://dray.it/) 也是如此——工作流有一个“作业”序列——在这里是 docker 图像执行。 [Pinball](https://github.com/pinterest/pinball) 分裂并行执行，但仅支持“[同步](http://www.workflowpatterns.com/patterns/control/basic/wcp3.php)”连接–并在所有输入分支完成后继续。Pinball 的可插拔的基于令牌的设计是一个强大的抽象，可以添加连接、条件等等。Mistral 试图用简单易用来平衡功能:它支持条件转换、并行执行、各种连接，并处理多实例，处理引擎的输入集合。

[![workflow](img/6283283b0c56f9797c34a5b294b5cdc1.png)](https://devops.com/wp-content/uploads/2015/04/workflow.jpg)

“One example of non-trivial join pattern, Structured partial join. Supported by Spiff and Mistral.”

(请单击链接以 Flash 动画形式查看此图):

[****http://www . workflow patterns . com/patterns/control/new/wcp 30 _ animation . PHP****](//www.workflowpatterns.com/patterns/control/new/wcp30_animation.php,)

***1.2 数据传递***

*数据传递是系统自动化中另一个重要的工作流功能。它是一种使用工作流输入和上游任务输出作为下游任务的输入或条件的能力。将命名变量发布到执行上下文是许多引擎提供的便利特性。*

*通常作为 JSON 传递的结构化数据。Ansible Playbook，StackStorm [ActionChain](http://docs.stackstorm.com/actionchain.html) ，以及其他大多数使用 [Jinja 模板](http://jinja.pocoo.org/)进行数据操作。Jinja 被广泛采用并有据可查；超级用户可以用它做很好的黑客攻击。我们面临的挑战是在 Jinja 模板之外保存类型。毕竟它是模板引擎，而不是查询语言。 [Mistral](https://wiki.openstack.org/wiki/Mistral%20) 用 [YAQL](https://github.com/stackforge/yaql) 解决了这个问题。YAQL 是 JsonPath 的现代扩展，使用简单，功能强大，易于扩展，但目前它缺乏文档(根据 YAQL 作者的说法，这将会改变)。 [Score](//www.openscore.io/#/) 工作流在任务定义中提供了 python 语法:虽然方便，但也带来了安全问题。 [Dray.it](http://dray.it) 通过传递环境变量和将 stdouts 连接到 stdins(可能的文件输出通道)来使作业进行通信，但是在平台端不提供任何数据转换。目前，Pinball 对数据传递的支持还很初级:它使用一个约定来发布一个字符串值，并让 jobs 来决定数据格式。*

### *2.展开性*

*向工作流程中添加新类型的操作需要什么？怎么写？如何部署？怎么升级呢？大多数工作流工具都有一些答案，但很少有人给出一个既适合开发又适合运营的完整答案。 [Pinball](https://github.com/pinterest/pinball) 推出可插拔作业模板，开箱即用提供 Bash、Python、Hadoop 和 Hive 作业。然而，它留给作业来产生预期的输出格式(智能作业、简单平台)。 [Spiff](https://github.com/knipknap/SpiffWorkflow/wiki) 工作流有可插入的任务，但不够动态，因此 Spiff 最常与 Celery 一起使用，利用其可扩展性和远程执行功能。StackStorm 将其完整的动作库作为工作流构建块，并将动作执行输出带入一个公共的“消息结构”更好的是，工作流本身变成了一个动作。操作和运行单个动作和工作流的能力使得开发、调试和操作变得容易。*

### *3.可靠性*

*工作流需要长时间运行。长意味着:1)足够长的时间来预期任何组件的失败，并且执行必须维持它，以及 2)足够长的时间，如果工作流执行由于任何原因失败，我不想从头开始，而是修复一个问题并继续。这使得可靠性成为一项关键要求。*

*[弹球](https://github.com/pinterest/pinball)在可靠性方面得分最高。[它的容错架构](https://github.com/pinterest/pinball/blob/master/ARCHITECTURE.rst)(非常类似于 [Mistral](https://wiki.openstack.org/wiki/Mistral%20) )基于每次状态转换时的原子状态更新，提供横向扩展主和工作器、容错执行、崩溃恢复和“无停机升级”Ansible 采取了一种不同的方法:剧本执行没有弹性，但是任务被假定为幂等的，当它们是幂等的时，重新运行整个剧本是安全的。Dray 选择了简单，而[似乎还没有容错](https://github.com/CenturyLinkLabs/dray/blob/master/job/manager.go#L50)。*

*Luigi workflow 带来了一个有趣的架构，在这个架构中，分布在各地的工作人员可以选择类似的工作流和任务，本质上将工作流处理视为另一项工作。它实现了很好的横向扩展，但目前缺乏容错能力:整个工作流的执行是在它开始的地方由一个工人运行的[。](https://luigi.readthedocs.org/en/latest/execution_model.html)*

### *4.工作流定义*

*用于声明工作流的人类可读的、机器可编写脚本的语言不仅仅是方便。这是在实时系统上动态创建、上传和更新工作流以及将“基础设施视为代码”的必要条件坚实的 DSL 是在其上构建 UI 的良好基础(而不是相反！).基于 XML 的工作流语言已经成为过去；YAML 是事实上的新标准。*

*StackStorm 的 [ActionChain](http://docs.stackstorm.com/actionchain.html) 和 [Ansible](https://github.com/ansible/ansible) 剧本提供了有趣的 YAML 工作流定义。它以牺牲高级功能为代价，反映了底层引擎的简单性。*

*[Spiff](https://github.com/knipknap/SpiffWorkflow/wiki) workflow 提供 XML、JSON 和纯 python 可编程定义。 [Dray](http://dray.it) 使用 JSON。[弹球](https://github.com/pinterest/pinball)没有开箱即用的 DSL。它为以编程方式构建工作流提供了 python 接口；添加 JSON 或 YAML 工作流定义就是编写一个解析器的事情。根据 Pinball team 的说法，这是一个“有意识的选择，不将配置语法作为系统核心的一部分，以便给开发人员很大的灵活性，以最有意义的方式定义工作流配置。”*

*但是老实说，两个 DSL 用于同一个工作流没有多大意义。查看[分数](//www.openscore.io/#/):它已经将这种可插拔的方法进行到底，通过可插拔编译器将“语言”从工作流中分离出来，其想法是支持同一工作流的多种语言。然而，功能是在工作流中定义的，所以如果不入侵工作流处理程序，就不可能引入有意义的新构造——比如用神牙替换 YAQL，添加“*鉴别器*模式，或者引入*超时*关键字。除了表面的语义糖，语法和功能不能真正分开。*

*Mistral 和 TaskFlow 采取了不同的策略，支持可插拔的工作流处理程序。 [Mistral](https://wiki.openstack.org/wiki/Mistral%20) 带有两个处理程序，代表两种类型的工作流，具有不同的功能。直接工作流明确定义了成功/失败时的任务流。“反向”工作流使用“requires”关键字定义上游任务的任务相关性，并运行所有相关任务来满足目标任务，如 make 或 ant。基本工作流 DSL 用特定于处理程序的关键字进行了扩展。*

### *5.漂亮的 GUI*

*一个好的图形表示使得理解工作流的结构和跟踪工作流的执行变得更加容易。以图形方式构建工作流不仅让用户兴奋，还能帮助用户了解系统并极大地加速工作流创作(你可以在这里体验一下)。一个问题:正如[弹球作者正确地说的](https://engineering.pinterest.com/post/74429563460/pinball-building-workflow-management)，“现实的工作流程是数百个步骤。”你猜怎么着，现有的 UI 表示并不能很好地适应 100 步的工作流。不只是新电影:我们在过去 20 年里看到的任何电影[^(【2】)](#_ftn2)——都很烂。我相信这个 UX 问题还没有解决。*

*Pinball 没有让优秀成为优秀的敌人:它提供了工作流的可视化表示，甚至提供了从 UI 构建工作流的能力。 [Luigi](https://github.com/spotify/luigi) 是另一个让基于 d3 的简单地图“足够好”来显示任务的软件。*

*[Score](http://www.openscore.io/#/docs) 和 [Mistral](https://wiki.openstack.org/wiki/Mistral%20) 采取了一种替代方法，使创作工作流程更快、更无 bug，为语法检查提供了 [Sublime 插件](https://github.com/giampierod/mistral-sublime)。StackStorm 的 WebUI(如下)为 [ActionChain](http://docs.stackstorm.com/actionchain.html) 和 [Mistral](https://wiki.openstack.org/wiki/Mistral%20) 工作流带来了高效的工作流执行表示。在即将发布的版本中，我们将勇敢地面对表示工作流执行计划和可视化工作流构建的挑战。*

*[![stackui](img/eca00d941006550b2a684159c13f5b4d.png)](https://devops.com/wp-content/uploads/2015/04/stackui.jpg)

StackStorm presentation of workflow execution in WebUI* 

## *结论*

*StackStorm 喜欢工作流:它们对于更高级别的自动化是必不可少的。可定制的 CI/CD、自动扩展、自动故障修复、自动安全响应—这些都是工作流。不同的工作流程针对不同的工作进行了不同的优化，也有不同的品味。所以我们把工作流引擎做成一个可插拔的组件。目前，我们提供 [ActionChain](http://docs.stackstorm.com/actionchain.html) 来实现速度和简单性，提供 [Mistral](https://wiki.openstack.org/wiki/Mistral%20) 来实现复杂的工作流逻辑和可扩展的可靠执行。*

*我们喜欢 [Pinball](https://github.com/pinterest/pinball) :它建立在简单而强大的基本任务模型和作业令牌的抽象之上，具有可靠且可扩展的架构，并为工作流和作业定义提供了良好的编程接口。随着 StackStorm 的成熟和发展，我们肯定会考虑支持它。*

*…*

**此表总结了文章中讨论的功能领域，但没有对每个工作流为优化目标用途而做出的实际选择做出判断。**

|  | 高级流量控制 | 数据传递和转换 | 容错执行 | YAML/JSON DSL | 可插入操作 | 视觉表现 |
| [弹球](https://github.com/pinterest/pinball) |  |  | + |  | + | + |
| [Spiff](https://github.com/knipknap/SpiffWorkflow/wiki) | + |  |  | + |  |  |
| 路易吉 |  |  |  |  | + | + |
| [可回答的](https://github.com/ansible/ansible) |  | + |  | + | + |  |
| [Dray](http://dray.it) |  |  |  | + |  |  |
| [分数](http://www.openscore.io/#/docs) | + | + | + | + | + |  |
| [动作链](http://docs.stackstorm.com/actionchain.html) |  | + |  | + | + |  |
| [西北风](https://wiki.openstack.org/wiki/Mistral) | + | + | + | + | + |  |

### *脚注和参考文献*

**[^(【1】)](#_ftnref1)工作流执行模型和状态比符合图灵的语言的模型和状态要简单得多，也小得多，这使得在每一步大规模地保持和恢复变得切实可行。**

**[^(【2】)](#_ftnref2)M＄System Center Orchestrator(原 Opalis)、HP Operations Orchestration(原 iConclude)、BMC Atrium Orchestrator(原 Realops)、CA ITPAM(现已死亡)、VMware vCenter Orchestrator(原 Dunes)、NetIQ Aegis、MaestroDev、Cisco CPO(原 Tidal)、Cisco UCS Director(原 clou pia Unified infra structure Controller)、Citrix Workflow Studio–看看它们，看看它们如何处理 100 步工作流，然后再作出判断。**

*为了方便读者，下面是文章中提到的产品和工具的详细参考。*

*   *Pinterest 上的弹球游戏

    *   架构[https://github . com/Pinterest/pinball/blob/master/architecture . rst](https://github.com/pinterest/pinball/blob/master/ARCHITECTURE.rst)
    *   介绍博客[http://engineering . Pinterest . com/post/74429563460/pinball-building-workflow-management](https://engineering.pinterest.com/post/74429563460/pinball-building-workflow-management)
    *   opensoucing Pinball 博客[http://engineering . Pinterest . com/post/113376157699/open-sourcing-Pinball](https://engineering.pinterest.com/post/113376157699/open-sourcing-pinball)
    *   来源 https://github.com/pinterest/pinball* 
*   *斯皮夫工作流程[https://github.com/knipknap/SpiffWorkflow/wiki](https://github.com/knipknap/SpiffWorkflow/wiki)*
*   *惠普得分:

    *   主页[http://www.openscore.io/#/](http://www.openscore.io/#/)
    *   文件http://www.openscore.io/#/docs* 
*   *德雷，由世纪链接[http://dray.it/](http://dray.it/)*
*   *Luigi，Spotify—[https://github.com/spotify/luigi](https://github.com/spotify/luigi)*
*   *https://github.com/ansible/ansible*
*   *任务流[https://wiki.openstack.org/wiki/TaskFlow](https://wiki.openstack.org/wiki/TaskFlow)*
*   *来自阿帕奇的奥齐[http://oozie.apache.org/](https://oozie.apache.org/)*
*   *领英的阿兹卡班[http://data.linkedin.com/opensource/azkaban](http://data.linkedin.com/opensource/azkaban)*
*   *动作链，由 stack storm:[http://docs.stackstorm.com/actionchain.html](http://docs.stackstorm.com/actionchain.html)*
*   *Mistral，来自 OpenStack 社区[https://wiki.openstack.org/wiki/Mistral](https://wiki.openstack.org/wiki/Mistral)(集成到 [StackStorm](http://stackstorm.com/product/) )*

****关于作者/德米特里·齐明****

***[![Dmitri headshot](img/15c531e367104f3ff8c068db6c5312d7.png) ](https://devops.com/wp-content/uploads/2015/04/Dmitri-headshot-e1428544770309.jpg) Dmitri Zimine，** CTO，StackStorm 是 StackStorm 的“首席风暴师”和联合创始人。Dmitri 在担任 Opalis 首席架构师和工程主管期间，帮助引领了第一波运营自动化浪潮。Opalis 在 2009 年被微软收购之前发明了“run book automation”，现在是 System Center Orchestrator。最近，Dmitri 在 VMware 工作，领导 vSphere Client 团队完成了四个主要版本，并参与了各种相关项目。在这个职位上，Dmitri 还领导了 vSphere Client 向新技术体系的成功过渡。Dmitri 拥有俄罗斯托木斯克州立大学的数学和物理学博士学位。*