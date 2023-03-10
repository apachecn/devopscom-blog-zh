# DevSecOps 如何帮助避免灾难性违规

> 原文：<https://devops.com/how-devsecops-can-help-avoid-catastrophic-breaches/>

今年早些时候，[特斯拉的云被劫持](https://www.infosecurity-magazine.com/opinions/tesla-hack-cryptojacking-warning/)并用于开采加密货币，利用了该公司 Kubernetes 集群中的一个漏洞。堆积如山的[联邦快递数据](https://arstechnica.com/information-technology/2018/02/fedex-customer-data-left-online-for-anyone-to-rifle-through/)最近被曝光，影响了 119，000 个人。在估计有 1.455 亿美国人受到危害后，Equifax 漏洞引起了国际关注。在其他新闻中，我们已经报道了 [Vine Docker 注册表惨败](https://containerjournal.com/2016/08/04/vines-registry-fiasco-means-docker-security/)如何被黑，留下了一个尴尬的公关痕迹。

所有这些场景的共同点是什么？如果有健康剂量的国防开支为基础的基本保障措施，这些问题可以避免。事后来看，让我们看看开发人员可以采取哪些具体策略来避免这种可怕的泄漏。

## 基本的 DevSecOps 可以防止漏洞

DevSecOps 被描述为将安全性放在每一个操作的最前面。在云工具的世界里，这意味着在构建生命周期的每一点都注入保护。您可能会认为这等同于高级容器和编排安全性、强大的访问管理以及为内部应用程序建立强化的监督，对吗？实际上，许多现代漏洞只是缺乏基本的密码保护。

## 案例研究 1:特斯拉云密码劫持

2018 年年中，特斯拉的亚马逊服务器被恶意软件劫持，并被用于为流氓代理挖掘加密货币。金雅拓(Gemalto)、英杰华(Aviva)和其他公司也发生过类似的黑客入侵。根据 [RedLock 的报告](https://redlock.io/blog/cryptojacking-tesla)，黑客渗透进了没有密码保护的 Kubernetes 控制台。在一个 pod 中，他们发现了特斯拉 AWS 环境的访问凭据。据特斯拉称，这次入侵暴露了敏感的遥测数据，尽管仅限于“内部使用的工程测试车”。

### 如何预防

Kubernetes 管理控制台的密码保护是一个显而易见的教训。所有云帐户，即使是内部使用的，也必须配备更好的设备，并隔离访问凭据。当然，灌输一种“安全由设计”的心态可以帮助限制这种游戏机的数量。

## 案例研究 2: Vine 注册管理机构违规

2016 年，化名为 [avicoder](https://avicoder.me/2016/07/22/Twitter-Vine-Source-code-dump/) 的白人黑客得以渗透到视频分享社交网络 Vine。黑客使用工具来发现子域名，并在一个子域名后面发现了一个开放的 Docker 私有注册表，其中存放了 Vine 源代码。这种漏洞可能被用于收集用户详细信息或出于恶意目的注入恶意软件。值得庆幸的是，没有用户受到损害，Twitter Bug 赏金计划因这一发现奖励了 avicoder 一大笔钱。

### 如何预防

在这一特定事件中，Docker 或 Docker 集装箱没有任何问题。这项服务(本来应该是私有的)只是公开的，没有访问控制。教训是万维网上的 URL 就是这样——公开地暴露给世界。如果没有文档链接到它们也没关系；这样的子域很容易被爬虫发现，一旦发现就会被利用。

## 案例研究 3: Equifax 漏洞

在 Equifax 事件中，数百万条客户记录被盗。Equifax 报告指出黑客利用了一个“网站应用程序漏洞”根据 [Apache Struts 项目管理委员会](https://blogs.apache.org/foundation/entry/apache-struts-statement-on-equifax)的说法，进一步的报告详细说明了 2017 年的入侵利用了 Apache Struts 中的缺陷，很可能是通过零日利用。

### 如何预防

有人指出，Apache Struts 应用程序中固有的不可信数据的反序列化留下了一些主要的漏洞和潜在的恶意代码执行。

由于容器的寿命很短，它们不是持久的，因此使得持续的黑客攻击更加困难。他们还可以隔离功能，从而减少攻击媒介。关于 Equifax 违规事件， [Aquasec](https://blog.aquasec.com/equifax-breach-hindsight-what-if-they-used-containers) 推测使用容器可能会减轻影响:

> “…很可能这种违规行为在容器中会更加困难，即使成功了，也不会那么持久，不会那么普遍，也不会很快得到缓解。”

一些人认为，如果为网络连接配备行为分析和防火墙，容器将是一股强大的力量。尽管如此，其他人注意到集装箱更安全这一假设的缺陷。

不管架构如何，在 DevSecOps 中，客户数据的安全性并不在后台考虑；相反，它渗透到整个工具过程中，并在每个构建中保持平等的地位。

## 灌输 DevSecOps 文化

DevSecOps 寻求将安全性提升到每个决策中，而不是现在构建，以后安全的态度。在每一次构建中，安全性都融入了对如何处理数据的影响的更多预先考虑。

Kubernetes 集群的管理控制台必须配备有密码保护，私有 GitHub 存储库或 Docker 注册表也是如此。任何通过云 SaaS 服务的数据传输都必须获得授权。一个最明显的教训是用密码保护那些带有可发现 URL 的“隐藏”注册表。

针对白人黑客的赏金计划继续导致成功的漏洞检测。至少对于这些机构来说，用户数据受损的证据更少，补救速度更快。

其中大部分可以通过尽职调查和培育安全文化来提炼。虽然这对于一些人来说有点模糊，但对于不断取消这些基本保障的机构来说，显然仍需要重复。

— [比尔·多菲尔德](https://devops.com/author/bill-doerrfeld/)