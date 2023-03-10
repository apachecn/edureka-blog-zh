# Hadoop 2.0–常见问题

> 原文：<https://www.edureka.co/blog/hadoop-faq/>

这是一篇后续文章，回答了 edureka 在公共网络研讨会上提出的常见问题！关于 Hadoop 1.0 的局限性及其在 Hadoop 2.0 中的解决方案。

## **关于 Hadoop 的常见问题**

**迪帕克:**

**什么是 Hadoop？** Apache Hadoop 是一个开源软件框架，用于在商用硬件集群上存储和大规模处理数据集。它是一个开源数据管理软件框架，具有横向扩展存储和分布式处理功能。它由全球贡献者和用户社区构建和使用。

在我们的 Hadoop 博客文章[这里](https://www.edureka.co/blog/what-is-hadoop/ "What is Hadoop")和[这里](https://www.edureka.co/blog/why-hadoop/ "Why Hadoop")阅读更多内容。

**t1 干 T3**

**旅游、交通、航空行业有哪些大数据用例？**

**晴天:**

你能给我们指出一些我们可以研究的 Hadoop 实施的真实例子吗？ 我们生活在 ng 一个高峰时间日益拥堵的时代。运输运营商一直在寻求经济高效的方式来提供服务，同时保持其运输车队处于良好状态。在这一领域使用大数据分析可以帮助组织:

*   路线优化
*   地理空间分析
*   交通模式和拥堵
*   资产维护
*   收入管理(即航空公司)
*   存货管理
*   燃料节约
*   目标营销
*   客户忠诚度
*   产能预测
*   网络性能和优化

现实世界中的几个用例是: a) [确定飞行成本](http://hortonworks.com/blog/determining-flight-costs-with-storm-and-hadoop-and-yarn/ "Flight Costs")b)库存物流预测建模 c)[Orbitz world wide–客户购买模式](http://gigaom.com/2011/11/22/big-data-reveals-mac-users-book-pricier-hotels/ "Customer Buying Pattern")d)[六个超大规模 Hadoop 部署](http://www.datanami.com/2012/04/26/six_super-scale_hadoop_deployments/ "Hadoop Deployments")e)[Hadoop–不止增加了](http://gigaom.com/2012/06/05/10-ways-companies-are-using-hadoop-to-do-more-than-serve-ads/ "Hadoop - More than Ads") f) [企业中的 Hadoop](http://pramanicks.wordpress.com/2012/09/05/think-big-act-small-use-case-series-part-5-of-5-using-big-data-in-insurance-utilities-ecommerce-hi-tech-digitial-and-travel-industry/ "Hadoop in Enterprise")

您可以通过以下网址了解有关 Hadoop 实际实施的更多信息:

*   【2016 年里约奥运会:大数据助力年度最大体育盛事！
*   [医疗保健中的大数据:Hadoop 如何革新医疗保健分析](https://www.edureka.co/blog/hadoop-big-data-in-healthcare)

**:**

**Hadoop 是关于数据处理和加工的吗？我们如何进行报告和可视化分析。Qlikview，Tableau 可以用在 Hadoop 上面吗？**Hadoop 的核心组件 HDFS 和 MapReduce 都是关于数据存储和处理的。HDFS 用于存储，MapReduce 用于处理。但是 Hadoop 核心组件如 Pig 和 Hive 用于分析。对于可视化报告 Tableau，QlikView 可以连接到 Hadoop 进行可视化报告。

**Amit :**

**Hadoop 与 mongoDB** MongoDB 被用作“可操作的”实时数据存储，而 Hadoop 被用于离线批量数据处理和分析。 mongoDB 是一种面向文档的无模式数据存储，您可以在 web 应用程序中将其用作后端，而不是 MySQL 等 RDBMS，而 Hadoop 主要用于大量数据的横向扩展存储和分布式处理。

在我们的 [mongoDB 和 Hadoop 博客文章](https://www.edureka.co/blog/mongodb-with-hadoop-and-related-big-data/ "mongoDB and Hadoop")中阅读更多内容。

**:**

**Apache Spark 是 Hadoop** 的一部分吗？ Apache Spark 是一个用于大规模数据处理的快速通用引擎。Spark 速度更快，支持内存处理。Spark 执行引擎拓宽了 Hadoop 可以处理的计算工作负载类型，并且可以在 Hadoop 2.0 YARN 集群上运行。它是一个处理框架系统，允许在内存中存储对象(RDD ),并能够使用 Scala 闭包处理这些对象。它支持图形、数据仓库、机器学习和流处理。

如果你有一个 Hadoop 2 集群，你可以运行 Spark 而不需要任何安装。否则，Spark 很容易独立运行或在 EC2 或 Mesos 上运行。它可以读取 HDFS、HBase、Cassandra 和任何 Hadoop 数据源。

点击阅读更多关于 Spark [的内容。](http://spark.apache.org/ "Apache Spark")

**普拉萨德:**

**什么是阿帕奇水槽？** Apache Flume 是一个分布式的、可靠的、可用的系统，用于有效地从许多不同的源收集、聚集和移动大量的日志数据到一个集中的数据源。

**阿米特**

**SQL 与非 SQL 数据库** NoSQL 数据库是下一代数据库，主要解决一些问题

*   非关系的
*   分布的
*   源代码开放的
*   水平可伸缩

通常更多的特征适用，例如无模式、简单的复制支持、简单的 API、最终一致性/基础(非 ACID)、大量数据等等。例如，几个独特优势是:

*   NoSQL 数据库水平扩展，增加更多的服务器来处理更大的负载。另一方面，SQL 数据库通常是纵向扩展的，随着流量的增加，会向单个服务器添加越来越多的资源。
*   SQL 数据库要求您在添加任何信息和数据之前定义模式，但是 NoSQL 数据库是无模式的，不需要预先定义模式。
*   SQL 数据库是基于表的，具有遵循 RDBMS 原则的行和列，而 NoSQL 数据库是文档、键值对、图形或宽列存储。
*   SQL 数据库使用 SQL(结构化查询语言)来定义和操作数据。在 NoSQL 数据库中，不同数据库的查询是不同的。

**热门 SQL 数据库:** MySQL、Oracle、Postgres 和 MS-SQL热门 NoSQL 数据库:MongoDB、BigTable、Redis、RavenDb、Cassandra、HBase、Neo4j 和 CouchDB

查看我们关于 [Hadoop 和 NoSQL](https://www.edureka.co/blog/increasing-demand-for-hadoop-and-nosql-skills/ "Hadoop and NoSQL") 数据库的博客，以及其中一个数据库的优势: [Cassandra](https://www.edureka.co/blog/apache-cassandra-advantages/ "Apache Cassandra")

**:**

**Hadoop 有内置集群技术吗？** 一个 Hadoop 集群采用主从架构。它由一个主节点(NameNode)和一组从节点(DataNodes)组成，用于存储和处理数据。Hadoop 被设计为在大量不共享任何内存或磁盘的机器上运行。这些数据节点使用 [Hadoop 配置文件](https://www.edureka.co/blog/hadoop-cluster-configuration-files/ "Important Hadoop Configuration Files ")配置为集群。Hadoop 使用复制的概念来确保集群中始终至少有一份数据副本可用。因为有多个数据副本，所以存储在离线或失效服务器上的数据可以从已知的完好副本自动复制。

**:**

**Hadoop 中的作业是什么？什么都可以通过工作来完成？** 在 Hadoop 中，一个作业就是一个 MapReduce 程序来处理/分析数据。术语 MapReduce 实际上指的是 Hadoop 程序执行的两个独立且截然不同的任务。第一个是 Map 任务，它获取一组数据并将其转换成另一组中间数据，其中各个元素被分解成键值对。MapReduce 作业的第二部分是 Reduce 任务，它将来自 map 的输出作为输入，并将键-值对组合成一个较小的聚合键-值对集。正如名称 MapReduce 的顺序所暗示的，Reduce 任务总是在 Map 任务完成之后执行。点击阅读更多关于 MapReduce 作业[的信息。](https://www.edureka.co/blog/anatomy-of-a-mapreduce-job-in-apache-hadoop/ "MapReduce Job")

**:**

**NameNode**有什么特别之处？NameNode 是 HDFS 文件系统的核心。它保存元数据，如文件系统中所有文件的目录树，并跟踪文件数据在群集中的保存位置。实际数据作为 HDFS 块存储在 DataNodes 上。每当客户端应用程序希望定位文件或添加/复制/移动/删除文件时，它们都会与 NameNode 对话。NameNode 通过返回数据所在的相关 DataNodes 服务器列表来响应成功的请求。点击这里阅读更多关于 HDFS 建筑[的内容。](https://www.edureka.co/blog/apache-hadoop-hdfs-architecture/ "HDFS Architecture")

**:**

**Hadoop 2.0 是什么时候推向市场的？** 管理 Hadoop 开发的开源组织 Apache Software foundation (ASF)于 2013 年 10 月 15 日在其博客中宣布，Hadoop 2.0 现已正式发布(GA)。这一宣布意味着，经过漫长的等待，Apache Hadoop 2.0 和 YARN 现在已经准备好进行生产部署。更多关于[这个](https://www.edureka.co/blog/apache-hadoop-2-0-and-yarn/ "HAdoop 2.0")博客。

**:**

**非 MapReduce 大数据应用的例子不多？** MapReduce 对于解决大数据问题的很多应用来说都很棒，但并不是万能的；其他编程模型更好地服务于需求，例如图形处理(例如 Google Pregel / Apache Giraph)和具有消息传递接口(MPI)的迭代建模。

**:**

HDFS 的数据是如何排列和索引的？ 数据被分成 64 MB 的块(可通过参数配置)并存储在 HDFS。NameNode 将这些块的存储信息作为块 ID 存储在其 RAM 中(NameNode 元数据)。MapReduce 作业可以使用存储在 NameNode RAM 中的元数据来访问这些块。

**:**

我们可以在同一个集群上同时使用 MapReduce (MRv1)和 MRv2(带 YARN)吗？ Hadoop 2.0 引入了新的框架 YARN，在 Hadoop 上编写和执行不同的应用。所以，YARN 和 MapReduce 在 Hadoop 2.0 中是两个不同的概念，不应该混用。正确的问题是**“有可能在支持 YARN 的 Hadoop 2.0 集群上同时运行 MRv1 和 MRv2 吗？”**这个问题的答案是**“否”**，因为即使 Hadoop 集群可以配置为运行 MRv1 和 MRv2，但在任何时间点只能运行一组守护进程。这两个框架最终都使用相同的配置文件( **yarn-site.xml** 和 **mapred-site.xml** )来运行守护程序，因此，在 Hadoop 集群上只能启用这两个配置中的一个。

**马尼卡 :**

**下一代 MapReduce (MRv2)和 YARN 有什么区别？** YARN 和下一代 MapReduce (MRv2)是 Hadoop 2.0 中两个不同的概念和技术。YARN 是一个软件框架，不仅可以用来运行 MRv2，还可以运行其他应用程序。MRv2 是一个使用 YARN API 编写的应用程序框架，它在 YARN 中运行。

**巴拉特:**

**Hadoop 2.0 是否为 Hadoop 1.x 应用提供了向后兼容性？** **内哈 :**

**Hadoop 1.0 到 2.0 迁移需要繁重的应用代码** **迁移吗？** 不，大部分使用“org . Apache . Hadoop . mapred”API 开发的应用程序都可以在 YARN 上运行，无需任何重新编译。YARN 与 MRv1 应用程序二进制兼容，可以使用“bin/hadoop”在 YARN 上提交这些应用程序。点击阅读更多关于此[的内容。](http://hortonworks.com/blog/running-existing-applications-on-hadoop-2-yarn/ "MRv1 and MRv2")

**谢林:**

**Hadoop 2.0 中资源管理器节点失效会怎样？** 从 Hadoop 2 . 4 . 0 版本开始，也提供了对资源管理器的高可用性支持。ResourceManager 使用 Apache ZooKeeper 进行故障转移。当资源管理器节点出现故障时，辅助节点可以通过 ZooKeeper 中保存的集群状态快速恢复。在故障转移时，ResourceManager 重新启动所有排队的和正在运行的应用程序。

**:**

**Apache 的 Hadoop 框架在 Cloudera Hadoop 上能用吗？** Apache Hadoop 于 2005 年推出，其核心 MapReduce 处理引擎支持存储在 HDFS 的大规模数据工作负载的分布式处理。它是一个开源项目，有多个发行版(类似于 Linux)。Cloudera Hadoop (CDH)就是来自 Cloudera 的一个这样的发行版。其他类似的发行版有 HortonWorks、MapR、Microsoft HDInsight、IBM InfoSphere BigInsights 等。

**:**

**有什么简单的方法可以在我的笔记本电脑上安装 Hadoop，并尝试将 Oracle 数据库迁移到 Hadoop？** 你可以[从](https://www.edureka.co/blog/install-hadoop-single-node-hadoop-cluster "Hadoop 2.0 Installation")[开始](https://www.edureka.co/blog/install-apache-hadoop-cluster/ "Hadoop on Amazon AWS")在你的笔记本电脑上安装一个 HortonWorks 沙盒或者 Cloudera Quick VM(至少 4 GB RAM 和 i3 以上处理器)。使用 SQOOP 将数据从 Oracle 移动到 Hadoop，如这里的[所述](https://www.edureka.co/blog/hdfs-using-sqoop/ "SQOOP and Oracle")。

**巴巴尼:**

**学习 Hadoop 的最佳书籍有哪些？** 从[Tom White 的《Hadoop:权威指南](http://www.amazon.in/Hadoop-The-Definitive-Guide-White/dp/9350237563 "Hadoop Definitive Guide")和 Eric Sammer 的 [Hadoop Operations](http://www.amazon.in/Hadoop-Operations-Eric-Sammer/dp/1449327052 "Hadoop Operations") 开始。

**:**

Hadoop 2.0 有什么读物吗，就像《Hadoop 权威指南》一样？ 回顾书架上由 Hadoop 2.0 的少数创造者撰写的。

请继续关注本系列的更多问题。