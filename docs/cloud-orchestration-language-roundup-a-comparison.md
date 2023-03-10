# 云编排语言综述:比较

> 原文：<https://devops.com/cloud-orchestration-language-roundup-a-comparison/>

您与哪些云提供商合作？谷歌云平台(GCP)？亚马逊 AWS？微软 Azure？哪些服务？你是否在使用 GKE、AKS、Openshift 或 EKS 等托管的 Kubernetes？您如何管理您的云资源？您如何管理您部署的基础设施和应用程序的发布周期？

如果以上问题是描述您工作的基本介绍，那么您可能也熟悉某个主要云提供商的控制台、API 或两者。您可能知道如何使用配置管理工具，例如 Ansible 或 Chef、Terraform 或 CloudFormation，或者其他类似的工具。此外，您还熟悉其中一种工具的语言。您可能对这些语言有自己的看法，这些看法会影响您对所选工具的兴趣。

Kubernetes 和 Ansible 用途 [YAML](https://en.wikipedia.org/wiki/YAML) 。CloudFormation 和 Azure ARM 可以是 [JSON](https://en.wikipedia.org/wiki/JSON) 或者 YAML。Chef 和 Terraform 有各自的语言。(准确的说，Terraform 也可以用 JSON 来表达。)

![cloudify orchestration language comparison](img/c529055181a61645e909708ee6e3ec66.png)

A comparison of cloud orchestration languages

每当你开始学习一种新工具时，了解这种工具的语言是很有帮助的。使用标准语言的优势在于，如果新用户已经理解了一种语言的基本语法，他们会觉得在学习使用这种语言时更加得心应手。就像许多说英语的人在不使用音译的情况下会联想到法语、德语或拉丁语的同源词，而不是希腊语或梵语，了解 YAML 的开发人员会发现学习 Ansible 比学习依赖 XML 的工具更容易。然而，仅仅因为你知道这种语言并不意味着你知道 DSL。DSL 可能以一种新奇甚至奇怪的方式使用一种语言，这种方式与你认为正确的方式相矛盾。

当用户对一个工具产生看法时，许多变量可能会发挥作用。最重要的是，“对我来说，创造一个能做我想做的事情，并把以后的挫败感降到最低的东西有多简单？ “下一个经常是”，我冒昧地依赖于第一个，是明显的科学和分析思考？它适合复杂的数据结构吗？保持可读性的努力会因为空间或标点符号的低效使用而受挫吗？”

一些项目，比如 HashiCorp 的(Terraform ),放弃了一种标准语言来避免这样的问题，而是创建了他们自己的语言。这里的主要缺点是，将该工具与现有项目和软件库集成更加困难(尽管用标准语言(如 JSON)提供输入和输出可以缓解这些问题)。

Cloudify 有一个基于 YAML 的 DSL。Cloudify 使用 YAML，因为它比 JSON 更容易阅读，但足够强大，可以在必要时定义新的类型。

无论是使用 YAML 这样的通用语言还是专有语言，某些指定都是必要的:资源的类型、资源的名称，甚至通常是指资源、参数还是依赖关系。

为了说明这两种语言之间的差异，以及已经提到的相关产品，我们来看几个例子。让我们用一个相对简单的例子，一个 AWS VPC，名为“myVPC”在任何语言中，这都是一个简单的资源定义，因为它的参数相对较少，除了 AWS 帐户之外，没有任何依赖关系。

地形:

**资源“AWS _ VPC”“myVPC”{**

**cidr_block = "10.0.0.0/16"**

**instance_tenancy = "专用"**

**标签= {**

**foo = "bar"**

**}**

**}**

Terraform，或 HCL，因两个原因而出名。首先，HCL 的“block”语法让人想起许多熟悉的编程语言中的方法定义语法。在所有这些工具中，这是对 Terraform 如何将基础设施定义打包成代码的认可。第二，Terraform 最简洁。只需要七行。

此外，Terraform 语法通过使用标识符(如“resource”、“aws_vpc”和“main”)从字符串位置推断重要性 HCL 知道首先是块类型，其次是类型，然后是名称。就可读性而言，这可能是定义组件的理想且优雅的方法。块定义内部是 AWS EC2 服务接受的 API 有效负载，用于创建 VPC。

HCL 的一个缺点是标点符号的要求。需要用大括号将块和字典括起来。数组需要方括号。

让我们比较一下 HCL/Terraform 和云的形成:

**myVPC:**

**型号:AWS::EC2::VPC**

**属性:**

**CidrBlock: 10.0.0.0/16**

**实例租用:专用**

**标签:**

**–按键:foo**

**值:条**

CloudFormation 利用了 YAML 和 JSON。这些是数据序列化语言。所以，我们正在看我们的资源定义，更少地作为代码，更多地作为信息。这导致了更多的冗长和降低的可读性。不太简洁，CloudFormation 是八行。

鉴于 HCL 对资源使用“块”。CloudFormation 模板只是称它们为“资源”我们有键和值，而不是位置参数。“类型”定义了类型。属性引入 AWS EC2 服务接受的资源 API 负载。然而，YAML 减少了对标点符号的需求。字典是通过缩进和连字符列表来介绍的。这可以提高可读性，如果有人真的喜欢使用大括号和方括号，没有人会强迫他们不这样做。然而，它增加了所需的行数和字符数，因为即使是 DSL 的抽象部分也需要引入关键字。这是因为 YAML 接受 JSON。

Ansible 也有一个在 AWS 中创建 VPC 的模块。

**–名称:创造 VPC。**

**ec2_vpc_net:**

**名称:myVPC**

**cidr_block: 10.10.0.0/16**

**地区:美国东部-1**

**标签:**

**foo: bar**

**租赁:专用**

Ansible 也用 YAML；但是，API 有效负载和其他参数之间没有分离。例如，认证参数与有效负载参数处于同一级别。Ansible 使用模块进行基础设施管理，就像它使用模块来管理应用程序一样，这种方式虽然新颖，但却是以一种笨拙且相对无用的方式实现的。例如，您需要一个用于创建的剧本和一个用于删除的剧本。

云化:

**myVPC:**

**类型:cloudify.nodes.aws.ec2.Vpc**

**属性:**

**资源配置:**

**CidrBlock: 10.10.0.0/16**

**实例租用:专用**

**标签:**

**–按键:foo**

**–值:条**

Cloudify 也使用 YAML。它也适用于键值对。Cloudify 甚至比 CloudFormation 还要冗长。

节点模板可以是一个资源，也可以是一组资源。在 Cloudify 中，有三种类型的属性。resource_config，包含 API 有效负载；client_config，包含 API 认证；和编排属性，这些附加属性使您能够描述 Cloudify 将如何与资源交互。比如所有的资源都有 use_external_resource，也就是说 Cloudify 可以使用 Cloudify 没有创建的资源。

Terraform/HCL 使用“资源块”，CloudFormation 使用“资源”，而 Cloudify 使用“节点模板”节点模板可以是 VPC 或其他云资源，甚至是云形成模板或地形模板。

Azure 也有一个 orchestrator，Azure ARM，并且有自己的 DSL 来描述 Azure 资源。这就是 Azure ARM 中虚拟网络的定义:

**类型:微软。网络/虚拟网络**

**apiVersion: '2019-11-01'**

**名称:myVPC**

**位置:“[参数('位置')]”**

**属性:**

**地址空间:**

**      addressPrefixes:**

**–10 . 0 . 0 . 0/24**

**子网:**

**–名称:"[参数('子网名称')]"**

**属性:**

**        addressPrefix: 10.0.0.0/24**

Azure ARM 的一个显著区别是 YAML 中的资源条目没有键名，其定义是 name key 的值；相反，整个字典是一个列表项。这可能更简洁，但可能会损失一定的可读性。此外，Azure 与 Cloudify 的相似之处在于，资源定义“属性”与其他更一般的细节(如“apiVersion”或“location”)不在同一级别上。

访问参数的语法也有点迟钝。通过方括号和圆括号访问字典中的键可能是我们正在研究的 DSL 中最难读的方法之一。

和云形成一样，ARM 可以用 JSON 或者 YAML 写。

Terraform 可以用更少的代码行定义相同的 Azure 资源。

**资源“myVPC”【示例】{**

**name = "virtualNetwork1"**

**location = azure RM _ resource _ group . example . location**

**资源组名称= azurerm 资源组示例名称**

**地址空间= ["10.0.0.0/16"]**

**子网{**

**name = "subnet1"**

**address _ prefix = " 10 . 0 . 1 . 0/24 "**

**}**

**}**

Cloudify 将在 14 行中定义相同的资源。但是，这可以使用默认值来缩短。

**网络:**

**类型:cloudify . azure . nodes . network . virtual network**

**属性:**

**资源组名称:{获取输入:资源组名称}**

**名称:{获取输入:网络名称}**

**位置:{ get_input: location }**

**资源配置:**

**地址空间:**

**          addressPrefixes:**

**–10 . 10 . 0 . 0/16**

**子网:**

**–名称:子网 1**

**地址 _ 前缀:10.0.1.0/24**

Azure 和 Amazon 分别将 ARM 和 CloudFormation 公开为 API 对象。这使得编排者能够将这些资源栈作为单个资源来管理。

您可以在 Terraform 中定义一个 ARM 部署，如下所示:

**资源“azerm _ template _ deployment”“deployment”{**

**name = "myArmDeployment"**

**资源组名称= azurerm 资源组示例名称**

**template _ body = file(" $ { path . module }/environment . JSON ")**

**}**

类型需要部署名称、资源组名称和模板体。后者可以内联提供，也可以使用 Terraform 的文件函数提供。

Ansible 也可以定义 ARM 模板:

**–名称:创建 Azure 部署**

**azure_rm_deployment:**

**资源组:我的资源组**

**名称:我的部署**

**template _ link:' https://…/azure deploy . JSON '**

**parameters _ link:' https://…/azure deploy . parameters . JSON '**

Cloudify 还可以协调 ARM 部署。下面是 ARM 中使用 Cloudify 的一个简单的基础设施栈:

**部署:**

**类型:cloudify.azure.Deployment**

**属性:**

**位置:{ get_input: location }**

**名称:{获取输入:资源组名称}**

**template _ file:' resources/arm/environment . JSON '**

Cloudify 也可以接受文件或内联 JSON(或 YAML)。

已经为我们的基础设施组件定义了源代码，我们现在可以将其他资源和流程连接到这个基础设施依赖项。我们可以将 Terraform 模板用于 CICD 工作流或网络应用程序。

使用相同的方法，Cloudify 也可以调用 Terraform 堆栈:

**基础设施:**

**类型:cloud ify . nodes . terraform . module**

**属性:**

**资源配置:**

**来源:resources/terraform/template . zip**

**变量:**

**访问密钥:{获取密钥:aws 访问密钥 id }**

**秘密密钥:{获取秘密:aws 秘密访问密钥}**

**AWS _ region:{ get _ input:AWS _ region _ name }**

**AWS _ zone:{ get _ input:AWS _ zone _ name }**

**管理员用户:{获取输入:代理用户}**

**管理员密钥公共:{获取输入:公共密钥}**

Cloudify 还利用其他 Cloudify 部署堆栈作为服务组件:

**基础设施:**

**类型:cloudify.nodes.Component**

**属性:**

**资源配置:**

**蓝图:**

**id: my_deployment**

**蓝图 _ 档案:{ get_input: infra_archive }**

**主文件名:infra.yaml**

**部署:**

**id: my_deployment**

总而言之，有许多 DSL 用于编排云资源。两者各有侧重:Terraform 侧重于简单性和可重复性，CloudFormation 侧重于 Amazon，ARM 侧重于 Azure，Ansible 侧重于设置应用程序，Cloudify 侧重于使用户能够自动化任何任务，包括自动化 Cloudify。我们称之为“编排管弦乐”