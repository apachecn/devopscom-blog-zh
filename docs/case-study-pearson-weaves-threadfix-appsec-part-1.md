# 案例研究:Pearson 将 ThreadFix 编入 AppSec，第 1 部分

> 原文：<https://devops.com/case-study-pearson-weaves-threadfix-appsec-part-1/>

[Pearson](https://www.pearson.com/) 是一家教育行业内容的出版商，旨在满足从幼儿园/早期学习到高等教育和继续教育(针对专业人士)的教师和学生的需求。培生的高级软件安全工程师马特·特索罗(Matt Tesauro)表示，该公司使用一系列软件，从传统的第三方软件和“亚马逊上的经典 ASP 应用程序到自动伸缩系统”。“这是一个非常多样化的开发环境。”这意味着保护它的安全并不容易。

## DevOps 之前的 Pearson

在采用 DevOps 之前，Pearson 陷入了手动流程的困境，尤其是在应用程序安全性方面。“人们发送的请求隐藏在电子邮件中，或者，如果你幸运的话，隐藏在谷歌的电子表格中。由 AppSec 小组负责的不同活动之间很少有明确的界限和交接，”Tesauro 解释道。就请求处理而言，这是一种非常手动的定制方法:有人会用活动来响应请求，这需要一份报告，然后通过电子邮件发送。

当时，培生没有针对这些活动的单一、完善的方法或工作流程。创建动态、手动或静态评估没有特定的外观和感觉或设计。没有流程输入或流程结束时预期输出的列表。“在最好的情况下，一切都是以一种特别的方式流动的，”特索罗说。

然后，大约两年前，特索罗和培生的一位高层同事试图对公司最需要评估安全性和相关问题的应用程序进行优先排序。他们希望并计划大约 10 个应用程序，以保持数量和工作量可控。出于政治原因，他们选定了不少于 64 个需要评估的应用。“我们最终只能评估 64 款顶级应用中的 44 款。粗略估计，培生有 2000 多个应用程序。“只是规模告诉我们，从长远来看，我们将会失败，”特索罗说。

## 加速改变

为了解决这一应用评估挑战，Tesauro 希望制定开发计划并构建管道方法，为最终将安全性集成到 Pearson 的各个开发团队中奠定基础。“我做了 DevOps 的等价物，并为我们在培生的 AppSec 项目中的工作建立了管道方法，”Tesauro 说。这些包括服务请求输入和接收的标准方法，类似于企业如何为开发运维团队制定软件开发目标。就在那时，皮尔森开始着手建立和利用 ThreadFix。

“ThreadFix 是这条管道的前两部分之一，”他说。AppSec pipeline 解决方案的另一部分是 Tesauro 所说的“存储袋”，一种用于跟踪所有团队间交互和工作分配的机制和存储库。输入 ThreadFix。

在那段时间里，大约在 2015 年上半年，特索罗和一名队友通过创建代码来执行“无需动脑的工作”，从而自动化了许多手动步骤，因此开发人员可以专注于他们的核心业务。“现在，当静态代码分析工具 [Checkmarx](https://www.checkmarx.com/) 完成分析时，它会生成一份报告，清洗目录并将报告推送到 ThreadFix，”Tesauro 说。他还自动化了许多其他测试应用程序和工具。

敬请关注本案例研究的第二部分，即将推出。