# ShiftLeft 宣布微软的代码通知运行时保护。Net 框架

> 原文：<https://devops.com/shiftleft-announces-code-informed-runtime-protection-for-microsofts-net-framework/>

**T1。Net 开发者现在可以自动为每个软件版本的每个版本创建自定义安全性**

### **加州圣克拉拉，2018 年 9 月 26 日** —应用安全领域的创新者 shift left Inc .今天宣布其面向微软的安全即服务平台全面上市。Net 框架(。网)。。Net 开发人员现在可以利用商业源代码分析解决方案来自动创建自定义的安全配置文件，在运行时保护他们的应用程序。

随着企业对其软件开发实践(如敏捷方法、云基础设施、开源库、DevOps 自动化和微服务架构)进行现代化，他们在功能发布速度方面的效率提升给传统安全实践带来了压力，传统安全实践在很大程度上仍然是手动的。".微软 Azure 云原生计算首席项目经理 Gabe Monroy 表示:“Net Core 的前沿开发工具集吸引了想要最新最好的开发团队。“shift left 通过在开发和生产过程中完全自动化持续的应用程序安全性，消除了手动安全瓶颈。Net 开发者在竞争中又多了一条腿。”

最普遍的漏洞。Net 应用程序是信息泄漏，如无意中将关键数据推到外部日志、代码库或数据库[2]。与依赖高度不准确的模式匹配来识别数据泄漏的传统方法不同，ShiftLeft 从应用程序内部绘制数据流。ShiftLeft 识别哪些对象和变量是关键的，并绘制它们在源、转换和接收器之间的路径，无论它们是微服务、开源库、商业 SDK 还是第三方 API。

“随着欧洲的 GDPR 和加利福尼亚州等州采用类似的隐私法，数据保护不再仅仅是金融和医疗保健行业的问题。ShiftLeft 首席技术官兼联合创始人 Chetan Conikee 表示:“对于所有行业来说，必须视为关键的数据类型和数量都在飞速增长。" ShiftLeft 现在启用。Net 开发人员可以自动确定新版本是否在无意中泄露数据，例如在 Splunk 中记录设备令牌或在 S3 记录未加密的信用卡号码。”

作为。Net Core 和 Azure 已经接受了开源，在。Net 应用程序正在快速增长。基于 NuGet(软件包管理器)的最新统计数据。Net)，存在 127，558 个独特的包，迄今为止由应用程序开发者/供应商发起的峰值为 110 亿次下载。

在开源包中发现的漏洞可能会影响包含这些漏洞的应用程序。在披露每个新漏洞时，应用程序开发人员必须评估此类漏洞在其应用程序的特定使用环境中是否可被利用，这是一项手动任务，每个漏洞可能需要几个小时。

ShiftLeft 的信息流跟踪器旨在将应用程序的源代码及其库作为一个单元进行分析，以确定不受信任/受感染的输入是否会(或不会)触发特定的漏洞。这是在 ShiftLeft 分析一个新版本的几分钟内完成的。

“直到现在，。ShiftLeft 首席执行官兼联合创始人马尼什·古普塔说:“网络安全团队面临着一个可怕的选择:要么放慢创新速度，要么发布不安全的代码。“在不到 10 分钟的时间内，代码属性图可以确定应用程序在构建过程中易受攻击的原因和位置，并在漏洞未修复的情况下阻止生产中的漏洞利用企图。这意味着，即使是最先进的 CI/CD 环境现在也可以随心所欲地发布，而不必担心安全性会降低发布速度。”

**关于 Shiftleft**

shift left Inc .是特定于应用程序的云安全领域的创新者，提供业界首个全自动安全即服务(SECaaS)解决方案，该解决方案了解每个应用程序的每个版本的独特安全需求，并为其创建自定义安全和威胁检测。借助 ShiftLeft，DevOps 可以将威胁检测作为其 CI/CD 流程的一部分。ShiftLeft 的方法允许团队既能立即保护他们的应用程序，又能增强他们代码的安全性。该公司由一个在安全和云基础设施领域拥有丰富背景的团队创建，他们是沙盒、下一代防火墙、下一代电子支付网络和欺诈建模等技术以及多项开源计划的早期创新者。总部位于加州圣克拉拉的 ShiftLeft 得到了贝恩资本风险投资公司和梅菲尔德公司的支持。更多信息，请参见[https://www.shiftleft.io/](https://www.shiftleft.io/)。

[1] [https://www.shiftleft.io/press/shiftleft-achieves-highest-ever-sast-score-on-owasp-benchmark/](https://www.shiftleft.io/press/shiftleft-achieves-highest-ever-sast-score-on-owasp-benchmark/)[2] [https://www.veracode.com/sites/default/files/Resources/Reports/state-of-software-security-focus-on-application-development.pdf](https://www.veracode.com/sites/default/files/Resources/Reports/state-of-software-security-focus-on-application-development.pdf)