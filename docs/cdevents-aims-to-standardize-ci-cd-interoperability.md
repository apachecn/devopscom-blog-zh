# CDEvents 旨在标准化 CI/CD 互操作性

> 原文：<https://devops.com/cdevents-aims-to-standardize-ci-cd-interoperability/>

公司面临着不断发布新应用和新功能的巨大压力。随着软件开发生命周期变得更加迭代，持续集成和持续交付(CI/CD)已经成为实现更快速部署的必要因素。

许多开发团队现在都采用 DevOps，但是完全自动化从源代码到产品部署的 CI/CD 管道并不是一件容易的事情。首先，正在使用的工具数量继续膨胀，这意味着 CI/CD 构成了一个持续的维护障碍。此外， [CI/CD 工具](https://containerjournal.com/features/6-cncf-projects-for-ci-cd/)经常采用不同的格式来描述它们的事件。CI/CD 管道是事件驱动架构的一种形式，如果每个工具的输出不是标准化的格式，它可能需要大量特殊的“粘合剂”来将事件修补在一起。

有趣的是， [CDEvents](https://cdevents.dev/) ，一个来自[连续交付基金会](https://cd.foundation/) (CDF)的新兴开源标准，正致力于标准化 CI/CD 工具如何描述其事件有效负载的根语义，比 [CloudEvents](https://cloudevents.io/) 更精细。该项目旨在建立描述常见 CI/CD 事件的模式，简化集成并提供更多关于 CI/CD 管道的可操作数据。

我最近会见了 IBM 的开源开发者倡导者 Andrea Frittoli，以了解为什么存在 CDEvents 项目，它是如何工作的，以及他们希望实现什么。Frittoli 同时也是 CDEvents 项目的创建者和 CDF 技术监督委员会的成员，他认为 CDEvents 有潜力为庞大的 CI/CD 工具生态系统带来急需的互操作性。下面，我们将调查项目在哪里，并考虑它的方向。

## CI/CD 的问题

Frittoli 解释说，CDEvents 试图解决的核心问题是 CI/CD 领域缺乏互操作性。目前，DevOps 工程师必须定期在 CI/CD 工具之间进行点对点集成。“没有一个工具能让你完全从管理源代码到生产，”他说。他补充说，一个开发团队可能在一个管道中使用多达 15 个独特的组件，并且不同团队的工具偏好可能会有很大差异，这进一步使 CI/CD 互操作性变得复杂。

尽管 CloudEvents 作为描述事件数据的规范已经取得了进展，但是还没有专门用于描述 CI/CD 事件的规范。根据 Frittoli 的说法，CloudEvents 在这方面有所欠缺，因为它不知道有效载荷中插入了什么。

## 了解 CD 事件

CDEvents 是“连续交付事件的通用规范”。Frittoli 将其描述为公共事件的共享字典或共享语义。这些事件可能是源代码中的更改、运行测试或者代码执行或部署。CDEvents 使用 JSON 对象模式来描述事件类型，并且可以作为属性与 CloudEvents 一起工作。“CDEvents 不仅是信封的标准格式，也是有效载荷的标准格式，”Frittoli 说。

正如 Frittoli 解释的那样，CDF 特别兴趣小组仍在起草 CDEvent 规范的确切语义和通用名称。目前，CDEvent 将这些对象组织成四个主要桶:[核心事件](https://cdevents.dev/docs/core/)、[源代码版本控制](https://cdevents.dev/docs/source-code-version-control/)、 [CD 事件](https://cdevents.dev/docs/continuous-deployment-pipeline-events/)和 [CI 事件](https://cdevents.dev/docs/continuous-integration-pipeline-events/)。

虽然该小组仍在最终确定事件的格式，但下面的示例是最终格式的近似值:

```
"meta": {
  "version" : "draft",
  "event_id" : "A234-1234-1234",
  "source" : "/staging/tekton/",
  "type" : "dev.cdevents.taskrun.started",
  "timestamp" : "2018-04-05T17:31:00Z"
},
"subject": {
  "id": "/namespace/taskrun-123",
  "type": "taskrun",
  "content": {
    "URL": ...
    "pipelinerun": ...
  }
},
"extensions": [{
  "name": ,
  "content": ...}
],
"links": [{
...
}]
```

## CI/CD 活动标准化的好处

那么，为什么要定义 CI/CD 事件数据的格式呢？这对开发者和整个企业有什么好处？弗里托利看到了两个潜在的主要应用案例。首先，CDEvents 可以减少编写和维护常见 DevOps 工具(如 Spinnaker、Argo 或 Flux)之间的粘合代码的工作量。“这将使所有部分之间的整合更加顺畅，”弗里托利说。缓解这种情况有助于扩展 CI/CD 计划并提高整体敏捷性。

另一个积极的副作用是收集更多关于工作负载及其性能的详细信息。Frittoli 解释说，如果所有这些组件都生成类似格式的事件，那么您就可以开始创建整个 CI/CD 管道的真正的端到端可视化。然后，您可以开始衡量部署频率、故障率、变更时间和其他指标。

弗里托利说，如果事件开始使用共同语言，你可以用这些数据做许多有趣的事情。事件数据有助于确定事件的根本原因，并有助于调试。人们甚至可以预见一些 AIOps 的潜力，以进一步自动化操作并提高 CI/CD 的可观察性。

## 最终想法和参与方式

CDEvents 出现在迭代软件开发变得司空见惯的时候。大量有用的 CI/CD 工具可供我们使用，以支持利基业务。然而，这个空间仍然需要一种标准的方式在它们之间运作。CDEvents 是一个令人兴奋的前景，然而该项目仍处于早期阶段。它还没有达到完全发布或任何生产使用和概念验证仍在开发中。

当然，鼓励厂商中立的规范需要工具社区的参与。Frittoli 说:“不同的工具实现 CDEvents 对于它的成功是至关重要的。他鼓励工具社区加入工作组，合作构建概念验证。SIG 计划继续完成规范的第一版。与此同时，该小组使用 Tekton 和 keptn 制作了一个概念验证，该项目未来的目标是 Knative 和 Jenkins。

CDEvents 项目处于酝酿阶段，由 CDF 的事件特别兴趣小组(SIG)维护。要了解更多信息，您可以在这里阅读 [CDEvents 文档](https://cdevents.dev/docs/)或在这里参与[社区](https://cdevents.dev/community/)。Events SIG 还每两周举行一次会议，而 [CDEvents 社区峰会](https://events.linuxfoundation.org/cdcon/features/add-on-programming/)将是即将到来的 CDcon 的一部分。