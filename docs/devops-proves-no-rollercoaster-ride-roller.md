# DevOps 证明没有过山车乘坐过山车

> 原文：<https://devops.com/devops-proves-no-rollercoaster-ride-roller/>

保持游乐园运转和乐趣流动是[罗拉](https://roller.software)的主要工作。该公司为休闲和娱乐行业提供软件，特别是主题公园、游乐园和蹦床公园。其核心功能是票务、POS 和 CRM。客户包括[科尼岛月神公园](http://lunaparknyc.com/)、[澳洲世界](http://www.aussieworld.com.au/)和[双湖公园](https://www.twinlakespark.co.uk/)。

当 Roller 在 2015 年决定扩大和重新开发其业务时，DevOps 是主要的吸引力。首席技术官安德鲁·布罗迪(Andrew Brodie)领导了该公司的推动，他在担任数字产品设计工作室 Bravo 的联合创始人和技术总监期间，曾参与过 Roller 的原始实现。

罗拉生产过程的自动化是一个主要目标。Brodie 说，即使是小组织也应该采用良好的实践，这包括自动化一切可以自动化的事情(在合理的范围内),达到能够点击一个按钮来部署系统的程度。

## DevOps 之前

在早期，Roller 使用包括 Web Deploy 在内的微软工具来交付满足最低可行产品要求的整体应用程序。Roller 最初在 Ninefold 上运行，nine fold 是一个现已解散的澳大利亚 IaaS 平台。

当该公司在 2015 年吸引了额外的资金时，它能够扩大其开发团队，拥有包括开发人员在内的各种技能的人。今天，它由大约 50 人组成——12 名开发人员和各种用户体验、质量保证和项目管理专家。

新发现的专业知识支持将系统重新开发为一系列应用程序和微服务，并消除了最频繁执行的手动操作。

## 工具

Roller 的部署流程已经成为瓶颈，因此该公司投入时间采用最合适的工具。有几个来自 [HashiCorp](https://www.hashicorp.com/#open-source-tools) ，包括 Packer(用于创建机器映像)、Terraform(跨提供商基础设施管理)、Consul(服务发现、配置和编排)和 Vault(集中存储和控制密钥等分布式机密)。

在 Ninefold 消亡后，Roller 开始大量参与 AWS，AWS 以 API 和工具集的方式“拥有我们需要的一切”，以“编码我们的基础设施”，Brodie 说。但即使“我们真的很喜欢亚马逊”，该公司也避免使用专门的 AWS 工具来保留转移到 Azure 等其他平台的能力。

将负载平衡、自动扩展组等作为代码实现花了大约一个月的时间。“对我们来说，这是一个伟大的举动，”他说。

Roller 使用的其他工具包括 [Chocolatey](https://chocolatey.org/) 包管理器，微软 [PowerShell](https://msdn.microsoft.com/powershell) 及其[期望状态配置](https://docs.microsoft.com/en-us/powershell/dsc/overview)功能。在机器映像经过测试后，这正是进入生产环境的东西，提供了它将按预期工作的信心。

Roller 使用蓝绿色部署和自动缩放组，以便在必要时轻松回滚。部署或回滚不到 10 分钟。当个别问题出现时，Roller 的做法是杀死不健康的服务器，并提出一个新的。

该公司为每个应用程序和服务维护单独的部署管道，使用 Atlassian 的 [Bitbucket](https://bitbucket.org/) 分布式版本控制系统及其[管道](https://bitbucket.org/product/features/pipelines)功能来自动部署签入的代码。

如有必要，Roller 可以在一个小时内部署代码，但目前是每周发布一次。目标是在一天内发布多个版本。

## 资源

澳大利亚主要的工作场所 [Seek](https://www.seek.com.au/) 为罗拉的 DevOps 之路提供了灵感。布罗迪指出:“我们一直在关注更大的玩家。”此外，聚会(“每个人都有自己的事情”)和会议(他特别提到了 [DDD 墨尔本](https://www.dddmelbourne.com/)和 [NDC 悉尼](http://ndcsydney.com/))在与其他公司交流经验方面发挥了不可估量的作用。“我们渴望走在最新实践的前沿，”他说，因此公司鼓励员工参加这样的活动。

他发现其他有用的资源包括[堆栈溢出](https://stackoverflow.com/)和[复数](http://plural.com/)。此外，他还推荐了吉恩·金(Gene Kim)、杰兹·亨布尔(Jez Humble)、帕特里克·德博伊斯(Patrick Debois)和约翰·威利斯(John Willis)所著的《[devo PS 手册](http://itrevolution.com/devops-handbook)》，他将其描述为“一个了不起的资源”，提供了实用的建议，尤其是围绕组织层面的问题。

## 技巧

当被问及对那些开始新业务或重大项目的人的建议时，布罗迪建议实用主义:

*   从一开始就考虑 DevOps“但是不要煮过头了。”换句话说，从基础开始，然后从那里发展。
*   以持续改进为目标——人们会不断产生新的想法，但是选择合适的时间来实现它们是很重要的。
*   找一个导师，和人们谈论他们正在使用的工具。
*   利用外部组织的能力。例如， [Rackspace](https://www.rackspace.com/) 可以帮助设计 AWS 的应用程序。

斯蒂芬·威瑟斯