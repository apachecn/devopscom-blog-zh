# 简化开发运维及基础设施即代码(IaC)

> 原文：<https://devops.com/simplifying-devops-and-infrastructure-as-code-iac/>

让我们面对现实吧，[基础设施即代码](https://stackify.com/what-is-infrastructure-as-code-how-it-works-best-practices-tutorials/) (IaC)配置管理工具可能至关重要，但它们很难使用。但是如果与其说是工具本身，不如说是我们对它们的理解呢？如果我们以不同的方式看待供应和配置系统，并使用更少混淆和更常见的词汇，会怎么样？

简而言之，如果术语更简单，我们会对这些工具有更好的理解——因此，它们会更容易使用。重构这些复杂的工具不仅能让我们更好地理解这个领域，还能更有效地解决我们都经历过的 DevOps 和软件问题。

## 接受基础设施即代码(IaC)

软件工程包括开发人员为创建软件和技术产品而采取的所有行动。这通常需要编写代码，测试它，并确保它满足用户的原始需求。运营是确保这些软件系统准备就绪并能够在日常基础上为用户服务的实践。运营工程师不像开发人员那样专注于编写新代码；相反，他们关注的是现有软件在现有系统中的行为。

现在让我们来看看我们在 DevOps 中经常使用和听到的其他一些关键短语。

前向工程意味着根据系统的需求创建一个系统。它需要首先构建一个模型，在软件中实现它，然后配置并部署到操作中。虽然目标是让新系统紧密匹配原始需求，但是建模过程可能是不明确的，导致系统以无法预料的方式运行。此外，随着时间的推移，由于与环境的相互作用，系统本身可能不同于原始模型。考虑到某些部分可以改变其他部分的配置；工程师执行的程序也会改变系统状态或配置。

不幸的是，在模型创建过程中，正向工程没有提供关于产品最终成功或失败的反馈。首先创建这些模型和后续的软件，然后部署以测试是否成功。这种系统只能在以后根据其行为提供反馈，然后用于改进和建立新的模型。

逆向工程要求理解现有的系统，通常首先通过检查这样的系统来创建部分心智模型，然后使用它来计划任何修改。通常，在没有完全理解系统如何工作的情况下，直接对系统进行更改。对变化的反馈很快，因为测试系统的速度和检查结果相对简单、容易和便宜。逆向工程的一个很好的例子是软件安全专家，他们扫描网络服务或内存以识别异常和可利用的漏洞，然后试图操纵其内容以获得即时反馈。

然后是基础设施即代码(IaC) 。这种建模技术始于关于服务器操作系统内容应该如何出现的声明，后来被用于使用 API 调用来布局和配置云资源。虽然许多供应商和产品来了又走，但大多数工具都是声明性的——这是有充分理由的。

## 有什么要申报的吗？

使用声明性工具，您可以指定事情应该如何出现，而无需明确显示您将如何到达那里。为什么？这是创建模型、模板和地图的最简单的方法，因为工程师只需要声明事物应该是什么样子，而不是让它们变成正确的形式或实际这样做的地方。重点是从随时间发生的迭代改进中演化而来。

声明式 IaC 工具的另一个特性是幂等性，这意味着多次重复一个动作会得到一致的结果；系统只有在检测到与模型的偏差时才会改变。这可以与命令式方法相比，命令式方法要求开发人员首先找到模型和系统之间的所有差异，然后编写系统匹配模型所需的每个步骤。

声明性 IaC 工具消除了开发人员为这些更改手动编写实现的需要。这些工具通过发布可重复使用的模板节省了数千个工时，从而以更少的时间和精力构建相同的系统。问题是声明式工具依赖于一种前瞻性的工程思维——这意味着没有办法从一个活跃的系统中获得反馈——导致用户的许多抱怨。

## 漂移的裂缝

配置漂移是当声明性正向工程模型不再匹配系统状态时发生的情况。当开发人员更改了模型的代码而没有更新使用该模型构建的系统时，就会发生这种情况。这也可能是由于工程师进行了探索性的特别操作并更改了系统，但未能返回模板并更新其代码。

禁止运营商临时探索现实吗？实际上，一些公司有政策禁止任何操作员或开发人员接触真实的生产环境。具有讽刺意味的是，当一个生产系统崩溃时，它的第一条规则就被忽略了:任何能够找到问题根源的人都欢迎特别的探索。

采用 IaC 的工程师通常不喜欢改造现有系统的工作。尽管如此，由于用户的挫折感引发的高需求，每种配置管理语言都有一种工具——它们只是辜负了工程师的期望。最好的情况是，工程师可以使用逆向工程模板将片段复制并粘贴到一个模板中，但需要在其他地方手动编写。

## 弥合差距

我们需要一种新型的 IaC 工具。这些必须将逆向工程整合到核心，并允许来自生命系统的反馈来更新创造它们的模型。在这样做的时候，运营商可以采用特别的改变或者简单地回复到在原始模型中声明的系统。

然而，今天的标准工具达不到这一目标，也不能很好地帮助工程师解决系统操作问题。的确，有些人能够审计模板并挑出错误配置和错误。尽管很有帮助，但更大的价值是能够检查一个有生命的系统，而不仅仅是工程师最初用来创建它的模板。

我们有监控和可观察性工具和 IaC 工具，但是在它们之间有一个很大的鸿沟。对于有效的 DevOps，需要的是一种新型的 IaC 工具，它集成了支持运营工程师的逆向工程实践，并使公司能够弥合任何开发差距。