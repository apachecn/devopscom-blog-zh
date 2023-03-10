# 将 z/OS 系统引入当今的现代应用程序开发

> 原文：<https://devops.com/bringing-z-os-systems-into-todays-modern-application-development/>

**将 z/OS 系统引入当今的现代应用开发**

现代应用程序开发都与自动化有关，解决了开发人员和公司运营方面的问题，并支持保持应用程序最新所需的通用 CI/CD(持续集成/持续交付)方法。

开发人员通常利用各种开源工具和其他工具来帮助他们的工作。虽然这些工具中的大多数是为传统的服务器或云原生环境创建的。一些最强大的工具可以在 z/OS 环境中本地运行。

Ansible 就是一个例子，它是一个用于应用程序部署、配置管理和编排的开源社区项目。它适用于 z/OS。

IT 自动化引擎的工作原理是连接到您的节点，并将称为“可转换模块”的小程序推送给它们。这些程序被编写成系统期望状态的资源模型。Ansible 然后执行这些模块，并在完成时删除它们。

简单来说，Ansible 允许开发人员自动化 z/OS 应用程序。借助 Ansible，开发人员可以使用现有的 JCL、REXX 和 z/OSMF 来自动化基于 z/OS 的软件。这使得开发人员可以采用通用的方法来开发混合应用程序，并将 z/OS 一致地集成到企业自动化策略中。

一个很大的优势就是开发者可以用 Ansible 和 [Python](https://devops.com/python-remains-popular-in-programming-language-study/) 工作。这些都是市场上现成的技能，可以应用到 z/OS 应用程序中。

另一个常用工具是 Jenkins，它是一个开源的、基于服务器的工具，可以持续构建和测试软件，支持 CI/CD。Jenkins 集成了广泛的源代码管理系统，如 Git 和 Subversion。Jenkins 的能力可以使用插件扩展到不同的平台和系统。一个这样的 z/OS 连接器是 IBM z/OS 连接器 T1，一个用于连接 Jenkins CI 和 IBM z/OS 的插件，包括集成 IBM SCLM 作为 SCM。

使用这样的工具，开发人员可以构建一个 CI/CD 管道，例如，调用您在 z 上运行的开源脚本。它可能会将一些文件从 A 移动到 B，或者调用编译器。它帮助熟悉这些工具的人执行这些任务，并将它们合并到他们的流程中。如果他们运行在 z/OS 平台上，开发者可以直接在这个平台上进行交互和调用。例如，一个应用程序可以利用现有的大型机 Rex 脚本，而不必重写它。

**考虑文化差异**

在当今这个永远在线、即时访问一切的世界中，员工和客户需要对现有的应用程序和服务进行频繁的更新和添加新功能，同时还需要更好的新产品。满足这些需求是一项竞争优势。

将常用的开源开发、工作流自动化和 CI/CD 工具引入 z/OS 环境，有助于企业加快新应用程序的开发，以满足客户不断变化的需求。它允许企业利用其 z/OS 系统上的数据和应用程序，并创建创新的新应用程序。

它还包括为开发人员提供他们熟悉的工具，并提供构建 z/OS 应用程序的工具，就像构建其他应用程序一样。许多人用同样的工具在平台外构建他们的应用程序。拥有在 z/OS 上运行的工具是有帮助的。这样更容易。企业可以减少应用程序变更。所以，风险更小。

如果一个企业在 z/OS 上运行了 20 年、30 年甚至 40 年的遗留应用程序，那么这些应用程序已经被证明是安全、稳定和可靠的。一个用于 z/OS 的开源应用程序开发工具提供了一种方法来保留这些品质并使应用程序开发现代化，以构建管道并制定新一代开发人员熟知的 DevOps 原则和实践。