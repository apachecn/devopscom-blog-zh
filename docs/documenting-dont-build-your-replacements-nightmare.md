# 记录:不要做你的替代者的噩梦

> 原文：<https://devops.com/documenting-dont-build-your-replacements-nightmare/>

***想减轻明天的头痛？**记录今天的一切*

大约一年一次，我觉得有必要提醒你，你正在创造技术债务。DevOps 是好东西，大多数商店很快就克服了“无论给定项目团队决定什么”的服务倍增，但是您编写的每一行 DevOps 代码都在产生技术债务。

这个事实是无法回避的。您正在编写代码(如果您愿意，也可以是脚本)并开发做出假设的配置。这些假设将会改变——产品将会得到不兼容的升级，供应商将会倒闭，库将会过时……不胜枚举。

我们与[技术债务](https://en.wikipedia.org/wiki/Technical_debt)有很长的历史。DevOps 部分源于花更少的时间维护和更多的时间发布特性的需要，然而我们正在重新创建技术债务；在某些情况下规模要大得多。这是不可避免的，但可以控制。保留一个假设参考列表——“本应用假设环境包含 X，”或“本应用支持思科网络应用编程接口 X.Y 版”——这样你就知道当事情不可避免地出错时去哪里找。当你发现你的中间件供应商倒闭了，或者 MySQL 被淘汰了，MariaDB 进来了，这个列表可以方便地作为需要更新的参考。

你使用的尖端工具越多，你就越有可能把未来的问题带到你的环境中。这不是避免尖端的建议；这是一个建议，当你将新事物带入你的环境中时，要认清现实并保持密切跟踪，这些新事物可能是不成熟的，或者其市场注定要整合。

我们的 IT 环境变得超级复杂。DevOps 帮助我们管理这种复杂性，但不鼓励足够的文档。我们都听说过，“它是自文档化的”(不，不是)或者“有基本的文档化”(基本几乎总是意味着，“我们在它刚建立的时候划了一些笔记”……之后就再也没碰过)。不要那样做。确保你们所有人离开[后，新来的人能够弄清楚](https://devops.com/knowledge-is-power/)在这个高度复杂的环境中发生了什么。新人并不能成为拥有读心术的超级学习者；实现人员有责任确保新人能够明白发生了什么，而不必浪费 5000 个小时在脚本中摸索。

记录依赖关系并不需要太多时间。记录关系并不需要太多时间。未来，当他们走进来并需要在短时间内达到速度时，你会很感激。因为当自动化出现故障时，自动化程度有多高并不重要，重要的是现场员工能多快修复并让事情再次顺利进行。

你让世界继续运转。花一秒钟，确保下一个人也能做到。继续摇摆。