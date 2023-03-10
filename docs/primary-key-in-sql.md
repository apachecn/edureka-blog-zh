# SQL 中的主键:关于主键操作你需要知道的一切

> 原文：<https://www.edureka.co/blog/primary-key-in-sql/>

在一个每天产生 2.5 万亿字节数据的时代 ，以适当的方式处理数据并识别唯一的记录非常重要。因此，在这篇关于 [SQL](https://www.edureka.co/blog/sql-commands/) 中主键的文章中，我将讨论当存在关系数据库时，如何惟一地标识表中的每条记录。

本文将涵盖以下主题:

1.  什么是主键？
2.  [主键规则](#RulesforPrimaryKey)
3.  [主键操作:](#PrimaryKeyOperations)
    *   [创建表上的主键](#PrimaryKeyonCreateTable)
    *   [变更表上的主键](#PrimaryKeyonAlterTable)
    *   [删除主键](#DropPrimaryKey)

## **什么是 SQL 中的主键？**

主键约束是一种键，通过它可以唯一地标识表中的每个元组或记录。每个表只能有一个主键，但可以有多个[候选键](https://www.edureka.co/blog/sql-commands/#Keys%20In%20Database)。此外，每个主键都应该是唯一的，并且不能包含任何空值。

主键与外键一起用来引用各种表，形成引用完整性。对于表 A，主键可以由一列或多列组成。

既然你知道什么是主键，接下来在这篇关于主键的文章中 [SQL](https://www.edureka.co/blog/sql-commands/) ，让我们了解主键的规则。

## **主键规则**

主键的规则如下:

1.  选择作为主键的列中的所有值必须是唯一的。
2.  每个表只能有一个主键
3.  主键列中没有值可以为空
4.  您不能插入具有预先存在的主键的新行

现在你已经知道了主键的规则，接下来在这篇关于 SQL 主键的文章中，让我们看看主键的操作。

## **主键操作:**

为了理解主键上存在的各种操作，考虑下表:

### **客户表:**

| **客户 ID** | **客户名称** | **电话号码** |
| one | rohit！rohit | 9876543210 |
| Two | 声音的 | 9765434567 |
| three | 阿贾伊 | 9765234562 |
| four | 艾什瓦里亚 | 9876567899 |
| five | 阿卡什 | 9876541236 |

### **创建表上的主键**

在创建该表时，可以使用以下语法在“customerID”列上创建主键:

```

#For SQL Server/ MS Access/ Oracle
CREATE TABLE Customers (
CustomerID int NOT NULL PRIMARY KEY,
CustomerName varchar(255) NOT NULL,
PhoneNumber int
);
#MySQL
CREATE TABLE Customers (
CustomerID int NOT NULL,
CustomerName varchar(255) NOT NULL,
PhoneNumber int
PRIMARY KEY (customerID)
);

```

#### **在多个列上应用主键**

在 [创建表](https://www.edureka.co/blog/create-table-in-sql/) 时，要在多列上应用主键，参见下面的例子:

```
CREATE TABLE Customers (
customerID int NOT NULL,
CustomerName varchar(255) NOT NULL,
PhoneNumber int,
CONSTRAINT PK_Customer PRIMARY KEY (CustomerID,CustomerName)
);

```

参考下图。

![Primary Key - Primary Key in SQL - Edureka](img/d5dbbbf51329c32793694a8334067ce1.png)

接下来，在这篇关于 SQL 主键的文章中，让我们看看如何在 Alter Table 上使用主键。

### **变更表上的主键**

当已经创建了“customers”表，并且您只想改变该表时，您可以使用以下语法在“customerID”列上创建主键:

```
ALTER TABLE Customers
ADD PRIMARY KEY (CustomerID);

```

如果要为主键约束添加一个名称，并在多个列上定义它，请使用以下 SQL 语法:

```
ALTER TABLE Customers
ADD CONSTRAINT PK_Customer PRIMARY KEY (CustomerID,CustomerName);

```

接下来，在这篇关于 SQL 主键的文章中，让我们了解如何删除主键

### **删除/丢弃主键**

要删除主键，可以参考下面的例子:

```
#For SQL Server/ MS Access/ Oracle
ALTER TABLE Customers
DROP CONSTRAINT PK_Customer;
#For MySQL
ALTER TABLE Customers
DROP PRIMARY KEY;

```

到此，我们结束这篇文章。我希望您理解了如何在 SQL 中使用主键。 *如果您希望了解更多关于*[*MySQL*](https://www.edureka.co/blog/what-is-mysql/)*并了解这个开源关系数据库，那么请查看我们的*[*MySQL DBA 认证培训*](https://www.edureka.co/mysql-dba) *，它附带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在“SQL 中的主键”这篇文章的评论部分提到它，我会回复您。*