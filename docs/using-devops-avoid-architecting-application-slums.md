# 使用 DevOps 避免架构应用贫民窟

> 原文：<https://devops.com/using-devops-avoid-architecting-application-slums/>

大约建于 1950 年至 1980 年的英国高层塔楼被誉为建筑奇迹——大型混凝土塔楼很容易容纳与它们所取代的较小房屋相同的人口。房间大，视野好，周围是开放空间，它们最初是受欢迎的住宅——低成本和未来主义。

但是，展望未来有时会有一个习惯，回来困扰你。

由于削减成本、不合标准的材料、苛刻的期限和仓促的施工实践，这些现代住房奇迹变成了当时的新贫民窟。通过在全国复制高楼，城镇规划者不知不觉地在各地复制了糟糕的设计。结果是:不受欢迎的住房和高犯罪率，导致贫民窟和城市衰败。甚至周围的空地也被忽视了，因为没有人拥有维护和监督的所有权。

在其中，我们有自己的设计和建筑灾难。

现有的 IT 应用程序和破旧的塔楼之间有许多相似之处。IT 整体很难扩展，需要昂贵的维护以避免年久失修。他们也很难对付警察，故意破坏和盗窃是一个持续的问题。再加上这种整合问题(这是无人监管的开放空间和通道的版本)，我们剩下的系统不足以满足现代数字业务的需求。

## 企业架构必须与时俱进

DevOps 专注于整个服务生命周期的运营和开发协作，现在被视为这些问题的答案——一种基于敏捷和精益原则的快速交付高质量数字服务的方法。这听起来很棒，但是我们不要忘记[企业架构](https://en.wikipedia.org/wiki/Enterprise_architecture) (EA)，因为如果没有它，我们可能仍然在建造 it 贫民窟——只是更多，更快。

当然，许多 DevOps 的忠实拥护者可能会争论(有一定的理由)繁重的 EA 实践和框架没有进化到与敏捷的步伐相匹配。迭代式开发意味着您开始的地方不一定是您结束的地方，这就需要从一成不变的架构设计过渡到不断发展的决策的流动组合。而且，如果 EA 不能适应，自治和自我管理的敏捷团队越来越多地被授权进行架构调用。

但是伟大的开发人员不一定是杰出的架构师；他们并不是天生如此。这意味着他们可以在没有架构指导的情况下沿着开发路径前进，或者在战术上做出基于团队的决策，从而损害程序级的目标。例如，支持三倍客户群和增加满意度分数的业务策略所需的可伸缩性和性能可能会丢失，因为开发短视地关注于交付更多的功能。

然而，我们不能只把责任归咎于开发商。企业架构师必须认识到，他们的过程(尤其是僵化和静态的过程)与日益软件驱动的业务愿景之间的任何不一致只会进一步孤立实践。

## 构建新的流体指南和原则

EA 在敏捷环境中的角色仍然存在争议，但是这不应该阻碍我们。通过使用架构师和流动的指导方针，我们可以保持交付的速度，同时防止混乱。当然，诀窍是限制架构过度工程化，同时为开发人员提供最小的 EA 集，以避免技术和架构债务。

即使在最小模式下，EA 仍然可以帮助开发人员快速确定在设计过程中应该考虑什么。其目的是指导开发人员理解成功的应用程序是由哪些体系结构方面组成的，更重要的是，新的思维方式如何支持更长久、更可持续的软件创新。

有趣的是，这些做法可以在“避免贫民窟”的背景下提出:

*   **避免不合标准或不受支持的材料**–正在使用的工具链可能包括商业软件和开源软件，但要小心任何不受支持的东西。正如维护高层建筑的成本达到了不可持续的水平，如果软件没有商业支持，尤其是在 IT 运营方面，也会给组织带来负担。此外，与开发部门合作，理解约束导致测试妥协的地方——“构造捷径”综合症，导致更多的缺陷和技术债务。

*   **永远不要使用新技术来解决老问题**-随着高层建筑的退化和破坏行为的增加，许多地方当局试图通过将“问题群体”安置在同一个街区来控制局面。但这只是增加了问题。企业架构师会犯同样的错误——例如，制定疯狂的法令，规定所有东西都必须容器化，甚至一些遗留应用程序；不理解运行时独立性只会延长问题应用程序的寿命；或者没有激励推动改进和清除现有的遗留 IT 贫民窟。

*   **监控和管理您的分包商—**无论您采用何种云模型，抽象出基础设施或应用程序堆栈都可以让开发人员专注于编码。这很好，但不要忘记将应用“PaaS-ing”到云并不意味着放弃应用性能和终端用户体验的所有权。为此，架构师必须充当云代理顾问——例如，努力确保任何云服务都提供开放的 API，以便将监控无缝集成到统一的解决方案中。

当然，用 DevOps 构建伟大的新数字服务只是答案的一部分。今天的创新可能会成为未来的遗产，许多新的应用程序也必须与现有系统集成。因此，架构必须涵盖两个基础:以最小模式工作，以确保快速构建高质量的服务，同时在需求指示和系统变化时应用标准和治理。

无论你的应用程序设计在纸上看起来有多好，糟糕的架构只是意味着建立更多有问题的系统，并且永远不会清理现有的贫民窟。