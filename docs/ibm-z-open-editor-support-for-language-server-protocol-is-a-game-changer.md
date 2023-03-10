# IBM Z 开放编辑器对语言服务器协议的支持是一个游戏改变者

> 原文：<https://devops.com/ibm-z-open-editor-support-for-language-server-protocol-is-a-game-changer/>

集成开发环境(IDE)是软件开发人员不可或缺的工具。在它出现之前，编码是一项艰苦细致的工作。我们已经习惯了语法检查和代码完成功能，甚至比最基本的 ide 提供的功能还要多。如今，我们往往会忘记，只用一个基本的文本编辑器编程是多么困难。像查找一个丢失的逗号或一个放错位置的花括号这样简单的事情会导致编译错误，这可能需要几个小时，如果代码库足够大的话，可能需要几天。当你为了找到运行时错误的罪魁祸首而在看似无穷无尽的函数和类链中追踪时，嗯…fuggedaboutit！如果没有现代 IDE，我们将会陷入困境。

嗯，那是过去，这是现在。几年前，技术领域出现了一种新技术，它增强了 IDE 的功能，并随之将开发人员的工作范围和决策范围提高了一个数量级。这项新技术就是语言服务器协议(LSP)。![](img/4e94068f8645cb15dd30d696d31aaca2.png)

## **LSP 将 IDE 带到了一个全新的水平**

