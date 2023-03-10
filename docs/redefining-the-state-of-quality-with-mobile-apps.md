# 通过移动应用重新定义质量状态

> 原文：<https://devops.com/redefining-the-state-of-quality-with-mobile-apps/>

虽然许多组织都在寻求敏捷方法来更快地交付移动应用，但他们也面临着在整个组织中采用这种方法的挑战。移动应用敏捷的基础是关注“质量状态”，或者需要知道你的代码是否有效，你的应用是否也有效。许多组织面临的主要问题是:DevOps 团队正在半途而废地进行敏捷开发。他们执行夜间构建，但是没有人知道质量的状态。

是什么限制了对质量状态的了解？有三个因素:

1.  首先，不稳定或有限的测试自动化功能会影响可以运行的非单元测试的数量。测试自动化能力经常类似于一片瑞士奶酪——它看起来很好，但是肯定有漏洞。
2.  其次，不稳定的开发环境导致了变通办法，例如不可伸缩的脚本或跳过影响测试环境的主要因素，例如与 wifi 的弱连接。稳定开发环境对于敏捷移动应用程序开发生命周期的其余部分至关重要，而变通办法不是一个可持续的解决方案。
3.  最后，周期外测试会多次影响质量，由于复杂性，组织将测试部分，如负载测试，排除在生命周期之外。这意味着在移动应用程序的生命周期中，从来没有对质量状态的真正了解。

为了弄清楚如何知道任何一天的质量状况，组织需要采取“没有代码遗留”类型的过程。不断地将质量嵌入到移动应用的生命周期中，将确保代码和应用能够正常工作。

以下是实现这一目标的步骤:

*   **切掉瑞士奶酪:**通过实现满足需求的广泛而稳定的自动化来对抗有限的测试自动化。在选择自动化引擎之前设置这些要求:
    1.  你需要与设备交互还是只与应用程序交互？
    2.  你需要分析屏幕上的内容吗？
    3.  万一系统崩溃，需要自我恢复吗？
*   **工作人员相应:**设备根据定义是不稳定的。人类更稳定。组织可以通过相应地为环境配备人员，让一些人可以处理测试，从而使环境变得稳定。
*   **利用混合云:**创建一个永远在线的测试实验室，并有专人负责。这减少了诸如 USB 连接问题、违反安全准则、Mac 支持等陷阱。让一个局外人来管理一个测试实验室会打破你的循环。
*   **进入周期:**周期外的测试部分也会打破你的周期。构建一个支持各种测试案例并引入异常值的环境，例如不同的网络条件、同时连接的多台设备、容量问题以及始终准备好进行负载或安全测试的能力。
*   **教育组织**:在拥抱[持续质量](http://www.perfectomobile.com/solution/what-is-continuous-quality)的过程中，教育你的员工在云中使用自动化测试的好处和力量，以及他们将在自己的工作中看到的结果。

一个开放和集成的环境，并提供尽可能少的限制，将允许开发人员在一个舒适的地方产生创造力，并提供对质量状态的可见性。持续的质量是确保你的应用运行良好并更快发布的唯一方法。

***作者简介/约兰***

[![Yoram-Mizrachi-ws-new](img/b4af96525c9ce5830da9c725a0d355ea.png)](https://devops.com/wp-content/uploads/2015/04/Yoram-Mizrachi-ws-new-e1429762839849.png) 约拉姆·米兹拉奇是[完美移动](http://www.perfectomobile.com)的 CTO。Yoram 为 Perfecto Mobile 带来了在网络、安全和移动通信方面的丰富经验。Yoram 在担任 Comverse 移动数据部门 cto 后，创立了 Perfecto Mobile。在这个职位上，Yoram 处理了移动应用、WAP 和基于位置的服务方面的各种技术问题。1999 年，Yoram 是 Exalink 的 CTO(也是创始人)，该公司后来被 Comverse 以 5.5 亿美元收购。在创建 Exalink 之前，Yoram 曾在通信和密码学领域担任多个技术相关职位。