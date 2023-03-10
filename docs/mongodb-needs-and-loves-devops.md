# MongoDB 需要并热爱 DevOps

> 原文：<https://devops.com/mongodb-needs-and-loves-devops/>

DevOps 不仅仅是更智能地运行基础设施，实现更多自动化。这是一种通过混合传统上孤立的管理和开发领域来设计敏捷、健壮和现代软件的方法。这意味着基础设施是代码，开发人员关注运营。它不仅仅意味着称系统管理员为“DevOps 工程师”；这意味着运营商和开发商无缝合作。总的来说，NoSQL 是一个天生喜欢开发运维的解决方案，它在采用开发运维方法的团队中茁壮成长，但如果你不这样做，它真的会伤害你。MongoDB 也不例外。通过融合灵活性、特性和性能，它在开发人员社区中获得了巨大的吸引力。一些团队被设置 MongoDB 进行开发的便利性所吸引，而忽略了考虑容量规划、调优、监控和维护。不要让这种事发生在你身上！或者，你将在凌晨 3 点付出代价，那时你正忙着找出你的 swell 应用程序停止运行的原因。相反，请花时间了解 MongoDB 的需求和功能，因为它不仅仅使开发变得容易，它还可以通过无障碍复制和通过用于执行数据访问的相同 API 对管理任务的完全访问来真正改善操作。让我们从 DevOps 的角度来看看 MongoDB。

## DevOps 想要:

### 精明的管理者。

