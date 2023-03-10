# 云原生应用中的依赖性会放大风险

> 原文：<https://devops.com/dependencies-in-cloud-native-apps-can-amplify-risks/>

**云原生应用中隐藏的依赖关系会放大安全风险**

云原生应用程序和现代开发实践产生了高度分布式和松散耦合的应用程序。在许多情况下，组织无法控制或很少了解他们在应用程序中使用的不同元素和软件实体。结果往往是隐藏的依赖关系，这会影响性能并增加安全风险。

《纽约时报》提到了一个隐藏依赖后果的例子。文章引用了研究人员的工作，他们观察到，随着疫情期间航空旅行的减少，天气预报模型的质量下降了。人们可能很容易猜测这其中有物理上的因果关系。喷气发动机的废气包括水蒸气、烟灰、二氧化碳、未燃烧的燃料和几种氧化物。也许由于商业飞行的减少，这些微粒数量的减少对平流层下部的动力学有一些影响。

事实证明情况并非如此。[文章报道](https://www.nytimes.com/2020/10/29/climate/slump-in-air-travel-hindered-weather-forecasting-study-shows.html)研究人员发现“当短期预测模型从飞机上收到的温度、风和湿度数据较少时，预测技能(预测的气象条件和实际发生的之间的差异)就更差。”

根据这篇文章，商业和货运飞机上的仪器进行的大气观测是“预测模型中使用的最重要的数据之一”。测量结果被实时传输到世界各地的预报机构，包括国家气象局。

疫情导致航班减少。因此，数据很少或没有。由于这种数据中断导致的预测降级不仅会影响主要的预测应用程序，还会对下游产生许多影响。例如，这些短期预测被许多行业(物流、农业、娱乐、公共安全等)用于制定商业决策。因此，由于之前未知的依赖性而导致的该应用程序的性能下降可能会传播到第三方应用程序，这些第三方应用程序只是依赖该应用程序的输出作为其输入。从某种意义上说，这种特殊的相关性(较少的观测值导致较差的预测质量)在许多其他应用程序中变成了一种不同的隐藏相关性。

**安全隐患**

正如这个例子所说明的，复杂系统中的小变化可能会对应用程序性能产生意想不到的影响。它们还会带来意想不到的安全问题。

问题的核心是，今天的云原生应用程序是复杂的系统。云原生系统中的安全性可能会受到微小变化的影响。

这可能就像重用一个组件一样简单，该组件的原始权限设置只允许开发团队出于测试目的访问某些数据。随着软件组件重用变得非常普遍，这一点可能会在某个时候被遗忘，代码可能会被其他团队使用。这些群体可能只想要数据库中的匿名记录或不包括应保持隐私的记录的数据子集。在更大的云原生应用中使用这些代码不一定会暴露数据。但是有人可能会发现这个错误并加以利用。

[云原生应用安全](https://webinars.devops.com/the-next-thinking-regarding-cloud-native-application-security)的另一个方面是，许多模块化元素通过 API 和微服务调用链接在一起，形成一个更大的应用。这些软件元素(无论是开源的还是商业的)通常都有安全缺陷。

哈佛大学创新科学实验室和 Linux 基金会去年的一份报告强调了这个问题，指出需要“理解和解决现代软件供应链中的安全复杂性。”随着组件的频繁重用，即使一个已知的漏洞已经用补丁解决了，问题也可能无法消除。有人需要知道这段代码在一个分布式的云原生应用程序中，有一个漏洞补丁，并且应用了补丁。

任何像这样的小缺陷都会对整个云原生系统的安全性产生更大的负面影响。

**需要什么**

云原生应用程序对[开源](https://devops.com/how-to-stop-copying-and-pasting-flaws-using-open-source-code/)和第三方代码的依赖要求安全性贯穿应用程序的整个生命周期。事后测试漏洞已经不够了。在大型应用程序的任何一个元素中使用的第三方或开源代码可能会随时更改。如果引入了漏洞，开发人员可能并不知道。

因此，在庞大的云原生应用中协同工作的离散代码的相互依赖性要求对安全性有新的认识。应用程序的不断刷新、更新和替换决定了安全性必须是应用程序整个生命周期中不可或缺的一部分。因此，公司必须将安全性引入应用程序生命周期，就像 DevOps 为开发和部署所做的那样。

为了发现这些影响，领先于它们，并在它们出现时做出有效和高效的反应，开发人员和公司需要深入了解他们系统的上下文以及所有部分如何协同工作。正如与大流行相关的商业航班下滑会影响预测模型的准确性一样，云原生应用程序某个部分中看似不相关(或未知)的安全缺陷也会影响整个应用程序。

为了避免这样的问题，越来越需要一种 DevSecOps 方法来发现由许多相互连接的部分组成的当今应用程序中隐藏的依赖性所导致的弱点和漏洞。