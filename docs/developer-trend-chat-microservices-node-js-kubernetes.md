# 开发者趋势聊天:微服务、Node.js、Kubernetes

> 原文：<https://devops.com/developer-trend-chat-microservices-node-js-kubernetes/>

软件开发人员的角色从未如此重要。开发者几乎触及我们生活的每个角落，从医疗保健、零售到教育。这是一个非常有回报的职业——以至于软件开发现在被列为美国最好的工作[](https://www-bizjournals-com.cdn.ampproject.org/c/s/www.bizjournals.com/bizjournals/news/2018/01/10/software-developer-bumps-health-care-for-best-job.amp.html)。

软件开发的本质要求开发人员行动迅速。新的工具和技术为开发人员提供了采用新技能、提高工作效率和重塑工作方式的能力。在这个 Q & A 中， [的 CEO lunch badger](https://www.lunchbadger.com/)Al Tsang 讨论了软件开发的趋势。

问:数据分发仍然是打破单一架构的一个困难而复杂的方面。企业架构师如何避免这种情况，或者当他们最终会遇到这种障碍时，处理这种障碍的好策略是什么？

![](img/643918a0c1887e04b9f6b76a1e3af4de.png)

Al Tsang, CEO, LunchBadger

**Al:** 数据的位置、相关性和不同级别的数据标准化，使得打破整体架构成为一项挑战。微服务计划可以通过构建全面的数据模型来应对这些挑战。过去，我们有 UML 工具，比如 ERD 图。这些工具不再常见，但是，它们所代表的实践仍然为理解您的应用程序当前使用的数据、过时的数据、冗余的数据以及与依赖关系相关的数据带来了价值。

微服务和与数据的关联应该足够原子化，以便它所操作的数据完全被拥有和包含。这说起来容易做起来难。通常可以划分出反映业务功能本身的分界线——无论是按领域、按实体还是按业务流程。在某些情况下，它是上述所有因素的结合。

问:你为什么认为无服务器和 FaaS(功能即服务)发展如此之快，无服务器平台(如 LunchBadger)解决了哪些具体的痛点？

**艾尔:**我认为无服务器和 FaaS 发展迅速有几个主要原因:

(1)基础设施和应用平台变得高度商品化，开发者可以将运营问题推卸给第三方。

(2)创新的压力和需求要求专注于核心知识产权，以此作为差异化优势，而代码中的其他内容都是辅助性的，而且往往完全是样板文件(例如，考虑数据库或 NoSQL 数据源的持久性)。

(3)实现微服务背后的运动和驱动意味着深入到小块的功能，意味着削减您的逻辑，做不同的可重复使用的分割代码块，即功能，而“无服务器”很好地适应了这种范式，补充说您应该只关心基于事件驱动的代码块。

新老公司都积累了大量的技术语言和平台，如果你有一个通用的运行时范例，并且能够编写支持多语言使用的业务功能，那么你的技能和资源可以得到更有效的利用。

**问:根据 2017 年的一项调查，Node.js 主要用作 API 的后端基础设施。Node.js 的主要优势之一是可以在整个堆栈上使用同一种语言。你认为 Express.js 和其他类似的极简框架是如何让它流行起来的，为什么？**

**Al:**node . js 被迅速广泛采用的一个原因是因为它是一个巨大的均衡器。Node.js 开发人员不需要在高可伸缩性、多并发连接、线程或类似的复杂主题方面拥有忍者级别的领域专业知识，就可以构建一个可伸缩的应用程序。

Node.js 利用了一种内置了高可伸缩性原则的语言，即事件异步编程。Node.js 还有一个优势，由于浏览器无处不在，任何 web 开发人员都会接触到这种语言。将同一种语言及其优势转移到服务器上，对于真正成为“全栈”的人们来说是一个巨大的胜利

Express.js 通过在 Node.js 中添加 web 实用程序的基础知识，进一步促进了 Node.js 的成功。每个 web 应用程序都需要一个 web/app 服务器，它将 URL 作为路由公开。所有服务器都有发出请求的消费者，处理这些请求通常会被从一个逻辑链接到另一个逻辑。Express 吸取了 Ruby 和 Sinatra 的经验，并将它们带到了 Node.js。您搭建了一个模板项目，并根据需要和需要的地方填充了空白。它非常高效，因为许多 web 应用程序的起点都遵循相同的模型。

Express Gateway 促进了 Express.js 的成功——其丰富的中间件模块生态系统和许多开发人员的普遍理解，并通过将配置、元数据和条件性分离为声明性和动态的，使其云就绪和云原生。通过这样做，Express Gateway 以分布式方式在容器和编排器中运行，而不用担心在应用程序的任何给定层上耦合。

问:Node.js 和 Kubernetes 是一个受欢迎的组合，但许多开发者和公司对从哪里开始或者它将如何影响他们的技术堆栈感到困惑。你能解释一下你看到的最大的障碍，以及公司如何克服它们吗？

**Al:** 路障#1:应该在哪里扩展 Kubernetes 或者应该在哪里扩展 Node.js 应用？

我认为这一团乱麻实际上并不像人们通常认为的那样糟糕。如果它是应用程序的核心部分，并且你已经用 Node.js 编写了它，那么它应该完全独立于你在哪里以及如何运行它。在广泛采用容器之前，许多 Node.js 应用程序是在流程管理器中运行的。许多仍然在容器中的进程管理器中运行。简而言之，如果它是应用程序逻辑的核心部分，那么它应该在 Node.js 中。如果它涉及到如何以及在哪里运行应用程序逻辑，那么现在您将看到 Kubernetes 中的配置或扩展。

路障 2:我应该使用 Node.js 来编排我的应用程序还是把它留给 Kubernetes，为什么？

编排意味着在基础设施层面上连接你的应用。将这一块留给 Kubernetes，它可以将您的微服务真正作为“服务”来公开和管理。当您编写 Node.js 应用程序时，您不必担心不同 Node.js 进程如何互操作的“I/O”。微服务背后的整个前提是，在进程*必须*互操作而不假设另一个进程可能已经启动并正在运行的情况下，存在明显的界限。

路障#3:如果我有一个既关注基础设施又关注应用程序的组件，该怎么办？

这是一个艰难的时期，许多大大小小的公司都感受到了痛苦。Kubernetes 有一个入口控制器的概念，它实际上只不过是将请求路由和公开给内部指定的资源，以便在 Kubernetes 集群的某个地方处理请求。这就产生了一个问题:你应该在入口控制器上考虑应用程序级的问题吗？

我相信关注点的清晰分离，即使这意味着会有一些运行时开销。如果您的业务需求不需要超低延迟或其他让您模糊基础架构和应用程序之间界限的情况，那么如果有一个清晰的分离，维护起来会容易得多。这实际上与将您的应用程序分割成更小的微服务没有什么不同。它只是在你的堆栈中水平执行，而不是垂直执行。构建一个只关心路由到正确资源的入口控制器。然后构建一个独立的 API 网关，位于微服务的前面，以处理应用程序级别的问题。

— [玛利亚·鲍尔斯](https://devops.com/author/mpowers/)