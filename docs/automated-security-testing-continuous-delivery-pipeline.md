# 连续交付管道中的自动化安全测试

> 原文：<https://devops.com/automated-security-testing-continuous-delivery-pipeline/>

自动化单元、集成和验收测试是运行可靠的持续集成或持续交付管道的基本质量控制。由于错误地认为安全测试仅仅是穿皮夹克的安全专家的领域，安全测试经常被排除在这个过程之外。

### 安全测试不需要特殊处理

我们已经在自动化许多重复的质量测试任务方面取得了长足的进步，我们可以使用同样的方法来自动化安全测试。出于安全性和质量的考虑，智能人工测试总是有需求的，但这并不意味着所有的**安全性测试都必须手动驱动。很大一部分安全测试本质上是检查已知的弱点没有被引入，这些非常适合自动化。事实上，使用人工来执行这些类型的检查是对资源的极大浪费。**

从自动化的角度来看，安全测试可以分为以下几类:

1.  **功能安全测试**。
    这些基本上与自动化验收测试相同，但是目标是验证安全特性，比如
    认证和注销，是否如预期的那样工作。它们大部分可以使用现有的验收测试浏览器自动化工具，如 Selenium/WebDriver 来自动化。
2.  **针对已知弱点的特定非功能测试**。
    包括测试已知的弱点和错误配置，例如会话 cookies 中缺少 HttpOnly 标志，或者使用已知的弱 SSL 套件和密码。这些特别适合自动化，因为弱点是预先知道的(如果开发团队不知道，那么安全团队也知道)。更重要的是，这些测试有助于 TDD 方法，因为在构建应用程序和环境之前，它们可以**作为安全规范**。
    在将这些类型的测试提取到安全测试自动化框架方面已经做了一些工作，参见: [BDD-Security](http://www.continuumsecurity.net/bdd-intro.html) (我是作者)、F-Secure 的 [Mittn](https://github.com/F-Secure/mittn) 和 [Gauntlt](https://github.com/GAUNTLT/GAUNTLT) 。
    因为这些测试应用程序的非功能方面，它们需要访问浏览器自动化工具不提供的 HTTP 层。所以测试这些需要一种混合的方法:浏览器自动化和代理服务器一起检查和注入请求。我更喜欢 WebDriver 和 OWASP ZAP 的组合。
3.  **应用和基础设施的安全扫描**。
    即使是手动驱动的渗透测试，通常也是从使用 Nessus、Burp 和 OWASP ZAP 等漏洞扫描工具的自动扫描开始的。了解这些工具之间的区别以及如何使用它们是值得的。Nessus 主要是一个基础设施扫描器，它将测试一个 IP 地址和所有暴露的端口的已知弱点。它还包括一个“web”扫描组件，该组件将测试 HTTP 服务是否存在类似的已知弱点，但是 web 层的扫描非常肤浅。例如，Nessus 不能扫描登录表单后面的任何内容或功能，也不能通过 web 向导导航。
    [Burp 入侵者](http://portswigger.net/)(商用)和 [OWASP ZAP](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project) (开源)专注于 web 层，是真正的应用程序扫描器，它们通过将攻击数据注入参数并评估应用程序的响应，在 HTTP 层进行检查和测试。如果使用正确，它们可以提供深度安全扫描。但是，如果它们只是用来抓取应用程序并运行自动化测试，那么它们很可能无法找到或测试所有可用的内容。
    要成功实现应用程序扫描自动化，应确保在开始抓取和扫描应用程序之前，所有要扫描的内容都已在扫描工具中导航和填充。如果您已经有了驱动浏览器的验收测试，那么在开始扫描之前，可以重用这些测试来填充 Burp 或 ZAP 内容。
4.  **Security testing application logic**.
    Automated tools can only go so far in detecting security flaws. Toidentify flaws in the logic of the application requires a human brain (at time of writing). From an automated scanner’s point of view an online auction site and an online bank are the same type of application, i.e. a series of HTTP requests. But from a human attacker’s point of view, they are vastly different beasts offering very different functions. A human security tester might try tests such as:
    *   我可以操纵 HTTP 请求对已经结束的项目进行投标吗？
    *   我可以操纵 HTTP 请求以高金额投标，然后在拍卖结束前将该金额修改为较低的金额吗？
    *   我可以使用负数作为值将资金转移到其他人的帐户吗？

    这些需要独创性和经验来发现，但是一旦攻击被定义，它们也可以被记录为自动化测试，并成为安全回归测试的一部分。

## [![Screen-Shot-2015-03-18-at-21.21.253](img/0294fb70cea76fb61cd7df3a0fcbffe6.png)](https://devops.com/wp-content/uploads/2015/04/Screen-Shot-2015-03-18-at-21.21.253.png)

## 跑步前先走

如果您刚刚开始自动化安全测试的旅程，上述步骤可能会令人望而生畏。但是没有必要实现所有这些来获得自动化安全测试的好处。第 2 点和第 3 点可能代表了投入的时间相对于提取的安全价值的最大价值，因为它们有助于识别许多在正常开发过程中遗漏的常见安全缺陷。

任何测试框架都可以用来编排和运行这些测试，但本着真正的 SecDevOps 精神，最好选择一个开发、操作和安全团队使用起来舒适的框架，并且可以轻松地与您的 CI/CD 服务器集成。我偏爱 BDD 框架，因为它们使用自然语言来定义测试步骤，这意味着它们可以被广大受众立即理解，并使它们非常适合用作*安全测试规范*。但是一些精通编程语言 X 的团队可能会发现这个额外的自然语言层是多余的。

如果我们想要将这些测试集成到 CI/CD 环境中，上面的第 3 点需要一个额外的步骤。其他测试都有明确定义的通过和失败标准，但运行自动扫描工具通常会导致大量误报结果:工具报告的安全问题实际上并不存在风险。使用自动化工具的手动安全测试包括调查和消除这些误报的过程。自动化测试必须做同样的事情，也要指定成功的标准。这可以通过在测试中包装扫描操作并指定给定特定扫描工具和目标的已知误报来完成。

例如， [BDD-Security](http://www.continuumsecurity.net/bdd-intro.html) 框架使用以下测试对 SQL 注入漏洞执行自动扫描:

[![SQL injection scanning example](img/4e713e2ccd12629357b93ac9c24aeda8.png)](https://devops.com/wp-content/uploads/2015/04/Screen-Shot-2015-04-02-at-11.53.46.png)

和附加文本文件:tables/false_positives.table 来定义要忽略的已知误报:

[![false positives example](img/af74c982e3fed6bad4223abb5aeb76a9.png)](https://devops.com/wp-content/uploads/2015/04/Screen-Shot-2015-04-02-at-11.56.12.png)

测试的最后一步定义了成功标准，需要根据应用程序和所用扫描工具的安全要求进行选择。

## 何时运行测试

因为它们是自动化的，运行测试的成本非常低，所以我们自然希望快速失败并尽早运行它们。但是安全问题通常是在组件级别发现的，很难在单元/类级别测试。因此，应用程序层的测试应该在运行的应用程序上进行。换句话说，在自动化验收测试的同时。

应该在尽可能接近真实的环境中测试基础设施的安全性。这通常是生产前环境。当然，由于运行测试不需要花费任何成本，所以在生产环境中连续地执行相同的测试是有道理的。

## 阻塞测试还是并行测试？

作为一名安全从业者，我希望将安全测试作为 CD 过程的一部分，如果测试失败，就阻止交付。但在现实中，这可能并不适用于所有团队；归根结底，这是一个文化问题，即安全性在多大程度上集成到开发和运营团队中。

对于那些没有实现 SecDevOps 涅槃的人来说，测试可以在安全团队的监督下与构建并行运行。如果测试失败表明存在不可接受的风险，那么安全团队就有责任手动阻止交付。

## CI 服务器集成

安全测试与 CI 服务器的集成程度取决于测试框架和 CI 选择。Java、Python 和 Ruby 测试框架可能会得到所有主要 CI 服务器的支持。使用 Jenkins 和 JBehave 生成 JUnit 和 HTML 报告，测试输出将是:
[![xunit-test-results](img/2a51cd76e97457bb2003b34e4272fec8.png)](https://devops.com/wp-content/uploads/2015/04/xunit-test-results.png)

![bdd-report-ssl-snippet](img/c65d15b72c6ffb7dacb031c1ff75b027.png)