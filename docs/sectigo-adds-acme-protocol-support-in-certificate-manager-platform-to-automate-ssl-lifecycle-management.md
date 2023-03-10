# Sectigo 在证书管理器平台中添加了 ACME 协议支持，以实现 SSL 生命周期管理的自动化

> 原文：<https://devops.com/sectigo-adds-acme-protocol-support-in-certificate-manager-platform-to-automate-ssl-lifecycle-management/>

*限制人为错误和网站中断，同时支持企业配置自动化工作流程*

**新泽西州 ROSELAND–2019 年 4 月 4 日**–尽管企业越来越多地使用现代、灵活的计算环境，包括虚拟化、集装箱化、物联网(IoT)和云，但大量 IT 管理员仍在继续使用老式技术来部署和管理证书，这些技术更适合 90 年代的基础设施，而不是今天的 DevOps 环境。这种“通过电子表格进行管理”会带来效率低下、停机风险或因人为错误导致的不合规风险。

为了解决这个问题，全球最大的商业认证机构和网络安全解决方案的领导者 [Sectigo](https://sectigo.com/) (前身为 Comodo CA)今天宣布在其广受欢迎的[Sectigo Certificate Manager](https://sectigo.com/products/management-solutions/sectigo-certificate-manager)平台中支持 ACME 协议。通过添加 ACME 支持，Sectigo 为企业证书管理带来了自动化的可靠性和效率。

Sectigo 产品管理副总裁 Lindsay Kent 表示:“任何跨数百台 web 服务器手动管理证书的组织都面临着意外证书过期和由此导致的系统故障的巨大风险，这可能会在一段时间内使业务陷入瘫痪。

**降低证书管理的总拥有成本**

单服务器 SSL 证书安装需要多达九个时间密集型步骤，包括登录、下载、续订配置和测试，每次安装或续订的成本估计为每个网站 50 至 100 美元。此外，对于使用多个域、通配符证书、反向代理或负载平衡器的 web 服务器，复杂性和成本只会增加。

每一步都需要 web 管理员或具有技术技能的员工进行精确管理，以避免人为错误和意外停机的风险，这可能会造成很高的成本。例如，移动运营商 [O2 在全球 3200 万客户以及其他运营商的客户服务中断后，要求爱立信](https://www.bbc.com/news/business-46499366)赔偿数百万美元。2018 年 12 月长达一天的网络数据崩溃归因于服务这些运营商的爱立信技术堆栈中的一个过期证书。

“手动安装 SSL 证书需要专业技能，否则企业会面临配置错误、无法了解已安装的证书，以及由于计划外事件而无法快速替换证书的风险。Kent 补充说:“一个对 HTML 编码和网站构建更熟练，而对 Linux shell 经验较少的网站管理员，在执行必要的步骤时可能会有很大的困难，或者可能要花大量的时间去学习。

**保持控制的同时实现自动化的四种方式**

Sectigo Certificate Manager 平台的改进通过提供自动安装和更新传统数据中心或 DevOps 环境中服务器的 SSL 证书的机制来解决这些企业级挑战，从而完全自动执行部署和持续管理。这种 ACME 支持适用于扩展验证(EV)、组织验证(OV)和域验证(DV) SSL 证书。

*   **行业标准 ACME 协议**—由 IETF 开发，自动化证书管理环境(ACME)定义了一个可扩展的框架，用于自动化证书的颁发和验证程序，使服务器无需用户手动交互即可获得 DV、OV 和 EV SSL 证书。超过 100 个开源 ACME 客户端可用于在 Apache、IIS、NGINX、F5 BIG-IP、Citrix Netscaler 和其他流行的 web 服务器和网络设备上自动颁发证书。ACME 工具完全自动化了密钥生成、域控制验证、证书创建以及在服务器上的安装。如果需要公共证书，客户可以直接向 Sectigo 申请。

*   **专有自动化方法**–对于 Apache、IIS、Tomcat 和 F5 BIG-IP 环境，Sectigo 提供了一个安装在客户所在地的客户端，然后该客户端可以与企业的所有服务器进行通信。Sectigo 证书管理器将 web 服务器管理员凭据嵌入到此代理中，用于安装证书和私钥传播。

*   **使用 REST API** 定制工作流——客户可以使用 Sectigo 的 [REST](https://www.smashingmagazine.com/2018/01/understanding-using-rest-api/) ful(表述性状态转移)API 来安装证书，允许定制工作流，包括批准和其他步骤。管理员可以要求批准来自 ACME 客户端的证书请求，并可以发现、跟踪、运行证书报告和手动更改证书。

*   **与第三方产品更紧密的集成—**Sectigo 已经与 F5 BIG-IP 集成，并致力于其他第三方集成，以提供完全自动化和工作流管理。

要了解更多信息，请观看 [Sectigo ACME 自动化视频](https://sectigo.com/resources/sectigos-acme-automation)。

**关于 Sectigo**

[Sectigo](https://sectigo.com/) (前身为 Comodo CA)提供网络安全产品，帮助客户保护、监控、恢复和管理他们的网络状态和连接设备。作为 20 多年来深受全球企业信赖的最大商业证书颁发机构，Sectigo 在 200 多个国家/地区颁发了超过 1 亿份 SSL 证书，拥有业经验证的性能和经验，能够满足保护当今数字环境的不断增长的需求。在 [LinkedIn](https://www.linkedin.com/company/sectigo/) 或 Twitter[@ sectighq](https://twitter.com/SectigoHQ)上关注 Sectigo。