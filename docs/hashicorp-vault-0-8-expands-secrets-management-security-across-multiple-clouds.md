# HashiCorp Vault 0.8 扩展了跨多个云的机密管理和安全性

> 原文：<https://devops.com/hashicorp-vault-0-8-expands-secrets-management-security-across-multiple-clouds/>

加利福尼亚州旧金山—(market wired—2017 年 8 月 9 日)—云基础设施自动化领域的领导者 HashiCorp 今天发布了 HashiCorp Vault 0.8，其中包括对开源和企业版的重大更新，包括新的安全插件、灾难恢复、装载过滤复制功能和多因素身份验证(MFA)。

全球 2000 强企业广泛使用 Vault 来应对分布式环境中基础架构和应用程序安全性的挑战。Vault 开源产品解决了机密管理、加密即服务和特权访问管理的核心安全使用案例。Vault Enterprise 使团队和组织能够通过协作和操作功能简化 Vault 的使用，提供治理功能，并跨多个数据中心扩展 Vault。

0.8 版 Vault 开源版本的一个重要新增功能是:

*   **安全插件:**安全插件使个人和组织能够集成定制的认证后端和工作流。这使得为整个社区创作插件更加容易，也使得 Vault Enterprise 用户可以创建和集成自定义后端。

Vault Enterprise 0.8 包括改进操作、安全工作流程和多数据中心控制的功能:

*   **灾难恢复:**一种新的复制模式，允许复制令牌和租用凭据以及机密和策略，并优先考虑从停机状态快速恢复的能力，而不必为访问机密的应用程序/用户重新生成令牌。
*   **装载过滤复制:**装载过滤器是 Vault Enterprise 0.7 中发布的 Vault Replication 性能模式的新增功能，它只允许将选定的机密和身份验证装载从主服务器复制到辅助服务器。这对于管理由数据主权、治理、风险管理和法规遵从性管理的机密至关重要。
*   **多因素认证(MFA):** 全新的 MFA 子系统允许在 Vault 内的认证路径上的任何操作都需要 Duo Push、Okta Push 和基于时间的一次性密码(TOTP) MFA 方法。

“以前版本的 Vault Enterprise 引入了多数据中心复制，这使我们的许多企业客户能够采用或扩展他们对 Vault 的使用。HashiCorp 的联合创始人兼首席技术官 Armon Dadgar 表示:“新版本使多数据中心功能更加丰富，并为最关键的任务使用案例增加了灾难恢复复制功能。“此外，我们还添加了一个安全插件机制，允许用户和客户在 Vault 上进行创新，并在它提供的安全基础上进行构建。”

Adobe 的安全工程师 Chandler Allphin 表示:“一年多以前，Adobe 开始部署 HashiCorp Vault，并迅速成为我们大规模、分布式、混合云环境的一个基本特征。“原生插件系统只是工程师们兴奋地在新的 0.8 版本中利用的部分之一。通过增加灾难恢复功能，Vault 使我们能够扩展在分布式基础架构中处理容错和复制的方式。”

**附加资源**

*   [HashiCorp Vault 0.8 博客](https://www.hashicorp.com/blog/vault-0-8/)
*   HashiCorp 和 Adobe 网络研讨会重播，7 月 25 日:[在混合云环境中大规模解决安全性问题](https://www.youtube.com/watch?v=AkyVTrhHcQA)
*   [HashiCorp 金库网页](https://www.hashicorp.com/products/vault/)

**可用性** HashiCorp Vault 0.8 今天正式上市。Vault Enterprise 0.8 中的新功能增强了已经丰富的企业功能集。用户可以在[https://www . Vault project . io](https://www.vaultproject.io/)下载 Vault 的开源版本。Vault Enterprise 有两个版本。Vault Enterprise Pro 产品侧重于协作和操作功能，如用于管理机密、健康监控、初始化和安全引导工作流的用户界面。Vault Enterprise Premium 产品侧重于多数据中心和治理功能，如硬件安全模块(HSM)集成和多数据中心复制。欲了解更多关于 HashiCorp Vault Enterprise 的信息，请访问[https://www.hashicorp.com/products/vault/](https://www.hashicorp.com/products/vault/)。

**关于 HashiCorp** HashiCorp 是一家云基础设施自动化公司，支持组织采用一致的方法来配置、保护、连接和运行任何基础设施。HashiCorp 开源工具，包括 vagger、Packer、Terraform、Consul、Vault 和 Nomad，每天被下载数千次，并被全球 2000 强广泛采用。这些产品的企业版增强了开源工具，具有促进协作、安全性和治理的特性。该公司总部位于旧金山，由梅菲尔德、GGV 资本、红点和 True Ventures 提供支持。欲了解更多信息，请访问[https://www.hashicorp.com](https://www.hashicorp.com/)或在 Twitter @HashiCorp 上关注 HashiCorp。

— [帕克·耶茨](https://devops.com/author/parkerdevops-com/)