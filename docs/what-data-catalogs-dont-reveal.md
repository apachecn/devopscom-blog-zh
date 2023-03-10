# 哪些数据目录没有揭示

> 原文：<https://devops.com/what-data-catalogs-dont-reveal/>

在当今的数据密集型世界中，顾名思义，数据目录只是信息的目录(有些是人工输入的，有些是从系统的元数据中提取的)。数据在企业中的重要性越来越大，分析在创造价值方面发挥着越来越重要的作用。因此，尽管收集、存储和组织所有这些数据很重要，但数据目录却遗漏了一个重要部分——它们未能绘制出数据资产之间的准确关系以及它们如何相互关联(或如何计算)。

这就像有一个包含世界上所有电子元件描述的目录，但却不知道如何将这些元件组装到一个时钟、一台收音机甚至一台计算机中。或者当设备停止工作时如何诊断需要更换什么。

数据目录无法回答一大堆问题，比如“如果我对这个数据集进行更改，会有什么后果？”即使数据目录中的信息被严格地更新，如果实际上发生了更改，受该更改影响的用户(无论是直接还是间接)也无法知道发生了更改。因此，不明问题的风险很高。

下表总结了传统[数据目录](https://devops.com/?s=data+catalog)产品的优缺点。

| **发布** | **数据目录优势** | **数据目录弱点** |
| 数据发现 | 

*   Collect metadata information from various systems
*   Provide users with the flexibility to update information manually.
*   Simplify data asset search across various systems
*   Easily identify subject matter experts (SMEs) related to data sets

 | 

*   Documents that rely on manual maintenance
*   Unable to automatically correlate data sets.
*   Don't understand how data assets are calculated with each other
*   Unable to identify who used a particular data set (and how they used it)

 |
| 数据治理 | 

*   Provide a robust framework for managing the availability, usability, integrity and security of data.

 | 

*   Rely on manually maintained user-defined rules to specify data access.
*   You cannot automatically propagate access rules from one data set to the previous data set.

 |
| 信息安全合规 | 

*   It is convenient for users to mark personal identification information (PII) and other infosec risk data sets

 | 

*   Do not automatically infer the impact of data processing on PII operation in enterprises.

 |
| 数据质量 | 

*   Data directories don't actually check data, so they don't help data quality problems.

 | 

*   Completely failed to identify the problems, and failed to convey the impact of these problems on the downstream of data quality problems.

 |

## 数据发现

数据目录解决方案为收集元数据和促进数据集文档化提供了强大的框架。元数据的收集和聚合是自动化的，数据工程师/分析师有望(但很少)遵从记录他们的工作，以便其他人可以利用它。

不幸的是，数据目录无法识别数据集和处理是如何相互依赖的。没有办法可靠地识别哪些用户直接或间接地访问和依赖特定的数据集。

以此为目标，数据工程师可以通过搜索和分析相关的数据处理代码来人工回答这些问题。这种方法使用昂贵的数据工程资源，耗费时间，并导致分析师和数据工程生产力降低。

## 数据治理

创建新数据集时，作者必须标记数据以控制数据治理。这不仅依赖于作者的遵从，而且必须传播规则以确定谁可以使用新处理的数据。应该如何传播规则？这是一个复杂的问题。例如，某个地址中的城市可能受到限制，但该城市的聚合可能不受限制。定义这些规则本身是复杂的——应用它们甚至更复杂。

依靠数据工程师和分析师来遵守数据治理文档和系统来执行容易出错且成本高昂。敏感数据集面临暴露的高风险。

## 信息安全合规

当前的[信息安全](https://securityboulevard.com/?s=infosec)合规解决方案依赖于:

*   用户手动记录他们的数据处理活动是否使用(或产生)infosec 敏感数据。
*   通过检查实际数据并使用算法来确定需要如何保护数据，自动识别 infosec 敏感数据。

数据目录用于帮助用户记录数据处理活动，以符合 infosec 的合规性要求。这个过程依赖于人工维护文档和系统(并执行实际的数据检查)。)这些流程本身存在严重的安全风险，因为数据检查(本身也存在风险)和熟练的手工操作都是必需的。

## 数据质量

数据工程已经有流程来识别何时有问题将数据放入表中。自动化系统可以检查数据值，并就数据是否可接受做出智能决策(有些甚至基于机器学习)。这些系统存在于传统的数据目录之外。

问题是，这个问题会影响到谁？您必须确定谁是数据的直接用户。您还必须确定低质量数据的间接用户。

目前解决这个问题的方法是让熟练的数据工程师审查所有数据处理代码，并手动识别要警告的用户——这既昂贵又耗时。除此之外，风险在于用户未被识别；如果错误影响到了 CFO 办公桌上的报告，而他们没有得到警告，该怎么办？

数据目录解决方案擅长解决其最初设计的问题，即找到数据工程师和数据分析师感兴趣的数据集。

DevOps 的风险在于，数据发现、数据治理、信息安全合规性和数据质量问题都依赖于数据目录，而这些问题在当今复杂的数据处理环境中无法解决。