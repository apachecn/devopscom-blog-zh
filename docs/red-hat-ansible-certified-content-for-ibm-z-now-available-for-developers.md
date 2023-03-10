# 面向 IBM Z 的 Red Hat Ansible 认证内容现在可供开发人员使用

> 原文：<https://devops.com/red-hat-ansible-certified-content-for-ibm-z-now-available-for-developers/>

这些新的 Ansible 模块加入了 IBM Z 上 z/OS 的 DevOps 工具的其他新成员。

整个 IBM Z 平台正在快速发展，主要的进步来自于 Z、LinuxONE 和 z/OS 上的 Linux。混合多云需要所有这些平台的一致性和敏捷性。在 Z 和 LinuxONE 上验证几十个针对 Linux 的[开源项目](https://www.ibm.com/community/z/open-source-software/)对开发者和 DevOps 实践者来说都是一个福音。

这就是为什么我很高兴地宣布面向 IBM Z 的[Red Hat ansi ble Certified Content 的可用性，它包括 z/OS 核心集合，现在可以在](https://github.com/ansible-collections/ibm_zos_core#ibm-z-core-collection) [Ansible Galaxy](https://galaxy.ansible.com/ibm/ibm_zos_core) 和 [Ansible Automation Hub](https://www.ansible.com/products/automation-hub) 上获得，作为 Red Hat 支持的认证集合。

这是向前迈出的重要一步，使 z/OS 能够以与您的环境中的其他部分完全相同的方式参与基于 Ansible 的企业自动化策略。利用 Ansible 自动化 z/OS 带来了混合多云环境的一致性，并使 z/OS 透明地参与到您的基础架构中。

这些新的 Ansible 模块加入了对 IBM Z 系统上 z/OS 的 DevOps 工具支持的其他重要开发。你现在可以使用现代的 ide，如 [Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=IBM.zopeneditor) 和 [Eclipse Che platform](https://developer.ibm.com/mainframe/2019/12/11/ibm-z-open-editor-in-the-cloud-with-eclipse-che/) ，使用熟悉的工具为 IBM z/OS 编写 COBOL 和 PL1 代码。IBM Dependency Based Build (DBB)支持使用 Jenkins 和 Git 构建 z/OS 源代码文件，并且可以存放在 Artifactory 或 Nexus 等通用工件存储库上，作为标准 CI/CD 管道的一部分进行部署。为了快速集成基于 Linux 的软件和工作负载以支持 z/OS 应用程序，请查看 [z/OS 容器扩展(zCX)](https://www.ibm.com/support/z-content-solutions/container-extensions/) ，它直接在 z/OS 上支持 Docker 容器化的工作负载。

所有这些现在在 IBM Z 上可用的 DevOps 工具更紧密地将开发管道与在整个组织中使用的那些相结合。IBM 杰出的工程师 Rosalind Radcliffe 描述了 IBM Z 上的应用程序现代化工作，他说“从管道的角度来看，CI/CD 协调器，SCM 部署工具，无论我是否使用 Java、COBOL、Node、C#都是一样的。没关系。”

当您还添加了 Red Hat OpenShift(最近在 IBM Z 上为 [Linux 提供)时，在 z/OS 上拥有基于 Ansible 的供应为您的组织提供了巨大的价值。它使 IBM Z 用户能够在一个易于使用的平台上无缝地将工作流编排与配置管理、供应和应用程序部署结合起来，而不受操作系统的影响。](https://developer.ibm.com/blogs/willie-tejada-redhat-openshift-ibmz/)

放眼 IBM Z 环境之外，您可能已经在使用由 Ansible 管理的基于云的部署。在包含 IBM Z 的混合基础设施中，Ansible 可以管理您传统的基于云的工作负载，以及您在 IBM Z 上的工作负载，进一步实现构建智能、构建安全。

准备好开始了吗？试用[这个 IMS 供应示例](https://github.com/imsdev/ims-ansible-tmdb)开始。

### 后续步骤

*   要了解关于 IBM Z 上的 DevOps 的更多信息，请访问[大型机开发博客](https://developer.ibm.com/mainframe/category/devops/)的 DevOps 部分，查看最新进展。
*   查看新的 [Z DevOps 讲座播客](https://developer.ibm.com/mainframe/category/podcasts/)，与 IBM Z 领域 DevOps 的主要参与者进行轻松但深入的技术讨论。
    *   他们的第一个播客是 Rosalind Radcliffe，他是 IBM 杰出的工程师，也是 IBM z Systems devo PS 的首席架构师。
    *   2 月 11 日的第[集](https://developer.ibm.com/mainframe/2020/02/11/z-devops-talks-season-1-episode-6-kyle-charlet/)讲述了 Ansible for z/OS 与 Kyle Charlet(IBM 杰出的工程师)合作开发 Ansible 模块等内容。