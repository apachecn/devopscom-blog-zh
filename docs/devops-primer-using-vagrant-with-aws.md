# DevOps 初级教程:在 AWS 中使用 vagger

> 原文：<https://devops.com/devops-primer-using-vagrant-with-aws/>

现代软件开发中最常见的问题之一是这样一句话，“它在我的机器上工作”，当一段特定的代码在开发人员的机器上运行，但在其他团队成员的机器上产生错误。令人欣慰的是，现在有一个插件可以帮助确定为什么某些东西只在特定环境下有效，把这句话变成更多的观察而不是借口。

# 流浪者去救援

是一个构建和维护可移植软件开发环境的工具。它将项目的依赖项和配置从项目中隔离出来，而不会干扰应用程序正在使用的工具。通过使用与您的机器相同的配置，您可以很容易地在其他机器上复制类似的环境。

## 《流浪者》中的基本概念

在进一步讨论之前，理解以下对流浪者工作至关重要的基本概念是很重要的。

### 供给商

置备程序为安装不同的软件和配置提供自动化。当您不想手动将软件安装到您的机器上时，这很有用。

### 提供者

提供商提供运行您的机器所需的基本服务。虽然流浪者提供了对 VirtualBox，Hyper-V 和 Docker 的支持，但也可以通过适当的插件使用其他提供者。

### 盒子

盒子是可迁移的环境包，可以被复制到任何其他机器上以复制类似的环境。流浪者提供了一个可以下载的这些盒子的[库](https://app.vagrantup.com/boxes/search)，你可以通过添加自己定制的盒子来为列表做贡献。

## 安装插件

这个过程的第一步是确保你的机器上安装了[vagger](https://www.vagrantup.com/downloads.html)。正如我前面提到的，您可以通过安装相应的插件来使用提供者。出于本教程的目的，我将通过以下命令下载**流浪者-aws** 插件:

流浪者插件安装流浪者-aws

接下来，通过命令验证插件安装:

vagrant plugin list

插件列表中应该有**vagger-AWS**插件

## 设置流浪箱

安装插件后，下一步是安装一个流浪盒。问题是没有 AWS 提供者的盒子。为了让事情顺利进行，我推荐你使用 Mitchell Hashimoto 提供的虚拟箱。

运行以下命令添加虚拟框:

流浪者盒子添加 AWS[https://github . com/Mitchell h/流浪者-aws/raw/master/dummy.box](https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box)

虽然我将这个盒子命名为 **aws** ，但是你可以给它取任何适合你的名字。一旦这个过程完成，我就可以创建 AWS 实例了。

## 创建实例

运行**travel init**命令创建一个 travel 文件:

流浪者初始化

接下来，编辑这个流浪者文件，如下所示:

# -*-模式:ruby -*-
# vi: set ft=ruby:

# Require AWS provider 插件
Require ' vagger-AWS '

#创建和配置 AWS 实例
vagger . configure(' 2 ')do | config |

#使用虚拟 AWS 框
config.vm.box = 'aws '

#指定 aws 提供程序的配置
config . VM . provider ' AWS ' do | AWS，override|
#从环境变量中读取 AWS 验证信息
AWS . access _ key _ id = ' abcr 2 ndjkzjiaj 5 qvxgjk '
AWS . secret _ access _ key = ' wauze 39 lkhxajncfbz f2y 6 dzrfecspuu/yZMRDWo '

#指定 SSH 密钥对以使用
AWS . key pair _ name = ' vagger '

#指定区域、AMI ID、实例和安全组
AWS . region = ' AP-southeast-2 '
AWS . AMI = ' AMI-14b 55 f 76 '
AWS . Instance _ type = ' T2 . micro '
AWS . security _ groups =[' default ']

#指定用户名和私钥路径
override . ssh . username = ' Ubuntu '
override . ssh . private _ key _ path = ' ~/游民/游民'
end
end

## 流浪者档案解释

下面的列表解释了上述文件的重要变量和方面:

*   box:指定盒子。使用虚拟 aws 箱进行 AWS 部署
*   aws.access_key_id:您的亚马逊帐户的访问密钥 id
*   aws.secret_access_key:亚马逊账户的秘密访问密钥
*   aws.keypair_name:您在 aws 中的 SSH 密钥对
*   aws.region:要在其中创建实例的 aws 区域
*   aws.ami:您要使用的 AMI ID。AMI 指定了在 EC2 中启动虚拟机所需的信息
*   aws.instance_type:要创建的 aws 实例
*   aws.security_groups:指定将应用于实例的安全组的名称
*   override.ssh.username:将用于访问实例的用户名
*   override.ssh.private_key_path:您的 ssh 私钥的路径

## 启动实例

在配置了 lavour file 之后，我将简单地运行**lavour up**命令。travel 将使用 travel file 中提供的凭证通过配置中提供的 AWS AMI 启动一个 AWS 实例。

![](https://devops.com/wp-content/uploads/2017/12/Vagrantdetails.png)
您可以在 AWS 控制台面板中查看新创建的实例。

现在，您可以 SSH 到您的 AWS 实例或者执行其他的漫游操作。

## 最后的话

正如您所看到的，使用 vagger 启动 AWS 实例只是简单地安装插件，然后通过简单的步骤启动实例。如果你在这个过程中需要帮助，请在下面留下评论。

## 关于作者/阿里·阿兹米

![](https://devops.com/wp-content/uploads/2017/12/AliAzmi.jpg) Ali Azmi 是 Cloudways——一个托管的 [PHP 云托管平台](https://www.cloudways.com/en/php-cloud-hosting.php)的 DevOps 助理工程师。他擅长开发 PHP 应用程序，尤其是 Laravel。他热衷于为开源项目做贡献。