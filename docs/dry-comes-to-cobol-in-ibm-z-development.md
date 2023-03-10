# IBM Z 开发中的 DRY 来到 COBOL

> 原文：<https://devops.com/dry-comes-to-cobol-in-ibm-z-development/>

不要重复你自己(干)是现代计算机编程的一个基本原则。几乎每个计算机科学的学生都被告知，在应用程序中复制代码是迟早会发生的事故。危险在于，您可能在一个地方修改了一段代码，但却没有修改该代码的另一个相同实例。然后当你运行代码时，各种奇怪的事情发生了。在某些情况下，改变的行为是有效的。在其他情况下，它不是。维护变成了一场噩梦。

这年头坚持原则干并不是那么难。面向对象的语言，如 Java、C#和 Objective-C，可以很容易地将一组函数封装到一个类中，该类可以在整个应用程序中重用。此外，RPC、XML-RPC 和 gRPC 等技术使得以可共享的方式向网络公开不同的功能成为可能。当一段代码可以在运行时轻松共享时，编写冗余代码的风险就会降低。当你可以使用一个已经存在的众所周知的方法时，为什么要重新发明轮子呢？

![](img/94697c31d60dc6b8c50db77ceb478c26.png)然而，情况并不总是如此。在编程的早期，代码行是按顺序执行的。你从第 1 行开始，到第 200 行结束。中间没有旁站。

语言设计者意识到了这一缺点，并让程序可以跳过代码行。你可以从第 1 行开始，运行到第 20 行，然后跳到第 190 行，运行到第 220 行，回到第 21 行，然后再次跳到第 240 行退出。这绝对是 hopscotching，但它的工作。

不久之后，程序化编程出现了，随之而来的是将代码分割成一个独立的执行单元——函数——的早期尝试。函数引入了应用程序内代码共享的概念。尽管如此，在网络上的整个系统(更不用说许多系统)之间共享单个代码单元的框架需要一段时间才能开发出来。因此，在编程的早期，代码冗余非常普遍。

需要记住的是，冗余代码的泛滥与其说是专业能力不足的反映。更确切地说，这是因为缺少一个避免代码冗余的编程框架。

但是，那是过去，这是现在。今天，干是一个标准的操作咒语。这很好。另一方面，仍然有很多冗余代码，特别是在有很多遗留 COBOL 的商店里。记住，COBOL 刚刚庆祝了它的 60 岁生日。已经有一段时间了。

幸运的是，随着内置于 IBM Developer for z/OS 的重复代码检测技术预览版的引入，COBOL 中的冗余代码世界将会变得更小。

## **了解重码检测技术预览**

重复代码检测技术预览版(DCD)是一个由 IBM Developer for z/OS (IDz)支持的特性，可以自动发现给定代码库中的重复代码。这是一个可选功能，从版本 14.2.2 开始提供，需要在 IDz 安装期间添加。DCD 是一个企业级工具，旨在用于大量的 COBOL 源代码，达到一百万行代码或更多(见图 1)。

![Duplicate Code Detection Technology Preview for IBM Developer for z/OS](img/1d2f0a7b49b3ba73ffe25d540bf07501.png)

Figure 1: Duplicate Code Detection Technology Preview for IBM Developer for z/OS exposes duplicate code for elimination or refactoring.

一旦发现重复，开发人员可以使用 DCD 来判断给定的冗余是否合适，或者是否是需要删除的重复。因此，DCD 可以用作评估代码质量的工具和重构代码库的工具。

