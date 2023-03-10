# 近距离观察 Azure DevOps

> 原文：<https://devops.com/a-closer-look-at-azure-devops/>

微软的 Azure DevOps 服务器正在成为最受欢迎的云应用开发环境之一。像大多数持续集成/持续交付(CI/CD)平台一样，它提供了版本控制、报告、项目管理、自动化构建和测试等特性。它涵盖了应用生命周期的所有方面，并支持开发运维。下面我们来仔细看看这个云计算环境。

Azure DevOps 提供了许多不同的开发人员服务，允许 DevOps 团队规划工作、协作进行代码开发以及构建和部署应用程序。它是高度协作的，将开发人员、项目经理和个人贡献者聚集在一起开发软件。它允许组织比传统的软件开发方法更快地创建和改进产品。

## 服务还是服务器？

团队可以使用 Azure DevOps 服务在云中工作，也可以使用 Azure DevOps 服务器在内部工作。

云产品 Azure DevOps Services 是一种可扩展、可靠且全球可用的托管服务。它由 99.9%的 SLA 提供支持，由微软的 24/7 运营团队进行监控，并可在世界各地的本地数据中心使用。

内部部署产品 Azure DevOps Server 构建在 SQL Server 后端之上。当组织需要将其数据保留在其网络中，或者当他们希望访问与 Azure DevOps 服务器数据和工具集成的 SQL Server reporting services 时，内部版本是首选。

尽管两种产品都提供相同的[基本服务](https://docs.microsoft.com/en-us/azure/devops/user-guide/services?view=azure-devops)，但 Azure DevOps 服务提供了一些额外的好处:

*   简化的服务器管理。
*   立即访问新功能和更新。
*   改善了与远程站点的连接。
*   资本支出(服务器等)的过渡。)到运营支出(订阅)。

根据您的组织或团队的需求，还有一些其他的关键差异。如果您要从内部迁移到云，这些也很有帮助:

*   [范围和规模数据](https://docs.microsoft.com/en-us/azure/devops/user-guide/about-azure-devops-services-tfs?view=azure-devops#scope-scale-data)
*   [认证](https://docs.microsoft.com/en-us/azure/devops/user-guide/about-azure-devops-services-tfs?view=azure-devops#authentication)
*   [用户和组](https://docs.microsoft.com/en-us/azure/devops/user-guide/about-azure-devops-services-tfs?view=azure-devops#users-groups)
*   [管理用户访问](https://docs.microsoft.com/en-us/azure/devops/user-guide/about-azure-devops-services-tfs?view=azure-devops#manage-user-access)
*   [安全和数据保护](https://docs.microsoft.com/en-us/azure/devops/user-guide/about-azure-devops-services-tfs?view=azure-devops#security-data)

### 特定功能领域的差异

虽然 Azure DevOps Services 是 Azure DevOps Server 的托管版本，但有一些功能差异。服务不支持某些服务器功能；例如，Azure DevOps Services 没有与 SQL Server Analysis Services 集成来支持报告。流程定制和报告在支持方面也有所不同。

## 集成功能

Azure DevOps 提供了可以通过 web 浏览器或 IDE 客户端访问的集成功能。根据贵组织的业务需求，可以使用以下一项或多项独立服务:

*   [**Azure Repos:**](https://docs.microsoft.com/en-us/azure/devops/repos/get-started/what-is-repos?view=azure-devops)Azure Repos 提供 Git 库或 Team Foundation 版本控制(TFVC)进行源代码控制。
*   [**Azure Pipelines:**](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/what-is-azure-pipelines?view=azure-devops) 该服务提供构建和发布服务，支持应用的持续集成和持续交付。
*   [**Azure Boards:**](https://docs.microsoft.com/en-us/azure/devops/boards/get-started/what-is-azure-boards?view=azure-devops) 这套敏捷工具支持使用看板和 Scrum 方法规划和跟踪工作、代码缺陷和问题。
*   [**Azure 测试计划:**](https://docs.microsoft.com/en-us/azure/devops/test/overview?view=azure-devops) Azure 测试计划提供了几种测试应用的工具，包括手动/探索性测试和持续测试。
*   [**Azure 工件:**](https://docs.microsoft.com/en-us/azure/devops/pipelines/artifacts/artifacts-overview?view=azure-devops) 这些允许团队从公共和私有来源共享 Maven、npm、NuGet 等包，并将包共享集成到管道中。

还支持使用以下协作工具:

*   可定制的团队仪表盘，带有可配置的小部件，用于共享信息、进度和趋势。
*   用于共享信息的内置维基。
*   可配置的通知。

Azure DevOps 支持添加扩展和与其他流行服务集成，如 Campfire、Slack、Trello、UserVoice 等。此外，DevOps 团队还可以开发自己的定制扩展。

Azure DevOps 服务支持与 GitHub 和 GitHub 企业服务器代码库的集成。Azure DevOps 服务器支持与 GitHub 企业服务器存储库集成。

## 入门指南

注册 Azure DevOps 时，必须先注册组织、项目和版本控制类型。DevOps 团队可以创建多个项目，并使用单独的名称和访问权限来区分它们。项目可以设置为公共或私有。团队还可以使用 Azure Boards 进行协作和项目管理，还可以配置敏捷实践的使用。组建好你的团队后，你就可以使用这个平台开始向 Azure 部署你的应用了。

除了协作环境，Azure DevOps 还提供对支持多种语言和平台的 Azure 管道服务的访问。Azure DevOps pipeline 是一组被分组到单个项目中的服务。

此外，Azure 测试计划功能有助于自动化测试。还可以为多个应用程序设置具有不同组件的部署管道。

Azure Pipeline 可以跟踪工作状态，管理积压工作，并创建自定义报告。在 Azure DevOps pipeline 的帮助下，开发人员可以在单一环境中创建、管理和部署他们的项目。有了这个解决方案，DevOps 团队将有一个单一的联系点，可以相互交流。