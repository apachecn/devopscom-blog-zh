# GitLab 向 DevSecOps 工具箱添加模糊测试

> 原文：<https://devops.com/gitlab-adds-fuzz-testing-to-devsecops-toolbox/>

GitLab 今天宣布，它已经收购了协议模糊测试和动态应用安全测试(DAST) API 测试工具提供商 Peach Tech 和连续模糊测试工具 Fuzzit，作为其推动采用最佳 DevSecOps 实践的[努力的一部分。](http://www.globenewswire.com/news-release/2020/06/11/2046908/0/en/GitLab-Acquires-Peach-Tech-and-Fuzzit-to-Expand-its-DevSecOps-Offering.html)

GitLab Secure & Defend 的产品总监 David DeSanto 表示，这两项收购应该会使 DevOps 团队更容易在应用程序开发和部署过程中更早地整合白盒和黑盒模糊测试技术进行安全测试。

![](img/cc7a6037349e5eab2e365e93e3788c48.png)模糊测试是一种自动化技术，包括向软件提供无效的、意外的或随机的数据作为输入，然后对其进行监控以查看发生了什么——例如，是否出现崩溃或内存泄漏。

Peach Tech 添加了 Peach Fuzzer，这是一个自动化的安全测试平台，它使用称为 Peach Pits 的定义文件来生成测试目标使用的模糊数据，以及一个自动化 web 应用程序编程接口(API)安全测试过程的框架。

Fuzzit 提供了一种服务，使 DevOps 团队能够持续生成模糊测试，并以一种能够[集成到持续集成/持续交付(CI/CD)工作流](https://devops.com/gitlab-releases-massive-update-to-ci-cd-platform/)中的方式关联崩溃。

一旦 Peach Tech 和 Fuzzit technologies 相互之间以及与 GitLab 平台完全集成，DeSanto 表示，GitLab Secure 客户将能够自动执行无数任务，从安全测试到漏洞管理和补救。

GitLab 还将采用这两家公司的技术，进一步推动交互式应用安全测试(IAST)的采用。DeSanto 说，我们的目标不仅是让开发者更容易使用 DevSecOps 工具，还能了解在开发应用程序时会产生什么问题。他指出，这种方法应该减少开发团队在多个应用程序开发项目中不断犯同样错误的情况。

网络安全测试越左移，长期人手不足的网络安全团队的压力就越小。面临的挑战是，虽然大多数组织都认识到了 DevSecOps 的潜在好处，但在教育开发人员应该寻找哪些问题以及为他们提供发现和修复漏洞所需的工具方面，还没有取得太大进展。

当然，在网络安全方面没有灵丹妙药。只要人类编写代码，就总会有潜在的问题。然而，在将应用程序部署到生产环境中之前，许多常规的网络安全问题就应该得到解决。为了实现这一目标，除了将更多的安全测试整合到 CI/CD 工作流中之外，组织还为开发人员提供了在他们编写代码时识别网络安全问题的工具。

当然，GitLab 并不是专注于如何促进采用最佳 DevSecOps 实践的 CI/CD 平台的唯一提供商。很明显，在 CI/CD 平台中嵌入安全测试工具的竞争应该会促进 DevSecOps 的采用，如果没有其他原因，只是因为它们变得更容易被开发人员发现和使用。