# IBM 和 LFAI 在可信和负责任的人工智能方面取得进展

> 原文：<https://devops.com/ibm-and-lfai-move-forward-on-trustworthy-and-responsible-ai/>

托德·摩尔、斯里拉姆·拉格哈万、亚历山大·莫西洛维奇

一个多世纪以来，IBM 创造了深刻改变人类工作和生活方式的技术:个人电脑、ATM、磁带、Fortran 编程语言、软盘、扫描隧道显微镜、关系数据库，以及最近的量子计算等等。将信任作为我们的核心原则之一，我们在过去的一个世纪里创造了客户可以信任和依赖的产品，指导他们负责任地采纳和使用，并尊重我们服务的所有用户和社区的需求和价值。我们目前在人工智能(AI)方面的工作正在给当今世界带来类似规模的变革。我们将这些信任和透明的指导原则融入到我们所有的人工智能工作中。我们的责任不仅是取得必要的技术突破，使人工智能值得信赖和合乎道德，而且要确保这些可信的算法在现实世界的人工智能部署中按预期工作。
我们在公平机器学习方面的理论工作导致了最早的 [和被引用最多的](https://www.ibm.com/blogs/research/2017/12/ai-reducing-discrimination/) 偏差缓解算法。我们应用先进的机器学习方法来减少对受保护群体和个人的不必要的歧视。将我们的偏差检测和缓解算法集成到 [Watson OpenScale](https://www.ibm.com/cloud/watson-openscale) 中，使 IBM 成为第一家在真实产品中解决人工智能偏差的供应商。作为这项工作的高潮，我们创建了[AI Fairness 360](https://aif360.mybluemix.net/)，这是一个全面的开源工具包，用于处理机器学习算法中的偏差。此外，我们还有两个开源的可信 AI 工具包: [对抗性鲁棒性 360](https://github.com/IBM/adversarial-robustness-toolbox) ，这是一个用于保护 AI 免受对抗性攻击的工具箱和库，以及 [AI 可解释性 360](https://github.com/IBM/AIX360/) ，这是一个解释 AI 系统决策的工具箱。
2020 年 6 月 18 日，Linux Foundation AI Foundation(LFAI)的技术顾问委员会已经投票赞成在 LFAI 中托管和孵化这些可信的 AI 项目。我们正在进行入职流程，以正式确定这些项目的章程、治理和 IT 后勤，并将它们转移到基金会之下。敬请关注 LFAI 博客公布的细节。向 LFAI 捐赠这些项目将进一步推动创建负责任的人工智能技术的使命，并使更大的社区能够在 Linux 基金会的管理下站出来共同创建这些工具。
**可信 AI 360 工具包**

*   [AI Fairness 360 (AIF360)工具包](https://github.com/IBM/AIF360) 是一个开源工具包，可以帮助检测和减轻机器学习模型和数据集中不必要的偏见。它提供了大约 70 个度量来测试偏差，以及 11 个算法来减轻数据集和模型中的偏差。[AI Fairness 360°互动体验](http://aif360.mybluemix.net/data) 对概念和功能进行了温和的介绍。最近，AIF360 还宣布兼容 Scikit Learn，并为 R 用户提供了一个接口。
*   [对抗性鲁棒性 360 (ART)工具箱](https://github.com/IBM/adversarial-robustness-toolbox) 是用于机器学习安全的 Python 库。ART 提供了工具，使开发人员和研究人员能够评估、保护、认证和验证机器学习模型和应用程序，以抵御规避、中毒、提取和推理的对抗性威胁。ART 支持所有流行的机器学习框架(TensorFlow、Keras、PyTorch、MXNet、scikit-learn、XGBoost、LightGBM、CatBoost、GPy 等。)、所有数据类型(图像、表格、音频、视频等。)和机器学习任务(分类、物体检测、生成、认证等。).

去年，DARPA 授予 IBM 研究科学家一笔补助金，用于推进对抗性人工智能的研究

*   [AI explaibility 360(AIX 360)工具包](https://github.com/IBM/AIX360) 是一个全面的开源工具包，包含各种算法、代码、指南、教程和演示，支持机器学习模型的可解释性和可解释性。[AI explaibility 360°互动体验](http://aix360.mybluemix.net/data) 通过针对不同消费者角色的示例用例，对概念和功能进行了温和的介绍。

继续 LFAI 可信人工智能委员会的使命
去年，IBM 与 LFAI 合作成立了可信人工智能委员会，其使命是推进可信人工智能的实践。该委员会后来发展到包括 10 多个组织，致力于定义和实施人工智能部署中的信任原则。该委员会一直在推动的一项活动是将 Trust 360 工具包集成到 Apache Nifi 或 Kubeflow 管道中，以此作为启动可信机器学习工作流的一种方式。
我们还认识到，在促进可信、有益和公平的人工智能方面，技术只是等式的一部分。我们有责任审视人工智能系统如何设计和部署、如何使用以及由谁使用的更广泛背景，并评估它们对用户和社区的影响。
在这个使命中，来自社会科学、政策和立法的贡献以及不同的视角发挥着与技术本身同样重要的作用。我们期待来自不同领域和利益相关者的贡献，并邀请他们加入社区，为推进基金会的使命及其值得信赖的人工智能开源项目做出贡献。
有关 LFAI 可信 AI 委员会活动的更多信息，请参见提交给 LFAI 管理委员会的 [报告](https://docs.google.com/presentation/d/1mAoU2k7RKLo4Rz2My-nxUN5VAaZxoEPiuZZPysmu9Mw/edit#slide=id.p1) 。有意加入者可通过 [可信 AI 委员会页面](https://wiki.lfai.foundation/display/DL/Trusted+AI+Committee) 加入。