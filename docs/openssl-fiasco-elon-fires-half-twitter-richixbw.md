# OpenSSL 惨败:DevOps 能学到什么？|埃隆解雇了推特“50%”

> 原文：<https://devops.com/openssl-fiasco-elon-fires-half-twitter-richixbw/>

欢迎来到[![](img/8e1bf334637b8fb6bf0c280349f31d8b.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周:OpenSSL 项目面临失败，Twitter 一半的员工明天将被解雇。*

 *## 1.尴尬的 Bug——应该被发现

本周首先报道:一年前添加到 OpenSSL 中的一个特性包含了两个令人讨厌的 bug。虽然他们不像上周看起来那么令人讨厌，但他们仍然很坏。

### 分析:C 代码分析器被认为是危险的

我们能学到什么:你已经编写或编辑了一些解析输入的代码？在你祝贺自己之前，你有没有运行一个 fuzzer 来对抗它？

[Sergiu Gatlan](https://www.bleepingcomputer.com/news/security/openssl-fixes-two-high-severity-vulnerabilities-what-you-need-to-know/ "read the full text"):**OpenSSL 修复两个高严重性漏洞**

**`Tagged as vulnerable`**
【CVE-2022-3602 是任意 4 字节堆栈缓冲区溢出，可能触发崩溃或导致远程代码执行(RCE)，而 CVE-2022-3786 可以…通过缓冲区溢出触发拒绝服务状态。…根据 OpenSSL 的政策，自 10 月 25 日以来，组织和 IT 管理员一直被警告要在他们的环境中搜索易受攻击的实例，并准备好在 OpenSSL 3.0.7 发布时进行修补。
…
最新的 OpenSSL 版本包含在多个流行的 Linux 发行版的最新版本中，Redhat Enterprise Linux 9、Ubuntu 22.04+、CentOS Stream9、Kali 2022.3、Debian 12 和 Fedora 36 被标记为易受攻击。…荷兰国家网络安全中心[还列出了[Amazon Linux 2022、NetApp 集群模式 Data ONTAP、Node.js 18/19、Oracle Linux 8、VMware Harbor 和 VMware Tools]。](https://github.com/NCSC-NL/OpenSSL-2022/blob/main/software/README.md)

等等。*暂停。*这不是上周作为[天降](https://securityboulevard.com/2022/10/openssl-critical-patch-richixbw/ "OpenSSL ‘CRITICAL’ Bug — Sky Falling — Patch Hits 11/1")“关键”bug 预演的吗？凯文·波弟嘴硬:

**`Patch as soon as possible`**
曾经被认为是自互联网重塑 Heartbleed bug 以来的第一个关键级别补丁…它最终成为一个针对缓冲区溢出的“高级”安全修复，不太可能导致远程代码执行。…包括 Fedora 在内的一些 Linux 发行版在补丁发布之前一直没有发布。但是这个漏洞主要影响客户端，而不是服务器，所以类似 Heartbleed 的互联网范围的安全重置(和荒谬)不太可能发生。一次攻击可能会覆盖尚未使用的相邻缓冲区，从而导致溢出。…另一个漏洞只允许攻击者设置溢出的长度，而不是内容。
…
然而，任何 3.x OpenSSL 实现的用户都应该尽快打补丁。每个人都应该留意软件和操作系统的更新，这些更新可能会修补各种子系统中的这些问题。

与 OpenSSL 团队沟通并添加他自己的分析，这是[Marcus " @ MalwareTechBlog " Hutchins](https://twitter.com/MalwareTechBlog/with_replies "read the full text"):

“为了您的方便，我们还没有为这个漏洞发布 CVE 号码，我们提前几周就发出了警报。我们还提供了一个 3 小时的发布窗口，以最大化供应商花在谷歌搜索随机搜索词的时间，希望找出 wtf。谢谢大家的理解。”
…
考虑到漏洞的复杂性，主要是客户端的事实，恶意证书需要由可信的 CA 签名，以及受影响的系统数量较少，我认为利用漏洞的可能性很低。……理论上，这可能会导致 RCE，但实际上可能性极小。…在 1-10 分的恐慌值不值得的范围内，我给的分数低于零。

哎哟。并且[原名](https://news.ycombinator.com/item?id=33422861 "read the full text")也同意:

CAs 通常不会让您直接构造您自己的证书，并且我认为您将很难获得一个既用于邮件加密(因此您会得到一个电子邮件名称约束)又用于 TLS (SAN 约束)的证书。大约 99.99%的没有 TLS 客户端认证的服务器不会受到影响。TLS 客户端身份验证通常只在企业网络中使用，并且通常由运行古老软件的中间体终止。

但是考虑到这只是在相当新的 3.x 分支中，它是如何发展到现在的呢？ [@hanno](https://twitter.com/hanno/status/1587775675397726209 "read the full text") 想知道:

这些漏洞位于 punycode 的解析函数中。这是一项新功能…所以没有“这是遗留问题”的借口。
…
解析某个东西的代码…会包含缓冲区溢出，这是最不足为奇的事情。…最简单的 fuzzer 使用标准的先进工具(libfuzzer)在不到一秒钟的时间内就能找到它。【TL；DR:] OpenSSL 添加了新的 C 解析器代码——众所周知容易出现内存崩溃——而没有做任何基本的安全测试。
……
这个错误让人心痛。我们进行了所有这些讨论。我当时在场。…我们似乎已经失去了那些我们已经拥有的洞察力[例如，不要在没有模糊目标的情况下添加新的解析器代码]。

生病烧伤。[失败 2Boot](https://arstechnica.com/information-technology/2022/11/openssl-3-patch-once-critical-but-now-just-high-fixes-buffer-overflow/?comments=1&post=41353541#comment-41353541 "read the full text") 至少庆幸这些 bug 没有被追踪到的那么糟糕:

好吧，那根本不算什么。谢天谢地。

* * *

## 2.马斯克的狡猾计划:裁掉 50%的 Twitter

有消息称，埃隆明天将宣布大规模裁员。DevOps 的工作人员正在为**失去生计**做准备。

### 分析:文化消失了

如果是真的，这就不仅仅是“砍掉枯木”了。这种变化会撕裂一个组织的机构记忆和共享文化的核心，给它致命的一击。**推特:RIP** 。

[Edward Ludlow，Kurt Wagner 和 Emily Chang](https://www.bloomberg.com/news/articles/2022-11-02/musk-plans-to-eliminate-half-of-twitter-jobs-in-cost-cut-drive "read the full text") : **马斯克计划削减一半的 Twitter 职位**

一位知情人士说，产品团队的高级人员被要求实现裁员 50%的目标。…据知情人士透露，Twitter 的新主人计划在周五通知受影响的员工。……马斯克还打算扭转公司现有的随处工作政策，要求留下来的员工到办公室报到。马斯克面临压力，要想方设法削减他认为自己支付过高的业务成本。…在马斯克收购前的准备阶段…潜在投资者被告知，他将裁员 75%。…从那以后，Twitter 员工就一直在为裁员做准备。

通过一些深刻的分析，这里是 [50me12](https://arstechnica.com/tech-policy/2022/11/report-musk-to-lay-off-50-of-twitter-staff-reverse-work-from-home-policy/?comments=1&post=41359572#comment-41359572 "read the full text") :

马斯克和其他类似的人一样，已经想出了一个系统，他们的行为可以过滤特定类型的员工。如果你能忍受他的****，他知道他能从你身上得到更多——否则他对你毫无用处。有些在家工作的无人驾驶飞机可能不太担心，“好吧，我让他们做了一件事，让我们看看我还能做多少。”任何没有做他想要的事情的人，他不需要/想要他们。

所有迹象表明，他让他们通宵达旦地工作。[云沃尔](https://news.ycombinator.com/item?id=33452836 "read the full text")有大-ol' *smh* 瞬间:

老实说，我不明白为什么有人会为了 Twitter 的一份工作而自杀？…对于开发人员来说，似乎仍然有一个不错的就业市场。我真的不明白为什么有人会在周末为埃隆工作。

* * *

## 这个故事的寓意是:
**如果生活是可预测的，它将不再是生活——而且没有味道**

*—埃莉诺·罗斯福*

*你一直在读*里奇·詹宁斯的《远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#82f6eef4c2f0ebe1eaebace1edacf7e9bdf1f7e0e8e7e1f6bfafd6ced4af) 联系他。*

图片:[Kenshi Kingami](https://unsplash.com/photos/Y2gfzL5qohA)(via[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)*