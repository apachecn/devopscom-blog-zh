# AWS re:Invent round up:Private 5G | graviton 3 ARM 芯片| DevOps Guru++

> 原文：<https://devops.com/aws-reinvent-roundup-private-5g-graviton3-arm-chips-devops-guru/>

欢迎来到[](https://devops.com/author/richi/)*——在这里，我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么才是真正重要的**。*

*本周:亚马逊网络服务的三件事引起了我的注意:发明 2021 会议:私人 5G，Graviton3 芯片，以及一种叫做 RDS 的 DevOps Guru 的东西(是的，真的)。*

 *## 私有 NRaaS 与 Wi-Fi

本周第一条新闻: *AWS Private 5G* 是一项新的交钥匙服务，为 Wi-Fi 无法覆盖的地方提供本地私人蜂窝数据基础设施。尽管名为 4G/LTE，但它提供了 5G/NR 的备用方案。因为是 AWS，硬件是免费的——你只需**支付使用费**。

### 分析:结合一个前哨来获得更锋利的边缘

Wi-Fi 不可靠且功耗低。3.5 GHz 以上的 5G“公民波段”似乎是一个很好的替代方案(只是不要告诉反 5G 大队的极端分子)。

当然，AWS 很容易购买——亚马逊会“免费”向你提供所有私人无线电设备，并根据容量和使用情况向你收费。它是自动配置和远程维护的。你只需要把你的网络连接和插上电源就可以了。

[Aisha Malik](https://techcrunch.com/2021/11/30/amazon-announces-the-preview-of-aws-private-5g/ "read the full text") : **亚马逊发布新 AWS 私有 5G 托管服务预览**

“AWS Private 5G”…是一项新服务，旨在让您轻松部署和管理自己的专用网络。… AWS 首席执行官 Adam Selipsky 表示，通过 AWS Private 5G，您可以在几天内建立和扩展一个专用移动网络，而不是几个月。
…
没有前期费用或每台设备成本:…客户只需为他们请求的网络容量和吞吐量付费。[它]按需扩展容量。
……
AWS Private 5G 在美国提供预览版。

这比 Wi-Fi 更好吗？ [Ballu](https://news.ycombinator.com/item?id=29398181 "read the full text") 盘点方式:

*工业区域覆盖:*如果您需要 50 台 Wi-Fi 无线电设备，您可以使用 3-4 台 p4G/p5G 无线电设备提供服务。
……
*危险区域:*当您无法在所有角落或区域提供网络时，一个 p5G 无线电爆炸区域(尤其是带有波束技术的区域)可以。
…
*丢包:*相比 Wi-Fi 丢包更少(相信我，这在工业世界里是件大事)
…
*兼容性:*5G 调制解调器有什么不好(没有多少设备可用)，某种程度上是积极的。一旦对 5G 调制解调器进行投资，这些设备也可以上路了。

不出所料，[布莱恩·罗梅尔](https://twitter.com/brianroemmele/status/1465743401790312451 "read the full text")觉得自己被证明是对的:

正如我在 2017 年写的那样，一家著名风险投资公司的分析师对我大加嘲讽:亚马逊正在成为一家电话公司。
…
从人行道网络到柯伊伯卫星系统再到本地 5G。网络不再只是“哑管道”

* * *

## 重力 3: AWS ARM SoC 为 PDQ

*Graviton3* 是亚马逊最新版本的 ARM 服务器芯片。看起来它是基于实现最新 ARMv9 ISA 的 5 纳米工艺。AWS 通常声称它比上一代产品快得多，但它也有新的**安全功能**。

### 分析:酷芯片

AWS 非常重视低功耗、高性能计算。亚马逊只是一家对英伟达拥有 Arm 感到苦恼的被许可方。

正如我上周和上一周所说，ARM 芯片在数据中心越来越常见，尤其是那些重视“性能功耗比”的芯片其他 IaaS 提供商可能会抱怨他们如何减少用于冷却数据中心的能源，但从减少废热开始无疑是一个更好的计划。

[Maria Deutscher](https://siliconangle.com/2021/11/30/aws-debuts-new-compute-intensive-ai-instances-powered-custom-chips/ "read the full text") : **AWS 推出由定制芯片驱动的新计算密集型和人工智能实例**

AWS 的新亚马逊 EC2 C7g 实例面向计算密集型工作负载，如分析工具和科学建模软件。C7g 系列基于 AWS Graviton3 芯片，这是云巨头内部设计的处理器的第三代产品。
…
计划使用 C7g 实例来处理机器学习工作负载的公司可以期待人工智能性能的三倍提升。速度的提升部分是由于处理器支持 bfloat16，这是一种专门的数据格式，使应用程序能够比 FP32 更快地处理浮点数，并使用更少的内存，FP32 是历史上用于该任务的数据格式。
…
对于加密任务，Graviton3 的性能是 Graviton2 的两倍。…该芯片引入了一种称为指针认证的功能，以降低网络攻击的风险。

蒂姆·安德森一直在筛选重新发明的公告:

首当其冲的可能是 Graviton3，AWS 自制的下一代[ARM]服务器处理器。这些芯片将用于预览的新 C7g 实例，提供 DDR5 内存(比 DDR4 多 50%的带宽)和比 Graviton2 驱动的实例高 25%的计算性能。亚当·塞利普斯基以 AWS 首席执行官的身份发表了他的第一次主题演讲。他说引力子使用的能量“减少了 60%。”… Graviton 很重要，因为它是率先将更多[ARM]微处理器用于数据中心和云基础设施的公司之一，还因为如果它的运营更节能、更具成本效益，它对亚马逊的底线至关重要，抱歉，是今天的环境问题。

指针认证功能有用吗？是的，非常，斯皮吉达尔说:

非常有用。…如果性能良好，这是一个很好的额外层，使面向返回的编程更加困难。结合 NX bits，确实提高了开发/使用多种类型漏洞的难度(不是不能绕过……但是没有完美的安全性)。

* * *

## DevOps Guru 增加了 RDS 支持

用于 RDS 的 DevOps Guru】是 AWS 奇怪命名的**智能监控功能**的最新升级。

### 分析:傻名字；有用的工具

拉普拉斯和高斯是对的:你的 DevOps 团队并不都是摇滚明星。“一般”运营人员占大多数。因此，将 AWS 的监控自动化扩展到您的数据库实例应该是一个积极的步骤。

但是品牌:有人能认真对待吗？

[斯蒂芬妮·康登](https://www.zdnet.com/article/aws-brings-more-automation-to-database-management/ "read the full text") : **AWS 为数据库管理带来更多自动化**

新的 Amazon DevOps Guru for RDS 可以自动查找和修复数据库问题…帮助使用 Aurora 的开发人员检测、诊断和解决数据库性能问题。[它]可以帮助修复一系列问题，如主机资源的过度利用、数据库瓶颈或 SQL 查询的不当行为。
…
去年，AWS 推出了 DevOps Guru，这是一项使用机器学习来自动检测和提醒客户应用程序问题的服务。… Amazon DevOps Guru for RDS 建立在
…
用户可以在 DevOps Guru 控制台中查看[问题],或者通过来自 Amazon EventBridge 或 Amazon Simple Notification Service(SNS)的通知来查看。

听起来很有趣，说 [u/random_dent](https://www.reddit.com/r/aws/comments/r6hr27/comment/hmujde0/?utm_source=reddit&utm_medium=web2x&context=3 "read the full text") :

我觉得 RDS 的 DevOps Guru 听起来很有趣。您需要首先启用性能指标，它有自己的费用，但它看起来仍然不太贵，加上三个月的免费层，所以我们可以尝试一下。

我们在 RDS 性能方面遇到了一些奇怪的问题，这些问题太不稳定，无法锁定。看看这是否能给我们一些启示会很有趣。

但是那个名字！下面是托马斯·拉洛克— [@SQLRockstar](https://twitter.com/SQLRockstar/status/1466087766412783618 "read the full text") :

我已经老了，还记得 RDS 的 DevOps Guru 刚刚被称为“数据库性能监控”的时候。

和 [@shmick](https://twitter.com/shmick/status/1466088105727954945 "read the full text") 年轻到可以这样说:

这样一个令人生厌的名字

* * *

## 这个故事的寓意:**不幸考验朋友的真诚**

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#37435b4177455e545f5e19545819425c084442555d5254430a1a637b611a) 联系他。*

图片:[安德鲁·斯维克](https://unsplash.com/photos/HnIsaTBxTbI)(通过 [Unsplash](https://unsplash.com/license "Some rights reserved") )*