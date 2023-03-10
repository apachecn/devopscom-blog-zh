# DevOps:记录系统和参与系统一样重要

> 原文：<https://devops.com/devops-critical-systems-record-systems-engagement/>

有很多关于 DevOps 的讨论，以及它如何改进交付商业价值的过程。关于 DevOps 的大部分讨论都集中在基于网络的公司上，比如脸书，或者移动和分布式开发团队。但是 DevOps 原则同样适用于传统的记录系统、z/OS 应用程序。这些应用程序中的许多已经存在了很长时间，并且具有非常成熟的开发和部署流程。这些流程包括职责分离和审计跟踪的要求。这些年来，这些流程已经发展成为冗长的程序，总的来说，其净效果是减少了部署的数量和频率，从而降低了风险。但是，有更好的办法。

在 Ashok Reddy 最近的博客文章中，他谈到了 8 个关键的 DevOps 实践:创新、交付、重复。所有这些都适用于 z/OS 应用程序，对于这个博客，我想集中讨论一些实践，**松散耦合架构，使用 API 自动化测试，透明度和最小化移交，最大化流程**。

DevOps 是关于将整个组织整合在一起，包括开发和运营，以更有效地交付商业价值。“透明度”和“最小化移交，最大化流程”的实践涉及 DevOps 的人员方面的核心概念，即整合组织。通过打破组织之间的壁垒，人们可以一起工作，更快地完成业务目标。这不一定意味着实际上改变组织结构，但它意味着让组织结构作为跨职能团队一起工作。

监控和优化实践就是一个例子。这些通常是在应用程序部署到生产环境后由运营部门完成的。但是，如果在开发周期的早期，运营和开发部门共同协作，使用将在生产中使用的相同功能来监控和优化应用程序，那么任何问题都可以在周期的早期得到解决。这也有助于两个团队在应用程序部署到生产环境之前就了解监控和管理应用程序的要求。在今天的许多 z/OS 环境中，测试环境中已经有了相同的基础设施，但是很少使用。

第二个例子是让操作定义部署自动化，这样它可以在早期阶段由开发完成，并在后期阶段移交。这确保了对部署能力的持续测试，以及在生产中完成部署时的验证；部署过程本身将得到很好的检验。通过这种开发和操作的集成，您消除了目前只发生在生产部署之前的最后阶段的移交。

在构建多平台应用程序时，松散耦合架构的实践是关键。在应用程序的不同部分之间有清晰的接口定义对于松散耦合的架构来说是必不可少的。更容易的是允许独立构建功能，在接口级别进行测试，然后在各部分准备就绪时将它们组合在一起。通过在应用程序组件之间定义清晰的接口，并正确处理向前和向后兼容性，减少了对协调的同时部署的需求。这允许团队在开发过程中减少对应用程序其他部分的依赖，并允许更容易的自动化测试。

自动化测试实践对于任何 DevOps 转换都是至关重要的。它能够提高交付速度，同时降低风险。转移到敏捷开发实践，同时仍然要求人们执行手动测试，将不允许在能力上的快速迭代。即使对于现有的应用程序，您也可以生成接口测试来开始构建自动化回归测试用例。自动化测试可以基于接口定义来生成，比如 JSON 模式或者新开发的 COBOL copybook。越来越重视早期测试接口有助于减少通常在开发周期后期发现的集成问题。

这些只是 DevOps 的一些关键实践，但希望它们已经开始展示 DevOps 如何适用于 z/OS 上的记录系统，就像它适用于接洽系统一样。要了解更多信息[，请阅读 IBM System z 方法的最佳实践白皮书](https://www14.software.ibm.com/webapp/iwm/web/signup.do?source=swg-rtl-sd-wp&S_PKG=ov26345)或观看 11 月 20 日在[举行的 IBM DevOps 研讨会网络广播的重播](https://w.on24.com/r.htm?e=879165&s=1&k=7557958DD1C9F547F12C3BA083632062)。

**关于作者:**

[![Rosalind](img/4fe7a0d2024624a8eecde612f9297a4d.png) ](https://devops.com/wp-content/uploads/2014/11/Rosalind.jpg) Rosalind Radcliffe 是 IBM Rational 组织中的杰出工程师。她是 CLM 和德沃普斯的首席建筑师。她负责推动面向多平台架构的开发运维。这包括 z 系统和动力系统。此外，她还负责企业解决方案的协作管理功能的架构。这包括 UrbanCode Deploy 和 Rational Team Concert 对标准大型机开发活动的支持。

她是 IBM 技术学院的成员，也是一位发明家大师。在加入 Rational 之前，她在 Tivoli 负责 IBM 的 SOA 管理策略。