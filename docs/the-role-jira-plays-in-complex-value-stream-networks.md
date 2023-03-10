# JIRA 在复杂价值流网络中扮演的角色

> 原文：<https://devops.com/the-role-jira-plays-in-complex-value-stream-networks/>

没有人否认 JIRA 已经接管了开发者的空间。结论几乎是一致的:大多数开发者只想使用 JIRA。这很好，但是如果不了解它在您的整个价值流网络中所扮演的角色，您的组织很可能没有精心制作最有效的价值流。

JIRA 在任何复杂的价值流中都扮演着关键角色，充分利用 JIRA 以及价值流的其他关键方面是更快交付软件并实现您所寻求的软件结果的关键。

但是开发人员只包括构建复杂软件所需的一个角色。此外，尽管 JIRA 对开发人员来说很棒，但它通常不是构建软件中许多其他角色的首选工具，例如产品经理、产品分析师和测试工程师。甚至销售人员也是你价值流的一部分。

从根本上来说，我们需要认识并理解交付软件需要一个庞大的网络，这个网络由具有不同角色的人组成，他们需要不同的工具。但是我们需要在该网络中传递的信息的总体价值流无缝地协同工作。流经网络的信息需要以自动化的方式进行连接和追踪。这实际上可以归结为识别具有相关工件的“关键中心”,并相应地构建您的价值流网络。

# JIRA，临界中心和价值流

什么是软件交付价值流中的“关键中心”?它们是工件和相关的工具，代表了业务价值到业务价值表现的主要连接器。更具体地说，当业务要求一些新功能时，它被表示为一个或多个工件，通常是需求、特性或史诗(有时三者都有)。这些工件充当所有其他关键信息的“粘合剂”您想要运行的测试、变更集和代码审查、缺陷、构建……所有这些信息都应该与需求/特性/史诗联系在一起。并且那些“粘合”工件也需要与最初的业务计划或项目联系起来。因此，对这些类型的工件进行操作的工具实际上是您的“临界中心”

这就是 JIRA 发挥重要作用的地方。它充当了开发人员应该构建什么之间的接触点——关键点的中心，与构成最终工作软件的实际工件相关联，也与最初的业务需求相关联。

考虑一个熟悉的例子，当销售人员从客户那里听到他们真的想要一个新功能。因此，她希望将这一全新的请求与机会联系起来，并能够通过 Salesforce 跟踪客户是否会很快收到新功能请求。

这里有一个很好的价值流:请求被输入到 Salesforce，并自然地绑定到客户帐户。该请求应该流向正在使用的产品管理工具，在某些情况下可能是 JIRA，但是通常，特别是在大的组织中，是一个更专门构建的产品管理、项目组合管理或者需求管理工具。此时，来自 Salesforce 的请求被审查并确定为三种不同的功能。一旦公司决定要建造它们，这些特征就会像史诗一样流入 JIRA。从 JIRA 的 epic 开始，开发团队开始创建构建特性所必需的故事和任务，然后将变更集、测试和缺陷与这些故事和任务联系起来。

结果，在没有任何人工努力的情况下，团队创建了一个动态的工件网络，提供了从客户开始请求到最终无缝交付的完全可追溯性。JIRA 扮演着关键的接触点角色，即最终软件的实际位和字节应该构建“什么”。

现在考虑一个不同的例子。您已经发布了应用程序的下一个版本，一切进展顺利。支持人员使用 ServiceNow 或现有的众多 IT 服务管理(ITSM)工具之一。您的支持团队是应用程序后续工作的发起人。标签源于 ITSM 工具——但是它们也需要与需要关注的最终缺陷联系起来。因此，您需要从 ITSM 工具到必须驻留在 JIRA 的最终缺陷的票据和事件的无缝流程。这些缺陷需要与受影响的故事和史诗联系起来。他们也居住在 JIRA。

这两个例子都说明了“临界中心”的重要性，JIRA 就是其中一个临界中心。在一个复杂的价值流网络中，JIRA 扮演着重要的角色，是比特、字节和商业价值的连接点。但是，如果没有来自价值流中其他工具的流入和流出 JIRA 的信息，你会留下一个破碎的价值流，而没有真实、准确、自动化的知识来了解你在建造什么和为什么建造什么。因为知道你是否已经交付了商业价值来自于理解你正在构建的东西的出处。可能是有多少客户(内部或外部)要求上一个版本提供的 20 个特性。或者，如果没有这些功能，有多少客户不会续订您的软件。或者甚至有多少新的机会你可以跟进，告诉他们他们所要求的现在在你的产品中。

## 结论

构建真正满足业务需求的复杂软件需要有一个同样复杂的底层价值流网络，只有在仔细考虑需要连接的关键工件和工具的情况下，该网络才是高效和有效的。JIRA 显然是这些工具之一。因此，拥抱 JIRA 成为开发商的心跳——并且知道，通过将 JIRA 作为“关键中心”之一来精心打造您的端到端价值流网络，您可以拥有一个高效、完全连接和完全可追溯的价值流。祝连接愉快！

妮可·布莱恩