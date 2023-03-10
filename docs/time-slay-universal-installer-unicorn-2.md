# 是时候杀死通用安装独角兽了

> 原文：<https://devops.com/time-slay-universal-installer-unicorn-2/>

虽然许多人想要一个通用的“简单按钮安装程序”，但他们也希望它能在他们独特的基础设施、工具、网络和操作系统上工作。我称它们为雪花，因为它们的微小差异会组合扩展。这种分歧将说明性参考架构的想法变成了一个破坏性的神话，限制了社区和生态系统的发展。

因为有太多必要的变化和改变，所以最好放弃试图拥有一个安装程序的开源项目，而是专注于使它们所需的组件更具弹性和可移植性。

## 通用安装程序谬误

那么一个简单的按钮安装看起来像什么呢？让我告诉你一个我做的。

![](img/685afdb10a8e295b1a22305ae8e5ba1a.png)

Crowbar Mascot

那是 2011 年，OpenStack 时代的黎明，我们在戴尔的团队已经厌倦了尝试围绕 Azure、Eucalyptus、Joyent 和 Hadoop 进行可重复安装。简单的现实是，在部署这些平台中的任何一个时，我们都没有可以遵循的成功模式，当然也没有跨平台的模式。尽管它们都使用基本相同的计算和网络基础设施，但每个都有定制的部署代码和配置方法。我们立即成为 OpenStack 的创始合作伙伴，试图打破这种失败模式。

什么失败了？每个平台都深深嵌入了不可重复或不可移植的环境假设。

例如，其中一个平台需要三十(30！)满满一架子的设备，并拴系回主部署者，因为它的管理和拓扑是硬连线到它的基础设施中的。其他的也好不到哪里去:安装通常是“ssh apt-get 安装平台”，然后是“scp 预构建的配置文件”。更糟糕的是，这些步骤总是与每天更新的 30 页说明性手动系统准备步骤一起进行。

我们错误地认为解决方案是为 OpenStack 创建一个更好的安装程序。

SUSE 仍在使用的 Crowbar 项目创建了一个完全集成的安装序列，从 PXE 启动和发现到测试最终的 OpenStack 安装。我们可以在几分钟内用盒子在完整的齿轮架上构建云。开源项目甚至使用诸如 Chef 和硬件无关选项等开放工具来增加其社区吸引力。作为第一个安装程序(它甚至早于 DevStack)，该项目在早期 OpenStack 评估中被广泛使用。

尽管取得了成功，但作为 v1 技术，Crowbar 的主要缺点是它将组件和服务紧密耦合在一起。这使得安装和管理过程非常僵化，不符合完全不同的运营模式和环境。

我们的安装伤痕向我们展示了阻碍可移植性的真正战线。即使很小的基础设施变化也会导致不完整的或特定于站点的配置。挑战的主要部分是变异没有被整齐地包含；相反，它散布在整个环境中。我们需要创建自动化，既能应对整个社区的异构性，又能在安装后容忍变更，以支持升级。

我们开始接受没有单一的安装程序。相反，可伸缩的安装者必须假设他们将以协调的方式与系统的其他部分一起操作，因为选项的多样性使得他们不可能控制一切。事实上，我们已经看到，更小的、可组合的安装步骤更容易一致地自动化。更重要的是，更小的步骤使得以可控的方式管理系统范围的升级成为可能。

问一个“简单按钮”安装程序是一个错误的问题。相反，让我们问一问，“我们能否创建可以用多种方式自动化的可共享组件？”

没有通用的安装脚本来创建云彩虹；但是，我们可以使用一些策略来使单个项目可以在多种选项上安装。这些方法包括可组合性、一致的配置以及标准工具和操作模式的使用。这些项目有助于项目关注他们自己的问题，并允许运营商应用最佳实践技术。

基本上，项目开发商的第一步是限制他们的范围，将运营问题委托给运营商。

即使在试图对开发人员隐藏操作复杂性的平台即服务(PaaS)项目中，如 Kubernetes，仍然有人必须使用基础设施和工具来操作该平台。当我们试图将新概念应用于旧的基础设施时，我们会使这项工作变得更加复杂。对阻抗不匹配的处理将注意力从中心抽象转移开。

因为我们*确实*需要来自社区的一致安装，项目*确实*有责任帮助这些努力。

他们能提供什么帮助？通过确保他们的组件服务与清晰的输入配置、操作需求、升级模式和输出期望结合良好。

但真的，那是以后的帖子。请让我知道你的想法，以及我们该何去何从。