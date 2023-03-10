# Quest Software 旨在为数据库管理员修补 DevOps 围栏

> 原文：<https://devops.com/quest-software-aims-mend-devops-fences-dbas/>

众所周知，应用程序开发人员和数据库管理员(DBA)之间存在很多争议，前者面临着加快应用程序构建速度的压力，后者负责为开发人员提供数据访问权限。历史上，开发人员一直依赖 DBA 来创建允许他们访问数据的模式。但是构建模式需要时间，这就是为什么最近许多开发人员选择使用不需要模式来访问数据的 NoSQL 数据库。虽然这为开发人员提供了一些急需的灵活性，但如今企业中存储的大部分数据仍然在关系数据库中。

为了使数据库管理员能够更快地响应开发人员的需求，Quest Software [发布了 Toad for DevOps toolkit](https://www.quest.com/community/news/b/press-releases/posts/quest-launches-new-toad-devops-toolkit-to-increase-velocity-of-application-updates) ，该工具可以更轻松地将 Oracle 等关系数据库纳入由 Jenkins、Bamboo 和 Maven 等框架管理的更大的持续集成/持续开发(CI/CD)流程中。

Quest database management solutions 的产品管理和营销执行总监 Greg Davoll 指出，传统上，DBA 一直是最后一个拒绝接受 DevOps 的人，因为 DBA 并不真正拥有能够让他们参与敏捷开发环境的工具。Davoll 表示，Toad for DevOps 工具包解决了这一问题，使他们能够在应用程序构建过程中测试 PL 和 SQL 代码，并确保 DevOps 管道流程环境中模式、数据和数据库的完整性，增加参与 DevOps 流程的数据库管理员现在还可以执行静态代码审查，并将工件提升到目标环境中，以查看它们在生产环境中的表现。

Toad for DevOps Toolkit 的到来计划与 Toad for Oracle 2017 R2 的发布相一致，这将在代码分析代码审查流程中添加通过/失败状态通知，重新设计的多模式比较和同步功能，以及作为基准工厂测试工具一部分的增强 REST API，以帮助在 CI/CD 工作流中自动执行性能测试。达沃尔说，随着时间的推移，Quest Software 将在其支持的所有数据库中增加类似的功能。Quest Software 刚刚宣布推出一款用于 MySQL 的 Toad 产品，以补充其对 Oracle 和 Postgres 数据库的现有支持。

这些年来，许多关于使用什么数据库的决策都归结于开发人员部署哪个平台的摩擦最少。这并不总是导致做出正确的数据库决策。事实上，开发人员通常很快就会想把数据库的管理工作交给 it 部门。这必然会导致数据库管理员不得不管理多个数据库平台。虽然使用关系数据库之外的东西可能有完全合理的理由，但该决定应该基于数据库的属性，而不是内部 IT 政策和购买过程。DBA 现在面临的挑战是如何重新吸引那些对特定数据库类别有偏见的开发人员，不管他们拥有多少关键数据。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)