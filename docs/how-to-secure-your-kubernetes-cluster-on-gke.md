# 如何保护 GKE 上的 Kubernetes 集群

> 原文：<https://devops.com/how-to-secure-your-kubernetes-cluster-on-gke/>

Google Kubernetes 引擎(GKE)很容易上手，但需要额外的安全控制。文档很难掌握，因为有许多特性和变化与特定的 Kubernetes 版本相关，需要使用 beta 特性支持，还有一些过时的文档会让人不知所措。

还有一个我们在 Kubernetes 上养的 [突出 bug](https://github.com/kubernetes/kubernetes/issues/68717#issuecomment-593458451) 被 GKE 打了。如果您最终直接运行 pod 而不是部署，这是一种边缘情况，并且只有在您启用 pod 安全策略(出于安全原因，我们建议这样做)时才会发生。

如果您正在考虑生产，并且有敏感的工作负载，我们建议您实现本文中的所有内容。

## **保护您的 Kubernetes 基础设施**

## ![](img/52687802253cf78246bf1bcf5d78aea7.png)

当您部署默认的 GKE 集群 而没有提供额外的选项时，您将获得一些合理的安全默认值:

1.  基本认证被禁用。
2.  操作系统(OS)映像的静态加密已启用。
3.  客户端证书颁发被禁用。
4.  安全操作系统(使用容器优化的操作系统；COS)。
5.  虚拟机完整性监控，以防范恶意软件/rootkit。
6.  受限服务账户。

那么，谷歌为什么默认启用这些东西呢？本质上它的意思是:

*   您只能通过谷歌云平台(GCP)单点登录(SSO)到 Kubernetes API 进行身份验证。这意味着，不能使用基本身份验证或客户端证书。
*   操作系统被锁定，容器通过有限的只读根文件系统进行优化，并带有完整性检查。启用操作系统的完整性监控，以防范 rootkits 和恶意软件。
*   Kubernetes 节点正在使用的服务帐户受到限制，只有访问它需要的云服务的权限，例如用于日志记录和监控的 Stackdriver。

您需要确保启用的内容:

*   启用安全引导来验证操作系统和内核模块的真实性。(如果您决定不使用默认操作系统，这可能会导致问题)。

![](img/c3f73cba87292ae3627896bea85b56e7.png)

使用[虚拟可信平台模块(VTPM)](https://cloud.google.com/blog/products/gcp/virtual-trusted-platform-module-for-shielded-vms-security-in-plaintext) 对内核映像和操作系统进行签名，意味着可以建立真实性。它还保证没有任何东西被篡改，内核模块没有被包含恶意软件或 rootkits 的模块替换。

*   启用节点内可见性，以便您可以看到单元和节点之间的数据流动。

![](img/171e82ef1c833d1c60b18a39c9f2a28e.png)

确保记录和跟踪单元和节点之间的所有流量将有助于您识别以后可能出现的任何潜在风险。这不一定是开发时需要做的事情，而是生产时应该做的事情。

*   把 Kubernetes API 放到一个私有网络上。

![](img/d81c379638f9b606fe2af71d81c22d1c.png)

*   将节点池放在专用网络上。

![](img/1f187436f699de20d0ab2e4013e1eee1.png)

*   提供应被允许与 API 对话的授权网络列表。![](img/6260d01ce3bf401a91f703a72d5f0c20.png)

将你的节点和 Kubernetes API 设为私有意味着它不会受到机器人、黑客和脚本小子一直在进行的网络扫描。

将它放在只能通过 VPN 访问的内部网络之后也不错，但是，这是 GKE 的一个更复杂的过程，不像其他的功能标志那么简单。你可以 [了解一下这里涉及的内容。](https://cloud.google.com/solutions/creating-kubernetes-engine-private-clusters-with-net-proxies)

## **保护您的应用程序容器**

同样，谷歌启用了一些默认功能来帮助你入门。然而，仍然有一些空白需要你去填补。

你得到了什么？

*   托管证书
*   基于角色的访问控制(RBAC)

您想要启用的内容:

*   Pod 安全策略。这是测试版，需要您通知 Google 您想在测试版模式下运行集群创建:

![](img/5ee0bbf0d3878027ddf439f93bc7d5e7.png)

*   网络政策。

![](img/87760666467a2ce02338804f131ffb9b.png)

这听起来很棒，但它实际上意味着什么呢？基本上，这些角色可以分成两部分，一部分是应用程序开发团队，另一部分是集群管理员。

**应用开发者**

*   在应用程序级别设置网络策略，以便只允许正确的访问级别，即 AppA 可以与 AppB 对话，但 AppC 不能与任何一方对话。
*   对您想要的域的服务端点进行加密，即[【https://www.mydomain.com】](https://www.mydomain.com)。

Kubernetes 可能需要一点时间来学习，有一些技术可以简化依赖关系，例如 helm，它允许您使用预定义的部署来部署应用程序依赖关系。但是从了解 Kubernetes 的主要成分没有真正的替代品； [网络策略](https://cloud.google.com/kubernetes-engine/docs/tutorials/network-policy) ， [入口](https://cloud.google.com/kubernetes-engine/docs/concepts/ingress) ， [证书管理](https://cloud.google.com/kubernetes-engine/docs/how-to/managed-certs) ， [部署](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) ，[config maps](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)， [机密](https://kubernetes.io/docs/concepts/configuration/secret/)

主要的安全组件是网络策略、秘密和证书管理。网络策略将允许您控制进出应用程序的流量。秘密是 base64 编码的，所以在如何存储它们方面没有真正的安全性；因此，确保集群管理员启用了秘密加密(如下所述)，将会添加额外的层。

[证书管理](https://cloud.google.com/kubernetes-engine/docs/how-to/managed-certs) 将确保到您服务的流量被加密，但是如果您在服务之间通信，那么您还应该在您的应用程序之间添加 TLS。让集群管理员安装类似于 [证书管理器](https://github.com/jetstack/cert-manager) 的东西，将允许更容易的方式在服务之间加密。也有像[Istio](https://istio.io/)这样的服务，但由于该产品不仅仅是证书，它会增加不必要的复杂性。

**集群管理员**

*   有能力控制用户可以做什么，在什么命名空间(RBAC)，即，也许开发人员鲍勃可以做部署，(创建，更新，删除)，但不能查看命名空间 our-teams-app1-dev 中的秘密。
*   对出口和入口(出站和入站)实施拒绝所有网络策略。这可能会有争议，因为它可能会让团队陷入困境，所以确保你在沟通这一点是关键。然而，这将迫使团队定义网络策略以使他们的应用程序工作。
*   通过 Pod 安全策略强制实施应用程序部署安全策略。这意味着防止在集群中运行的容器提升特权、在节点上安装设备(包括绑定到主机网络)或运行更多特权内核系统调用。

你要确保开发团队不能部署不安全的应用程序或试图提升他们的权限，安装他们不应该安装的设备或进行不必要的内核系统调用。Pod 安全策略提供了一种方式来限制用户、团队或服务帐户如何将应用程序部署到集群中，从而强制实施良好的安全状态。

RBACs 和 Pod 安全策略密切相关。一旦您定义了一个好的 Pod 安全策略，您就必须创建一个引用它的角色，然后将一个用户、组和/或服务帐户绑定到它，无论是在集群范围还是在名称空间级别。

**注:** GKE 为 RBAC 使用了一个 webhook，它将首先绕过 Kubernetes。这意味着，如果您是 Google Cloud Identity Access Management(IAM)的管理员，它将始终让您成为集群管理员，因此您可以从意外锁定中恢复。这在控制平面内被抽象出来，由 GKE 自己管理。

我们推荐以下是一个好的 PSP。这将确保用户、服务帐户或组只能部署满足以下条件的容器。

![](img/c794fd645712cd6aa01daecce1586dd6.png)

如果您想创建一个角色来使用上面定义的 PSP，那么它看起来会像下面这样，这是一个集群角色，而不是一个标准角色。为了对所有经过身份验证的用户实施这一点，您需要创建一个角色绑定来应用于“system:authenticated”组。

![](img/2d36d3006e5aff074e146b38d694efa0.png)

请记住，由于这是集群范围的，任何需要更多特权权限的应用程序都将停止工作，其中一些将是 Google 添加到 kubernetes 中的内容；比如 kube-proxy，它运行在 kube-system 名称空间中。

你可以在 [kubernetes.io](https://kubernetes.io/) 上阅读更多关于 [RBAC](https://kubernetes.io/docs/reference/access-authn-authz/rbac/) 和 [PSP 的](https://cloud.google.com/kubernetes-engine/docs/how-to/pod-security-policies) 的信息。

## **保护敏感数据和应用云服务**

我们将把它分成两部分。

**1。在 Kubernetes 中加密您的秘密**

对使用谷歌云 KMS 服务加密机密的建议是分离角色和职责，并在将托管 Kubernetes 和应用程序的谷歌项目之外定义一个新的谷歌项目。这是为了确保加密密钥，更重要的是，签署其他密钥的密钥(信封加密)不在同一个项目中，否则可能会受到威胁。

要加密机密，您需要:

*   建立一个新的谷歌项目来实现职责分离(如有必要)。
*   在该项目中创建主密钥环和密钥。
*   仅允许 Kubernetes 托管项目中的 GKE 服务帐户访问专用密钥项目中的密钥。
*   只允许服务帐户的正确权限(加密和解密)。

关于如何做的文档可以在 [这里找到](https://cloud.google.com/kubernetes-engine/docs/how-to/encrypting-secrets) 。但是要记住的主要是:

*   密钥必须位于与集群相同的位置(区域)(这是为了减少延迟或区域丢失)。
*   服务帐户的访问权限必须正确。
*   该绑定是 KMS IAM 策略绑定。

一旦设置完成，您就可以将路径传递给密钥，即“gcloud container clusters create”命令:

![](img/22e1f41da435711e861459f7df5b4d75.png)

**注意:** 如果以上任何一个不正确，当你去创建一个集群的时候，你会得到一个 500 内部服务器错误。这可能是路径不正确、位置错误或权限不正确。

**2。在 Kubernetes 内部消费云服务**

有四种不同的方式允许应用程序容器使用云服务。所有这些都在某种程度上有局限性，即，对开发人员来说不太用户友好和不自动化(使开发人员等待提供相关的访问权限)，或者对 Kubernetes 和云管理员来说在将可审计性结合在一起方面具有较低的可见性和较高的复杂性。

1.  **工作负载身份**(这仍处于测试阶段，是谷歌的长期发展方向):需要一个持续的过程来管理谷歌 IAM 和 Kubernetes 服务账户，以将它们联系在一起。这意味着管理特定应用服务线的 Google IAM 角色、策略和服务帐户以及 Kubernetes 服务帐户。但是，它确实提高了可审核性。
2.  **Google Cloud Service Account keys 存储为 Kubernetes 名称空间内的秘密**(应用程序将驻留的地方):与上面类似，但是没有绑定。这意味着提供一个服务帐户，并将其作为一个秘密放在应用程序名称空间内，供其本机使用。这有一个缺点，就是在 Google 云和 Kubernetes 中没有完全的可审计性。
3.  **使用类似于 [Vault](https://github.com/hashicorp/vault)** **的东西在云和应用程序之间进行代理** : 使用 Vault 提供了对云的抽象，并将生成应用程序的短期访问密钥。但是，仍然需要一个密码才能与 Vault service 通信，因此，权限仍然相同，只是减少了一个。它也使谷歌云和 Kubernetes 之间的可听度脱节。
4.  **使用 GKE** 的默认服务账户节点角色:更简单，对开发者更友好，但风险更大。这将意味着允许应用程序使用默认的节点服务帐户，并修改角色以迎合应用程序需要的所有服务策略，将节点服务帐户的范围和功能扩大到大多数 Google 云服务。

## **能见度好的；当前和历史**

**注意:** 到今天为止，Google 访问您的 Kubernetes 集群时没有访问透明性(Google Access Transparency)。这对于许多希望获得提供商数据访问保证的组织来说可能是个问题。

配置集群时，所有审计日志和监控数据都被推送到 Stackdriver。由于控制平面由 Google 管理，您不能覆盖或修改审计格式、记录或扩展它到您自己的 webhook。

例如，这意味着你可以在你的审计日志中搜索 Kubernetes 内部正在发生的事情；要根据您的用户 ID 查询特定 Google 项目中某个集群的所有事件，您可以执行以下操作:

![](img/653ab7d57bd8c8ae65131e184cbd7ef9.png)

从现在开始，您可以更进一步，添加额外的安全规则，例如设置自定义指标，以便在发生集群管理更改或角色(集群管理角色)发生特定修改时发出警报。

## **总结**

安全是每个人都想要的，但是正如你所看到的，实现它是一个相当复杂的过程。它还需要领域知识，以获得足够的上下文来评估风险及其对您的应用程序和业务的意义。

没有自动化的安全性会降低生产力。安全性不足会使您的企业面临风险。启用需要测试版功能的安全功能也可能不适合业务，只有一般可用性功能是可接受的，这会损害安全性。

一般来说，强化您的集群并加强与 Kubernetes、容器、云服务和您的应用程序的安全合作方式，最终会让您获得最佳结果。可能会有令人沮丧的学习曲线，但随着行业的成熟，这些将慢慢得到补救。

*要了解更多关于集装箱化基础设施和云原生技术的信息，请考虑来阿姆斯特丹的 [KubeCon + CloudNativeCon EU](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/) 。CNCF 已决定推迟该活动(原定于 2020 年 3 月 30 日至 4 月 2 日)，改为在 2020 年 7 月或 8 月举行。*

——[刘易斯·马歇尔](https://devops.com/author/lewis-marshall/)