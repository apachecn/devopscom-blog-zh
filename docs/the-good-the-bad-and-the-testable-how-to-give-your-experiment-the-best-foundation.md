# 好的，坏的和可测试的:如何给你的实验最好的基础

> 原文：<https://devops.com/the-good-the-bad-and-the-testable-how-to-give-your-experiment-the-best-foundation/>

无论你是在建造一栋房子，一个新的企业还是一个移动应用程序，一个坚实的基础是至关重要的。它为您提供了一个坚实的基础，并且它会对您的项目生命周期产生巨大的影响。这同样适用于实验过程。

在开始软件实验之前，通过在实验设计阶段投入时间来创建一个强大的基础是很重要的。一个设计良好的实验将有一个清晰且可测试的假设，一套通过功效分析计算的运行时间，以及一个分析阶段的预定计划。规划分析的两个关键部分是决定您将测量哪些指标，以及您将使用哪种统计测试来确定任何变化是否具有统计显著性。不幸的是，这说起来容易做起来难，如果使用错误的统计测试或度量标准，你的实验注定会失败。

## 如何发现一个糟糕的指标或错误的测试？

通常，人们没有意识到他们使用了一个不好的度量或者错误的测试。在这两个指标中，一个不好的指标更容易被发现。首先，问问自己，“如果这个指标增加，意味着什么？”有了这个答案，你应该能够很容易地解释这是一个好的还是坏的结果，和/或用户行为或产品性能的哪个方面发生了变化，以及以何种方式发生了变化。如果有多种不同的方法来解释度量的变化，那么这可能不是一个好的方法。

确定你是否使用了错误的统计测试更加困难。有许多不同类型的测试适用于不同的场景。例如，虽然卡方检验可能适用于比例指标(如转换的独立用户的百分比)，但如果应用于非比例指标(如页面加载时间)，该检验将不会给出准确的结果。相反，对于均值或实值，t 检验通常是应用于结果的正确方法。

要记住的最重要的事情是，度量标准应该满足您对其应用的测试的所有假设。例如，t 检验和卡方检验都假设观察值是独立的，并且数据中的噪声是正态分布的。检查这一点的一种方法是 AA 测试，这是一种两种治疗方法没有任何区别的实验。如果您运行一系列 AA 测试，将您的统计测试应用于指标，p 值应该是均匀分布的，并且具有统计显著性的 AA 测试部分应该大致等于您的假阳性率，例如，如果使用 0.05 的 p 值阈值，则为 5%。

## **不良指标或错误测试的后果**

没有正确的度量和测试，你的实验一定会遇到麻烦。具体来说，使用一个不好的指标会使你很难解释你的实验结果，或者在最糟糕的情况下，它会让你不知不觉地得出错误的结论。这可能意味着你没有从实验中获得尽可能多的价值和知识。

类似地，使用不适合您所应用的度量标准的统计测试也会导致您得出不正确的结论。在这种情况下，它会导致比设置显著性级别时预期的更高的假阳性率。这会让你认为你的实验产生了影响，而这只是数据中的正常噪音。

## 什么是好的衡量标准？

理想情况下，一个好的指标应该是可解释的、有意义的、敏感的，并且适合你所应用的统计测试。可解释意味着，如果指标发生变化，您应该能够轻松确定它会产生积极影响还是消极影响，以及这对用户行为或系统性能意味着什么。一个有意义的度量直接测量你在实验中关心的东西。这可能是业务价值或客户满意度的一个很好的代理。敏感指标能够检测给定流量的较小变化。例如，缓慢移动的指标(如保留率)或高方差指标(如收入)虽然很重要，但本质上并不敏感，因此可能不是您实验的主要指标的最佳选择。

最后，适合测试意味着指标应该满足前面提到的统计测试的所有假设。例如，当您在 users⎯would 上随机化时，分母不等于随机化 unit⎯e.g.每会话指标的指标不会给出独立的观察值，因此不适合用于标准统计测试，如 t-检验或[卡方检验。](https://en.wikipedia.org/wiki/Chi-squared_test)

## **良好指标的好处**

一个好的度量标准对于任何成功的实验都是至关重要的。它可以让你从实验中获得最多的信息和知识，使实验更容易理解，运行更有效。使用一个好的度量标准和适当的测试也将避免夸大的假阳性率和被数据误导的机会，这提供了最大的好处:节省时间和金钱。

— [利齐·艾德利](https://devops.com/author/lizzie-eardley/)