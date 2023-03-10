# 一切都与工具有关:生命周期安全性和测试

> 原文：<https://devops.com/all-about-tools-lifecycle-security-testing/>

在过去，每当一个新的应用程序或一个应用程序的新版本被推向市场，用户经常被滥用为安全性和可用性的 beta 测试者。这很大程度上是因为缺乏有效测试大型代码库的机会。

类似地，随后的补丁和新的应用程序版本都是在最少测试的情况下推出的，通常会修复现有的错误，但也会引入许多新的错误。因为用户不知道有替代品，所以勉强接受了这种情况，形成的共识是没有无 bug 软件这种东西。

今天的用户对 bug 的容忍度要低得多，尤其是当这些 bug 是托管应用程序中的安全漏洞时。如今，任何在线提供应用程序的人很少需要等很长时间，黑客就会检查这些弱点，对于供应商来说，这意味着他们自己网络的完整性受到威胁。例如，在电子商务应用程序或在线预订系统中找到这些安全弱点对黑客来说极具吸引力，因为他们有机会窃取身份或发布勒索软件，从而可能损害公司的可持续性。

黑客不仅仅针对应用程序中明显的漏洞。分布式拒绝服务(DDoS)攻击越来越多地针对应用程序，而不是网络基础设施，经常使应用程序对合法用户不可用。

开发人员需要确保他们理解安全性和负载测试在应用程序开发生命周期中的重要性。为了向市场提供更安全的产品，有必要确定开发的哪些方面可以利用安全缺陷，并在 C-suite 和 it 高管的时间和资金支持下解决这些挑战。

## 缺乏安全测试的时间

必须尽可能避免安全缺陷。这需要密集的测试和正确的工具。时间是宝贵的，上市时间通常是新应用程序成功的关键因素。对于 IT 决策者来说，有必要在这些安全问题和时间压力与组织的风险偏好及其资源分配之间进行平衡。

此外，IT 领导和开发人员需要考虑他们的安全测试的有效性和敏捷性。敏捷软件开发将软件发布的周期从几个月缩短到几天甚至几个小时。众所周知，用于故障排除的经典迭代、开发-测试-开发过程耗时太长，因此经常被忽视。因此，安全缺陷仍然经常出现在软件版本中，并且必须在以后消除，这使得成本更高。例如，根据国家标准和技术研究所(NIST)的数据，开发阶段每个缺陷的成本是 80 美元，但是在测试阶段每个缺陷的成本迅速上升到 960 美元，在生产阶段上升到 7，600 美元。NIST 估计，仅在美国，这些费用每年就高达近 600 亿美元。

开发人员普遍意识到安全测试面临越来越大的挑战。在最近 Ixia 对 363 名开发人员的调查中，很明显大多数受访者认为安全测试是开发周期中最重要的组成部分。事实上，93%的人报告说他们在开发过程的早期就对他们的应用程序进行了安全测试，并且持续不断。然而，三分之二的受访者承认他们交付的产品存在漏洞和/或安全缺陷。无论是因为缺少时间、合适的工具还是财务支持，这都会使应用程序的安全性和功能性以及组织的网络面临风险。随后，用补丁或更新来消除这些缺陷比在开发期间解决它们至少要贵四倍。

## 尽早、经常并在真实条件下进行测试

一系列全面的安全测试解决方案正在出现，以将安全测试与开发周期更紧密地集成在一起。这些解决方案为开发人员提供了强大而全面的测试环境，以仔细监控应用程序的行为，应对 DDoS 攻击、恶意流量和自动化攻击，从而让开发人员在编码阶段发现错误或漏洞。这些工具还为负载和安全测试生成真实的流量，以模拟各种协议组合和流量模式。此外，这些解决方案包括开发工具，如集成调试器，可以导入和重放记录的数据包捕获。

通过使用 REST APIs 和丰富的命令行界面，这些集成的安全性测试解决方案可以与一系列持续集成/持续部署(CI/CD)框架一起工作。这些敏捷 CI/CD 框架简化了在应用程序开发生命周期的不同阶段发现和解决问题的过程。

这些解决方案还通过一系列社区功能(如推荐、实时反馈和任务分配)简化了多功能团队内部的沟通和报告。使用完全虚拟化的解决方案还可以让开发人员改进整个应用生命周期的安全性测试，同时最大限度地减少任何硬件或基础设施投资。此外，敏捷 CI/CD 模型有助于服务提供商中的不同团队(QA、生产、开发和供应商)有效协作，并简化不同阶段发现的问题的发现和解决，从而加快上市时间。

在提高应用程序安全性的同时，提高开发团队的敏捷性和速度的能力正在引起许多 IT 决策者的关注。随着公司董事会要求 IT 部门更快、更有效地应对技术机遇，IT 领导们看到了这种结合了灵活性和安全性这两个优先事项的新工作方式的优势。

开发团队应该与 IT 主管进行清晰的沟通，以确保所需的时间、资金和资源，从而确保新的应用程序和更新在发布到市场上面对黑客的攻击之前经过严格和现实的测试。使用商业工具和系统进行安全性和负载测试有助于确定应用程序在不同压力负载下的行为。它们还帮助开发人员以更具成本效益、及时和敏捷的方式向市场交付产品。

## 关于作者/菲尔·特雷纳

![Phil Trainor headshot](img/7398bf7e6c8c015b518c6a4248886864.png) Phil Trainor 是 [Ixia](https://www.ixiacom.com/) 的 APAC 安全业务主管。Phil 在网络安全行业工作了 14 年，在加州的初创公司担任高级工程职位。他最近在滨海湾金沙举行的 2016 年 RSA 大会上担任客座讲师，讨论“高级持续威胁”，并在 Blackhat、DefCon、ToorCon 和许多其他著名的安全活动上发表演讲。在 [LinkedIn](https://sg.linkedin.com/in/phtrainor) 上与他联系。