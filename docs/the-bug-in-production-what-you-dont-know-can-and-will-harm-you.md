# 生产中的缺陷:你不知道的会伤害你

> 原文：<https://devops.com/the-bug-in-production-what-you-dont-know-can-and-will-harm-you/>

尽管存在计划外停机的风险，但许多开发软件和服务的组织在没有充分测试会影响生产流量的缺陷的情况下就将它们投入使用。这是一场巨大的赌博:这些错误可能会导致服务完全瘫痪。没有足够的测试就推出 live 可能会对您的业务不利。

## **代码中存在 bug 的问题**

软件停机会导致收入和声誉的损失。事实上， [Gartner 分析师](http://blogs.gartner.com/andrew-lerner/2014/07/16/the-cost-of-downtime/)估计停机时间的平均成本为每分钟 5，600 美元，远远超过每小时 300，000 美元。为了提供这种情况的真实例子，[微软 Azure](https://duo.com/decipher/software-update-led-to-microsoft-azure-mfa-outage) 在 2018 年 11 月遭遇了一次重大宕机，原因是作为代码更新的一部分引入的问题，持续了 14 个小时，影响了整个欧洲及其他地区的客户。随着从遗留系统到云中微环境的迁移，中断和停机造成了越来越严重的问题。

随着公司[转向 devo PS](https://devops.com/5-mistakes-to-avoid-when-chasing-devops-transformation/)和 CI/CD 模型以加快速度并更快地提供应用程序更新，软件开发人员不断发布新功能，并经常在编写代码时就推送代码更新。开发、质量保证(QA)和 beta 测试的传统六个月开发时间表已经被压缩到几天甚至几个小时。团队可以与客户进行长时间的 beta 测试以标记实时错误的时代已经一去不复返了。

使用当前的质量测试工具，开发人员不知道一个新的软件版本在生产中的表现如何——或者它是否能在生产中工作。Cloudbleed bug 就是这个问题的一个例子——2017 年 2 月，安全厂商 Cloudflare 的软件升级中的一个简单的编码错误导致了一个严重的漏洞，几个月后被谷歌的一名研究人员发现。

除了上面提到的直接影响之外，缺陷还会导致严重的安全问题。 [Heartbleed，](http://heartbleed.com/)2014 年出现的一个漏洞，源于 OpenSSL 库中的一个编程错误，将大量私钥和敏感信息暴露在互联网上，使得原本受 SSL/TLS 加密保护的[被盗。](https://www.welivesecurity.com/2014/04/09/heartbleed-encryption-flaw-leaves-millions-of-sites-at-risk/)

## **标准 QA 测试是不够的:使用生产流量进行测试**

QA 测试通常采用的方式已经不能满足当今日益频繁和快速的开发周期。传统上，DevOps 团队无法对产品版本和升级候选版本进行并行测试。许多组织使用的 QA 测试是一套模拟的测试套件，它可能无法全面洞察客户实际使用软件的无数方式。仅仅因为升级后的代码可以在一组测试参数下工作，并不意味着它可以在不可预测的生产环境中工作。

与 Cloudflare 事件的情况一样，该错误在很长一段时间内完全没有被最终用户注意到，并且没有因该缺陷而记录系统错误。正如 QA 测试是不够的一样，依靠系统日志和用户也只能检测有限的范围。

据估计，在软件发布后修复缺陷的成本可能是在设计阶段修复缺陷的五倍，并且可能导致更昂贵的开发延迟。使软件团队能够在发布之前识别潜在的错误和安全问题，可以减少这些延迟。显然，在代码开发过程的早期使用生产流量进行测试可以节省时间、金钱和痛苦。软件和 DevOps 团队需要一种方法来快速准确地测试新版本在真实(而非模拟)客户流量下的表现，同时保持最高标准。

通过并排评估发布版本，团队可以快速定位任何差异或缺陷。此外，他们还可以真正了解网络性能，同时验证升级和补丁在工作环境中的稳定性。有效地做到这一点将会大大降低发布以后需要回滚的软件的可能性。回滚是昂贵的，正如我们在微软 Azure 事件中看到的那样。

一些组织实施推广，这需要在生产中运行多个软件版本。软件团队将一小部分用户放在新版本上，而大多数用户运行现状。不幸的是，这种用生产流量进行测试的方法管理起来很麻烦，成本也很高，而且仍然容易回滚。这种滚动部署的另一个问题是，虽然可以在过程的早期发现故障，但根据设计，只有在故障影响到最终用户后才能发现故障。

这带来了更多的问题，包括:你如何知道新软件是否导致了故障？而且，在召回或回滚软件之前，企业允许多少次失败，因为企业没有观察到来自同一客户的并行结果？这会扰乱最终用户体验，最终影响业务运营和公司声誉。和阶段可能无法提供足够的样本来衡量新版本对整个客户群体的有效性。

成本仍然是一个问题。如果您让 10%的客户使用新版本，并且一次故障每小时的成本超过 300，000 美元，那么影响 10%用户的一次故障每小时的成本仍可能超过 30，000 美元。当然，影响减少了，但仍然很大——还不算何时回滚的不确定性。

## **展望未来**

标准的 QA 测试已经不够了。为了降低当今快速迭代注入到软件开发生命周期中的风险，DevOps 团队可以在生产中测试，并同时评估发布版本。这将有助于防止成本高昂的回滚或升级，同时仍然发布高质量、安全的产品。旧的做事方式是不充分的，但幸运的是，有一个更好的方法。

弗兰克·韦尔塔