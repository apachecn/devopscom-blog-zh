# 迁移到 GitHub

> 原文：<https://devops.com/migrating-to-github/>

最近几个月，Newt Global Consulting 将多个源代码库迁移到 GitHub。这些存储库的源代码从 10MB 到几千兆字节不等。这个博客是为了分享我们将源代码从 SVN 和 AccuRev 迁移到 GitHub 的经验。下面的大部分材料应该对任何 Git 存储库都有效。

我们使用了 100%免费的开源工具，并开发了符合我们需求的流程。非常感谢这些工具的作者；没有他们，我们不可能成功。开源社区万岁，愿机器编码的那一天永远不会到来！

本文主要关注执行迁移；GitHub 的最佳实践或分支策略不在范围之内。

在开始迁移之前，我们观察到了一些促使组织远离传统源代码库的因素:

*   管理者和架构师喜欢 GitHub 的分布式和离线特性。
*   加强开发人员的纪律(减少依赖的借口——你有所有东西的本地副本，智能合并 GitHub，等等)。).
*   精通技术的团队已经在使用 GitHub (Git 桥)。
*   开发人员讨厌一开始的变化，但他们学得很快，喜欢适应行业的其他部分。
*   与其他 DevOps 工具包的集成是一个动力(例如:Webhooks)。
*   自然适合开源软件开发(易于扩展和贡献)。
*   企业级的团队正在推动变革(追赶单个开发团队和行业的其他成员)。
*   GitHub 的文件大小限制迫使使用二进制库和类似的安全团队，因为他们现在可以监控遍布整个组织的大型开源库。

## SVN 到 GitHub 的迁移

网上有很多关于 SVN 和 GitHub 之间区别的资料。我建议你看一看(如果你不得不看的话)。以下是我们觉得有趣的几个链接:

