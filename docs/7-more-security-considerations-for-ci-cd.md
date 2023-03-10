# 7(更多)CI/CD 的安全注意事项

> 原文：<https://devops.com/7-more-security-considerations-for-ci-cd/>

CI/CD 编排在 DevOps 实践中变得越来越流行。它促进了软件和产品交付的快速部署。通过在构建、测试和部署应用程序时使用自动化，CI/CD 在开发、运营活动和团队之间架起了一座桥梁。

然而，在频繁部署时，有许多安全注意事项需要牢记。从质量自动化到代码历史分析，安全性必须融入到您的 CI/CD 管道中，以确保您的产品和流程免受黑客攻击。

为了深入了解 CI/CD 的顶级安全考虑，我询问了即将到来的[](https://devopsinstitute.com/cicd-2021/?utm_campaign=SKILup%2520Day-CI-CD-July%25202021&utm_source=DevOps-8-Security-Considerations-for-CI-CD)滑雪日的演讲者和赞助商以及几位 [DevOps Institute 大使](https://www.devopsinstitute.com/about-us/ambassadors/?utm_campaign=Brand%2520Awareness%25202021&utm_source=DevOps-8-Security-Considerations-for-CI/CD) 的想法。在这个由两部分组成的系列中，我将分享他们的见解。你错过了第一部分吗？你可以[看这里](https://devops.com/8-security-considerations-for-ci-cd/)。以下是他们在本系列的第二部分中不得不说的话:

**议长、** [**【拉维拉赫曼】**](https://www.linkedin.com/in/ravilachhman/) **、传道者、马具**

“CI/CD 平台是组织工程效率的核心，通常对敏感环境(如生产环境)具有更高的权限。因为通常会部署 CI/CD 平台，所以这是有意义的。使用二进制工件签名等深入研究网络安全管理软件产品黑客技术。，可以将安全问题分成两部分。一个关注点是实际 CI/CD 平台的安全性，另一个关注点是 CI/CD 管道中的 DevSecOps 目标。随着如此多的项目左移，拥有适当的基于角色的访问控制(RBAC)是至关重要的。随着监管环境的职责分离和工程师高效工作的需要，确保只有特定实体可以部署和特定实体可以查看管道的控制变得非常重要。围绕 DevSecOps 运动，容器/OSS 扫描仍然是许多公司的首选。”

**赞助商，基础科技，****[**Eran Kriegshauser**](https://www.linkedin.com/in/erankriegshauser/)**，基础科技‘SAP devo PS’架构师****

**“您应该问的问题是‘我如何在当今业务要求的频繁部署节奏下保持质量？’我们需要质量自动化和有保证的严格性。例如，以促进系统、应用程序和产品(SAP)中的安全配置变更为例。如今，这是由 SAP transports 完成的，在 SAP 开发系统中创建变更，然后导入 QA，最终导入生产。您如何确保开发人员不能通过角色修改给自己额外的安全访问权限？自动化分析和批准工作流必须支持职责分离要求。用户不能批准他们创建的变更，相应的 CI/CD 流程不允许这样做。**

**另一个领域是对敏感的企业资源规划(ERP)对象的变化的自动同行审查通知。一旦确定，这些对象变更的升级将停止，直到得到团队领导或变更和发布经理的批准。"**

**[**萨文德普里**](https://www.linkedin.com/in/savinderpuri/) **、DevOps 福音传道者、Zensar 科技****

**“将尽可能多的安全方面融入您的 CI 渠道。CD 对于安全性来说已经太晚了—您已经将应用程序部署到环境中了。**

**从基本的静态代码分析、安全扫描器等开始。，然后不断成熟。无论您将什么工具集成到 CI 服务器中，都要确保开发人员可以使用相应的集成开发环境(IDE)插件。这样，开发人员可以在他们的 IDE 内部进行第一级验证，甚至在编译之前就可以在编码时进行。这是经常被过度使用的术语“左移”的实际应用。"**

**[**Vishnu Vasudevan**](https://www.linkedin.com/in/vishnuvasudevan811/)**产品工程与开发负责人 Opsera****

**“现在，随着云迁移、新兴技术和开源技术的出现，公司必须确保拥有合适的工具来衡量不同开发活动带来的安全挑战并采取相应措施。**

**重点需要放在管理与业务关键程度相关的风险上。每个行业、领域、技术等。，都有自己独立的安全目标，对于不同的技术和不同的领域，您不能在整个企业中有一个安全目标。评估所使用的技术并相应地权衡安全需求非常重要。"**

**[**斯蒂芬·沃尔特斯**](https://www.linkedin.com/in/1stephenwalters/) **，销售工程师，光大桥****

**“包容！这就是 DevSecOps 这个术语的由来——因为安全性错误地没有作为 DevOps 转换的一部分，SDLC 转换以纳入安全性也是如此。**

**安全性仍然被视为非功能性需求；事后的想法。如果说有什么是我们应该学习的，那就是没有所谓的非功能性需求。安全需求必须与所有其他需求同等对待，并融入任何功能的设计、测试、部署和交付中。"**

**[**马克·彼得斯**](https://www.linkedin.com/in/tinycyber/) **，技术负责人，诺维塔****

**“CI/CD 管道应该在每一步都实现安全性。测试可以在工具中自动进行，以在多个级别上进行各种功能的代码准确性测试、通过模糊化和集成的单元测试或漏洞测试。管道中的大多数漏洞测试实际上是补丁管理，确保发布软件的所有商业和专有漏洞都被填补。第一步应该是使用编码检查来确保代码没有任何常见的问题。虽然这看起来很容易，但如果你不能完成这一基本步骤，你就无法进入更复杂的领域。”**

**[**Pawel Piwosz**](https://www.linkedin.com/in/pawelpiwosz/)**，EPAM 系统首席系统工程师****

**“从高层次来说，我认为安全性仍然不在 CI/CD 的主要范围之内。在这里，我们应该考虑几个方面和不同的角度。安全不仅要通过 CI/CD 来实现；CI/CD 应以安全的方式实施。一切即代码是一种解决方案:策略即代码、安全即代码、漂移即代码，如果我们谈论基础设施，补救即代码。”**

**如果您想了解 CI/CD 和类似主题的更多最新信息，请查看即将推出的[SKILup Day schedule](https://www.devopsinstitute.com/all-events/?utm_campaign=SKILup%2520Days%25202021%2520%255BGeneral%255D&utm_source=DevOps-8-Security-Considerations-for-CI-CD)。或者，了解更多成为 [DevOps 学会会员](https://devopsinstitute.com/membership?utm_campaign=Paid%2520Membership%2520Launch%2520Campaign&utm_source=DevOps-7-More-Security-Considerations-CI-CD) 的好处。**