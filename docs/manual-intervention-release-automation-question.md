# 人工干预还是发布自动化？这是一个问题

> 原文：<https://devops.com/manual-intervention-release-automation-question/>

当谈到发射核武器时，有各种各样的步骤和各种各样的故障安全机制，都是为了确保那些按下按钮的人真的想做核发射系统设计要做的事情。

我担心把核战争等同于发布代码是某种迷你戈德温式的争论，但是请耐心听我说，因为我们确实会说，“那核化了系统！”当事情变得糟糕透顶时，我愿意提出论点。

DevOps 社区中的一些人——尤其是 ARA 社区中的更多人——希望您自动化开发和发布之间的每个步骤。虽然我完全理解这种心态，但肯定有一些应用程序你不想在没有人说“是的，这是真正准备好了”的情况下上线，就像你不想在没有总统(在美国)说“是的，我们真的打算这么做”的情况下发射核武器一样。

## 有一点点

我的一个同事指出了“消除人工干预”的明显谬误:基础设施作为代码和代码本身都是人工的。发布的最大瓶颈其实还是在创造东西。所以告诉人们不要在过程的关键时刻插入偶尔的理智检查是有点…愚蠢的。

## 有时需要人工干预

举个简单的例子。你希望核电站在没有最终审查和批准的情况下发布新的控制代码吗？没有吗？那么，如果您的应用程序是您的面包篮，或者甚至对业务有重大影响，为什么您希望代码在没有人工批准的情况下发布呢？你不应该。DevOps 圈子里的信念是，任何事情都是可以恢复的，速度就是一切，这种信念有一种内在的自毁机制。如果你发布了应用程序，而你的客户失去了使用你的应用程序的能力，那么钟摆就会产生混乱。

只需对批准流程进行优先级排序，并使流程按下按钮，即“是的，我们准备好了”，授权人员可以按下按钮并完成部署。我们谈论的是在运行最良好的环境中的几分钟，以及在更复杂、不太彻底的环境中的几天(悲观估计，几周)。这不是一项巨大的投资，它是 CI/CD 之外的一步，真正影响的只是发布自动化。大多数企业级公司不会一天部署无数次，所以这不会成为瓶颈。

简而言之，放松我们所容忍的，减少短期目标和自动化开发/测试/部署环境的大部分都是很大的进步。但是，在决定未经批准就发布出去是否是一个好主意之前，先看看你的业务，确定给定的应用程序可能对你的业务产生什么影响，以及自动化的状态。不管专家们怎么说，事实往往并非如此。但也经常是这样。我不想给人留下我反对全过程自动化的印象；当组织的生存岌岌可危，解决方案非常复杂时，我只是赞成获得批准。

## 寻求平衡

像往常一样，你必须问自己，谁更了解你的业务和你的业务系统，专家还是你？这里有一个平衡；专家们有一些伟大的想法，但企业有平衡的需求。

随着自动化的不断发展，发布前需要审批的应用数量无疑会继续减少，但不要让这种时尚影响你的底线。DevOps 不是关于它自己，而是关于业务及其需求。

唐·麦克维蒂