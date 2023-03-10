# 使 SBOMs 可操作

> 原文：<https://devops.com/making-sboms-actionable/>

一个[软件材料清单(SBOM)](https://devops.com/?s=SBOM) 是在给定代码库中找到的或者在给定软件构建中使用的所有软件组件的列表。太好了。那么，现在怎么办？我们为什么要关心 SBOMs？

这些都是很好的问题——因为就其本身而言，SBOM 并没有真正做什么；这只是达到目的的一种手段。那就是更高的软件安全性和更安全的软件供应链。

让我们退一步来理解为什么对 SBOMs 的需求如此突然和迫切。最近对软件供应链的“大爆炸”攻击是 2021 年 12 月发现的 [Apache Log4j](https://devops.com/?s=Log4j) 漏洞。该漏洞为无数的违规行为打开了大门，并造成了数十亿美元的损失。在此之前，网络安全管理软件产品备受瞩目的黑客攻击也造成了类似的损害。

现在，SBOM 会阻止这种情况(再次)发生吗？不会。然而，SBOM *所能做的是*告诉你确切地这些类型的漏洞存在于软件中的什么地方，并使你能够快速修补你的系统或阻止利用。有了软件材料清单，您可以快速评估代码库中的风险，并根据需要减轻风险。

强烈建议您使用动态 SBOM(相对于静态 SBOM ),它会自动更新到最新的 SBOM 信息，并作为 SBOM 数据库的一部分提供广泛的搜索功能。这允许立即识别特定的依赖版本，如 Log4j 的情况。[一些解决方案还基于运行时更新 SBOM 信息](https://codenotary.com/products/ci-cd/)(如 Docker 或 Kubernetes)。这样，你不仅知道*是否使用了*某个组件，还知道*在哪里*。

SBOMs 是一个非常有价值的工具，因为它们允许对许可证、库、模块、应用的补丁和其他组件进行审计，以寻找弱点。然而，为了使这种审计能够可靠地跟踪用于构建软件的组件，SBOM 必须具有某些属性。

*   每个软件组件的唯一标识
*   独立的身份(独立于组织内部使用的身份)来标识开发过程中涉及的每台机器和用户
*   时间戳有助于每次变更或组件合并的可追溯性

此外，从安全角度来看，SBOM 可靠性的一个关键要素是防止对其进行未经授权的更改。最有效的方法是使用不可变的分类帐，记录每次变更的历史。

一旦 SBOM 的可靠性得到保证，DevSecOps 团队就可以将其作为威胁扫描工具箱的一部分，从而提高软件的安全性。

毫无疑问，您应该向您的软件供应商请求 sbom，并且您应该考虑创建 sbom 以及您自己开发的软件。这一切都是为了正确存储 SBOMs，以便您可以确保它们是最新的、可搜索的、值得信赖的和防篡改的。

SBOMs 的优势和使用案例数不胜数；它们因生产、选择和操作软件的利益相关者而异，并在组合时被放大。SBOMs 的用例包括更好的软件开发、供应链管理、漏洞管理、资产管理和高保证流程。好处包括降低成本、减轻安全风险、许可证风险和合规性风险。

但关键是让 SBOM 变得可行。

没有一个开发人员、软件维护人员或 DevOps 工程师想要手动收集依赖项并生成 SBOM 文档。它需要在软件构建和部署管道中完全自动化，并且需要主动检查它当前运行的位置。

处理普遍的 SBOM 策略的最有效的方法是让它们作为现代开发 CI/CD 过程的副产品生成。

在当今复杂的开发环境中，作为软件管理透明性的一个基本部分，SBOMs 必须能够在团队和组织之间无摩擦地共享。这个透明模型由 ISO 协会通过其 [开放链规范](https://www.openchainproject.org/) 提供支持，并且它是在数字产业中提高安全性 的 [努力的一部分。](https://www.whitehouse.gov/briefing-room/presidential-actions/2021/05/12/executive-order-on-improving-the-nations-cybersecurity/)

有两个 SBOM 规范:由 Linux 基金会支持的软件包数据交换(SPDX)和由 CycloneDX 核心工作组管理的 CycloneDX 规范。更多详情，请看这里的[](https://codenotary.com/blog/what-is-an-sbom-bill-of-materials-and-what-does-it-do/)。

请确保选择对您最有意义的 SBOM 标准，并在您的基础设施中开发或使用的所有软件都遵循该标准。当下一个 Log4j 时刻到来时，你的 SBOM 是否可行的考验就会到来。您应该能够查明有问题的组件的存在和位置，以便有效地降低风险。

* * *

*要了解更多关于云原生的话题，请加入 [云原生计算基金会](https://cncf.io/?utm_content=sponsor-disclosure) 和云原生社区，地址: [KubeCon+CloudNativeCon 北美 2022–2022 年 10 月 24-28 日](https://events.linuxfoundation.org/kubecon-cloudnativecon-north-america/)*