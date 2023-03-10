# 具有 SDO 和 Open Horizon 的板载边缘计算设备

> 原文：<https://devops.com/onboard-edge-computing-devices-with-sdo-and-open-horizon/>

**作者 Joe Pearson，工程战略和创新负责人，IBM 边缘计算**

对于许多公司来说，跨远程站点设置异构边缘设备群一直是一个耗时且有时困难的过程。本周在 [开放网络& Edge 峰会](https://events.linuxfoundation.org/open-networking-edge-summit-north-america/) 会议上，IBM 宣布英特尔的安全设备部署(SDO)解决方案现已完全集成到 Open Horizon 和 [IBM Edge 应用管理器](https://www.ibm.com/cloud/edge-application-manager) 中，并作为技术预览版提供给开发者。
英特尔开发的 SDO 可在设备初始上电时实现所需软件的低接触自举。对于 Open Horizon 项目，这使得代理软件能够自动和自主地安装和配置。SDO 技术现在正被纳入由 FIDO 联盟开发的新行业 onboarding 标准中。开发人员可以使用一体化版本的 Open Horizon 来尝试这一点。只需在目标边缘计算设备或虚拟机上运行一个 [单行脚本](https://open-horizon.github.io/quick-start) ，然后 [模拟启动支持 SDO 的设备](https://github.com/open-horizon/devops/blob/master/mgmt-hub/README.md#-try-out-sdo) 及其启动。
Open Horizon 和 SDO 最近都加入了 LF Edge umbrella，该组织旨在为独立于硬件、芯片、云或操作系统的边缘计算建立一个开放、可互操作的框架。感谢 IBM 加入 [LF Edge](https://www.lfedge.org/) 开源社区，社区中的贡献者正在 [帮助推进](https://www.lfedge.org/2020/07/07/lf-edge-drives-cross-ecosystem-collaboration-publishes-industry-defining-white-paper-on-multi-functional-edge-computing-adds-projects-and-members/) 开源计算解决方案的未来。
**简化边缘设备上线**
我们的团队使用术语“设备上线”来描述在边缘计算设备上安装和配置所需软件的初始引导过程。对于 Open Horizon，这包括将其连接到 Horizon 管理中心服务。我们通过提供一行脚本简化了软件安装过程，因此用户可以在笔记本电脑或小型虚拟机上安装和运行 Open Horizon 和 SDO 的开发版本。
在 SDO 可用之前，典型的安装流程需要一个人打开到设备的安全连接(有时在本地)，手动安装所有软件先决条件，然后安装 Horizon 代理，对其进行配置，并向管理中心注册。启用 SDO 支持后，管理员只需在购买设备时将 [凭证](https://fidoalliance.org/specs/fidoiot/FIDO-IoT-spec-v1.0-wd-20200730.html#OVIntro) 加载到管理中心，然后关联配置。当技术人员打开设备电源并将其连接到网络时，设备会自动找到 SDO 服务，出示凭证，并自动下载和安装软件。
**将 SDO 集成到 Open Horizon 中**
[Open Horizon](https://developer.ibm.com/depmodels/edge-computing/blogs/open-horizon-joins-linux-foundation-grow-open-edge-computing-platform/)项目创建了一个专门用于将 SDO 项目组件集成到 Open Horizon 管理中心服务和 CLI 中的存储库。SDO rendezvous 服务与管理中心一起运行，并提供一个简单的接口来批量加载导入凭证。
[访问 SDO GitHub](https://github.com/open-horizon/SDO-support)
**LF Edge 和开源领导**
LF Edge 组织继续努力确保边缘计算解决方案保持开放。2020 年 5 月， [IBM 向 LF Edge 贡献了](https://developer.ibm.com/depmodels/edge-computing/blogs/open-horizon-joins-linux-foundation-grow-open-edge-computing-platform/) Open Horizon。由于英特尔也 [为 LF Edge](https://www.lfedge.org/2020/07/07/lf-edge-drives-cross-ecosystem-collaboration-publishes-industry-defining-white-paper-on-multi-functional-edge-computing-adds-projects-and-members/) 贡献了 SDO，这确保了完整边缘计算框架的另一个重要组件也是开源的。
我们很高兴能与英特尔合作，将应用的部署从开放的混合云环境扩展到边缘，使它们对开发人员生态系统和社区来说是可访问的、安全的和可扩展的。
**参观我们的展台观看演示**
虚拟演示将在本周的大会上首次亮相。视频将在虚拟展台和 LF Edge YouTube Open Horizon plalist 上提供，IBM 和英特尔的代表将到场回答问题。
展位安排是:

*   9 月 28 日星期一。美国东部时间上午 9:00-10:15 开放。美国东部时间下午 4:00–5:30 进行展位搜索。
*   9 月 29 日星期二。美国东部时间上午 9:30-11:30 开放。
*   9 月 30 日星期三。美国东部时间上午 10:00-11:30 开放。