# 如何构建可操作的日志记录系统

> 原文：<https://devops.com/how-to-build-actionable-logging-systems/>

日志通常被认为是一个不需要太多思考的自动过程。一般来说，我们可以从任何系统中看到日志，并理所当然地认为这些日志包含了所需的信息。然而，考虑日志策略和架构对于故障排除和性能效率是极其重要的。不管你是如何记录日志的，日志记录最重要的部分，在简单地把日志放在第一位之后，是拥有你可以实际使用的日志。可操作的日志提供了足够的信息、足够的细节和足够的历史，以确保您可以使用日志来完成工作。

让我们检查一个示例系统。这个示例系统是一个应用程序，具有微服务架构，运行在 RHEL 机器上的 Kubernetes 集群上。默认情况下，您从操作系统和 [Kubernetes](https://kubernetes.io) 获取日志。但是要获得不同微服务的日志，您必须在构建代码库时将这些日志编程到您的应用程序中。那么，如何成功地建立有用的、可操作的日志呢？

## 三个主要考虑因素

当您考虑构建可操作的日志时，请考虑以下因素。

### 足够的信息

您的日志应该提供足够的信息来回答任何事件的“时间”、“人”和“地点”。例如，假设您想要访问日志。如果您的系统有一个访问事件，该访问事件的日志行应该会告诉您该访问是何时发生的；这就是所谓的时间戳。日志行还应该包括谁访问了系统的信息。通常，这些细节以 IP 地址或其他标识符的形式出现，而“谁”不仅应该包括人类交互，还应该包括其他系统的动作。总是记录每次访问！最后，日志行应该包括访问系统的位置，即访问了哪个服务或平台的哪个部分。

### 足够的细节

您的日志应该提供足够的细节来告诉您在任何单个事件中到底发生了什么。简单地回答谁、何时、何地并不能真正告诉你发生了什么，一个基本的答案，如“这个 pod 启动了”，并不能提供足够的细节来区分触发 pod 重启的代码更改和触发 orchestrator 重启 pod 的系统崩溃。

### 足够的历史

最后，您的日志应该提供足够的历史来理解为什么会发生一些事情。总的来说，日志有助于您理解所采取的操作的上下文。将日志行写到某个终端而不存储它们是没有意义的。单个日志行不能为您提供足够的上下文来理解任何操作或事件的“为什么”。对于一个没有易于访问的历史的系统，您如何判断一个事件是否正常？

所有这三个组件对于创建可操作日志的计划来说都是必要的，这些日志实际上可以用来了解发生了什么、为什么会发生以及如何处理这种情况。如果您可以从日志中回答谁、什么、在哪里、何时以及为什么，那么您可能拥有可操作的日志，并且正在达到或超过日志记录最佳实践。

## 下一级考虑事项

一旦您考虑了这些更高层次的考虑因素，您就可以考虑日志本身的本质了。当我考虑日志记录的实用性时，我会考虑以下主要因素:日志级别和数据需求、格式和结构以及安全性和合规性

### 日志级别和数据需求

正确使用日志级别可以确保收集和存储您需要的数据，并且只存储这些数据。在现代环境中，记录会变得非常嘈杂、非常快。日志级别提供了对日志进行微调的能力，以便只存储您需要的内容；这可以帮助你在紧急情况下快速找到信息，而不是像谚语所说的那样大海捞针。此外，当有噪音时，如果有人能够降低噪音并微调信息，他们更有可能保持日志记录功能打开，而不是只有一个开关。

不同的编程语言使用不同的日志级别组合，但是它们都有主要、次要和调试日志的一般类别。正如您可能猜到的，所有环境都应该打开主要日志。一般来说，次要日志是在您需要能够理解数据流而不必知道细节的环境中打开的。最后，调试日志通常在开发或 QA 环境中打开，并且只有当您需要了解每个细节时才打开——例如当您正在寻找可能在以后变成问题的问题时。您需要确保在代码中设置必要的日志级别，因为它们不一定是自动的，但是采取这一额外步骤是值得的。

### 格式和结构

你需要考虑谁或者什么是你的日志的主要受众。如果您打算自己筛选日志，您可能不会介意基于文本的格式。然而，大多数现代日志记录使用机器来解析日志，使成堆的数据更加有用。在这种情况下，您应该使用结构化日志记录；JSON 是结构化日志的标准，因为有太多的工具可以使用这个标准。

### 安全性和合规性

安全性和合规性日志记录可能([并且已经！](https://devops.com/?s=logging%20for%20security%20and%20compliance))一整篇文章，自成一家。然而，简而言之，日志记录是了解并主动监控其安全性的兼容系统的关键支柱。如果您的堆栈没有将所有内容记录到一个或多个仅附加的日志文件中，这些文件存储在安全的位置，而只读归档文件存储在单独的位置，那么您就面临着攻击者进入并修改或删除日志的风险，因此您无法跟踪他们在整个系统中的操作。

你的日志记录过程也不应该以明文或易破解的密码存储个人身份信息(PII)。如果您确实需要以某种形式在日志中保留该 PII，或者在不需要时将其删除，那么最好将该 PII 保存在安全的散列数据库中，并使用与数据库相关的唯一标识符(UID)。

### 一起工作

所有这些建议都很好，直到你意识到你无法从其他人那里获得足够的支持来确保每个人都遵循相同的最佳实践。一般来说，最好在整个组织内就日志标准和实践达成一致。这也将有所帮助，因为在不同系统上工作的任何人都将从相同的基线开始，并且如果他们在紧急情况下来帮忙，不必理解另一个团队的标准。跨多个系统工作的运营团队也会喜欢这些标准。要让每个人都坐到谈判桌前，首先要满足他们的每一个需求。询问人们在日志记录方面的问题，并倾听他们的回答。你可能需要解决人们的假设、误解、自满和怨恨。关键是听；直到每个人都感到被倾听和被认可，你才会得到认同。

为了让每个人都在同一页面上，您应该首先根据可操作日志的组成部分，从整个组织的角度来确定您对日志的需求。确保每个人都有一席之地，并有能力讨论和发掘所有需求，这样就没有人会试图绕过团队的决策。一个团队的需求不会与另一个团队的需求相匹配，因此您需要确保所有的观点都被听取和考虑。然后，组织相关的需求，并为这些需求设定标准。一旦你同意了你的新标准，一起更新你的系统。这需要时间，就像解决任何技术债务一样！从较小的系统或不太重要的系统开始，这样您就可以监视标准在现实生活中的表现，以及每个人的需求得到满足的程度。如果需要，在所有人同意的情况下进行调整。需求和标准会改变，就像你的系统会改变一样，它们需要适应来满足你的团队的需求。如果你花时间让每个人都坐到桌子上，并确保每个人都在船上，你会更好。

## 成功需要什么

日志可能看起来像是简单的“管用”的魔法，但是在你拥有一个成功的、有用的系统之前，有很多事情需要考虑。您需要有足够信息、详细信息和历史记录的可操作日志。您需要考虑各种系统所需的数据，如何构建这些数据，以及如何确保安全性和合规性。最后，您需要确保您的团队遵守标准，这样日志记录才能尽可能有用。但是，如果你做到了所有这些，你会发现日志变成了一种跨团队和组织交流的好方法，以确保你交付最好的产品。