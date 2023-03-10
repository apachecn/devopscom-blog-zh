# 谷歌利用网飞进行开源金丝雀分析

> 原文：<https://devops.com/google-taps-netflix-for-open-source-canary-analysis/>

谷歌和网飞今天联合宣布了一项开源的自动化金丝雀分析服务，称为 [Kayenta](https://cloudplatform.googleblog.com/2018/04/introducing-Kayenta-an-open-automated-canary-analysis-tool-from-Google-and-Netflix.html) ，该服务应用统计分析来优化 DevOps 流程。

谷歌云平台(GCP)的产品经理 Andrew Phillips 表示，目标是通过将 Kayenta 与谷歌开发的开源 Spinnaker 连续交付管道平台相集成，使高级分析更容易使用。然而，因为 Kayenta 是基于网飞开发的软件，IT 组织可以将任何云或内部 IT 环境中的数据输入到 canary analysis 服务中，Phillips 说。Kayenta 还可以从各种 monitong 工具中获取数据，包括 Stackdriver、Prometheus 和 Datadog。

Phillips 表示，目标是不断迭代 Kayenta，使其足够简单，几乎任何组织都可以利用 canary analysis，这使 DevOps 团队可以跟踪关键组件的内存使用情况等指标。Kayenta 从数据源获取用户配置的指标，运行统计测试，并为金丝雀提供一个总分数。Kayenta 可以根据这些测试结果自动提升或取消“金丝雀”或触发人类批准的请求。

具体来说，Kayenta 创建了一对控制/实验时间序列数据集，并调用 canary judge，它执行统计测试，单独评估每个指标，并使用预先配置的指标权重返回从 0 到 100 的总分数。根据不同的配置，分数被分为“成功”、“勉强合格”或“失败”成功提升金丝雀并继续部署，边缘分数触发人工批准路径，失败触发回滚。

金丝雀的基本概念包括通过反映变更的部署(金丝雀)和与生产环境具有相同代码和配置的新部署实例(用作测试基线)来路由一小部分生产流量。然后，分析引擎将金丝雀与基线之间的指标进行比较，以确定变更可能对生产环境产生的任何重大影响。菲利普斯说，Kayenta 实际上提供了一种基于生产环境的拟议变化的风险建模机制。

谷歌和网飞预计第三方供应商将很快将 Kayenta 整合到各种 DevOps 工具和云平台中。与此同时。Google 认为 Kayenta 是吸引 DevOps 团队利用 Spinnaker 来管理他们在云中的 DevOps 管道的又一种方式。

从历史上看，建立金丝雀分析系统是一项复杂的工作，需要大量的工程技术。菲利普斯说，谷歌正在努力使金丝雀分析民主化，使其成为一种可以按需调用的服务。

Phillips 表示，Kayenta 提供了对数据的访问，这些数据可用于驱动广泛的预测分析应用程序，这些应用程序可用于自动化开发运维流程。Kayenta 数据用于驱动人工智能(AI)模型来自动化这些 DevOps 过程还需要一段时间。

考虑到生产环境中应用程序添加和更新的速度，依靠手动测试很快变得不可行。DevOps 团队需要手动创建他们自己的统计分析模型的日子显然即将结束。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)