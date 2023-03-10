# FLAP，第 1 部分:服务器供应

> 原文：<https://devops.com/flap-part-1-server-provisioning/>

我们已经达到了实现端到端数据中心配置的状态。现在还为时过早，所以还需要做一定的工作，但是今天一个 DevOps 团队基本上可以打开自动化并转移到其他 DevOps 优先事项上。根据所选的解决方案，这需要一些努力，但最终结果是一个基础架构，只需按一下按钮，即可安装操作系统(OS)、硬件(如果需要)和应用，以及整体配置。

目前，有许多解决方案可供您的数据中心使用，这个由三部分组成的系列将探讨这些解决方案。在第一部分中，我们将讨论服务器配置，这一部分将您从未安装的服务器或虚拟服务器转移到为您的环境配置的正常运行的操作系统。接下来的两篇文章将介绍应用程序供应以及将两者合并以实现 FLAP。(是的，我编了 FLAP。用不用，你看着办吧。)

**免责声明:**我为这个领域的一家供应商工作。虽然我认为这不会影响我的客观性，但我会记下我的雇主被提到的地方，并让读者来决定我是否对基于我的关联的某些项目/问题视而不见。

## 服务器供应:什么和谁

服务器配置系统将物理或虚拟服务器从无到有，直至完全安装操作系统。这层襟翼是自动化整个过程的基础。如果系统必须手动安装，使用工具和脚本来安装应用程序并不能像整个过程自动化时那样提供整体优势。

在本次讨论中，我们将坚持使用现有的主要资源调配工具。当然还有更多，我也有关于它们的信息，但对于这篇简短的博文，我们将坚持那些具有特殊之处的公司——市场份额、历史、整合、关联——这使它们成为一个很好的长期赌注。我们的列表是按字母顺序排列的，并不显示排序的偏好。

### [补鞋匠](https://cobbler.github.io)

Cobbler 是最初的服务器自动化工具集之一，它的历史和稳定性绝对值得您关注。对于使用大量 Fedora 和 CentOS 的商店来说，结合 Spacewalk 的 Cobbler 特别有吸引力，我们稍后会谈到。支持包括大多数 Linux 发行版。用户已经创建了将 Windows 包含在可安装操作系统列表中的方法，但是还没有针对 Windows 的官方解决方案。

