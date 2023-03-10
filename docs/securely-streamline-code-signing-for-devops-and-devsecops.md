# 安全简化 DevOps 和 DevSecOps 的代码签名

> 原文：<https://devops.com/securely-streamline-code-signing-for-devops-and-devsecops/>

***引入代码签名在应用程序中提供了安全性，但是团队应该注意有效地理解和实现这个过程***

[数字证书管理](https://devops.com/?s=Digital%20certificate%20management)，需要成百上千的证书来支持 IT 基础设施，这很容易导致应用程序完整性下降，并给业务带来不必要的风险。手动管理数字证书的孤岛式团队的繁琐本质经常导致绕过其组织强制的 PKI 标准。

基于其管道的复杂性，DevOps 和 DevSecOps 团队可能会颁发由不可信来源签名并不安全存储的证书，以加快 CI/CD 工作流的构建和部署阶段，从而避免耗时数周甚至数月的漫长证书申请流程。使用这种手动的、不安全的加密实践来签署和部署代码，会使组织暴露于高度可避免的风险中。

代码签名以及该过程中使用的证书应该使用加密硬件进行集中和自动化。在这里，我们将介绍强化代码签名的过程，以及如何在 DevOps 和 DevSecOps 管道中简化其管理。

## 4 步强化代码签名

1.  **准备分发的未签名代码。生成公钥-私钥对的时间**

我们从一个准备发布的未签名的可执行文件开始。为了安全地对代码进行签名，代码发布者需要生成一个公钥-私钥对。这是大多数运行时架构所需要的，包括 Windows、Java 等。生成代码签名密钥最安全的方法是使用 FIPS 140-2 三级验证的硬件安全模块(HSM)。

2.  **向证书颁发机构(CA)提交公钥和证书签名请求(CSR)**

使用步骤 1 中生成的密钥对，CSR 被生成并提交给发布 CA。CSR 包含标识发行者和签名算法以及数字签名的信息。颁发证书的 CA 使用此信息来颁发代码签名证书。

在某些情况下，例如物联网(IoT)设备制造，组织可能会决定充当自己的颁发 CA。

3.  **发布者的识别和 CSR 的认证**

发行 CA 验证代码发行者的身份，然后验证 CSR，确保发行者已对其进行了数字签名。如果标识和身份验证都成功，则发行 CA 将发行者的身份与公钥打包，然后对该包进行签名，创建代码签名证书。

4.  **准备签字。确定安全级别**

既然代码签名证书已经可以使用了，那么就可以对任何可执行文件进行签名和部署了，除非需要进行进一步的代码测试或 QA。企业，尤其是快速发展的企业，经常发现自己将代码签名密钥存储在代码发布者的本地机器或服务器上，这是一种不安全的方法，可能会导致严重的问题。将密钥存储在本地机器或服务器上会带来很大的安全风险。本地机器可能会连同代码签名密钥一起被破坏/窃取，或者心怀不满的员工可能会恶意签名并部署未经授权的代码，这在一段时间内可能不会被注意到。

最好将代码签名证书导入并存储在密钥管理服务器(KMS)中，该服务器将证书存储在 FIPS 140-2 级防篡改物理边界之后。除了加固存储之外，还可以利用具有适当加密特性和功能的 KMS 来帮助自动化整个代码签名和证书管理生命周期。KMS 允许 DevOps 和 DevSecOps 团队无缝地满足最佳实践，同时消除手动工作流瓶颈并与 CI/CD 系统进行本机集成。减少生成和管理数字证书的时间会导致更快的代码部署和团队产出的增加。

## 简化持续集成

使用 HSM 进行安全的密钥生成和证书存储具有巨大的价值。此外，DevOps 和 DevSecOps 团队可以大大减少持续集成代码构建所需的人工劳动。对于需要定义和可跟踪的签名工作流的构建，集成 CI/CD 的代码签名可以提供显著的好处。

此工作流通常由管理构建和签名请求过程的 CI/CD 系统、管理所有代码签名密钥并执行签名过程的集中式安全密钥管理服务器以及管理以授权方式对代码进行签名的过程的批准实体组成。

当部署像这样的系统时，由 FIPS 140-2 3 级验证的 HSM 支持，组织还可以将自动化引入该过程。这意味着代码签名不再是一个引入人为错误空间的手动驱动步骤，而是被原生地合并到代码开发和发布工作流中。

## 与代码签名技术的集成

提供强化密钥存储的 KMS 和 HSM 加密设备通常与流行的代码签名技术相集成，这些技术执行各种任务，如验证发布者身份和确保代码完整性。例如，使用带有 Microsoft Authenticode 的 SignTool.exe 的组织可以直接与具有完整证书管理功能的 KMS 集成。其他集成和用例包括 Java Jar Signer、RPM(红帽)、Docker 和各种物联网实现。除此之外，创新型组织正在寻找能够在标准操作系统和运行时 SDK 之外部署更高级代码签名工作流的系统，以便与 CI/CD 系统更紧密地集成。

将 HSM 集成到 DevOps 和 DevSecOps 管道中可同时提高工作流效率，并支持整个组织的其他加密操作。