# 为移动应用程序创建单元测试的技巧

> 原文：<https://devops.com/tips-creating-unit-tests-mobile-apps/>

移动应用程序测试确保您的应用程序完美运行，没有任何冻结、错误或崩溃。有单元测试、自动测试、系统测试和验收测试，在本文中，我们将讨论移动应用的单元测试。

首先，我们来讨论一下一般情况下什么是单元测试。单元测试检查代码的某些部分是否正常工作。换句话说，它帮助我们产生更健壮和可维护的代码。每个小测试都致力于一个小特性。然而，所有这些都是相互联系的，所以你会得到一种链条。如果这个链条中的任何一个环节出了问题，整个链条也会出问题。

作为[移动应用测试](https://www.mobindustry.net/20-best-mobile-app-testing-tools-for-android-ios/)的一部分，单元测试可以在开发的任何阶段编写，甚至可以在开发之前编写(测试驱动开发，或 TDD，是 iOS 单元测试最佳实践之一)。对于这种开发，您让您的测试驱动开发过程。它们表明你做什么，你下一步应该做什么，结果应该是什么。测试控制设计。

因此，单元测试是完美运行代码的第一步。但是它也是软件质量保证的主要手段。在本文中，我们将解释如何在一个 iOS 示例上进行移动应用单元测试，并给你一个小的 [iOS 单元测试教程](https://www.raywenderlich.com/150073/ios-unit-testing-and-ui-testing-tutorial)。

## 我需要进行单元测试吗？

每个人都需要做单元测试吗？简短的回答是否定的。长的回答是它是一个非常好的工具，尽管它不是在所有情况下都是必要的。

在下列情况下，您不需要单元测试:

1.  你的应用程序很小很简单。如果你的应用很小，手动检查会更快，因为没有那么多逻辑需要检查。
2.  你不打算让你的[应用](https://en.wikipedia.org/wiki/App)长期工作，你只需要它来做演示。
3.  你是一个写出完美代码而没有任何错误的超人。

如果你不属于这些类别中的任何一个，那么单元测试就是你所需要的。起初，这种测试似乎太费时间了。时间不足被认为是与测试相关的最严重的问题之一，但实际上执行单元测试可以节省大量时间并提高开发速度。此外，它可以作为你的图书馆的一种文件。我们在 Mobindustry 花了 30%的开发时间在测试上。

单元测试有两个主要目的:

1.  通过确保我们的类/模块/组件在所有可能的输入下都像预期的那样工作来减少错误的数量。
2.  通过确保我们的新功能、错误修复或重构没有破坏任何现有功能来减少回归的数量。

## 单元测试是如何工作的？

如何创建 iOS 单元测试？Xcode 内置了对单元测试的支持，并作为一个 [iOS 单元测试框架](https://saucelabs.com/blog/top-5-ios-testing-frameworks)工作。您可以通过按 cmd+U 或通过菜单选择产品-&gt；来使用 Xcode。测试。xCode 将运行所有活跃的测试，并生成一份结果报告(通过/失败)。所有失败的断言都会被指出。代码覆盖率数据也是在这个框架中生成的，它允许您访问任何类，并检查哪些代码行被调用了以及它们被调用了多少次。

## 单元测试的类型

[iOS 的单元测试](https://developer.apple.com/library/content/documentation/DeveloperTools/Conceptual/testing_with_xcode/chapters/04-writing_tests.html)可以检查应用程序的 UI 或逻辑。逻辑 1 有几种亚型:

*   常规的用于检查简单的功能。

func testExample() {

let account = Account()

帐户.金额= 100.0

帐户.取款(20.0)

XCTAssert(account.amount == 80.0，"账户当前金额应为 80.0，但实际金额为

(账户.金额)"

}

这用于简单地检查 retract()方法是否正常工作。

*   异步测试使用 XCTestExpectation 来检查预期的结果。

func testExample() {

让 url = URL(字符串:"http://www.google.com")

假设期望= XCTestExpectation(描述:"期望 _ 描述")

let task = URL session . shared . data task(with:URL){(data，response，error) in

if let error = error {

XCTFail( "错误:(error.localizedDescription) "

返回

} else if let status code =(response as？HTTPURLResponse)？。状态代码{

if statusCode == 200 {

expectation.fulfill()

}否则{

XCTFail( "请求失败，状态码为(statusCode) ")

expectation.fulfill()

}

}

}

task.resume()

waitForExpectations(超时:10) {(错误)in

XCTFail( "期望(expectation.description)失败"

}

}

这将检查谷歌的网站是否可用(即，它是否返回状态代码 200)。

XCTestExpactation 用于等待异步任务完成。期望要么通过调用 fulfill()方法成功完成，要么在超时时间已过但尚未调用 fulfill()时失败。

*   衡量一个检查重逻辑:

func testExample() {

自我测量{

让 loto objects =[]

对于 lotOfObjects 中的对象{

obj.makeCalculations()

}

}

}

您可以创建这个测试来测量在 measure()块中的特定计算上花费了多少时间和多少资源。

## 移动应用单元测试技巧

*   ### Remember the structure

结构化的通用 AAA 方法是编写测试最常见和最方便的方法。AAA 代表:

1.  排列–分配所有必要对象并设置初始参数的部分
2.  act–执行逻辑的部分
3.  断言–检查获得的结果是否与预期结果相匹配的部分

以这种方式编写的 ode 易于阅读和使用，这意味着它更易于维护。

*   ### Use the test to cover only the necessary things

有些人认为有必要用单元测试覆盖代码的每一个部分。这种方法实际上既耗时又复杂，而且完全没有用。

您的项目中可能有四种类型的代码。让我们从最极端的选项开始看它们:

1.  没有任何依赖关系的简单代码:对于这种代码来说，可能一切都已经很清楚了，没有必要对它进行评估。
2.  **有很多依赖关系的复杂代码:**如果你有这种代码，重构是个好主意。没有必要覆盖这段代码，因为我们将重写它，这意味着新的类将会出现，方法签名将会改变。为什么要写不会用的东西？当然，这样的代码也需要质量评估，只是在更高的层面上。
3.  **没有依赖关系的复杂代码:**此代码包含算法或业务逻辑。这是用于测试的完美代码，因为它们是系统中非常重要的部分。
4.  具有依赖性的中等复杂代码:这种代码将不同的组件链接在一起。测试在这里非常重要；它们告诉我们组件必须如何交互。

通常，它们涵盖以下代码领域:

*   通用功能、核心模型、类及其交互
*   主 UI 工作流
*   关键逻辑
*   错误修复

单元测试不仅适用于这些领域。它们实际上可以用于测试几乎任何功能。

不要涵盖琐碎的功能和系统功能。

*   ### Test only one thing at a time

这个想法是将你的应用程序分成不同的独立模块，这些模块能够独立工作，而不与应用程序的其他部分交互。这允许您分别处理每个模块并简化代码。如果你同时检查几件事，你的代码迟早会变得过载和过于复杂。支持它和使用它将变得困难。

*   ### Name your test

    logically.

正确命名您的测试并将它们分配到项目的正确部分是非常重要的。许多项目都有测试，由于不方便的放置和命名，没有人运行。以下是关于逻辑结构的一些提示:

1.  在版本控制系统中选择一个逻辑位置:它们必须是版本控制的一部分。根据你的需要，它们可以有不同的组织方式，但是这里有一个共同的建议——如果你的应用是单一的，把它们都放在一个测试文件夹中；如果它有许多组件，将相关的测试存储在每个组件的文件夹中。

2.  选择命名约定:最好的方法之一是向您构建的每个项目中添加一个测试项目。

3.  使用与命名项目类相同的命名测试类的约定:如果您有一个类 ProblemResolver，那么添加一个名为 ProblemResolverTests 的类是一个好主意。每个班级应该只做一件事；否则，你的测试将很难管理。

*   ### Use imitation object

您可以使用不同的伪对象来简化测试过程。不需要分配和管理一个巨大的类或组件来使用其中的一个方法。这种伪对象可以分为两类:

*   存根
*   嘲弄

存根是返回预定响应的假方法。存根的主要用途是在与 API 交互时。这个想法不是等待实际的连接完成，而是立即返回预定义的数据或预定义的错误。

让我们假设我们有一个应用程序，你可以添加一个朋友关系。有一个 FriendListViewController 可以显示你所有朋友的列表。这个朋友列表可以从后端下载，所以有一个 ApiManager 类，它有这样一个方法:

API manager . shared . getlistofffriends(with completion:{(friends)in

let friendsListVC = friendlistviewcontroller . init(friends:friends)

//呈现 friendsListVC

}) {(错误)in

//显示错误

}

这个方法有一个完成处理程序，我们需要等待它完成。

但是我们实际上不需要等待，因为我们不需要任何 API 甚至互联网连接。我们需要确保 FriendListViewController 正常工作，我们所需要的只是一些朋友列表；他们来自哪里并不重要。因此，我们将引入一个 ApiManagerStubs 类，它将从实际的 ApiManager 复制方法，但不会执行任何实际的 API 请求。

对于这个特殊的测试，我们将编写一个获取朋友列表的方法:

func getlistofffriends()->[朋友] {

let friend1 = Friend.init(姓名:"鲍勃"，姓氏:"巴克"，年龄:34 岁)；

let friend2 = Friend.init(姓名:"约翰"，姓氏:"多伊"，年龄:30)；

return[朋友 1，朋友 2]；

}

之后，我们可以很容易地分配和测试 FriendListViewController。

func testExample() {

let friends = apimanagerstubs . shared..getListOfFriends()

let friendsListVC = friendlistviewcontroller . init(friends:friends)

//测试 friendsListVC.tableView

}

模拟是部分复制真实对象的假对象，允许您检查在某些事件之后是否调用了方法或设置了属性。

在上面的例子中，当一个朋友被删除时，我们需要清除这个朋友的聊天记录。我们有一些类似 ChatManager 的类来实现这个功能。但是同样，为此，我们不需要实际删除任何数据或调用任何 APIs 我们只需要检查相应的回调是否被触发。因此，我们将引入模拟对象 ChatManagerMock，它的行为类似于 ChatManager，只是它不删除数据，而是记住触发了哪些回调。

ChatsManagerMock 类{

var deleteFriendWasCalled = false

func clearchatshistoryforfriend(_ Friend:Friend){

deleteFriendWasCalled = true

}

}

现在我们可以如下实现我们的测试:

func testExample() {

let friends = apimanagerstubs . shared . getlistofffriends()

let friendsListVC = friendlistviewcontroller . init(friends:friends)

let mock = ChatsManagerMock()

friendslistvc . chats manager = mock

//触发列表中第一个朋友的删除操作

friendslistvc . deletefriendbuttonaction(无，索引:0)

XCTAssert(mock . deleteFriendWasCalled，" deleteFriendWasCalled 本应被调用")

}

## 结论

单元测试是一个非常强大的工具，可以帮助开发人员避免错误，并在错误出现时快速发现它们。他们帮助你维护你的代码，但同时他们也需要维护。许多项目的大问题是没有人使用的测试，为了避免它，你需要坚持一些规则。您的测试必须:

*   要靠谱；
*   不依赖于它们运行的环境；
*   易于维护；
*   易于阅读和理解(即使是初学者也必须能够理解正在发生的事情)；
*   有一个标准的命名约定；和
*   定期启动并实现自动化。

遵循这些基本规则将帮助你得到一个有效的系统。每次测试只检查一件事。你的测试将是类方法的规范；它将告诉所有关于他们期望的输入和其他系统组件期望的输出。像这样的系统很少。这种系统有一个实际的规范，通常没有太多的文本——只有基本功能、服务器方案和“入门”指南。这类项目的生命不再依赖于人；当系统被可靠地测试，并在它自己的测试的帮助下告诉所有关于它自己的事情时，开发人员可能来来去去。

## 关于作者/斯维特拉娜·切雷德尼申科

斯维特兰娜·切雷德尼申科是一位内容作家。目前，她是 Mobindustry 营销团队的一员。她是辩论运动的积极成员，并且是两次地区锦标赛的冠军。现在，她正在提高自己的平面设计技能，学习新的框架。她毕业于第聂伯彼得罗夫斯基国立大学。Svetlana 喜欢旅游、阅读科技新闻和玩电子游戏。在 [LinkedIn](https://linkedin.com/in/светлана-чередниченко-099530145) 上与她联系。