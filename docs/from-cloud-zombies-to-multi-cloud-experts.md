# 从“云僵尸”到多云专家

> 原文：<https://devops.com/from-cloud-zombies-to-multi-cloud-experts/>

与[云迁移](https://devops.com/?s=cloud+migration)相关的一个重大风险是超支。多年来，对 AWS 的僵尸般的服从导致了许多组织的价格锁定和费用上涨——这是一个与云僵尸斗争的故事。

围绕数据出口或应用带宽的云成本通常不透明，因此高度不可预测。让这个问题变得复杂的是快速开发和扩展大型应用程序生态系统的需求，这导致项目工程师仓促做出购买工具的判断。或者，云购买决策由首席财务官做出，他可能没有资格理解技术上的细微差别。如果没有对云支出的预先考虑，很容易做出令人不快的定价承诺。

然而，这一切都在改变。随着云服务提供商(CSP)产品的成熟，竞争对手开始接受 AWS，在整个云环境中为消费者提供了更多选择。在一个多云的世界里，[云经济学家](https://devops.com/the-rise-of-the-cloud-economist-the-other-cfo/)正在利用提升和转移能力来优化性能。具有讽刺意味的是，公司也看到了保留一些本地服务器的成本优势。

我最近与 Virtana 的首席转型官 Scott Leatherman 进行了交谈，了解他对防止云成本上升的看法，以及 IT 部门应如何简化多云环境以抑制云预算。

## 云中的僵尸

当云到来时，它承诺以低成本获得高性能。为了简化云安排，公司很乐意卸载内部服务器。莱泽曼说，多年来，人们对云平台有一种“僵尸般的忠诚”。

很少有人想到随着网络、移动和物联网的天文数字般增长，成本也在上升。高管们不假思索地签订了长期定价合同。最终，现实降临了。而且价格不菲。

## 幽灵云费用

随着云计算业务的兴起，他们遇到了许多隐性费用。仅举几个例子:

*   **Egress** :将数据移入和移出云端的费用。
*   **应用**:将应用迁移到新实例的费用。
*   **工作负载**:增加带宽和工作负载的成本。

这些和其他附加服务可能会很快将每月的云账单从 200 美元提高到 200，000 美元。让情况变得复杂的是，许多大型组织购买了锁定在特定价格的多年期云订阅。

莱泽曼说，与直觉相反，这种成本节约保证是“完全落后的”。根据摩尔定律，随着计算能力的指数级增长，服务器的维护成本也越来越低。

“你实际上是在承诺做一些成本正在下降的事情，”他说。然而，这些节省并没有渗透到消费者身上，服务级别协议仍然相当平淡。“最让我沮丧的是，经营这家企业的最佳方式是把人锁在里面。”

## 僵尸开始意识到

在 COVID 刺激的数字转型之后，云僵尸正在醒来削减预算，在多云战略中找到成本效益。一些公司甚至重申与本地服务器的联系。

如果性能抵不上成本，那就完全抵消了迁移到云的好处。那么，我们如何明智地优化我们的环境，以获得高质量的性能和更少的财务利润呢？莱泽曼分享了一些实现云智能的步骤:

**1。基线您的足迹**

降低云成本的第一步是维护所有云依赖和私有数据中心的基线。这应该包括深入的成本和性能分析。

“您的数据中心需要一个基准，我可以移动什么？我该动什么？”莱泽曼说。除非您对您的数据中心正在做的事情(私有和公共)有一个基线，否则您永远无法理解哪些资源应该转移到云。用于监控公共云的强大应用程序可以帮助审计架构。

**2。优化，优化，优化**

只有在映射拓扑之后，您才能开始优化性能。由于使用情况因季节而异，云优化应该响应全年的应用使用趋势。例如，ERP 软件可能会在季度末拉动更多的请求，而电子商务会在假期出现高峰。

组织应确保弹性云真正根据应用需求扩展，但仅在需要时扩展。确保协调和路由系统正常运行，并努力寻找隐藏的费用。莱泽曼说:“在弹性云中悄悄靠近你的成本总是会出现的。”。

繁重的计算过程，如基于大数据的机器学习，将需要大量的服务器消耗。对于资源密集型场景，Leatherman 建议保持代码精简。虽然 CPU 依赖于物理定律，但“应用程序开发人员只受创造力的限制，”他说。

应用程序开发人员应该尽可能优化代码以避免冗余。这样做还会产生积极的环境影响——消除运营效率低下可以减少云服务器的使用，从而减少碳足迹。

**3。提升和移动**

GCP、Azure、甲骨文等 CSP 成熟，对 AWS 僵尸般的忠诚正在消退。“现在云供应商之间已经平等了，事情正在发生变化，”他指出。“市场的灵活性确实是动态的。”

在多云世界中，组织可以利用混合云，并“提升和转移”到满足其特定需求的最佳成本优化。在这种情况下，保持一个强有力的基准将有助于不断测试云竞争对手的成本效率。

**4。优化您的工具采购流程**

另一个解决方案包括仔细检查您的云采购流程和相关人员。如上所述，新的云工具采购可能发生在开发运维级别，或者大型合同可能升级到 CFO 办公室。

不幸的是，双方都不处于做出明智财务决策的理想状态——一方面临交付的紧迫性，另一方看不到森林中的树木(尤其是没有白蚁吃掉宝贵的木材)。许多人认为需要一个新的角色来帮助优化云堆栈。

**5。保留并优化私有数据中心**

到目前为止，大多数企业都习惯于同时拥有数据中心和云中心团队。Leatherman 认为，最终这两个团队必须合作，以避免停机并降低迁移到云的指数级成本。

从安全角度来看，维护内部私有云及数据中心仍有显著优势。通过利用私有资产，您有助于数据保护工作并增强了控制力。“数据中心有价值，”他说。“除非你从那里开始，否则没有人会是 100%的云。”

尽管云迁移似乎不可避免，但根据软件自动化和摩尔定律，内部部署是有价值的。因此，Leatherman 预测第三方的私有云数据中心优化和管理服务将会增加。

**6。面向云成本感知的 AI:*DevFinOps***

最后，人工智能很快就可以在应用程序部署之前自动扫描云成本影响。

大多数 DevOps 团队使用[容器安全扫描](https://containerjournal.com/topics/container-security/methods-to-audit-docker-container-security/)或自动化合规性验证作为其 DevSecOps 流程的一部分。Leatherman 建议，未来的 DevOps 工具将类似地发展，以显示自动通知，实时估计您的行动的云成本。

例如，当工程师正在编写代码时，一个弹出窗口会显示服务器利用率和成本影响明细。或者，内联代码验证建议可以找到冗余来减少浪费。也许我们需要一个新的缩写来代表这个开发者+财务+运营的焦点——DevFinOps，有人知道吗？

这样的人工智能可能不会否定云经济学家帮助管理多云复杂性的需要。“我们仍然需要它们，”莱泽曼说。

## 多云世界中的惊喜

COVID–19 正在加速标记为更短时间范围的部署，迫使更多实例迁移到公共云。企业需要提高性能并满足其服务级别协议。为了减少开支，他们必须快速提升并转移到性能和成本效益最高的环境。

严重性是显而易见的，但现在仓促行动可能会对未来的安全和数据隐私造成灾难性影响。除了不断上升的云成本，还有其他与云相关的风险，这些风险随着多云环境呈指数级增长。“不仅仅是财务支出，还有随之而来的安全性和风险，”莱泽曼说。“有多少人可以访问，这真的很可怕。”

不仅云支出决策必须左移，而且[安全性也必须在开发周期](https://devops.com/shifting-left-with-devsecops-esg-report-exposes-difficulties/)的早期出现。遵守诸如 GDPR 或 HIPPA 之类的法规也应该影响团队如何管理云之间的数据。

## 云相对较新

IBM 支持的一项研究发现[企业在其云之旅中只走了 20%](https://www.ibm.com/blogs/cloud-computing/2019/03/05/20-percent-cloud-transformation/)。许多企业仍处于云转型的初级阶段，90%的企业计划在下一年扩大其云足迹。

云之旅相当漫长，许多人还有相当长的路要走。了解了这一点，云经济的重要性只会上升。正如我最近提到的，[云专业知识现在比大学学位更重要。](https://devops.com/report-cloud-expertise-now-superior-to-university-degree/)

莱泽曼说，当前的力量，如 COVID–19 危机，无疑将继续“将人们推向云”。在响应提供更多更高速度的要求的同时，明智地利用现有资产并在每个可能的级别优化云的使用是至关重要的。“不应该只是云优先，”他说。“它应该是云智能的。”