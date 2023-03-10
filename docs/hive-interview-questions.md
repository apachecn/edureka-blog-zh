# 2023 年要准备的顶级 Hadoop 面试问题 Apache Hive

> 原文：<https://www.edureka.co/blog/interview-questions/hive-interview-questions/>

寻找雇主经常问的 Apache Hive 面试问题？ 这里是 Hadoop 面试问题系列中关于 Apache Hive 面试问题的博客。希望大家一定没有错过我们之前的 *[**Hadoop 面试问题** **系列**](https://www.edureka.co/blog/interview-questions/top-50-hadoop-interview-questions-2016/)* 的博客。

浏览完这篇 Apache Hive 面试问题博客后，您将深入了解雇主在与 Apache Hive 相关的 Hadoop 面试中经常问的问题。要了解 Hive & Hadoop 框架的每一个细微差别，你可以看看我们的 [***Hadoop 在线课程***](https://www.edureka.co/big-data-and-hadoop) 。

如果您以前参加过任何 Hadoop 访谈，我们鼓励您在评论选项卡中添加您在这里遇到的 Apache Hive 问题。我们很乐意回答这些问题，并向求职者传播这个信息。

## **阿帕奇蜂巢——简介**

Apache Hive 是建立在 Hadoop 之上的数据仓库系统，用于分析结构化和半结构化数据。它提供了一种机制来将结构投射到数据上，并执行用 HQL (Hive 查询语言)编写的类似于 SQL 语句的查询。在内部，这些查询或 HQL 被 Hive 编译器转换为 map reduce 作业。

## **阿帕奇蜂巢工作趋势:**

今天，许多公司将 Apache Hive 视为在大型数据集上执行分析的事实。此外，由于它支持类似 SQL 的查询语句，它在非编程背景并希望利用 ***[Hadoop MapReduce 框架](https://www.edureka.co/blog/mapreduce-tutorial/)*** 的人当中非常受欢迎。

现在，让我们来看看过去几年阿帕奇蜂房工作的上升趋势:![Apache Hive Job Trends - Apache Hive Interview Questions - Edureka](img/314550141e0dcb733402cd88c535c0a3.png)

**来源:**

上图清楚地显示了该行业对 Apache Hive 专业人员的巨大需求。因此，是时候做好准备，抓住这个机会了。

我建议你在继续这篇阿帕奇蜂巢面试问题博客之前，先浏览一下关于阿帕奇蜂巢教程的专门博客，以修正你的概念。

## **阿帕奇蜂巢面试问题**

下面是 Apache Hive 面试中最常被问到的问题的完整列表，这些问题是经过深入研究并与行业专家讨论后形成的。

### **1。定义 Hive 和 HBase 的区别？**

 <caption>#### **【hive vs hbase】**</caption> 
| **HBase** | **鼠标** |
| 1。HBase 建在 HDFS 的顶端 | 1。这是一个数据仓库基础设施 |
| 2。HBase 操作在其数据库上实时运行，而不是 | 2。配置单元查询作为 MapReduce 作业在内部执行 |
| 3。为大型数据集的单行提供低延迟 | 3。为大型数据集提供高延迟 |
| 4。提供对数据的随机访问 | 4。提供对数据的随机访问 |

### **2。Apache Hive 支持什么样的应用？**

Hive 支持所有用编写的客户端应用程序

*   Java
*   PHP
*   Python
*   C++
*   红宝石

通过暴露它的廉价服务器。

### **3。配置单元表的数据存储在哪里？**

默认情况下，Hive 表存储在 HDFS 目录–/ user/Hive/warehouse 中。可以通过在 hive-site.xml. 中的*hive . metastore . warehouse . dir*配置参数中指定所需的目录来更改它

### **4。什么是 Hive 中的 metastore？**

Hive 中的***[Metastore](https://www.edureka.co/blog/hive-tutorial/)***使用 RDBMS 和称为 Data Nucleus 的开源 ORM(对象关系模型)层存储元数据信息，该层将对象表示转换为关系模式，反之亦然。

### **5。为什么 Hive 不在 HDFS 存储元数据信息？**

Hive 使用 RDBMS 而不是 HDFS 在 metastore 中存储元数据信息。选择 RDBMS 的原因是为了实现低延迟，因为 HDFS 读/写操作是耗时的过程。

### **6。本地和远程 metastore 有什么区别？**

*本地 Metastore:*

在本地 metastore 配置中，metastore 服务在运行 Hive 服务的同一个 JVM 中运行，并连接到在同一台机器或远程机器上的单独 JVM 中运行的数据库。

*远程 Metastore:*

在远程 metastore 配置中，metastore 服务运行在它自己单独的 JVM 上，而不是在 Hive 服务 JVM 中。其他进程使用节俭网络 API 与 metastore 服务器通信。在这种情况下，您可以拥有一个或多个 metastore 服务器来提供更高的可用性。

### **7。Apache Hive 为 metastore 提供的默认数据库是什么？**

默认情况下，Hive 为 metastore 提供一个由本地磁盘支持的嵌入式 Derby 数据库实例。这称为嵌入式 metastore 配置。

### **8。场景:**

***假设我已经使用默认 metastore 配置在我的 Hadoop 集群上安装了 Apache Hive。那么，如果我们有多个客户端同时尝试访问 Hive 会怎么样呢？***

默认 metastore 配置一次只允许打开一个配置单元会话来访问 metastore。因此，如果多个客户端试图同时访问 metastore，它们将会收到一个错误。必须使用独立的 metastore，即 Apache Hive 中的本地或远程 metastore 配置，以允许同时访问多个客户端。

以下是将 MySQL 数据库配置为 Apache Hive 中的本地 metastore 的步骤:

*   应该在 hive-site.xml 中进行以下更改:
    *   *javax . jdo . option . connection URL*属性要设置为 JDBC:*MySQL*:*//host/*dbname？create databa*seIfNotExist = true。*
    *   *javax . jdo . option . connection driver name*属性应该设置为*com . MySQL . JDBC . driver .*
    *   用户还应该将用户名和密码设置为:
        *   javax . jdo . option . connection username 被设置为所需的用户名。
        *   javax . jdo . option . connection password 设置为需要的密码。
*   用于 MySQL 的 JDBC 驱动程序 jar 文件必须在配置单元的类路径上，即 JAR 文件应该被复制到配置单元的 lib 目录中。
*   现在，重启 Hive shell 后，它将自动连接到作为独立 metastore 运行的 MySQL 数据库。

### **9。外部表和托管表有什么区别？**

外部表和托管表的主要区别如下:

*   在托管表的情况下，如果删除托管表，元数据信息连同表数据一起从 Hive warehouse 目录中删除。
*   相反，对于外部表，Hive 只删除关于该表的元数据信息，并保留 HDFS 中的表数据不变。

***注:*** 建议大家去看看 ***[Hive 教程](https://www.edureka.co/blog/hive-tutorial/?#data_model)*** 上的博客，了解更多关于 Hive 中托管表和外部表的知识。

### **10。可以改变托管表的默认位置吗？**

是的，可以改变被管理表的默认位置。可以通过使用子句–LOCATION '<HDFS _ path>来实现。

### **11。什么时候应该使用排序依据而不是排序依据？**

当我们必须对大型数据集进行排序时，我们应该使用 SORT BY 而不是 ORDER BY，因为 SORT BY 子句使用多个归约器对数据进行排序，而 ORDER BY 使用单个归约器对所有数据进行排序。因此，对大量输入使用 ORDER BY 将花费大量时间来执行。

### **12。Hive 中的分区是什么？**

Hive 将表组织成分区，以便根据列或分区键将相似类型的数据分组在一起。每个表可以有一个或多个分区键来标识特定的分区。从物理上讲，分区只不过是表目录中的一个子目录。

### **13。为什么我们要在 Hive 中执行分区？**

分区提供了配置单元表中的粒度，因此，通过仅扫描与**相关的**分区数据而不是整个数据集，减少了查询延迟。

*以*为例，我们可以将一个电子商务网站的交易日志按月份进行划分，如一月、二月等。因此，任何关于特定月份(比如一月)的分析都必须只扫描一月分区(子目录)，而不是整个表数据。

### **14。什么是动态分区，什么时候使用？**

在动态分区中，分区列的值在运行时是已知的，即在将数据加载到配置单元表的过程中是已知的。

在以下两种情况下可以使用动态分区:

*   从现有的未分区表中加载数据，以改善采样，从而减少查询延迟。
*   当人们事先不知道分区的所有值时，因此从庞大的数据集中手动找到这些分区值是一项繁琐的任务。

### **15。场景:**

***假设，我创建一个包含 2016 年客户完成的所有交易明细的表:*** **创建表 transaction_details (cust_id INT，amount FLOAT，month STRING，country STRING)行格式分隔字段以'，'结尾；**

***现在，在这个表中插入 5 万个元组后，我想知道每个月产生的总收入。但是，Hive 在处理此查询时花费了太多时间。** **你将如何解决这个问题，并列出为此我将采取的步骤？***

我们可以通过按照每月对表进行分区来解决查询延迟的问题。因此，每个月我们将只扫描分区的数据，而不是整个数据集。

众所周知，我们不能直接对现有的未分区表进行分区。因此，我们将采取以下措施来解决这个问题:

1.  创建一个分区表，比如说 partitioned_transaction:

*创建表 PARTITIONED _ transaction(cust _ id INT，amount FLOAT，country STRING)PARTITIONED BY(month STRING)行格式分隔字段以'，'结尾；*

2。在配置单元中启用动态分区:

*设置 hive . exec . dynamic . partition = true；*

*设置 hive . exec . dynamic . partition . mode = non strict；*

3。将数据从非分区表转移到新创建的分区表:

*插入覆盖表 partitioned _ transaction PARTITION(month)从 transaction_details 中选择 cust_id，金额，国家，月份；*

现在，我们可以使用每个分区来执行查询，从而减少查询时间。

### **16。如何在上面的分区表中为十二月添加新的分区？**

为了在上面的 partitioned_transaction 表中添加一个新的分区，我们将发出下面给出的命令:

*ALTER TABLE partitioned _ transaction ADD PARTITION(month = ' Dec ')LOCATION '/partitioned _ transaction '；*

***注:*** 我建议你去看看关于 [***Hive 命令***](https://www.edureka.co/blog/hive-commands-with-examples) 的专门博客，在那里已经用一个例子解释了 Apache Hive 中出现的所有命令。

成为一名数据工程师的最佳途径是在德里 获得 [数据工程认证。](https://www.edureka.co/microsoft-azure-data-engineering-certification-course-delhi)

### **17。映射器/缩减器可以创建的默认最大动态分区是多少？你怎么能改变它？**

默认情况下，映射器或缩减器可以创建的最大分区数量设置为 100。可以通过发出下面的命令来改变它:

*设置 hive . exec . max . dynamic . partitions . pernode =<值>*

***注意:*** 可以使用:SET hive . exec . max . dynamic . partitions =<value>设置一条语句可以创建的动态分区总数

### **18。场景:**

***我正在基于分区动态地向一个表中插入数据。但是，我收到了一个错误——语义分析失败的错误:动态分区严格模式需要至少一个静态分区列。*** **你将如何消除这个错误？**

要消除此错误，必须执行以下命令:

*设置 hive . exec . dynamic . partition = true；*

*设置 hive . exec . dynamic . partition . mode = non strict；*

***事情要记住:***

*   默认情况下，如果您使用的是 0.9.0 之前版本的 hive，hive.exec.dynamic.partition 配置属性设置为 False。
*   hive . exec . dynamic . partition . mode 默认设置为 strict。只有在非严格模式下，Hive 才允许所有分区都是动态的。

### **19。为什么我们需要水桶？**

对一个分区进行存储有两个主要原因:

*   A***[map side join](https://www.edureka.co/blog/map-side-join-vs-join/)***要求属于唯一连接键的数据出现在同一个分区中。但是对于那些分区键和连接键不同的情况呢？因此，在这些情况下，您可以通过使用连接键对表进行分桶来执行映射端连接。
*   分桶使采样过程更加高效，因此，我们可以减少查询时间。

### **20。Hive 如何将行分布到桶中？**

Hive 通过使用公式确定行的桶号:*hash _ function(bucket ing _ column)modulo(num _ of _ buckets)*。这里，hash_function 依赖于列数据类型。对于整数数据类型，hash_function 将是:

*hash _ function(int _ type _ column)= int _ type _ column 的值*

### **21。如果你没有发出命令会发生什么:*' SET hive . enforce . bucket ing = true；'*在 Apache Hive 0.x 或 1.x 中的 Hive 中存储表之前？**

命令:*' SET hive . enforce . bucket ing = true；'*允许在使用' CLUSTER BY '子句对列进行分桶时拥有正确数量的 reducer。如果不这样做，人们可能会发现在表目录中生成的文件的数量不等于桶的数量。或者，也可以使用*set mapred . reduce . task = num _ bucket*将减速器的数量设置为等于铲斗的数量。

### **22。什么是索引，我们为什么需要它？**

Hive 查询优化方法之一是 Hive 索引。Hive 索引用于加速对 Hive 数据库中的一列或一组列的访问，因为使用索引，数据库系统不需要读取表中的所有行来查找用户选择的数据。

### **23。场景:**

***假设我有一个 CSV 文件——‘sample . CSV’存在于“/temp”目录下，条目如下:***

**id 名字姓氏邮箱性别 ip 地址**

1 休杰克曼 hughjackman@cam.ac.uk 男 136.90.241.52

2 大卫劳伦斯 dlawrence1@gmail.com 男 101.177.15.130

3 安迪·霍尔 andyhall2@yahoo.com 女 114.123.153.64

4 塞缪尔·杰克逊·samjackson231@sun.com 男 89.60.227.31

5 rose.emily4@surveymonkey.com 女 119.92.21.19 艾米丽·罗斯

***你将如何使用构建的 SerDe 将这个 CSV 文件消费到 Hive 仓库中？***

SerDe 代表串行器/解串器。SerDe 允许我们将非结构化的字节转换成可以使用 Hive 处理的记录。SerDes 是用 Java 实现的。Hive 自带了几个内置的 SerDes，也有很多其他第三方的 SerDes。

Hive 提供了一个特定的 SerDe 来处理 CSV 文件。我们可以通过发出以下命令将这个 SerDe 用于 sample . CSV:

*创建外部表样*

*(idint，first _ namestring，*

*姓氏 字符串 ， 邮箱 字符串 ，*

*性别 字符串 ， ip_address 字符串 )*

*行格式 SERDE' org . Apache . Hadoop . hive . SERDE 2 . opencsvserde '*

*存储为 TEXTFILE 位置'/temp '；*

现在，我们可以对表‘sample’执行任何查询:

*从性别=‘男’的样本中选择名字；*

### **24。场景:**

***假设，我在 HDFS 的/input 目录中有很多小的 CSV 文件，我想创建一个对应于这些文件的 Hive 表。这些文件中的数据格式为:{id，姓名，电子邮件，国家}。现在，正如我们所知，当我们使用大量小文件时，Hadoop 的性能会下降。***

***那么，如果我们想为大量小文件创建一个单独的 Hive 表，而又不降低系统的性能，你将如何解决这个问题呢？***

**通过** *[*蔚蓝数据工程认证*](https://www.edureka.co/microsoft-azure-data-engineering-certification-course)* **可以更好的理解。【T12**

可以使用序列文件格式，将这些小文件组合在一起，形成一个序列文件。这样做的步骤如下:

*   创建临时表:

*创建表 temp_table (id INT，姓名字符串，电子邮件字符串，国家字符串)*

*行格式字段以'，'分隔终止，存储为文本文件；*

*   将数据加载到 temp_table:

*将 PATH '/input '中的数据加载到表 temp_table 中；*

*   创建一个表格 th 一个 t 将以顺序文件格式存储数据:

*创建表格 sample _ seq file*(*id INT，姓名字符串，电子邮件字符串，国家字符串)*

*行格式字段以'，'结束，存储为 SEQUENCEFILE*

*   将数据从临时表转移到 sample_seqfile 表:

*插入覆盖表样 SELECT * FROM temp _ table*

因此，生成了一个包含所有输入文件中的数据的单个序列文件，因此，最终消除了拥有大量小文件的问题。

### **结论:**

我希望这篇关于 Apache Hive 面试问题的博客对你有所帮助。欢迎您查看我们的其他采访问题博客，这些博客涵盖了 Hadoop 框架中的所有组件。请参考下面的链接，享受阅读:

*   [***50 强 Hadoop 面试问题***](https://www.edureka.co/blog/interview-questions/top-50-hadoop-interview-questions-2016/)
*   [***Hadoop 集群面试题***](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-hadoop-cluster/)
*   **[*Hadoop HDFS 面试题*](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-hdfs-2/)**
*   [***Hadoop MapReduce 面试问题***](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-mapreduce/)
*   ***[猪面试问题](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-pig/)***
*   [***HBase 面试题***](https://www.edureka.co/blog/interview-questions/hbase-interview-questions/)

*有问题吗？请在 Apache Hive 面试问题的评论部分提到它，我们会回复您。*