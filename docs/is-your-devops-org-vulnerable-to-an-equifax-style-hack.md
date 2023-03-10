# 开源:你的 DevOps 组织容易受到 Equifax 式的攻击吗？

> 原文：<https://devops.com/is-your-devops-org-vulnerable-to-an-equifax-style-hack/>

《财富 100 强》中超过一半的公司可能面临遭受去年在 Equifax 造成破坏的同类黑客攻击的风险，这一切都归结于糟糕的开源组件治理。

《财富》的一份新报告称，在 Apache Software Foundation 发布 Apache Struts 框架更新以修复一个众所周知的关键反序列化漏洞后的一年里，超过 10，000 个组织下载了易受攻击的版本。根据 Sonatype 提供给《财富》杂志的数据，其中有 57%是财富 100 强。

众所周知，该漏洞引发了 2017 年 Equifax 的灾难性泄露，泄露了 1.48 亿人的记录。这是一个惊人的漏洞——一个允许未经授权的远程代码执行的命令注入漏洞——这种漏洞让攻击者在受影响的系统中获得强大的立足点。

Nick Bilogorskiy 说:“对于组织来说，七个月的时间应该足够安装必要的补丁，但不幸的是，许多人仍然选择下载旧的易受攻击的版本。“这真的没有任何借口。”

对于 DevOps 组织来说，这个消息应该是发人深省的。他们越来越多地转向以组装为中心的软件交付模式，这种模式严重依赖于开源组件，而不是开发人员用新代码重新发明轮子。它为 DevOps 组织敲响了警钟，让他们认真对待跟踪和保护他们使用的第三方代码。

在最近由 451 Research 代表 Synopsys 进行的 [DevSecOps 调查中，40%的组织没有对他们的软件进行任何类型的软件组成分析。这是有问题的，因为这意味着组织通常不知道易受攻击的开源组件(如 Apache Struts)何时被编入他们的代码库。](https://www.synopsys.com/software-integrity/resources/analyst-reports/examining-devops.html)

更令人不安的是，更少的组织拥有可以实际控制何时、何地以及在他们的软件开发中使用什么开源组件的系统。根据 Sonatype 进行的 [different DevSecOps 调查，62%的组织对其应用程序中的组件没有任何有意义的控制。](http://www.sonatype.com/2018survey)

这是一个令人不安的统计数据，考虑到当今开发中开源组件的使用量——无论是否在 DevOps 商店中。在上个月 RSA 大会上举行的 DevOps Connect 活动中，Derek Weeks 发表了题为“[我们都是 Equifax](https://www.youtube.com/watch?v=IvcTAOdWnQg) ”的演讲，他强调了一个事实，即在过去 10 年中，开源组件下载请求增加了 87 倍。

“增长率和消费量是巨大的。它将进入你的组织，”Weeks 告诉听众。“由于这种行为，您的开发人员正在构建的应用程序现在有 80%到 90%是开源组件，这些组件不是由您从头开始编写的代码构建的。”

Sonatype 的调查显示，今年几乎有三分之一的组织怀疑或已经证实他们在过去 12 年中遭受了与开源组件相关的违规行为。

-[契柯夫斯基](https://devops.com/author/ericka-chickowski/)