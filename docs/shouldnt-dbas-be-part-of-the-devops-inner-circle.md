# DBA 不应该是 DevOps 核心圈子的一部分吗？

> 原文：<https://devops.com/shouldnt-dbas-be-part-of-the-devops-inner-circle/>

DevOps 正在改变 IT 文化。这一运动将应用程序开发和运营团队带到同一张桌子上，同时努力理解和克服整个应用程序交付流程所面临的挑战——而不仅仅是他们所面临的挑战。开发和运营团队正本着加速软件发布周期的精神打造新的纽带和联盟。

然而，尽管快速上市对成功至关重要，但企业不能忘记加速发布周期的内在含义。考虑到这一点，在“DevOps 核心圈”中有一个明显空着的位置，那就是数据库管理员(DBA)。

DBA 掌握着企业最重要的资产之一:数据库的钥匙。但是数据库变更创新并没有跟上敏捷开发方法和 DevOps 工具的步伐，这些方法和工具支持软件更新和变更的持续交付。绝大多数企业仍在以过去三十年的大部分时间里的相同方式更新数据库:通过手动脚本审查、验证、执行和个人英雄主义。因此，应用程序发布周期最终会在最后一英里——数据库——变慢。

是时候采用更好的方法了。是时候让数据库和它们的管理者 DBA 成为 DevOps 核心圈子的一部分了。包括 DBA 可以创建更好、更高效的团队；节省时间和金钱；甚至帮助公司为他们的客户或他们自己的需求创造更好的解决方案。

## 粉碎筒仓

DevOps 背后的基本原则之一是打破开发和运营团队之间的孤岛。产品经理可以很容易地翻译客户需求，并以他们理解的方式将反馈传达给开发人员——例如，使用史诗和主题。这有助于将所有人聚集在同一页面上，以便应用程序更新或更改可以快速编码、测试和交付。但是在应用程序更新可以安全有效地发布给用户之前，它们必须被转换成更新数据库的更改。这就是 DevOps 故障发生的地方。数据库管理员通常不得不依靠大量手动操作、耗时且容易出错的流程和工具来确保对数据库做出正确的更改。

通过将 DBA 邀请到 DevOps 核心圈子中，开发团队可以更快地发现违反业务策略并最终锁定数据库或“破坏构建”的数据库更新(想象一下当行数超过一百万时插入一个具有默认值的新列)，并在更改到达数据库之前解决这些更新。让 DBA 更快地参与发布周期有助于确保开发人员在编写代码时考虑到公司合规性，最终使数据库的更改更加顺利，同时遵守 DBA 通常遵守的准则。

曾经有一段时间，数据库需要保护，以免受到开发中创造性解决问题所带来的变化的影响，但是 DBA 根本无法承受加速周期所带来的大量变化。邀请 DBA 进入 DevOps 核心圈子，可以让团队考虑整个技术体系中新的变更和更新的影响。打破孤岛，让团队更加了解发布过程最后一英里的要点，让他们能够预测和避免数据库问题——这意味着更快的发布和每个人更少的麻烦。

## 节省时间(时间就是金钱)

更快的发布周期对企业有利，这不仅仅是因为它们能更快地将应用程序呈现在最终用户面前。连续交付周期旨在通过节省工时来大幅削减与应用程序开发相关的成本。尽管开发时间越来越短，但是部署数据库变更的工作量和时间却越来越长。

企业可以有多个数据库配置，因此需要检查每个更改的兼容性。随着数据存储库复杂性的增加，审查和批准变更所需的时间也在增加。在 2015 年 IOUG 关于数据库可管理性的调查中，41%的受访者表示更改需要一周或更长时间才能获得批准。随着 DBA 每月、每周甚至每天都会收到多个变更请求，很明显，纯粹的人力无法永远跟上持续交付的步伐。没有自动化，DBA 就没有解脱。

还记得我们之前的例子吗，当行数超过一百万时，我们通过插入一个具有默认值的新列来冒锁定数据库的风险？数据库自动化软件通过预测应用程序变化对数据库的影响来防止这种结果。数据库管理员可以使用自动化软件生成的预测报告来查明任何问题，而无需花费数小时或数天进行昂贵的搜索。

作为 DevOps 团队的一员，配备自动化的 DBA 可以做的不仅仅是为自己节省时间和解决麻烦。防止可能破坏构建的错误可以节省团队寻找和修复故障源的时间，还可以在修复过程中避免企业损失收入。如果如此多的时间、金钱和潜在的挫折都依赖于 DBA 以持续交付的速度实现变更的能力，为什么他们仍然处于 DevOps 核心圈之外？

## 腾出时间进行创新

当你试图让自己的头露出水面时，灵感很少闪现，对于许多数据库管理员来说，这就是工作的现实。今天，企业与数据库打了一场消耗战，将人力投入到发布周期的最后一关。除了节省工时的诱人好处之外，将 DBA 引入 DevOps 核心圈子并自动化他们的一些任务也为创新创造了时间和空间。

关系数据库是近 50 年的创新，它改变了人和计算机通过数据进行交互的方式。过了这么长时间，地平线上又出现了这么多东西，下一个创新似乎迫在眉睫，甚至可能姗姗来迟。量子计算的出现可能会给数据库之间的交互方式带来根本性的改变。这肯定会带来数据存储和检索方式的转变，尽管目前专家预计只有最复杂的业务流程会从量子计算中受益。因此，虽然未来的技术仍然遥不可及，但数据库管理员在努力创新更快、更简化的方法来处理零和一方面将至关重要。

因此，创新的第一步是解决数据库管理员以及客户和开发人员的需求。打破现有 DevOps 团队和 DBA 之间的壁垒并提高效率，将使团队有更多的机会为他们的用户和他们自己的问题创建新颖的解决方案。为核心圈增加另一个席位，节省时间和资金，更快地将优质应用推向市场，并为当前和未来的问题创造创新的解决方案。

## 关于作者

![Derek Hutson Headshot](img/4b4f6f0282b1217b9e1294882638842a.png) Derek Hutson 于 2015 年加入 [Datical](http://www.datical.com/) 担任首席执行官，他在企业软件领域拥有超过 15 年的领导经验。在加入 Datical 之前，他领导多家公司经历了长时间的快速增长，并在 IBM 担任过多个高管职位。在那里，他在 IBM 收购 Telelogic 的领导团队中任职，负责尽职调查和整合收购的全球销售职能。他目前在 Hart InterCivic 和 Charity Dynamics 董事会任职。其他董事会或顾问职位包括 CoreTrace(被 Lumension 收购)、Innography、StreamStep(被 BMC 收购)和 Phurnace(被 BMC 收购)。