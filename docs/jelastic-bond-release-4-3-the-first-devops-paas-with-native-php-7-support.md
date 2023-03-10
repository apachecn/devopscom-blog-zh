# je lastic Bond Release 4.3–第一个具有原生 PHP 7 支持的 DevOps PaaS

> 原文：<https://devops.com/jelastic-bond-release-4-3-the-first-devops-paas-with-native-php-7-support/>

*Jelastic DevOps PaaS 发布了一个新版本，原生支持 PHP 7，为客户提供更高的性能*

加州帕洛阿尔托(PRWEB)2016 年 1 月 13 日

Jelastic，Inc .是一家提供 DevOps PaaS 来管理认证容器(Java、PHP、Ruby、Node.js、Python 和。NET)和使用定制 Docker 容器的能力，今天推出了新的 4.3 版本。这个版本的名字是 Bond，Jelastic Bond，这是对 PHP 7 或 007 支持的恰当命名。

“PHP 团队和社区在大幅提高性能方面做了大量工作。我们很高兴成为云计算市场中 PHP 7 的早期采用者，因为它为从以前版本的 PHP 迁移提供了一个低门槛。众所周知，开发人员喜欢新功能，简单的入门点会让他们更快地采用新功能。”

“让人们从不受支持的旧版本 PHP 升级对我们来说一直是个问题。PHP 之父拉斯马斯·勒德尔夫说:“很高兴看到 Jelastic 让客户在这方面变得更加主动，结合这个版本的改进性能和新功能，我认为 Jelastic 的客户应该对此感到兴奋。”

早在 6 月份，PHP 7 Beta 就已经作为 Docker 容器提供给 Jelastic 客户[，现在，经过与社区的全面测试，我们已经为认证容器添加了对最新 PHP 版本的原生支持。基于名为 PHPNG (PHP 下一代)的重构 Zend 引擎，与传统版本相比，它显示了显著的容量提升。这使得你的 PHP 应用程序的性能提高了 2 倍，只需要升级运行它的服务器引擎版本。](http://blog.jelastic.com/2015/06/18/help-rasmus-lerdorf-polish-php-7/)

“性能和稳定性是 Layershift 客户的关键，因此我非常高兴能够在我们的平台上提供最新的稳定 PHP 7 版本，使用完全认证的 Jelastic 容器。PHP 7 中的性能改进令人难以置信，但因为 Jelastic 独特地按资源消耗而不是按实例大小收费，PHP 7 更低的资源使用率也节省了我们客户的资金！”Layershift 的服务总监达米安·兰塞姆(Damien Ransome)说。

我们非常重视语言语法的增强，也就是说，删除了以前版本中不推荐使用的功能，同时提高了语言的一致性。关于新特性和向后不兼容问题的详细信息可以在从 PHP 5.6.x 迁移到 PHP 7.0.x 的官方文档中查看。

“我们很高兴 Jelastic 现在可以提供 PHP 7 支持。我们的许多用户，主要是 WordPress 和 Drupal 应用程序的用户，现在可以升级到这个强大的版本，以获得更高的性能，使他们的应用程序速度提高一倍。

由于面向 PHP，这个 Jelastic 版本还带来了一些与这种编程语言相关的额外改进，例如:

*   PHP 更新的 MongoDB 驱动程序

为了使用 MongoDB 数据库，PHP 需要一个特殊的低级驱动程序，这个驱动程序是最近更新的。因此，在当前的 4.3 Jelastic 版本中，新的 [mongodb.so](https://docs.jelastic.com/connection-to-mongodb-for-php#module) 模块被添加到扩展池中，默认情况下为 PHP 应用服务器提供。

*   PHP 模块列表重构

Jelastic PaaS 提供了最受欢迎的现成 PHP 模块,无需任何代码更改即可启动大多数应用程序。目前，所有新创建的 PHP 应用服务器容器将只启动默认启用的几个最常用的模块，以实现更低的默认资源消耗和更灵活的扩展可配置性。其余模块[可以通过几个简单的步骤手动启用](https://docs.jelastic.com/php-extensions#activate)。

*   通过 CLI 进行外部 IPs 交换

在当前的平台更新中，[je elastic CLI](https://docs.jelastic.com/cli)的功能补充了一种新方法，允许在两个节点之间交换外部 IP 地址或将地址转移到另一个实例。这可以让 PHP 和其他应用程序在不停机的情况下更新到新版本。

“对于我们和我们的客户来说，Jelastic 4.3 版本最值得期待的特性无疑是对 PHP 7 的支持。在这个引擎版本发布后，我们已经收到了很多将它添加到平台的请求。因此，我们没有让客户等太久，因为所提供技术的灵活性是 Jelastic PaaS 的主要优势之一，”MyCloud.by 的副总监 Evgeniy Kozhuhovskiy 说道

关于 Jelastic

Jelastic 是一款面向部署在裸机硬件或任何云 IaaS 上的容器的企业开发平台即服务。Jelastic 的客户和合作伙伴，如 ISV、托管服务提供商、系统集成商、外包公司、DevOps 团队和企业，可以在公共云、私有云、混合云和多云选项之间进行选择。该平台为 Java、PHP、Ruby、Node.js、Python 和。NET 和使用定制 Docker 容器的能力。Jelastic 提供灵活的部署模式，无需对专有 API 进行编码，为无状态和有状态应用程序、协作、访问控制、监控、备份和灾难恢复、内置计费和业务分析工具提供灵活的自动扩展，同时通过高密度和硬件利用率降低总拥有成本。Jelastic multi-cloud 功能使客户能够通过跨不同数据中心或云的地理分布实现高可用性，借助实时环境迁移轻松地将项目重新定位到高级硬件，在更高质量或更经济实惠的硬件之间进行选择，并通过值得信赖的云供应商托管应用程序。欲了解更多信息，请访问我们的网站[http://www.jelastic.com](https://jelastic.com/)

有关 PRWeb 上的原始版本，请访问:[http://www.prweb.com/releases/2016/01/prweb13162913.htm](http://www.prweb.com/releases/2016/01/prweb13162913.htm)