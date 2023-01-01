# 2023 年 HBase 上的 Hadoop 面试问题

> 原文：<https://www.edureka.co/blog/interview-questions/hbase-interview-questions/>

## **Apache HBase 面试问题**

寻找雇主经常问的 Apache HBase 面试问题？这里是关于 Hadoop 面试问题系列中 Apache HBase 面试问题的博客。希望大家一定没有错过我们 *[**Hadoop 面试问题** **系列**](https://www.edureka.co/blog/interview-questions/top-50-hadoop-interview-questions-2016/)* 的早前博客。

在浏览完 HBase 面试问题后，您将深入了解与 HBase 相关的 Hadoop 面试中雇主经常问的问题。这绝对有助于你启动大数据工程师的职业生涯，成为 ***[大数据认证专家](https://www.edureka.co/big-data-and-hadoop)*** 。

如果您以前参加过任何 HBase 访谈，我们鼓励您在评论选项卡中添加您的问题。我们很乐意回答这些问题，并向求职者传播这个信息。

## **Hadoop 面试问答|大数据面试问题|爱德华卡**



[https://www.youtube.com/embed/LgSiVWjTIUg?rel=0&showinfo=0](https://www.youtube.com/embed/LgSiVWjTIUg?rel=0&showinfo=0)*This Edureka video on Hadoop Tutorial on Hadoop Interview Questions and Answers will help you to prepare yourself for Big Data and Hadoop interviews.*

## **关于 Apache HBase 需要记住的要点:**

*   Apache HBase 是一个面向 NoSQL 列的数据库，用于存储稀疏数据集。它运行在 Hadoop 分布式文件系统(HDFS)之上，可以存储任何类型的数据。
*   客户端可以通过本地 Java API，或者通过 Thrift 或 REST 网关访问 HBase 数据，从而可以从任何语言访问它。

*♣提示:在阅读本 Apache HBase 面试问题之前，我建议您阅读一下 [**Apache HBase 教程**](https://www.edureka.co/blog/hbase-tutorial)* 和 *[**HBase 架构**](https://www.edureka.co/blog/hbase-architecture/) 来修正您的 HBase 概念。*

![HBase Logo - Edureka](img/e71a3284574cab308240bb8fbc7d973b.png)现在继续，让我们看看 Apache HBase 面试问题。

## **1。HBase 的关键组件是什么？**

HBase 的关键组件是 Zookeeper、RegionServer 和 HBase Master。

 <caption>#### **h base 的关键部件**</caption> 
| **分量** | **描述** |
| **地区服务器** | 一张表可以分成几个区域。一组区域由区域服务器提供给客户端 |
| **HMaster** | 它协调和管理区域服务器(类似于 NameNode 管理 HDFS 的 DataNodes)。 |
| **动物园管理员** | Zookeeper 在 HBase 分布式环境中扮演着协调者的角色。它通过会话通信来帮助维护集群内部的服务器状态。 |

## **2。您何时会使用 HBase？**

*   HBase 用于我们需要随机读写操作的情况，它每秒钟可以对大型数据集执行多次操作。
*   HBase 提供强大的数据一致性。
*   在商用硬件集群上，它可以处理具有数十亿行和数百万列的超大型表格。

## **3。get()方法有什么用？**

get()方法用于从表中读取数据。

## **4。定义 Hive 和 HBase 的区别？**

Apache Hive 是建立在 Hadoop 之上的数据仓库基础设施。它有助于使用 Hive Query Language (HQL)查询存储在 HDFS 的数据进行分析，Hive Query Language()是一种类似 SQL 的语言，可以翻译成 MapReduce 作业。Hive 在 Hadoop 上执行批处理。

Apache HBase 是 NoSQL 的一家关键/价值商店，位于 HDFS 之上。与 Hive 不同，HBase 操作实时运行在其数据库上，而不是 MapReduce 作业上。HBase 对表进行分区，表被进一步划分为列族。

Hive 和 HBase 是两种不同的基于 Hadoop 的技术——Hive 是运行 MapReduce 作业的类似 SQL 的引擎，HBase 是 Hadoop 的 NoSQL 键/值数据库。我们可以一起使用它们。Hive 可用于分析查询，而 HBase 可用于实时查询。甚至可以在 HBase 和 Hive 之间读写数据，反之亦然。

## **5。解释 HBase 的数据模型。**

HBase 包括:

*   套表。
*   每个表格由列族和行组成。
*   行键在 HBase 中充当主键。
*   对 HBase 表的任何访问都使用该主键。
*   出现在 HBase 中的每个列限定符表示对应于驻留在单元中的对象的属性。

## **6。定义柱族？**

列族是列的集合，而行是列族的集合。

## **7。在 HBase 中定义独立模式？**

这是 HBase 的默认模式。在独立模式下，HBase 不使用 HDFS，而是使用本地文件系统，它在同一个 JVM 进程中运行所有 HBase 守护进程和一个本地 ZooKeeper。

## **8。什么是装饰滤镜？**

修改或扩展过滤器的行为以获得对返回数据的额外控制是很有用的。这些类型的过滤器被称为装饰过滤器。它包括 SkipFilter 和 WhileMatchFilter。

## **9。什么是 RegionServer？**

一张表可以分成几个区域。一组区域由区域服务器提供给客户。

## **10。HBase 的数据操作命令有哪些？**

h base 的数据操作命令有:

*   **放置**–将单元格值放置在特定表格中指定行的指定列。
*   **获取**–获取一行或一个单元格的内容。
*   **删除**–删除表格中的单元格值。
*   **delete all**–删除给定行中的所有单元格。
*   **扫描**–扫描并返回表格数据。
*   **count**–计算并返回表格中的行数。
*   **截断**–禁用、删除和重新创建指定的表格。

## **11。在 HBase 中使用哪个代码打开连接？**

下面的代码用于打开一个 HBase 连接，这里*用户*是我的 HBase 表:

```
Configuration myConf = HBaseConfiguration.create();
HTable table = new HTable(myConf, “users”);

```

## **12。truncate 命令有什么用？**

用于禁用、删除和重新创建指定的表。

***♣提示:**要删除表格先禁用它，然后再删除它。*

## **13。** **在 HBase 中发出删除命令会发生什么？**

一旦在 HBase 中对单元格、列或列族发出删除命令，它不会立即被删除。插入了一个墓碑标记。Tombstone 是一种指定的数据，它与标准数据一起存储。这个逻辑删除隐藏了所有被删除的数据。

实际数据在大压缩时被删除。在主要压缩中，HBase 将一个区域中较小的 HFile 合并并重新提交给一个新的 HFile。在此过程中，相同的柱族一起放置在新的 HFile 中。在此过程中，它会丢弃已删除和过期的单元。scan 和 get 的所有结果都会过滤已删除的单元格。

## **14。****h base 中有哪些不同的墓碑标记？**

h base 中有三种类型的墓碑标记:

*   版本标记:只标记一个列的一个版本进行删除。
*   列标记:将整列(即所有版本)标记为删除。
*   族标记:将整个列族(即列族中的所有列)标记为删除

## **15。HBase blocksize 配置在哪个级别？**

块大小按列族配置，默认值为 64 KB。该值可以根据需要进行更改。

## **16。哪个命令用于运行 HBase Shell？**

T1。/bin/hbase *shell* 命令用于运行 HBase shell。在 HBase 目录中执行该命令。

## **17。哪个命令用于显示当前 HBase 用户？**

whoami 命令用于显示 HBase 用户。

## **18。MSLAB 的完整形式是什么？**

MSLAB 代表 Memstore-本地分配缓冲区。每当请求线程需要向 MemStore 中插入数据时，它不会从整个堆中为该数据分配空间，而是分配专用于目标区域的内存区域。

## **19。定义 LZO？**

伦佩尔-齐夫-奥伯胡默(LZO)是一种无损数据压缩算法，专注于解压缩速度。

## **20。什么是 HBase Fsck？**

HBase 附带了一个名为 hbck 的工具，由 HBaseFsck 类实现。HBaseFsck (hbck)是一个用于检查区域一致性和表完整性问题以及修复损坏的 HBase 的工具。它以两种基本模式工作——只读不一致识别模式和多阶段读写修复模式。

## **21。什么是休息？**

Rest 代表表述性状态转移，它定义了语义，因此该协议可以以通用的方式用于寻址远程资源。它还支持不同的消息格式，为客户端应用程序与服务器通信提供了多种选择。

## **22。什么是节俭？**

Apache Thrift 是用 C++编写的，但是提供了许多编程语言的模式编译器，包括 Java、C++、Perl、PHP、Python、Ruby 等等。

## **23。什么是 Nagios？**

Nagios 是一个非常常用的支持工具，用于获取有关集群状态的定性数据。它定期轮询当前指标，并将它们与给定的阈值进行比较。

## **24。ZooKeeper 有什么用？**

ZooKeeper 用于维护区域服务器和客户端之间的配置信息和通信。它还提供分布式同步。它通过会话通信来帮助维护集群内部的服务器状态。

每个区域服务器和 HMaster 服务器定期向 Zookeeper 发送连续的心跳，并检查哪个服务器是活动的和可用的。它还提供服务器故障通知，以便可以执行恢复措施。

## **25。在 HBase 中定义目录表？**

目录表用于维护元数据信息。

## **26。在 HBase 中定义压缩？**

HBase 通过合并 HFiles 来减少存储空间，减少读取所需的磁盘寻道次数。这个过程称为压缩。压缩从一个区域中选择一些 HFiles 并组合它们。有两种类型的压实。

*   **次要压缩** : HBase 自动挑选较小的 hfile，重新提交给较大的 hfile。
*   **大压缩**:在大压缩中，HBase 将一个区域中较小的 HFile 合并并重新提交给一个新的 HFile。

## **27。HColumnDescriptor 类有什么用？**

HColumnDescriptor 存储关于列族的信息，如压缩设置、版本号等。它在创建表或添加列时用作输入。

## **28。哪个过滤器接受 pagesize 作为 hBase 中的参数？**

PageFilter 接受页面大小作为参数。将结果限制在特定页面大小的过滤器接口的实现。一旦过滤通过的行数大于给定的页面大小，它就终止扫描。

语法:page filter(<page _ size>)

## **29。您将如何以编程方式设计或修改 HBase 中的模式？**

可以使用 Apache HBase Shell 或使用 Java API 中的 Admin 来创建或更新 HBase 模式。

创建表模式:

```
Configuration config = HBaseConfiguration.create();
HBaseAdmin admin = new HBaseAdmin(conf); // execute command through admin</span></pre>

// Instantiating table descriptor class
HTableDescriptor t1 = new HTableDescriptor(TableName.valueOf("employee"));

// Adding column families to t1
t1.addFamily(new HColumnDescriptor("professional"));
t1.addFamily(new HColumnDescriptor("personal"));

// Create the table through admin
admin.createTable(t1);

```

*♣提示:修改列族时必须禁用表。*

进行修改:

```
String table = “myTable”;
admin.disableTable(table); 
admin.modifyColumn(table, cf2); // modifying existing ColumnFamily 
admin.enableTable(table);

```

## **30。Apache HBase 中有哪些可用的过滤器？**

h base 支持的过滤器有:

*   **【columnprifxfilter】**:接受单个参数，一个列前缀。它只返回以指定的列前缀开始的列中的键值。
*   **TimestampsFilter** :获取时间戳列表。它返回那些时间戳与任何指定时间戳匹配的键值。
*   **PageFilter** :接受一个参数，一个页面大小。它从表中返回页面大小和行数。
*   **multiplecolumnprixfilter**:获取列前缀列表。它返回以任何指定的列前缀开头的列中存在的键值。
*   **ColumnPaginationFilter**:接受两个参数，一个 limit 和一个 offset。它返回偏移列数之后的限制列数。它对所有行都这样做。
*   **【SingleColumnValueFilter】**:接受一个列族、一个限定符、一个比较运算符和一个比较器。如果找不到指定的列，将发出该行的所有列。如果找到了该列，并且与比较器的比较返回 true，则将发出该行的所有列。
*   **RowFilter** :接受一个比较运算符和一个比较器。它使用比较运算符将每个行键与比较器进行比较，如果比较结果返回 true，则返回该行中的所有键值。
*   **QualifierFilter** :接受一个比较运算符和一个比较器。它使用比较运算符将每个限定符名称与比较器进行比较，如果比较结果返回 true，则返回该列中的所有键值。
*   **ColumnRangeFilter** :取 minColumn、maxColumn 中的一个，或者两个都取。只返回那些列在 minColumn 和 maxColumn 之间的键。它还需要两个布尔变量来指示是否包含 minColumn 和 maxColumn。如果不想设置 minColumn 或 maxColumn，可以传入一个空参数。
*   **ValueFilter** :取一个比较运算符和一个比较器。它使用比较运算符将每个值与比较器进行比较，如果比较结果返回 true，则返回该键值。
*   **【前缀过滤器】**:接受一个参数，一个行键的前缀。它只返回以指定行前缀开始的行中的键值。
*   **singlecolumnvaluexclundefilter**:采用与 SingleColumnValueFilter 相同的参数，并且行为相同。但是，如果找到了该列并且条件通过，则除了测试的列值之外，该行的所有列都将被忽略。
*   **ColumnCountGetFilter** :接受一个参数，一个限制。它返回表中的第一个限制列数。
*   **【InclusiveStopFilter】**:接受一个参数，一个停止扫描的行键。它返回直到并包括指定行的所有键值。
*   **【DependentColumnFilter】**:带两个参数必需参数，一个族和一个限定符。它尝试在每行中定位该列，并返回该行中具有相同时间戳的所有键值。
*   **FirstKeyOnlyFilter** :不带参数。返回第一个键值对的键部分。
*   **KeyOnlyFilter** :不带参数。返回每个键值对的键部分。
*   **FamilyFilter** :取比较运算符和比较器。它使用比较运算符将每个家族名称与比较器进行比较，如果比较结果返回 true，则返回该家族中的所有键值。
*   **自定义过滤器**:您可以通过实现过滤器类来创建自定义过滤器。

## **31。我们如何备份 HBase 集群？**

执行 HBase 备份有两种主要策略:完全关闭集群进行备份，以及在活动集群上进行备份。每种方法都有优点和局限性。

**全关机备份**

一些环境可以容忍其 HBase 群集定期完全关闭，例如，如果它正被用作后端进程，而不是为前端网页提供服务。

*   **停止 HBase** :先停止 HBase 服务。
*   **Distcp** : Distcp 可以用来将 HDFS 的 HBase 目录的内容复制到另一个目录中的同一个集群，或者复制到不同的集群。
*   **恢复**:来自 HDFS 的 HBase 目录的备份通过 distcp 复制到‘真实的’h base 目录。复制这些文件的行为会创建新的 HDFS 元数据，这就是为什么这种恢复不需要从 HBase 备份时开始恢复 NameNode 编辑，因为这是对特定 HDFS 目录(即 HBase 部分)而不是整个 HDFS 文件系统的恢复(通过 distcp)。

**活集群备份**

无法处理停机的环境使用实时集群备份。

*   **CopyTable** : Copy table 实用程序既可以用来将数据从一个表复制到同一个集群上的另一个表，也可以将数据复制到另一个集群上的另一个表。
*   **导出**:导出方法将表的内容转储到同一个集群上的 HDFS。

## **32。HBase 如何处理写失败？**

故障在大型分布式系统中很常见，HBase 也不例外。

如果托管尚未刷新的内存的服务器崩溃。内存中但尚未保存的数据会丢失。HBase 通过在写入完成之前写入 WAL 来防止这种情况。每台服务器都是。

HBase cluster 在发生变化时保持记录状态。WAL 是底层文件系统上的一个文件。在新的 WAL 条目被成功写入之前，写入不被认为是成功的。这种保证使得 HBase 像支持它的文件系统一样持久。大多数时候，HBase 是由 Hadoop 分布式文件系统(HDFS)支持的。如果 HBase 关闭，还没有从 MemStore 刷新到 HFile 的数据可以通过重放 WAL 来恢复。

## **33。从 HBase 读取数据时，在返回值之前，将从哪三个位置对数据进行协调？**

读取过程将依次经历以下过程:

*   为了读取数据，扫描器首先在块缓存中寻找行单元。这里存储了所有最近读取的键值对。
*   如果扫描仪未能找到所需的结果，它会移动到 MemStore，因为我们知道这是写缓存。在那里，它搜索最近写入的文件，这些文件还没有被转储到 HFile 中。
*   最后，它将使用布隆过滤器和块缓存从 HFile 加载数据。

## **34。能解释一下数据版本化吗？**

除了是无模式数据库之外，HBase 也是版本化的。

每次对单元格执行操作，HBase 都会隐式存储一个新版本。创建、修改和删除一个单元都被同等对待，它们都是新版本。当一个单元超过最大版本数时，额外的记录将在主要压缩过程中被删除。

您可以在单元格内的特定版本上操作，而不是删除整个单元格。单元格内的值被版本化，并被标识为时间戳。如果没有提到版本，则使用当前时间戳来检索版本。单元版本的默认数量是三。

## **35。什么是布隆过滤器，它如何帮助搜索行？**

HBase 支持 Bloom Filter 来提高集群的整体吞吐量。HBase Bloom Filter 是一种节省空间的机制，用于测试 HFile 是否包含特定的行或行列单元格。

如果没有布隆过滤器，确定 HFile 中是否存在行关键字的唯一方法是检查 HFile 的块索引，该索引存储 HFile 中每个块的起始行关键字。两个开始键之间有许多行落差。因此，HBase 必须加载块并扫描块的键，以确定该行键是否确实存在。

## **结论:**

我希望这些 Apache HBase 面试问题对你有所帮助。这只是我们 Hadoop 面试问题系列的一部分。请参考下面的链接，享受阅读:

*   [***50 强 Hadoop 面试问题***](https://www.edureka.co/blog/interview-questions/top-50-hadoop-interview-questions-2016/)
*   [***Hadoop 集群面试题***](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-hadoop-cluster/)
*   **[*Hadoop HDFS 面试题*](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-hdfs-2/)**
*   [***Hadoop MapReduce 面试问题***](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-mapreduce/)
*   ***[猪面试问题](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-pig/)***
*   ***[蜂巢面试问题](https://www.edureka.co/blog/interview-questions/hive-interview-questions/)***

![edureka-logo](img/bca9d88a43f9e9eea1cbd535cdb93e01.png)有问题吗？在评论区提到它们，我们会给你回复。