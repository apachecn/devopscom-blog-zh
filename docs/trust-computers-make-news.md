# 信任和电脑制造新闻

> 原文：<https://devops.com/trust-computers-make-news/>

OpenSSL 中的心脏出血错误是本周的主要新闻。当您等待 sudo apt-get dist-upgrade 在您的所有服务器上运行时，让我们花一点时间来思考 SSL 信任系统是如何工作的，以及依赖于它的各种系统关系。

简单回顾一下，基于 SSL 的信任来自于一个“受祝福的”证书颁发机构，这个证书颁发机构可以创建其他可以“受信任”的证书，只要它们的血统可以追溯到最初的颁发机构。在这个系统中，“我应该相信你吗？”是二进制；根据证书链，答案要么是“是”，要么是“否”。

如果认证机构受到威胁，那么所有派生的可信系统也会受到怀疑。真证书变得无法与假证书区分开来，并且不再可能知道“谁或什么值得信任”。绝对的全有或全无信任是基于证书的信任和基于 X.509 的信任系统的固有弱点。

这种情况让我开始思考人类信任系统和计算机信任系统之间的区别。有趣的是，人们对信任计算机采取了非常不同的方式，就像我们对彼此一样。我们很少能回答“我信任你吗？”关于另一个人，用简单的“是”或“否”来回答所有情况。大多数情况下，答案是“这取决于”我们信任另一个人去做什么，这一点可以更好地用可信任度的概念来描述。在人际网络中，你建立信任的基础是你对这个人的了解，他们的诚实和声誉，以及来自其他人的信息，这些人有着与你试图评估的人相似的经历和互动。

SSL 不让我们评估计算机的可信度。它给出了一个“确定的”信任答案，我们对这个答案寄予了太多的信心。基于网站的 SSL 认证，我们很容易将我们的信用卡交给陌生的计算机，而这种方式是我们不会对人做的。

在计算中建立信任有 SSL 的替代方案。例如，Pretty Good Privacy (PGP)是一个信任系统，其运行方式有点类似于人类对彼此信任的看法，尽管它需要额外的开销来管理基于个案建立的信任系统。此外，PGP 不一定包含类似于可信度的“可靠性”参数的历史经验。

本周的新闻强调了对可访问和可管理的信任系统的需求，这种信任系统可以提供介于 SSL 提供的信任类型和像 PGP 这样的逐案管理的信任系统之间的可信度评估。