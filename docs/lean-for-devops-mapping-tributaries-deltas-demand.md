# 精益开发:绘制需求的支流和三角洲

> 原文：<https://devops.com/lean-for-devops-mapping-tributaries-deltas-demand/>

在 IBM 的精益实践中，我们使用一个名为“密西西比”的图表来分析需求。之所以这么说，并不是因为它起源于密西西比州——事实上，据我所知，这种工具是在我们英国的实践中开发和命名的*。相反，它被称为密西西比河，因为就像那条大河一样，需求来自许多不同的来源(或支流)，并可以通过许多不同的点(三角洲)留下一个过程。显然，有时密西西比三角洲会反映潮汐模式和逆流。同样，需求可以返回到流程中或流程上游——例如，以返工的形式。

出于多种原因，我们希望分析需求的数量和频率。了解需求有助于我们:

*   识别“跑步者”(日常请求)、“重复者”(不太频繁，但并非不寻常的请求)和“稀有者”(不频繁的请求)。这可能是根据用户组、应用程序或请求类型(例如，小的变更与大的项目)。当我们设计我们改进的未来状态时，我们将为跑步者和重复者设计它。有时候，异常的影响可能会非常痛苦，团队会忽略它们有多罕见，并设计一个流程来防止或管理这些罕见的情况——这对所有跑步者和重复者来说都是低效的。
*   识别失败需求-在哪里有额外的请求重新进入流程，作为返工？哪里有“无处可去”的流程活动？
*   说明流程内外的渠道，以便我们可以识别潜在的控制点，或者说明过滤器的缺乏，并查看需求可能通过意外渠道传递到哪里。
*   告诉我们不知道的:哪些需求元素是我们不知道的？我们需要理解所有的需求，以便我们能够构建和资源化(负载水平)一个能够满足该需求的过程。有时候发现我们不知道的事情本身就是一个教训。

这些优势对于精益开发和其他领域同样重要。

很难说你会从进行这种分析中学到什么，直到你做了它，因为每个密西西比都是不同的。但是为了展示我从起草《密西西比河》中学到的一些有价值的经验，这里有一些现实生活中的例子:

[![Lightbulb moment: 'Churn is a fact of life - we need a better way to handle it'](img/76f8ea69119a41c57509d23549e66e18.png)](https://devops.com/wp-content/uploads/2015/07/Mississippi-2-DevDemand.jpg)

Lightbulb moment: ‘Churn is a fact of life – we need a better way to handle it’

[![Lightbulb moment: 'We need to start saying no to enhancement requests'](img/0de37e5799badfce583f2c95ecdee837.png)](https://devops.com/wp-content/uploads/2015/07/Mississippi-1-Maintenance.jpg)

Lightbulb moment: ‘We need to start saying no to enhancement requests’

[![Lightbulb moment: 'We have way too many changes taking the emergency route: a faster 'normal' route will reduce that demand and the associated risk.'](img/3727b34205b5f5accaabef78d23ecb23.png)](https://devops.com/wp-content/uploads/2015/07/Mississippi-3-Change-Reqs.jpg)

Lightbulb moment: ‘We have way too many changes taking the emergency route: a faster ‘normal’ route will reduce that demand and the associated risk.’

以不同的方式，这些都有助于缩短 SDLC，更紧密地将开发与业务需求结合起来，以及更灵活的部署过程。

*如果您已经在 IBM 项目之外看到了它的使用，我很想听听它的情况！在推特上找到我来澄清事实。