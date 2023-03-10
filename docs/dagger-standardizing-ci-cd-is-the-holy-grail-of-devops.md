# Dagger:标准化 CI/CD 是 DevOps 的圣杯

> 原文：<https://devops.com/dagger-standardizing-ci-cd-is-the-holy-grail-of-devops/>

持续集成和持续交付(CI/CD)已经成为快速软件发布生命周期的标志。如今，许多团队支持他们软件的 CI/CD 管道，提供了一个可重复的途径来构建、测试和部署代码。CI/CD 管道对于支持迭代的、快速的部署方法是必要的——然而，维护一个管道并不是一件容易的事情。

输入[匕首](https://siliconangle.com/2022/03/30/docker-founders-launch-devops-software-deployment-startup-dagger-20m-funding/)。Dagger 是一个实用程序，旨在简化开发人员创建和管理 CI/CD 管道的方式。Dagger 由 Docker 的创始人领导，最近推出了他们的公开测试版，同时由 Redpoint Ventures 领导的[A 轮 2000 万美元融资](https://dagger.io/blog/series-a)。虽然市场上已经存在许多开源 [CI/CD 项目](https://containerjournal.com/features/6-cncf-projects-for-ci-cd/)，Dagger 在提供更简单的配置、预构建的组件和更多可重用的动作方面是独一无二的。

类似于传统的供应链管理，[软件供应链管理](https://devops.com/?s=software+supply+chain)是一项日益复杂的工作，涉及许多第三方依赖。开发团队确实需要一套标准的构建模块来将它们组合在一起。出于这个原因，Dagger 的联合创始人兼首席执行官 Solomon Hykes 告诉 [SiliconANGLE](https://siliconangle.com/2022/03/30/docker-founders-launch-devops-software-deployment-startup-dagger-20m-funding/) “解决这个问题是 DevOps 的圣杯。”

下面，我们将看看在创建和管理现代软件交付链中固有的常见压力。我们还将看一眼 Dagger beta，看看它试图完成什么。

## CI/CD 面临的问题

软件开发供应链正变得越来越大，以支持软件架构的复杂网络。但是必须自动化这个链的 DevOps 工程师正淹没在[工具蔓延](https://devops.com/api-sprawl-a-looming-threat-to-digital-economy)中——将这些组件缝合在一起以制作定制管道可能会成为一个大瓶颈。

特别是当一个组织将其[分布式微服务架构](https://devops.com/how-to-use-microservices-to-evolve-devops-pipelines/)扩展到云中时，跨不同部门和不同技术堆栈扩展[可重复 CI/CD 管道](https://devops.com/how-to-scale-microservices-ci-cd-pipelines/)可能会很棘手。这通常会导致许多定制的 CI/CD 管道。即使在同一个团队中，代码库之间的细微差别也会使每个 CI/CD 流程变得复杂，并需要工程师重写脚本。

与此同时，组织也面临着巨大的压力，要满足新的[数字创新需求](https://devops.com/the-state-of-digital-innovation-one-year-into-the-pandemic/)。但是，直到 DevOps 可以使发布过程更有效率，[软件开发自动化](https://accelerationeconomy.com/automation/the-benefits-and-pitfalls-of-software-development-automation/)冒着引入比它带走的更多辛劳的风险。

## 潜入匕首

那么，Dagger 是如何缓解这些担忧的？Dagger 的创造者将其描述为“CI/CD 管道的可移植开发包”使用 Dagger，DevOps 工程师可以使用一组标准的构建块来组装他们的 CI/CD 管道，然后在他们选择的云上运行它们。这就像是 CI/CD 管道创建的更好的开发人员体验。

那么，匕首是如何在引擎盖下工作的呢？Dagger 由 [Buildkit](https://github.com/moby/buildkit) 提供支持，它是 Dockerfile 不可知的构建工具包。开发人员然后使用[提示](https://cuelang.org/)来指定他们的代码如何在容器中运行，并链接动作。Cue 是 Google 开发的一种开源配置语言。

根据[文档](https://docs.dagger.io/1200/local-dev)显示，安装 Dagger 和必要的依赖项大约需要五分钟。Dagger 还提供了样板代码来集成预先存在的 [CI 环境](https://docs.dagger.io/1201/ci-environment)。本质上，Dagger 不需要取代您的 CI 工具——它添加了“一个可移植的开发层”

然后，还有行动本身。Dagger 支持一个不断增长的动作库，它称之为 Universe。在撰写本文时，行动的宇宙是有限的，并且正在主[匕首库](https://github.com/dagger/dagger/tree/main/pkg)中上演。这些动作是可重用的提示包。例如，[这个包](https://github.com/dagger/dagger/blob/main/pkg/universe.dagger.io/nginx/nginx.cue)详细描述了如何在 Cue 中运行和部署 Nginx web 服务器:

```
package nginx

import (
    "universe.dagger.io/docker"
) 
```

然后，

```
#Build: {
 output: docker.#Image & _pull.image
 _pull: docker.#Pull
    *{
 flavor: "alpine"
 _pull: source: "index.docker.io/nginx:stable-alpine"
    } | {
 flavor: "debian"
 _pull: source: "index.docker.io/nginx:stable"
    }
} 
```

## 利益

CI/CD 当然可以从标准构件和工具间更流畅的连接中受益。Dagger 的提议有几个潜在的好处:

*   统一:统一开发人员和 CI 环境可以避免令人头疼的问题。
*   **本地化** : Dagger 支持本地测试闭环管道。这有助于调试。
*   可重用性:构建块有助于避免重复重写自动化脚本。
*   **多云**:更容易将管道从一个云迁移到另一个云，从而避免供应商锁定。
*   兼容性:Dagger 可以在任何与 Docker 兼容的环境中运行，这意味着它可能与您当前的工具集兼容。

## 最后的想法:CI/CD 的乐高积木

Docker 简化了管理容器化应用程序的过程，彻底改变了软件行业。现在，Docker 创始人 Solomon Hykes、Sam Alba、Andrea Luzzardi 和 Dagger 的其他人正在解决当今复杂软件生态系统中的另一个有意义的问题。鉴于他们之前努力的成功，不难想象一个可重用 CI 配置的网络会像 Docker Hub 一样令人兴奋地出现。

当然，Dagger 仍处于早期阶段，未来还有很多发展。毫无疑问，这将是一个有趣的项目。Dagger 正在作为一个开源项目被构建在 GitHub 上。该公司还开设了一个[不和谐](https://discord.com/invite/dagger-io)频道，与社区接触。