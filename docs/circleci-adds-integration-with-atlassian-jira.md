# CircleCI 增加了与亚特兰蒂斯吉拉的整合

> 原文：<https://devops.com/circleci-adds-integration-with-atlassian-jira/>

在 DevOps 时代，IT 供应商正在处理的一个更棘手的问题是，很少有组织在单一供应商的平台上实现标准化。组织不仅可以根据自己的需要混合和搭配工具，而且同一组织内的不同部门也可以采用不同的工具来自动化相同的任务。开发运维的现实需要 IT 供应商之间的协作，而不管他们喜不喜欢，这些供应商通常都不愿意合作。

一个典型的例子是 CircleCI，一个持续集成/持续交付(CI/CD)平台的提供商，提供与 Atlassian 开发的吉拉项目管理软件[的集成。CircleCI 业务发展主管 Tom Trahan 表示，虽然 Atlassian 开发了自己的 CI/CD 平台，但客户和业务合作伙伴都明确表示，他们需要 CircleCI 来支持吉拉。在某些情况下，这些组织采用了吉拉系统，但其环境中没有 Atlassian 的 CI/CD 平台，而在其他情况下，一个组织的一个部门选择了 CircleCI，而其他组织则采用 Atlassian 的 CI/CD 平台。](https://circleci.com/blog/circleci-launches-support-for-jira-software/)

与此同时，Trahan 指出，许多 DevOps 项目现在跨越多个组织，这些组织在不同的 DevOps 平台上实现了标准化。他说，吉拉为不同组织的团队合作管理这些项目提供了一种方式。

为了实现与吉拉的集成，CircleCI 现在提供了 CircleCI for 吉拉模块，通过该模块，团队可以根据 CircleCI orbs 的工作状态分配新的任务和修复，CircleCI orbs 是一套可重复使用的配置包，允许 circle ci 客户将外部工具集成到他们的工作流程中。这一功能还使得在 CircleCI 用户界面的工作页面上直接发布新的吉拉问题成为可能。

[![CircleCI Integrates with Jira](img/1e85b7505c7f2c439496d1cec400ebc0.png)](https://containerjournal.com/wp-content/uploads/2019/05/CircleCI-Create_IssueJira-1.jpg)

Trahan 说，在 DevOps 的多语言世界中，很明显，供应商被要求公开开放应用程序编程接口(API ),使组织能够以他们想要的方式构建和集成各种 DevOps 平台。他说，组织不会考虑在集成水平方面过于死板的 IT 供应商。

随着 DevOps 的不断发展，很明显，合并和收购活动的浪潮正在使 it 供应商的前景变得有些不稳定。组织已经标准化的 DevOps 工具提供商正在被快速收购。IT 组织无法确定他们正在使用的任何给定工具或平台不会被他们可能不想合作的供应商抢走。在这种环境下，it 组织利用开放 API 至关重要，这不仅可以简化协作，还可以在必要时替换 DevOps 堆栈的元素。

当然，挑战在于 IT 供应商总是试图尽可能多地锁定客户。这些努力不像以前那样严厉了。但是几乎不可避免的是，如果支持它的底层平台突然消失了，为访问功能而提供的扩展也会消失。因此，IT 组织需要确定这些扩展是否值得，它们可能会在 DevOps 之路的某处引起任何潜在的麻烦。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)