# 私人执业:加密暴露

> 原文：<https://devops.com/private-practice-encryption-exposed/>

2014 年 9 月，随着 iPhone 6 的推出，苹果将加密设置为默认设置。然后，在 2016 年 2 月，一名洛杉矶法官发布命令，迫使苹果公司帮助闯入属于一名参与大规模枪击事件的恐怖分子的加密 iPhone。

苹果公司使用了一些最强的加密技术和实践来保护其用户和他们的数据。加密技术不区分合法用户和非法用户。虽然这个问题有很多方面，但它引发了许多关于安全、隐私和公民权利的重要辩论。

## 躲猫猫

对于希望在应用程序中添加加密库的开发人员来说，有许多开源组件可供他们使用。当然，任何试图给应用程序添加加密的人都对它所提供的隐私和安全性有着重要的要求。

加密的一个更受欢迎的选择是 Bouncy Castle Java Cryptography 库的[军团。根据“2016 年软件供应链状况”报告，记录显示去年所有版本的弹力城堡组件被下载了 1740 万次。其中，580 万个(33%)是充气城堡的已知易受攻击版本。](https://www.bouncycastle.org)

![peekabo](img/f0298cfdcd8be5fdd0af7a0bb7b55fe6.png)

这是一个令人清醒的事实，但这是事实。仅去年一年，组织就下载了 580 万次弹力城堡加密库的易受攻击版本。缺陷组件下载发生在 197 个国家/地区的 13，824 个组织的 93，253 个唯一 IP 地址上。

## 思考不同

想想吧。弹力城堡项目由密码学专家开发。偶尔，他们的加密库被发现有缺陷，项目所有者迅速修复并发布新版本。如果您使用没有已知漏洞的最新版本，您的应用程序、用户和数据都会受到保护。如果您使用包含已知漏洞的版本，您已经选择性地拒绝了这些保护。

使用开源组件的两个关键原则是**使用最高质量的组件**和**从最好的供应商中选择组件**。在这种情况下，Bouncy Castle 项目在发布新的和改进的版本方面做得非常好。虽然有缺陷的版本仍然存在，但那些寻求保护应用程序、用户和数据的人需要使用最高质量的版本。

## 您使用的是哪个版本？

确定你正在使用的 Bouncy Castle 或任何其他开源组件的版本很简单。有许多免费和付费的服务可以帮助您分析您的应用程序，并报告所用组件的完整列表，包括依赖项。

一些免费服务要求您上传应用程序进行分析，而其他服务则在内部执行。用于创建软件材料清单的免费内部工具的一个例子是 Sonatype 的[应用健康检查](http://www.sonatype.com/download-application-health-check)应用。另一个例子是 [OWASP 依赖检查](https://www.owasp.org/index.php/OWASP_Dependency_Check)应用。这些工具的精度可能会有所不同，但是无论您使用哪种工具，您都应该使用一种。

关于用于构建现代应用的开源组件的质量、安全性和完整性的更多见解，请参见“ [2016 年软件供应链状况](http://www.sonatype.com/ssc2016)”报告。