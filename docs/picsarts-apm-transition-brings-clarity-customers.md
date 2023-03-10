# PicsArt 的 APM 过渡为客户带来了清晰性

> 原文：<https://devops.com/picsarts-apm-transition-brings-clarity-customers/>

PicsArt 的技术前景

PicsArt 使其创意用户群能够在全球网络社区中自由上传或绘制、编辑和交换数字图像。PicsArt 可以在网络和 [Android](https://www.android.com/) 、 [iOS](https://www.apple.com/ios/) 和 [Windows Phone](https://www.microsoft.com/en-us/windows/phones) 平台上运行。

PicsArt 应用最先进的后端基础设施为其社区提供编辑应用程序和社交范围。PicsArt 使用流行的 DevOps 技术，如 [MongoDB](https://www.mongodb.org/) 数据库、[节点。JS](https://nodejs.org/en/) JavaScript 运行时，和 [Redis](http://redis.io/) 内存数据工具。在这些工具和基础设施的基础上，PicsArt 构建并支持应用程序，这些应用程序为用户创造和欣赏原创数字艺术提供了许多免费选项。

PicsArt 首席技术官 Mikayel Vardanyan 表示，PicsArt 应用和技术每天都要处理数百万次用户请求。“我们还将很快向我们所有的开发者提供一个公共 API，让他们有机会使用我们的后端服务来创建自己的应用，”Vardanyan 说。虽然这将满足客户对额外功能的需求，但它也将进一步增加 PicsArt 系统的复杂性，使得它们从基础到顶峰的正确运行变得更加重要。

PicsArt 经历了和其他科技公司一样的陷阱，并做出了回应

与任何技术系统一样，PicsArt 的基础设施也面临着停机的风险，随时都有可能影响业务和挑战客户满意度。不可预见的事件以及计划内的维护中断会造成停机，并且是系统生命周期中的预期部分，尽管它们并不总是受欢迎的。

但是故障和停机可能会恶化开发运维流程，破坏和削弱用户体验。停机可能会暂时中断整个服务，当服务不可用时，客户肯定会注意到并错过这些服务。“例如，如果用户不能上传他们的照片，那肯定对我们不利，”Vardanyan 说。

PicsArt 后端系统上足够长的停机时间也会导致用户注册功能失败。后端还支持 PicsArt 的社区活动，如分享艺术作品、喜欢他人的艺术作品和评论人们的创作，这些活动可能会受到影响。“我们试图通过提供冗余和可扩展的系统来防止停机。“我们定期对我们的系统进行适当的测试，”Vardanyan 说。

“当我们开始意识到此类问题时，我们的运营团队会立即着手解决我们需要解决的问题。Vardanyan 说:“我们会调查遇到的所有问题，并通过增加更多冗余和可扩展性层来应对。

PicsArt 向 APM 寻求图像完美改进

PicsArt 希望提高其基础设施的可见性，以便从一开始就监控上述问题，创建故障问题警报和状态报告，并获得整个基础设施在国家与国家、地区与地区之间发生的情况的指标。

PicsArt 知道它需要广泛的监控，最好的方法是将监控集中在一个产品中。“我们需要全天候监控基础设施，以便为我们的社区提供最好的服务，”Vardanyan 说；“我们需要外部和内部监控，我们需要监控用户体验”。

APM 很好地解释了性能挑战

PicsArt 目前使用 [Monitis](http://www.monitis.com/) 。在 PicsArt，系统一直在努力应对紧迫的负载和负载平衡。如果系统性能由于任何原因而滞后，网络将成为最薄弱的环节和最大的瓶颈。“我们利用 Monitis 的不同警报功能，如语音呼叫和短信，并使用其通知系统提供的所有升级程序。Vardanyan 说:“我们还使用 Monitis 为某些脚本和 Redis 作业创建定制监视器。

基于云的监控解决方案使数字艺术编辑和共享平台提供商能够利用来自多个全球有利位置的视图，澄清 PicsArt 基础设施的透明性。“通过 Monitis，我们可以检查我们的全球 CDN 位置，并找出哪个位置可能有问题。好处是一个潜在的问题重重的位置不会逃脱例行的监控，”Vardanyan 说。企业越早发现它，就能越快修复它。

在一个单一的仪表板中进行剖析的便利性和效率使 PicsArt 能够修复其 DevOps 和平台交付过程中的实际问题，而不会触及任何没有失调的地方。