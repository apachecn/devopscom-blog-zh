# 发现和搜索。JSON

> 原文：<https://devops.com/api-discovery-and-search-with-apis-json/>

如果这听起来有点像 UDDI(他讲述了 WSDL 的发现和搜索)，那么你就对了。

Glue 就在本周，在会议之前是 2015 年 API 战略和实践技术联合国研讨会。其中一个闪电般的演讲(让我告诉你，他们快如闪电)是关于 API 的。JSON——Kin Lane、 [API 布道者](http://www.apievangelist.com/)和 [3scale networks](https://www.3scale.net/) 的 Steven Willmott 和 Nicolas Grenie 之间相对较新的合作成果，

这项工作——你可以在 apisjson.org 深入研究——是试图为“自动化软件代理(机器人)的公共部署和消费”提供一个更正式和标准化的 API 定义。简而言之，自动化代理(如果你喜欢阅读机器可消费的元数据，也包括人)可以访问一个已知(标准化)URI 的组织可用的 API 的元描述，比如 http://company.com/apis.json 的[。](http://company.com/apis.json)

这并不完全是 JSON 的 WSDL，因为元数据并没有描述实际的接口，而更像是曾经(现在可能仍然)托管在注册中心(存储库)中的 UDDI 条目。当前版本提供了关于 API 的基本信息，包括基本属性，如名称、描述和 URL，还可以包含更多(有些人可能会说是可用的)信息，如文档链接或实际的、现实生活中可读的 API 定义，如 Swagger 或 API 蓝图格式以及 WADL 和 WSDL。

这种努力在一个开放的 API 搜索引擎( [http://apis.io](http://apis.io) )中得到了展示，该引擎允许个人根据各种标准来寻找 API(今天列出了 900 多个)，当然所有这些都是从 API 中的元数据派生出来的。JSON 文件。

这些和 DevOps 有什么关系？正如史蒂夫·威尔莫特在他的闪电演讲中指出的，APIs。JSON 不仅仅是以一种可消费的格式描述 API，而是能够让机器发现和引导 API。这意味着潜在地能够触发和通知关于 API 的变化，以启动新的构建和部署过程。

这是一个很好的例子，说明了当一切都像代码一样对待，自动化从简单的任务转移到工作流，再到流程编排时，开发人员和运营人员之间的协作可能性。

我可能不需要提到(但我会提到，因为我),相同的触发和信号流程可以(并且可能会)挂钩到更广泛的网络基础设施(表现出高应用亲和性的组件，如负载平衡和缓存以及应用安全性)来驱动更自动化的变更管理。

API。JSON 不是第一个(也不会是最后一个)这种努力，因为未来的移动和应用经济是建立在 API 之上的，因此，正如 Steve Willmott 在他的演讲中所说，“API 的网络是网络的未来。”