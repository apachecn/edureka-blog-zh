# SQL 教程:学习 SQL 的一站式解决方案

> 原文：<https://www.edureka.co/blog/sql-tutorial/>

在今天的市场中，每天都会产生大约 2.5 万亿字节的数据，了解如何处理如此庞大的数据量非常重要。这就是结构化查询语言或 SQL 的用武之地。因此，在这篇关于 SQL 教程的文章中，我将讨论以下重要概念，它们是成为一名数据库管理员的必经之路。

*   [SQL 简介](#sql)
    1.  [什么是 SQL？](#whatissql)
    2.  [SQL 的应用](#applications)
    3.  [SQL 数据类型](#datatypes)
    4.  [SQL 运算符](#operators)
*   [顶级 SQL 命令](#sqlcommands)
    1.  [创造](#create)
    2.  [下降](#drop)
    3.  [改变](#alter)
    4.  [截断](#truncate)
    5.  [解释](#explain)
    6.  [插入](#insertinto)
    7.  [更新](#update)
    8.  [选择](#select)
    9.  [喜欢](#like)
    10.  [授予](#grant)
*   [数据库中的密钥](#sqlkeys)
*   [SQL 约束](#sqlconstraints)
*   [归一化](#normalization)
*   [SQL 连接](#sqljoins)
*   [视图](#sqlviews)

## **SQL 教程:SQL 简介**

### **什么是 SQL？**

由 Donald D.Chamberlin 在 20 世纪 70 年代开发的结构化查询语言(通常称为 SQL)是用于从关系数据库操纵、存储、更新和检索数据的最流行的语言之一。SQL 由分为 4 类的各种命令组成，即 DDL、DML、DCL 和 TCL，用于处理数据库中的数据。同样，关系数据库如 [MySQL 数据库](https://www.mysql.com/)、 [Oracle](https://www.edureka.co/blog/interview-questions/top-50-oracle-interview-and-answers/) 、MS SQL Server、Sybase 等使用 SQL 来修改数据。

### **SQL 的应用**

SQL 的应用如下:

*   使用 SQL，您可以创建和删除表和数据库。
*   它允许用户定义和操作数据库中的数据。
*   SQL 允许用户访问、修改和描述 RDBMS 中的数据。
*   使用 SQL，您可以设置表、视图和过程的权限，并向不同的用户授予特定的权限。
*   SQL 允许您使用 SQL 库和模块嵌入到其他语言中。

现在你已经知道了 SQL 的[基础知识，接下来在这个 SQL 教程中，让我们了解什么是不同的 SQL 数据类型。](https://www.edureka.co/blog/sql-basics/)

### **SQL 数据类型**

SQL 数据类型分为以下几类:

*   **数字**–数字数据类型允许有符号和无符号整数。它们可以进一步分为精确数据类型和近似数据类型，其中精确数据类型允许整数形式的整数，近似数据类型允许浮点数形式的整数。
*   **字符串**–该数据类型允许固定和可变长度的字符。这种数据类型还可以进一步分为 Unicode 字符，允许 Unicode 字符的固定长度和可变长度。
*   **二进制**–二进制数据类型允许数据以固定和可变长度的二进制值格式存储。
*   **日期&时间**–T他的数据类型允许数据以不同的日期和时间格式存储。
*   **其他**——该段数据类型有表格、XML、游标、 uniqueidentifier、sql_variant 等数据类型。

如果您希望详细了解不同的 SQL 数据类型，您可以参考关于 [SQL 数据类型的详细指南。](https://www.edureka.co/blog/sql-data-types/)

### **SQL 运算符**

运算符是可以操作操作数值的结构。考虑表达式 4 + 6 = 10，这里 4 和 6 是操作数，+称为运算符。

SQL 支持以下类型的运算符:

*   算术运算符
*   按位运算符
*   比较运算符
*   复合运算符
*   逻辑运算符

要详细了解 SQL 支持的不同操作符，可以[点击这里](https://www.edureka.co/blog/sql-commands#Operators)。现在你已经知道了什么是 SQL 及其基础知识，让我们了解一下 SQL 中最常用的命令或语句。

## **SQL 教程:顶级 SQL 命令**

SQL 由各种命令或语句组成，用于添加、修改、删除或更新数据库中的数据。在这篇关于 SQL 教程的文章中，我们将讨论以下语句:

在本 SQL 教程中，我将以下面的数据库 为例，向您展示如何使用这些 SQL 命令编写 查询。

| **客户 ID** | **客户名称** | **电话号码** | **地址** | **城市** | **国家** |
| one | 西蒙 | Nine billion eight hundred and seventy-six million five hundred and forty-three thousand two hundred and ten | 唐纳德街 52 号 | 海得拉巴 | 印度 |
| Two | 阿卡什 | Nine billion nine hundred and fifty-five million four hundred and forty-nine thousand nine hundred and twenty-two | 皇后大道 74 号 | 孟买 | 印度 |
| three | 帕特里克(男子名) | Nine billion nine hundred and fifty-five million eight hundred and eighty-eight thousand two hundred and twenty | 丝绸板 82 | 德里 | 印度 |
| four | 萨米尔 | Nine billion six hundred and forty-seven million nine hundred and seventy-four thousand three hundred and twenty-seven | IG 路 19 号 | 海得拉巴 | 印度 |
| five | 约翰 | Nine billion six hundred and seventy-four million three hundred and twenty-five thousand six hundred and eighty-nine | 大队路第九街区 | 班加罗尔 | 印度 |

### **创建**

[CREATE 语句](https://www.edureka.co/blog/create-table-in-sql/)用于以如下方式创建表格、视图或数据库:

#### **创建数据库**

用于创建数据库。

#### **语法**

```
CREATE DATABASE DatabaseName;

```

#### **例如**

```

CREATE DATABASE CustomerInfo; 

```

#### **创建表格**

该语句用于创建表。

#### **语法**

```
CREATE TABLE TableName (
Column1 data type,
Column2 data type,
....

ColumnN data type
);

```

#### **例如**

```

CREATE TABLE Customers
(
CustomerID int,
CustomerName varchar(255),
PhoneNumber int,
Address varchar(255),
City varchar(255),
Country varchar(255)
);

```

#### **创建视图**

用于创建视图。

#### **语法**

```
CREATE VIEW OR REPLACE ViewName AS
SELECT Column1, Column2, ..., ColumnN
FROM TableName
WHERE Condition;

```

#### **例如**

```
CREATE VIEW OR REPLACE HydCustomers AS
SELECT CustomerName, PhoneNumber
FROM Customers
WHERE City = "Hyderabad";

```

**注意:**在开始创建表和输入值之前，您必须使用数据库，使用 use 语句作为[ **使用 CustomersInfo** ]

**下降**

DROP 语句用于删除现有的表、视图或数据库。

#### **删除数据库**

用于删除数据库。使用此语句时，数据库中的所有信息都将丢失。

#### **语法**

```
DROP DATABASE DatabaseName;

```

#### **例子**

```
DROP DATABASE CustomerInfo;

```

#### **下降表**

用来摔桌子。使用此语句时，表中的完整信息将会丢失。

#### **语法**

```
DROP TABLE TableName;

```

#### **例子**

```
DROP TABLE Customers;

```

#### **下拉视图**

用于删除视图。使用此语句时，视图中的完整信息将会丢失。

#### **语法**

```
DROP VIEW ViewName;

```

#### **例子**

```
DROP VIEW HydCustomers;

```

### **改变**

ALTER 语句用于添加、删除或修改现有表中的约束或列。

#### **更改表格**

[ALTER 语句](https://www.edureka.co/blog/alter-table/)用于删除、添加、修改现有表中的列。您可以使用 ALTER TABLE with ADD/ DROP column 在表中添加或删除列。除此之外，您还可以更改/修改特定的列。

#### **语法**

```
ALTER TABLE TableName
ADD ColumnName Data Type;
ALTER TABLE TableName
DROP COLUMN ColumnName;

ALTER TABLE TableName
ALTER COLUMN ColumnName Data Type;

```

#### **例题**

```
--ADD Column Gender:
 ALTER TABLE Customers
ADD  Gender varchar(255);

--DROP Column Gender: 
ALTER TABLE Customers
DROP COLUMN Gender ;

--Add a column DOB and change the data type from Date to Year.

ALTER TABLE DOB
ADD DOB date;

ALTER TABLE DOB
ALTER DOB year;

```

### **截断**

TRUNCATE 语句用于删除表中的信息，而不是表本身。因此，一旦您使用这个命令，您的信息将会丢失，但不是表将仍然存在于数据库中。

#### **语法**

```
TRUNCATE TABLE TableName;

```

#### **例子**

```
TRUNCATE Table Customers;

```

### **解释**

EXPLAIN 和 DESCRIBE 语句是同义词，分别用于获取查询执行计划和关于表结构的信息。该语句可以与 INSERT、DELETE、SELECT、UPDATE 和 REPLACE 语句一起使用。

#### **语法**

```
--Syntax for DESCRIBE
DESCRIBE TableName;

--Sample syntax for EXPLAIN
EXPLAIN ANALYZE SELECT * FROM TableName1 JOIN TableName2 ON (TableName1.ColumnName1 = TableName2.ColumnName2);

```

#### **例题**

```
DESCRIBE Customers;

EXPLAIN ANALYZE SELECT * FROM Customers1 JOIN Orders ON (Customers.CustomerID = Orders.CustomerID);

```

### **插入**

[INSERT INTO 语句](https://www.edureka.co/blog/insert-query-sql/)用于向表中插入新记录。

#### **语法**

```
INSERT INTO TableName (Column1, Column2, Column3, ...,ColumnN)
VALUES (value1, value2, value3, ...);

--If you do not want to mention the column names then use the below syntax, but the order of values entered should match the column data types :

INSERT INTO TableName
VALUES (Value1, Value2, Value3, ...);

```

#### **例题**

```
INSERT INTO Customers(CustomerID, CustomerName, PhoneNumber, Address, City, Country)
VALUES ('06', 'Sanjana', '9654323491', 'Oxford Street House No 10', 'Bengaluru', 'India');

INSERT INTO Customers
VALUES ('07', 'Himani','9858018368', 'Nice Road 42', 'Kolkata', 'India');

```

### **更新**

UPDATE 语句用于修改表中已经存在的记录。

#### **语法**

```
UPDATE TableName
SET Column1 = Value1, Column2 = Value2, ...
WHERE Condition;

```

#### **例题**

```
UPDATE Customers
SET CustomerName = 'Aisha', City= 'Kolkata'
WHERE EmployeeID = 2;

```

### **选择**

SELECT 语句用于从数据库中选择数据并存储在结果表中，称为 **结果集** 。

#### **语法**

```
SELECT Column1, Column2, ...ColumN
FROM TableName;

--(*) is used to select all from the table
SELECT * FROM table_name;

-- To select the number of records to return use:
SELECT TOP 3 * FROM TableName;

```

#### **例题**

```
SELECT CustomerID, CustomerName
FROM Customers;

--(*) is used to select all from the table
SELECT * FROM Customers;

-- To select the number of records to return use:
SELECT TOP 3 * FROM Customers;

```

除此之外，你还可以用 SELECT 关键字与， [区别开来，顺序由](https://www.edureka.co/blog/order-by-in-sql)， [分组由](https://www.edureka.co/blog/sql-commands#GROUP%20BY)， [HAVING 子句](https://www.edureka.co/blog/sql-commands#HAVING%20Clause)， [变成](https://www.edureka.co/blog/sql-commands#INTO)。

### **喜欢**

该操作符与 WHERE 子句一起使用，在表格的一列中搜索指定的模式。与类似操作符的[一起使用的通配符主要有两个:](https://www.edureka.co/blog/like-in-sql/)

*   **%**–匹配 0 个或多个字符。
*   **_**–只匹配一个字符。

#### **语法**

```
SELECT ColumnName(s)
FROM TableName
WHERE ColumnName LIKE pattern;

```

#### **例题**

```
SELECT * FROM Customers
WHERE CustomerName LIKE 'S%';

```

### **授予**

GRANT 命令用于向用户提供数据库及其对象的特权或访问权。

#### **语法**

```
GRANT PrivilegeName
ON ObjectName
TO {UserName |PUBLIC |RoleName}
[WITH GRANT OPTION];

```

在哪里，

*   **PrivilegeName**–授予用户的特权/权限/访问权。
*   **object Name**–表/视图/存储过程等数据库对象的名称。
*   **用户名**–被授予访问/权限/特权的用户的名称。
*   **公共**–授予所有用户访问权限。
*   **RoleName**–一组特权的名称。
*   **带授予选项**–赋予用户访问权限，授予其他用户权限。

#### **例题**

```
-- To grant SELECT permission to Customers table to admin
GRANT SELECT ON Customers TO admin;

```

现在您已经知道了[顶级 SQL 命令](https://www.edureka.co/blog/sql-commands)，让我们了解一下数据库中使用的不同类型的键。这个概念将帮助您理解在关系数据库管理系统中，每个表是如何与其他表相关联的。

## **SQL 教程:键**

以下是数据库中可以考虑的 7 种关键字:

*   **候选关键字—**可以唯一标识一个表的一组属性可以称为候选关键字。一个表可以有多个候选键，在选择的候选键中，可以选择一个键作为主键。
*   **超级键——**能够唯一标识一个元组的属性集合称为超级键。因此，候选键、主键和唯一键是超级键，但反之亦然。
*   **[主键](https://www.edureka.co/blog/primary-key-in-sql/)–**用来唯一标识每个元组的一组属性也是主键。
*   **备用键—**备用键是候选键，不会被选为主键。
*   **唯一键【T1—**唯一键类似于主键，但在列中允许有一个空值。
*   **[外键](https://www.edureka.co/blog/foreign-key-sql/)–**一个只能将当前值作为某个其他属性的值的属性，是它所引用的属性的外键。
*   **组合键【T1—**组合键是两列或更多列的组合，唯一标识每个元组。

我希望你已经理解了数据库中不同类型的键，接下来在这篇关于 SQL 教程的文章中，让我们讨论一下数据库中的约束。嗯，SQL 约束用于增加通过表格进入数据库的数据的准确性和可靠性。

## **SQL 教程:** **约束**

SQL 约束确保在数据交易方面没有违规，如果发现违规，将终止操作。以下约束的主要用途是限制 可以放入表中的数据类型。

*   **NOT NULL**–这个约束用于确保一个列不能存储空值。
*   **UNIQUE**–UNIQUE 约束用于确保在列或表中输入的所有值都是唯一的。
*   **CHECK**–该约束用于确保一列或多列满足特定条件。
*   **DEFAULT**–如果没有指定值，默认约束用于设置列的默认值。
*   **INDEX**–该约束用于表中的索引，通过该索引，您可以非常快速地从数据库中创建和检索数据。

如果你想深入了解以下约束的语法和例子，可以参考其他关于 SQL 的[文章。](https://www.edureka.co/blog/sql-commands#NOT%20NULL)既然您已经了解了数据库中的键和约束，接下来在这篇 SQL 教程中，让我们来看看一个有趣的概念规范化。

## **SQL 教程:规范化**

标准化是组织数据以避免重复和冗余的过程。规范化有许多连续的级别，这些级别被称为 **范式** 。而且，每个连续的范式都依赖于前一个范式。以下是常见的形式:

![Normalization - SQL Tutorial - Edureka](img/8a51a4518d2683ffd0ae3736f71563ac.png)为了理解上述范式，让我们考虑下表:

![Normalization Example - SQL Tutorial - Edureka](img/93f174113ecef469b2b0735e3df429d2.png)

通过观察上表，你可以清楚地看出数据冗余和数据重复。所以，让我们把这个表归一化。要开始规范化数据库，您应该始终从最低范式(即 1NF)开始，然后最终走向更高范式。

现在，让我们看看如何对上表执行第一个范式。

### **第一范式(1NF)**

为了确保数据库必须在 **1NF** 中，每个表格单元格应该有一个单独的值。所以，基本上所有的**记录必须是唯一的**。上表将被归一化为 1NF，如下所示:

![First Normal Form - SQL Tutorial - Edureka](img/75cf4add6ffbb70c350714761255ed60.png)

如果观察上表，所有的记录都是唯一的。但是，仍然存在大量的数据冗余和重复。因此，为了避免这种情况，让我们将数据库规范化为第二范式。

### **第二范式(2NF)**

为了确保数据库必须在 **2NF** 中，**数据库应该是 1NF** 并且**也应该有单列主键**。上表将被归一化为 2NF，如下所示:

![Second Normal Form - SQL Tutorial - Edureka](img/68ef74e7cb07b2afe727c2df6e5b5b11.png)

如果观察上面的表，每个表都有一个单列主键。但是有许多数据冗余和少数几列的重复。为了避免这种情况，让我们将数据库规范化为第三范式。

### **第三范式(3NF)**

为了确保数据库必须在 **3NF** 中，**数据库应该在 2NF** 中，**不能有任何可传递的函数依赖**。上述表格将被归一化为 3NF，如下所示:

![Third Normal Form - SQL Tutorial - Edureka](img/4bd13f748d7b5da3522bce4798291d97.png)如果你观察上面的表，数据库没有任何传递依赖。因此，在这一步之后，我们不必进一步规范化我们的数据库。但是，如果您看到任何异常或不止一个候选关键字，那么您可以使用下一个更高的范式，即 BCNF。

### **博伊斯-科德范式(BCNF)**

要确保数据库必须在 BCNF，数据库必须在 3NF 中，表必须进一步划分，以确保只有一个候选键。

这样，我们就结束了正常化。现在，在本 SQL 教程中，让我们讨论 SQL 中的一个重要概念，即连接。

## **SQL 教程:连接**

联接用于根据两个或多个表之间的相关列以及一些条件来组合这些表中的行。主要有四种类型的连接:

*   **内部连接:**该连接返回那些在两个表中都有匹配值的记录。
*   **完全连接:**完全连接返回在左表或右表中匹配的所有记录。
*   **左连接:**该连接返回左表中的记录，以及右表中满足条件的记录。
*   **右连接:**该连接返回右表中的记录，以及左表中满足条件的记录。

所以，这是一个关于连接的简短描述，但是如果你想要一个关于连接的详细描述和一个详细的例子，你可以参考我关于 [SQL 连接](https://www.edureka.co/blog/sql-joins-types)的文章。接下来，在本 SQL 教程中，让我们讨论本文的最后一个概念，即视图。

## **SQL 教程:视图**

SQL 中的视图是从其他表派生的单个表。视图包含类似于真实表的行和列，并且具有来自一个或多个表的字段。参考下图:

![Views - SQL Tutorial - Edureka](img/f3ae2631fa7cac13f0d4c35ddc1cb740.png)

要理解如何创建和删除视图，可以参考上面提到的 create 和 drop 语句。至此，我们结束了这篇关于 SQL 教程的文章。我希望你发现这篇文章信息丰富。此外，如果您正在准备数据库管理员面试，并且正在搜索问题的综合列表，您可以参考我们关于 [SQL 面试问题的文章。](https://www.edureka.co/blog/interview-questions/sql-interview-questions)

如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，那么请查看我们的 [MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)，该培训包含讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。

有问题要问我们吗？请在本指南的评论部分提及，我们将会回复您。