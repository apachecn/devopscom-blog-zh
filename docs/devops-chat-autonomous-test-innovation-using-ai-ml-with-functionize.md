# DevOps Chats:使用 AI/ML 和函数化的自主测试创新

> 原文：<https://devops.com/devops-chat-autonomous-test-innovation-using-ai-ml-with-functionize/>

按照 DevOps 的速度，自动化测试对于 QA 来说是必不可少的，以便与软件创建保持同步。自动化测试的创新时机也已经成熟。我们如何知道我们正在执行最相关的测试，软件中的新功能没有被遗漏或忽略，或者高度动态的应用程序没有超过静态测试用例和逻辑？

[functionalize](https://www.functionize.com/)旨在带来创新以实现自主测试，使测试、测试的创建和维护更加高效。创始人兼首席执行官 Tamas Cser 加入我们这一集的 DevOps 聊天，分享他的公司给 DevOps 团队带来的几项创新。

加入我们，讨论用英语编写测试用例如何有助于捕获意图，并随着时间的推移产生不那么脆弱的测试，以及在运行时实现函数化和以编程方式改变对象模型和内部的能力。了解 AI 如何改善网页的视觉检测和网页行为的变化，以及 AI 如何根除随着软件功能变化而可能不再有效的测试用例。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/695469463&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/695469463&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

米奇·阿什利:大家好。我是 DevOps.com 的米奇·阿什利，您正在收听的是另一个 DevOps 聊天播客。今天，我邀请了 Functionize 的创始人兼首席执行官 Tamas Cser。我们今天的话题非常有趣——自动化 DevOps 测试的 AI 机器学习。塔玛斯，欢迎来到 DevOps 聊天播客。

嘿，米切尔，很高兴来到这里。谢谢你邀请我。

阿什莉:嗯，当然。我很乐意。谢谢你加入我们。你能从自我介绍开始，告诉我们一些关于你和功能化的事情吗？

绝对的。我叫塔玛斯·塞瑟，是 Functionize 的创始人兼首席执行官。我在技术领域工作了大约 15 年，最初是一名顾问，在湾区经营自己的公司，专注于开发，我们也做了许多开发操作和构建基础架构，最初只是看到了发布，然后是云混合。

在那几年里，我碰到了很多次测试，真的是在房子的前面，经营公司，与客户打交道。很明显，很多领域都缺乏测试，随着 DevOps 开始变得越来越成熟，越来越受欢迎，我们也越来越投入其中，测试再次成为一个大问题。

所以，真的，那是我开始测试的时候，我试着看问题，了解我们现在有哪些尚未探索的云和大数据的机会，以及如何应用这些机会来解决其中的一些问题，这就是 Functionize 大约四年前诞生的原因。

阿什利:嗯。

从那以后，这是一次令人惊奇的旅程。现在，你知道，四年来，我们真的获得了一个伟大的团队，我们有一个非常令人兴奋的产品和客户，这是一个不可思议的旅程。

阿什利:太好了。嗯，我肯定想听到更多关于产品的信息等等。首先，在软件部署的世界里，尤其是在 DevOps 的世界里，我们正在自动化，我们正在把事情向左移动，测试只和实际发生的测试一样好。糟糕的自动化测试仍然是糟糕的测试。

在我们转向更像 DevOps 风格的容器云时，您看到了哪些障碍？测试标准中引入了哪些内容？您如何以不同于传统的方式解决这些问题，比如使用 Selenium 风格的工具或类似的工具？

**Cser:** 我认为，如果你考虑整个 DevOps 工具链和云以及包括容器在内的许多自动化，我们在软件开发方面取得的所有令人难以置信的进展带来的最大变化是速度。

因此，随着速度的提高，软件的部署变得更加频繁，公司能够非常非常快速地围绕他们的产品进行迭代。这给回归测试以及测试你发布的任何新特性带来了巨大的挑战，尤其是围绕它的维护是一个巨大的挑战。

所以，我要说，真的，我们最近看到的一些更新的方法的速度，以及敏捷的，每天多个版本，确实给质量部门带来了巨大的压力。因此，有巨大的机会来改善这一点，并真正加快速度，如果你愿意，与 QA 相比，QA 已经停滞了很长时间，如果你回顾过去 15 到 20 年，看不到很多创新。

阿什利:嗯，你知道，这是显而易见的，如果你要更快地生产更多的软件，你需要更快地进行测试。所以，自动化当然非常重要。

你如何看待这样一个问题，当你有了正确的覆盖率时，你如何知道测试正确的东西，记住，你知道，你可能有开发人员，开发人员，工程师以及 QA 人员来定义那些测试标准是什么？

**Cser:** 所以，我认为覆盖率是一个非常有趣的话题，也是我们许多客户都有的一个重要话题，我应该有多少覆盖率，我有合适的覆盖率吗？这也是一个我们可以收集数据、理解和分析来自应用程序本身甚至来自实时用户使用的数据的领域，以便了解模式在哪里，正在使用什么，如果特定的特性或功能崩溃，它可能对软件产生什么潜在的影响。

因此，我再次认为这是一个巨大的机会——这无疑是我们利用自主下一代能力关注的一个领域，我们正在努力缩小这方面的差距，并对公司分析和理解他们真正需要测试什么的能力产生影响。

Ashley: 我相信，如果我没记错的话，就你们的技术和产品而言，你们实际上是以一种英语格式编写测试，而不是代码，对吗？对吗？

Cser: 所以，是的，我们确实有英文版的桌面创建功能。这不是唯一的一个，但这是我们创新的关键领域之一，即理解用户意图和测试用例需要做什么，并能够围绕这一点进行建模，这对于如何随着时间的推移维护测试用例变得非常有趣和非常重要。

因此，对于非常具体的实现和特定的按钮或 HTML 元素交互，这些测试用例变得不那么脆弱了。因此，这是我们正在创新的一个非常令人兴奋的领域。

阿什利:优秀。所以，我也可以想象，作为 CI/CD 流程的一部分，你必须与许多不同的工具集成，或者至少适应一个框架，在这个框架中，你知道，你显然不拥有整个流程。请告诉我们你是如何做到这一点的。

**Cser:** 所以，我们的方法是——同样，这是 DevOps 和构建一项技术的一个超级重要的部分，尤其是在这些天，因为工具链非常重要。因此，我们的方法有两种:第一，我们有通用的 API，并给出现成的解决方案来与你通常怀疑的 GitHub 和吉拉集成

阿什利:和詹金斯。

**Cser:** 还有各种不同的 CI 工具比如 Jenkins。

阿什利:嗯，还有阿吉拉，是的。

**Cser:** 我们正在做的另一件真正有趣的事情是，我们——我们在 Functionize 中有一个生态系统，它基本上允许我们的用户对实际执行测试的运行时环境进行编程。

阿什利:嗯。

这打开了所有的对象模型和实际测试用例运行的隐藏内部。这真的非常非常有趣，因为它让您能够与第三方应用程序或任何其他外部功能进行非常非常深层次的集成，这可能是一种复杂而高级的使用情形。

Ashley: 现在，当测试运行时，你可以通过编程控制功能化，改变或调整它测试的行为，或者它如何测试，或者与此相关的事情，我对你所说的理解正确吗？

**Cser:** 精确，精确。因此，这是市场上的第一项功能，不仅仅是控制测试案例或行为的结果，您还可以访问我们正在收集的丰富数据集，包括我们正在收集的所有视觉截图或视频。

阿什利:嗯。我也知道，你在屏幕截图中以一些非常独特的方式使用了一些人工智能机器学习，也许是产品中的其他方式。稍微谈一谈这个。

当然，我很乐意。因此，随着应用程序一次又一次地运行，显然，应用程序的行为和外观非常重要。因此，有一个客户关心的领域就是视觉测试，“我的应用程序是否按照我和客户期望的方式显示？”因此，这是我们正在努力的一个关键领域，模板识别功能可以检测页面上的破损，这不是基于传统的逐像素计算，查看差异，而是实际的深度学习，可以了解您的页面通常是什么样子，以及我们通常在哪里看到变化，而不是看起来像异常的变化集。

阿什利:嗯。

Cser: 还有另一个领域，也很有趣。这其中的一部分可用于根本原因分析，例如，了解页面发生了什么变化，引入了什么新元素，并且可能有一个现在不再有效的测试用例可被自动更新。

Ashley: 哦，那么，在某些情况下，可能一个页面发生了足够大的变化，以至于测试不再有意义，那种情况？

**Cser:** 正是。您提到有人在表单中添加了几个新的表单字段，现在这些字段是必填的，您无法完成测试。因此，这是我们可以通过分析、可视化分析以及一些 DOM 分析来识别自动用法和相关解决方案的事情。

Ashley: 哇，我们已经从测试 ui 的屏幕抓取矢量图形走了很长一段路，不是吗？*【笑声】*

Cser: 哦，肯定的。*【笑声】*有很多令人兴奋的工作投入其中。同样，我们显然也在利用令人难以置信的开源功能，以及我们在过去一年中在 LP 中看到的进步，所以这是整个行业中真正令人兴奋的进步。

阿什利:优秀。那么，稍微谈一下云环境，你知道，我们生活在一个世界里，你可能是一个云原生应用程序，但你也可能在混合私有云，甚至可能不是云数据中心，你知道，私有数据中心和多云。这些环境会带来哪些挑战，您会如何应对？

Cser: 这是一个很好的问题。总的来说，云环境对我们来说是一个很好的合作环境，而处于云中并利用云的客户对我们来说也是一个很好的合作环境。这并不代表任何一种重大挑战。这实际上让我们更容易合作。

我要说的是，云混合环境或本地环境肯定会带来挑战，我们有各种不同的方式与这样的客户合作，仍然能够带来云的价值、规模和我们所做的大量建模，并且仍然能够测试隐藏在防火墙后面的应用程序。

阿什利:嗯。这是否也是因为传统数据中心中的环境，可能是测试工具等，私有数据中心环境只是该环境特有的，而云环境更标准化，如果您在 Azure 或 Google 或 AWS 中，这是为什么？

Cser: 我会说更多，这与访问有关。这是我们访问应用程序的方式。这是客户提供专用于测试的环境的能力，通过这种方式，这些环境可以获得正确的资源和计算资源，以便在您进行敏捷测试时，它可以处理我们将施加给它的负载。相比之下，在传统环境中，硬件是有限的，并且可能，你知道，你必须处理一些进入系统的安全隧道，这会降低它的速度。因此，总的来说，您的速度会降低，这些环境的灵活性也会降低。比方说，客户调配新硬件的能力会大大降低，因为他们希望加快测试速度。

**Ashley:** 企业家令人敬畏的一点是，他们经常会拿着自己职业生涯中遇到的问题，也许是上一份工作中遇到的问题，说:“有更好的方法来解决这个问题。让我去创造一个产品，创造一个公司，去做吧，”因为这也是你故事的一部分。

在你的经历中，软件和测试本身是什么阻碍？有没有具体的问题，或者只是，必须有一个更好的捕鼠器，或者你是如何——你从那次经历中带来了什么来剥离和创造功能？

Cser: 这是一个很好的问题。这真的和疼痛有关，对吗？当某个特定的 bug 因为您的流程不在而在那个星期第三次倒退时，接到一个愤怒的客户的电话——这真的非常非常痛苦。这就是最初的起点。

我想说的第二点是，它有一点独特之处——我们谈到这一点，左移非常重要，因此您可以尽早开始测试。你被教导向右移动是非常重要的。测试生产环境真的很重要，因为现在发生了很多事情，应用程序在浏览器中进行实时编译，有很多实时依赖项、第三方和 API 等等。生产中可能会出现很多问题，这些问题实际上可能不是代码缺陷，他们可能不得不处理一些其他缺陷或其他依赖问题。

因此，这肯定是我正在大力推进的一个领域，我认为这是未来的发展方向，是双向的。我们在左移的同时，也在思考如何测试生产。

**阿什利:**有意思。你知道，你肯定会听到测试环境中有很多变化，但生产环境中没有那么多变化。你提到的应用程序，如果你愿意的话，是不是在生产环境中，在运行时，在浏览器中组合在一起。

对于测试和生产，还有其他类似的用例吗？这个我真的很好奇。

Cser: 哦，当然。我能想到的非常有趣的有很多，也有一些是最近正在发生的个性化。因此，我们看到客户也在努力实现这些新的营销能力，以及你向用户展示的这些体验。测试非常困难和具有挑战性，很难从生产环境中看到。你有正确的数据和正确的经验，如果你愿意，出现。

因此，这也为我们提供了在 Functionize 中创建特定产品和功能来解决该问题的机会。

阿什利:嗯。你知道，这似乎是一种边缘情况，也许今天我们会看到越来越多的这种情况，但更受事件驱动而不是传统事务驱动的无服务器应用可能也是一个很好的生产测试案例。

哦，我同意。所以，当然，这将是一个早期的，让我们称之为角落案例，拉什案例，但我认为，随着公司的成熟和这些技术变得更加主流，我们会看到越来越多的这种情况出现。

阿什利:嗯。嗯，这里有点不同的方向，一只小鸟告诉我，你们都在争取某种类型的人工智能机器学习奖——这是怎么回事？

Cser: 嗯，我们最近刚刚在旧金山被提名为爱琴奖候选人。因此，我们很高兴能成为其中的一员。显然，我们会出席并观察它的进展。我们很荣幸能在那里被提名。所以，看到一家公司因为我们所做的工作而得到认可是非常令人兴奋的。

阿什莉:太棒了。好吧，我祝你好运。此外，我知道在 Functionize 的合作伙伴关系上发生了一些事情—那里发生了什么？

是的，绝对的。我们有很多很大的吸引力，因此，我们将很快宣布，可能在本季度末或第四季度初，一个非常具有战略意义的合作伙伴，一个与 Functionize 合作的最大的全球服务创新者，我们将一起营销，这再次表明，我真的为这个团队感到骄傲，它展示了我们正在做的工作和营销正在做的工作，以提高对人工智能和机器学习的力量的认识，以及这将如何改变测试。

阿什利:嗯。因此，我们期待第四季度可能会发布一些公告。得留意这一点。太好了。

绝对的。

阿什莉:是的。所以，我会让你有点为难。如果你必须说出你学到的一些最佳实践，不仅是在 Functionize，而且是在自动化测试之前，你知道，DevOps，cloud world——如果你可以归结为两三个最佳实践，你会从哪里开始？你会告诉人们什么？

Cser: 我想说，找到合适的工具并构建合适的工具链绝对非常重要。第二，和其他地方一样，我想说你确实需要合适的人，因此，培训和了解如何应用这些工具是绝对重要的。

最后，我想说的是，您在该应用中的策略，显然，回到之前关于测试什么和如何测试的讨论，对您的成功至关重要。因此，很明显，工具是主要领域，当然教育也是我们非常关注的第二个领域。

阿什利:我很好奇*【相声】*——我也很好奇。你在测试技能的人身上观察或寻找什么样的东西，或者你在现有员工身上投资的培训和技能发展技能？你在寻找哪些东西？

**Cser:** 你能澄清一下问题吗？在我们招聘的技能组合中寻找— *【相声】*？

**Ashley:** 那么，你提到的第二个项目是你的员工在测试和雇佣这些人以及培训测试人员方面的能力和技能。对于 Functionize 的潜在客户或现有客户，你已经学会寻找哪些好的建议？

Cser: 是的，这是一个很好的问题。所以，我会说，你知道，很明显，就像任何招聘一样，你想雇佣那些非常积极的聪明人，所以我假设这是底线。

就技能组合而言，我认为我们肯定在寻找有丰富经验的专业人士，但我们也可以真正启用和帮助那些主要是手动的，或者说，现在技术含量低得多的人，并将他们带入自动化世界，真正为我们的客户群创造大量价值。因为我们看到许多客户在努力扩展和寻找合适的技术人才。所以，我会说，这绝对是能够将它传播给更广泛受众的关键点，但同时我认为，让技术用户参与到项目中来，我认为，仍然非常重要。

阿什莉:好的。非常好。嗯，正如这些播客经常发生的那样，我们已经没有时间了。Tamas，非常感谢你今天参加播客。

谢谢邀请我。很高兴来到这里。

阿什莉:我也很荣幸。感谢 Functionize 的创始人兼首席执行官 Tamas Cser 今天加入我们，当然，也感谢您，我们的听众加入我们。您已经听到了另一个 DevOps 聊天。我是 DevOps.com[的米奇·阿什利。祝你愉快。在外面要小心。](https://devops.com/)

— [米切尔·阿什利](https://devops.com/author/mitchellashley/)