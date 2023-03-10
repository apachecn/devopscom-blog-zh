# 作战在无作战世界中的作用

> 原文：<https://devops.com/role-operations-no-ops-world/>

似乎每隔一段时间，我们这些高科技人员就会被下一件将会消除工作和/或工作的事情所困扰。有时候，就像 DevOps 的情况一样，我们得到了一些减少多余工作的东西，从长远来看，实际上使我们的生活变得更容易。然而，大多数时候，我们不会。XML 将终结编程，Java 将让每个人都成为程序员，SOAP 意味着非程序员也可以将大量代码拼凑在一起，创建复杂的系统……这样的例子不胜枚举。

今天的旋转木马之旅是为了 Ops 和 DevOps。某些方面的爱是“无手术”——根本不需要手术！数据中心会自己运行！但是，这些说法有什么根据呢？在今天的技术下，哪里是不可能的呢？让我们来看看。

# SaaS 是今天的无操作选项

如果您现在想要一个几乎完整的无运营解决方案，请注册软件即服务(SaaS)。您仍然需要管理用户和访问——正常的 AAA 工作——但是应用程序是由其他人构建和管理的。这就像我们在今天的世界中所做的一样。

无论我们被告知什么，任何其他解决方案都需要相当数量的 ops。安装服务器——无论是在硬件上的数据中心、虚拟机中还是在云实例中——仍然需要工作。即使您有 Ansible 或 Kubernetes 这样的工具为您努力工作，并完成大部分重复性的繁重工作，您仍然可以将各个部分结合在一起，使事情正常工作。联网通常留给运营/开发团队，将服务器变成牲口需要运营的重担，即使你是自动化的。应用程序中断和故障排除在很大程度上仍然是一项手动工作，在自动帮助下找出问题所在，但修复工作仍然主要由运营部门负责。

# 暗示未来的无核武器区行动

通常情况下，声称结束部分 IT 工作负载会有一些潜在的好处，如果你不被宣传所吸引的话。请记住，在云计算的早期，有些人告诉我们，不再需要本地数据中心。当然有十亿个原因，每个环境都不一样。但不可否认的是，云开启了我们看待服务器部署的方式。无操作也是如此。有很多理由表明，它实际上不会对整个项目(更不用说整个数据中心)无操作，但这一想法有巨大的好处。

## 无服务器

在 serverless 中，您开发代码和 API，然后公开 API。该系统被设计成仅在有请求时才运行代码。应用程序防火墙通常是强制性的，内置于系统中。这部分是安全特性，部分是用于确定需要调用什么代码来服务给定请求的位置。云中的想法是，您只需在 API 运行时付费，呼叫的所有操作部分都会为您处理。这是真的，如果你接受，在无服务器中，开发人员将操作作为开发的一部分——应用防火墙配置，即使是无服务器使用的简化版本，也绝对是操作，而不是开发。调用 API 的无服务器应用程序和基于服务器的应用程序之间的故障排除至少在某种程度上取决于操作。这是必须的，因为操作人员拥有网络和互联网络知识。

不过，无服务器提供了一些很好的部署选项，不可否认地降低了操作开销。对于像云爆炸这样的事情，好处是不可否认的。它使随增长付费的云成为一个非常精细的命题，并可以通过为每个连接建立一个新的实例来消除所有代码都存在的瓶颈。

## 集装箱管理

随着容器管理工具中包含的功能越来越多，自动扩展应用程序(或者至少是应用程序一部分的实例)的能力是向无操作迈出的一大步。无需人工干预，容器管理工具可以根据连接、响应时间等扩展或收缩应用程序的内存占用。当内置路由满足组织的需求时，它还会限制促进这种扩展所需的网络数量。随着时间的推移，预计容器管理将包含更多的自动化，至少使应用程序的维护变得更容易。宣传的对应用程序执行滚动升级同时保持其运行的能力也是一个巨大的运营优势。确切地说，这不是不行动，但肯定是不那么不明智的行动。

## 开发/测试/部署

应用程序发布自动化、持续测试/交付/部署和配置自动化工具的发展都降低了运营成本。它们不会导致无操作，但它们确实促进了概念的发展，在推进开发运维概念的同时减少了操作开销。预计这些工具将继续增长。大多数配置管理/应用程序部署工具已经与一系列网络设备/装置一起工作，预计这一趋势将会继续。再说一遍，这是运营成本的降低——并非完全没有运营成本，而是朝着这个方向迈出的一大步。

## 更多

我们已经看到了一些非常酷的技术，它们超越了这里列出的内容，推进了减少运营的主题。审计的自动化和安全测试的完全自动化(结合代码分析和实时数据以获得比现在更好的覆盖率)只是两个例子。随着这些工具集的成熟，请密切关注市场。

# 继续踢它

与此同时，行动组不会消失。在扩展技能的同时保持专家的身份。正如我(和其他人)以前说过的，减少操作实践方面的工具不是威胁，而是机会。腾出的时间对那些你希望能做但没有时间做的项目很有用。或者，更好的情况是(我们可以稍后再讨论这句话)，所有那些业务部门希望您能做但您没有时间做的事情。

最终，你保持了组织的运转，并与世界相连。接受那些让你的工作变得更容易的不可操作的部分是有意义的。不要上炒作的当；捡起好的部分，继续摇摆。

唐·麦克维蒂