对于至少不会说一种高级语言的系统管理员来说，DevOps 运动没有太大的空间。就系统编程而言，我个人认为 Ruby 最吸引我，但 Python 也是一个不错的选择。MongoDB 管理员应该擅长使用 javascript shell 和他们选择的编程语言来执行管理任务，为丰富的基础设施监控和自动化代码库打下基础。管理最佳实践在[管理文档](http://docs.mongodb.org/manual/administration/)中有广泛(如果不是详尽)的记录，所以从那里开始吧。请特别注意手册的[操作策略](http://docs.mongodb.org/manual/administration/strategy/)部分，该部分提供了您在规划系统设计和部署时应该注意的事项清单。

### 了解其基础设施后果的开发人员。

幸运的是，将应用程序扔过围墙投入运营的时代即将结束。开发人员必须了解他们的基础设施的本质，如何最好地利用它，以及它如何处理故障。MongoDB 为开发人员提供了编码基础设施细节的能力，而无需耦合到特定的实例，甚至主机名。在此，[标签](http://docs.mongodb.org/manual/tutorial/configure-replica-set-tag-sets/)、[写关注](http://docs.mongodb.org/manual/core/write-concern/)、[读喜好](http://docs.mongodb.org/manual/core/read-preference/)都是你的朋友。运行报告的代码(应该远离您的生产实例)可以指定它将只从标记为“报告”的实例中读取。管理员可以添加标记为“报告”的实例，或者用几行代码交换具有该标记的实例。参考本文的[结尾，获取示例代码](#example)。

### 基础设施状态清晰地发出警报，并使趋势可视化。

[MongoDB 监控](http://docs.mongodb.org/manual/administration/monitoring/)手册部分概述了监控实例的方法，包括第三方解决方案，包括自托管和 SaaS。 [MongoDB 管理服务](http://mms.mongodb.com/?pk_campaign=DevOps.com-MongoDB-loves-and-needs-DevOps-3-14)是 MongoDB，Inc .的免费监控、趋势分析和警报服务，您应该从第一天开始设置它，以监控您所依赖的每个实例。

### 基础设施可编程。

好了，您正在监视您的实例，为什么不致力于自动化您的基础设施来响应故障和负载需求呢？虽然 [MMS](http://mms.mongodb.com/?pk_campaign=DevOps.com-MongoDB-loves-and-needs-DevOps-3-14) 是一个显而易见的工具，但它不会插入到你的基础设施代码中。您可以使用 MongoDB 通过数据库命令方便地公开其内部机制，并使用`local`数据库进行复制。例如，您可以像这样在 Python 中检查副本集延迟:

```
import pymongo
# three mongods running on my laptop
c = pymongo.MongoReplicaSetClient(
    'Kusanagi.local:29017,Kusanagi.local:29018,Kusanagi.local:29019',
    replicaSet='test'
)

rs_status = c.admin.command('replSetGetStatus')

lag_threshold = 120 # up to two minutes of replica lag is ok for this example
primary_optime = [ member['optime'].as_datetime()
    for member in rs_status['members'] if member['state'] == 1 ][0]
secondary_optimes = [ member['optime'].as_datetime()
    for member in rs_status['members'] if member['state'] == 2 ]
for secondary_optime in secondary_optimes:
    if ( (primary_optime - secondary_optime).total_seconds > lag_threshold):
        # do stuff
```

使用[官方 ami](http://docs.mongodb.org/ecosystem/platforms/amazon-ec2/#deploy-from-aws-marketplace)在 Amazon EC2 上以编程方式提供 MongoDB 实例很容易，但是自动化 MongoDB 基础设施远不止于此。学习使用[数据库命令](http://docs.mongodb.org/manual/reference/command/)来配置副本集，因为您可以编写脚本将新实例加入副本集。如果使用分片，可以更新分片集群的[标签范围](http://docs.mongodb.org/manual/core/tag-aware-sharding/)，将块迁移到专门提供给仓库数据的分片中。

### 灾难恢复功能强大且自动化。

有许多方法可以备份 MongoDB，您选择的方法应该适合您的部署。所以通读一下 MongoDB 手册的[备份部分中的选项。你应该把那部分读两遍。](http://docs.mongodb.org/manual/core/backups/)

### 以帮助发布管理。

由于是无模式的，MongoDB 将企业从模式变更及其维护窗口的麻烦中解放出来。您的应用程序的新版本将开始编写包含该属性的用户文档，而不是修改用户表来包含新的“出生地”列。当然，您的用户配置文件渲染不会假设设置了这个值并抛出异常，它只是不显示“出生地”。这并不能成为您不进行变更管理的借口！在 DevOps 商店中，所有适用于生产的监控都适用于您的集成环境，我真诚地希望这是持续的。配置您将在生产中使用的所有监视器，并在指标超出范围时提醒*开发人员*。

## 结束语

在 DevOps 文化中，管理员阅读代码，开发人员规划基础设施，他们都参加相同的规划会议。使用 MongoDB 的工程师，无论是运营还是开发，都应该阅读[完整手册](http://docs.mongodb.org/manual/)。如果您的开发人员阅读开发部分，而您的管理员阅读管理部分，那么您实际上只是在做开发*和*操作。

## 示例代码–标签

在 MongoDB shell 中，标记副本集的实例如下所示:

```
test:PRIMARY> config = rs.config()
{
    "_id" : "test",
    "version" : 2,
    "members" : [
        {
            "_id" : 0,
            "host" : "Kusanagi.local:29017"
        },
        {
            "_id" : 1,
            "host" : "Kusanagi.local:29018"
        },
        {
            "_id" : 2,
            "host" : "Kusanagi.local:29019"
        }
    ]
}
test:PRIMARY> config.members[0].tags = { "use": "production" }
{ "use" : "production" }
test:PRIMARY> config.members[1].tags = { "use": "reporting" }
{ "use" : "reporting" }
test:PRIMARY> config.members[2].tags = { "use": "production" }
{ "use" : "production" }
test:PRIMARY> rs.reconfig(config)
Fri Mar  7 18:35:25.040 DBClientCursor::init call() failed
Fri Mar  7 18:35:25.042 trying reconnect to 127.0.0.1:29017
Fri Mar  7 18:35:25.042 reconnect 127.0.0.1:29017 ok
reconnected to server after rs command (which is normal)
```

下面是 Ruby 代码，假设配置相同:

```
require 'mongo'

# I'm running 3 mongods on my laptop
rset = Mongo::MongoReplicaSetClient.new(["Kusanagi.local:29017",
                                        "Kusanagi.local:29018",
                                        "Kusanagi.local:29019"])

# using the local db to get current config
config = rset['local']['system.replset'].find_one() 
admin_db = rset['admin']
config['members'][0]['tags'] = { "use" => "production" }
config['version'] += 1  # mongod avoids reconfig conflicts by insisting on an increasing version value
verify_version = config['version']
begin
    admin_db.command({ 'replSetReconfig' => config })
rescue Mongo::ConnectionFailure # expect your connection to close during this operation
    actual_version = rset['local']['system.replset'].find_one()['version']
    raise unless actual_version == verify_version
end
```

指定标记集仅适用于从辅助节点读取(因为只有一个主节点可供选择)。在 Ruby 中，它看起来像这样:

```
rset = Mongo::MongoReplicaSetClient.new(["Kusanagi.local:29017",
                "Kusanagi.local:29018", "Kusanagi.local:29019"])
analytics = rset['analytics']  # say we have an 'analytics' DB
cursor = analytics['page_views'].find({'page' => 'home'},
                                        :read => :secondary,
                                        :tag_sets => {:use => 'reporting'})
```

该查询使用`:read`选项指定只有辅助节点应该应答，使用`:tag_sets`选项指定只有标记有`'use': 'production'`的辅助节点才能使用。如果我在`members[0] (Kusanagi.local:29017)`是主服务器时将其关闭，并且`members[1] (Kusanagi.local:29018)`成为主服务器，那么上面的查询将会失败，因为作为主服务器，它不再有资格回答针对辅助服务器的查询，即使成员 1 被标记为`use: 'production'` 。这正是您想要的，以防止您的报告查询淹没您的生产实例。在评估了情况之后，您可能决定将`'use': 'reporting'`分配给成员 3，然后上面的查询将再次工作。请注意，Ruby 驱动程序创建的`MongoReplicaSetClient`在默认情况下不刷新副本集状态(从 1.9.2 版开始)，它们使用连接建立时存在的配置(并非所有驱动程序都如此，请确保您确定了驱动程序的行为)。这意味着，如果您重新分配标记值，现有连接将不会注意到这一变化。如果我将成员 1 的标签改为`'use': 'not reporting'`，上面的查询不会失败，它会将查询直接路由到成员 1。因此，如果您使用标记和 Ruby，请使用 refresh_mode 选项实例化您的客户端:

```
rset = Mongo::MongoReplicaSetClient.new(["Kusanagi.local:29017",
            "Kusanagi.local:29018", "Kusanagi.local:29019"],
            :refresh_mode => :sync)
```

详见 [MongoReplicaSetClient 文档](http://api.mongodb.org/ruby/1.9.2/Mongo/MongoReplicaSetClient.html)。Python 驱动程序通过启动后台进程来监控副本集健康和配置更改来处理这一问题，但是 API 并没有记录任何配置其轮询间隔的方法。