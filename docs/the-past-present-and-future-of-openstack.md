# OpenStack 的过去、现在和未来

> 原文：<https://devops.com/the-past-present-and-future-of-openstack/>

被称为世界上部署最广泛的开源云软件的 OpenStack 将于 2022 年晚些时候迎来其 12 周年里程碑。2012 年 9 月，OpenStack 基金会作为一个独立组织启动，以管理和推广这项技术——这是两年前宣布的一个项目的分水岭时刻。

今天，根据现在被称为开放基础设施基金会(OIF)的组织的说法，OpenStack 是三个最活跃的开源项目之一，另外两个是 Linux 内核和 Chromium web 浏览器。全球有超过 2500 万个 OpenStack 内核投入生产运行。

人们很容易忘记，就在几年前，许多人预测 OpenStack 将会消亡。最初，OpenStack 被定位为一个通用的私有云平台，提供亚马逊网络服务(AWS)的开源替代方案，但在这场竞争中，它从来没有太大的机会。

然后，在 OpenStack 重新获得动力并转向成为电信网络功能虚拟化基础设施(NFVI)的平台后，有传言称它将被新的“下一件大事”——[Kubernetes](https://kubernetes.io/)，即用于容器化应用的开源编排和协调系统超越。

回想起来，Kubernetes 作为 OpenStack 杀手的说法是愚蠢的，因为这些技术是互补的，而不是竞争的。事实上，根据 OIF，超过 70%的 OpenStack 用户报告在 OpenStack 上运行 Kubernetes 进行容器协调。

OpenStack 的采用将在 2022 年继续蓬勃发展。Gartner [预测](https://www.gartner.com/en/newsroom/press-releases/2021-08-02-gartner-says-four-trends-are-shaping-the-future-of-public-cloud) 今年全球云服务支出将超过 4800 亿美元，高于 2020 年的 3130 亿美元，因为越来越多的组织投资于混合云:一种按需付费的公共云和私有云的组合，可以提供更低、更可预测的运营成本和更大的定制化。随着混合云市场的扩大，开源在开发和 IT 组织中的地位越来越稳固，OpenStack 比以往任何时候都更加重要。

如果你不熟悉 OpenStack，这里有 10 件关于它的过去、现在和未来你应该知道的事情。

1.OpenStack 始于 2010 年初，由 Rackspace 和美国宇航局位于加州山景城的埃姆斯研究中心的工程师合作开发。Rackspace 希望重写运行其云服务器的基础设施代码，NASA 团队希望标准化航天局的网站。他们最初的使命是“生产无处不在的开源云计算平台，通过简单的实施和大规模的扩展，满足各种规模的公共云和私有云的需求。”

2.第一届 OpenStack 设计峰会于 2010 年 7 月在得克萨斯州奥斯汀举行，该项目于当月晚些时候在 O'Reilly 开源大会(OSCON)上正式启动。

3.多达 80%的 OpenStack 云用于生产，而 13%正在开发中，8%处于概念验证阶段，根据 OIF 的 [。有了这样的采用水平，难怪 OpenStack 被认为是部署最广泛的开源云软件。](https://www.prweb.com/releases/openinfra_software_adoption_surges_spurred_by_growth_in_openstack_deployments_which_now_exceed_25_million_cores/prweb18341197.htm)

4.一项 OIF [调查](https://openinfra.dev/user-survey/) 显示，近一半使用 OpenStack 的组织已经部署了至少 1000 个内核。细分如下:29%的组织拥有 1，000-9，999 个内核，13%的组织拥有 10，000-99，999 个内核，6%的组织拥有 100，000-999，999 个内核，1%的组织拥有 100 万个或更多内核。

5.一个庞大的企业生态系统支持 OpenStack，包括 IBM、Red Hat、HP Enterprise、Intel、华为、NEC、Cisco、VMware、美国电话电报公司和 Canonical，Canonical 的 Ubuntu Linux 发行版是 OpenStack 部署最受欢迎的操作系统(全球约 40%的 OpenStack 云使用它)。

6.OpenStack 在 openstack.org 上有一个很棒的资源 [指南](https://developer.openstack.org/) ，为开发者提供了各种有用的信息，包括那些平台新手。

7.人们喜欢 OpenStack 的一个主要特点是，它是一个模块化的架构，具有互连的组件，例如，公开 API 端点和处理基本云功能的服务、仪表板、存储 OpenStack 服务创建的记录的 SQL 数据库和用于促进进程间通信的消息队列。

8.OpenStack 行话包括几个特殊术语。例如，租户是拥有独立云资源的用户或用户组。(OpenStack 是多租户的。)映像是包含用于实例供应的操作系统的模板。一个风格是一个为实例供应定义云资源的模板。实例是从映像和风格中调配的虚拟机(VM)。诸如此类。

9.多年来，该平台已经扩展到包括一整套核心服务，如管理域、项目、角色、组和用户帐户的 Keystone identity 服务，管理云图像目录的 Glance 服务，Nova(例如供应、调度和终止)，Neutron network 服务和 Cinder block 存储服务。

10.除了这些核心服务之外，一些新的服务正被越来越多的人采用。例如，根据 OIF 的数据，提供裸机的项目在 2016 年至 2021 年间增加了近两倍。其他越来越受欢迎的包括奥克塔维亚，它提供负载平衡功能，Manila 用于实例之间的文件系统共享，OpenStack Charms 为服务提供丰富的生命周期管理功能。

正如这 10 点所显示的，OpenStack 非但没有奄奄一息，反而幸存了下来，并作为开源和云计算领域的一支独特力量蓬勃发展。考虑到它过去 10 年的发展历程，看看未来 10 年的前景将会很有意思。