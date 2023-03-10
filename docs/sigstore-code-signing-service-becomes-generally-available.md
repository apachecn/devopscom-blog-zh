# Sigstore 代码签名服务变得普遍可用

> 原文：<https://devops.com/sigstore-code-signing-service-becomes-generally-available/>

Sigstore 开源社区为软件创建的免费数字签名服务本周已经可以通过云获得。

在 [KubeCon + CloudNativeCon 北美](https://events.linuxfoundation.org/kubecon-cloudnativecon-north-america/)会议期间举行的 [SigstoreCon](https://events.linuxfoundation.org/sigstorecon-north-america/) 活动上宣布，云服务使开发人员能够加密签署工件并验证用于构建应用程序的组件是安全的。

Sigstore 社区在开源安全基金会(OpenSSF)的支持下运行，OpenSSF 是 Linux 基金会的一个分支。Sigstore 项目的赞助商，包括 Google、Red Hat、GitHub 和 Chainguard，已经承诺运营一项 99.5%正常运行时间和全天候寻呼机支持的服务。包括 Shopify、Autodesk、Trail of Bits 和 Rancher Government Solutions 在内的 70 多家组织积极参与维护和扩展 Sigstore。

使用 Sigstore 已经记录了超过 400 万个 Sigstore 签名，这主要归功于 Sigstore 支持，开源 Kubernetes 和 Python 项目的维护者已经包含了 Sigstore 支持。npm 社区还宣布，它正在努力将 Sigstore 集成到所有用于构建 JavaScript 应用程序的包中。

Sigstore 的联合创始人、谷歌开源安全团队的技术负责人兼经理鲍勃·卡拉威(Bob Callaway)表示，这项服务将使开发人员更容易以一种更容易在软件材料清单(SBOM)中验证的方式向代码添加数字签名。

他补充说，现在的目标是扩大致力于使用 Sigstore 来更好地保护软件供应链的开源项目的数量。

![](img/229daca3c1782bd3320d35964d671c98.png)

在开源 [Log4j 零日漏洞](https://devops.com/?s=Log4j)之后，开源软件的安全性成为一个主要关注点。Sigstore 在披露之前正在开发中，但拜登政府的行政命令要求联邦机构验证开源软件的安全性，这使得该项目可以获得更多资源。

作为对行政命令的回应，OpenSSF 概述了一个 10 点计划来保护开源软件，该计划需要超过 1 . 5 亿美元的资金。其中一个目标是让前 200 个项目中的 50 个和前 10，000 个项目中的 1，000 个采用可互操作的软件签名方法。该项目估计第一年耗资 1 300 万美元，以后每年耗资 400 万美元，第一年后还需要一次性追加 1 000 万美元。

目前还不清楚开发人员将在多大程度上使用数字签名，但是考虑到目前的关注程度，很可能大多数组织将很快要求他们使用的任何代码都要进行数字签名，以便可以验证它是不可变的。当然，下一个巨大的挑战是找到一种方法来操作将包括这些签名的所有[sbom](https://devops.com/?s=SBOMs)的集合。毕竟，SBOMs 只是更大的 DevSecOps 工作流中的第一步，它将使组织能够根据收集的所有数据接受或拒绝软件组件。