LSP 是微软开发的一个 [规范](https://microsoft.github.io/language-server-protocol/specifications/specification-3-14/) ，它标准化了在编程 IDE 中实现某些典型特性的方式。LSP 试图将 IDE 常见功能(如代码完成、悬停提示、跳转到定义、查找引用和语法检查)的实现整合到一个标准格式中，该格式可以以不可知的方式应用于任何 IDE。

LSP 是一项旨在解决以下问题的技术。 想象一下，一个工具供应商有一个实现新插件的想法，这个插件将为用 COBOL 编程语言编写的程序自动完成代码。这种特性可能对任何数量的 COBOL 程序员都有用。然而，并不是每个 COBOL 程序员都使用相同的工具进行编程。有些人可能正在使用 IDE，例如用于 z/OS 的[IBM Developer](https://www.ibm.com/us-en/marketplace/developer-for-z-systems)。另一种可能是使用文本编辑器，比如 [崇高文本](https://www.sublimetext.com/) ， [原子](https://atom.io/) 或者甚至是更基本的东西，比如[vim](https://www.vim.org/)。在早期，为了将该特性推向市场，供应商需要以特定于给定开发环境的方式实现不同版本的插件。会有一个团队致力于插件的高级文本版本，另一个团队致力于 vim 插件等等。不仅工具开发人员需要适应不同的操作系统，而且每个团队都可能想出自己特定的方法来实现该特性。随着团队成员离开公司，新成员接替他们，这些新的开发人员需要学习实现特性的每一种特定方式。正如你所看到的，不仅多样性滋生了复杂性，而且东西很快变得非常昂贵。

LSP 不再需要这种专门的工具开发。LSP 提供了可以在任何工具中实现的标准协议。该协议定义了一组标准方法、对象和通信方法，在任何 ide 中提供一组通用的服务。

因此，要将前面描述的 COBOL 代码完整特性推向市场，唯一需要做的工作就是用一种与 LSP 兼容的方式来表达它。实现该特性的实际工作包括编写一个支持该标准的客户端。可以说这是一个“一环定天下”的过程。

LSP 规范最初由 Microsoft specific 发布。但是这个标准已经被全行业奉为[](https://langserver.org/)。在[Java](https://github.com/eclipse/eclipse.jdt.ls)[c++](https://github.com/MaskRay/ccls)[c#](https://github.com/CXuesong/LanguageServer.NET)[Python](https://github.com/sourcegraph/python-language-server)[Scala](https://github.com/scalameta/metals)[中有实现还有 z/OS](https://github.com/rlovelett/langserver-swift) 下有一个针对 [COBOL 的 LSP 实现，这就把我们带到了 IBM Z Open Editor。](https://marketplace.visualstudio.com/items?itemName=IBM.zopeneditor)

## **在大型机中使用 LSP**

[IBM Z Open Editor](https://marketplace.visualstudio.com/items?itemName=IBM.zopeneditor)是一个免费的 Visual Studio 代码扩展，为 [COBOL](https://www.ibm.com/us-en/marketplace/ibm-cobol/resources) 和[PL/1](https://www.ibm.com/us-en/marketplace/pli-compiler-zos/resources)开发人员提供了一流的编程体验。还有，IBM Z Open 编辑器集成了[Eclipse Che](https://www.eclipse.org/che/)和 [Eclipse 忒伊亚](https://theia-ide.org/) 。与 Eclipse Che 和忒伊亚的集成特别有趣，因为它支持基于浏览器的编辑。这是一个强大的工具，尤其是考虑到历史上 COBOL 和 PL/1 程序员一直生活在现代 IDE 开发的死水中。IBM Z Open Editor 使基于 IDE 的软件开发成为一种普通的编程体验。开发人员可以使用相同的工具来编写 COBOL，就像他们使用 Java 甚至 HTML 一样。

| **IBM Z Open Editor 中启用 LSP 的特性**下面是在启用 IBM Z Open Editor 的情况下，使用 Visual Studio 代码的大型机程序员可以使用的工具特性列表:

*   代码完成。
*   将鼠标悬停在说明和片段上。
*   跳转到定义。
*   工作空间符号。
*   查找参考资料。
*   诊断和语法错误检测。
*   概要视图。
*   在 hover 上预览包含的字帖。
*   导航至字帖。
*   代码模板片段。
*   重构，如“重命名符号”
*   变量补全。

 |

使用一个 IDE 来编写多种语言的程序是一种已经发展了一段时间的趋势。但是，将 LSP 添加到组合中允许任何 IDE 呈现一组一致的设计时功能。例如，一个 IDE 现在能够完成代码完成、悬停报告和变量跟踪，而不管使用哪种编程语言。

例如，下面的图 1 显示了 IBM Z Open Editor plugin For Visual Studio 代码的 COBOL 代码完成特性。IBM Z Open Editor 使用 LSP 来促进代码完成。

![](img/33cd021774ec6d322c3b96023291f2c5.png)

Figure 1: IBM Z Open Editor uses the Language Server Protocol to facilitate context-sensitive code completion.

图 2 显示了 IBM Z Open Editor 的搜索和排序特性，它也是根据 LSP 实现的。

![](img/85fd1f8de8e5062c3a6fcf71e746a1ba.png)

Figure 2: Using LSP to implement IBM Z Open Editor’s sortable and searchable outline view for navigation.

最后，图 3 显示了 IBM Z Open Editor 如何利用 LSP 的可扩展性来实现 这是一个解析并加载复制本以供预览的特性。一个 [字帖](https://en.wikipedia.org/wiki/Include_directive#COBOL) 是可以从主源复制并插入到几个不同程序或单个程序的不同位置的代码。copybook 用于定义程序数据的物理布局，例如变量，以及程序代码的实例。

![](img/0a0f04eef5b322d60228301ff7389abe.png)

Figure 3: IBM Z Open Editor extends LSP to review and load a copybook within Visual Studio Code.

很明显，LSP 给大型机编程体验带来了很多好处。现在，工具开发人员可以使用通用方法创建统一的编程体验。但是真正有趣的地方是当 LSP 被用来报告超出标准编程和代码管理活动的数据时，报告使用已部署代码的人的实时行为。换句话说，LSP 不仅可以获取开发者桌面本地的代码信息，还可以获取运行时在互联网上使用的代码信息。

## **超越大型机:LSP 的长期意义**

LSP 根据设计是可扩展的。如上所述，IBM Z Open Editor 扩展了 LSP，允许程序员预览和加载 copybooks。这是通过扩展协议来实现的。

LSP 下典型的 IDE 到服务器的交互是，当一个代码文档被打开、更改、保存和关闭时，LSP 客户端向 LSP 服务器报告。然后，一旦 LSP 服务器意识到代码文档正在运行，服务器就可以检查该文档并报告与编程语言相关的事件(图 4)。

![](img/45ef5b8edfa2d8c686c57c4b38999c85.png)

Figure 4: LSP uses a predefined set of commands and request/response objects to support programming IDE is a language and operating system agnostic manner.

例如，LSP 服务器可以检查文档以确保代码在语法上是正确的。如果遇到错误，服务器会报告错误的开始和结束位置，并附带一条消息。在复制本检查特征的情况下，客户端报告光标在代码窗口中的位置，并且服务器确定复制本检查的机会并相应地通知客户端。

虽然字帖预览功能很强大，但它仅限于即时文档。这很好。但是，想象一下，如果服务器知道在连接到互联网的计算机上部署和运行的代码的所有实例，会是什么样子？

例如，假设您的代码支持运行在互联网上的 API，并且您有能力了解对支持该 API 的特定函数的调用次数，或者更好的是，想象您有能力了解遇到特定问题的函数调用，例如错误输入的参数模式或高延迟调用。然后想象一下，如果在 IDE 中报告了全局运行时行为，会怎么样？这些信息将改变程序员处理工作的本质。更重要的是，它将改变企业管理程序员的方式。

如果程序员可以根据通过 LSP 扩展报告到 ide 中的全局运行时行为来决定做什么，会怎么样？例如，回到错误输入参数的想象模式，假设当开发人员将鼠标悬停在 IDE 中的相关函数上时，会出现一个警告图标，通知开发人员在全局级别出现了 1000 个错误输入的调用实例。开发者认为这样的错误率是不可接受的。然后，他/她检查开发人员的文档，发现函数的参数类型定义描述得很差，文档需要更正。然后，开发人员将更新开发人员文档作为一个关键路径，这是一天中需要立即交付的工作的一部分。

鉴于 LSP 给编程体验带来的力量，这样的场景是完全可能的。事实上，有些公司，如 [阿波罗图形管理器](https://www.apollographql.com/docs/graph-manager/) ，目前允许开发者和第三方注册他们的生产 API，以便收集上述的全局信息，并通过 LSP 在 IDE 中报告。正如我们这些已经在软件行业工作了一段时间的人所了解到的那样，一旦像全球报告这样的功能流行起来，它成为全行业的惯例只是时间问题。向程序员 LSP 交付全球收集的运行时指标变得司空见惯只是时间问题。

再次强调，后果是重大的。一旦程序员有能力做出关于特性开发和部署时间表的基本决策，那么项目经理和产品经理的角色是什么？

更进一步说，程序员应该被赋予多大的权力？就一般商业惯例而言，程序员应该对一家公司的产品了解多少？这些问题可能看起来很奇怪，但是请记住，公司曾经把他们的源代码作为商业秘密来保护。今天，作为开源运动的一部分，更多的代码在公司之间共享。因此，代码的编写方式和开发人员的工作方式都发生了变化。由于扩展 LSP 能力的增长趋势，也存在同样的可能性。LSP 的结果不仅仅是报告语法错误和完成代码。LSP 将改变整个行业的工作方式，从大型机编程到在云中或商用硬件上工作的开发人员。

## **将所有这些放在一起**

鉴于目前的趋势，毫无疑问，LSP 将使最基本的代码编辑器成为软件开发的强大工具。将 IDE 功能标准化为一种通用格式，可以让任何开发工具的新功能以更低的成本更快地实现。我们甚至很快就能找到使用 LSP 的方法，不管使用什么编程语言，只需开发人员在键盘上敲几下键盘，就能自动编写大量代码。很有可能。

LSP 不仅会使编码变得更容易、更快，还会改变软件开发者的角色。一旦运行在互联网上的所有代码都可以被 LSP 识别和访问，开发者将会获得关于他们的代码在运行时如何在全球范围内执行的运行时信息。这一趋势已经开始。历史已经证明，一项技术越深入某一特定人群，这个人群就变得越强大，当这种力量发挥出来时，就会产生越大的影响。支持 LSP 的 IDEs 提供的信息很有可能使日常的程序员在产品决策过程中更加突出，而目前这是程序和项目经理的职责。一旦这种转变发生，我们很可能会看到软件制作和交付方式的另一次行业范围的转变。历史表明，这种转变有长期的好处，但在短期内是破坏性的和令人不安的。我们会做好准备的。

鲍勃·雷瑟曼