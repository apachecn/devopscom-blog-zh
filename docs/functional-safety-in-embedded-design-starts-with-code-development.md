# 嵌入式设计中的功能安全始于代码开发

> 原文：<https://devops.com/functional-safety-in-embedded-design-starts-with-code-development/>

***随着嵌入式软件可能变得更加复杂，现在是时候开始考虑功能安全***

随着世界越来越依赖功能安全市场中的嵌入式系统，如铁路、汽车、航空航天和医疗，确保这些系统中软件的安全性变得更加重要。这种保证必须从软件开发开始。

众所周知，软件开发是引入许多漏洞的起点，潜在地导致未来的性能、安全性和安全问题。许多嵌入式软件开发人员面临的挑战是，他们经常要处理高度复杂的环境。一般来说，这些复杂的环境是使用 C 和 C++编程语言构建的。

虽然 C 和 C++为开发人员提供了嵌入式环境所需的灵活性和创新空间，但它们也带来了风险。代码可能具有未定义或未指定的行为，或者在不同的硬件上运行时可能行为不同。即使是最熟练的开发人员也可能做出无意中导致错误的决策。

## 嵌入式系统和功能安全:文化欣赏

降低软件开发风险的方法有很多。从文化的角度来看，安全性需要融入到软件开发过程中，从一开始就如此，并贯穿整个 DevOps 生命周期。当然，这是所有软件市场都应该采取的做法，而不仅仅是在嵌入式设计领域。

与此同时，需要[更加关注强制遵守功能安全标准](https://devops.com/safety-nets-become-optional/)。这种实践需要策略来确保系统的安全性。在某些行业，如铁路和汽车行业，这些标准的使用被强制作为批准和合规流程的一部分。

## 功能安全标准

功能安全标准要求对系统进行危害分析和风险评估。根据结果，实施安全功能，将风险降低到可接受的水平。功能安全标准规定了适当的软件开发和验证措施，以降低已知风险。

目前使用的一些主要功能安全标准包括 IEC 61508，涵盖电气、电子和可编程电子安全系统。20 多年前首次发布，IEC 61508 也是其他几个功能安全标准的基础，包括汽车的 ISO 26262、铁路的 EN 50128、医疗设备的 IEC 62304 和农业机械的 ISO 25119。

与其他标准类似，功能安全标准并不总是受到热烈欢迎，因为人们认为它们需要额外的工作和费用。事实上，通过要求一致的、高质量的编码实践，功能安全标准可以减少上市时间和成本，因为它们将最佳实践效率引入了开发过程。

## 编码标准

大多数功能安全标准要求或建议使用编码指南。例如，在汽车行业，ISO 26262 要求使用编码指南，并强调必须涵盖的特定领域，例如使用安全语言子集和命名约定。

通常，编码标准是由许多人和组织的集体知识组成的，例如制造商、顾问和行业协会。然后，这些集体知识被用来为开发人员提供一组规则，以确保他们正在开发的代码是安全的、可靠的和符合规范的。编码标准还通过使代码在团队中更加一致、可读和可理解来产生更高质量的编码实践。

根据项目的不同，组织通常选择完全或部分地实现外部编码标准。他们也可能决定根据外部标准或自己的经验创建自己的内部编码标准。

虽然 MISRA C 和 MISRA C++最初是为汽车行业创建的，但这些编码标准现在已经广泛应用于多个行业。AUTOSAR C++14 编码指南旨在满足现代 C++开发环境的要求，包括自动驾驶汽车，未来将用作新的 MISRA C++标准的基础。

另一个跨多个市场使用的流行编码标准是 CERT(由卡内基梅隆大学软件研究所的 CERT 部门协调)，它专注于安全性。随着对网络安全风险意识的增强，CERT 在嵌入式软件开发中的使用可能会增加。

## 成功实施

不管采用哪种方法，编码标准的成功实现取决于几个因素。由于实现可能会遇到阻力，团队需要参与编码标准和支持工具的选择过程。通过被包括在决策过程中，它帮助团队理解为什么需求是关键的。

此外，尽管可以根据编码标准执行手工代码审查，但是任何大规模的项目都需要自动化的静态代码分析工具。

静态代码分析工具可以快速准确地检测成千上万的缺陷，这使得开发人员可以考虑设计的实现。这些工具通过在提交之前分析单个开发人员的代码变更，然后作为持续集成(CI)的一部分扫描整个项目来工作。因此，静态代码分析器在 DevOps 主导的开发环境中协调得很好。

随着嵌入式软件可能变得更加复杂——特别是在人工智能、人工智能和物联网的背景下——现在是开始考虑实施有效的功能安全战略的好时机，其中包括静态代码分析器和编码指南等工具。