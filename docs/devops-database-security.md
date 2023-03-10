# 开发运维与数据库安全

> 原文：<https://devops.com/devops-database-security/>

Osterman Research 最近发布了一份基于调查的关于数据库安全性的报告。调查结果并没有让人们对用户名泄露产生信心:超过 50%的受访者认为数据库泄露对他们的组织来说是一个严重的问题，而 44%的受访者认为检测泄露的凭据和数据泄露需要一天以上的时间。考虑到攻击者会尽可能快地进入和离开，超过 24 小时的时间对于那些被破坏的凭证来说是足够的，从而导致表的副本进入黑暗网络。我们一些最大的黑客*——雅虎！*突然想到——需要更长的时间才能被发现。

有一些工具可用于监控数据库登录和活动，从免费(有时很麻烦)的 MariaDB、MongoDB 和 MySQL 等数据库日志记录，到大多数数据库系统的 Splunk 插件等审查和分析。一旦您跟踪登录和源 IP，并可能观察查询量的峰值，DevOps 的强大功能可以帮助您管理监控。

![](img/f7f2bfbdd43f8b3a3b63efc2cc136e21.png)

这里的关键是收集数据，即使是暂时的。很好的第一步是构建一个流程，在设定的时间段内打开登录尝试日志记录，然后处理生成的文件，向用户发送他们登录的时间和地点的列表。

接下来，捕获关于查询数量和响应大小的摘要信息。这可以显示内部或外部不良行为者对凭证的滥用。问题不在于完成这些工作的工具的可用性；这个问题是使它成为一个优先事项。

虽然不将数据库暴露给 internet 是一个好策略，但是监视数据库凭证可以提供针对外部攻击者的深度防御，以及针对内部攻击者的防御。利用可用的工具加上 DevOps 的一些工作(自动化该过程，然后制定出向监控系统添加新的应用程序和用户登录的方法)将提高您检测凭据问题的能力，并且该过程(当涉及 DevOps 时经常发生)将迫使您审查哪些应用程序从哪里访问数据库，可能会发现改进数据库使用和位置的想法。

这些都是 DevOps 真正能提供帮助的安全领域；很少有任何一个团队能够控制数据库登录/查询的安全性。这是数据库管理员的责任吗？安全小组？运营(通常创建账户)？利用可用的工具，坐下来讨论哪个对您的组织最有意义，您可以生成一个简单的报告，定期进行审查，并解决责任问题。这意味着没有大量的时间浪费在浏览日志上，也没有等待数周的时间去发现你的数据库已经被入侵。这很有意义，它弥补了安全性从开发运维中获得直接好处，而不是从标准化流程中获得间接好处的差距。

唐·麦克维蒂