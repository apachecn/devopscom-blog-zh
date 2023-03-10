# 使用 Node.js 的几大理由

> 原文：<https://devops.com/top-reasons-use-node-js/>

当考虑一个新的 web 应用程序的架构时，将 Node.js 作为该架构的关键部分包括在讨论中可能是一个好主意。Node.js 可以为您提供额外的速度，可以在许多平台上使用，并且有一个活跃的社区，从中可以获得模块和其他帮助。

## **node . js 是什么？**

Node.js 是 Ryan Dahl 在 2009 年开发的服务器端平台。它建立在 Chrome 的 V8 JavaScript 引擎上，设计有一个非阻塞的事件驱动 I/O。它也是跨平台的，能够在 Windows，Linux 和 OS X 上运行。它的非阻塞 I/O 是由于它使用了异步功能，使服务器不必等待数据返回，然后才能继续执行其他任务。

## **为什么要用？**

给定 Node.js 的架构，对于开发人员和他们开发的应用程序都有许多好处。这些优势包括速度、编程语言的一致性、易于开发的实时应用程序以及开发人员在创建新应用程序时可以使用的大量模块/包。

### **速度**

在许多情况下，Node.js 提供了速度优势。首先，它使用 Google V8 引擎，该引擎针对 JavaScript 速度进行了优化。此外，它对非阻塞异步行为的使用可以减少用户看到操作完成所需的时间，因为当用户转移到其他任务时，事情可以在后台进行。

### **一种语言**

![](img/5130f3496a879e4ce3422fb9135f74cf.png)

JavaScript 被列为最流行的编程语言。来源:[the newstack](http://thenewstack.io/javascript-popularity-surpasses-java-php-stack-overflow-developer-survey/)

使用 Node.js，前端和后端代码都可以在 JavaScript 中，因此您的开发人员在堆栈中移动时不必在语言之间转换。有些架构，比如 MEAN stack (MongoDB，Express.js，Angular.js，Node.js)，就是围绕这个原则设计的。在这种情况下，堆栈对 Express、Angular 和 Node 使用 JavaScript。MongoDB 使用 BSON 进行数据库查询，它使用与 JSON (JavaScript 对象表示法)相同的语法。

将全栈开发人员视为最大的职业，将 JavaScript 视为后端和前端的顶级语言，这与我们所看到的 JavaScript 整体采用情况一致。

*来源: [Mikeal Rogers，Node，js 基金会社区经理](http://thenewstack.io/javascript-popularity-surpasses-java-php-stack-overflow-developer-survey/)*

对于开发人员来说，这既有助于在开发过程中跨栈移动，也有助于开发人员之间的交流，因为他们在讨论编程决策时将引用相同的语言(JavaScript)。

### **实时应用**

Node.js 是一个创建实时应用的伟大平台。使用 [Sockiet.io](http://socket.io/) 等模块，您可以创建实时聊天、游戏等。除了它的非阻塞异步架构，实时应用程序的开发速度和响应速度都很快。

### **模块**

节点包管理器(NPM)使得安装其他人开发的用于执行任意数量任务的包变得容易。这有助于鼓励开发人员之间的代码共享，并减少当一个或多个包可以为您处理代码时必须完成的定制开发的数量。

## **显著的例子**

Paypal 和优步就是使用 Node.js 的一些著名例子，这表明它确实可以用于大型项目。

### **Paypal**

Node.js 和全 Javascript 开发堆栈帮助 PayPal 提高了工程效率，并帮助重新思考和重新启动了产品、设计和运营思维。

*来源: [Sameera Rao，Paypal 高级业务产品工程经理](https://blog.risingstack.com/how-enterprises-benefit-from-nodejs/)*

早在 2012 年，Paypal 有一个单一的应用程序运行所有的东西，包括 UI、API 等等。这包括从一个应用程序复制并粘贴到另一个应用程序的大量重复代码，以制作不同位置的应用程序。

使用 Node.js，该公司能够模块化并清理其代码和流程，这反过来加快了其在任何给定时间所需的应用程序的开发。

根据 Paypal 的[工程团队](https://www.paypal-engineering.com/2013/11/22/node-js-at-paypal/)的说法，他们能够用比以前少 33%的代码行和 40%的文件来构建 Node.js 应用程序，并且能够以两倍的速度和更少的人员来构建它。当然，Node.js 被证明有利于他们的发展。

### **优步**

优步从一开始就使用 Node.js，它的分布式系统非常适合，因为会产生大量的网络请求。Node.js 使用的非阻塞异步 I/O 有助于确保快速发出和处理这些请求，从而尽可能提供最好的服务。

## 结论

Node.js 的好处已经被证明了。它有助于加速开发，可以在许多平台上使用，并且有一个活跃的社区，从中可以获得模块和其他帮助。在你未来关于网站架构的谈话中加入 Node.js。

— [布莱恩·惠勒](https://devops.com/author/bwheeler/)