# DevSecOps 实现:SIEM

> 原文：<https://devops.com/devsecops-implementation-siem/>

世界充满了事件。我们的收件箱充斥着营销人员真正希望我们关注的事件，而新闻源则充斥着他们试图在背景噪音之上提出的事件，但随后，狗叫声打断了我们对这些信息的消费。与此同时，我们的家人给我们发短信，告诉我们家庭层面的事件，这些事件可能与国家或世界舞台上的事件有关……与此同时，[社交媒体](https://en.wikipedia.org/wiki/Social_media#:~:text=Social%20media%20are%20interactive%20Web,the%20lifeblood%20of%20social%20media.)充斥着关于事件的垃圾信息，这些信息可能是真实的，也可能不是真实的，你可能关心也可能不关心。

我们忽略了绝大多数的这些输入，继续我们的一天。需要我们注意的输入通常，但不总是，得到它。有时，我们在过滤、判断重要性或两者都做得很糟糕，这会产生影响生活的后果。

这和[安全信息与事件管理](https://devops.com/?s=SIEM) (SIEM)诞生时的安全事件管理状态差不太远。不同的信息从四面八方传来。分析师——无论是专门的安全人员还是戴着额外帽子的系统管理员——都必须猜测几十、几百甚至几千个事件中的哪一个是对环境的真正威胁。

控制环境的第一步是标准化和聚合。将事件放在一个地方，相似的信息可用于相似的事件。暹罗就是从那里来的。

从那以后，事件的数量持续上升。以前每天看到数百个事件的公司现在每小时看到数百个事件，SIEM 供应商必须跟上。攻击的复杂性和检测攻击的能力已经提高，SIEM 供应商也必须跟上步伐。用于支持 SIEM 和处理聚合数据的工具不断发展……SIEM 供应商必须跟上步伐。

此时此刻，SIEM 的最佳特征是作为一个数据聚合平台，其有限的智能有助于过滤不相关的事件。这类似于关掉社交媒体，告诉你身边的人如果需要就打电话；它过滤掉最糟糕的噪音，提升最重要的信息。

其他工具可以分析自己的数据并做出自己的推断，但 SIEM 是将所有安全相关事件捆绑在一起的地方，因此它是过滤噪音和提高意识的合理位置。但是它需要大容量、适应性强的数据存储。供应商已经到达了那个平台。

一旦解决了音量问题，SIEM 供应商就开始帮助过滤疯狂的安全事件噪音。是的，如果 Bob 登录到一个新的工作站，这是一个安全事件，但它可能不是一个*值得注意的*安全事件。除非 Bob 的新工作站位于该公司不开展业务的国家/地区，或者 Bob 仍然登录在自己的工作站上，幸运的是不知道另一次登录。

因此，对 SIEM 中的事件数据应用了基本的过滤器。这消除了大量的噪音。接下来是过滤事件，从逻辑上看，这些事件看起来像值得注意的安全事件，但仅仅是*不是*。有东西在扫描防火墙上的端口。内部防火墙。听起来很糟糕，除非安全工具的日志显示是授权用户启动了扫描。然后，这是一个简单的问题问用户，“你在扫描 X 吗？”继续前进。对于系统来说，最好是降低事件的重要性，因为事实上是授权用户使用公司批准的工具进行扫描。然后，分析师可能根本不需要介入(我的安全朋友畏缩了，因为从字面上看，他们不信任任何人，并会指出授权用户也可能滥用工具——所以我在这里会注意到这一点)。

但是事件数量持续上升，分析师们甚至被淹没了。在添加新的报告应用程序(仅 HIPS 就可以向 SIEM 添加数千个报告点)和增加现有监控点的事件之间，情况很糟糕。

输入 AI。这是机器学习(ML)开始成为 SIEM 标准的时候。现在，我们希望系统避免使用必须维护的硬性规则，而是使用它通过观察数据流和分析师的分辨率获得的知识来选择性地提高/降低事件的优先级。现在，实际上出现在分析师面前的事件是 ML 引擎认为可疑的事件，并且数量大大减少。假阳性仍然会发生，但不会像以前那样多，因为系统学会了如何检测它们。

但是等等！还有呢！

对于数据科学家和知识渊博的安全人员来说，将所有数据放在一个地方并由 ML 引擎覆盖实在是太有诱惑力了。因此，能够通过看似不相关的安全事件绘制路线，并确定*这个*或*那个*实际上是入侵者或攻击者活动在系统中传播的证据，这是下一个目标。这就是我们现在所处的位置——将分析师(或系统)可能过滤掉的事件点连接起来，以找到指示入侵的模式的能力。

但这是有代价的。建立这样一个系统并不便宜，训练起来也不容易，而且维护一个从各个地方获取输入并试图关联产生的数据集的系统是…工作。我们不是在谈论一点点数据，就像它来自的环境一样，我们不是在谈论一点点复杂性。你需要它吗？我会说是的。即使您仅将 SIEM 用作大数据存储，它也可以帮助您在发生违规时(而不是在发生违规时)执行事后检查。这是值得努力的，除非你很小或没有互联网存在可言。

继续摇吧！当你走向统治地位时，SEIM 是另一个可以考虑的工具，但同样，它只是一个需要你保持组织安全的工具。