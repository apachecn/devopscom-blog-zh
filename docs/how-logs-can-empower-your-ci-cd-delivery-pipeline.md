# 日志如何增强您的 CI/CD 交付渠道

> 原文：<https://devops.com/how-logs-can-empower-your-ci-cd-delivery-pipeline/>

变化是软件成功的货币。这种变化和成长的需求是持续集成和持续交付(CI/CD)的基础。每年，新的行业都信奉这种不断变化的哲学，但是没有必要的数据来支持他们的决策，每一次部署都是一种风险。当您用日志数据和最佳实践日志管理来丰富您的软件交付时，您减轻了这种风险，并在您的组织中实现了快速、安全的变化。

日志通常是关于应用程序行为的最常见的信息源。它们提供了上下文和结果，比简单计数指标提供了更多的信息。尽管他们可以提供巨大的洞察力，组织经常忽视他们。许多人将日志保存在服务器上的文件中，远离需要它们的 CI/CD 管道。不一定非要这样；通过一些最佳实践，企业的每个部分都可以收集、分析和利用日志中隐藏的知识。

## **用 JSON** 给日志数据添加生命

以非结构化格式记录日志会大大增加检测日志模式的复杂性。通过在 JSON 中记录您的应用程序输出，您打开了分析所有日志的可能性。这给你一个自上而下的整个系统的视图，同时仍然保持可读性。这通过允许您查询和过滤您的日志来增强您的 CI/CD 管道，然后使您能够集中于问题并精确地诊断您的最新变更的任何不想要的副作用。

## **创建可操作的警报**

如果警报被正确定义和引导，有上下文并能被容易地解释，它们将是可操作的，增加上下文并提供更大的价值。当单个指标超过阈值时，很难提供上下文，但是日志行更加复杂。它们可以包括额外的信息来提供背景信息，使我们能够快速找到问题的根源。对于采用 CI/CD 的公司来说，这是一项必不可少的能力。

## **排列日志的优先顺序**

结构化日志通常附带一个严重性，它表明我们应该多认真地调查一个事件。信息级日志表示一切正常，但是错误需要立即引起注意。一旦您的日志有了这些标记，您就可以做出智能、自动化的决策，自动响应系统中不需要的更改。

## **对每个版本进行基准测试，以了解“正常”**

在[微服务](https://coralogix.com/log-analytics-blog/the-ultimate-guide-to-microservices-logging/)架构中工作时,“正常”是一个复杂的概念。忽略单个服务的轻微变慢可能是安全的，但是不幸的事件组合可能导致灾难。基准测试使我们能够在用户之前很早就看到这些灾难。基准测试是记录应用程序正常行为的行为。在每次从 CI/CD 管道进行部署之后，将您的新行为与之前的基准进行比较。如果事情不正常，日志会提供您需要的信息，以便果断地采取行动。它们为您的基准提供了出色的基线信号。

## **经过分析的日志可以提升您的 CI/CD 渠道**

构建 CI/CD 管道并不是最困难的部分。新功能的部署也是如此。事实上，任何想要通过 CI/CD 管道交付变更的组织所面临的最大挑战是可观察性。通过采用最佳实践方法来准备、监管和分析应用程序和系统日志，我们可以克服这一挑战，并自信地以推动我们走在市场前沿的步伐进行变革。