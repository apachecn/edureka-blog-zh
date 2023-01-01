# 处理大数据的基本 Hadoop 工具

> 原文：<https://www.edureka.co/blog/essential-hadoop-tools-for-big-data>

如今，IT 界最流行的术语是“Hadoop”。在短短的时间内， [Hadoop](https://www.edureka.co/blog/business-applications-of-hadoop/) 大规模增长，并被证明对大量不同的项目非常有用。Hadoop 社区正在快速发展，并在其生态系统中扮演着重要角色。

*下面是用于处理大数据的基本 Hadoop 工具。*

**[![ambari](img/e8deb364cd175fe1a93acc54c874a141.png) ](https://www.edureka.co/blog/wp-content/uploads/2014/01/ambari.jpg)** 

**Ambari** 是由 Hortonworks 支持的 Apache 项目。它提供了一个基于 web 的 GUI(图形用户界面),带有向导脚本，用于设置包含大多数标准组件的集群。Ambari 供应、管理和监控 Hadoop 作业的所有集群。

**[![hdfs-logo](img/d97ee19c7da7b3de8c1c230d0d62b3eb.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/hdfs-logo.jpg)**

在 Apache 许可下发布的 **HDFS** 提供了一个在多个节点之间分割数据集合的基本框架。在 HDFS 中，大文件被分成块，其中几个节点保存文件中的所有块。文件系统的设计将容错和高吞吐量结合在一起。加载 HDFS 块以保持稳定的流。它们通常不被缓存以最小化延迟。

**[![hbaselogo](img/e2603d3a35385ee0b899640063ec97b6.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/hbaselogo.jpg)**

HBase 是一个面向列的数据库管理系统，运行在 HDFS 之上。HBase 应用程序是用 Java 编写的，非常像 MapReduce 应用程序。它由一组表组成，每个表像传统数据库一样包含行和列。当数据落入大表中时，HBase 将存储数据，搜索数据，并在多个节点之间自动共享该表，以便 MapReduce 作业可以在本地运行它。HBase 为某些局部变化提供了有限的保证。单行中发生的更改可以同时成功或失败。

[![hive](img/e58187febff094e891593b57c0766881.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/hive.png)

如果你已经精通 SQL，那么你可以使用 **Hive** 来利用 Hadoop。Hive 是由脸书的一些人开发的。Apache Hive 管理从 HBase 中的所有文件中提取位的过程。它支持对存储在 Hadoop HDFS 和兼容文件系统中的大型数据集进行分析。它还提供了一种类似 SQL 的语言，称为 HSQL (HiveSQL ),可以进入文件并提取所需的代码片段。

**[![sqoop](img/9030d539093d8e6ad5e0083cfa36368a.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/sqoop.jpg)**

Apache Sqoop 是专为将大量数据从传统数据库高效传输到 Hive 或 HBase 而设计的。它还可以用于从 Hadoop 中提取数据，并将其导出到外部结构化数据存储中，如关系数据库和企业数据仓库。Sqoop 是一个命令行工具，在表和数据存储层之间进行映射，将表转换为 HDFS、HBase 或 Hive 的可配置组合。

**[![Pig1](img/0476ea48f3fd8daae2a3df50d9e36d87.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/Pig1.png)**

当存储的数据对 Hadoop 可见时， **Apache Pig** 会深入数据并运行用自己的语言编写的代码，这种语言称为 Pig Latin。Pig Latin 充满了处理数据的抽象概念。Pig 附带了用于普通任务的标准函数，如平均数据、处理日期或查找字符串之间的差异。当标准函数不够时，Pig 还允许用户自己编写语言，称为 UDF(用户定义函数)。

**[![zookeper](img/1e44ea58b80210e4cd9eb05226e269a5.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/zookeper.jpg)**

Zookeeper 是一个集中的服务，它维护、配置信息、命名并提供集群间的分布式同步。它在集群上强加了一个类似文件系统的层次结构，并存储机器的所有元数据，因此我们可以同步各种机器的工作。

NoSQL

一些 Hadoop 集群集成了 **NoSQL** 数据存储，这些数据存储自带跨节点集群存储数据的机制。这使他们能够使用 NoSQL 数据库的所有功能来存储和检索数据，之后可以使用 Hadoop 在同一集群上安排数据分析作业。

**[![mahoutlogo](img/fb1401fb8a2ba45a0f8dbc9a8b6cd5bc.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/mahoutlogo.jpg)**

**Mahout** 旨在对 Hadoop 集群实现数据分析的大量算法、分类和过滤。许多标准算法，如 K-means、Dirichelet、并行模式和贝叶斯分类，都可以在 Hadoop 风格的地图和 reduce 上运行。

**[![lucene](img/5f99796fb6257806a8d57fd7b517f783.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/lucene.jpg)**

Lucene，用 Java 编写，易于与 Hadoop 集成，是 Hadoop 的天然伴侣。这是一个用于索引大块非结构化文本的工具。Lucene 处理索引，而 Hadoop 处理集群中的分布式查询。随着新项目的开发，Lucene-Hadoop 的特性也在快速发展。

**[![Avro](img/e5c97746b76b9aac8b377e2c921a9b60.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/Avro.jpg)**

Avro 是一个序列化系统，它将数据和理解数据的模式捆绑在一起。每个包都有一个 JSON 数据结构。JSON 解释了如何解析数据。JSON 的头指定了数据的结构，可以避免在数据中编写额外的标记来标记字段。输出比 XML 等传统格式要紧凑得多。

**[![Oozie](img/71d2d9153289d17b9265b590b40cd032.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/Oozie.jpg)**

一项工作可以通过分成几个步骤来简化。在将项目分成多个 Hadoop 任务时， **Oozie** 开始以正确的顺序处理它们。它按照 DAG(有向无环图)的规定管理工作流，不需要及时监控。

**GIS 工具**

对于运行 Hadoop 的集群来说，处理地理地图是一项繁重的工作。用于 Hadoop 项目的 GIS ( **地理信息系统**)工具采用了最佳的基于 Java 的工具来理解地理信息，以便与 Hadoop 一起运行。数据库现在可以使用坐标处理地理查询，代码可以部署 GIS 工具。

**[![flume-logo](img/e090132b9447b8629cac6c390b8afdba.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/flume-logo.png)**

收集所有数据等于存储和分析数据。Apache Flume 派遣“特工”收集信息，这些信息将被储存在 HDFS。收集的信息可以是日志文件、Twitter API 或网站碎片。这些数据可以被链接起来进行分析。

**[![Spark](img/d0b57162af77c1fcb8c3770de6c815a2.png)](https://www.edureka.co/blog/wp-content/uploads/2014/01/Spark.jpg)**

Spark 是下一代产品，它的工作方式非常像 Hadoop，可以处理缓存在内存中的数据。它的目标是通过一个通用的执行模型使数据分析快速运行和写入。这可以优化任意运算符图并支持内存计算，这使它比 Hadoop 等基于磁盘的引擎更快地查询数据。

**Hadoop 上的 SQL**

当需要对集群中的所有数据运行快速特别查询时，可以编写一个新的 Hadoop 作业，但这需要一些时间。当程序员开始更频繁地这样做时，他们想出了用简单的 SQL 语言编写的工具。这些工具提供了对结果的快速访问。

**阿帕奇演习**

Apache Drill 为大量不同的数据源(包括嵌套数据)提供了低延迟的即席查询。Drill 的灵感来自谷歌的 Dremel，旨在扩展到 10，000 台服务器，并在几秒钟内查询数 Pb 的数据。

这些是处理大数据必不可少的 Hadoop 工具！

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子:**

[学习 Hadoop 2.0 的实用理由](https://www.edureka.co/blog/4-practical-reasons-to-upgrade-to-hadoop-2 "4 Practical Reasons to Learn Hadoop 2.0")

[大数据是你的正确选择吗？](https://www.edureka.co/blog/is-big-data-the-right-move/ "Is Big Data the Right Move for You")

[Hadoop 如何助推你的事业](https://www.edureka.co/blog/5-reasons-to-learn-hadoop "5 Reasons to Learn Hadoop")

[Hadoop 入门](https://www.edureka.co/big-data-and-hadoop)