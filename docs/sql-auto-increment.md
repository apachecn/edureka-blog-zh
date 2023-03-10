# 如何在 SQL 中使用自动增量？

> 原文：<https://www.edureka.co/blog/sql-auto-increment/>

众所周知，数据库以逻辑格式存储海量数据。但是，您有没有想过这样一种情况，在这种情况下，您必须为表中的每个新记录提供一个唯一的编号？嗯，我认为，手动输入数字实际上是不可能的。因此，相反，您可以在 [SQL](https://www.edureka.co/blog/sql-data-types/) 中使用 Auto Increment，为表中的每个新记录自动输入一个惟一的数字。

本文将涉及以下主题:

1.  [什么是 SQL 中的自动增量？](#autoincrement)
2.  [如何设置自动增量？](#syntaxandexample)

## **什么是 SQL 中的自动增量？**

我确信这个名字本身就暗示了它的功能。自动增量是一个字段，用于为添加到表中的每个新记录生成一个唯一的编号。 这通常用于[主键列](https://www.edureka.co/blog/primary-key-in-sql/)，因为开发人员很容易为每个新记录自动生成一个唯一的编号。

现在，你知道了什么是 SQL 中的自动增量，让我们讨论一下如何在各种数据库管理系统中使用这个字段。

## 如何设置自动增量？

为了让您更好地理解，我将考虑下表:

| **客户 ID** | **客户名称** | **年龄** | **电话号码** |

如果你想知道如何创建一个表格，你可以参考我关于[创建表格命令](https://www.edureka.co/blog/create-table-in-sql/)的文章。。让我们从不同 DBMS 中的自动增量字段的语法和示例开始。

### **SQL Server 的语法和示例**

要使用自动增量字段，在 SQL Server 中，你必须使用**标识**关键字。

#### **语法:**

```
CREATE TABLE TableName (
Column1 DataType  IDENTITY(starting value, increment by),
Column2 DataType, 
);

```

### **举例:**

创建一个名为 Customers，列为 CustomerID、CustomerName、Age 和 PhoneNumber 的表。这里，自动递增 CustomerID，并使其成为表的主键。

```
CREATE TABLE Customers (
CustomerID int IDENTITY(1,1) PRIMARY KEY,
CustomerName varchar(255),
Age int,
PhoneNumber int);

```

在上面的例子中，IDENTITY 的**起始值是 1** ，它应该为每增加一条新记录**增加 1** 。你可以根据你的愿望提到这些值。 同样，要在上表中插入值，您必须以如下方式使用[插入查询](https://www.edureka.co/blog/insert-query-sql/):

```
INSERT INTO Customers (CustomerName,Age, PhoneNumber)
VALUES ('Abhay','25','9876543210');

```

在这里，如果您注意到，我没有提到 CustomerID 列，因为 ID 是自动生成的。因此，如果您看到使用下面的查询再插入 4 个值:

```
INSERT INTO Customers (CustomerName,Age, PhoneNumber)
VALUES ('Sonal','22','9812313210');

INSERT INTO Customers (CustomerName,Age, PhoneNumber)
VALUES ('Anuj','19','9956413210');

INSERT INTO Customers (CustomerName,Age, PhoneNumber)
VALUES ('Mona','24','9876543911');

INSERT INTO Customers (CustomerName,Age, PhoneNumber)
VALUES ('Sanjay','31','9657154310');

```

然后，你会看到下面的输出:

| **客户 ID** | **客户名称** | **年龄** | **电话号码** |
| 1 | abhaba的缩写形式 | 25 | 9876543210 |
| 2 | Sonal | 22 | 9812313210 |
| 3 | Anuj | 19 | 9956413210 |
| 4 | 莫娜 | 24 | 9876543911 |
| 5 | 桑杰 | 31 | 9657154310 |

接下来，在这篇关于 SQL 自动递增的文章中，让我们看看如何在 MySQL 中自动递增一列。

### **MySQL** 的语法和示例

要使用自动增量字段，在 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 中，必须使用**AUTO _ INCREMENT****关键字**。AUTO _ INCREMENT**的**起始值**默认为 1**，每增加一条记录**增加 1** 。

#### **语法:**

```
CREATE TABLE TableName (
Column1 DataType  AUTO_INCREMENT,
Column2 DataType, 
);

```

#### **举例:**

创建一个名为 Customers，列为 CustomerID、CustomerName、Age 和 PhoneNumber 的表。这里，自动递增 CustomerID，并使其成为表的主键。

```
CREATE TABLE Customers (
CustomerID int AUTO_INCREMENT PRIMARY KEY,
CustomerName varchar(255),
Age int,
PhoneNumber int);

```

如果您希望以任何其他数字开始自动增量值，那么您可以按以下方式使用关键字:

#### **语法:**

```
ALTER TABLE TableName AUTO_INCREMENT=50;

```

#### 示例:

```
ALTER TABLE Customers AUTO_INCREMENT=50;

```

类似于 SQL Server，你可以通过使用 INSERT 语句向表中插入值。在插入值时，您将看到相同的输出，如上表所示。接下来，在这篇关于 SQL 自动递增的文章中，让我们看看如何在 MS Access 中自动递增列。

### **MS Access** 的**语法和示例**

要使用自动增量字段，在 MS Access 中，必须使用 **自动增量** 关键字。

#### **语法:**

```
CREATE TABLE TableName (
Column1 DataType AUTOINCREMENT,
Column2 DataType,
);

```

#### **举例:**

创建一个名为 Customers，列为 CustomerID、CustomerName、Age 和 PhoneNumber 的表。这里，自动递增 CustomerID，并使其成为表的主键。

```
CREATE TABLE Customers (
CustomerID int AUTOINCREMENT PRIMARY KEY,
CustomerName varchar,
Age int,
PhoneNumber int);

```

**自动递增的**默认起始值**为 1** ，每增加一条记录**也会增加 1** 。但是，如果你想改变这一点，比如说，你想设置起始值为 20，增量为 2，你可以使用自动增量功能如下:

```
AUTOINCREMENT(20,2)

```

类似于 SQL Server，你可以通过使用 INSERT 语句向表中插入值。在插入值时，您将看到与上表相同的输出。接下来，在这篇关于 SQL 自动递增的文章中，让我们看看如何在 Oracle 中自动递增列。

### **语法和示例为** **甲骨文**

要使用自动递增字段，在 Oracle 中， 您必须用序列对象创建一个自动递增字段。sequence 对象生成一个数字序列。

#### **创建序列的语法:**

```
CREATE SEQUENCE name_of_sequence
MINVALUE 1
START WITH 1
INCREMENT BY 1
CACHE 10;

```

在上面的语法中，

1.  **序列名称**–创建名为 的序列名称
2.  **开始**–提及开始值
3.  **增加**–提及增加的值
4.  **缓存**–提及为更快访问而存储的值的最大数量。

**举例:**

创建一个序列对象，其中起始值为 1，增量为 3，要存储的最大值为 20。

```
CREATE SEQUENCE seq_customers
MINVALUE 1
START WITH 1
INCREMENT BY 3
CACHE 20;

```

类似于 MySQL 和 SQL Server，您可以通过使用 INSERT 语句将值插入到表中。在插入值时，您将看到与上表相同的输出。接下来，在这篇关于 SQL 自动递增的文章中，让我们看看如何在 PostgreSQL 中自动递增列。

### **PostgreSQL** 的语法和示例

要使用自动递增字段，在 [PostgreSQL](https://www.edureka.co/blog/postgresql-tutorial) 、 中，你必须用序列对象创建一个自动递增字段。sequence 对象生成一个数字序列。

#### **语法:**

```
CREATE TABLE TableName (
Column1 DataType  SERIAL PRIMARY KEY,
Column2 DataType, 
);

```

**举例:**

创建一个名为 Customers，列为 CustomerID、CustomerName、Age 和 PhoneNumber 的表。这里，自动递增 CustomerID，并使其成为表的主键。

```
CREATE TABLE Customers (
CustomerID int SERIAL PRIMARY KEY,
CustomerName varchar(255),
Age int,
PhoneNumber int);

```

类似于 [MySQL](https://www.edureka.co/blog/mysql-tutorial/) 、SQL Server 和其他 DBMS，您可以使用 INSERT 语句向表中插入值。在插入值时，您将看到相同的输出，如上表所示。

至此，我们结束了这篇关于 SQL 自动增量的文章。我希望你明白如何使用上述命令。 *如果您希望了解更多关于**MySQL**并了解这个开源的关系数据库，那么请查看我们的*[*MySQL DBA 认证培训*](https://www.edureka.co/mysql-dba) *，它附带有讲师指导的现场培训和真实的项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在这篇关于“SQL 中的自动增量”的文章的评论部分提到它，我会尽快回复您。*