# 勒索软件将在 2017 年翻倍。你准备好了吗？

> 原文：<https://devops.com/ransomware-will-double-2017-prepared/>

最近的一份报告发现，2016 年勒索软件攻击翻了两番，2017 年可能会翻一番。毫不奇怪，[的一项研究调查](https://sentinelone.com/article/sentinelone-reveals-half-global-businesses-suffered-ransomware-attack-last-year/)显示，去年有 48%的组织受到勒索软件的攻击。正如我们在[最近的博客文章](http://datos.io/dont-let-applications-databases-become-ransomware-target-protect-database/)中强调的，下一代云应用和数据库正迅速成为犯罪分子的诱人目标。

攻击者现在的目标是关键数据或操作，而不仅仅是文件。过去两周的几个例子凸显了这一趋势:

*   [德克萨斯州一个警察局因勒索软件丢失了八年的证据](https://www.computerworld.com/article/3163046/security/police-lost-8-years-of-evidence-in-ransomware-attack.html)。包括监控和人体摄像头视频在内的文件永久丢失。该部门的备份过程在文件被感染后启动，因此备份也无法恢复。
*   就职典礼前八天，华盛顿特区的警方监控摄像头遭到攻击。勒索软件让大部分摄像头离线四天，直到软件可以重新安装。
*   奥地利一家豪华酒店在房间钥匙卡系统被禁用后向袭击者支付了赎金。勒索软件在旅游高峰期袭击，迫使酒店支付赎金，以便客人可以回到自己的房间。

攻击者变得越来越聪明，他们在企业内部挑选有价值的目标。勒索软件攻击运行在这些平台上的基于云的应用程序只是时间问题。你能做什么？做好准备。

分层的“洋葱策略”意味着使用一套安全工具来发现和隔离恶意软件和勒索软件，但仅此还不够。国土安全部[去年发布了一份警告](https://www.us-cert.gov/ncas/alerts/TA16-091A),强调了备份在防御勒索软件中的关键作用:

对所有关键信息采用数据备份和恢复计划。执行并测试定期备份，以限制数据或系统丢失的影响，并加快恢复过程。注意，联网备份也会受到勒索软件的影响；关键备份应与网络隔离，以获得最佳保护。

正如德克萨斯州警察局的例子所示，如果备份本身被感染，从备份中恢复将不起作用。业务数据和文件的版本化备份对于恢复至关重要。这就是大多数备份解决方案的不足之处，[，](http://datos.io/protecting-data-public-hybrid-cloud/)尤其是对于下一代应用程序和数据库，由于它们的分布式特性，无法通过停顿来在整个数据库群集中制作一致的备份副本。更重要的是，考虑到这些应用程序处理的数据量很大，对于应用程序一致性备份来说，数据进出群集不存在瓶颈至关重要。

— [Jeannie Liou](https://devops.com/author/jliou/)