# 更好的应用和更好的安全性

> 原文：<https://devops.com/better-apps-and-better-security-when-you-shift-left/>

4 月底，数万人和数百家网络安全供应商齐聚旧金山。虽然 RSA 大会是主要亮点，但本周还有许多外围活动，如云安全联盟峰会、CIO/CISO 交流会、BSides San Francisco 和 Qualys Security Conference。

我参加了一些 Qualys 安全会议(T1 ),并有机会在 T2 见到了 Qualys 产品管理安全解决方案架构师 Alex mander nack(T3 ),他讲述了网络安全需要左移的问题。

Mandernack 概述了当今组织在安全方面面临的一些问题。迁移到云并接受 DevOps 文化意味着更短暂、更有弹性的环境和压缩的开发时间框架。他指出，这些趋势使安全性更具挑战性，但也描述了它们带来的改变我们的方法以简化和提高安全性的机会。

## 传统管道被打破了

传统的应用程序开发模型更加线性。每个应用团队都建立了自己的形象——通常是在与其他团队隔离的孤岛或真空中。渗透测试偶尔或不经常进行，最终部署应用程序。漏洞扫描在生产中的应用程序上运行，问题或缺陷被报告给开发人员，以解决或纳入下一个版本。

这个过程既慢又麻烦。它也有可能带来浪费资源和降低组织效率的冗余。随着公司采用 DevOps 并转向云，传统的开发渠道根本不起作用——尤其是在安全性方面。

## DevOps、云和容器——天哪！

云和 DevOps 从根本上改变了开发生命周期。开发时间框架被压缩了，这个过程是一个自我反馈、迭代的循环，而不是重复的线性方法。在部署应用程序后识别和解决安全问题的传统方法在 DevOps 环境中不起作用，因为当问题被识别和解决时，应用程序本身可能已经转移到下一个版本。

网络安全和开发管道在云和 DevOps 方面面临着足够多的挑战，但还有一种更新的技术趋势加剧了这一问题——容器。容器被设计成快速获取代码和快速操作。它们也是为可伸缩性而构建的——不断产生和减少成百上千个容器，以跟上需求的步伐。

有各种各样的工具和平台与云、DevOps 和容器相关联。组织经常使用一个复杂的集合，包括 AWS、Azure、Docker、Kubernetes、OpenShift 和其他的一些组合。当涉及到安全性时，其结果可能会很快变成一个黑洞—这就是为什么将安全性留在 CI/CD 管道中很重要。

## 向左移动以帮助安全团队做得更好

在 DevOps 文化中，开发人员和安全团队需要尽快考虑安全问题。尽早将安全工具引入流程非常重要。幸运的是，借助 DevOps 生命周期和 DevOps 环境中常用的工具，这是可以做到的。

首先，公司应该建立黄金形象。开发人员不应该在开始开发之前就修补和更新基础操作系统。黄金映像采用 Ubuntu 或 CentOS 等基准操作系统，并对其进行完全修补和配置，以便每个人都有一个标准、一致的映像来开发。

有了黄金映像，向左转移安全性的下一步是在 CI/CD 管道中实现测试和扫描。将漏洞信息放在开发人员的手边，在管道中开发和实施漏洞门，以确保不符合策略和最低要求的应用程序不会被部署。

## 安全团队的新角色

安全性左移的一部分包括为 DevOps 团队提供使安全性自助服务的工具。通过脚本、API 和 CI 插件自动执行操作可确保安全性得到简化，从而为开发人员提供价值。

在这种左移的情况下，安全团队必须重新定义其在流程中的角色。安全团队仍然是至关重要的，但是安全的角色不是开发过程中的警察或路障，而是集中于验证和审计过程。安全框架应该具有仪表板和实时数据，使安全团队能够监控活动并识别可能需要进一步关注的趋势。

## 更好的安全性，更快

开发人员和安全团队之间经常会有冲突，但不需要这样。曼德纳克强调，开发者也不想创建不安全的应用。

将安全性转移到 CI/CD 管道简化了整个流程。最终，结果是更高质量、更安全、开发速度更快的应用程序。

托尼·布拉德利