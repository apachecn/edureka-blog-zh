# 带有 HQL 示例的顶级配置单元命令

> 原文：<https://www.edureka.co/blog/hive-commands-with-examples>

在这篇博文中，让我们用例子来讨论一下顶级的 Hive 命令。这些蜂巢命令对于 ***[蜂巢认证培训](https://www.edureka.co/big-data-and-hadoop)*** 设置基础非常重要。

Edureka 2019 Tech Career Guide is out! Hottest job roles, precise learning paths, industry outlook & more in the guide. [***Download*** ](http://bit.ly/2KmDS3b)now. 

## **什么是蜂巢？**

Apache Hive 是一个构建在 Hadoop 上的数据仓库系统。它用于查询和管理驻留在分布式存储中的大型数据集。在成为 Apache Hadoop 的开源项目之前，Hive 起源于脸书。它提供了一种机制，将结构投射到 Hadoop 中的数据上，并使用类似 SQL 的语言 HiveQL (HQL)查询该数据。

使用 Hive 是因为 Hive 中的表类似于关系数据库中的表。如果你熟悉 SQL，这是小菜一碟。许多用户可以使用 Hive-QL 同时查询数据。

## **什么是 HQL？**

Hive 定义了一种简单的类似 SQL 的查询语言来查询和管理大型数据集，称为 Hive-QL ( HQL)。如果你熟悉 SQL 语言，它很容易使用。Hive 允许熟悉该语言的程序员编写自定义 MapReduce 框架来执行更复杂的分析。

你甚至可以用班加罗尔 的 [Azure 数据工程认证查看大数据的细节。](https://www.edureka.co/microsoft-azure-data-engineering-certification-course-bangalore)

## **蜂巢的用途:**

1.阿帕奇蜂房分布式存储。

2.Hive 提供工具来实现简单的数据提取/转换/加载(ETL)

3.它提供了各种数据格式的结构。

4.通过使用 Hive，我们可以访问存储在 Hadoop 分布式文件系统(HDFS 用于查询和管理驻留在中的大型数据集)或其他数据存储系统(如 Apache HBase)中的文件。

## **蜂巢的局限性:**

Hive 不是为联机事务处理(OLTP)而设计的，它仅用于联机分析处理。

Hive 支持覆盖或理解数据，但不支持更新和删除。

在 Hive 中，不支持子查询。

## **为什么用蜂巢代替猪？**

以下是尽管有 Pig 供应，但仍使用 Hive 的原因:

*   Hive-QL 是一种声明性语言行 SQL，PigLatin 是一种数据流语言。
*   Pig:一种用于探索超大型数据集的数据流语言和环境。
*   Hive:分布式数据仓库。

## **蜂巢的组成:**

**Metastore :**

Hive 将 Hive 表的架构存储在 Hive Metastore 中。Metastore 用于保存仓库中有关表和分区的所有信息。缺省情况下，metastore 与 Hive 服务在同一个进程中运行，缺省 Metastore 是 DerBy 数据库。

**塞尔德:**

序列化程序、反序列化程序向 hive 提供如何处理记录的指令。

## **蜂巢命令:**

**数据定义语言(DDL )**

DDL 语句用于构建和修改数据库中的表和其他对象。

| **DDL 命令** | **功能** |
| **创建** | 它用于创建表或数据库 |
| **显示** | 它用于显示数据库、表格、属性等 |
| **改变** | 它用于对现有表进行更改 |
| **形容** | 它描述了表格列 |
| **截断** | 用于永久截断和删除表中的行 |
| **删除** | 删除表格数据，但是可以恢复 |

通过给出命令 sudo hive 转到 Hive shell 并输入命令**' create****database****<database****name>'**在 Hive 中创建新的数据库。

[![Create Hive database using Hive Commands](img/cf86f2218e426c095f1593940ad6abe9.png "Create Hive database using Hive Commands")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/201.png)

要列出 Hive warehouse 中的数据库，请输入命令' **show databases '。**

[![List Hive database using Hive Commands](img/7fed41aaac8f7e24741ffa4848fde592.png "List Hive database using Hive Commands")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/21-1.png)

数据库在配置单元仓库的默认位置创建。在 Cloudera 中，Hive 数据库存储在/user/hive/warehouse 中。

[![List Hive database using Hive Commands](img/a29657c90284a1dbdf7a7147324c91f5.png "List Hive database using Hive Commands")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/22-1.png)

使用数据库的命令是**使用<数据库名称>**

[![Hive command to use the database](img/ca81a6f0a5ba28a77e11d4d2844fdd1c.png "Hive command to use the database")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/23-1.png)

使用从本地复制命令将输入数据从本地复制到 HDFS。

[![ Input data in Hive](img/f17468636f1a15614d88264beda5efe9.png " Input data in Hive")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/24-1.png)

![Hive table](img/fcee02760cd4bf58a8d30db52db13f53.png "Hive table")

当我们在 hive 中创建一个表时，它在 hive 仓库的默认位置创建。–“/用户/配置单元/仓库”，在创建表之后，我们可以将数据从 HDFS 移动到配置单元表。

以下命令在“/user/hive/warehouse/retail.db”的位置创建一个表

*注意:* retail.db 是在蜂巢仓库中创建的数据库。

[![Creating Database in Hive Warehouse.](img/d1d3819aefe54544b361c7c268a4cf59.png "Creating Database in Hive Warehouse.")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/26-1.png)

**Describe** 提供关于表的模式的信息。

[![Describe - Hive Command](img/999596e1dcf7ec8b9cb660726450ad7e.png "Describe - Hive Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/27-1.png)

**数据操作语言(DML )**

DML 语句用于检索、存储、修改、删除、插入和更新数据库中的数据。

*举例:*

LOAD，INSERT 语句。

语法:

将路径`<file>`中的数据`<local>`加载到表【tablename】中

加载操作用于将数据移动到相应的配置单元表中。如果关键字 **local** 被指定，那么在 load 命令中会给出本地文件系统的路径。如果没有指定关键字 local，我们必须使用文件的 HDFS 路径。

[![DML statement - Load Command](img/79e42c30c64c773800e982799520955a.png "DML statement - Load Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/28-1.png)

[![DML statement - Load Command](img/b74fb633fedf6bac9395961ea05b1fac.png "DML statement - Load Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/29-1.png)

*以下是加载数据本地命令*的一些例子

[![DML statement - Load Command](img/fd5ccb48444f47fac0fb4f89dafdfddb.png "DML statement - Load Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/30-1.png)

[![DML statement - Load Command](img/84280a4403c95cd719f41d4c39de6d2b.png "DML statement - Load Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/311-1.png)

将数据加载到 Hive 表后，我们可以应用数据操作语句或聚合函数来检索数据。

*记录数计数示例:*

Count 聚合函数用于计算表中记录的总数。

[![Example to count number of records:](img/0d6bc9d62069fe9bafd134d8f0647285.png "Example to count number of records:")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/32-1.png)

**‘创建外部’表:**

**create external** 关键字用于创建一个表，并提供一个表创建的位置，这样 Hive 就不会使用这个表的默认位置。一个**外部**表指向其存储的任何 HDFS 位置，而不是默认存储。

[![Create External Command in Hive](img/0f1221602e5b4a6a223069c9328cfc55.png "Create External Command in Hive")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/33-1.png)

[![Create External Command in Hive](img/ddf05009346d5841c5ee7145321d9bd4.png "Create External Command in Hive")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/34-1.png)

**插入命令:**

**insert** 命令用于加载数据配置单元表。可以对表或分区进行插入。

INSERT OVERWRITE 用于覆盖表或分区中的现有数据。

INSERT INTO 用于将数据追加到表中的现有数据中。(注意:INSERT INTO 语法适用于 0.8 版本)

[![Insert Command](img/32b94a0811caee02c6302ab59e00f1ec.png "Insert Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/35-1.png)

[![Insert Command](img/1d56ffcc180e588437c2fa3863980dfc.png "Insert Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/36-1.png)

## **“分区依据”和“聚类依据”命令的例子 :**

由划分的**用于将表划分为分区，使用由**聚集的**命令可以将表划分为桶。**

[![Example for 'Partitioned By' and 'Clustered By' Command](img/a4afc3498943bfb7f57623aebb130fd1.png "Example for 'Partitioned By' and 'Clustered By' Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/37-1.png)

[![Example for 'Partitioned By' and 'Clustered By' Command](img/29fb8758a040bbf5580726e6998d6749.png "Example for 'Partitioned By' and 'Clustered By' Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/38-1.png)

当我们插入数据 Hive 抛出错误时，动态分区模式为严格，动态分区未启用(由 [杰夫](http://www.dresshead.com/dresshead-staff-profile-jeff-maurer/) 在 [dresshead 网站](http://www.dresshead.com) )。所以我们需要在 Hive shell 中设置以下参数。

set hive . exec . dynamic . partition = true；

要启用动态分区，默认情况下，它是 false

set hive . exec . dynamic . partition . mode = non strict；

[![Dynamic Partitions](img/407fd503f19d625aaa86f2059fa719a2.png "Dynamic Partitions")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/39-1.png)

[![Dynamic Partitions](img/814a88faa61a5199ea5e27e1ebcc3afe.png "Dynamic Partitions")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/40-1.png)

[![Dynamic Partitions](img/f1f13aee9d2fcf00654ad2f2de837f5e.png "Dynamic Partitions")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/41-1.png)

分区是按类别进行的，并且可以使用“Clustered By”命令划分为多个存储桶。

[![Partition](img/974201b7c795d07fdac84b5918c7f760.png "Partition")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/42-1.png)

“Drop Table”语句删除表的数据和元数据。对于外部表，只删除元数据。

[![Drop Table statement ](img/b225dd311491d18272b80f72d7356bbf.png "Drop Table statement ")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/43-1.png)

[![Drop Table statement ](img/72ec299780b93c1e2f763d9bf8160d1f.png "Drop Table statement ")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/44-1.png)

“Drop Table”语句删除表的数据和元数据。对于外部表，只删除元数据。

将本地路径中数据' aru.txt '加载到表 tablename 中，然后使用 Select * from table name 命令检查 employee1 表

[![To count the number of records in table by using Select count(*) from txnrecords;](img/ce53f6ef4034045de7a66e3c594debee.png "To count the number of records in table by using Select count(*) from txnrecords;")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/45-1.png)

使用 Select**count(*)**from txn records 计算表中的记录数；

[![To count the number of records in table by using Select count(*) from txnrecords;](img/a9162e40baf905a7a4e308e257273b72.png "To count the number of records in table by using Select count(*) from txnrecords;")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/46-1.png)

## **聚合:**

从表名中选择计数(不同类别)；

该命令将对不同类别的“cate”表进行计数。这里有 3 个不同的类别。

假设有另一个表 cate，其中 f1 是类别的字段名称。

[![ Count the different category of 'cate' table.](img/cd0f02506dec134e262ebfad9fe98c4e.png " Count the different category of 'cate' table.")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/47-1.png)

[![ Count the different category of 'cate' table.](img/ffbc5ce8dbed36ed2eb66ec346af8e7b.png " Count the different category of 'cate' table.")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/48-1.png)

## **分组:**

Group 命令用于按一列或多列对结果集进行分组。

从按类别分组的文本记录中选择类别、总和(金额)

它计算相同类别的数量。

[![Group command](img/295fb57544d1428a0a30f831cfb9d734.png "Group command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/49-11.png)

一个表的结果被存储到另一个表中。

将表 newtablename 创建为 select * from oldtablename

[![Group command](img/1e98b4052d0d6f77871994cd8166ae1c.png "Group command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/50-1.png)

## **加入命令:**

这里又创建了一个名为**‘mailid’**的表

[![Join Command](img/16bd5882cec29706789a28d3b5a9518a.png "Join Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/51-1.png)

[![Join Command](img/3b7b2afdc4fed91b0dbd594fe31d683b.png "Join Command")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/52-1.png)

## **加入操作** :

通过使用两个表中的公共值，执行连接操作来组合两个表中的字段。

[![Join Operation](img/0f10f2c9d7f60b04e0a23c2804112380.png "Join Operation")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/53-1.png)

## **左外接** :

表 A 和 B 的左外连接(或简单的左连接)的结果总是包含“左”表(A)的所有记录，即使连接条件在“右”表(B)中没有找到任何匹配的记录。

[![Left Outer Join](img/5c9125e74766c50b6b3a1b5837b3bc6d.png "Left Outer Join")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/54-1.png)

[![Left Outer Join](img/dfb75db93b577eb35824b1a7b1ebda39.png "Left Outer Join")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/55-1.png)

## **右外接** :

右外连接(或右连接)与左外连接非常相似，只是对表的处理相反。“右”表(B)中的每一行都将在连接表中至少出现一次。

[![Right Outer Join](img/e34083ffed41b706558150355ae2c46c.png "Right Outer Join")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/56-1.png)

[![Right Outer Join](img/fc4976a4deae6f6c3b3604ab7277656d.png "Right Outer Join")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/57-1.png)

## **完全加入** :

连接的表将包含两个表中的所有记录，并为任一侧缺失的匹配项填充空值。

[![Full Join](img/f87fd8c252463be790375c391bee2ad5.png "Full Join")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/58-1.png)

[![Top Hive Commands with Examples in HQL](img/da9fe7227a5d1cb6fb148feba4a99d95.png "Full Join")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/59-1.png)

完成配置单元后，我们可以使用 quit 命令退出配置单元外壳。

[![Exiting from Hive](img/535b8c16bf0f4b0ae643d9439fd5db26.png "Exiting from Hive")](https://cdn.edureka.co/blog/wp-content/uploads/2014/03/60-1.png)

Hive 只是被称为大数据和 Hadoop 的大拼图的一部分。Hadoop 不仅仅是 Hive。点击下面，看看你在 Hadoop 中还应该掌握哪些技能。你甚至可以通过 [数据工程师课程](https://www.edureka.co/microsoft-azure-data-engineering-certification-course) 了解大数据的细节。

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[大数据培训可以改变组织的 7 种方式](https://www.edureka.co/blog/7-ways-big-data-training-can-change-your-organization/)

[大数据入门& Hadoop](https://www.edureka.co/big-data-and-hadoop)

[蜂巢数据模型](https://www.edureka.co/blog/hive-data-models/)