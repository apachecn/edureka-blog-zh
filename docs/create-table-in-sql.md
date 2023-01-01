# 在 SQL 中创建表——关于在 SQL 中创建表你需要知道的一切

> 原文：<https://www.edureka.co/blog/create-table-in-sql/>

SQL 或[结构化查询语言](https://www.edureka.co/blog/sql-commands)由各种处理关系数据库的命令组成。这些命令分为不同的类别，如 DDL、DML、DCL 和 TCL。其中一个重要的查询是来自 DDL 命令的 CREATE Table 查询。因此，在这篇关于用 SQL 创建表的文章中，您将按以下顺序学习 Create Table 语句:

![SQL - Create Table in SQL - Edureka](img/da752ce4512e8070f2ce0a64cdf669c5.png)

## **什么是创建表查询？**

**create table 语句**用于为您正在使用的数据库创建一个表。根据需要，该表可以有 n 行和 m 列。因此，在这个查询的帮助下，您基本上可以以行和列的形式存储数据。

接下来，在这篇关于用 SQL 创建表的文章中，让我们看看 create 语句的语法。

## **创建表格语法**

CREATE TABLE 语句的语法如下:

```
CREATE TABLE tablename (
column1 data type,
column2 data type,
column3 data type,
column4 data type,
....
columnN data type);

```

在这里，列参数表示要包含在表中的列的名称。类似地，[数据类型参数](https://www.edureka.co/blog/sql-data-types/)表示数据列可以存储的类型。例如:字符、整数、日期、varchar 等。

### **举例:**

```
CREATE TABLE students (
studentID int,
studentname varchar(255),
parentname varchar(255),
address varchar(255),
phonenumber int
);

```

### **输出:**

| **studentID** | **学生名称** | **parentname** | **地址** | **电话号码** |

现在，一旦创建了表，就可以使用[插入查询](https://www.edureka.co/blog/insert-query-sql/)将值插入表中。 但是，如果您必须使用另一个现有的表来创建一个表呢？你会怎么做？

因此，接下来，在这篇关于在 SQL 中创建表的文章中，让我们来看看同样的内容。

## 如何使用另一个表格创建表格？

要从现有的表中创建另一个表，必须使用以下语法:

```
CREATE TABLE newtablename AS
SELECT column1, column2,..., columnN
FROM existingtablename
WHERE ....;

```

在这里，您试图从一个现有的表中创建一个新表。此外，您可以根据条件从现有的表中选择所需的列。但是，提及条件不是强制性的。

### **举例:**

```
CREATE TABLE sampletable AS
SELECT studentID, studentname
FROM students;

```

### **输出:**

| **studentID** | **学生名称** |

**注:** 新表的列定义与旧表相同。此外，如果您的现有表存储了任何值，那么新表将自动填充这些值。

到此，我们结束这篇文章。我希望你明白，如何使用 SQL 创建表。 *如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在这篇文章的评论部分提到它，我会回复你。*