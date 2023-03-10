# DevOps 101 的安全策略

> 原文：<https://devops.com/security-policies-for-devops-101/>

不久前，我和一些朋友讨论了如何在 devops 环境中确保安全性。第一个简单的想法是，不，DevOps 说哪里可以取消安全性。相反，考虑在 DevOps 给工作环境带来变化的情况下，您现有的信息安全实践和策略需要如何调整。经验丰富的安全专业人员知道，许多安全实践始于策略。此外，任何政策都不是一成不变的。未能至少每年更新政策和程序已经是一个灾难的处方。

我告诉很多人回想 iPhone 首次推出的时候。IT 组织中的安全专业人员的自然倾向是 1)简单地忽略该设备，或者 2)建立一种完全拒绝的策略。两个选项都不是正确答案。我可以直接说，我是这种隧道决策的受害者。我们更新了我们的移动设备政策，明确提出了“没有 iPhone 给你…两年后再来”的原则。我抵挡 iOS 设备的微弱尝试持续了大概一年。与此同时，办公室里的许多人被看到手里拿着 iPhones，他们不断地说着“但我不是在工作中使用它”之类的话。我和他们都断然否认。

归根结底，政策是为了适应不断变化的环境而改变的。DevOps 也不例外。

## 最低要求

就像在开发中我们谈论最小可行产品一样，我们可以将相同的概念应用于实现安全实践。首先，确保你的组织已经起草了一些政策，并得到了执行人员的同意和批准。任何组织需要的最低限度的一套政策应包括:网络或因特网安全、计算机安全、信息和知识产权安全政策；安全软件开发政策和程序。

### 成为冠军

但是这项工作并不仅限于政策制定。即使您的高管同意这些政策，也不意味着他们会被您的 DevOps 团队遵守或理解。

我经常与安全主管交谈，告诉他们需要离开座位，与公司的所有员工交谈。首先要进行的对话之一是开始支持安全策略。确保人们理解这些政策，更重要的是理解选择这些政策的原因。

你还记得上高中时被告知你必须遵守一条你认为完全愚蠢的规则吗？非安全人士可能会对愚蠢的政策有同样的想法，甚至可能会故意反对它们。冠军需要教授并实践这些政策。当有人质疑这些政策时，花时间与他们进行双向对话。在你试图把你愚蠢的安全理念强加给他们之前，确保你首先理解他们的观点。

## 泰勒你的政策

虽然在线提供的策略模板(如 San 中提供的模板)是一个很好的起点，但不要照原样将它们放在内部网中。阅读它们并根据你的公司、你的文化和你的开发实践进行调整。更好的是，包括特定于云和开发运维的策略。

定制的一个开始领域是为特定的云供应商创建策略。例如，考虑围绕公司应该如何使用亚马逊的 IAM 功能制定政策。围绕如何配置和使用 IAM 用户和组制定具体的策略。使用最小特权原则，设计合理的访问控制策略。考虑这样一个策略，其中只有几个受信任的用户拥有完全的管理访问权限，其他用户属于超级用户组，他们可以启动实例，但不能改变 AWS 控制台配置或访问权限。您可能希望授予您的会计团队对控制台的有限访问权限，以便查看计费和使用情况。同时，围绕云 API 密钥的使用、分发和存储制定具体的策略。此外，考虑实施双因素身份认证。这些特定的用例策略对于安全团队获得 DevOps 团队的信任大有帮助。

DevOps 可能是正在各种组织中掀起波澜的酷新热点，但这并不意味着我们可以在 DevOps 环境中忘记我们的信息安全要求。确保 DevOps 组织遵循良好的安全实践的起点之一是从一组最基本的安全策略开始。请确保您支持这些策略，并根据您的特定组织和使用情形对它们进行定制。只要有一点运气和决心，即使您的 DevOps 团队也可以遵循安全性最佳实践。