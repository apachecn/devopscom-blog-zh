# 开发运维与安全性:准备好保护您的应用

> 原文：<https://devops.com/devops-and-security-be-ready-to-shield-your-application/>

我们都听说过持续改进/持续交付(CI/CD)。实施 CI/CD 有许多好处，因为它有助于开发和部署流程的端到端无缝集成。CI/CD 有助于快速改进、缩短发布周期等，但它也有助于以 DevOps 的速度有效处理安全性的挑战。

## **用于固定 DevOps 的工具**

市场上有成千上万的 DevOps 安全工具可以帮助我们 HCL Technologies 在 CI/CD 管道的各个阶段保护我们的软件开发。每天都有新的漏洞出现，因此我们必须保持警惕，确保我们的应用程序安全并为未来做好准备。

这些是我们使用的 DevOps 安全工具(大多数工具都是开源的，带有企业版选项):

1.  OWASP SonarQube
2.  OWASP ZAP
3.  OWASP 相关性检查
4.  OWASP 胶水
5.  锚
6.  克莱尔-韩文
7.  凹
8.  赛博方舟魔法

## **我们的 DevOps 工具链图**

![](img/4125a3376345f8df00843d82940abf29.png)

## **保护 CI/CD**

让我们考虑一个作业，其中我们通过自动提交从 GitLab/GitHub 签出代码(一旦开发人员对代码进行任何更改，就会触发 Jenkins 作业)。你可以参考[这个链接](https://medium.com/@teeks99/continuous-integration-with-jenkins-and-gitlab-fa770c62e88a)了解更多关于 Jenkins GitLab automation 的信息。

![](img/d54dffbe86dcbc44494fc10fa8555a7b.png)

现在，在 Jenkins 中，我们可以运行安全测试，并以报告和仪表板的形式呈现它，以满足我们的需求。首先，我们可以使用 OWASP SonarQube 进行静态分析。OWASP SonarQube 包括已发现的 bug、PMD 和几个现成的安全插件。接下来，对于动态分析和渗透测试，我们可以使用 OWASP ZAP，它以 XML/HTML 格式呈现报告，可用于创建吉拉问题。

![](img/2e7ad6d9bfbc993fcd0f2f9b62dd875a.png)

![](img/a8c4014ee3e1aedf0cadf33ca4ee26d2.png)

![](img/9bacf2b82ee8b11d725fbbdb0ed57970.png)

![](img/350fb53523b7ef9c701f50bc836889a8.png)

在上面的场景中，我们也可以通过自定义工具集成来使用 [ZAP。在我们的例子中，我们在本地机器上安装了 ZAP。我们也可以使用安装在远程机器上的 OWASP ZAP。](https://medium.com/@we45/a-step-by-step-guide-to-integrate-zap-with-jenkins-96ef4a7c2f64)

## **远程 OWASP ZAP 连接步骤**

![](img/8a47fe7c9a52b995adf2d84d9ff21359.png)

![](img/c637115903ab06f26b143182c55383c4.png)

![](img/8580aa86f12aedec580d0a6a46700553.png)

Windows 命令:C:Program files OWA spzed Attack Proxy > zap . bat-config API . disable key = true-config API . addrs . addr . name =。*-config API . addrs . addr . regex = true

Linux 命令:Zed Attack Proxy > zap . sh-config API . disable key = true-config API . addrs . addr . name =。*-config API . addrs . addr . regex = true

## **Jenkins 中的 OWASP 配置**

![](img/f11e9389dcacf31c4f617eebeca2ea1f.png)

![](img/416cf255edd09657111eff14d175538e.png)

![](img/82473a081a00932310682ebcb3e921be.png)

![](img/0afb4c467605bbaca3fc9edef204e8ee.png)

报告将在中生成。xml 和。html 格式。现在，根据 ZAP 生成的报告，我们开发了一个 Java 程序，为检测到的每个漏洞创建吉拉问题，并将其分配给相关人员。

![](img/cc2602d10428719e92415f511658ac2e.png)

接下来，我们对项目进行 OWASP 依赖检查分析。要为 Jenkins 配置，请执行以下步骤:

首先，我们需要 OWASP 依赖检查插件(我已经安装了)。此过程可能需要几分钟，因为它是从 NVD 服务器下载的。

以下是接下来的步骤:

![](img/55eb55bff03fe853fa168d365d4073a7.png)

![](img/fd546a2dc80c1958672b61af2ebac77b.png)

![](img/dfe27fa9e41e02794383a91ecf9ebadc.png)

或者，我们可以使用 OWASP Glue 插件，它运行 OWASP ZAP、OWASP 依赖性检查和其他安全自动化测试。

![](img/f4f99d0ced211610e1ee95b612cee21a.png)

我们还在项目中使用 FOSSA 进行许可证审计和操作系统依赖性的漏洞管理。我们可以在内部使用 FOSSA，但是它只能在 Ubuntu 机器上使用。

![](img/5c95f343d00d3c5b064b788a3308cf53.png)

![](img/53db61f29a3e7619bfd7da96aaba6a6d.png)

![](img/e9b04fe1162a0092700f2f566431697c.png)

在 HCL，我们目前正与 Anchore 和 Clair-CoreOS 合作开发集装箱安全产品。我们还将身份访问管理(IAM)集成到我们的 CI/CD 工作中。至于 IAM，我们正在开发赛博方舟和哈希公司的金库。

## **赛博方舟变戏法**

![](img/0b08480c176865dcb26fda6f2f40c4ab.png)

魔术师 Jenkins 凭证插件:

![](img/6341863fa4c3e82c29c6465eb4ff16ad.png)

![](img/682313eb8c3f795fe8b72853b4ad9eaa.png)

![](img/2697cbac66831d9cf73a55e49be22b54.png)

## **哈希公司金库**

![](img/97a270fc817059529ff301a0b37f0dac.png)

![](img/6b90ffb706200aad18a0d9295c994fc5.png)

![](img/47156fd07320c80c0c2b583ef451589f.png)

## **结论**

我使用 DevOps 开发过各种安全工具。下面是可用于应用程序安全性的工具的快速比较。

![](img/5b1234fddb4983c32cec4aa9e26b15d2.png)

![](img/d1407a24b6f6b265a57d923433559de8.png)

既然您已经有了使用哪些工具的想法，那么就拥抱安全性，而不是担心它。DevSecOps 可以帮助改善和提高任何组织的成果和效率。

— [德巴尔基亚·潘迪特](https://devops.com/author/debarghya-pandit/)