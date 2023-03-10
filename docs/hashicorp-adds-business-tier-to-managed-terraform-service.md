# HashiCorp 向托管平台服务添加业务层

> 原文：<https://devops.com/hashicorp-adds-business-tier-to-managed-terraform-service/>

HashiCorp 今天宣布，它已向 HashiCorp Terraform 云添加了一个业务层，该业务层扩展了[托管服务](https://devops.com/hashicorp-updates-terraform-tool-for-azure-cloud/)，提供了高级安全性、合规性和治理功能，以及并发执行多个运行的能力，并利用了更灵活的服务级别协议(SLA)选项。

HashiCorp 的产品营销总监 Meghan Liese 表示，这一新层满足了企业 IT 组织的需求，这些组织正在寻找一种方法，使开发团队能够使用开源 Terraform 工具更安全地配置 IT 基础设施。

例如，服务的业务层提供了与 Okta 提供的单点登录工具的集成，而日志审计则通过与 Splunk 的工具集成来提供。该层还提供对具有固定 IP 地址的专用网络的访问，以及自托管代理，以便在需要时与其他管理平面进行交互。

HashiCorp 报告说，自从去年为不想配置服务器的 IT 组织推出托管服务以来，它现在每月增加 5，000 多名新用户，每月运行 500，000 次配置基础架构。

HashiCorp 提供的其他两个现有级别的服务是针对个人开发人员的免费实例，以及团队和治理服务，可用于创建管理和治理可重用配置实例的团队。

Liese 说，HashiCorp 推出业务层的部分原因是为了满足企业 IT 组织的需求，这些组织希望大规模地自动提供 IT 基础架构。Liese 说，虽然开源 Terraform 工具的使用非常自由，但企业 IT 组织需要确保安全性并满足合规性要求。

Liese 指出，这些企业 IT 团队还倾向于同时提供 IT 基础架构，这意味着等待一个配置完成后再启动另一个配置是不现实的。

Terraform 在个人开发者中获得了很大的吸引力，他们倾向于使用开源工具来提供 IT 基础设施。这一势头使 HashiCorp 能够为 IT 组织提供对其部署和管理的 Terraform 实例的商业支持，以及通过 HashiCorp 管理和更新 Terraform 实例的服务。

无论选择哪种方式，以代码形式提供 IT 基础设施的 IT 团队的数量都在大幅增加。相对于精通 Terraform 的 IT 运营人员，开发人员在多大程度上完成了配置工作尚不清楚。在许多组织无法增加更多 IT 人员的时候，自动化配置 IT 基础架构的需求从未像现在这样迫切。

当然，仍有不少 IT 团队倾向于依赖 IT 管理员使用传统工具来配置 IT 基础架构。然而，随着变得更加敏捷的压力不断增加，使用这些工具构建的手动工作流过时只是时间问题。