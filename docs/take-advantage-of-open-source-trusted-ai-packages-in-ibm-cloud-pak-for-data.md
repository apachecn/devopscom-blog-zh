# 利用 IBM Cloud Pak 中的开源可信 AI 包来获取数据

> 原文：<https://devops.com/take-advantage-of-open-source-trusted-ai-packages-in-ibm-cloud-pak-for-data/>

**IBM 开放技术副总裁 Todd Moore**

随着开源人工智能技术的发展，人工智能系统公平决策、不受篡改和可解释的需求比以往任何时候都更加重要。在 IBM，我们相信建立对人工智能的信任始于开放，代码是透明的，任何人都可以访问。鉴于我们对可信人工智能的承诺，IBM 已经使安全访问 IBM Cloud Pak 中的三个可信人工智能包变得很容易。

具体来说，我们正在向 IBM Cloud Pak for Data 添加人工智能公平性 360 工具包、人工智能可解释性 360 工具包和对抗性鲁棒性工具箱，以便我们的用户可以利用关键包，帮助他们以更明智的方式做出有关数据的决策。

*   [【AIF 360】AI Fairness 360 Toolkit(AIF 360)](https://github.com/IBM/AIF360):AI Fairness 360 包有 Python 和 R 两种版本，包括一套全面的数据集和模型的度量标准(超过 70 种)，用于测试偏差，对这些度量标准的解释，以及减轻数据集和模型偏差的算法(约 11 种)。AIF360 将实验室的算法研究转化为金融、人力资本管理、医疗保健和教育等广泛领域的实际实践。 [找到使用工具的指导](http://aif360.mybluemix.net/resources#guidance) 。
*   [AI explailability 360 Toolkit(AIX 360)](https://github.com/IBM/AIX360):开源库，在整个 AI 应用生命周期中支持数据集和机器学习模型的可解释性和可解释性。AI Explainability 360 Python 包包括一套全面的算法，涵盖了解释的不同维度以及代理可解释性度量。 [找到使用工具的指导](http://aix360.mybluemix.net/resources#guidance) 。
*   [【对抗性鲁棒性工具箱(ART)](https://github.com/IBM/adversarial-robustness-toolbox) :一个 Python 库，支持开发者和研究人员防御机器学习模型对抗对抗性威胁(包括规避、提取和中毒)，并帮助使 AI 系统更加安全和可信。ART 包括用最先进的威胁模型测试防御的攻击。找到关于 [笔记本](https://github.com/IBM/adversarial-robustness-toolbox/blob/master/notebooks/README.md) 和 [示例](https://github.com/IBM/adversarial-robustness-toolbox/blob/master/examples/README.md) 的教程来使用该工具。

IBM Cloud Pak for Data 的用户可以通过产品中的开源管理服务来利用这些包。

**在开源管理服务中使用可信 AI 包**

5 月，IBM [宣布](https://www.ibmbigdatahub.com/blog/improve-your-roi-open-source-management-ibm-cloud-pak-data) 在 Cloud Pak for Data 3.0 中提供开源管理(OSM)服务，这是我们完全集成的数据和人工智能平台，可以使您的企业收集、组织和分析数据的方式现代化，以在整个组织中注入人工智能。

该服务提供对 800 个开源包的精选列表的访问，并引导您通过受管理的工作流来请求提供对安全和漏洞风险的见解的包。结果是，您能够更好地了解哪些开源包使用得最多，您的组织中谁在使用这些包，以及与每个项目相关的漏洞。

您可以通过 IBM Cloud Pak 中的开源管理服务来使用可信的 AI 包。安装 OSM 服务后，您可以选择两种不同的方式与包进行交互:

**选项 1–查看见解**

此选项显示了使用开源包的项目数量、使用每种许可证类型的包数量、受漏洞影响的包数量、用户与开源包交互的次数以及所有包中最活跃的用户的整体视图。

**选项 2–查看套餐**

此选项使您能够查看所有可用的包。每个软件包都包括一个摘要、漏洞检查报告、与软件包相关的支持文档、使用软件包的项目列表以及链接到新项目的条款。一旦请求，批准过程就开始了。批准后，您可以在链接的项目中安全地使用它，并使用“View Insights”管理它。

[查看我们的文档](https://www.ibm.com/support/knowledgecenter/en/SSQNUZ_2.5.0/cpd/svc/opensource/opensource.html) 了解更多关于开源管理服务的信息。如果你已经准备好亲自试用 Cloud Pak 获取数据，可以考虑免费试用 [7 天](https://www.ibm.com/account/reg/us-en/signup?formid=urx-34120) 。