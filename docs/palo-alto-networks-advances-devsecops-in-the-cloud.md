# Palo Alto Networks 在云中推进 DevSecOps

> 原文：<https://devops.com/palo-alto-networks-advances-devsecops-in-the-cloud/>

Palo Alto Networks】更新了其 Prisma Cloud ,以便在云中部署工作负载时更容易采用最佳 DevSecOps 流程。

新功能包括定义网络安全策略并将其应用于持续集成(CI)和持续交付(CD)工作流的能力，以及用于发现云基础架构模板中错误配置的扫描工具，这是云安全问题最常见的来源。

Palo Alto Networks 还增加了在部署之前扫描 Amazon Web Services (AWS)本机虚拟机的功能，以及通过单击将策略应用于 AWS Lambda 无服务器计算框架上运行的工作负载的功能。该功能消除了在 AWS Lambda 框架上运行的应用程序代码中手动安装包装器的需要。

Palo Alto Networks 负责产品管理、容器和无服务器安全的副总裁 John Morello 表示，随着新冠肺炎疫情的到来，工作负载向云迁移的速度将会加快。部署应用程序使组织能够保持更高的灵活性，鉴于目前不确定新冠肺炎疫情会持续多长时间，甚至在最近的疫情得到控制后会卷土重来，这意味着组织需要能够从其 IT 员工所在的任何位置集中管理工作负载。

当然，特别擅长扫描云错误配置的网络罪犯也意识到了这一点。Morello 指出，因此，他们中的许多人将把未来的工作重点放在扫描驻留在公共云上的易受攻击的工作负载上。

Palo Alto Networks 的 Unit 42 研究部门最近发布的公共云配置分析发现，超过 199，000 个模板存在中度至高度漏洞。大多数漏洞是在使用 CloudFormation (42%)、Terraform (22%)和 Kubernetes 的 YAML(9%)创建的模板中发现的。

随着云计算环境变得越来越复杂，错误配置的机会只会增加，例如，端口保持打开。IT 组织越来越多地试图保护在基于虚拟机、Kubernetes 集群和无服务器计算框架的公共云服务上运行的各种应用程序工作负载。公共云计算环境假定网络安全的责任由云服务提供商和使用这些服务的 IT 团队共同承担。不幸的是，开发人员经常认为云服务提供商承担了比他们实际承担的更多的责任。大多数云服务提供商实际上只是承诺保护他们管理的基础设施。应用程序安全性的责任仍然牢牢掌握在部署云应用程序的 IT 团队手中。

为了应对这一挑战，许多组织已经采用了最佳 DevSecOps 流程，将网络安全责任进一步转移给开发人员。然而，为了实现这一目标，开发人员需要访问与 CI/CD 平台良好集成的工具，DevOps 团队依赖这些工具将代码推送到云平台。显然，这种转变代表了一种实质性的文化变革，需要时间才能在大多数组织中完全体现出来。但是，如果没有在现有 CI/CD 工作流环境中增强应用程序安全性所需的工具，就不可能实现这种改变。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)