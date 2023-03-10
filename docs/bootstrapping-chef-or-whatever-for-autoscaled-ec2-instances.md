# 为自动缩放的 EC2 实例引导 Chef(或任何东西)

> 原文：<https://devops.com/bootstrapping-chef-or-whatever-for-autoscaled-ec2-instances/>

我意识到，开始写一篇新的博客有一些背景，并对作者写这篇博客的个人动机进行深刻反省，这是一种传统，但我从来不是这样的传统。因此，对于我的第一个正式 DevOps 帖子，我想我会直接写一个关于去年夏天必须解决的问题的技术教程，我在其他地方还没有看到很好的记录。

你可以阅读我的简历了解更多，但这里是你在 HackOps 上可以期待的。我是一名行业分析师(在证券；我是 Securosis)的 CEO，但是有一个在 DEFCON 上做技术演讲的坏习惯。换句话说，是技术和执行层面的研究和分析的混合。

## 问题是

现在，让我们从技术层面开始:

去年夏天，我正在为黑帽会议组织一次示威游行，这时我遇到了一个小小的障碍。我想启动实例，让它们自动连接到一个 [Chef 服务器](https://www.getchef.com/chef/ "Chef")，并下拉一组默认的(安全)策略。问题是真的没有一个很好的内置方法来做到这一点，我在任何地方也找不到这样的文档。通常，在 EC2 实例中安装 Chef 的选项有:

*将 Chef 和配置加载到定制的 Amazon 机器映像中。我想使用默认的 ami，而不是维护我自己的 ami，所以这是行不通的。
*使用刀命令行工具(你如何管理厨师，为那些不知道的人)和 EC2 选项启动实例。但我想自动缩放我的图像，这意味着我不能从 Knife 启动它们，因为亚马逊网络服务将为我启动它们。
*使用 SSH 引导启动并运行后的引导实例。但是这是手动的，或者需要我在一些 automagic 代码中嵌入我的 SSH 密钥，所以这不是一个选项。
*手动安装和配置 Chef。不太像德文郡人，是吗？

现在我已经有了一些使用`cloud-init`配置实例的经验。`cloud-init`是一些操作系统中包含的一个工具，最著名的是 Ubuntu 和 Amazon Linux，它允许你在启动一个实例时注入一个脚本，并让它在你登录之前运行命令。您只需将您的脚本粘贴到**用户数据**字段中。

## 概观

Chef 实际上并没有很好地设计来处理这一点，因为它似乎更喜欢手动安装，但我设法拼凑了一个有效的过程。概括地说，它是这样工作的:

1.将您的 chef 配置(`client.rb`)、验证证书(`validation.pem`)和初始首次运行 Chef 文件(`first_run.json`)放入亚马逊 S3 桶中。
2。使用 AWS IAM 角色提供对 S3 时段的访问。IAM 角色本身就值得一贴，但简而言之，您可以通过 Amazon 为一个对象设置角色，并为其提供一组轮流访问 Amazon 其他部分的临时凭证。
3。编写一个 cloud-init 脚本来下载 Chef 和 s3cmd，这是一个用于访问亚马逊 S3 的命令行工具。
4。在您的脚本中，通过安装一个空白的配置文件将 s3cmd 设置为使用 IAM 角色(考虑到这部分是一个大问题，因为当时没有记录)。
5。在您的脚本中，使用 s3cmd 下载您的 Chef 配置文件，然后使用我们从 S3 下载的配置文件安装 Chef，其中一个将首次运行它并设置初始角色，Chef 将使用该角色来下推第一个策略集。
6。手动启动实例或作为自动缩放组的一部分启动实例。设置 IAM 角色，并将您的云初始化脚本粘贴到*用户数据*字段中。

现在我假设一些事情。首先，您知道如何使用 EC2，并为所有东西设置正确的安全组来相互通信。其次，您知道如何创建自动缩放组(或者手动启动一个实例并设置用户数据字段)。第三，你有一个厨师服务器或托管厨师已经成立。

如果你想了解更多的步骤，你可以在我发表的一篇论文中详细阅读——软件定义的安全性的一个实际例子。它稍微有点过时，但仍然有效(只需调整它以获得 S3 工具的当前版本，并删除脚本中的*修复路由愚蠢*部分，因为不再需要它，它会破坏东西)。

## 细节

以下是文件和命令的技术细节:

首先，对于您的 IAM 角色策略。将“cloudsec”替换为您创建的用于存放 client.rb、validator.pem 和 first_run.json 的任何存储桶的名称(我稍后会给出一个例子):

`{
"Version": "2012-10-17",
"Statement": [
{
"Effect": "Allow",
"Action": [
"s3:Get*",
"s3:List*"
],
"Resource": "arn:aws:s3:::cloudsec",
"Resource": "arn:aws:s3:::cloudsec/*"
}
]}`

接下来是您的云初始化脚本。您可以在中跳过整个脚本，也可以使用以下命令:

`#include
http://url-to-script`

如果你使用一个远程脚本，你可能想把它保存在 S3 的某个安全的地方，没有人能看到它，也没有人能看到你是如何配置的。这是 cloud-init 脚本本身，神奇的事情就发生在这里(我们的博客平台有点弄乱了格式，但仍然可读):

`#cloud-config`

apt_update: true

#apt_upgrade: true

包装:
-卷曲

config chef:
-&config chef |
echo " deb http://apt.opscode.com/ precise-0.10 main " | sudo tee/etc/apt/sources . list . d/ops code . list
apt-get 更新
curl http://apt.opscode.com/[【电子邮件保护】](/cdn-cgi/l/email-protection)| sudo apt-key add-
echo " chef chef/chef _ server _ URL string http://your-chef-server-URL:4000 " | sudo debconf-set-selections&&sudo/s 3c MD-config/s 3c MD-1 . 5 . 0-beta 1/s 3c fg ls S3://cloud sec/
。/s 3c MD-config/s 3c MD-1 . 5 . 0-beta 1/s 3c fg-force get S3://cloud sec/client . Rb/etc/chef/client . Rb
。/s 3c MD-config/s 3c MD-1 . 5 . 0-beta 1/s 3c fg-force get S3://cloud sec/validation . PEM/etc/chef/validation . PEM
。/s3cmd-config/s3cmd-1 . 5 . 0-beta 1/S3 CFG-force get S3://cloud sec/first _ run . JSON/etc/chef/first _ run . JSON
chef-client-j/etc/chef/first _ run . JSON

runcmd:
- [ sh，-c，*configchef]- touch /tmp/done

您会注意到，当我们启动 Chef 时，我们使用命令行选项来加载 first_run.json，它建立了初始的 Chef 角色。这允许我们将初始策略推送到实例，否则我们必须做更多的手工工作(ick)。我保持它的简单，仅仅为实例建立了一个 starter 角色，它对应于一个基本的运行列表。first_run.json 看起来像这样:

`{“run_list”:[“role[base]”]}`

设置好所有这些之后，正如我前面提到的，您只需要启动一个具有正确 IAM 角色的实例来访问 S3 桶，然后将 cloud-init 脚本粘贴到*User Data*字段中。这些都可以设置为自动缩放组规则的一部分，以便在新实例启动时自动运行。

剩下的就是魔法了。这个实例运行起来需要一点时间，并且所有部分连接起来需要一点时间，但是我们说的是不到 30 分钟。通常少于 30 分钟。

现在，当我把它作为一个安全演示时，我知道这种技术被用在至少一个你们都听说过的非安全配置管理的主要 web 属性的产品中。我并不认为这是我的功劳，几个月后我发现他们使用了一种他们自己发现的非常相似的技术。

同样的基本技术也应该适用于 Puppet 或您选择的配置管理工具。

老实说，当我开始我的项目时，我很惊讶我在任何地方都找不到这个过程的文档。这似乎是几乎所有在公共云中使用配置管理工具的人都需要的基本东西之一，因为一直构建自己的 ami 确实效率低下。

这是我很高兴在 DevOps.com 这里写作的一个重要原因，因为我认为我们作为一个社区，需要一个好的聚会场所来分享这种信息。