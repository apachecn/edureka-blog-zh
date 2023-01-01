# DynamoDB vs MongoDB:哪个更符合你的业务需求？

> 原文：<https://www.edureka.co/blog/dynamodb-vs-mongodb/>

这篇关于 [DynamoDB](https://www.edureka.co/blog/amazon-dynamodb-tutorial) 与 [MongoDB](https://www.edureka.co/blog/mongodb-the-database-for-big-data-processing/) 的文章将帮助您比较这两个数据库，以便您可以决定哪个更好地满足您的需求。本文将涉及以下几点:

*   [DynamoDB vs MongoDB](#DynamoDBvsMongoDB)
*   [谁用 DynamoDB 和 MongoDB？](#WhousesDynamoDBandMongoDB?)
*   [数据结构的不同](#TheDifferenceinDataStructures)
*   [对索引的需求](#TheNeedforIndexes)
*   [查询中的差异](#ADifferenceinQueries)
*   [dynamo db 和 MongoDB 的部署](#TheDeploymentofDynamoDBandMongoDB)
*   [复制和集群](#ReplicationandClustering)

那么让我们开始吧，

**DynamoDB vs MongoDB**

MongoDB 在新闻中出现已经有一段时间了。自 2009 年推出以来，世界各地的许多公司都开始使用这种关系数据库管理系统，这要归功于它广泛的功能和强大的通用性。但即便如此，人们在市场上选择不同的选项时还是会感到困惑。

在今天的文章中，我们将比较 MongoDB 和 DynamoDB，并分析哪一个更适合您的使用和需求。我们开始吧！

在我们深入比较这两种平台的复杂性之前，让我们先了解这两种平台的个性，以及是什么让它们脱颖而出。

**DynamoDB**

DynamoDB 可以简单地定义为专有的 NoSql 数据库管理服务，由 Amazon.com 提供，作为其 AWS 或亚马逊网络服务计划的一部分。虽然 DynamoDB 与原始的 Dynamo 程序有很多相似之处，但它有一个不同的底层实现，这使它非常独特。![Image - DYnamoDB vs MngoDB - Edureka](img/ba1cd2b996f17fac62ff590d284fbf91.png)

**MongoDB**

MongoDB 可以简单地定义为一个跨平台的关系数据库管理系统，它作为一个独立的程序提供。在 NoSQL 专有标签下分类，MongoDB 使用类似 JSON 的文档和模式标记来处理数据库需求，从而使其独一无二。

![Image - DynamoDB vs MongoDB - Edureka](img/63f0f73bdf83a219e6fa8da314019747.png) 继续这篇关于 DynamoDB vs MongoDB 的文章，

**谁用 DynamoDB 和 MongoDB？**

DynamoDB 和 MongoDB 已经存在了一段时间，因此世界各地的公司都使用这两种程序来满足他们的数据库需求。下面提到的是一些最重要的。

**MongoDB**

联合包裹、脸书、谷歌、波什、Adobe 和福布斯等等。

**DynamoDB**

三星、Snapchat、纽约时报、HTC、Dropcam，当然还有亚马逊等等。

继续这篇关于 DynamoDB vs MongoDB 的文章，

**数据结构的不同**

MongoDB 和 DynamoDB 之间的一些关键区别在于它们处理数据结构的方式。下面提到的是一些最重要的。

**DynamoDB**

在 DynamoDB 中，表、属性和项目是人们必须处理的主要组件。简单地说，表是项目的集合，每个项目是不同属性的集合。该平台利用主键来标识表中的每一项，还利用辅助索引来增加查询的灵活性。

**MongoDB**

另一方面，MongoDB 利用类似 JSON 的文档来存储与模式无关的数据。DynamoDB 和 MongoDB 之间的一个关键区别是不需要预定义数据和结构，从而为程序员一次存储不同类型的文档铺平了道路。

MongoDB 本身就是一个非常强大的关系数据库管理系统。因为它是无模式的，所以它允许程序员创建用于存储数据的文档，而不需要先预定义它。

下面的例子说明了 MongoDB 和 DynamoDB 中数据结构的不同。

dynamo db 中的表|列|值|记录，而 MongoDB 中的集合|键|值|文档。

继续这篇关于 DynamoDB vs MongoDB 的文章，

**对索引的需求**

关系数据库管理系统中的索引提供了对替代查询模式的访问，这在需要高速查询时很有用。在索引方面，DynamoDB 和 MongoDB 之间有很多不同之处，如下所示。

**DynamoDB**

在 DynamoDB 中，如果你需要运行一个查询，你首先需要创建一个二级索引。在 DynamoDB 中创建二级索引时，需要首先指定它的关键属性，然后按照标准过程使用它来运行查询或扫描表。这里需要注意的一个关键事实是，DynamoDB 没有查询优化器，因此创建二级索引是执行查询的唯一方式。

**MongoDB**

在 MongoDB 中，索引是必须的。如果在某种情况下，一个文档缺少一个索引，那么所有曾经创建的文档都需要被扫描，以便匹配查询搜索。也就是说，缺少索引会大大降低 MongoDB 中查询过程的速度，因此需要优先创建索引。

继续这篇关于 DynamoDB vs MongoDB 的文章，

**查询中的差异**

为了理解 MongoDB 和 DynamoDB 在查询上的确切区别，请看下面的例子。

```
DynamoDB
db.query({
TableName: "customer"
})
```

```
MongoDB
db.customer.find()
```

继续前进，

**dynamo db 和 MongoDB 的部署**

DynamoDB 和 MongoDB 的另一个关键区别是这些关系数据库管理系统最初是如何部署的。

大多数人认为 DynamoDB 是用 Java 编写的，而有些人则认为 DynamoDB 最初是部署在 Node.Js 中的。不管是什么情况，DynamoDB 都支持以下语言:Java、Swift、JavaScript、Node.js、PHP、NET 以及 Python。

MongoDB: MongoDB 完全用 C++编写，可以在 Linux、Windows 和 Mac OS 上下载。在 C++上编码的 MongoDB 支持多种语言，包括但不限于 Prolog、Python、Ruby、Java、JavaScript、PowerShell、ColdFusion 等等。

继续这篇关于 DynamoDB vs MongoDB 的文章，

**复制和集群**

**DynamoDB**

由于 DynamoDB 是 AWS 或亚马逊网络服务家族的一部分，它积极利用亚马逊 DynamoDB 跨区域复制库来跨多个区域实时同步。当程序员写入 DynamoDB 中的一个表时，由于 AWS 的快速操作，其他位置和/或区域中的其他表会实时更新。

**蒙戈布**

另一方面，单主机复制系统支持自动选举，该功能内置于系统中。这基本上意味着，如果在某种情况下主数据库变得不可用，程序员可以建立一个辅助数据库，并将其编程为主数据库。在 MongoDB 中，第一个副本被称为主副本，所有其他副本被称为辅助副本。

**结论**

虽然第一眼看上去 MongoDB 和 DynamoDB 非常相似，但只有进一步观察，你才会意识到它们提供了非常不同的功能。也就是说，根据你的需要，选择使用哪一个。

这就把我们带到了这篇关于 MongoDB 与 DynamoDB 的文章的结尾。

*现在，您已经了解了 Hadoop 及其特性，请查看 Edureka 的* ***[Hadoop 培训](https://www.edureka.co/big-data-and-hadoop/)*** *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 大数据 Hadoop 认证培训课程使用零售、社交媒体、航空、旅游和金融领域的实时用例，帮助学员成为 HDFS、Yarn、MapReduce、Pig、Hive、HBase、Oozie、Flume 和 Sqoop 领域的专家。*

*有问题吗？请在评论区提到它，我们会给你回复。*