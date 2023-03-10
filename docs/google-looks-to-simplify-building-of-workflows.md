# 谷歌寻求简化工作流程的构建

> 原文：<https://devops.com/google-looks-to-simplify-building-of-workflows/>

谷歌本周推出了 [Cloud Composer](https://cloud.google.com/blog/big-data/2018/05/cloud-composer-is-now-in-beta-build-and-run-practical-workflows-with-minimal-effort) 的测试版，这是一个托管的 Apache Airflow 服务，用于构建工作流，有望简化集成 DevOps 流程的管理。Apache Airflow 是在 Apache Software Foundation 的支持下开发的孵化项目，它使 IT 团队能够使用有向无环图(Dag)以编程方式创作、调度和监控工作流，这些有向无环图可以可视化生产中运行的管道，监控其进度，并可用于解决问题。

谷歌云的产品经理詹姆斯·马龙(James Malone)表示，Cloud Composer 利用 Apache Airflow 不仅可以简化工作流的管理，还可以在各种公共云和私有云之间移植工作流，包括内部 it 环境。

Cloud Composer 还包括 Google 开发人员控制台和云软件开发工具包(SDK)，云身份感知代理，Stackdriver 日志记录和监控，身份访问管理(IAM)和 Python 支持，以及简化的 DAG 管理和简化的气流运行时。

Malone 说，谷歌计划随着时间的推移，在其他谷歌云区域增加对自动缩放和可用性的支持，并将 Google Composer 与 Kubernetes 集成，以将 Apache 气流工作流的范围扩展到容器。

Cloud Composer 的定价基于消耗，以 vCPU/小时、GB/月和传输的 GB/月来衡量。

Malone 表示，Cloud Composer 将在支持 DevOps 团队构建跨越混合云计算环境的管道方面发挥关键作用。如今，IT 管理员经常使用他们编写的文本编辑器或脚本来自动化流程。但是这些脚本很难在多个 it 管理员之间共享。Cloud Composer 和 Apache Airflow 使得跨开发运维团队共享自动化流程的工作流变得更加容易。同样重要的是，那些不具备开发脚本所需编程技能的 IT 管理员也可以访问这些工作流。

Malone 补充说，这些工作流还将在围绕一套通用的持续集成/持续部署(CI/CD)流程统一开发运维流程和数据运维流程方面发挥关键作用。

如今，大多数组织都在独立管理多个云。但是，随着组织希望更快地构建应用程序，他们希望能够在最佳平台上部署这些应用程序，而不必为每个云环境开发一套独特的管道。将应用程序锁定在特定的云平台上不仅在经济上不可接受，从应用程序开发和部署的角度来看，这也是非常低效的。

阿帕奇气流不是唯一可以用来建造管道的工具。但 Malone 指出，因为这是一个开源的 Apache 项目，所以组织可以放心，他们开发的工作流现在和将来都可以在任何地方运行。他说，谷歌选择 Apache Airflow 来构建 Cloud Composer 很大程度上是因为围绕这个开源项目正在出现一个活跃的开发社区。

IT 平台的管理方式正在迅速转变。孤立管理服务器和应用程序的时代已经过去。IT 管理员需要管理运行比以往更多应用程序的服务器和存储系统。令人欣慰的是，实现这一目标所需的工具现在对 IT 部门的每个人来说都变得更加容易获得。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)