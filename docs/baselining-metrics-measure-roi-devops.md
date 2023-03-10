# 衡量开发运维投资回报率的基准指标

> 原文：<https://devops.com/baselining-metrics-measure-roi-devops/>

评估开发运维的投资回报率通常是根据公司的基线成本进行的。问题是，大多数组织不收集或评估“自动化和交付”创新的成本；他们通常更关注创新产品本身。例如，如果一家公司创建了一个托管在 web 上的应用程序，为其客户提供购买库存的能力，该公司通常很想知道该应用程序的性能如何:有多少人在使用它？它因 bug 而失败的频率有多高？销售了多少？该公司通常专注于最终产品——应用程序，因为它接触到客户和潜在客户。在将应用程序加载到生产环境之前的交付过程通常不是严格审查的主题。至少，在采用 DevOps 方法和工具之前，大多数组织没有评估交付的速度和交付的过程有效性。

这种审查的缺乏导致了比较基准的缺乏。比方说，一个典型的程序员(在 DevOps 之前)混合使用脚本、人工智能和人工验证来创建和验证一个构建。在 DevOps 之前，目标仅仅是创建构建，并让它出来查看，并决定下一步做什么。大多数程序员并不关心整个过程的效率；对他们来说，这是达到目的的手段。因此，大多数程序员不会记录从头到尾创建一个版本所花费的平均时间。部署过程更是如此。一旦创建了一个构建(还是在 DevOps 之前)，将它部署到目标环境中可能会涉及几个不同的团队(取决于目标测试环境的类别)。这个过程可能包括向其他支持团队发送电子邮件请求，或者填写一张票来完成它。同样，大多数组织很少花时间从头到尾跟踪这个过程；它只是达到目的的一种手段。

事实上，如果一个组织正在密切关注创建一个构建需要多长时间，完成一个部署需要多长时间，那么这个组织将会全速向 DevOps 跑去，以看到否则无法实现的改进。正是那些我们无法衡量的东西很少受到关注——直到它们被打破。一旦我们的部署过程变得如此繁重或复杂，或背负着如此沉重的审批负担，以至于几乎没有东西可以部署，那么我们就开始审视它。这创造了一种“吱吱作响的轮子综合症”的文化，这使得我们的开发和运营团队只关注反应性的问题，而前瞻性的关注却被搁置一旁。当你不断地与其他严重损坏的东西战斗时，就没有时间去发明主动的改进了。如果 DevOps 要在您的组织中取得广泛的成功，这种文化也必须改变，所以请注意它对您今天的工作方式的影响。

## **准备收藏** 

鉴于大多数公司在这一领域缺乏真正的比较基准，要意识到收集一个基准本身就需要投资。这种基线指标收集成本通常会添加到开发运维的投资成本中。这有点不公平，因为你实际上是在说，在我们投资购买可以清洁我们的肥皂之前，肥皂公司还必须承担确定我们有多脏的成本。肥皂制造商倾向于认为你已经意识到自己有多脏，否则你一开始就不会考虑买肥皂。但是如果没有对问题程度的准确评估(在这种情况下，就是你今天花费的时间投资)，你将永远不会知道对 DevOps 所做的改进的投资回报(之后的图片)。

此外，请记住，手工测量任何东西都是困难的。这听起来像是显而易见的队长说的话，但是考虑到人工工作需要额外的人工工作来捕获它们并在某种系统中记录它们。举例来说，如果我的典型程序员在每次构建时花 15 分钟对构建进行人工验证，那么这段时间就没有得到反映。小时工通常记录他们每天工作多少小时，而不是他们一天中完成了什么任务。即使那些更谨慎地记录工作时间的员工也倾向于只记录他们花了“x”小时做“开发”，而不是在标题“开发”中发生的一般任务类别。因此，没有可以自动收集的电子记录来反映对应用程序的一般版本进行人工验证所花费的 15 分钟时间。了解这一点的唯一方法是个人面试，然后有人将数据输入某种收集系统。

知道您寻求的基线信息将来自人类交互和一些自动化日志，使用一个工具开始收集，该工具允许这些工作的最大灵活性。电子表格浮现在脑海中。当收集基线的工作开始时，您将对希望收集的数据种类以及它在您的组织中可能存在的方式有所了解。但不可能确切知道由此产生的努力将如何完成。简而言之，你不知道你不知道的。当您收集指标时，您总是会遇到一些人，他们透露了您不“计划”收集的关键指标相关信息。但是一旦发现了，你将需要结合“新”的信息来真正提供一个准确的基线评估。

## **确定基线**

下一步是开始收集过程本身。要检查的关键数据通常可以通过查看自动化和创新交付的给定核心“流程”中涉及的“人”时间来收集，然后再查看涉及的“机器”时间。例如，程序员在启动一个构建之前必须花费的时间(不是编码时间)——所有准备工作加倍检查系统是否准备好启动构建脚本(或者准备好手动按下按钮)——将被认为是“人”的时间。创建构建的脚本的执行被认为是“机器”时间。然后，在构建完成后，所有的工作都被创建来验证它，并确保事情如程序员所期望的那样，再次被放入“人”的时间类别中。DevOps 将系统地自动化“人”当前投资的前期和后期活动，因此所有这些时间都将计入 ROI。

