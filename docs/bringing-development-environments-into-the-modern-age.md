# 将开发环境带入现代

> 原文：<https://devops.com/bringing-development-environments-into-the-modern-age/>

现在是 时间 到 重新思考 如何 我们 交付 分发 访问 到

我们知道如何给 [写代码](https://devops.com/devops-golden-rule-writing-more-code-for-test-than-for-production/)。而且有大量的 工具、技术和 流程 对于 做 如此。

我们 知道 什么 种类代号 到 写法: F 代码 那是安全那是 需要 对 修改 就可以了。

我们 知道 为什么 我们 写出 代码。 我们 写 它 对 增强值 我们 削减最大限度地降低 风险 和

我们知道 谁 写代码——或者，更准确地说，是写代码的各种“谁”。我们需要 开发人员 具备 一 多样 多样的技能。作为我们的需要保持变化， 我们的 保持

我们 也 知道 当 到 写出 的代号——其中 就是 现在 和

我们仍然纠结的一件事是哪里写代码。不是物理意义上的“哪里”；w 木牌 方式 过去 那个。 我们 知道为 开发 团队 为为 最优地新冠肺炎有着引人注目的 钢筋 这一 原则。T88

‘凡’我们 奋斗 同 是虚‘凡’ 是的， 我们已经为开发者提供远程访问开发资源。算是吧。但是有一个lot—*lot*—的问题与我们这样做的方式有关。这些问题不利于发展 凡 天 经、 中间 其他 事、

*   踌躇 开发者 失望恼人的 技术 问题 那些妨碍他们能力的 t设定
*   强行 开发者 到 角力 与令人抓狂 复杂度配置
*   套住 开发商无穷无尽 循环往复心狠手辣 和

可惜， 我们已经 变成了习惯了 到 这些 问题 那个 我们 但是 我们 不能 承受 去 接受 他们 下面是 为什么。

### 开发环境:不安全，LostP生产力 和 T 技术 D ebt

一大 问题为 无论是开发者 还是 企业 是开发者工作区都不能 完全移植。我们用来让开发人员远程访问他们的环境的方法总是伴随着不可接受的不安全性。还有入职的问题。当一个 开发人员加入一个团队时——不管是作为新员工， 临时承包商或当前员工 切换到另一个 项目—it 可以 带 天 速度 用 访问 到所有他们需要的特定项目资源。 加速时间总是让 开发者感到沮丧。

上其他下架 开发者 能 成为安全 零敲碎打 开发者需要的多个资源的供应固有地导致那些相同资源的零敲碎打 停用。因此，当一个开发人员退出或被解雇时，或者当一个 承包商的合同到期时，我们不能 100%确定他们的所有权限都被 撤销了。

而且，当一个开发人员需要追溯到一个没有人在 月 或 甚至 年 碰过的项目时会发生什么？ 那他们在做那 对吗？

答案是我们不能。相反，一些不幸的开发者不可避免地不得不旋转他们的 车轮，试图拼凑 一个长期休眠的项目。这样一来，您所有老化的代码就保证了 成为“遗留代码”(这只是“没有人能十分确定如何工作的代码”的另一个名称)， 从而保证了您的组织将永远背负着不断增长的 山资源枯竭[](https://devops.com/?s=technical+debt)

### 年代 制鞋业 C 子辈

那么，我们如何重新设计远程工作区的交付，以便让 开发人员的生活更轻松，同时满足安全性 和 合规性

这里的 都是 一个 几个 点子 到 考虑:

*   在云中托管[开发人员工作区](https://en.wikipedia.org/wiki/Online_integrated_development_environment)。 开发者为其他人提供了 丰富的云资源，然而他们自己却很少充分利用云。有些 资源 他们 需要 可能 驻留 中云 但是完成 工作区 他们 要求 到 成为
*   但是 为什么 没有呢？ 一切 一个 开发者需求每一个 项目 应该 存在 他们可以在任何地方使用特定于项目的工作空间，就像所有的 其他SaaS解决方案 开发人员 构建 用于
*   鉴于世故当今的 浏览器， 基于云的 工作区 云也 启用 工作区到 成为 托管 任何地方 到
*   没事 应该 离开 你的 安全 工作区 储存库。 有史以来。确保安全所有 开发人员 工作产品，
*   只有 屏幕 像素按键 要 移动 跨越网络。 这款 远程访问 型号 让开发者的工作空间完全安全，完全便携。它还提供了最好的 保护 抵御 数据 渗透。
*   简化特定项目工作区的定义和管理。 你不要 希望开发人员四处寻找正在进行的任务、相关数据集或流程 工作流。相反，管理员应该能够配置工作区，给予 开发者 访问所有资源 他们 需要
*   利用[集装箱化](https://containerjournal.com/?s=containerization)来托管您的工作空间。 更好、更安全的企业 开发不仅仅是重新设计远程工作区访问。这也是关于 让这些工作区在后端更容易管理。最好的办法就是 容器化，其中 允许 你 到混搭 工作空间 元素。 即你 不要 有 要 造

而那些工作空间并不是作为铁板一块而存在的， 你 祈祷 你已经 搞定了 没错。 取而代之， 用你 可以 构建 项目专用 工作空间

有效 托管完全 便携 开发者 工作区 要求 其他 重要然而，在解决这些细节之前，开发领导者必须首先接受这样一个事实，即开发人员需要一份比更好的 方式 到 工作