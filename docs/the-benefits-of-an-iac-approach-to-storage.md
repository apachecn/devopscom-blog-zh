# IaC 存储方法的优势

> 原文：<https://devops.com/the-benefits-of-an-iac-approach-to-storage/>

***采用 IaC 存储方法可以免除存储基础架构方面的考虑***

如今的多云世界允许您根据自己的需求在云之间移动应用和/或功能，但这也让您不得不了解每个云提供商的不同存储要求。这些提供商有自己独特的存储产品和参数，不仅彼此不同，而且与私有云部署中使用的存储也不同。

基础设施即代码(IaC)对于驾驭这种多云环境非常有价值。在过去的几年里，IaC 已经成为应用程序开发中众所周知的一种 IT 基础设施，它可以使用一个通用的模板自动进行[管理和供应](https://devops.com/infrastructure-as-code-and-six-key-automation-concepts/)。

同样的基本原则也适用于跨云存储。借助 IaC，您的应用可以跨所有环境和提供商以一致的方式使用存储，因此您不必担心每个云平台的特定基础架构方面。它提供了一个抽象层，从根本上消除了不同提供商处理存储方式的不一致，同时获得了一组一致的接口，帮助您跨云管理应用程序。

## IaC 和存储

以下是 IaC 帮助您充分利用不同云的三种方式，无论它们的存储需求如何。

### 行动自由

让多云环境如此强大的原因之一是能够利用不同云的独特优势，尤其是当您的需求和业务需求发生变化时。例如，在高峰时段将某些功能托管在一个云中，然后在非高峰时段将该功能移回另一个云中，这可能更具成本效益。

使用 IaC 方法，您可以获得更好的应用程序可移植性，因此您可以跨云或跨区域移动应用程序。您不会受到特定基础架构组件或物理位置的限制。您可以根据需要转移工作负载。抽象层使您能够在所有云中以相同的方式管理这些工作负载。

您还可以通过跨多个云自动复制对象数据的副本来保护您的数据。如果一个拷贝被破坏，数据将继续在其他位置可用。您将拥有保持应用无中断运行的弹性。

### 保持数据安全的自由

数据重力可以通过减少延迟来提高性能。这对于需要快速访问数据或依赖大型数据集的应用程序尤其重要。数据离应用程序越近，应用程序的性能就越好。

为了保持性能，您必须能够随着应用程序移动数据。抽象层使您能够做到这一点，因为它消除了不同云提供商之间存在的障碍和各种数据参数。您可以将应用程序的数据与应用程序本身一起迁移。

### 自由扩展

您可能会为各种应用程序采用许多不同大小的工作负载和存储类型，例如，针对较小工作负载的传统文件存储，或针对较大且不断增长的数据集的对象或数据块存储。无论您目前拥有什么，您都希望能够随着业务需求的变化自由地横向扩展您的存储。抽象层使您能够接受多种多样的工作负载，而不用担心它们是否会在特定的云环境中得到支持。如果使用公共云的成本变得过高，或者如果您的安全性或性能需求发生变化，您也可以将应用程序迁移回内部。

然而，你不能给灵活性定价，这对现代敏捷软件开发很有帮助。您需要在云之间轻松移动的灵活性。采用 IaC 方法将使您能够放开对存储基础架构的考虑，将精力集中在开发最佳应用程序上。