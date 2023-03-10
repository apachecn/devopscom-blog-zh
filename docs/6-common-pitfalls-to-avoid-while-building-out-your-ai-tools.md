# 构建人工智能工具时要避免的 6 个常见陷阱

> 原文：<https://devops.com/6-common-pitfalls-to-avoid-while-building-out-your-ai-tools/>

在全球拥有数千名员工的企业级公司，可以让几乎任何规模的 B2B 公司复制他们的人工智能框架。事实上，即使没有大量的专有数据和强大的计算能力，你也可以构建出有效的人工智能工具。

首先，你可以从电影评论网站、电子商务评论网站和其他地方引入公开可用的数据集来训练你的系统。这样做的时候，一定要仔细检查这些公开发布的搜索集的许可细节，因为有些搜索集不允许商业使用。然后，在预处理阶段——从语料库中删除脏话、行话和其他不相关的元素——你可以添加噪音并稍微改变现有数据，以在语料库中创建更多相关的数据点。

在这之后，你可以通过 tri-training 之类的技术建立一个半监督学习算法。在 tri-training 中，我们本质上是在二进制分类数据上训练三个不同的神经网络。一旦两个模型彼此一致，数据被引入第三个网络，然后重新训练，直到所有三个模型都一致。然而，在你的人工智能工具启动并运行之前，重要的是要注意以下常见的陷阱。

## **过度拟合人工智能模型**

这可能看起来违反直觉，但是你真的不希望你的人工智能模型太精确。如果您的交叉验证分数高于 100，那么您可能需要重新考虑部署模型，因为它可能会过度拟合。如果您的训练数据过拟合，一个小的变化就可能使整个模型变得无用。你的模型应该是准确的。然而，它不能太精确，因为它需要自适应。

## **阶层失衡**

当训练你的人工智能工具时，有时包含不成比例的目标变量是有意义的。例如，也许你正在训练你的计算机视觉人工智能工具来识别仓库中的木板。即使木板只占你总库存的 1%,你也要对少数民族进行抽样调查。在这种情况下，您可能希望 60%的样本是木板。你真的想放大这个数字，以确保你有正确的阶级平衡。

## **数据泄露**

另一个常见的失误是未能捕捉到数据泄露，这可能以多种方式发生。一个常见的情况是，用于测试模型的元素混入了训练数据。这通常会导致您的模型表现良好。然而，当部署到生产中时，它的预测可能不会那么好。为了纠正这一点，跟踪你的人工智能工具的任何变化是至关重要的。除了你的组织的代码审查和配置变更审查，你应该有数据集审查，以确保你的人工智能工程是正确的。你的人工智能工具中的任何参数变化都需要一丝不苟地记录下来。

## **概念漂移**

所有的人工智能工具都依赖于进入你系统的数据的形状。例如，也许你的人工智能模型被训练为响应时间在 1-100 秒之间，突然之间，响应时间在 1-1000 秒之间。在这种情况下，您的模型可能无法捕获新的数据点。意识到这种情况很重要，这样您就可以相应地重新训练您的模型。

有许多技术可以用来识别概念漂移的实例。不要等待客户的反馈，你可以设置异常检测，它可以识别输入数据的概念漂移，并自动更新你的人工智能模型。

## **使用个人数据**

随着 CCPA 和 GDPR 的出台，以及联邦政府授权的美国数据隐私法即将出台，各组织对使用客户数据来训练他们的人工智能工具持谨慎态度。用匿名化的数据训练你的 AI 系统是谨慎的；这样，你就不会在以后遇到问题。

## **无法确保你所有的人工智能决策都是可以解释的**

大多数人工智能决策是由团队而不是个人制定的。因此，至关重要的是，你的人工智能模型推荐的行动路线要有解释。此外，这些解释应该有置信区间，这样更容易解释结果。

在根本原因分析和补救过程中，通常不清楚哪一个团队最终应对手头的问题负责。如果人工智能建议的行动过程附有解释，这在补救过程中会有很大帮助。例如，如果启动事件是网络建设，问题可能出在工程团队身上。或者，如果启动事件是网络配置更改，网络团队很可能是罪魁祸首。通过密切监控你的人工智能工具的性能，并确保所有的人工智能决策都是可以解释的，你可以快速解决问题并纠正方向。