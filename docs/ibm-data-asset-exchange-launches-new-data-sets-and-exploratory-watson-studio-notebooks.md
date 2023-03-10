# IBM 数据资产交换推出新的数据集和探索性沃森工作室笔记本

> 原文：<https://devops.com/ibm-data-asset-exchange-launches-new-data-sets-and-exploratory-watson-studio-notebooks/>

IBM 数据资产交换推出新的数据集和探索性沃森工作室笔记本。

由[爱德华·利尔迪](https://developer.ibm.com/profiles/edward)T2 出版 2020 年 5 月 26 日

The [IBM® Data Asset eXchange (DAX)](https://developer.ibm.com/exchanges/data/) is an online hub for developers and data scientists to find free and open data sets under open data licenses. A particular focus of the exchange is data sets under the [Community Data License Agreement (CDLA)](https://cdla.io/). Since launching the exchange in 2019, the [Center for Open-Source Data & AI Technologies (CODAIT)](http://codait.org/) team has been working on steadily adding new data sets to the exchange, as well as resources that help explore these data sets.

我们对数据资产交换的最新更新增加了大量新的数据相关资产和用户体验增强。对于现有的数据集，我们添加了七个新的 Watson Studio 笔记本以及三个 Watson Studio 项目(一种新的数据资产类别，将多个笔记本打包在一起)。除了这些笔记本电脑，我们还向 exchange 添加了八个新的数据集，涉及石油开采、遥感和语音识别等领域。最后，我们正在努力改进 DAX 显示数据集预览的方式。我们已经开始添加数据词汇表和详细的元数据部分，为用户提供数据集功能和用例背后的额外上下文。我们还开始致力于提供文本、图像和音频数据记录预览，允许用户对数据集进行采样，而不必下载整个数据集档案。

## 新沃森工作室项目

我们现在正在逐步将 Watson Studio 项目添加到数据集，其中包括说明用户如何提取、清理、分析和建模数据的笔记本集。要将项目导入 Watson Studio，请访问下面在 [IBM 数据资产交换(DAX)](https://developer.ibm.com/exchanges/data/) 上讨论的三个数据集之一，并单击**运行数据集笔记本**或通过单击**使用数据集**部分中的链接预览代码。要了解更多关于 Watson Studio 项目的信息，请查看本教程。第四个项目已经在开发中，我们将增加更多相关的项目。

### 数据资产交换气象项目

我们的第一个沃森工作室项目发布是 [DAX 天气项目](https://dataplatform.cloud.ibm.com/exchange/public/entry/view/a7432f0c29c5bda2fb42749f363bd9ff)，它使用了 [NOAA 天气-JFK 机场](https://developer.ibm.com/exchanges/data/all/jfk-weather-data/)数据集。这个项目有三个笔记本电脑执行不同的功能。第一个是数据清理笔记本，它指导用户如何估算缺失的数据值，并对某些天气特征进行编码，以获得更好的机器学习模型性能。该项目还包括一个数据分析笔记本，可以可视化数据集的功能依赖关系和随时间变化的趋势。最后，该项目包括一个时间序列预测笔记本，以建立一个 ARIMA 模型，并使用 RMSE 度量评估其性能。

### 数据资产交换时尚 MNIST 项目

[时尚-MNIST 项目](https://dataplatform.cloud.ibm.com/exchange/public/entry/view/61373b7f2fedecf546b89396da75fe20)通过探索服装图像数据集的潜在用途，建立了与其同名的 [DAX 数据集](https://developer.ibm.com/exchanges/data/all/fashion-mnist/)。这个项目从一个数据探索笔记本开始，它可视化各种服装物品类别并执行降维。第二个笔记本使用 scikit-learn 库来比较传统机器学习方法对服装标签进行分类的性能。第三个笔记本也设计了一个分类器，但这次使用 Keras 来构建深度学习卷积神经网络。

### 数据资产交换格罗宁根意银行项目

我们的第三个沃森工作室项目，[格罗宁根意义银行项目](https://dataplatform.cloud.ibm.com/exchange/public/entry/view/00d1f36477e7a092a43a264d410d5451)利用 [DAX GMB 数据集](https://developer.ibm.com/exchanges/data/all/groningen-meaning-bank/)来探索文本中的命名实体。该项目的第一个笔记本让用户熟悉数据集中发现的不同类型的实体和词性标签，并可视化语料库的属性，如最常见的标记。第二个笔记本指导用户如何构建一个简单的命名实体识别模型，包括特征工程和模型结果分析部分。

## 新的探索性数据分析笔记本

除了 Watson Studio 项目，我们还发布了一批新的探索性笔记本电脑，随附我们的 DAX 数据集。通过在每个数据集的 DAX 登录页面上点击**试用笔记本**，可以访问这些笔记本。

### 合同和金融服务银行

[合同命题库](https://developer.ibm.com/exchanges/data/all/contracts-proposition-bank/)和[金融命题库](https://developer.ibm.com/exchanges/data/all/finance-proposition-bank/)数据集，由法律和金融领域句子的命题库样式注释组成，现在有了加载和可视化这些注释的笔记本。包括例如可视化诸如词性标签的特征分布的图形，以及可视化存储注释的 CoNLL 节点图形格式的图形。

### 面向维基百科的相关性和类别立场

最近发布的另外两个笔记本支持 [IBM Project Debater](https://www.ibm.com/blogs/watson/2020/03/ai-learns-the-language-of-business-behind-the-scenes-at-ibms-nlp-innovation-event/) 数据集、[维基百科导向相关性](https://developer.ibm.com/exchanges/data/all/wikipedia-oriented-relatedness/)和[维基百科类别立场](https://developer.ibm.com/exchanges/data/all/wikipedia-category-stance/)，探索从维基百科提取的文本数据。这两个笔记本都将带您了解如何将数据加载到 Pandas 数据框架中。面向维基百科的相关度笔记本可视化概念相关度数据的样本(对两个维基百科文章之间的相关度评分)，而维基百科类别立场笔记本可视化类别立场数据的样本(对某个主题的维基百科文章的赞成或反对)。

### IBM Project Debater 声明句子、提及检测和情感词汇

最后添加的三个笔记本，[主张句搜索](https://developer.ibm.com/exchanges/data/all/claim-sentences-search/) , [提及检测基准](https://developer.ibm.com/exchanges/data/all/mention-detection-benchmark/),[情感作文词典](https://developer.ibm.com/exchanges/data/all/sentiment-composition-lexicons/)也全部是源自 IBM Project Debater 的特征数据集。索赔句子搜索笔记本使用主题建模可视化数据集的辩论主题集合。提及检测基准笔记本将包含的文本数据标记化，并探索数据中存在的各种实体类型。情感合成词典笔记本计算并可视化数据集中包含的各种二元词对的情感。

## 新数据集

### TF 语音命令

新添加的 [TensorFlow 语音命令](https://developer.ibm.com/technologies/artificial-intelligence/data/speech-commands/)数据集包含超过 65，000 个 30 个常见英语口语单词的简短音频剪辑。该数据集非常适合于训练音频分类器来检测诸如“是”或“否”的语音命令。数据集还包含带有背景噪声的音频文件，这些背景噪声可用于与语音剪辑合并，以使训练数据多样化。

### WikiText-103

[WikiText-103](https://developer.ibm.com/technologies/artificial-intelligence/data/wikitext-103/) 数据集的特点是从维基百科上经过验证的“好的”和“有特色的”文章集中提取了超过 1 亿个文本标记。它在 [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) 许可下可用，非常适合长期依赖语言建模。

### 油藏模拟

[油藏模拟](https://developer.ibm.com/exchanges/data/all/oil-reservoir-simulations/)数据集由 IBM 研究人员生成的 60，000 个基于物理的模拟油藏组成。该数据集的特性和生产率标签是基于序列的，这使得该数据集非常适合测试和验证序列算法。数据集包括一个[详细笔记本](https://dataplatform.cloud.ibm.com/analytics/notebooks/v2/b5e9870d-09e7-46e7-81f6-8fda491528ee/view?access_token=c41287b79fafacff3644c93bdac4006a79175161cbcfb5630c304781f641cfd4),它为生成顺序数据的模拟运行提供直观解释。数据集中包括基于物理的模拟器的输入文件以及数据的原始和预处理版本，使该数据集非常适合数据科学家新手和高级研究人员。

### 维基百科实体图

由 IBM Research 开发的[维基百科实体图](https://developer.ibm.com/exchanges/data/all/wikipedia-entity-graph/)数据集由来自维基百科的实体的知识图组成，其中每个实体由一个上下文文档补充，该文档表示该实体在维基百科上出现的所有上下文。这个数据集可以用于执行图形结构和文本数据的联合建模的问题和技术。

### Mono 湖表面水域范围 Landsat8 数据

[Mono Lake 地表水范围 Landsat8](https://developer.ibm.com/exchanges/data/all/mono-lake-surface-water-extent-landsat8-data/) 数据集包含由 IBM Research 的研究人员进行后处理的 Landsat8 卫星图像数据，以测量 Mono Lake 在 2013 年 4 月 18 日至 2019 年 12 月 31 日期间的地表水范围信息。地表水范围对于土地利用、水管理和生态系统健康的研究非常重要。这些数据可用于预测湖泊水域范围和条件的时间序列，以监测湖泊如何随时间变化。

### 塔拉纳基盆地策划测井

[塔拉纳基盆地管理的测井记录](https://developer.ibm.com/exchanges/data/all/taranaki-basin-curated-well-logs/)数据集由位于新西兰西海岸的 407 口油井组成。底层数据来自新西兰石油&矿产在线勘探数据库，由 IBM Research 进行处理和清理，生成一个简单的 CSV 文件，其中包含测井记录、油井坐标和油井地质特征。

### 简单问题和 WebQSP 关系检测

[SimpleQuestions 关系检测](https://developer.ibm.com/exchanges/data/all/simple-questions-relation-detection)和 [WebQSP 关系检测](https://developer.ibm.com/exchanges/data/all/web-qsp-relation-detection)数据集是由 IBM Research 从底层问答数据集生成的实体关系标注集。关系检测任务处理生成文本中实体之间的语义关系。SimpleQuestions 关系检测数据集是使用脸书研究所开发的 SimpleQA 数据集得出的，而 WebQSP 关系检测数据集是从微软研究所创建的 WebQSP 数据集得出的。

如果您对数据资产交换有任何意见或反馈，请使用 [GitHub](https://github.com/codait/max-central-repo) 或 [Slack](https://model-asset-exchange.slack.com/join/shared_invite/enQtNDQ4OTQxODUyMTYwLTI1NzgyMTRlNWE4ZGE3NmQ5ZjJhYjEwZjA3ZmY4NWViN2MxMWJiZjg0NzM1MTNiZGYwYmQ0MjQ2Mzk3YzI1Yjc) 与我们联系。