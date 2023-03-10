# 2021 年持续交付的状态

> 原文：<https://devops.com/the-state-of-continuous-delivery-in-2021/>

DevOps 的标志之一是改进软件的交付。因此，成熟的 DevOps 系统采用连续交付(CD)，即定期发布小型软件变更的过程。在对[数字创新](https://devops.com/the-state-of-digital-innovation-one-year-into-the-pandemic/)的高需求中，简化这一发布渠道对于实现整体软件流动性变得越来越重要。

那么，CD 在如今的开发团队中是什么状态呢？[连续交付基金会(CDF)](https://cd.foundation/) 最近发布了其 2021 年[连续交付状况报告](https://cd.foundation/blog/2021/06/24/state-of-cd-report/)，这是一项帮助建立基线连续交付指标的研究。下面，我们将回顾报告中的一些关键要点，并发现部署频率、恢复时间和代码更改的平均交付时间等方面的平均比率。

## 连续交付(CD)的优势

在我们查看 CD 采用的广泛指标之前，让我们考虑一下:CD 的好处是什么？报告指出，CD 的一大净好处是它有助于在软件开发周期的早期实现反馈。一个精益的、CD 驱动的开发方法可以帮助快速发现不会成功的特性，从而避免浪费宝贵的开发资源。

CD 还提高了小软件块的整体交付速度。在一个[微服务架构](https://devops.com/how-to-use-microservices-to-evolve-devops-pipelines/)风靡一时的时代，这一过程对于持续启动许多不同的更新是必要的。例如，[网飞利用 Spinnaker](https://netflixtechblog.com/multi-cloud-continuous-delivery-with-spinnaker-report-now-available-6040ba83b765) 交付数百项微服务和数千项日常部署。

有了这些成果，组织可以获得更高的响应能力和敏捷性。CD 可以实现对变化的快速反馈，这可以帮助企业适应不可预见的情况，例如零日漏洞。根据该报告，对 CD 的投资也可以给开发者团队带来净收益。

## 连续交货统计

软件性能可以指示整个组织的性能。那么，一个组织应该如何衡量其软件交付的成功呢？嗯，Accelerate 这本书概述了四个需要关注的关键指标:变更的准备时间、部署频率、恢复服务的时间和变更失败率。CDF 报告确定了其中三种产品的当前行业平均水平。

在部署频率方面，研究发现，开发者每周发布一次到每月一次的比例最高(31.3%)。很大比例的开发者，27.3%，每个月到半年发布一次。只有 10.8%的开发者是精英执行者，每天发布多次。这表明跨组织的快速发布周期仍在不断成熟。

变革的平均准备时间比你想象的更加多变。28.3%的开发人员从提交代码到在生产中成功运行代码需要一周到一个月的时间。对于 27.3%的开发人员来说，这个交付时间增加了，从一个月增加到六个月。只有 5.74%的开发人员说它需要不到一个小时，这表明真正的按需交付机制在大多数组织中仍然遥不可及。

另一方面，在恢复服务方面，开发人员的行动要快得多。调查显示，34.4%的受访者表示，他们需要一个小时到一天的时间来应对计划外停机。相当多的人(15%)在不到一小时内对事件做出响应。尽管如此，大约 50%的异常值会在一天到六个月之间做出反应。

缩短平均恢复时间(MTTR)对于响应损坏的应用程序、快速解决[安全漏洞](https://devops.com/majority-of-orgs-lack-visibility-into-container-vulnerabilities/)以及满足[不断变化的客户期望](https://devops.com/digital-customer-experiences-the-future-is-modular/)是必不可少的。因此，MTTR 已经成为[站点可靠性工程师](https://devops.com/how-the-sre-role-is-evolving/) (SREs)密切关注的事实指标。

## 影响软件交付的因素

其他因素可能会影响软件交付的敏捷性，例如行业类型和编程语言偏好。在许多试图改进其交付模式的行业中，该报告强调零售业是速度和稳定性指标排名较高的行业。金融服务、政府和能源等其它行业在稳定性方面排名靠前，但在速度方面仅获得平均分。电信等行业的整体得分较低。

编程语言的选择也可能决定整个软件交付的性能。该研究发现，根据使用每种语言的组织的综合软件交付性能数据，shell 脚本语言、Go、JavaScript、PHP 和 Scala 是前五大编程语言。

## DevOps 旨在改进 CD

持续交付对于快速响应变化和实现新特性的迭代、[渐进交付](https://devops.com/maintaining-progressive-delivery-quality-with-feature-flags/)至关重要。

现代 CD 的另一个不可低估的方面是对开源工具的广泛流行和依赖。像[詹金斯](https://devops.com/cdf-officially-graduates-jenkins-ci-cd-platform/)、詹金斯 X、 [Spinnaker](https://devops.com/armory-looks-to-drive-enterprise-adoption-of-spinnaker/) 和 [Ortelius](https://devops.com/cd-foundation-welcomes-ortelius-open-source-microservices-management-platform-as-new-incubating-project/) 这样的 CDF 开源包对于众多开发团队实现 CD 过程仍然至关重要。

《2021 年持续交付状态报告》提供了跨公司和行业的标准持续交付实践的基准。这些发现是基于 SlashData 的开发者国家调查，该调查从 2020 年底到 2021 年初访问了来自 155 个国家的 19，000 多名受访者。缺少报告的一个领域是变更失败率，我们希望未来的研究能够以此为基准。要了解更多信息，您可以点击下载报告[。](https://cd.foundation/blog/2021/06/24/state-of-cd-report/)