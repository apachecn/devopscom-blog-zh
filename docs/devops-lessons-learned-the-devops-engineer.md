# DevOps 经验教训——“devo PS 工程师”

> 原文：<https://devops.com/devops-lessons-learned-the-devops-engineer/>

早在 2008 年，我是一家初创公司的成员，这家公司取得了成功，三年后被卖给了一家大公司。在创业初期，我们有三个人，外加一个负责网站开发的离岸团队。三个核心资源拥有从 API 开始的所有东西，而离岸团队拥有前端。由于我们很小，我们每个人都拥有自己的架构部分，并且管理系统的部署和操作，很少出现问题。一旦我们被收购，我们的世界就彻底改变了。

我们的团队很快增加到 20 多人，而我最初的两个架构师很快离开去了更好的地方。现在我们有更多的人参与到这个过程中，而且没有一个是领域专家。随着服务器蔓延开始蔓延，部署变得越来越具有挑战性且容易出错，事情很快开始失控。我们雇佣了第一个“DevOps”来帮助我们控制这一切。然后事情变得很糟糕。对于那些关注我的 DevOps 文章和我的狂言“[不，你不是 DevOps 工程师](http://www.virtualizationpractice.com/devops-engineer-25120/)”的人来说，我将要描述的是我在 DevOps 上的立场的基础。

**DevOps 作为一个角色:失败模式**

我们从未打算创建一个 DevOps 筒仓或位置。我们只是想要一个具有云和自动化专业知识的人，因为团队中的其他人都是开发人员，他们中的许多人对云和平台都是陌生的。无意中，这个人被贴上了 DevOps 的标签，他很快就和其他三个人一起加入了 DevOps 官方团队。我们现在自豪地拥有了一个新的筒仓，它成了新的瓶颈。

DevOps 团队忙着重新控制环境。权限必须收回，以防止服务器继续蔓延。开发团队现在必须向 DevOps 团队请求环境。当我们还是一家初创公司时，这很容易，也很容易管理。随着团队越来越大，同时运行的项目越来越多，这变得越来越具有挑战性。DevOps 的人忙于满足需求，以至于他们并不总是与不同项目的目标和可交付成果保持一致。应用程序开发团队太专注于“敏捷”了，以至于他们没有在项目的早期就让开发人员参与进来。

DevOps 团队变得过度劳累。他们负责监控和操作系统，他们被从可交付产品中抽出来以供应环境，他们试图对一个经历了从 3 人创始人团队到 20 多人新人团队的突然增长的平台进行控制。更糟糕的是，我们知道我们想要做什么来解决这些问题，但是一天中没有足够的时间来完成。我们已经制定了一个完整的持续集成和交付策略，但是我们没有足够的时间来关注它。

DevOps 开始受到应用程序开发团队的指责，因为在及时调配环境方面经常出现延迟。我们在开发、QA 和 stage 之间遇到了环境问题，因为应用程序开发团队没有及时沟通环境要求，而且不同的应用程序开发团队也不一致(例如，不同版本的 Python 和不同的库)。

所有这些都导致了来自企业的挫败感，尤其是来自创业公司并习惯于高质量的频繁部署的业务人员。

**吸取的教训**

最终，该团队扭转了这一局面。虽然他们仍然有一个官方的 DevOps 团队，但该团队与应用程序开发团队的合作更加密切。现在，环境已经实现了高级别的标准化。团队在项目生命周期的早期共享操作需求，开发人员帮助创建环境。这里学到的教训是，创建 DevOps 角色或组织不是正确的方法。创建新的筒仓只会制造新的瓶颈。DevOps 不是一个角色，而是一种将高质量、可靠的软件更快推向市场的方式。一个组织越早认识到这一点，他们就能越早达到成功的状态。