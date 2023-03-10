# 积极技术公司发现 WAGO 工业控制器的漏洞

> 原文：<https://devops.com/positive-technologies-identifies-vulnerabilities-in-wago-industrial-controller/>

*攻击者可以访问控制器文件系统，造成故障，并扰乱工艺流程*

**俄罗斯莫斯科，2021 年 6 月 7 日—**积极技术专家 Vyacheslav Moskvin 和 Sergey Fedonin 披露了 WAGO 750-8207 工业控制器固件中的两个漏洞，其中一个非常严重。750 系列控制器[用于](https://www.wago.com/global/automation-technology/discover-plcs/controllers-750)可再生能源在众多设施中的建筑自动化:石化工业中的变电站和其他配电设施、供水和其他公共设施、造船、海洋和海岸结构、机械工程以及其他领域。制造商发布了[安全更新和降低风险的建议](https://cert.vde.com/de-de/advisories/vde-2021-014)。

漏洞 CVE-2021-21001 位于 CODESYS 2.3 运行时组件中，该组件是 WAGO 控制器固件的一部分。利用此漏洞需要控制器的授权和网络访问权限。

“WAGO 给这个漏洞的 CVSS 3.0 评分是 9.1，”积极技术公司 ICS Security 负责人 Vladimir Nazarov 说。“通过利用此漏洞，攻击者可以以读写权限访问控制器文件系统。PLC 文件系统的更改可能会导致工艺流程中断，甚至导致工业事故。”

第二个漏洞，CVE-2021-21000 (CVSS 3.0 评分 5.3)，在 WAGO 开发的 iocheckd 服务中发现。它设计用于检查 PLC 的输入和输出，以及显示 PLC 配置。要利用这个漏洞，不需要授权，只要有网络访问权就够了。攻击可能导致控制器突然关闭，进而中断技术进程。

要修复该漏洞，建议组织遵循 [WAGO 的通知](https://cert.vde.com/de-de/advisories/vde-2021-014)中的建议。利用持续信息安全监控和 ICS 事件管理的解决方案，例如 [PT 工业安全事件管理器](https://www.ptsecurity.com/ww-en/products/isim/)，可以检测到对该错误的利用(例如，如果无法安装更新)。

**关于积极的技术**

Positive Technologies 是全球领先的企业安全解决方案提供商，提供漏洞和合规管理、事件和威胁分析以及应用程序保护。对客户和研究的承诺为积极科技赢得了工业控制系统、银行、电信、网络应用和 ERP 安全领域最权威的声誉，并得到了分析师团体的认可。

ptsecurity.com，[facebook.com/PositiveTechnologies](https://facebook.com/PositiveTechnologies)，[facebook.com/PHDays](https://facebook.com/PHDays)。