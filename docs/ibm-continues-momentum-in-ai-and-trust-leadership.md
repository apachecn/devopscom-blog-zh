# IBM 继续在人工智能和信任领域保持领先

> 原文：<https://devops.com/ibm-continues-momentum-in-ai-and-trust-leadership/>

AI Fairness 360 toolkit 对于更广泛的开发者来说变得更加容易使用

威利·特哈达
2020 年 6 月 3 日出版

The field of artificial intelligence (AI) is making progress as it looks to improve industries and society. But, while the technology continues advancing, the idea of “build for performance” will no longer suffice as an AI design paradigm. We are now in an era where AI must be built, evaluated, and monitored for trust.

IBM 继续作为行业领导者推进我们所谓的[可信人工智能](https://www.research.ibm.com/artificial-intelligence/trusted-ai/)，专注于开发多样化的方法，在人工智能应用程序的整个生命周期中实现公平、可解释和可问责的元素。

## IBM AI 公平 360 工具包

在我们可信的人工智能努力下，IBM 在 2018 年发布了[人工智能公平 360 工具包](https://www.ibm.com/blogs/research/2018/09/ai-fairness-360/) (AIF360)，这是一个[可扩展的开源工具包](http://aif360.mybluemix.net/?_ga=2.10956279.236899408.1590515107-1612769744.1584890321&cm_mc_uid=90353198868315831834576&cm_mc_sid_50200000=77837031590698244299)，可以帮助你在整个人工智能应用生命周期中检查、报告和减轻机器学习模型中的歧视和偏见。它包含研究社区开发的 70 多个公平指标和 11 个最先进的偏见缓解算法，旨在将实验室的算法研究转化为金融、人力资本管理、医疗保健和教育等广泛领域的实际实践。

## 为 AI Fairness 360 添加新功能

现在，IBM 增加了两种新的方式，使 AIF360 变得对更广泛的开发人员更容易访问，并增加了功能:与 scikit-learn 和 r。

### r 用户现在可以使用人工智能公平 360 工具包

随着机器学习模型越来越多地用于高风险决策，人工智能公平是一个重要的话题。机器学习发现并归纳数据中的模式，因此可以复制特权群体的系统优势。为了确保公平，我们必须分析和解决任何可能出现在我们的训练数据或模型中的认知偏差。

我们很高兴地宣布发布 AI Fairness 360 R 包，这是一个开源库，包含在整个 AI 应用程序生命周期中帮助检测和减轻数据集和机器学习模型中的偏差的技术。请阅读“[AIF 360 公平工具包现已面向 R 用户](https://developer.ibm.com/blogs/the-aif360-team-adds-compatibility-with-r/)”了解详细信息。

### 人工智能公平 360 现在可以兼容 scikit-learn

scikit-learn 数据科学库对于训练已建立的机器学习算法、计算基本指标和构建模型管道非常有用。事实上，AI Fairness 360 中的许多示例笔记本已经使用了具有预处理或后处理工作流的 scikit-learn 分类器。然而，在 AI Fairness 360 toolkit 算法和 scikit-learn 算法之间切换会破坏工作流，并迫使您来回转换数据结构。你也不能使用 scikit 中一些强大的元编程工具——比如管道和交叉验证。

于是，AIF360 团队在 aif360 最新版本 0.3.0 中加入了新的 aif360.sklearn 模块。在本模块中，您可以找到所有当前已完成的兼容 scikit-learn 的 AIF360 函数。在"[中获取有关此更新的所有信息。AIF360 团队增加了与 scikit-learn 的兼容性](https://developer.ibm.com/blogs/the-aif360-team-adds-compatibility-with-scikit-learn/)。

## 推动可信人工智能向前发展

用户可以使用 AIF360 在 Watson Studio 中检测训练时的公平性问题，并使用[Watson open scale](https://www.ibm.com/cloud/watson-openscale)在运行时检测公平性。Watson OpenScale 已经支持一些 AIF360 指标，从长远来看，我们正在设计时和运行时将更多的 AIF360 指标集成到 Watson OpenScale 中。AIF360 也将通过 IBM Cloud Pak for Data 开源目录提供。