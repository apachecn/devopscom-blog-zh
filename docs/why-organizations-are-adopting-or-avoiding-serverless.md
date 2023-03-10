# 为什么组织采用或避免无服务器

> 原文：<https://devops.com/why-organizations-are-adopting-or-avoiding-serverless/>

在首届 [奥赖利无服务器架构采用调查](https://www.oreilly.com/radar/oreilly-serverless-survey-2019-concerns-what-works-and-what-to-expect/) 中，我们对高水平的回应感到惊喜:来自不同地点、公司和行业的 1500 多名受访者参与了调查。高回复率告诉我们，无服务器在社区中赢得了广泛的关注。

下面我们来看看调查中最值得注意的三个发现。

## **为什么组织采用无服务器**

当我们询问受访者的组织是否采用了无服务器(将“采用”定义为与供应商签订合同以提供无服务器资源)时，我们预计这种相对较新的发展中技术的采用率较低。有趣的是，高于预期的 40%的受访者表示他们已经采用了无服务器(图 1)。在那些其组织已经采用无服务器的受访者中，超过 50%的受访者在一至三年前实现了飞跃，15%的受访者在三年多前采用了无服务器。

![](img/02a583b2604904fe8f182e5ae7fa0fb9.png)

Figure 1: Serverless adoption among survey respondents’ organizations.

当被问及采用无服务器的优势时(图 2)，有一些突出的问题。运营成本的降低是最大的收益。与购买需要处理最大潜在流量且大部分时间处于闲置状态的机架和机架服务器相比，无服务器的计算支付方式似乎证明有利于组织的底线。

这可能与第二个最受欢迎的采用原因密切相关:自动随需求扩展。您可以部署无服务器，而不是规划平均或最大使用量，它将扩展到当前的使用量。您只需为使用的东西付费。这种扩展消除了对随机和意外流量高峰或季节性大流量的担忧。

![](img/3d86a729be7783ca318f987ab9bcacc4.png)

Figure 2: Serverless benefits among survey respondents.

## **无服务器问题**

在已采用无服务器的组织中，教育现有员工是受访者最关心的问题(图 3)。这是有道理的——由于无服务器相对年轻，很难找到正式的培训，必须生成特定的文档，并且(在成长过程中)很难找到可供学习的案例研究。此外，组织有时会发现成功需要定制功能。随着供应商激烈竞争以吸引和留住客户，这些功能发展迅速，使得最新的正式培训难以维持。

第二大挑战是供应商锁定。为一个供应商平台编写代码并不能让它变得可移植或容易移植到其他地方。因为无服务器是一个新生的领域，所以市场似乎在等着看供应商之间的可移植性问题如何发展。

![](img/71785c8a85592616daff5b3f4508ea02.png)

Figure 3: Serverless challenges faced by survey respondents’ organizations (respondents whose companies have adopted serverless).

60%的受访者的组织已经 而不是 采用了无服务器(图 4)，他们表示安全问题是他们避免使用无服务器的主要原因。因为我们处在一个安全至上的环境中，任何新技术的采用都有很大的分量。此外，无服务器引入了一种不同的数据管理模式，其中敏感数据更加动态。由于有价值的业务数据不受您公司的管理或控制，人们总是担心谁有权访问、安全性如何、供应商是否查看数据或元数据，以及软件是否打了补丁或易受攻击。

与安全性相邻的还有满足监管要求(如 GDPR)的挑战。在第三方服务器上的云中，您能保证与您自己的基础设施上的安全性和质量水平相同吗？

![](img/121150a61a9d6b2ca52f01e26a172505.png)

Figure 4: Reasons why survey respondents’ organizations have not adopted serverless.

## **无服务器供应商和工具**

图 5 中的结果反映了我们对云市场的了解，也反映了我们在 2019 年 [云本地调查](https://www.oreilly.com/ideas/how-companies-adopt-and-apply-cloud-native-infrastructure) 中的发现。亚马逊的早期上市无服务器产品和市场主导地位使他们在云市场上比主要竞争对手更有优势。然而，微软和谷歌都增加了自己的无服务器产品，并可能保留他们在更广泛的云市场中已经开发的任何市场差异化——即，已经喜欢并使用 Azure 或谷歌云平台的客户可能会发现 Azure 功能和谷歌云功能具有相同的优势。

![](img/504c17499fd5bf7a1bebb83dfe3d799b.png)

Figure 5: Serverless vendors used by survey respondents’ organizations.

定制工具在受访者组织使用的无服务器工具中排名第一(图 6)。这可能意味着标准化或改进现有工具的市场，让公司要么放弃他们的内部工具，要么说服新客户避免花费时间来构建定制的东西。这也可能意味着当前的工具不能解决正确管理和部署无服务器基础架构所需的所有问题。

![](img/fde0d1aef94a8f65567cd2f65588cdbf.png)

Figure 6: Serverless tools used by survey respondents’ organizations.

## **结论**

根据调查，我们预计对无服务器的需求将在短期内增长，成为许多组织的另一个有价值的基础架构选项。由于不依赖于特定的技术或编程语言，serverless 可以处理广泛的任务，并且随着时间的推移，入门变得越来越容易。

你可以在这里 查看奥莱利无服务器调查 [的更多发现和分析。](https://www.oreilly.com/radar/oreilly-serverless-survey-2019-concerns-what-works-and-what-to-expect/)

*要了解更多关于集装箱化基础设施和云原生技术的信息，请考虑来阿姆斯特丹的 [KubeCon + CloudNativeCon EU](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/) 。CNCF 已决定推迟该活动(原定于 2020 年 3 月 30 日至 4 月 2 日)，改为在 2020 年 7 月或 8 月举行。*

*![](img/700ba386b313c30354fd9e8d02dc2102.png)*

本文由 Chris Guzikowski 合著。Chris 是 O'Reilly 的高级内容总监，负责管理软件架构和软件开发中内容的获取和开发。他还是 O'Reilly 软件架构会议的联合主席。Chris 从事技术内容和技术营销工作已经超过 30 年。

——[罗杰·马格努拉斯](https://devops.com/author/roger-magoulas/)