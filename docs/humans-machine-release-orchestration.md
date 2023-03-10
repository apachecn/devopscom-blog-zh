# 发布协调机器中的人类

> 原文：<https://devops.com/humans-machine-release-orchestration/>

让我们面对现实:大多数组织仍然在努力实现全门控自动化的涅槃。首先，我们自动化开发运维服务的核心，即构建和部署规程。随着时间的推移，我们认识到，模板化或框架化(或者用你的类似术语)的自动化方法考虑到了规模和可预测性，降低了成本。正是在这里，最大份额的可变性得以减少，可伸缩性得以实现。

下一个引起注意的罪魁祸首通常是测试自动化，但是这往往是自动化过程的工作水平遇到困难的地方。所以一般来说，完成的工作是最少的，根据 80:20 法则，80%是可以快速完成的，应该足够了，剩下的 20%就太难了。但是在 DevOps 成熟度等级中深入了解之后，发布流程编排(RO)通常是我们连续服务中的下一个。

发布编排的自动化与构建、部署甚至测试自动化的核心是不同的动物。发布协调更多的是关于自动化我们的变更管理过程。过去的电子表格或 SharePoints 总是要让位于我们首选的供应商的方法，即在他们的专有工具集中重新发明发布轮(尽管预期会有更好的结果)。但是通常这也是错误的方法。

## **改变人类对屋顶建设的思维**

正如我不断重复的，DevOps 是关于“我们如何创新”的不同思考(如果你需要更多这方面的战略领导帮助，请告诉我，我正在寻找。)考虑到我们的电子表格和 SharePoint 虽然令人印象深刻，但却限制了我们在电子表格和 SharePoint 工具的架构构造或限制内思考发布和变更管理。它们是面向任务的，较少交互的，自顶向下的列表，列出了我们认为在任何给定的版本中需要做的事情。如果我们真的回到绘图板，考虑创建一个没有那些约束的发布，或者仅仅是并行跟踪的想法，我们会完成什么？

用一种精益的心态来消化发布过程，将大的部分分解成更易管理的子部分。这降低了风险，提高了速度，特别是在与并行执行相结合的情况下。如果我们的任务中真的存在顺序依赖，让我们把它说出来，但是当我们这样做的时候，我们必须问自己，这种依赖是对所有活动都适用还是只对其中的一些活动适用。如果是前者，那就这样吧；如果是后者，那么也许我们可以调整我们的部分来解决这个问题，并并行运行更多的部分。仅仅实现一个并行的思维模式就可以从根本上减少从头到尾运行一个版本所花费的时间。但是我们也必须问自己，任何首选的版本编排工具集的其他关键特性会改变我们的思维方式吗？

## **改变人类对 RO 执行的思维**

另一个轴是实时交互性。考虑一下，有些任务不能或者永远不会完全自动化。有些任务将由人类来完成。例如，(我想不出为什么，但请原谅我)，如果我们需要在发布期间在裸机服务器上安装额外的硬盘，物理安装总是需要人工来完成。使用旧版本的编排技术，我们必须等待共享的电子表格文件被工程师更新，当他/她完成这个任务时(或者你能想到的任何其他手动任务的例子)。

借助新的移动版本编排技术，工程师可以站在数据中心的硬盘/服务器前，在他/她的移动设备上实时标记完成(或完成百分比)。这节省了多少时间，仅仅是走到他的终端，登录并更新一个文件，通过电子邮件发送给变更经理，将其与当前文件合并，等等..简单一扫就搞定了。工程师现在能够以最少的工作量向团队实时提供更多的信息。这为发布经理提供了前所未有的实时可见性。

它还可以让他们有一定程度的直接互动。假设硬盘的物理安装已经完成，但是手动测试失败了。如果工程师没有好的方法与团队共享信息，就无法正确评估整体按时完工的风险。适当的工具可以避免变更和发布经理等待一个任务，而下钻活动不可用的情况(描绘一个旋转的图标，而不是特定任务项的完成百分比)。添加红-黄-绿维度来跟踪任务的完成情况，无论是否并行，并且我们有一个指示板来实时提醒我们注意影响发布的问题。这在较老的 RO 技术中是不太可能的，直到有人检查了他们的手表并开始打电话。

## **改变人类对 RO 估值的思维**

现在，每个组织都梦想有一个版本，其中只包含针对每个应用程序(甚至是传统应用程序)的虚拟化全栈部署，在部署过程中，自下而上的一切都是自动化的。然而，我们中的一些人生活在现实世界中，仍然有一些数据库脚本必须在生产部署期间手动运行(不要问我为什么)。或者在你所面对的现实世界中选择你的毒药，通常基础设施和平台任务是最后被完全自动化的。

因此，在发布期间，工程师需要随时待命。然而，如果我们现在都订阅了一个工具解决方案，作为我们的发布流程编排的一个公共主干……工程师们确切地知道什么时候做某事，他们是否可以早做，以及之后什么时候他们可以回家。对于工程师来说，这是一个有价值的提议，他们可以在周末花更少的时间做单调乏味的工作，否则他们宁愿呆在家里。

对发布经理的价值主张是实时洞察发布期间的所有活动。自动化任务正如您所期望的那样顺利完成，并具有最新的进度状态，直到完成为止。剩余的手动任务提供同样实时的“原样”状态更新，并作为未来版本之前自动化的下一个机会目标。

## **改变人类对 RO 视角的思考**

我在版本编排市场上评论过的许多供应商的产品中似乎总是缺少一样东西，那就是以人为中心的观点。大多数发布流程编排工具痴迷于任务管理，将它与日历调度集成在一起，并将其设计为最大效率地完成下一步。然而，如果我们的供应商社区能够更多地接受智能日历的想法(未来的文章将更详细地讨论这一特性)，这些产品可以形成一个更加以人为中心的版本编排过程的视图。

想象一下，如果工程师或变更经理登录到发布协调工具集，并拥有一个个性化的仪表板，概述需要批准、处理或完成的任务，以支持该用户的所有待定发布(基于集成的工作流和智能调度)，会是什么样子。一个自动化的红-黄-绿注意力吸引，对于可能落后的、按计划的或提前完成的工作，将极大地改善发布协调的人类体验。从经理或以员工为中心的观点来看，以部门或团队为中心的综合观点会增加对工作表现的批评——证明一段时间内表现的优劣。

这仅仅代表了一个简单的认识，即人类不应该停留在发布流程编排工具的机器中，从属于以机器为中心的待完成操作的视图。相反，供应商可以重新校准一个更人性化的视角——一个细微的视角变化会使这个版本编排工具集的价值呈指数级提升，在我看来，任何供应商都可以成为第一个……如果他们愿意的话。

要继续对话，请随时[联系我](/cdn-cgi/l/email-protection#c2a9b0abb1b6aba3acecaca7aeb1adac82aaadb6afa3abaeeca1adaf) …