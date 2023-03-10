# 报告将云安全问题归咎于有缺陷的开发运维流程

> 原文：<https://devops.com/report-pins-cloud-security-woes-on-flawed-devops-processes/>

到目前为止，很明显，大部分涉及云平台的安全事件都围绕着某种类型的配置问题。Palo Alto Networks 的 Unit 42 研究部门今天发布的对这些云配置的分析表明,[该问题的根本原因很可能是](https://www.prnewswire.com/news-releases/palo-alto-networks-report-finds-poor-security-hygiene-leads-to-escalating-cloud-vulnerabilities-300999159.html)许多开发人员和 DevOps 团队用来配置云基础架构的模板。事实上，根据 Unit 42 的分析，超过 199，000 个模板在公共云上使用时存在中高漏洞。

Palo Alto Networks 公共云首席安全官 Matt Chiodi 表示，这个问题源于组织现在希望能够在公共云上部署应用程序的速度。模板[极大地加快了进程](https://devops.com/implementing-devops-goes-beyond-technology/)，但这些模板中很少经过网络安全团队的审查。

根据该报告，最常用的模板是使用 Kubernetes (39%)、Terraform 和 CloudFormation (24%)实例上的 YAML 文件创建的。大多数漏洞是在使用 CloudFormation (42%)、Terraform (22%)和 Kubernetes 的 YAML(9%)创建的模板中发现的。

Chiodi 指出，大多数模板都是通过简单的三步开发运维流程创建的:设计、编码和部署。不幸的是，在匆忙部署的过程中，大多数 DevOps 团队忘记了扫描漏洞问题。因此，Chiodi 表示，网络犯罪分子已经非常善于抽取云资源，以足够低的消费率挖掘加密货币，从而不被许多 IT 组织注意到。

报告中提到的其他重大云安全问题包括，43%的云数据库没有加密，60%的云存储系统禁用了日志记录，Chiodi 指出，这使得人们无法知道这些系统是否受到了威胁。此外，该报告发现 76%的云工作负载暴露 SSH(端口 22)，而 69%的组织暴露 RDP(端口 3389)，27%的组织使用过时版本的传输层安全性。

Chioti 说，总的来说，现在的目标是让 DevOps 团队尽可能简单地做正确的网络安全事情。

Unit 42 研究人员采用了公开可用的 GitHub 搜索应用程序编程接口(API)来查找 AWS CloudFormation 文件、Kubernetes YAML 文件和 HashiCorp Terraform 文件。然后，数十万个模板被下载，并由 Prisma Cloud infra structure-as-code(IaC)扫描仪进行分析，以识别不安全的配置。每个 IaC 文件也被发送到 IaC 资源检查器，以分析模板中使用的云资源。研究人员还使用 Palo Alto Network 专有的 AutoFocus 和 Wildfire 工具，通过使用定制工具集(恶意软件样本)来识别和调查网络犯罪集团。对这些样本进行了动态和静态分析，以确保发现危害迹象。

Unit 42 的研究清楚地表明，在云时代采用最佳 DevSecOps 流程还有很大的改进空间。然而，挑战可能与可用的工具没有太大关系。相反，似乎造成最大损害的是缺乏一套结构化的流程，开发运维团队和网络安全专业人员可以通过这些流程进行协作。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)