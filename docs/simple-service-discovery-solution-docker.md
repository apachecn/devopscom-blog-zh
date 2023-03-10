# 一个简单的 Docker 服务发现解决方案

> 原文：<https://devops.com/simple-service-discovery-solution-docker/>

大使模式是一种多主机 Docker 应用程序部署的方法。它帮助不同主机上的容器发现彼此并进行通信。尽管有各种变体，但这一思想可以如下说明:

*(web)-link->(web 代理)-network->(db 代理)-link->(db)*

代替`web`直接与`db`连接，

1.  本地 web 代理与`web`链接，并且`web`被配置为将所有流量发送到`localhost`，该流量由 web 代理接收
2.  除此之外，db 代理在键/值注册表中用预定义的键宣布`db`容器( [etcd](https://github.com/coreos/etcd "etcd") 、[consult](https://www.consul.io/ "consul")等)。web 代理也使用这个键来发现注册表中的`db`容器

3.  一旦发现，web 代理将把流量路由到 db 代理，db 代理与`db`容器链接。

结果，连接被建立。

**优点&缺点**

这种模式有许多优点:

1.  非侵入式:Docker 镜像可以在不做任何修改的情况下使用，因为它是静态配置的
2.  动态:容器可以以动态的方式发现彼此，这对于自动伸缩/负载平衡的情况特别有价值
3.  弹性:故障转移对容器是透明的

然而，对于上述好处也有一些权衡:

1.  复杂:需要学习和管理更多组件
2.  更多活动部件:错误的键或值可能会导致一些奇怪的结果，这可能特别难以调试
3.  不灵活:代理适合一对一或负载平衡的连接，但它不能处理其他拓扑，如发电机环

**解决方案**

与大使模式相比，服务发现的另一个解决方案是利用[文件挂载](https://docs.docker.com/v1.2/userguide/dockervolumes/#mount-a-host-file-as-a-data-volume)特性将应用程序配置文件从主机实例挂载到容器中:

*$ sudo docker run —rm -it -v ~/。bash_history:/。bash_history ubuntu /bin/bash*

方法是:

*   **简单**:没有代理，没有注册表，简单的配置文件
*   **非侵入式**:无代码更改或图像修改
*   **灵活**:适用于任何应用配置
*   **没有活动部件**:容易推理

有人可能会说这是容器的静态配置，不能处理自动伸缩和故障转移等场景。这个问题的答案是一个[编排引擎](www.visualops.io)。引擎需要密切关注集群，并重新生成配置文件，以确保无论何时发生什么，容器总能获得正确的连接。

从技术上讲，该解决方案可以解释为:

![](img/03f8890125955f4a8d2156de6d366430.png)

Docker Service Discovery Solution

这种显式的路由指定了服务之间的逻辑关系，而不是让实例通过中央数据库相互通告和发现。然后，引擎会在资源调配时呈现该文件:

*mysql:// [【电子邮件保护】](/cdn-cgi/l/email-protection) @{db。private IP address }:3306—->MySQL://[【邮件保护】](/cdn-cgi/l/email-protection) :3306*

使用这种方法部署多实例 Docker 应用程序，您需要做的只是指定三件事:

*   运行哪个 docker 映像，即我的/节点
*   容器设置，即端口、cpu、内存
*   应用程序配置文件内容以及与其他容器的链接

这个解决方案看起来并不特别性感，但是它非常简单和健壮；并且对于任何类型的应用程序都有绝对的吸引力。