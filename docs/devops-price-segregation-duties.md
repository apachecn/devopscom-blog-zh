# 职责分离的代价。

> 原文：<https://devops.com/devops-price-segregation-duties/>

职责分工将会改变，因为它必须改变。这对我们的动机、上市时间和 It 安全性有着巨大的影响。它影响组织的许多部分。大多数组织都是从开发运维、持续交付和持续部署开始的，因此很自然会想到职责分离以及我们今天如何处理它。今天，它花费了我们一大笔钱，而我们不愿意在不久的将来支付。我们为什么要这样做？

## 开发人员对职责分离的看法。

[![Sven Malvik - DevOps Consultant from Oslo/Norway](img/d9846db12fea5e98239d383980c9eb85.png)](http://sven.malvik.de/blog)

Sven Malvik – Sopra Steria – DevOps Consultant from Oslo/Norway

作为父母，我们看着孩子长大。我们看着孩子做的每一件事，这样我们就不会错过任何东西。生命中最伟大的时刻之一是当他们自己迈出第一步的时候。我们感到自豪和幸福。保护他们并帮助他们成为伟大的成年人是我们的工作和责任，100%。

作为一名开发人员，我们对自己的应用程序感觉非常相似。当我们将应用程序的第一个版本发布到产品中时，我们就像父母和孩子一样感到自豪和幸福。我们的工作和责任是保持应用程序正常运行，并维护它，确保我们的应用程序始终提供 70%的价值。什么？

这个数字是虚构的，但可能与事实相差不远。在许多大型组织中，不可能 100%负责并完全拥有我们自己的应用程序，即使我们应该并且真的想这样做。我们称之为“职责分离”。IT 安全确保没有一个人可以独自完成从开发到生产的所有工作。职责分离增强了防范欺诈和错误的能力，是内部控制的一个关键概念。但它也会给组织带来很多危害。职责的分离会剥夺人们的动力，会让我们沮丧，有时会生气。

你熟悉帕累托原理吗？它说 20%的员工做了 80%的工作，而剩下的 80%的员工只做了 20%的工作。想象你是那 20%真正完成工作的人之一。想象一下，你正在把东西拿出来，并向客户、业务和 IT 部门交付价值，因为你被 100%地信任和赋予责任。

我曾多次参与解决生产问题的任务组。在其中一个任务组中，我们有来自开发、安全、运营、基础架构和变更管理等不同部门的 12 个人。立即找到了根本原因。一个修补程序在变更管理批准后立即发布到生产环境中。从修补程序准备好到我们实际发布到生产之间的时间持续了 2 小时 5 分钟。我们没有从运营团队获得合适的资源，而运营团队是被允许做这项工作的。花了 125 分钟从运营部门找到有权访问生产系统的合适人员，并教会该人员如何进行部署。部署是 Jenkins 的工作，需要 3 分钟。125 分钟 x 12 个人= 25 小时，我们浪费了这些时间，因为我们将职责划分得非常严格。不是所有的资源都可以在任何时候获得，我也不认为这是可能的。

我希望了解他们的应用程序的开发人员变得更加聪明，并负责在所有环境中运行他们的应用程序。一切能有多快？上市时间可以缩短许多倍。动力会直冲云霄。

如果我们希望开发团队对他们自己的工作承担 100%的责任，我们必须把责任明确地放在那里，并对他们表现出 100%的信任。开发人员想要关心，但他们就是不能。

Ron Westrum 在安全文化方面的工作表明，没有任何流程或控制可以弥补人们不关心客户和组织成果的环境。除了创建控件，解决方案可以是创建一种文化，在这种文化中，开发人员对他们的行为后果负责，实际上有一个简单的方法来实现这一点。

1.  你建造它，你经营它。构建新产品和服务的团队必须对这些服务的操作和支持负责。
2.  将中央 IT 转变为产品开发组织。

员工是公司最有价值的资产，应该被信任来完成他们的工作。高度信任的组织文化应该受到青睐，而不是矛盾的命令和控制文化。

## IT 安全部门对职责分离的看法。

最近，我和一位在 IT 安全部门工作的人聊了聊。他喜欢职责分离。“合规和稳定是赢得客户信任的关键”是他的口头禅。“在满足法律合规性要求的同时，将尽可能减少对日常运营的干扰，访问控制是一种简单而高效的职责分离方法。但这是以灵活性为代价的。当通过访问控制机制实施职责分离时，重要的是要遵循关于什么角色允许什么类型的访问的指导原则，以便不仅合规，而且保护系统和数据并维护运营稳定性、完整性和机密性”。他对自己的工作真的很认真，什么都好。安全是一项具有挑战性的艰苦工作。

想象一下，我们的系统将生活在一个锁着的盒子里，真的一切都将自动化。一切正常，我们不需要讨论 IT 安全、访问控制和职责划分。可能有一种方法——德沃普斯方法。

## DevOps 如何处理职责分离？

追求敏捷与实施更强的访问控制，开发工作与职责分离——我们有两个相互冲突的计划吗？这取决于组织和自动化交付的进展，以及如何将变更发布到生产中。

想象一下，在客户服务报告了一个非常严重的错误后 10 分钟，您将一个紧急修补程序提交到公共源代码库中。想象一下，根据修补程序发布的速度，您可以调整您的更改发布的速度，跳过一些非功能性测试。5 分钟后，您的修补程序发布就绪。IT 业务打开组织的生产发布仪表板，在那里可以找到您的更改。从现在开始，他们所要做的就是按下屏幕上的一个绿色大按钮。2 分钟后，最终测试将决定您的紧急修复程序是继续生产，还是启动自动回滚程序。

不幸的是，在许多较大的组织中，这种情况仍然与现实相差甚远。我曾经是一个 12 人工作小组的成员，在那里我们有一个紧急修复程序，准备在发现路由原因 10 分钟后发布。但是我们没有绿色的大按钮。我们也没有在出现故障时自动回滚的例程。我们做的是詹金斯的工作，没人知道那份工作在哪里。我们 IT 运营部门的人员维护着数百个 Jenkins 职位，而当时唯一有空并且能够访问生产部门 Jenkins 仪表板的人不知道该职位在哪里。时间一分一秒地过去，在超过 10 到 20 个小时后，我们把补丁发给了抱怨糟糕的客户服务的客户。12 个人花了 120 多分钟做出了一个重要的改变。詹金斯的工作花了 24 小时，太疯狂了。

## 结论

我认为 DevOps 是一种放松职责分离，但保持 IT 安全并使组织变得前所未有的强大的方法。简单是真正力量的最终关键。更多关于 [http://DevOps。城镇](http://DevOps.Town)

[/Sven mal vik–devo PS 顾问](http://sven.malvik.de/)