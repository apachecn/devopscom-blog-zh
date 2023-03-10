# 实施 DevSecOps 时的 3 个必备条件

> 原文：<https://devops.com/3-must-haves-when-implementing-devsecops/>

DevSecOps 这个术语已经有十几年的历史了。devo PS——将软件开发与 IT 运营相结合以更快部署应用程序的实践——在 2008 年首次被[](https://www.coursehero.com/file/26635477/DevOPs-Notestxt/)创造，并在 2009 年一次历史性的 [会议陈述](https://www.youtube.com/watch?v=LdOe18KhtT4) 中得到完善。DevSecOps——在敏捷开发的每个阶段烘焙安全性，而不是在最后处理安全性的概念——紧随其后。

尽管围绕着 [DevSecOps](https://devops.com/?s=DevSecOps) 有大量的行业对话和活动，但很难说这场运动获得了多大的推动力。

在 Synopsys 网络安全研究中心 2020 年对全球 1，500 名 IT 专业人员进行的 [调查](https://news.synopsys.com/2020-12-08-Synopsys-Study-Shows-Open-Source-Security-Top-of-Mind-but-Patching-Too-Slow) 中，63%的人表示他们正在将至少一些 DevSecOps 活动整合到他们的开发管道中。然而,“至少有一些”表明一部分采纳者还没有完全接受 DevSecOps。那另外 37%的人呢，他们根本没有把它纳入其中。

尽管如此，两个因素表明 DevSecOps 在主流采用的道路上正开始越过一个临界点。

第一，攻击公司和政府机构的[](https://www.csis.org/programs/strategic-technologies-program/significant-cyber-incidents)数量惊人的网络攻击需要积极主动的方法来解决安全问题，这正是 DevSecOps 所做的。

第二，疫情一直是数字化倡议的强大催化剂。例如，根据 Gartner 的[](https://www.gartner.com/en/newsroom/press-releases/2021-04-21-gartner-forecasts-worldwide-public-cloud-end-user-spending-to-grow-23-percent-in-2021)预测，全球公共云服务支出预计将在 2021 年增长略高于 23%，从 2020 年的 2700 亿美元增至 3323 亿美元。除了对由新冠肺炎推动的技术 的更大依赖之外，诸如[集装箱化](https://containerjournal.com)和边缘计算等新兴技术的日益使用正在推动更高的云支出。所有这些都表明组织需要在现代软件开发生命周期中考虑安全风险。

DevSecOps 背后的逻辑是不可否认的。将安全性视为开发、运营和安全职能部门之间的共同协作责任，从尽可能早的阶段开始(这种方法被称为“左移”),而不是各自为政，这有助于以当今业务条件所需的速度和响应能力部署安全软件。

在更广泛的 DevOps 范式下成功整合了这三个功能的公司在软件开发和生产中享受到了从根本上减少的摩擦。这些组织可以更快、更安全地部署软件，减少设计缺陷、错误配置和其他可能导致安全问题的失误。

在发展合作之旅中走得不是很远的公司倾向于支持它的一些实践，但并不一致。笨重的线性瀑布方法随处可见。在生命周期的后期，漏洞管理仍然是一种被动的检查工作，迫使开发人员回溯并修复代码，而不是一个从设计到生产无缝集成的主动预防性过程。

更先进的组织通常关注三个关键因素来确保成功。

**1。教育。** DevSecOps 既是一种技术转变，也是一种文化转变。它需要一种新的思维方式，使开发人员能够在软件开发生命周期的开始就拥有创建安全代码的所有权。因此，IT 领导不能只是打个响指就指望 DevSecOps 站稳脚跟，而不对团队成员进行培训，让他们了解它为什么如此重要，以及它如何推动而不是破坏伟大的工作。

“组织学习和变革是开发运维蓬勃发展的关键，”Gartner 高级分析师乔治·斯帕福德 [写道](https://www.gartner.com/smarterwithgartner/the-secret-to-devops-success) 。“换句话说，与人相关的因素往往是最大的挑战，而不是技术。”

这意味着*在*将 DevSecOps 引入组织之前，重要的是将努力与它将带来的价值联系起来，并解释为什么它将允许企业向客户交付更多价值并提高其竞争力。

**2。** **流程。**正确的 DevSecOps 策略和过程可以决定一台敏捷的软件开发机器和一台仍然因效率低下而停滞不前的机器之间的差别。

例如，许多严重依赖扫描工具来检测漏洞的组织为它们的使用分配了无意义的策略。假设在将代码部署到生产环境之前，需要消除特定分数或类型的漏洞。但是如果缺陷存在于代码的不重要部分并且不可利用，该怎么办呢？

最好的 DevSecOps 计划包括寻求理解项目的整个环境(从设计到生产)的策略和过程，并以反映安全和法规遵从性需求的真实风险的方式处理一切，而不仅仅是通过同一管道运行所有代码。

3。 **明面上。**事实:如果没有正确的自动化工具来提供对代码的深入了解，DevSecOps 实现就没有机会。

为了实现 DevSecOps 承诺的协作和敏捷性的品质，组织应该倾向于开发工具，为开发人员提供他们做出更明智决策所需的所有相关信息。

这些工具必须真正简化将安全性添加到开发运维方法中的过程，方法是自动执行各种手动流程，这些手动流程通常会降低工作效率— 威胁模型、安全性和合规性审查、pentests 和风险评估等。这些工具不能只是从筒仓 — 中聚合数据，筒仓无法提供足够的上下文信息，并产生太多的误报—它们需要在功能请求、提交、拉取请求和 CI/CD 阶段为负担过重的团队提供整体救济，以保护应用程序。

通过记住这三个要素，组织可以实现 DevSecOps 作为真正的游戏规则改变者的潜力。随着 DevSecOps 继续跨越鸿沟走向更普遍的采用，组织可以向早期采用者寻求如何正确使用 DevSecOps 的指导。