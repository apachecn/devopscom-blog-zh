# 物化视图简介

> 原文：<https://devops.com/introduction-to-materialized-views/>

通常，使用物化视图的查询类型比那些仍然直接处理对基表的查询的查询类型更快，并且使用的资源更少。但是理解物化视图所带来的潜力的关键在于首先尽可能多地理解它们。

## 什么是物化视图？

在计算世界中，物化视图是一个由任何查询结果组成的数据库对象。请注意，这可能是也存储在单独的远程位置的数据的本地副本，也可能是从连接结果中导出的。有时，甚至可以在用户执行聚合函数后创建物化视图，从而允许它充当数据库信息的摘要。

Oracle Database 首先在其软件的 8i 版本中提供了物化视图，从那以后，它就成了每个版本的一部分。支持物化视图的环境包括但不限于 SQL Server、BigQuery、PostgreSQL 和 Sybase SQL Anywhere 等。

## 视图与物化视图

常规视图和物化视图有什么区别？有一些重要的事情你需要记住。

其中最主要的是，视图本身是通过“Create View”命令创建的虚拟表的精确类型。顾名思义，它收集从您执行的任何相关查询中获得的所有数据。每次以任何方式使用或访问视图时，都会对其进行编译。这就是一个视图如何能够确保你总是得到最新的数据，无论发生什么——它就是为了做到这一点而设计的。

如果您对该视图中包含的数据进行任何更改，它将被推出到它原来所在的表中。同样，对该基表所做的任何更改都会自动推送到视图中，因此相同的信息会同时出现在两个地方。

由于这个额外的步骤，在性能方面，视图总是比物化视图慢一点。好处是，这真的不需要太多的存储空间。但这确实意味着您将在性能方面有所牺牲。

对于实例化视图，您谈论的是包含在原始表中的信息的物理副本。这意味着它不会在你每次与它交互时都更新——你必须特意手动更新它。或者，如果您愿意，您可以使用预定义的触发器来更新它。

因此，物化视图的响应速度总是比传统视图快得多。但是，如果您不努力确认它已经被更新，您也将面临检索陈旧数据的风险。

## 为什么要使用物化视图？

因此，在这一点上，您可能会问自己，"[为什么首先要使用物化视图](https://materialize.com/why-use-a-materialized-view/)？这能为我做些简单视图做不到的事情吗？”需要理解的关键是，无论何时查询数据库，都会产生成本。

甚至一个简单的查询仍然需要被解析、验证、计划、优化和执行。从操作角度来说，这相当于 CPU 时间。这意味着内存使用。随着时间的推移，这甚至会直接影响你的机会成本。所有这些加起来——尤其是当您正在使用的应用程序继续发展并变得更加资源密集型时。

精明的开发人员总是在寻找降低成本的方法，物化视图是他们能够做到这一点的重要部分。请记住，获得的结果总是保存在内存中，这意味着它们只在绝对需要时才会更新。这与查询表或使用逻辑视图时的情况相反；这些结果会不断更新。因此，使用[物化视图](https://www.appservgrid.com/documentation111/docs/rdbms12cr1/DWHSG/basicmv.htm#DWHSG8169)是显著降低成本的好方法，而且不会影响性能，也不会影响最终用户。

## 物化视图最佳实践

为了获得最佳结果，您应该始终确保您的物化视图反映了针对您正在使用的原始表的查询模式。不要只为查询的每次迭代创建一个物化视图。相反，创建一个来帮助关注更广泛的查询集。

同样，如果您正在使用的基表是分区的，那么您的物化视图可能会增长到超出您所能接受的大小。因此，也应该对它进行分区，以保持它应该带来的性能优势。