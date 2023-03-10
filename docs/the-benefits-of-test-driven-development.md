# 测试驱动开发的好处

> 原文：<https://devops.com/the-benefits-of-test-driven-development/>

这听起来有点矛盾:在编码之前创建测试用例。在编写功能之前编写和使用测试用例的过程中，开发人员可以开发出更高质量的软件。这就是测试驱动开发(TDD)背后的概念，并且它是有效的。

## **TDD 快照**

TDD 至少从 1999 年就出现了，它是与极限编程相关的新兴测试优先开发方法的一部分。2003 年，美国软件开发人员 Kent Beck“重新发现”了 TDD，并将其作为一种创建简单设计和激发开发人员信心的方法。快进到今天的敏捷开发世界，TDD 是一个使用非常短的反馈循环的软件开发过程，在这个过程中，开发人员做以下事情:

1.  创建一个会立即失败的测试。
2.  编写必要的代码以尽快通过测试。
3.  使用创建的测试作为参考，重构第二步中编写的代码。

## **![](img/40a64b7487a03f13814849aa1da08193.png) TDD 好处**

那么，为什么老掉牙的软件开发方法在敏捷开发世界中会有切实的好处呢？因为用最简单的术语来说，TDD 是一种开发高可用性软件的方法。

遵循 TDD 过程，开发人员必须在实际编码之前关注测试用例。这意味着开发人员更多地考虑软件的使用和用户界面的设计来实现这一点。结果，开发人员对界面比对实现更感兴趣——这导致了更有用的软件。

采用 TDD 方法还有其他几个切实的好处，包括:

*   为代码质量创建一个简单快捷的度量标准。
*   允许快速可视化以确定代码库是否有任何功能问题。
*   编写了新代码的活功能文档。
*   允许代码的安全重构，无论是基于提高代码质量的尝试还是基于变更的需求。

最后一点值得花点时间细想。TDD 方法要求不断发展的代码库经常被清理，这样新的测试和代码就很容易引入。这通常意味着代码从它当前的位置移动到它在软件中更符合逻辑的位置。这有助于减少任何无关的代码重复，并加强对对象、类、模块等的严格控制。通过这种方式，软件的整体可维护性逐渐增加。

可读性和可维护性的提高将在软件的预期生命周期中带来巨大的收益。遵循 TDD 方法需要开发人员专注于编写更小的可测试代码单元。通过遵循 TDD 方法，这导致了更加模块化、灵活和可扩展的软件。

## TDD 适合哪里？

TDD 方法适用于新的绿地软件和遗留系统。对于一个必须处理现有遗留软件的开发团队来说，关键是从小处着手，从修复 bug 开始。一个好的实践是，对于每个报告的 bug，创建一个测试来解决被破坏的 bug，然后修复功能。经过几次迭代之后，开发团队创建了一个可重复的工作测试来解决 bug 修复。当将这种方法应用于新的软件应用程序时，要特别注意理解用于技术堆栈的测试工具。

例如，当在通常使用 [Jasmine 测试框架](https://jasmine.github.io/)进行单元测试的 Angular 应用程序中工作时，以及当使用 Angular CLI 进行创建时，单元测试是与代码模块一起创建的。使用 TDD 方法，该方法将:

1.  确定要用该组件创建的功能的一部分。
2.  针对这部分功能创建一个会立即失败的单元测试。
3.  运行测试运行程序以确认失败的测试(在每次保存源文件后让测试运行程序继续运行可能会有所帮助，这样可以加快过程)。
4.  在角度组件中编写代码，这将使书面测试通过。
5.  确认通过后，对 Angular 组件进行任何重构更改，使用测试作为指南，以确保代码重构不会破坏功能。

## **用代码覆盖率测量可测试性**

在提高代码的可测试性时，另一个重要的考虑是使用代码覆盖工具。代码覆盖率是一个度量标准，用来显示为其编写了单元测试的代码的百分比。Angular 应用使用 [伊斯坦布尔](https://github.com/istanbuljs) 通过应用计算代码覆盖率。在现有项目中运行一次代码覆盖率会产生以下输出:

伊斯坦布尔提供的输出给出了总体测试覆盖率和测试中需要改进的代码区域的度量。代码覆盖率在几个方面很有用:

*   提供了总体可测试性的概念，允许一个阈值来确保总体软件可测试性不会超过某个点。
*   识别代码库中测试不佳的区域，使它们成为重构的机会。

然而，尽管代码覆盖率听起来很有效，但重要的是要理解它只是一个度量标准。编写好的单元测试是一个遵循代码将做什么的问题，诸如此类的度量标准不应该驱动重要的决策。

## **使用 TDD 时的考虑事项**

需要注意的是，TDD 并不能解决所有问题。创建一个全面的测试策略需要许多不同类型的测试，包括验收测试。在 TDD 中，焦点是一次一个代码单元。一个复杂的软件应用程序可能有成千上万个代码单元及其相应的测试。这就是为什么在遵循 TDD 方法时，确保测试质量保持高水平是至关重要的。测试不能成为为了追求更多功能或便利而被绕过的东西。避免测试会产生测试创建成为开发人员障碍的风险。

例如，忽略失败的测试会使确定应用程序的实际状态变得困难。让所有参与工作的团队都接受 TDD 方法也很重要。在业务方面，买入尤其如此。必须花时间预先讨论 TDD 方法的本质和好处，并且相信使用 TDD 会改进最终的软件。否则，业务管理将编写测试视为对底线没有贡献的活动。

## **结论**

TDD 强调有效和可持续的测试方法的重要性。TDD 也直接有助于软件的整体质量。对于小型或大型系统开发来说，这是一个老生常谈的问题，在日常将新功能投入生产的过程中，这一点经常会被忽略。当认识到质量测试代码应该得到与质量生产代码同等的关注和资源，因为它们在开发中同样重要时，质量软件就建立起来了。

戴夫·法里内利