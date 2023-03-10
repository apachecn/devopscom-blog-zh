# 下一代 ML 工具的三大要求

> 原文：<https://devops.com/top-3-requirements-for-next-gen-ml-tools/>

随着[机器学习](https://devops.com/?s=machine+learning)市场的成熟，新的工具正在发展，可以更好地满足数据科学和机器学习团队的需求。开源和私有的供应商都在快速推出新产品，以更好地满足需求，从而更容易、更快地开发模型和实现协作。

这些新产品包括基于云的平台，可以轻松构建和部署模型，以及专门的软件，可以加快培训过程。例如，现有的 ML 实验跟踪领域是一个数十亿美元的市场，有大量的供应商:Comet ML、Weights & Biases、Neptune AI、Databricks 的 MLflow 等等。这些工具将需要发展，以超越仅满足 ML 团队的基本要求，如实验跟踪、可视化和模型培训，以解决协作和技术要求，以便这些团队可以更快地将模型推向市场。

推动现代数据科学需求的团队类型是 [普通团队类型](https://medium.com/sapphire-ventures-perspectives/the-future-of-ai-infrastructure-is-becoming-modular-why-best-of-breed-mlops-solutions-are-taking-fd85c6ca8bcf) ，在这种团队中，所有的一切都是为了找到新的技术和解决方案来提高效率，并让模型更快地上市，从而为他们的组织保持竞争优势。展望未来，当 ML 团队评估要添加到其 MLOps 堆栈中的工具时，我们看到了以下要求。

### 一种开放的、模块化的方法

数据科学家和 ML 工程师使用多种工具来完成他们的工作，从用于模型编码的 Jupyter 笔记本到用于实验和数据版本控制的 DVC，再到自动化工具，如 AirFlow 和模型可视化工具。解决方案将需要开放与其他工具的集成，而不是像云供应商(如 Amazon SageMaker 等)提供的许多 ML 工具那样的围墙花园。)现在都是。

### 熟悉的开发人员体验

ML 开发人员和工程师熟悉标准的 DevOps 工具和工作流，如 [GitOps](https://devops.com/?s=GitOps) (想想 GitHub 或 GitLab)，并生活在面向 CLI 的解决方案中。ML 工具应该与这些现有的工具紧密集成，而不是用一个独立的生态系统使开发人员的体验变得复杂。作为开发者体验的一部分，工作流也很重要。数据科学家可以使用他们首选的基于 CLI 的解决方案运行数百个实验，但通常所有这些实验都是流式的，并发布到现有的 ML 工具中。更好的方法是为数据科学家提供在本地运行实验的经验，让他们只提交最重要的实验进行进一步的讨论和协作，这样团队就不会不堪重负。

### 与源代码的紧密联系

这种方法为跟踪 ML 实验打下了更坚实的基础。当 ML 团队竞相将模型推向市场并不断改进它们时，与 DevOps 团队保持同步以将那些 ML 模型部署到生产中是至关重要的。一个例子是一个开发人员用变化的超参数跟踪五个实验。对于这些实验，他们可能有一个到特定版本源代码的 Git repo 的链接。但是，如果源代码变更或数据集变更没有在他们现有的 ML 解决方案中提交或报告，该怎么办呢？然后，连接丢失，现有的度量将基于不再准确的源代码或数据的先前版本。这种失去的联系会减缓上市时间，并使优化模型变得更加困难。

从上面的例子可以看出，ML 团队在为各种应用程序和服务开发模型时，会处理各种各样的工具和工作流。所讨论的需求将有助于这些团队在日益多样化的 MLOps 环境中更好地协作和更快地构建模型。