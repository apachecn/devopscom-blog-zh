# Git:向 DevOps 迈出的一大步

> 原文：<https://devops.com/git-one-giant-leap-toward-devops/>

如果您在一个尚未采用 DevOps 的组织中工作，那么您可能想知道从哪里开始。还好，[有很多好答案](https://devops.com/2015/04/20/9%C2%BD-simple-steps-start-devops-today/)。但是我想介绍一个你可能没听过的简单的起点:将 Git 引入操作。就其本身而言， [Git](https://www.atlassian.com/git/) 似乎不是一种有意义的方式来克服开发和运营之间的障碍。然而，Git 提供了一些标志着最低绩效的 it 组织和最高绩效的 IT 组织之间的差异的功能。IT 性能的差异可以转化为巨大的业务优势。最高绩效的 IT 组织[已经注意到了以下优势](https://puppetlabs.com/2015-devops-report):

*   他们超出盈利能力、市场份额和生产率目标的可能性大约是两倍。
*   他们的员工对工作的满意度要高得多。
*   他们在三年内实现了 50%以上的市值增长。

需要明确的是，再多的数据也无法证明 Git 的使用会直接带来增长、利润、生产率和工作满意度。 [Puppet Labs 的“开发现状调查”](https://puppetlabs.com/2015-devops-report)确实显示了 IT 组织中低绩效和高绩效之间令人难以置信的差距。高绩效组织的部署速度比最低组织快 30 倍。2014 年的调查显示部署失败减少了 50 %,而 2015 年的调查显示部署失败减少了 60%。该调查还显示了哪些做法将表现最好的人与表现最差的人区分开来。根据 DevOps 调查，高绩效的两大指标是:

*   所有产品工件的版本控制(令人惊讶的是，比源代码的版本控制更能预测性能)；和
*   生产变更的同行评审(与外部变更批准相反)。

这并不是说这两种做法神奇地产生了商业利益。事实上，ITIL 早就认识到生产工件的管理和生产变更的审查是最佳实践。但是太多的组织仍然认为更快的部署和更高的可靠性是一种折衷。高绩效组织的“神奇之处”在于他们意识到，通过跨组织边界协作和智能自动化，他们可以同时实现更快的部署和更高的可靠性。这意味着开发人员和运营人员共享目标、衡量标准和工具。因此，这些实践与典型的 ITIL 实践的一个不同之处是开发人员和运营人员如何协作执行它们。更具体地说，当开发人员和运营人员使用相同的工具进行版本控制时，他们可以更好地共享技术和工作流。例如，变更的同行评审可以包括开发和运营。因此，Git 是通往 DevOps 的门户。

Git 长期以来一直为软件开发人员提供这两种能力:开发人员使用 Git 来[版本源代码](https://www.atlassian.com/git/tutorials/comparing-workflows)和开发人员使用[拉请求](https://www.atlassian.com/git/tutorials/making-a-pull-request)来执行[源代码同行评审](https://www.atlassian.com/agile/code-reviews)。有了一些关于如何将 Git 应用到配置文件的技巧，操作可以使用 pull 请求来执行配置变更的对等审查。现在有了 [git-lfs](https://blogs.atlassian.com/2016/02/git-lfs-for-designers-game-developers-architects/) ，操作也可以对产品工件进行版本控制，这些工件通常是大型的二进制文件，在历史上 git 并不能很好地工作。更高级的概念，比如作为代码的基础设施和专用的二进制库建立在版本控制的基础上，所以即使 Git 的角色随着时间的推移而改变，技能和协作仍然是有价值的。

总之，Git for Ops 的业务案例很简单。Puppet Labs 的调查显示了低绩效 IT 组织变得高绩效的重要优势。调查显示，高绩效组织的特点是快速部署和高可靠性，而不是厚此薄彼。表现高性能 IT 组织特征的两个实践是产品工件的版本控制和变更的同行评审。Git 现在很适合提供这两种能力。如果您准备开始向 Git 引入操作，不要忘记 [Bitbucket](https://bitbucket.org/) 对私有存储库的数量没有限制。

## 关于作者/伊恩·布坎南

虽然 Ian Buchanan 在 Java 和。NET，他以大型企业中敏捷方法的拥护者而闻名。他目前是 [Atlassian](https://www.atlassian.com/) 的 [Developer Tools](https://www.atlassian.com/software/dev-tools) 的[开发者助手](https://twitter.com/devpartisan)，在那里他主要关注新兴的 DevOps 文化和 [Bitbucket](https://bitbucket.org/) 和 [Bamboo](https://www.atlassian.com/software/bamboo) 的应用，以实现更好的持续集成和持续交付。在他的职业生涯中，他成功地管理了企业软件开发工具生命周期的所有阶段，从摇篮到坟墓。他推动了整个组织的流程改进，从而提高了生产率、质量和客户满意度。他建立了重视自我指导和自我组织的跨国敏捷团队。当不说话或编码时，您可能会发现 Ian 沉迷于解析器、元编程和特定领域语言。