当一个人从头到尾完全控制一个过程时，上面的例子很好。当其他团队必须参与进来完成一项任务时，“人”的时间就开始暴涨。例如，如果一个程序员或者发布经理，必须得到一个请求电子邮件(或者票证系统等价物)来将一个特定的构建部署到一个特定的目标环境中，那么该票证的整个生命周期就变成了您需要跟踪的“人”的时间的一部分，作为您的基线度量。即使商店为周转创建了两天的服务水平协议(SLA ),它仍然代表部署生命周期中的两天延迟(由于“流程”时间)。“人类”实际花费在阅读请求、批准请求和路由请求上的时间都是 DevOps 将自动化和消除的时间。最后，当正确的支持团队(通常是 Ops)按下他们自己的脚本按钮来执行部署时，该流程的这一部分再次成为“机器”时间。可以想象，给定部署的端到端时间在 DevOps 之前的方法中可能需要几天，而在 DevOps 之后的方法中只需要几分钟。自助服务部署可以进一步缩短这一时间，消除交接，降低风险，随心所欲地进行创新。

对该度量数据的进一步分类也是有用的。例如，您可能希望将“机器”时间分成相关的子类别，如构建脚本执行、部署脚本执行、测试脚本执行和发布脚本执行。您可能还想将“人”的时间进一步细分为预构建/部署验证、后构建/部署验证和测试脚本结果评估。最后，您可能希望将“处理”时间进一步细分为请求生成、请求发送、请求批准、请求拒绝和请求通知。DevOps 将能够让您谨慎地了解您在这些子类别中节省的时间，尽管由于基线通常是一次性的工作，您可能不想追求这种级别的细节。这种子类化变得有用的地方就在后面——例如，当您试图确定一组测试是否比另一组运行得更快，或者一个云提供商是否比另一个运行得更快。

## **评估基线**

通过这个练习，一个隐藏的或次要的好处出现了。您的组织开始更好地理解它在当前创新过程的交付中投资了什么。一般来说，直接关注的领域会出现，并为开发运维服务交付提供路线图，首先解决哪些领域的问题，从而为公司带来最大的经济效益。如果没有这样的基线工作，您的 DevOps 服务交付计划将基于轶事般的想法或可能没有现场数据支持的行政命令。有了基线，就可以提供一个基于具体证据的交付路线图，说明在进行改进时什么对业务最重要。没有人可以对这些数字提出异议(假设它们是精心收集的)。路线图可能会揭示您组织产品组合中的哪些应用程序应该首先作为开发运维的目标。

此外，您的组织现在更好地理解了在此流程中它认为相关的“什么”数据，即使在实施 DevOps 之后也要继续收集。由于 DevOps 主要是一套自动化的工具和方法，DevOps 应该能够持续地交付这些指标。这允许持续的度量工作自动化，而不需要更多的人力，并且可以提供 DevOps 对组织的价值的持续证明，因为随着时间的推移，数字会继续提高。由于随着开发运维的到位，大部分手动任务都消失了，因此没有理由在前进的过程中必须手动收集指标数据。

最后，由 DevOps 部署一个自动化的度量收集系统，应该会导致思维的下一次进化:模拟。在 DevOps 服务的初始 ROI 获得应有的赞誉之后，自动化指标收集系统应该提供一些预测分析所需的所有原始数据。调整变量或流程点或“机器”效率应该会提高交付速度，这可以根据您系统收集的数据进行衡量(甚至在实现之前)。了解这些变化的影响比它的黄金重量更有价值，因为你可以在它们出现在路线图之前就剔除模拟建议反对的计划中的变化，更不用说在你的世界中发生了。

## **对底线的影响**

已经有足够的轶事证据吸引公司接受 DevOps 之旅。然而，随着您的战略开始着眼于从应用程序代码级别到中间件、数据库和操作系统的深入，可以根据基线对每一层进行评估，以确定您的路线图是否合理，更重要的是，是否按照正确的顺序获得最佳 ROI。这同样适用于您希望通过额外的服务横向扩展您的开发运维之旅，例如自动化测试和评估、门控进度、自动化配置、版本编排、配置管理数据库(CMDB)集成、按需生产配置和监控集成。每项新服务都可以根据基线进行评估，以确定其投资回报率是否仍然符合您的财务部门的要求，以及您的路线图是否符合实现最大性价比的正确顺序。

通过执行基线的微妙胜利是它通过你的整个组织分发的文化改变。基线度量告诉您的开发团队和运营团队(以及关注的业务单元),您打算度量性能并系统地改进它。仅仅因为一些事情以前没有被检查并不意味着它将继续如此，森林火灾不一定是这样做的动机。DevOps 是对您的自动化交付的主动改进。收集您的投资回报基线，开始播种主动改进对您的执行团队很重要的想法。这是对陈词滥调的行动展示。它开始消除你的员工的森林火灾反应，并创造一个新的前瞻性思维观点。这种文化变革对你的公司来说，比任何一种特定工具或方法的实施都更有价值，它可以追溯到改变你对在个人工作中交付创新的想法。这是 DevOps 最擅长的。

要继续对话，请随时[联系我](/cdn-cgi/l/email-protection#f4bf869d87809d959adaba9198879b9ab49c9b8099959d98da979b99) …