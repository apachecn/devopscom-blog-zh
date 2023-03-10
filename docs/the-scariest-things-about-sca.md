# 关于 SCA 最可怕的事情

> 原文：<https://devops.com/the-scariest-things-about-sca/>

这是一个食尸鬼、恶作剧鬼和大卫南瓜的时代。本着万圣节的精神，这里是软件组成分析(SCA)工具的五大最可怕的限制，足以让你不寒而栗。继续读下去…如果你敢的话！

### 1.SCA 只扫描应用程序代码

SCA 的范围是 [*可怕的* 狭窄的](https://giphy.com/gifs/mrw-boy-51Uiuy5QBZNkoF3b2Z)。当扫描易受攻击的依赖项时，SCA 仅检查您的源代码，即使用于构建您的软件的易受攻击的依赖项可能存在于您的整个开发管道中。在像 Jenkins 这样的开发工具、像 Jenkins 插件这样的开发工具插件、像 GitHub Actions 这样的构建模块、像 GitHub Actions libraries 这样的构建模块依赖以及基础设施即代码(IaC)依赖中可以找到易受攻击的依赖。如果你只是扫描应用程序代码，你应该*战战兢兢*因为这不足以抵御像网络安全管理软件产品或 Codecov 这样的现代软件供应链攻击。

好消息是，下一代 SCA， [管道组成分析](https://cycode.com/blog/pipeline-composition-analysis-the-next-generation-of-sca/) (PCA)，扫描您的应用程序代码和整个管道，寻找易受攻击的依赖项。PCA 在 SCA 的基础上进行改进，包括对交付管道每个阶段使用的工具、配置、流程、活动、组件和依赖关系的深入理解。当像 [Text4Shell](https://cycode.com/blog/cve-2022-42889-text4shell-attack/) 这样的新依赖关系被披露时，您可以确保漏洞的每个实例都被找到并得到补救。这样你就知道你没有任何众所周知的 [*骷髅潜伏在你软件的壁橱里*](https://www.flickr.com/photos/ricko19/6365441667) *。*

### 2.SCA 不能告诉你漏洞部署在哪里

漏洞修复可能是残忍的。当新的高严重性漏洞被披露时，您需要从所有可能被利用的生产环境中修复漏洞的每个实例，并且需要尽快完成。在您的代码库中识别一个像 Log4j 这样的 [漏洞是一个开始，但是在您消除生产系统中对您的组织构成真正风险的每个漏洞实例之前，您并不是真正安全的。尽管传统 SCA 可以告诉您应用程序代码中的漏洞在哪里，但是一旦代码被部署，它就不可见了。](https://cycode.com/blog/two-ways-to-address-the-log4j-vulnerability/)

PCA 使您能够了解整个开发流程，包括生产环境。这使您能够轻松地跟踪漏洞从代码到部署位置的路径，例如识别哪个 [Kubernetes 集群包含特定的漏洞。](https://cycode.com/blog/kubernetes-security-best-practices/) 这使组织能够更加敏捷地响应新披露的威胁，并确保每个漏洞实例都已得到补救。

### 3.SCA 没有将 AppSec 引擎之间的风险关联起来

一些传统的 SCA 解决方案可能能够从各种扫描引擎收集数据，但它们在各种数据点之间建立有意义的联系方面非常糟糕。正因为如此，“传统”SCA 无法提供所需的环境来对一个事件的影响以及其他相关事件如何加剧风险进行准确细致的评估。没有上下文的 SCA 会产生太多的误报——这导致你的团队浪费时间 [追逐*幽灵*](https://www.youtube.com/watch?v=Tlpc2d3TB5Y) 。

PCA 将 SDLC 所有阶段以及所有 AppSec 扫描工具中的风险和威胁关联起来。通过连接来自众多数据源的点，PCA 帮助您的安全和 [开发团队](https://devops.com/why-devsecops-should-be-top-priority/) 全面了解风险如何相互关联，以便他们能够首先最好地处理最重要的安全计划。

### 4.SCA 忽略了管道安全性和治理

现代的开发管道是复杂的，而且是紧密相连的——就像科学怪人[](https://www.google.com/search?q=dr+frankenstein+young+frankenstein&source=lnms&tbm=vid&sa=X&ved=2ahUKEwiA9dvApYH7AhXmkIkEHVX1AvwQ_AUoAnoECAIQBA&biw=1360&bih=694&dpr=2#fpstate=ive&vld=cid:7e3229bb,vid:UsOnSlh7Lns)的创造一样，它们被缝合在一起。尽管管理整个 SDLC 的安全策略是一项艰巨而痛苦的任务，但如果您想要防止 [软件供应链攻击](https://cycode.com/blog/what-is-a-software-supply-chain/) ，这是必不可少的。不幸的是，传统的 SCA 解决方案甚至无法帮助您管理管道安全和 [治理](https://cycode.com/blog/sdlc-governance-security/) 策略，如 [实施最小特权](https://cycode.com/blog/using-the-principle-of-least-privilege-for-maximum-security/) 或强化认证。

管道组成分析可以识别管道工具的错误配置，并帮助您在整个管道中实现安全控制的最佳实践。更好的是，为了防止您的工具被绕过，当 SCA 扫描等管道安全控制被删除或禁用时，PCA 会向您发出警报。

### 5.SCA 不提供对 SDLC 的可见性

传统的 SCA 解决方案只关注应用程序代码。它们不提供 SDLC 的可见性。它们不是为扫描开发和部署环境而设计的，所以它们不能保护 SDLC 的后续部分。网络安全管理软件产品是通过其 TeamCity build 服务器被渗透的，传统的 SCA 工具没有扫描到。那么如果你看不到它，你如何保护你的软件供应链呢？不要因为 SCA 工具无法扫描整个 SDLC 而受到困扰。

影响应用程序的易受攻击的依赖关系在 SDLC 中随处可见。您需要了解所有开发和部署工具——活动、设置、配置、用户等等——以保护您的应用程序。管道组成分析是从头开始设计的，旨在理解您的 SDLC，并为您的 SCA 发现提供上下文以提高准确性。它可以让您全面了解全局，减少传统解决方案产生的所有干扰。

### 管道成分分析:让您的噩梦安息吧

虽然在万圣节感到害怕很有趣，但你最不想做的事情就是被你的 AppSec 程序 吓得[*。当传统 SCA 解决方案的局限性威胁到您的睡眠时，请记住，AppSec 创新需要能够在整个 SDLC 中进行管道成分分析，因此从 SCA 转变为 PCA。PCA 堵住了这里提到的所有漏洞，有望让最糟糕的噩梦安息。*](https://www.google.com/search?q=home+alone+scream&oq=home+alone+scream&aqs=chrome..69i57j0i512l8j0i390.8061j0j4&sourceid=chrome&ie=UTF-8#fpstate=ive&vld=cid:857af6e0,vid:NSz14pbBDxg)