Cobbler 集成了 Ansible、Spacewalk、Saltstack、Puppet(用户创建)和 Satellite 的旧版本。有一些关于补鞋匠的未来增长的担忧，只是因为红帽在 6.0 版中把卫星从补鞋匠中移走了，尽管红帽仍然支持补鞋匠。现在预测这将如何结束还为时过早，但目前它似乎已经激励了补鞋匠核心团队做更多的工作。相关用户应该查看 [GitHub analytics](https://github.com/blog/1672-introducing-github-traffic-analytics) 以了解提交者和提交者在评估时的趋势(对所有这些产品来说都是好建议，但对有未来问题的产品来说更相关)。

Cobbler 的硬件支持比大多数都好，在应用程序支持方面，它是一个纯粹的服务器自动化工具；根本不支持应用程序—应用程序配置需要处理这方面的问题。

### [领班](https://theforeman.org)

Foreman 是一个开源项目，目前正在享受红帽的赞助，但支持不仅限于红帽 OS。事实上，Foreman 将安装几乎任何风格的 Linux，并且可以针对大多数物理/虚拟/云平台。使用 WDS，工头也可以安装窗户。

Foreman 的一大优势是它的互操作性——它不太关心您使用的是哪种应用程序供应工具。它被集成到 Satellite 中(使用 Puppet)，并支持所有其他主要的应用程序供应工具。这意味着无论你用什么来安装应用程序，Foreman 都值得你去安装服务器。

像大多数产品一样，Foreman 提供 CLI、API 和 GUI。相对于市场而言，它们相对稳定，原因很简单，因为 Foreman 比大多数竞争对手更早地实施了它们，并在不断改进它们。

简而言之，如果你处在一个有着广泛的操作系统、架构和应用需求选择的环境中，Foreman 应该是你的首选。对于更具针对性的解决方案(就操作系统而言，无论是云还是应用调配工具)，将特定特性/功能与此列表中一些更具针对性的工具进行比较更有意义。

### [马斯](http://maas.io)

马斯是自动化世界沉睡的巨人，但它看起来确实正在苏醒。MaaS 是 Canonical 的 Ubuntu 项目的一部分，因此有大量的支持，但从历史上看，它的目标是适度的，其文档更是如此。在夏季/秋季的某个时候，这种情况发生了变化，MaaS 显示出对操作系统越来越多的支持，更好的文档和更专注的尝试。如果你主要是一个 Ubuntu 商店，它是非常值得考虑的。

像该产品中的大多数产品一样，MaaS 使用 PXE 将机器安装到其系统中，然后使用已导入的预定义映像(Ubuntu 映像不需要导入)将机器从裸机/虚拟安装到工作操作系统。MaaS 宣布支持 CentOS、RedHat、SuSE、Ubuntu 和 Windows。对于那些不熟悉这个领域的人来说，这是一个令人印象深刻的列表。但是这位作者最后一次使用 MaaS 的时候，它仍然只有 Ubuntu，所以我不能对每个操作系统的支持水平/质量发表评论。尽职调查应该包括用您的组织需要的那些操作系统进行测试。

有些安装程序最薄弱的地方就是非标准的硬件，比如 RAID 控制器，专用网卡之类的。MaaS 支持这些组件，并在其打包中包括 UCS 支持。只有 MaaS 和 Stacki 会直接提到 UCS 支持，所以如果您是 UCS 商店，这是值得考虑的。

除了 CLI，MaaS 还推销 API 和 GUI。从 DevOps 的角度来看，这些都是重要的工具，因为 API 允许您将 MaaS 绑定到您的自动化架构中，GUI 有助于发现特定于 MaaS 及其领域的问题。特别有趣的是，日志集合清楚地显示了每台服务器的安装结果和操作结果。

MaaS 的一个主要缺点是其有限的应用程序供应支持——它与 Juju 很好地集成在一起，但没有这个领域中的其他大牌产品。

简而言之，对于使用 Juju 的 Ubuntu 商店来说，这是一个放在你的短列表顶端的工具。对于其他人来说，这个工具是可行的，但是应该根据其他工具的特性/功能来考虑。

### [剃须刀](https://docs.puppetlabs.com/pe/latest/razor_intro.html)

剃刀是木偶的较新的裸机安装程序。它还很年轻，仍然有问题需要解决，但是致力于 Puppet 的大量开发人员表示，Razor 将随着时间的推移继续改进。目前，它直接支持大多数版本的 Linux 和 Windows 安装。Razor 的问题在另一端:它被设计为与 Puppet 一起工作，对其他应用程序供应工具的支持很低——事实上，仅限于用户设计的解决方案。不用说，由于它是由傀儡赞助的，预计这一领域的官方工作将仍然缓慢，因为它不是一个优先事项。

Razor 没有专用的 GUI 相反，它使用 Puppet 的 GUI 来报告结果。与整合一样，这对于木偶商店来说是可以的，但对于其他商店来说，这几乎排除了 Razor 的考虑。(在本系列的未来博客中会有更多相关内容。)

因为 Razor 是新产品，该产品有几个严重的警告。首先，install 是市场上最差的产品之一，有许多预安装步骤、许多安装步骤，并且需要手动配置一系列底层系统。其次，您不希望 Razor 重新安装的每个当前安装的服务器必须在命令行上手动输入 Razor。这在广义的数据中心环境(Puppet 在其中大放异彩)中是如此的受限，以至于您可以预期这种限制会很快得到解决。

简而言之，对于那些没有看到他们的应用程序供应工具发生变化的傀儡商店来说，这是一个应该放在您的首选列表上的工具。对于其他商店，值得先看看竞争对手，因为剃刀需要木偶。

### [Stacki](http://www.stacki.com)

Stacki 是由 StackIQ 赞助的开源项目(正如承诺的，这是我的雇主)。Stacki 的历史可以追溯到十多年前，他专门从事 RedHat/CentOS 安装以及对集群软件的额外支持。在撰写本文时，CoreOS 和 Ubuntu 已经被添加到 Stacki 支持的操作系统列表中，并预计该列表将随着时间的推移而增长。

Stacki 最大的吸引力在于管理系统的方式多种多样。所有这些应用程序都会自动检测网络上的新服务器，抓取并安装它。Stacki 增加了在电子表格中列出应该全新安装的服务器的功能，下次每台机器启动时都会安装，但其他机器不会安装。虽然在所有这些系统中都有模拟这种功能的方法，例如，您可以通过 Razor 中的命令行将例外添加到“安装在该子网上引导的所有机器”规则中，使用电子表格来明确管理要安装哪些机器以及如何提供管理安装和重新安装的离线批量方式。

在撰写本文时，Stacki 还没有 API，只有通过商业插件才能拥有 GUI，但是随着社区开始指导开发工作，这些东西中的一个或两个都会发生变化。Stacki 经过优化，可以在几分钟或几小时内部署数百台服务器，而不是几周或几个月，随着越来越多的服务器上线，利用点对点并行安装程序可以更快地进行安装。虽然它在较小的环境中工作得很好，但当有大量服务器需要管理时，它真正发挥了自己的作用。在初始安装方面，当这个列表中的其他系统需要手动安装和/或配置先决条件和子系统时，Stacki 作为一个 ISO 提供了一个 UI，可以询问一些问题并配置所有内容。

Stacki 已经与大多数(Ansible、Puppet、Saltstack)本系列博客将考虑的主要应用程序供应工具一起使用，使它在应用程序方面更加通用。

总的来说，如果你是一家经常使用 CentOS 的红帽店，尤其是一家较大的商店，Stacki 应该是你的首选。对于其他人来说，这个工具是可行的，但是应该根据其他工具的特性/功能来考虑。

请继续关注本系列的第 2 部分，其中将介绍应用程序供应。