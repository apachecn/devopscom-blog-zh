# Gartner 给 Docker security 一个矛盾的大拇指

> 原文：<https://devops.com/gartner-gives-docker-security-ambivalent-thumbs/>

随着组织继续评估更广泛地使用容器化来实现持续部署，围绕广受欢迎的 Docker 的安全问题不断涌现。上周，Gartner 的一位分析师发表了一份报告，对 Docker 的安全性给予了积极的评价，但也提出了一些重大警告。

该报告由 Joerg Fritsch 撰写，检查了 Docker 的安全属性。根据 Fritsch 的说法，Docker 在资源隔离方面非常有效，并且在安全操作管理和配置治理方面已经与 Linux 操作系统和虚拟机管理程序不相上下。但是 Docker 容器的不足之处在于管理方面。

Fritsch 写道:“在安全管理和支持机密性、完整性和可用性的通用控制方面，他们令人失望。”他解释说，随着 Docker 完善其 libswarm 和 nsenter APIs，这种情况可能会有所改善。

就目前情况而言，Fritsch 建议不需要模拟虚拟专用系统的组织应该在 n center 上实现标准化，以便与正在运行的容器进行交互，并通过限制输入集来保护 n center。他还建议，在大规模工作时，组织应该选择一个管理资源和部署容器的框架，并考虑为 Docker/Swarm API 使用 SSL/TLS 包装器，以保证完整性和机密性。

与此同时，Fritsch 特别指出 Docker 容器缺乏端点保护平台和加密工具，并解释说这方面的前景“严峻”。

“传统的 EPP 和加密供应商尚未认识到容器是他们未来需要追求和保护的领域，”他说，并解释说，组织必须通过应用程序白名单、SELinux 或使用战略性 DevOps 工具链来自动化和保护他们的容器，本质上是使“容器成为自我评估的实体”，从而降低风险

随着 2015 年的进展，第三方供应商可能会更加关注 Docker，尤其是如果 Docker 的增长在 2014 年遵循相同的轨迹。仅从 6 月到 10 月，Docker 的下载量[就从 300 万增长到 2100 万](https://www.techrepublic.com/article/just-how-hot-is-docker/)。去年秋天，Docker 获得了 4000 万美元的额外资金，为未来的增长提供了风险支持，这是今年早些时候获得的上一轮 1500 万美元的融资。

然而，围绕 Docker 的安全问题已经开始像乌云一样聚集。事实上，对 Docker 的安全异议是 CoreOS 在 12 月初推出火箭集装箱化项目的一个重要原因。这一声明紧随 Docker Engine 1 . 3 . 2 版本的发布，该版本解决了许多可能通过恶意 Docker 文件、图像或注册表被利用的漏洞。它还增加了一个安全特性来验证容器中的图片。然而，到了 12 月底，安全专家开始质疑验证功能。

Flynn 的联合创始人 Jonathan Rudenberg 在[中写道:“Docker 关于下载的图像被“验证”的报告仅仅基于签名清单的存在，Docker 从未从清单中验证图像校验和，”这是对 Docker 图像下载过程](https://titanous.com/posts/docker-insecurity)的不安全性的一个长解释。“攻击者可以在签名清单旁边提供任何图像。这为许多严重的漏洞打开了大门。”