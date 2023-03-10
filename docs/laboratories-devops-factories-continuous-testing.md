# 从实验室到 DevOps 工厂进行连续测试

> 原文：<https://devops.com/laboratories-devops-factories-continuous-testing/>

之前的博客[SDN 和 NFV 的持续测试和监控要点](www.devops.com/2015/10/28/continuous-test-monitoring-essentials-sdn-nfv)讨论了测试和监控复杂系统(如软件定义的网络和虚拟化的网络功能)的重要性和建议做法。无论被测试的产品是否是一个复杂的网络系统，有了 DevOps，实验室不再仅仅是工程师们测试他们的变化的地方。在根据最佳实践实施的 DevOps 环境中，实验室正在成为可靠、可用、可远程访问的在线操作，并可由期望 24/7/365 可用性的多种类型的远程用户共享。

The old “Santa’s workshop” model of development engineering (elves) hand-crafting products in specialized local laboratories and then handing off their products to operations staff (reindeer) for infrequent delivery (on Santa’s sleigh once per year) is being replaced by a fully automated, orchestrated software DevOps laboratory infrastructure akin to a modern factory staffed by robots churning out products at a dizzy pace. Elves and reindeer need to rest between deliveries and simply can’t keep up with today’s continuous delivery expectations. Santa’s “lap-top” has become an app store where users can download products anytime no matter if they have been bad or good (but be good for goodness sake!).

如果一个现代化的 DevOps 工厂风格的实验室是你的圣诞清单上的优先事项，这里有一些关于工具要求的建议，你可能想在给圣诞老人的信中包括。

1.  记录和跟踪资源的库存工具:在测试中使用的所有系统，例如测试工具、被测系统和互连系统，都需要在在线库存数据库中被跟踪，在该数据库中，每个资源和关键属性都是可见的，并且可由管理人员和资源的用户来寻址。发现和导入新的或变化的资源的能力是必不可少的。没有这些能力，就不可能跟上 DevOps 持续测试环境为满足持续需求而发展的持续变化。
2.  管理用户的工具:
    随着大量用户访问实验室资源，管理用户和用户组的特性是必不可少的。大规模开发运维环境需要根据项目优先级和时间表管理数百或数千个拥有不同资源访问权限的用户。实验室管理员向单个用户或用户组分配权限的能力对于控制对某些资源的访问是至关重要的，这些资源可能由于安全或其他原因而受到限制。
3.  创建和保存测试配置的能力:
    虽然可以创建测试来使用各种各样的配置，但是每个测试都假设了一些关于测试配置的东西。在根据最佳实践实现的测试环境中，测试配置或至少测试配置的抽象版本被指定并与每个测试相关联。配置数据保存在数据库中，当需要运行测试时，可以通过搜索属性匹配来调用。
4.  保留测试和测试配置的能力:
    在大规模开发运维环境中有大量实验室用户，而实验室资源有限的情况下，需要冲突解决功能。将实际资源分配给抽象配置的能力提供了更有效地使用实验室资源的灵活性。对于时间窗口有限的用户或时间表不确定的自动化流程来说，根据日历提前或在事件触发时立即预留测试资源和测试配置的能力是最大限度减少时间浪费的重要选项。

5.  并行编排许多自动化测试的能力:
    在大规模的 DevOps 环境中，需要在给定的短 DevOps 周期中运行的测试数量可能从几个到几千个不等，这取决于周期中集成的变更的复杂性和性质。工具需要能够扩展测试，并在尽可能多的可用物理和虚拟测试资源上运行，以最小化测试的总时间。

6.  测试环境度量:
    整个 DevOps 管道依赖于可靠的、可伸缩的和可维护的持续测试。内置指标对于监控环境的可靠性、可扩展性和可维护性至关重要。

以上是对最先进的 DevOps 连续测试实验室“工厂”列表的部分建议。在思必驰，我们认为持续的测试实验室“工厂”对于成功的开发至关重要。

你可以在[Spirent.com/solutions/LabManagement](http://www.spirent.com/Solutions/LabManagement)了解更多我们的观点

你对这些建议有什么看法，你还有其他应该提到的建议吗？

同时，我们祝愿圣诞老人、小精灵和鲁道夫、驯鹿朋友和你节日快乐，新年快乐！

![Santa's Workshop](img/87737183e8f806c070bb43e9209a7ca3.png)