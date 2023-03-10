# Chef 扩大了合规自动化的范围

> 原文：<https://devops.com/chef-extends-scope-of-compliance-automation/>

Chef 通过添加插件架构扩展了其 InSpec 合规性自动化框架的范围，插件架构[使开发人员更容易以编程方式生成可应用于自动化框架的合规性控制](https://www.businesswire.com/news/home/20181016005211/en/InSpec-Chef-3.0-Accelerates-Compliance-Automation-DevSecOps)。HashiCorp 开发的 Terraform 配置管理框架是第一个通过插件架构支持的框架。InSpec 以前是与开源 Ansible automation framework 集成在一起的。

Chef 的产品营销总监朱利安·邓恩(Julian Dunn)表示，插件架构支持多种通信协议，以将其扩展到 Chef IT 自动化框架之外的多个框架。

除了稳定的应用程序编程接口(API)之外，InSpec 3.0 还使描述可以测试的新资源变得更加容易，该接口使 DevOps 团队能够修改如何进行测试。对概要文件打包机制的改进也将使开发人员更容易地迭代 InSpec 带有依赖项的概要文件。

最后，InSpec 3.0 添加了一个基于关键值的描述界面，以支持更细粒度的报告以及满足一个或多个法规遵从性制度的重复数据消除控制。这允许组织创建他们自己的自定义元数据类别。

![](img/2f36c115752d96c5fcf74f183a025863.png)
总的来说，Dunn 注意到，由于 DevOps 的兴起，应用程序开发和部署的速度超过了那些负责合规性的人的能力。邓恩说，因此，合规责任需要与网络安全的其他方面一起向左转移。

邓恩承认，就实现这种转变而言，现在仍为时尚早。但是，随着越来越多的组织发现应用程序的部署速度受到法规遵从性审核的阻碍，开发人员就越有动力以编程方式将适当的控件插入到他们的应用程序中。Dunn 说，一旦这些控制到位，InSpec 就会生成人类可读的代码，用于减少在生产环境中部署应用程序之前和之后通过审核所需的时间。

当然，通过合规性审核并不意味着应用程序是安全的。但是它至少提供了使应用程序名义上安全所需的基线。事实上，对任何向拥抱 DevSecOps 转变的阻力最小的路径可能是将法规遵循控制放置到位的过程自动化。

虽然有数百项法规要求不同级别的法规遵从性，但事实证明大多数法规都要求实施相同类型的控制。一旦组织开始以编程方式将这些控件嵌入到他们的应用程序中，这些应用程序被认证为符合多项法规的速度应该会提高。当控制可以被自动集成时，开发人员就没有理由为了满足应用程序开发的最后期限而跳过遵从性控制。

这并不意味着具有风险管理背景的人将很快参与开发运维流程。但这意味着 DevOps 团队的输出不会堆积起来等待通过合规性审查，因为它前面的所有应用程序都缺少这样或那样的关键控制。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)