# 让 DevOps 在复杂的企业环境中工作

> 原文：<https://devops.com/making-devops-work-complex-enterprise-environments/>

欢迎回到 DevOps.com 系列，[‘企业开发 Q&A’](https://devops.com/blogs/five-top-tips-devops-scale/)。请记住，如果您有关于企业开发运维的具体问题，请告诉我，我会尽力为您解答。

今天的问题是:

**问:在大型企业中，总是存在环境差异。从公共云到内部托管，从虚拟桌面到传统主机，环境之间不可能完全一致。你有什么解决这个问题的建议吗？**

## 企业复杂性的挑战

这在大型企业中是一个巨大的问题，尤其是当 DevOps 实践不仅仅局限于孤立的部门应用程序时。架构师有一个原型系统；开发人员有不同的系统来编码；测试和质量保证有自己独特的“标准”系统；而运营有着不可触及的生产系统。

除此之外，后端到 CICS 或 IMS 应用程序、从 iSeries 上的 DB2 或 ADABAS 访问数据，或者在 HP/UX 上自动化 WebSphere 部署也很复杂；加上 AWS 上的 Oracle 数据库或 Azure 上的 SAP 客户端的许可；以及满足数据隐私和操作安全性的合规性要求。这种企业复杂性和环境不一致性通常意味着新代码在投入生产之前不会得到适当的测试，从而导致不可接受的错误数量和平均每年大约 70 万美元的停机成本！

## 没有雪花

许多人会说，你不能延续“独特的雪花”，所以你必须标准化环境。这种教条很容易宣扬——原则上是一种最佳实践——但在现实中，它对大多数企业来说过于简单。不同的环境通常有很好的存在理由(例如，适应成本、技能、吞吐量、集成或其他技术需求)。在任何情况下，您都不能简单地践踏已建立的体系结构。所以尽可能标准化，但是要意识到这条路不太可能解决问题。

## 抽象平台

当您不能完全标准化时，您仍然可以通过抽象独特的平台来实现一致性。例如:

*   将定制的 Windows 配置保存为虚拟机，然后您可以将其自动重新部署到标准化的 Linux 虚拟化平台上
*   不要忘了，UNIX 等传统系统也可以被[虚拟化，即装即用](http://www.oracle.com/technetwork/server-storage/solaris/overview/virtualization-163570.html)；甚至 IBM i 系统也可以使用 [PowerVM](https://www-03.ibm.com/systems/power/software/virtualization/) 进行虚拟化
*   使用[企业基础设施即服务](http://www.centurylinkcloud.com/) (IaaS)，无论是私有云还是公共云，托管还是内部部署，尤其是对于较新的应用程序
*   采用[平台即服务(PaaS)](https://www.openshift.com/) ，即装即用，或者(正如我的公司一直在做的那样)构建支持您独特环境的平台即服务

## 自动化复杂性

自动化还可以帮助管理企业复杂性，以减轻环境不一致性的影响。例如，企业级[配置自动化](https://www.lmgtfy.com/?q=configuration+automation)或[发布自动化](https://www.lmgtfy.com/?q=release+automation)的解决方案都可以简化开发和运营团队之间的交接，因为环境不一致会导致重大问题。或者采用像[服务虚拟化](https://www.youtube.com/watch?v=Uk_DWebImI0)这样的测试自动化技术，可以简化开发、测试、QA 和其他生产前用例，从而

[通过按需一致地复制复杂的环境，缩短了测试时间，提高了生产率，提高了生产质量](http://servicevirtualization.com/profiles/blogs/independent-research-firm-sv-works-and-it-s-gaining-momentum)。

## 工具选择很重要

不过要小心。DevOps 不全是工具，所以自动化不是一个完整的答案；尤其对于企业来说，工具选择也更加困难。对于更复杂的企业环境，您可能需要超越流行的开源/webscale/startup 工具。例如:

*   厨师和 T2 都声称支持 Linux、Windows 和 Solaris，但不支持 AIX 或 HP/UX
*   Docker 声称支持 Linux 和 [Windows 桌面](https://docs.docker.com/installation/windows/)，但不支持 UNIX 或 Windows 服务器
*   Ansible 只记录了在最近的 [beta 版本](https://www.ansible.com/blog/ansible-1.7-is-released-windows-beta-and-more)中对 Windows [控制机器](https://docs.ansible.com/intro_installation.html#control-machine-requirements)的支持
*   大多数云服务只支持 x86 架构，然后只支持 Windows 或 Linux
*   除了[詹金斯](http://www.perfectomobile.com/articles/mobilecloud-jenkins-plugin)和一些[博客](http://puppetlabs.com/blog/devops-tools-natural-fit-mobile-apps)之外，对[移动开发](https://www.google.com/search?q=Mobile+DevOps)的具体支持有限
*   只有传统的大型供应商支持传统的大型系统，如 IBM i 或 System z

而且，必须指出的是，许多“企业”工具不支持更新的环境，如 MacOS、Azure 或 Google 或者不能很好地与多样化的工具链集成。

因此，在为您的 DevOps 工具链选择自动化和其他解决方案时，请确保它们支持您的环境，从移动到大型机，无论是内部部署、托管还是在云中。

## 你的解决方案是什么？

这些是大型企业面临的一致性差距的一些解决方案，但只是皮毛。我很想听听你们用 DevOps 方法处理企业复杂性的解决方案。或者，如果您有任何企业 DevOps 问题，请告诉我，我会尽力解答。您可以在下面的评论中留下您的想法或问题；在推特上联系我，地址是@ AndiMann 或者在 [【邮件保护】](/cdn-cgi/l/email-protection#e0818e8489ce8d818e8ea08381ce838f8d) 给我发邮件。