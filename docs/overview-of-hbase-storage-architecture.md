# HBase 存储架构概述

> 原文：<https://www.edureka.co/blog/overview-of-hbase-storage-architecture/>

[//www.youtube.com/embed/-VG_WXdvDI0](//www.youtube.com/embed/-VG_WXdvDI0)

Apache HBase 是一个开源、分布式、非关系数据库，模仿 Google 的 Bigtable，用 Java 编写。它在 Hadoop 和 HDFS (Hadoop 分布式文件系统)之上提供了类似于 Bigtable 的功能，即它提供了一种存储大量稀疏数据的容错方式，这在许多大数据用例中很常见。HBase 用于对大数据的实时读/写访问。

HBase 存储架构由众多组件组成。让我们看看这些组件的功能，并了解数据是如何写入的。

**HFiles:**

HFiles 构成了 HBase 架构的底层。HFiles 是为了快速高效地存储 HBase 的数据而创建的存储文件。

**h 主控:**

HMaster 负责在 HBase 启动时将区域分配给每个 HRegionServer。它负责管理与行、表及其协调活动相关的一切。Hmaster 也有元数据的细节。

从 [数据工程课程](https://www.edureka.co/microsoft-azure-data-engineering-certification-course) 中了解大数据及其应用。

## **组件****h base:**

HBase 具有以下组件:

*   表格–包含区域
*   区域–存储在一起的行的范围
*   区域服务器–服务一个或多个区域
*   主服务器–守护程序负责管理 HBase 集群

HBase 将数据直接存储在 HDFS 中，并且非常依赖于 HDFS 的高可用性和容错能力。

## **HBase 存储架构:**

![HBase Storage Architecture](img/0362dc7991b49cc0df6f18db98079c24.png "HBase Storage Architecture")

一般的流程是，客户端首先联系 Zookeeper 来找到特定的行键。它通过从 Zookeeper 中检索服务器名称来实现这一点。有了这些信息，它现在就可以查询该服务器，以获取保存元表的服务器。这两个细节都被缓存，并且只被查找一次。最后，它可以查询元服务器并检索包含客户机正在寻找的行的服务器。你甚至可以用亚特兰大 [Azure 数据工程认证](https://www.edureka.co/microsoft-azure-data-engineering-certification-course-atlanta) 查看大数据的细节。

一旦知道了行所在的区域，它也会缓存这些信息并直接联系 HRegionServer。因此，随着时间的推移，客户机已经获得了从哪里获取行的完整信息，而不需要再次查询元服务器。当 HRegion 打开时，它为每个表的每个 HColumnFamily 设置一个 Store 实例。当客户端向 HRegionServer 发出请求时，数据被写入，HRegionServer 向匹配的 HRegion 实例提供详细信息。第一步是，我们必须决定数据是否应该首先写入由 HLog 类表示的“提前写入日志”(WAL)。该决定基于客户端设置的标志。一旦数据被写入 WAL，它就被放入 MemStore。同时，检查 Memstore 是否已满，在这种情况下，请求刷新到磁盘。然后数据被写入 HFile。

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子**

[大数据和 Hadoop 培训](https://www.edureka.co/big-data-and-hadoop)

[对 HBase 架构的见解](https://www.edureka.co/blog/insights-on-hbase-architecture "Insights on HBase Architecture")

[h base Vs MongoDB Vs Cassandra](https://www.edureka.co/blog/mongodb-vs-hbase-vs-cassandra/ "Face Off: MongoDB Vs HBase Vs Cassandra")