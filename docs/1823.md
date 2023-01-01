# 如何在 SQL 中重命名列名？

> 原文：<https://www.edureka.co/blog/rename-column/>

我们经常会看到需要更改数据库中列的名称来满足自己的需求。借助于 [SQL](https://www.edureka.co/blog/sql-tutorial/) 或结构化查询语言，[数据库管理员](https://www.edureka.co/sql-essentials-training) 在关系数据库中存储、更新、操作和检索数据。因此，在本文中，让我们了解如何在 SQL 中重命名列名。

本文将涉及以下主题:

那么让我们开始吧，

## **什么是 SQL？**

SQL 是一种用于管理和访问数据库的结构化查询语言。它以英语为基础，旨在方便检索、操作和访问数据。如果你想深入了解 SQL 基础知识，可以参考[关于 SQL 基础知识的文章](https://www.edureka.co/blog/sql-basics/)。 在 SQL 中，有各种用于操作数据的语句/命令。在数据库中非常流行的一种操作是在 SQL 中重命名列名。

那么，让我们了解一下如何在 SQL 中使用 RENAME 命令。

## **SQL 中的重命名命令是什么？**

该命令用于将一个列名改为一个新的列名。它还用于将表更改为新的表名。 让我们了解如何在不同的数据库中使用该命令。但是，在此之前，让我们考虑一下下表来理解所有的例子:

| **投标** | **BName** | 型 | **价格** |
| 1 | 魔术镜 | 心理学 | 200 |
| 2 | 黛西·琼斯 | 谜团 | 350 |
| 3 | 湖里的女人 | 谜团 | 250 |
| 4 | 奇迹溪 | 惊悚片 | 第 450 章 |
| 5 | 消失的地球 | 剧情 | 300 |

## **如何在 SQL 中重命名列名？**

## **在 MySQL、MariaDB、Oracle 和 PostgreSQL 中重命名列名**

要重命名 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 、MariaDB、Oracle 和 [PostgreSQL](https://www.edureka.co/blog/postgresql-tutorial) 中的列名，可以遵循下面的语法:

### **语法**

```
ALTER TABLE TableName
RENAME COLUMN OldColumnName TO NewColumnName;

```

### **举例:**

编写一个查询，将列名“BID”重命名为“BooksID”。

```
ALTER TABLE Books;
RENAME COLUMN BID TO BooksID;

```

在执行上述查询时，您将看到以下输出:

### **输出:**

| **BooksID** | **BName** | 型 | **价格** |
| 1 | 魔术镜 | 心理学 | 200 |
| 2 | 黛西·琼斯 | 谜团 | 350 |
| 3 | 湖里的女人 | 谜团 | 250 |
| 4 | 奇迹溪 | 惊悚片 | 第 450 章 |
| 5 | 消失的地球 | 剧情 | 300 |

您也可以使用**更改关键字**来重命名列名，如下:

### **语法**

```
ALTER TABLE TableName
CHANGE COLUMN OldColumnName NewColumnName Data Type;

```

### **举例:**

编写一个查询，将列名“BID”重命名为“BooksID”。

```
ALTER TABLE Books;
CHANGE COLUMN BID BooksID INT;

```

在执行这个查询时，您将看到与上面的输出相同的输出。

## **在 MS SQL Server 中重命名列名**

与其他数据库相比，MS SQL Server 的列名重命名过程有所不同。在 MS SQL Server 中，你必须使用 名为 **的 sp_rename 存储过程。**

### **语法**

```
sp_rename 'TableName.OldColumnName', 'New ColumnName', 'COLUMN';

```

### **举例:**

编写一个查询，将列名“BID”重命名为“BooksID”。

```
sp_rename 'Books.BID', 'BooksID', 'COLUMN';

```

结果输出将与上述查询的结果相同。 现在，您已经了解了如何在各种数据库中重命名列名，让我们看看如何重命名表名。

## **重命名表名 MySQL，MariaDB，Oracle**

要重命名表名，可以使用 SQL 中的 rename 命令，方式如下:

### **语法:**

```
ALTER TABLE OldTableName
RENAME TO NewTableName;

```

### **举例:**

```
ALTER TABLE Books
RENAME TO ListOfBooks;

```

现在，如果您执行以下查询来查看表 ListOfBooks 中的详细信息，您将看到以下输出:

**查询:**

```
SELECT * FROM ListOfBooks;

```

| **BooksID** | **BName** | 型 | **价格** |
| 1 | 棘手的镜子 | 心理学 | 200 |
| 2 | 黛西·琼斯 | 谜团 | 350 |
| 3 | 湖里的女人 | 谜团 | 250 |
| 4 | 奇迹溪 | 惊悚片 | 第 450 章 |
| 5 | 消失的地球 | 剧情 | 300 |

至此，我们结束了这篇关于在 SQL 中重命名列名的文章。我希望你发现这篇文章信息丰富。 我希望你明白如何使用上面的命令。 *如果您希望了解更多关于*[*MySQL*](https://www.edureka.co/blog/what-is-mysql/)*并了解这个开源关系数据库，那么请查看我们的*[*MySQL DBA 认证培训*](https://www.edureka.co/mysql-dba) *，它附带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在本文“在 SQL 中重命名列名”的评论部分提到它，我会尽快回复您。*