| **See Duplicate Code Detection Technology Preview in Action**在 IBM 即将举办的网络研讨会上，“ 重复代码检测——更简单&更快速地贯穿整个生命周期网络研讨会，”2020 年 5 月 20 日上午 9 点到 10 点(东部时间)，您将深入了解 IBM Developer for z/OS 的重复代码检测技术预览。建筑师 Herve Le Bars 和 Jean-Yves Rigolet 将在现场讲解使用 DCD 消除重复代码和提高代码质量的细节。网上研讨会是免费的，其中充满了重要的信息，这些信息肯定会提高使用 IBM Developer for z/OS 的开发人员的工作效率。您可以在此注册 DCD 网络研讨会[。](https://community.ibm.com/community/user/imwuc/events/event-description?CalendarEventKey=c94053f2-2ea2-4f92-a4b3-f7ef0bcad577&CommunityKey=0ab505af-8e12-4199-843b-0dbbb3848f0e&Home=%2fcommunity%2fuser%2fimwuc%2fcommunities%2fcommunity-home%2frecent-community-events&_zs=d2jVb&_zl=TkO42) |

## **重复代码检测技术如何工作**

重复代码检测技术是一个可选特性，可以完全集成到 IBM Developer for z/OS 中。开发者可以使用 DCD 作为一个独立的应用程序来搜索他或她的工作区中的重复。此外，开发人员还可以在团队中共享重复代码检测结果。为了获得重复代码检测的协作体验，需要在服务器端安装三个附加组件。这些组件是:

*   IBM Websphere Liberty Server
*   重码检测喂养代理
*   源代码管理系统

让我们来看看它们是如何组合在一起的。

如上所述，开发人员可以使用 IBM Developer for z/OS 的 DCD 来检查单个开发人员的工作空间中的代码重复。在这种情况下，DCD 实质上是一个独立的工具(见图 2，插图编号 1)。

![Duplicate Code Detection](img/d196bf413abd6ab7f6601b8eade74aed.png)

Figure 2: Duplicate Code Detection works standalone and as a collaborative tool.

虽然让一个开发人员检测他/她的工作空间中的重复代码是有益的，但这在范围上是有限的。一个开发人员只能做这么多工作。当搜索代码重复的结果可以在团队中共享时，事情变得非常强大。这就是在客户端-服务器架构中使用 DCD 的地方。

DCD 客户机-服务器体系结构的核心是 DCD 服务器，它是 IBM Websphere Liberty 服务器和 DCD 网络应用程序。

DCD 服务器用于在开发团队的成员之间共享重复代码检测的结果。开发人员使用运行在 IBM Developer for z/OS 中的 DCD 组件与 DCD 服务器进行交互(参见上面的图 2，插图编号 1)。

在服务器端，有一个独立的客户端，即重复代码检测馈送代理，它充当存储在源代码控制管理系统下的源代码和 DCD 服务器之间的桥梁。

feeding agent 向 SCM 询问源代码管理系统中已更改的 COBOL 文件(见图 2，插图编号 2)。然后，DCD 馈送代理将更改发送到 DCD 服务器(参见图 2，插图编号 3)。

DCD 服务器跟踪重复代码(见图 2，插图编号 4)。如上所述，团队成员使用 IBM Developer of z/OS 来访问 DCD 服务器，以可视化重复的代码信息。DCD 馈送代理以增量方式工作:只传输更改过的 COBOL 文件进行检查，从而减少了操作开销。

| 您可以下载[【DCD】安装指南](https://epwt-www.mybluemix.net/software/support/trial/cst/programwebsite.wss?siteId=841&tabId=1929&p=&h=null) 阅读安装和配置重码检测的详细内容。 |

## **使用重复代码检测技术的好处**

使用重复代码检测技术有很多好处。自动重复检测简化了重构。重复代码检测技术可以自动识别数百万行代码中出现的冗余，而让开发人员来判断代码重复是否合理。如果确实需要删除重复的内容，DCD 允许开发人员立即进行修改，从而节省时间，同时提高生产率。请记住，重复代码检测以闪电般的速度工作。搜索 100，000 行代码平均需要 100 毫秒。

此外，当使用 DCD 服务器启用分布式协作时，可以与团队成员共享搜索并存储以备后用，从而改善团队和团队成员之间的协作。

重复代码检测通过检查直接存储在源代码控制管理存储库中的代码来提高搜索效率。DCD 提高了代码的可读性，同时降低了复杂性。此外，它支持使用标准的源代码控制管理框架(如 GitHub)进行版本控制。

## **将所有这些放在一起**

干的原则如今已是老生常谈。虽然这是一个在年轻公司中更容易实现的原则，但那些代码库可以追溯到几十年前的企业发现采用 DRY 很困难。重构可能有风险。许多公司认为，除非有令人信服的理由重构旧代码，否则大多数情况下最好不要去动它，尤其是如果代码是用 COBOL 编写的。

但随着戏剧性的 [对 COBOL 编程的需求](https://www.cnbc.com/2020/04/06/new-jersey-seeks-cobol-programmers-to-fix-unemployment-system.html) 新泽西劳工部最近透露，COBOL 事关重大。而且，当 COBOL 代码被重构时(这肯定会发生)，在重构工作中应用 DRY 将是一个驱动原则。因此，DCD 有机会发挥关键作用。这是一项引人注目的技术。鉴于 DCD 给 COBOL 编程体验带来的力量，对当前和遗留代码实现 DRY 原则并不比对一个大文档进行拼写检查需要更多的劳动。

自从半个多世纪前编写第一个 Hello World 以来，重复代码一直是开发人员的克星。随着时间的推移，情况有所改善，但对于许多公司来说，这仍然是一个问题，尤其是那些遗留了大量 COBOL 程序的公司。将重复代码检测技术作为其 COBOL 编程工具箱的一部分的公司将不仅拥有创建更优雅、更可读和更高质量的代码的好处，他们还将很好地将 DRY 原则置于其软件开发活动的最前沿。