*   SVN 和 GitHub 的分支差异:[http://stack overflow . com/questions/2471606/how-and-or-why-is-merging-in-git-better-SVN](https://stackoverflow.com/questions/2471606/how-and-or-why-is-merging-in-git-better-thanin-)
*   如果你是 SVN 的粉丝，看看下面这些关于 SVN 的伟大:[https://svnvsgit.com/](https://svnvsgit.com/)

### 先决条件

*   获取 SVN 资料档案库的只读用户访问权限。
*   确保“gitsvn”实用程序在本地环境中可用。
*   从[https://bitbucket.org/atlassian/svn-migrationscripts/](https://bitbucket.org/atlassian/svn-migrationscripts/)T2 下载 svn-migration-scripts.jar
*   关于以上脚本的更多文档，请参考以下 URL:[https://www.atlassian.com/git/tutorials/migrating-prepare/](https://www.atlassian.com/git/tutorials/migrating-prepare/)
*   决定 GitHub 组织名称、团队名称和团队成员。
*   建立组织。
*   建立团队并分配团队成员。
*   创建一个存储库，从您的工作区推送代码。

### 移民

*   从 SVN  中提取用户信息`java -jar svn-migration-scripts.jar authors <SVN Repo URL> > authors.txt`
*   克隆 SVN 库` git svn clone –stdlayout –authors-file=authors.txt <SVN Repo URL> <GitHub Repo
Name>`
*   创建到远程存储库的连接`git remote add origin <GitHub Repo URL>`
*   将代码从本地推送到远程`git push –u origin master`
*   将远程分支转换为本地`java -Dfile.encoding=utf-8 -jar svn-migration-scripts.jar clean-git –force`
*   将所有更改推送到远程`git push –all`

### 值得注意的

*   我们在 Linux(区分大小写的文件系统)上运行脚本；在 https://www.atlassian.com/git/tutorials/migrating-prepare/，OS X 有更多的步骤要遵循
*   如果 SVN 实例定义了本地用户 id(不是 SSO)，那么创建的作者文件就没有用了。但是您需要这个文件来成功运行脚本。
*   增量迁移是可能的，但是我们计划在过渡阶段每周进行完全迁移。
*   完全迁移需要时间；尽量避免网络延迟。对我们来说，我们的 300MB 回购大约需要 4 到 6 个小时。
*   在某些情况下，由于访问问题，我们不得不将 SVN 回购克隆到我们的本地文件系统。

## AccuRev 到 GitHub 迁移

[AccuRev](https://www.microfocus.com/products/changemanagement/accurev) 是 Borland(现微焦点)开发的集中式版本控制系统。它使用客户机-服务器体系结构和预备技术，因此提取完整迁移的代码有点棘手。我们使用了 Navico 开发的 ac2git 实用程序——该工具完成了繁重的工作，但进行了一些迭代和调整以满足我们的需求。最大的困难在于理解 AccRev 如何工作以及与 GitHub 的相对映射。

### 先决条件

*   安装 python 3.4、Git-Bash 版本 2.7.4 和 AccuRev
*   确保 AccuRev 和 git 可执行文件的路径对于您的机器是正确的，并且已经设置了 git 默认配置
*   从[https://github.com/NavicoOS/ac2git](https://github.com/NavicoOS/ac2git)克隆 ac2git 回购
*   运行 python AC 2 git . py–help 查看所有选项(强烈建议您这样做)
*   运行 python AC 2 git . py–example-config 获取配置示例
*   严格遵循“如何使用”一节中概述的步骤；否则，你会在几次失败的尝试后被强迫

### 移民

*   制作一个示例配置文件:
    *   python AC 2 git . py–示例-配置
*   修改生成的文件 ac2git.config.example.xml，(该文件中有大量注释，是时候运行了——如果您没有按照先决条件中的建议进行操作，请选择帮助选项)
*   将 ac2git.config.example.xml 文件重命名为 ac2git.config.xml
*   修改配置文件并添加以下信息:
    *   设置 accurev 用户名和密码
    *   说出仓库的名称。将每个仓库映射到单个 Git 存储库。分别为每个软件仓库运行脚本
    *   将多个软件仓库的脚本运行到单个文件夹会覆盖同一文件夹中的所有软件仓库流。当给定多个文件夹时，脚本会失败，因此始终一次为一个软件仓库运行脚本
    *   创建一个空文件夹，并在配置 xml 文件中提供完整的路径。文件夹必须存在，并且最好是空的
    *   不存在文件夹名称与流名称相同的概念。只需要有一个空的文件夹来存储流的所有内容
    *   开始和结束交易，对应于您在 accurev hist 命令中作为(关键字最高或关键字现在)输入的内容
    *   如果开始事务和结束事务有时间规定，脚本将只在此时间段内获取数据和历史记录。例如 start-transaction = " 2013-02-07 13:41:17 "和 end transaction =
        " 2014-02-07 13:41:17 "
    *   在结束交易中使用“最高”关键字，而不是“现在”
        *   “现在”将获取该日期之前的数据，如果有一些历史从工作区中删除或没有从其他流中提升，则“现在”关键字将不起作用
        *   “最高”关键字始终查找最新和最高的提交历史记录(首选选项)
    *   从 Accurev 到 GitHub 的用户映射。提示:运行 accurev show -fi users 查看所有用户的列表
    *   选择转换流的首选方法
        *   对于稀疏流，建议使用“deep-hist”方法(改变流内容的事务相距很远)
        *   推荐常规流的“diff”方法(有疑问时，就用“deep-hist”。)
    *   运行脚本
        *   python ac2git.py
    *   如果遇到任何问题，请运行带有–help 标志的脚本以获得更多选项。

### 值得注意的

*   这条河流总会有一些历史。当没有可用的历史时，脚本对我们不起作用。
*   如果有任何重复或缺失的用户名，请确保使用相应的参数。我们最终更改了脚本来处理重复的用户(如果您使用正确的参数，这是不需要的)。
*   在 ac2git.py 代码的 GetMissingUsers(config)方法中，注释最后两行
    *   #如果找不到:
    *   # missingList.append(用户)
*   迁移需要时间，尽量避免网络延迟。对我们来说，一个 300MB 的回购大约需要 6 到 8 个小时。
*   我们没有尝试增量迁移—我们计划每周进行一次完整迁移，并在一个长周末切换所有用户。

## 结论

总的来说，这次经历是非常有益的，不仅是在组装正确的工具包方面，而且在流程方面也是如此。每个组织都有自己的方法来管理源代码，以及如何提升代码(分支策略)。我们发现，中小型企业比一些大型企业有更成熟的流程，尽管它们正在快速追赶。

*   不要指望大型企业有集中管理的源代码回购(SVN 托管在经理办公桌下的一些可共享桌面上)。
*   很难让开发人员思考分布式思维(我为什么要克隆整个回购协议？).
*   与企业 GitHub 密切合作有助于让客户放心。
*   大多数开发人员喜欢使用 IDE 插件，而不是命令行或 web 客户端。
*   准备回答备份、高可用性和灾难恢复相关问题。
*   Enterprise GitHub 以虚拟设备而非应用程序的形式出现，让您做好准备，与基础架构团队一起将虚拟机部署到生产环境中。
*   一些应用程序组更喜欢提升和移位模式，而不是迁移模式；当他们说“不关心历史”时，不要感到震惊(通常这些是小的开发团队)。
*   将 Slack 与 GitHub 整合——这不仅受到了开发者的冲击，也受到了领导层的冲击。
*   扩展的 Hygeia 仪表板为领导层视图提供团队级分析。

## 关于作者/斯里达尔·佩丁蒂

![sridharpeddinti](img/99c6d9bdebf735418ba754da7d60d663.png)斯里达尔·佩丁蒂是纽特全球咨询公司开发运维及云实践副总裁。他是一名拥有 20 年技术和业务经验的领导者，在多个垂直行业执行大型项目方面拥有丰富的全球经验。他支持咨询领域，帮助客户解决复杂问题，并为他们提供开发运维及云战略。他在使用工具包组合和将大量遗留系统迁移到云和相关技术来改进流程方面拥有丰富的实践经验。在 [LinkedIn](https://www.linkedin.com/in/sridharpeddinti) 和 [Twitter](https://www.twitter.com/sridharpeddinti) 上与他联系。