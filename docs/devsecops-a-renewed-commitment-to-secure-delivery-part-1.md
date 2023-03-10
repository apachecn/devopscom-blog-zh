# DevSecOps:对安全交付的新承诺，第 1 部分

> 原文：<https://devops.com/devsecops-a-renewed-commitment-to-secure-delivery-part-1/>

安全从来没有像今天这样重要，因为公司担心他们会成为下一个头条新闻，下一个数据泄露的受害者。高管们还担心应用程序是否符合高标准的合规性——无论是符合全球法规，如 [GDPR](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation) ，面向国家的隐私法，还是涵盖金融、医疗保健、能源和其他行业的许多具体法规。

即使是为了增加安全性，在一个长期的软件开发生命周期中引入新的工具和过程也是一个挑战。这就是为什么公司需要首先仔细审查他们的开发和生产流程，以充分了解他们如何创建和发布软件，然后才能有效地将安全性集成到 DevOps 中。

可以说，应用交付的重建使公司能够后退一步，智能地更新他们的管道，以便在新的安全开发运维流程中最大限度地减少人工干预或机器中断。让 IT 安全作为利益相关者参与定义 DevOps 发布管道中的治理也是至关重要的。只有这样,“Sec”才能很好地适应 DevSecOps。在这个由两部分组成的系列中，我们将研究构成一个良好的 DevSecOps 管道的三个关键组件。它们很容易记住:流程、人员和工具。

## **漏洞呼唤对安全的狂热关注**

尽管微服务、容器和云原生架构使公司能够比以往更灵活、更快速地创建和交付应用，但许多这些创新技术也增加了产品中出现安全缺陷和漏洞的可能性。应用程序以更小的容器化部署单元以更高的频率和更高的数量发布，相对于在封闭的整体 Java 应用程序上进行的开发，暴露的风险要大得多。

例如，来自公共集装箱登记处的图像的出处可能会受到损害，从而成为开发中的潜在暴露点。同样，开源软件的激增也是如此，它们经常被用作库和依赖项。GitHub 等长期使用的工具促进了共享和开放社区的发展，有时会给那些向公共存储库发布敏感数据的贡献者带来严重后果。有多少次我们听说密码被推到公共回购上让全世界看到？

考虑到所有这些因素以及如此多的风险，公司现在疯狂地关注保护开发运维。但在他们正式考虑安全性之前，他们应该首先审查员工责任、组织责任、交付实践、治理以及数字产品设计、开发和交付的其他方面。对于正在向云原生平台和技术进行现代化的企业来说，这可能是重新审视和更新方法的大好时机。

DevSecOps 确实与人员、流程和工具有关。充分理解这三点，您就可以构建一个安全的交付流程，在 DevOps 中产生信任和信心。信任和信心培养责任感和数字声誉是每个人的责任的观念。

## **确定释放管道的流程**

在这里，它是关于巩固一个正式的过程治理，一个应用程序从一个点移动到另一个点背后的所有步骤。代码如何从本地开发和测试过渡到生产站——以及其间发生了什么？这是过去朴素的道德观念的一个基本原则。

在云原生管道中有一些值得注意的事项。例如，提升路径可以用 Kubernetes 名称空间和集群来描述(而不是过去的裸机服务器或 VM 环境)。另一种现代的 [DevOps](https://devops.com/implementing-devops-goes-beyond-technology/) 方法是将 DevOps 原则应用于应用程序和环境配置工件。也称为 GitOps，它将版本控制、访问管理和生命周期流程应用于 yaml 文件、掌舵图、监控脚本和其他主要与运营相关的工件。将开发运维扩展到运营(或 GitOps)可以降低环境错误配置和配置漂移的风险，这是一个额外的好处。在这方面，安全性是通过环境合规性来解决的。

目标是证明发布渠道中发生的一切。检查步骤的附加值，并使它们与它们试图缓解的安全风险相一致。下面是一些例子:

*   单元测试必须通过发布管道的构建阶段，以降低非工作代码被推到开发环境并进入提升路径的风险。
*   在上线之前，必须对所有 Docker 映像进行漏洞扫描，以降低在生产中引入安全缺陷或漏洞的风险。
*   所有 API 接口必须有一个 Swagger 定义和一组在构建阶段运行的相应契约/合同测试，以降低集成缺陷和相应中断的风险。

## **寻找答案，记录一切，包括安全性**

通过询问一切，答案将会揭示什么在安全镜头之下，什么在躲避它。最终，您希望记录实践和过程，以便它们被整理成文，并受到流程中每个人的尊敬。IT 安全应该在会议中占有一席之地(与开发、运营、产品负责人、QA 一起)，并且在检查发布渠道时拥有同等重要的发言权。敏捷的核心价值是对发布渠道采用以产品为中心的方法。在考虑交付速度的同时，涉及 IT 安全将为管道带来健康的风险缓解措施。

但那只是过程。正如我们将在本系列的第二部分中探讨的那样，人和工具也会产生影响。

— [安德里亚·克劳福德](https://devops.com/author/andrea-c-crawford/)