# 为什么你的软件供应链可能是你的致命弱点

> 原文：<https://devops.com/why-your-software-supply-chain-might-be-your-achilles-heel/>

从历史上看，网络罪犯既懒惰又善于创新。他们可以想出巧妙的利用和攻击手段，但他们通常仍然关注目标最丰富的环境中的低挂果实。最近，攻击者似乎已经转移了注意力，不再直接瞄准具有强大安全性或丰富资源的公司，而是瞄准软件供应链中的薄弱环节。

无论您投入多少资源或精力来保护您的网络和数据，如果您信任易受攻击的第三方供应商或销售商，一切都可能是徒劳的。软件供应链也是如此，因为开发和部署软件的过程为攻击者提供了可乘之机。

## Xcode Ghost 案例

iOS 设备被认为是非常安全的。iOS 并非不受攻击或利用，但它比竞争对手 Android 平台更安全。iOS 的应用也被认为更安全，因为苹果的应用商店是一个“有墙的花园”，对一个应用的批准有严格的审查过程。

然而几年前，人们发现[苹果应用商店中的 4000 多个应用程序包含恶意代码](https://en.wikipedia.org/wiki/XcodeGhost)。攻击者已经想出了如何利用软件供应链中的弱点来绕过围墙花园的门卫。

他们是怎么做到的？iOS 的应用都得用 Xcode 写。Xcode 软件是免费提供的，但苹果服务器通常很慢——尤其是在试图从中国下载时，所以开发者通常只是在网上搜索，从第三方网站获取 Xcode。网络罪犯开发了 Xcode 的恶意版本，然后对系统进行游戏，以确保他们的软件版本会出现在在线搜索的顶部。

使用恶意 Xcode 软件开发的应用程序包含额外的代码，这些代码会呼叫总部，并为攻击者提供后门程序，以及在受损的应用程序中注入恶意代码或执行命令的机会。

## 低垂的果实

Xcode Ghost 事件是软件供应链攻击的一个很好的例子，也是攻击者追逐低挂果实的一个完美例证。iOS 相对安全。苹果应用程序商店受到保护，应用程序受到审查，以确保它们符合严格的标准。因此，攻击者没有试图攻击苹果或 iOS，而是想出了如何攻击用于开发应用程序的平台，并通过后门潜入。

我与帕洛阿尔托网络公司的情报主管瑞安·奥尔森就软件供应链受到攻击的威胁进行了交谈。他解释说，攻击者知道，当他们追求一个难以直接击败的硬目标时，有一个更好、更容易的方法:只要找出他们信任的人，然后追求低挂的果实。

在开发运维及自动化环境中，这可能会成为一个更大的问题。最近的 NotPetya 勒索病毒是通过恶意更新传播的。如果您的系统或软件被配置为自动更新和/或部署，软件供应链攻击可能会无处不在，并在您意识到之前危及您的应用程序或数据。

有一些工具可以在部署之前扫描映像、应用程序或容器，但它们通常会测试已知的漏洞或公开的崩溃或冲突。它们不是为了寻找可能隐藏在代码中的潜在后门而设计的。

奥尔森建议你开始仔细看看你所依赖的软件供应商。了解他们如何保护自己的代码是非常重要的，因为他们的弱点会让你因为信任他们和他们的应用程序而面临威胁。

托尼·布拉德利