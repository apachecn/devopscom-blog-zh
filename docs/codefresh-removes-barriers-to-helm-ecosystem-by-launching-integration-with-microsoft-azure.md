# Codefresh 通过启动与微软 Azure 的集成，消除了 Helm 生态系统的障碍

> 原文：<https://devops.com/codefresh-removes-barriers-to-helm-ecosystem-by-launching-integration-with-microsoft-azure/>

Codefresh 揭示并简化了 Helm 的真正设计目的

**加利福尼亚州山景城，2018 年 11 月 13 日** — [Codefresh](http://www.codefresh.io) 今天宣布与微软 Azure 托管的 Helm 仓库集成，这是通过消除 Helm 生态系统的障碍，使团队采用 Helm 变得极其高效的重要一步。

随着 Helm 生态系统的发展，Codefresh 在微软的带领下，通过易于使用的 Codefresh GUI 更容易地构建、测试和部署 Helm Charts，并将它们存储在 Azure 容器注册表中。这对于使用 Kubernetes 的团队来说很有价值，因为用户可以将他们引用的图表和图像打包到 Kubernetes 应用程序中。

*code fresh 与 Azure 的集成提供:*

*   使用 Azure 登录以向 Codefresh 添加存储库；不需要额外的身份验证配置
*   从 Codefresh 消费和推送图表
*   管理所有连接的 Kubernetes 集群中的图表部署
*   使用 [Azure Container Registry 地理复制](https://aka.ms/acr/geo-replication)跨多个地区地理复制图表

Codefresh 的首席技术布道者丹·加菲尔德(Dan Garfield)说，“Codefresh 公开了 Helm 真正设计的模式，并使之变得更加简单，这种模式就是制作你的应用程序，打包它，存储它，然后消费它。这样，您就拥有了内置的灾难恢复功能，因为您可以随时回滚。”

作为第一个 Kubernetes-native 持续集成/持续交付(CI/CD)平台，Codefresh 帮助开发人员即时构建、测试和部署到 Kubernetes，并收集对应用程序的反馈，从而将开发速度提高了 24 倍。

Helm 孵化器 Cloud Native Computing Foundation(CNCF)的执行董事 Dan Kohn 表示:“随着 CNCF 专注于在云原生生态系统中促进创新，我们很高兴看到 Codefresh 和 Microsoft Azure 这样的成员致力于支持这样一个快速发展的社区的需求。

Rishidot Research 分析师兼云计算和开源专家 Krishnan Subramanian 补充道:“通过提供托管的 Helm 存储库，Codefresh 帮助 Helm 实现了软件包管理器的高预期市场期望，这是微服务大规模采用的关键组成部分。Codefresh 和微软的这一收购使 Helm 合法化，这意味着更多的企业将充分利用 Kubernetes 所提供的一切，以加快开发速度、提高安全性、轻松更新和管理应用程序，并最终缩短上市时间。”

“Helm Chart 存储库是 Azure Container Registry 的一个自然而明显的补充，因为我们看到越来越多的客户进入生产环境，需要一种方法来部署一组图像和配置。能够使用通用身份认证将舵图与其参考图像一起进行地理复制简化了海图部署。我们继续对 Codefresh 为容器本地开发带来的关注和经验，以及富有创造力和以客户为中心的团队印象深刻。

关于 Azure Helm 库整合的细节可以在 Codefresh 的新博客中找到，*[code fresh 为 Azure Helm 库](http://email.prnewswire.com/wf/click?upn=-2FmEiX4LzXW0kRprnsN-2BZVNyurxNx0Ivz4K0EgVDzZL45XDfU-2FAr5lGNJxKbLSYpS4-2BGfRfAwz8xsG8FzKn8vBIBKfIqsZNCTelrQLN6YZf3-2FBCNZ9QsX6rbl-2BDuDUC5rVFSF-2BQ-2Ft0XFkDZtg1EhMV1brYtbJlKnyA72nGq90gVt7GPoksg995giHUPlIyn6oNBh-2FOnHBNGw8gEnEDThepNNZfy-2BlvSoq-2BUAv67vpN-2FtMH86kdAjGyOZsv5G-2BshKZ_6OJ6tZJNEVMlWmWhOfe70QCeXOiuzuhL0z58as4Z2ospvLNydlzJmitIJdga1No0OoTDqyjyphs8Z11Oa2miPAS4SQzpFofeV8PumF4rOQcD8a8PNWehZD1GTSuTOn5miNDZDUrNodWRszXARCgj67y3qv5pTLXgMBlA97ybCyhRnGVOLtWva0Ck-2FOEsG4-2FMDkigLABR8KJbyKvQb0fYoArPXXQZ6DbKH1z4u-2B5sijeC9kUSkkEhq-2Fr-2FzY-2BSk8np0e9K6w9X5zRogcE0ktQjED7SDxNdPpJgVq8QlbX8Zbn9UqdTBvwH-2FWqy1xcx1srX)* 。”此外，Codefresh 将于太平洋时间 11 月 28 日星期三上午 10:00 举办一场网络研讨会，由微软 Azure 的 Lasker 和 Codefresh 的 Garfield 主办的 *[更新 Kubernetes With Helm Charts: Build，Test，Deploy With code fresh and Azure](http://email.prnewswire.com/wf/click?upn=-2FmEiX4LzXW0kRprnsN-2BZVNyurxNx0Ivz4K0EgVDzZL45XDfU-2FAr5lGNJxKbLSYpS4-2BGfRfAwz8xsG8FzKn8vBIBKfIqsZNCTelrQLN6YZf3-2FBCNZ9QsX6rbl-2BDuDUC5rVFSF-2BQ-2Ft0XFkDZtg1EhMV1brYtbJlKnyA72nGq90gVt7GPoksg995giHUPlIyn6oNBh-2FOnHBNGw8gEnEDThepPJV5uWLUnFV73BA7E-2B0FT0T5d6flQIgpboBpPmlV1EF_6OJ6tZJNEVMlWmWhOfe70QCeXOiuzuhL0z58as4Z2ospvLNydlzJmitIJdga1No0OoTDqyjyphs8Z11Oa2miPAS4SQzpFofeV8PumF4rOQcD8a8PNWehZD1GTSuTOn5miNDZDUrNodWRszXARCgj69NnNZipPlSvlr2LN9qaHXQTcMaYIBk0R0ACSLO-2BbX5qEu6YJ7zU8i2rwdNOZvROzvFLARemfPGPN4UW54caTCs3FOq3rP3c5jU4cTsatMVKkEhH811UK25ds-2FTqnP8MWuUVbxAT6ZUn8z2SXQlHs4SIOoc3h6Bt1OMFh0lGX92X)*。

**关于 Codefresh，Inc .** code fresh 成立于 2014 年，是第一家 Kubernetes-native CI/CD。2017 年 GA 之后，Codefresh 已经收获了超过 2 万的用户。与传统解决方案不同，Codefresh 管道专为 Kubernetes 和 Helm 等云原生技术而设计。Codefresh 总部位于加州山景城，由世界级投资者支持:M12、微软的风险基金、Viola Ventures、Hillsven、CEIIF、UpWest Labs 和 Streamlined Ventures。在 https://codefresh.io/[了解更多 Codefresh。在 LinkedIn 和 Twitter 上关注@codefresh。](https://codefresh.io/)