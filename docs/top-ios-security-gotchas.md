# 最常见的 iOS 安全问题

> 原文：<https://devops.com/top-ios-security-gotchas/>

确保应用程序中用户数据的安全性对于建立对您业务的信任和促进客户的在线安全至关重要。

以下是苹果公司为提升你的 iOS 应用程序的安全性而提供的 10 大基本安全机制。在您的产品中采用这些技术和 API 是编写更安全的应用程序的有效步骤，可以降低潜在的数据泄露风险，并增强您对安全状况的信心。

## **选择退出系统数据保护**

iOS 提供了数据保护设置，这是一种自动加密应用程序创建的任何文件的强大方法。这是一个重要的安全设置，但是，它在默认情况下是关闭的，许多开发人员从不启用它。利用系统的数据保护机制可以轻松提高应用程序中用户数据的安全性。

## **通过不安全的连接传输数据**

确保任何传输中的数据都通过安全的连接进行传输至关重要。通过对所有应用程序的网络活动使用加密的 HTTPS 连接，各种传输中的数据受到的损害得到了缓解。此外，建议组织利用 SSL 固定来实现最大的传输层安全性。

## **反序列化失败**

在 iOS 上序列化和反序列化数据的默认协议 NSCoding 容易受到对象替换攻击，这可能会允许攻击者获得远程代码执行权限。苹果公司提供了一种近乎插入式的替代品，NSSecureCoding，它不容易受到这种攻击。为了转换一个序列化的类以使用 NSSecureCoding 机制，苹果在其 [文档](https://developer.apple.com/documentation/foundation/nssecurecoding?language=objc#) 中概述了步骤。进行建议的更改允许系统实施安全的反序列化。

## **选择退出应用程序传输安全性**

App Transport Security (ATS)是 Apple 提供的一种机制，用于协调应用程序建立的所有网络连接，并验证数据是否安全传输。通过使用 NSAllowArbitraryLoads 或类似的豁免来退出 ATS 是搬起石头砸自己的脚和关闭强大的安全机制的一种简单方法。

## **加密 API 误用**

加密用户数据是显而易见的，但必须小心确保以加密的安全方式完成。有些系统 API，比如 CommonCrypto，很容易被误用。这导致了安全的假象，同时仍然允许用户数据的攻击媒介受到危害。确保使用这些带有安全选项的 API，并且永远不要静态嵌入加密密钥或使用一个简单派生的加密密钥。

## **将 PII 泄露给 nsuserrefaults**

在一个应用程序中处理个人身份信息(PII)时，以一种方便而直接的方式存储它可能会很有诱惑力，比如使用 NSUserDefaults 条目。但是，这种方法允许设备上的任何其他应用程序读取这些潜在的敏感数据。敏感数据，尤其是可识别的用户信息，应始终储存在安全的位置，如设备的钥匙串，并在必要时进行加密。

## **不安全的钥匙圈用法**

虽然钥匙串是苹果设备上最安全的数据存储，但开发者仍必须小心确保他们正确使用它。开发人员可以将数据保存到钥匙串中，即使设备被锁定，数据也会被加密，但数据始终是不加密且可访问的。 将敏感数据保存到钥匙串时，请确保您使用了最强的数据保护设置，以最大限度地提高安全性。

在钥匙串中保存项目时，尽可能使用“kSecAttrAccessibleWhenUnlocked”，这是最强的保护级别。这个保护类告诉系统，当用户不主动使用您的应用程序时，应该对数据进行加密。如果您的应用程序需要在后台运行时访问这些数据，您可能需要依靠“ksecattraccessiblafterfirstunlock”保护类，该类可确保数据仅在用户在启动后解锁设备之前加密。

## **嵌入易受攻击的 SDK**

当一个 SDK 链接到你的应用中时，你也隐含地将你的应用暴露给 SDK 中的任何潜在漏洞。受损的 SDK 导致了各种移动应用攻击，例如易受攻击的 AFNetworking 版本通过 MitM 攻击导致数据受损。如果没有对应用中使用的 SDK 进行安全审计，开发者就看不到他们引入的潜在漏洞。

## **在敏感输入栏上允许第三方键盘**

虽然安装第三方键盘有助于用户定制，但它们也带来了新的数据泄露途径。这是因为第三方键盘的开发者可能能够提取在键盘上键入的任何信息。因此，在处理敏感数据(如可识别信息或信用卡号)时，禁用这些键盘最符合用户的利益。

## **将 PII 泄漏到设备日志**

在生产版本中很容易留下调试日志，这可能包括 PII。在发布之前，验证是否从代码中清除了任何可能包含敏感数据的日志语句。这可以通过标志来实现，标志只在调试版本中启用这些日志语句。由于物理接触设备的任何人都可以看到日志，因此从日志中排除敏感数据至关重要。

由于采用最新技术通常会带来不可预见的风险，因此防御性安全是一项持续的工作。然而，遵循这 10 大提示将提高您组织的安全态势，并减少 iOS 风险带来的漏洞。