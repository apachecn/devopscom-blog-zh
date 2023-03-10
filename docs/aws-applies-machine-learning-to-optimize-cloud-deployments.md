# AWS 应用机器学习来优化云部署

> 原文：<https://devops.com/aws-applies-machine-learning-to-optimize-cloud-deployments/>

亚马逊网络服务(AWS)本周在其 [re:Invent 2019](https://reinvent.awsevents.com/) 会议上展示了两款基于机器学习算法的工具，以优化云应用部署。

[亚马逊 CodeGuru](https://aws.amazon.com/codeguru/) 是一项预览服务，云服务提供商将通过它[检查应用代码](https://devops.com/what-are-aws-application-patterns/)，使用机器学习算法分析代码，然后确定瓶颈，以及代码的哪一部分在 AWS 云上运行最昂贵。

[AWS Compute Optimizer](https://aws.amazon.com/compute-optimizer/) 同时为特定类型的工作负载确定最佳的 Amazon EC2 实例类型，包括那些属于自动扩展组的实例类型。它分析工作负载的配置和资源利用率，包括历史指标，以确定数十个特征来推荐最佳 AWS 计算资源。AWS Compute Optimizer 可通过 AWS 管理控制台进行访问。AWS 不是依靠人类来优化云平台，而是减少确定几十种实例类型中哪一种将以尽可能低的成本提供最高性能所需的时间和精力。

Amazon CloudGuru 可以从 GitHub 或 CodeCommit 存储库中提取代码，并计划支持其他存储库。它需要开发者将 AWS 开发的代理软件插入到他们的代码中。一旦发出拉取请求，亚马逊 CodeGuru 将自动开始使用训练有素的人工智能(AI)模型评估代码，这些模型是 AWS 利用从 AWS 及其母公司的数千个不同的开源软件项目中收集的数据开发的。

一旦分析完成，Amazon CodeGuru 将生成一个“火焰图”,显示例如延迟问题和 CPU 利用率，以及针对特定问题的人类可读建议和建议的补救措施，包括示例代码和任何代码行的相关文档的链接。Amazon CodeGuru 可以观察应用程序运行时，并每五分钟分析一次应用程序代码。

AWS 首席执行官 Andy Jassy 告诉与会者，亚马逊已经在 80，000 个应用程序中使用了亚马逊 CodeGuru，这导致基础设施利用率增加，在某些情况下达到了 325%。

虽然机器学习算法在使 DevOps 团队能够构建和部署更高效的代码方面有着明显的作用，但尚不清楚 DevOps 团队会在多大程度上希望让 AWS 获得对通常高度专有的应用程序的访问权限。许多 DevOps 团队可能更喜欢在持续集成/持续部署(CI/CD)环境中使用机器学习算法来驱动代码到多个云计算平台。无论采用何种方法，很明显机器学习算法将在 DevOps 中发挥更大的作用。事实上，Jassy 本周明确表示，AWS 将广泛应用机器学习算法，以增强从企业搜索到识别潜在欺诈的一切。

不太清楚的是，最佳 DevOps 实践将需要如何发展，以解释机器学习算法。构成 DevOps 工具链的许多流程越来越自动化。这并没有消除对工具链的需求，但它将大大减少构建和优化部署应用程序所需的时间和精力。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)