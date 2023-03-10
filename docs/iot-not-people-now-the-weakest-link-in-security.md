# 物联网，而不是人，现在是安全方面最薄弱的环节

> 原文：<https://devops.com/iot-not-people-now-the-weakest-link-in-security/>

快速搜索“人的最薄弱环节”，你会看到大量的文章，其中网络安全专家和计算机科学家指出员工或最终用户是最大的漏洞。毫无疑问，人们会做一些愚蠢的(或者公然滥用)事情，为各种各样的企业安全问题打开大门。剧透:有一种技术被称为物联网(IoT ),它比人们面临的安全风险更大。这个快速变化的物联网安全故事的新主题是数据完整性。

网络安全风险增加的部分原因是物联网应用接触的各种环境。大多数大规模物联网部署使用某种形式的三层架构，包括边缘、网关和云组件。

*   **边缘设备**是那些连接的传感器和接触真实世界的致动器。它们通常是小型、低功率设备，通常运行无线协议，如蓝牙、线程、ZigBee、Z-Wave、亚 GHz、低功率广域网(LPWA)、蜂窝物联网技术、Wi-Fi 或其他协议。
*   **网关设备**是一组传感器连接的集线器。网关的一个重要作用是将来自边缘设备的各种协议转换成网际协议(IP ),以便传输到企业网络中。网关在安全供应边缘设备方面也发挥着关键作用。运行 Android 或 iOS 的智能手机通常充当消费者物联网设备的网关。对于工业物联网设备，多协议网关通常构建在运行实时操作系统或 Linux 的小型计算机上。边缘计算或雾计算架构使用增强型网关进行更多算法处理。
*   **云平台**是大多数企业开发者非常熟悉的。在物联网应用中，来自边缘的数据将被处理、存储和呈现。算法可以在服务器集群或分布式计算框架(如 Hadoop 或 Apache Spark)上运行。商业智能以及预测性和规范性分析也驻留在云中。

在我们的实践中，我们看到许多物联网网络安全问题可以通过适当关注以下两个方面来缓解。首先是通过使用基本的互联设备安全措施来阻止简单的端点攻击。避免带有众所周知的默认密码或 PIN 的边缘设备-破坏这些默认设置可以像拔掉电池和重置出厂设置一样简单。如果设备使用加密，确保它不使用硬编码的密钥，如果被破解，会危及整个家庭。寻找使用空中下载(OTA)编程的边缘设备，允许在较长的生命周期内进行安全更新。随着越来越多的设备开发人员获得物联网安全经验并提供正确的功能，关闭这些基本的最薄弱环节就很容易了。

现在，对于更令人吃惊的最薄弱环节。物联网应用运行的时候，数据有什么好的？根据刚刚发布的对 950 名 IT 和业务决策者的调查，[只有大约 48%的公司有信心能够检测到物联网安全漏洞](https://www.gemalto.com/press/pages/almost-half-of-companies-still-can-t-detect-iot-device-breaches-reveals-gemalto-study.aspx)。(顺便说一句，不要让我从区块链开始；这是一种工具，不是万灵药。)在你的人参与进来之前，可能会发生很多事情。到那时，可能就太晚了。

数据完整性需要在大规模物联网部署期间持续监控，而不仅仅是在试点期间。进入未受保护的物联网网络的一种简单方法是在网关处添加未经授权的边缘设备，然后使用它来访问其他设备。端到端加密中的漏洞也很容易被利用。不可信的公共云元素也是坏消息，这是我们推荐混合云架构的一个重要原因。私有云层让您能够更好地控制算法性能和数据流安全性。呈现和归档可以留给公共云层面。

坏数据可能来自受损或有故障的设备。它会在系统中快速传播，当表示层的不知情用户在其上运行商业智能工具时，坏数据可能会导致问题。团队如何找出导致数据和结果损坏的漏洞和错误？

*   雇佣一个渗透测试人员，最好是一个从你的日常开发中脱离出来的承包商，他可以在试验阶段客观地评估你的架构，并在部署阶段重新评估它。
*   确保您的架构能够容忍边缘设备或网关故障，而不会在算法中产生连锁反应；换句话说，保护应用程序不会在坏数据流上长时间运行。
*   在将人工智能转向自动决策之前，考虑一种基于人工智能的物联网安全分析工具，以发现异常并快速将人们纳入循环。
*   将至少一部分网络安全专家重新定位于正在进行的数据完整性工作，并帮助他们跟上物联网技术和趋势。

这听起来像是 DevOps 的一份好工作，不是吗？你知道如何对待他人；现在你需要用设备施展魔法。当物联网应用程序在无人值守的情况下一直运行到呈现时，长期以来认为人是最薄弱环节的安全公理不再成立。当人们在边缘有更多的交互时，有一些例外，特别是在医疗设备领域。一般来说，我们会看到越来越大的物联网应用程序，数据越来越多，处理越来越多，与人的交互越来越少。

如果物联网上有人说有一个你可以驾驶卡车通过的安全漏洞，他们可能真的是这个意思。数据完整性措施对于开发运维团队的发展至关重要。你同意吗？您在物联网应用中遇到了哪些类型的数据完整性问题？

— [唐·迪丹吉](https://devops.com/author/don-dingee/)