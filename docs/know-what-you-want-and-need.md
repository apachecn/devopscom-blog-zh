# 知道你想要什么，需要什么

> 原文：<https://devops.com/know-what-you-want-and-need/>

这些年来，我们从供应商那里购买的东西发生了巨大的变化。过去，It 人员会定义一个需求，出去找一些软件来解决它，安装和配置软件，并且在大多数情况下，将大部分时间花在项目上，让它在他们的环境中正确工作。那些日子已经一去不复返了。首先，我们开始为一些功能购买设备，然后我们开始为一些或所有功能使用 MSP，然后一些供应商希望在虚拟机中提供，他们可以通过控制环境来简化配置。这是虚拟化购买的第一步。然后，我们开始考虑基础架构即服务(IaaS ),然后是 SaaS，然后是一些提供 PaaS 的供应商……目前，所有优秀的供应商都在提供容器，这是对虚拟机的一种改进，并且提供了一种可以快速运行并经过测试的虚拟设备，可以完成购买目的。或者至少测试过它的用途。我们都有这样的故事，关于我们是如何处理这些“标签外”的东西的——这些东西实际上并不是产品设计的目的。一路走来，我们还引入了开源厂商；这有点矛盾，实际上描述了基于开源项目的服务组织。有些人比其他人成功得多。

所有这些，亲爱的读者，就是我们在这里的原因。在购买之前，需要了解的东西比以前多得多。实际上，这个软件供应商卖的是什么产品？最终，它希望解决一个问题。大多数情况下，问题是由 SaaS、本地安装还是云实例解决，都不如问题解决得如何重要。但是实施和许可对一个组织来说很重要，即使不是立即重要，也是长期重要。

当购买一个[开源](https://devops.com/?s=open+source)“产品”时，你……其实不是。您将获得产品和购买支持。由于只要有足够的时间，开源软件可以被黑客攻击到任何地方运行，不止一个 OSS 供应商声称这使他们优于针对特定平台的商业产品。这显然是不真实的——除非 OSS 供应商在任何地方都支持该产品，当然，他们不是。我可以将 OSS 项目 MyFunApp 移植到我想要的任何平台上，而不需要支付支持费用，当我在 OS/2 上启动并运行它时，它不会为我做任何事情(作为一个极端的不存在的例子)。

谈到总拥有成本，SaaS 有更多的问题。虽然“随增长付费”很酷，但永远固定每月付费是一个很大的进步，应该予以考虑。而在一个企业，“永远”是需要现实考虑的。实施一个特定的 SaaS CRM，你就不太可能转移到另一个，即使你声称你会在心跳。是工作。很多工作。这肯定是可能的，但对大多数组织来说，不太可能。所以，要知道你正在进入的是什么。在评估时，不要忘记考虑可变费用，大多数 SaaS 产品都有可变费用。确保你了解每月的实际费用可能是多少。正如我们许多人所了解的那样，IaaS 也面临着同样的可变性问题。

[容器](https://containerjournal.com)是实现类似设备功能的一个非常好的解决方案——将容器放入您选择的 Kubernetes 口味中，然后继续前进。这里的问题是扩散的组合——需要多少？举例来说，随着时间的推移，每个 pod 一个会变得很贵。无论平台如何，这些资源都不是免费的。另一个问题是更新。自动更新是容器实例交付产品的标准。从安全角度来说，你应该有疑问。更新你网络中的东西可能需要你的批准。

我并不是说一种交付方式比其他方式更好；我只是建议，我们都需要比过去更慎重地考虑这些选择。不仅要了解 SLA，还要了解每个选择的成本和支持含义，这在今天和未来都很重要。

继续踢它，继续挑选最能解决组织问题的解决方案。请注意，有时，交付方法引入的问题会破坏解决方案的有效性。