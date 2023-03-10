# 牛，不是小猫——重访

> 原文：<https://devops.com/cattle-not-kittens-revisited/>

DevOps 的早期充斥着这样的声明:我们需要把我们的服务器当成牛，而不是宠物(小猫)。一年左右的时间里，到处都是这样的重复。我们做到了。我们将[服务器](https://devops.com/?s=servers)从专用硬件中分离出来，我们让启动和关闭变得如此简单，以至于我们只需更换故障服务器(这导致了[自身的问题](https://www.idtheftcenter.org/what-does-the-cloudflare-bug-mean-for-users/))，我们甚至让服务器设计为启动，做好一件事，然后再关闭，直到再次需要——这甚至在十年前都是不可想象的。

我们已经获得了好处。服务器较少受到开发人员和运营人员的关注，标准化使得为它们编写代码变得更加容易，让事情向前发展，并允许另一个团队的成员在因为熟悉而出现紧急情况时参与进来。

但是里面挤满了人，在过渡中发生了一些事情。事后看来，我们应该把它视为一种可能性，但事情变化如此之大，如此之快，以至于我认为没有人在考虑这种可能性。

我们的 DevOps 工具/工具链/过程成了我们的宠物(小猫)。

现在，需要特定知识并且必须小心处理的特殊雪花是 DevOps 步骤，而不是它使用的服务器。就像宠物服务器一样，正在工作的脆弱的步骤像瘟疫一样被避免，当它应该被支撑的时候。就像宠物服务器一样，一个进程被锁定在一个特定的工具、操作系统或平台上，即使其他选项是更好的解决方案。就像宠物服务器一样,“知道一切”的人被留下来管理这个步骤，这个步骤理所当然地应该被 DevOps 团队中的任何人容易地理解。

是时候开始像对待牛而不是小猫一样对待 DevOps 了。一些步骤(比如一些服务器)将更难做得不像宠物而更像牛，但是如果历史可以作为衡量标准，回报是值得投资的。

我们没有跨工具集的语言，除了在各种 shell 中做事情和从给定的工具集中调用 shell 脚本(这不是最好的解决方案，只是我们所处位置的一个例子)，但是这不应该阻止我们尽可能地标准化和通用化。更少的脆弱性，更多的可重用性和更广泛的支持团队对每个人都有好处。

你们都太棒了。我们——我们所有人——比以往任何时候都要花更多的时间在数字空间的工作和家庭中，总的来说，这些工具“工作正常”这全靠你了。继续踢。但是标准化以保持事情顺利运行是有意义的。你了解你的组织；最简单的方法可能是标准化一个工具链(也许是一个或两个记录了可重用性的工具链),可能是将一堆步骤塞进脚本，并在每个团队选择的任何工具之间共享(我和历史强烈反对这种方法，但是我和历史都不需要生活在您的环境中。这可能有一个很好的理由，所以我把它包括在这里)。

我要说的是，如果可以避免的话，不要一遍又一遍地重新实现每一步，不要把步骤做得如此晦涩难懂，以至于需要一个专家(不是内部的，也绝对不是外部的)。继续摇，让那些牛动起来！