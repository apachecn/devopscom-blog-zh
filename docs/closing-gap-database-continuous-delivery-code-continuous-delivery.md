# 缩小数据库连续交付和代码连续交付之间的差距

> 原文：<https://devops.com/closing-gap-database-continuous-delivery-code-continuous-delivery/>

关于数据库交付的当前状态，我得到的最重要的反馈直接来自我遇到的 DBA。他们的 DevOps 团队陷入了手工数据库交付的炼狱。开发经理只是希望数据库交付能够像他们的软件交付一样工作。然而，数据库完全是另一种动物。不幸的是，数据库的 DevOps 已经让位于源代码，因为我们看到了工具和方法的完善，让数据库自动化去玩一场追赶的游戏。

另一个问题是 DBA 不像代码开发人员那样信任部署自动化。所有的 DBA 都曾因这样或那样的故障或冲突而焦头烂额，他们中的大多数人只是觉得他们需要自己处理问题，以确保正确地完成发布。我们最近调查了 200 多名数据库管理员，其中最大比例的人指出对自动化的不信任是他们数据库采用连续交付的最大障碍。在同一个调查中，只有一半持续交付代码的公司说他们也在为数据库做开发运维。这需要尽快改变，否则数据库交付将停留在过去，并减缓所有公司的发布。

数据库保存着最重要的公司信息，它们需要被视为与为公司软件编写的代码同等重要，甚至更重要。所以，问题是，我们如何缩小源代码自动化和数据库自动化之间的差距？

答案比你想象的要简单。我们需要为数据库的开发运维带来相同的源代码持续交付流程。多么新奇的概念！

数据库开发运维需要最佳实践，就像源代码一样。需要加强部署实践。需要加强版本控制。需要创建安全的自动化流程。您需要将数据库包含在连续的流程和反馈循环中。最重要的是要确保你有办法控制这些过程，如果有什么事情需要处理，会有自动通知和危险信号指出问题。

也就是说，确保数据库的安全连续交付并不那么简单。数据库不是文件的集合；它们保存着客户信息、交易数据、应用程序内容等。要使自动化真正发挥作用，需要创建一个可靠的转换代码来处理数据库模式结构、数据库代码和元数据等内容。

此外，还需要进行组织层面的变革，以确保适当的连续数据库交付。DBAa 和 C 级管理层都需要采用这些数据库开发方法。这不可能也不是一个人的工作。双方都需要倡导数据库自动化。

每个人都认识到数据库对组织的重要性。这就是数据库管理员如此害怕自动化的原因，而且管理层也没有强制实施。应该正好相反！他们对数据库控制和自动化的看法需要更加积极。他们问的问题是——如果我们将连续交付引入数据库，会出现什么问题？问题应该是——如果我们*不*为我们的数据库带来持续交付，会出什么问题？

是的，数据库部署自动化不是一个简单的过程，但事实是，确保连续交付意味着提高生产力、加快上市时间、降低新版本的风险，以及更高的质量和更少的错误。否则，您的数据库会一直滞后，最终您会发现自己处于一个困难的境地。

* * *

#### 

**[![](img/928cbd4719a2396ee5a50ef2acada445.png)](https://twitter.com/dbmaestro)**

#### 关于作者

雅尼夫·耶胡达，首席技术官，db maestro(【http://www.dbmaestro.com/】T2)

*Yaniv 是 DBmaestro 的联合创始人兼首席技术官，db maestro 是数据库解决方案 DevOps 的领先提供商，能够控制数据库开发和部署。Yaniv 还是领先的 IT 服务解决方案提供商集团 Extreme group 的联合创始人和开发主管。*