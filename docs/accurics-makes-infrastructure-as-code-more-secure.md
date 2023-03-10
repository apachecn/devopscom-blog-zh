# Accurics 使基础设施代码更加安全

> 原文：<https://devops.com/accurics-makes-infrastructure-as-code-more-secure/>

刚刚筹集了 500 万美元的资金，Accurics today [推出了一个平台](https://www.businesswire.com/news/home/20200428005337/en/Accurics-Launches-Vision-Making-Cloud-Infrastructure-Security)，该平台分析用于管理基础设施的代码，作为漏洞和漂移指标的代码，以创建云应用程序工作负载的威胁模型，然后，如有必要，自动将云设置回滚到最近一次批准的状态。

Accurics 首席执行官 Sachin Aggarwal 表示，这家初创公司的平台不是简单地关注云基础设施，而是分析漏洞馈送、身份访问管理(IAM)权限和其他数据，以检测潜在的云安全问题。他说，然后可以与第三方安全工具共享该分析，以自动修复。

一旦构建了模型，Accurics 就会监控应用程序工作负载是否存在会带来风险的变化，并实时生成每个工作负载的拓扑，以识别偏离初始部署设置的任何潜在指标。如果漂移是由于合法的改变，则可以更新代码。他说，如果它引入了风险，it 团队可以使用 Accurics 已经嵌入其平台的“时间机器”功能，将代码回滚到最后一个已知的安全状态。

Accurics 平台采用了一种不同的方法来实现网络安全——它不仅仅关注云基础设施提供商提供的应用编程接口(API ),而是分析从用于以编程方式安装工作负载的 Terraform 代码到所采用的容器和无服务器计算框架的一切。Aggarwal 表示，Accurics 计划在未来增加与云环境中常用的其他基础设施的集成，包括 Jenkins、Bitbucket 和 GitLab 持续集成/持续交付(CI/CD)平台。

该分析基于安全运营中心(SOC) 2、通用数据保护规则(GDPR)、支付卡行业(PCI)、医疗保健信息便携性和责任(HIPAA)、国际标准化组织(ISO)、互联网安全中心(CIS)基准、亚马逊网络服务(AWS)最佳实践和 AWS 架构完善的框架，揭露违反常见合规性和网络安全实践的行为。

Aggarwal 表示，Accurics 使组织能够持续评估其云应用环境中的变化，从而推动了 DevSecOps 的发展。如今，大多数涉及云安全的问题都可以追溯到使用工具以编程方式配置云基础架构时出现的错误。他指出，Accurics 平台有助于开发人员和网络安全团队合作发现这些问题，并补充说，首要目标是让两个团队都能通过消除云计算环境中最常见的错误来降低风险。

随着开发运维团队和网络安全团队之间的关系不断发展，显然大多数组织在谈到云安全时需要解决的第一个问题是可见性。大多数 IT 团队关注云安全，并不是因为平台不如内部基础架构安全。总的来说，云基础设施更安全。然而，由于缺乏可见性，网络安全团队不容易发现错误配置何时会产生已知漏洞。如果这个问题得到解决，由安全问题产生的对云计算的抵制将会消失。