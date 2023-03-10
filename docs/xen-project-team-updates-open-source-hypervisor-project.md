# Xen 项目团队更新开源虚拟机管理程序项目

> 原文：<https://devops.com/xen-project-team-updates-open-source-hypervisor-project/>

开源 Xen 虚拟机管理程序背后的团队今天宣布为该项目提供了一个更新，增加了更好的嵌套性能，更强大的实时补丁功能，改进的安全性和对 Linux 子域的支持，使在专门的域内执行代码成为可能。

此外，Xen Project Hypervisor 4.14 增加了在 Hyper-V 下作为来宾运行 Xen 的能力，Hyper-V 是微软在 Azure 云上采用的 Hypervisor。

Xen 项目顾问委员会主席 George Dunlap 表示，后一种能力将更容易创建集中管理的混合云计算环境，该环境跨越网络边缘的 Xen 轻量级实例和运行在 Microsoft Azure 云中的 Xen 实例。Xen 是由 [LF Edge](https://devops.com/lf-edge-moves-open-networking-push-forward/) 开发的 Edge 虚拟化引擎(EVE)的核心组件，该引擎与 Xen 项目一样，正在 Linux 基金会的支持下开发。

Dunlap 还指出，IT 团队可以采用 Xen Project Hypervisor 在虚拟机上运行容器，这使得集中管理从边缘到云的容器化应用程序的部署成为可能。

Xen Project Hypervisor 4.14 除了支持代号为 Milan 的下一代 AMD EPYC 处理器外，还扩展了对 4GB 和 8GB RAM 设备的 Raspberry Pi 4 支持。

最后，Xen Project Hypervisor 4.14 增加了对恶意软件更快自检的支持；以确保以正确的顺序实施的方式实时修补安全补丁的能力；和控制流工具来对抗面向返回的编程(ROP)攻击。

Dunlap 指出，Xen 团队继续致力于无秘密 Xen，这可以防止内存被映射为旁路攻击的一部分。

Golang 绑定也进行了扩展，使得使用 Go 编程语言在 Xen 上开发代码变得更加容易，并且增加了在没有驱动程序或驱动程序损坏的情况下迁移虚拟机的能力。

虽然虚拟机并不缺乏选择，但 Dunlap 表示，它们越被视为商品，组织就越有可能选择依赖开源项目，因为许多组织都认为没有足够的差异化价值来保证支付商业许可证。

现在说组织将在多大程度上继续依赖虚拟机还为时过早。许多 IT 团队现在这样做是为了提供一层隔离，这通常被认为对安全性至关重要。其他 IT 团队开始更多地依赖部署在裸机服务器上的容器或仅用于隔离工作负载的轻量级虚拟机实例。

无论前进的道路如何，运行虚拟基础架构公共层的平台越多，管理混合 it 环境就越容易。真正的挑战是，在一个开发人员经常在任何地方发现虚拟机就启动虚拟机的时代，如何能够实施这种水平的 IT 纪律。