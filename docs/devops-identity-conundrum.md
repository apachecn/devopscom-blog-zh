# DevOps 和身份之谜

> 原文：<https://devops.com/devops-identity-conundrum/>

“我是谁？”这也许是最基本的意识问题。答案可以根据我生活故事的各个方面来细分……我的职业、我的家庭、我的信仰、我的教育……这个清单还可以继续。但是因为我是独一无二的，所以这个数字时代的挑战是我要以某种方式保持独一无二，无论用什么样的描述来描述我，我都必须保持在所有描述的中心。如果我的身份被盗，别人怎么知道我就是我所说的那个人？

这个问题是我与数字世界互动的基础。不幸的是，每一个与我互动的系统都希望我重新定义我是谁，一次又一次地为他们重新定义。我创建了一个脸书个人资料，一个 Twitter 个人资料，一个 LinkedIn 个人资料…这个清单还在继续。但我们数字时代的另一个弱点是，这些系统之间没有交叉参考来确保我是我所说的那个人。这种现象在 DevOps 工具中也是如此。

## **职业身份难题** 

让我们只关注我是谁的一个方面，我的事业。我现在的雇主是谁决定了我应该访问什么样的电子商务系统和网络。跳槽到另一个雇主改变了——或者应该改变——我拥有的访问权限。但更具体地说，我在当前雇主那里的角色也应该对我可以使用哪些工具以及在这些工具中我可以做些什么产生影响。随着我的角色改变，我在工具中的能力也应该改变。如果我从实践者，到管理者，到主管，我在给定工具中的能力可能会减少，让实践者对行动负责，而不是通过自己做事情来取代他们的责任。

然后是我工作的重点领域。与产品或服务“b”相比，业务细分将我的工作与产品或服务“A”区分开来。我的角色可能是应用程序程序员或数据库管理员，但我在公司内关注的“谁”是另一个层次的区分。企业可能更希望专注于产品“A”的团队不能对产品“b”进行实质性的更改。因此，两个不同的数据库管理员需要在同一个工具中有两个不同级别的访问权限，通过业务线或产品线来实现。

## **职业一致性难题**

在数字时代，我的企业身份的问题在于，它是流动的，就像生命一样。在我的职业生涯中，我会不时地更换雇主。但除此之外，随着时间的推移，我会在同一家公司内改变角色和/或关注领域。在我为某个雇主工作期间，除了我的正常职责之外，我还可能被分配去做一个“特殊项目”。在 DevOps 依赖几种类型的工具来促进连续性的地方，我职业生涯中的这种流动性使我很难跟上，并且会使管理成本相当高。

例如，如果我是一名应用程序程序员(正常情况下)，那么我将在构建、部署和发布工具中具有某些能力——可能在构建中具有高能力，在部署中具有中等能力，在发布中具有低能力。如果我被临时指派为一个不同产品/服务的发布经理(除了我的正常职责之外)，这将从根本上改变我在 DevOps 工具中的能力，至少在短时间内。但是当我回到正常的工作岗位时，唯一能让我的能力恢复正常的机制就是一个强大的过程控制系统。这些工具对此没有任何帮助(没有提醒，没有检查人力资源系统中的角色，没有互相看看我应该是什么样子)。

## **身份架构**

在我看来，解决这类问题的不变因素是时间和我是谁。如果我能持有一个标识结构，用职业术语来标识自己——哪个雇主，哪个角色，等等。以及持续多长时间——这种身份建构可以被每一个接受它的系统所采用。实际上，这将是用户管理的终极抽象，将负担从公司和人力资源部门转移到了解并需要了解最终用户的个人身上。虽然公司仍然需要与我的个人身份结构进行交互以进行验证、同意和记录保存，但让所有电子系统接受我的身份结构可以省去对这些接口进行编程的所有工作，使权限和角色变得通用，并跟上生活的流动性。

此外，我是谁在每一个接受这种建构的系统中都变得相同。我不能在一个工具中将自己定义为发布经理，在另一个工具中将自己定义为测试经理，在另一个工具中将自己定义为应用程序程序员，从而在我公司的 DevOps 工具中赋予自己上帝般的能力。每个工具将检查我持有的相同的身份构造，并从中接收我的正常职责、角色、权限等。我将拥有一个跨公司工具的一致的配置文件，它将反映我的最新角色，并使用日期(开始和结束)来对照他们自己的记录验证我。

## **一个身份锁箱**

关键是，我如何防止这个身份构造被窃取？我相信这就是生物识别开始发挥关键作用的地方。指纹技术现在很普遍，甚至在手机中也是如此，手机通常像一个额外的手指或脚趾一样拴在我们身上。我们很少去没有他们的地方。当携带它们时，我们使用触控 ID 等功能来代替手动键入密码。如果我的身份构造是在我可能独自拥有的信息和只适合我的生物特征(视网膜扫描、指纹等)之间配对的。)，配对可以解锁该构造用于使用或修订。

窃取构造没什么好处，因为没有配对生物特征，它就不能被使用或修改。像这样的身份构造的应用是无限的——从获得投票权、工作权和领取社会保障金到验证信用卡购买和开设新的社交媒体账户。如果脸书采用(或接受)这种构造，创建关于我的欺骗账户将会更加困难，因为无与伦比的配对可以破译谁真正拥有一张照片或文件等。展望未来，像这样的标准化身份结构可以与新兴的物联网世界互动，设备可以了解我的很多信息，并知道这是真正的我。

## **对底线的影响**

我并不是在暗示某种疯狂的世界末日场景，电脑控制着我们的一举一动。我们已经有了这样或那样的形式。但我建议，为了恢复数字隐私，我们应该将身份构造的所有权归还给拥有它们的人:我们。我们每个人都应该拥有自己独特的结构，保持它的最新状态，并按照我们的意愿进行填充或完善，只分享我们想要的东西。这样做的主要好处是增加了从我们这里窃取它们的难度。我们都可以跳过 666 纹身，而是通过拥有我们自己的数字身份来试图重新获得隐私的绰号。像使用万能钥匙一样使用它们，打开我们“应该”访问的系统和我们“需要”执行分配给我们的工作的能力。

对公司来说，有利的一面是安全性提高了，需要维护的部分减少了。带有开始和结束日期的一组记录验证了使用或试图访问的 id。软件行业作为一个整体的优势是一个使用谨慎的身份识别登录应用程序的通用界面。如果解锁访问还需要生物特征对，它消除了“借用”ID 的疑虑。它将允许每个应用程序抽象用户管理，并使之通用。角色将被抽象化。基于每个应用程序对角色的解释，它们的权限可能是唯一的。

转向自我维持的身份建构，可以在我们生活的其他领域带来更多益处。虽然我们已经讨论了我们身份的职业部分是如何被细分和分类的，想象一下将我们的健康特征与同一种身份结构联系起来的好处。家庭记录、会员资格和协会…选择你对一个人的分类。在数字时代拥有这些东西的所有权是保持我们在世界上独一无二地位的关键。失去对这些事情的控制会成为灾难。与社会收获的利益相比，DevOps 从这样的构造中受益的地方只是冰山一角——或者至少，如果我们追求它，我们的数字社会可以收获。

要继续对话，请随时[联系我](/cdn-cgi/l/email-protection#59122b302a2d30383777173c352a36371931362d34383035773a3634)。

[克里斯琴·纳尔逊](https://devops.com/author/knelson/)