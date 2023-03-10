# API 测试如何为您节省数千美元

> 原文：<https://devops.com/how-api-testing-can-save-you-thousands/>

***发布前的 API 测试可能意味着 25 美元的云数据库账单和 3 万美元的账单之间的差异***

基于使用的计费是基于云的 SaaS 平台中一种流行的支付模式。这个想法是，你只需为你的项目使用的数据量付费，这对于那些使用量有限的公司来说很好。

这就像从你厨房的水槽里拿一杯水。每次你打开水龙头，你都知道你的水费会上涨几分钱(实际上比这少得多，但举例来说)。假设水龙头是云平台，玻璃代表你的 API 请求。

组织积累过高的基于使用的账单的方式之一是来自 API 请求代码中的[关键错误](https://devops.com/challenges-of-designing-api-driven-experiences/)。例如，你的邻居要一杯水，你倒了 10 杯水，或者你倒完水后忘记关水龙头。这与 SaaS 平台上基于使用的计费非常相似，尤其是基于云的 API 请求。

## 数据请求出错的一个代价高昂的例子

哥伦比亚一个名为 Vaki 的众筹应用程序收到来自谷歌 Firebase 的[3 万美元账单](https://hackernoon.com/how-we-spent-30k-usd-in-firebase-in-less-than-72-hours-307490bd24d)时感到震惊，原因是一些非常简单的错误。该公司匆忙推出了自己的产品，然后注意到在版本合并后，应用程序运行速度慢得令人难以置信。

Vaki 有两个选择:要么关闭网站，要么在与金钱的赛跑中尝试调试应用程序。该公司选择了后一种选择，并发现其 API 的编码方式是，随着每个访问者访问他们的网站，它需要调用每个付款文件，以查看某个活动的支持者人数或收集的总数，在应用程序的每个页面上。

换句话说，该公司在不到 48 小时内向 Firestore 发送了超过 400 亿个请求——这是一个代价巨大的错误，尽管 Vaki 最终设法与谷歌解决了这个问题。一个问题是，Vaki 在网站已经上线时就已经在编写代码了，而这些 API 测试工具可能已经帮助公司在发布前发现了问题。

在发布之前，技术团队调试对服务器的每个请求是非常重要的。分析请求和数据传输的数量是否有意义，以及您的公司是否愿意承担大流量主机的成本。否则，你将会陷入循环或不优化的请求，导致巨额账单或网站瘫痪。

## api 从错误中学习

虽然亚马逊、谷歌云和微软 Azure 等基于云的数据库提供了按小时付费的模式，但 Firebase 基于对数据库的 100k-250k 读/写/删除请求计费。所以从技术上讲，如果你在这个范围内，你的账单*不应该超过 25 美元。*

但这也意味着你需要没有错误或循环的完美代码。Vaki 正在读取某个集合中的每个文档条目，以计算用户每次查看特定视图时的总收集值和支持值。

换句话说，如果一个众筹活动有 100 笔捐款，应用程序将调用数据库一次，但读取次数将等于 100 次读取两次，这意味着总共有 200 次读取请求。

显然，当一个活动的浏览量达到 200 万次时，对数据库的读取请求将很快超过数十亿次。值得称赞的是，这不是一个赚钱的计划，它是精心策划的，因为它很容易保持在目标指标之内。

在 Vaki 的案例中，这是数据结构中的一个简单的人为错误，没有针对效率进行优化，最终，该公司会遇到其他问题，如数据库连接达到极限。

## 如何将使用计费保持在最低限度

如今托管应用程序相当便宜，但如果不进行有效优化，数据库可能会迅速失控。当涉及到应用程序不同部分之间的流量时，读和写请求是整个流量中最频繁出现的。

因此，即使前端启动可能很快，也需要检查后端，尤其是在无服务器架构通常不提供后端数据会话的情况下。因此，由于后端需要更多的空间和处理能力，您的总账单会增加。

从所有这些中有一些关键的收获。一个是你需要重新考虑你的数据将如何影响读写总数的方法，以及需要多少处理能力，这基本上意味着优化你的代码以提高效率和长期稳定性。

另一点是在发布前测试你的 API 的重要性，这样你就可以在产品实际上线前发现 Vaki 遇到的缺陷。