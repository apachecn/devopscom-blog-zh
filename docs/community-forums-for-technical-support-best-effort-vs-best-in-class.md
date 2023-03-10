# 技术支持社区论坛:尽最大努力还是同类最佳

> 原文：<https://devops.com/community-forums-for-technical-support-best-effort-vs-best-in-class/>

像 Stack Overflow 这样的开发者网站越来越受欢迎，每月活跃用户超过 1.25 亿；然而，绝大多数问题从未得到回答。供应商社区论坛远远落后，活动水平明显较低，导致昂贵的支持案例，平均解决时间[为 14 天](https://devops.com/?s=time%20to%20resolve)。随着技术发展速度和复杂性的增加，我们认为技术支持需要充分利用社区论坛作为获得答案的最佳场所。

现实情况是，技术人员不希望与支持机器人交谈，并认为开立支持票证是最后的手段。他们希望从他们信任的人那里迅速得到答案，他们的问题通常包含丰富的技术细节。虽然今天的论坛可以成为提出技术问题和与专家联系的绝佳场所，但社区提供的答案都是“尽力而为”的，很快就会过时。

我们公司分析了 50 多个论坛，包括 1200 万个独特的问题和回答，涉及企业供应商、开放核心软件和云原生开源发行版。我们的目标是了解“尽最大努力”社区在解决技术问题方面的表现，并确定设立标杆的最佳论坛。搜索结果会发布给任何人[浏览](https://dashboard.peritus.ai/forum-benchmark)，并定期更新。

## 最大努力度量

下图显示了问题解决的关键指标，以及社区中参与生成答案的人数。这是发布时我们当前数据集中所有论坛的平均值。
![community forums](img/c9ef293745fb25225a16b3439ba41b2d.png)
一个关键的问题是，不到三分之一的问题得到了回答，不到 20%的问题在 24 小时内得到了解决。这是潜在不满意用户和新支持案例的关键风险指标。第二个更令人惊讶的结果是，只有 20%的社区产生了 80%的答案！这是一个清晰的信号，表明论坛在教育和激励社区成员快速响应方面做得并不出色。如今最常见的激励措施是针对社区贡献者的个人声誉评级和排行榜。堆栈溢出使用户能够为挑战性问题提供奖金。

## **同类最佳指标**

相比之下，下图显示了每个指标的最佳结果。

![community forums](img/eda58d9b8f528fa6cc29027cb356b5b6.png)

我们非常兴奋地发现，72%的社区成员提供了 80%的答案。这似乎是一个所有论坛都应该努力达到的好的高水位标志。另一方面，42%的问题在不到 24 小时内得到解决，这一指标表明论坛是获得答案的最佳途径，有很大的上升潜力。

那么，谁是一流的呢？截至本文发布之日，三个顶级论坛都是开源社区。

*   已解决的论坛帖子: **KUBERNETES**
*   不到 24 小时内解决: **POSTGRESQL**
*   通过第一次响应解决: **ALTERYX**
*   解决 80%问题的专家人数: **NGINX**

开源技术的生死取决于免费分发的大量采用，依赖于同行的支持和教育来建立病毒式传播。因此，它们在我们的基准测试中排名很高并不奇怪。我们确实发现，对最热门的云原生技术的讨论，包括 Kubernetes 及其许多变体和工具，发生在许多不同的论坛上。这包括由发行物所有者(例如，Google)托管的论坛、堆栈溢出(有时有许多不同的标签)和由云本地计算基金会托管的 Slack 频道。从一个论坛开始的对话很快被转移到另一个专门讨论这个话题的论坛。

## 谁是社区论坛专家？

在每个社区论坛中，我们还根据回答问题的活跃程度和可接受的结果对成员进行了分类。我们的目标是确定对社区体验有最大影响的最积极的专家。通常，这些专家的动机是他们在论坛上的个人声誉的隐性和显性回报。

评估专家的分类标准是:

*   **回复:**个人的回复数。
*   **解析:**个人解析的帖子数量。
*   **接受率:**已解析帖子除以个人回复的百分比。

使用这些指标，我们创建了以下分类:

*   **贡献者**:解决了至少一个论坛帖子的个人。
*   **专家:**在回复和已解决帖子数量方面处于第 90 个百分点的贡献者。
*   **MVP(最有价值球员):**发帖回复数和已解决帖子数高于平均水平的专家。
*   **后起之秀:**回复数量低于平均水平但接受率高于平均水平的专家。
*   **高潜力:**我们分类中剩下的专家。

思科论坛的结果在这里显示为一个例子，NGINX 紧随其后作为对比。注意每个气泡的大小代表接受率(%)。对于 NGNIX，即使在高潜力分类中，许多专家的接受率也超过 50%,而思科的 MVP 和后起之秀平均只有 20%左右。

思科:

![](img/9e43b482d9c2d18443ad0a08c44a2978.png)

nginx:

![](img/a5302406e7809856adcbbf8c3d5238c1.png)

在我们的基准测试中，所有论坛的专家分类可以在这里查看。

## 社区论坛:超越同类最佳

社区论坛基准测试显示，通过从当前的“尽力而为”状态转变为同类最佳指标，有可能大幅降低案例偏离成本。我们认为，释放这种潜力的关键是给那些表现出积极性的专家提供工具，帮助他们更快地回答更多的问题，并提高接受率。一种有前途的方法是将机器学习应用于所有先前的对话和发布的内容，以推荐最相关的信息来帮助专家解决问题。简而言之，随着越来越多的专家创造出更多成功的答案，每个论坛都有可能达到并超越当今同类最佳的指标。随着论坛的蓬勃发展，它们的问题量自然会增加，成为主要的技术支持渠道。