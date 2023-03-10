# 什么是 SQL 约束及其不同类型？

> 原文：<https://www.edureka.co/blog/sql-constraints/>

由于[数据库](https://www.edureka.co/blog/what-is-a-database/)中存在大量数据，因此提高数据库中数据的准确性和可靠性对我们所有人来说都非常重要。好吧，SQL 约束是用来保持不变的。可以使用不同类型的约束。在本文中，我将举例讨论这些约束。

本文将涵盖以下主题:

1.  [什么是约束？](#constraints)
2.  [SQL 中可用约束:](#differenttypesofconstraints)

## **什么是 SQL 约束？**

SQL 约束用于指定表中数据的规则。这些用于限制必须存储在数据库中的数据类型，旨在提高存储在数据库中的数据的准确性和可靠性。

因此，约束确保在数据交易方面没有违规，即使发现了任何违规；该操作被终止。

*有两种类型的约束可以应用:*

1.  **列级约束**–这些约束应用于单个列
2.  **表级约束**–这些约束是对整个表的应用

在本文中，让我们了解不同类型的约束。此外，我将考虑下表，以帮助您更好地理解。

## **可用的不同 SQL 约束:**

### **非空约束**

NOT NULL 约束确保列不能有空值。您可以在[创建表](https://www.edureka.co/blog/create-table-in-sql/)数据库或修改它时使用 NOT NULL 约束。

#### **例子**

#### **创建表**上的非空约束

编写一个查询来创建上面的学生表，其中 StudentID 和 StudentName 不能为空。

```
CREATE TABLE Students( 
StudentID int NOT NULL, 
StudentName varchar(255) NOT NULL, 
Age int, City varchar(255) );

```

### **ALTER TABLE 上的 NOT NULL 约束**

编写一个查询来修改上面的学生表，其中必须添加一个新的列 DOB，并且它不能有任何空值。

```
ALTER TABLE Students ADD COLUMN DOB year NOT NULL;

```

在这篇关于 SQL 约束的文章中，让我们了解如何使用 UNIQUE 约束。

### **唯一约束**

唯一约束用于确保一列中的所有值都是唯一的。可以对多个列或单个列使用 UNIQUE 约束。除此之外，您还可以使用 UNIQUE 约束来修改现有的表。

**注:**

1.  创建表时，主键约束自动具有唯一约束，以保证列的唯一性。
2.  一个表可以有许多唯一约束，但只能有一个主键约束。

#### **举例:**

#### **创建表的唯一约束**

编写一个查询来创建一个学生表，包含列 StudentID、StudentName、Age 和 City。这里，StudentID 对于每条记录都必须是唯一的。

```
CREATE TABLE Students ( 
StudentID int NOT NULL UNIQUE, 
StudentName varchar(255) 
NOT NULL, Age int, City varchar(255) );

```

#### **命名多列上的唯一约束**

要命名一个唯一约束并为多个列定义它，您可以参考以下示例:

编写一个查询来创建一个学生表，包含列 StudentID、StudentName、Age 和 City。这里，StudentID 和 StudentName 对于每条记录都必须是唯一的。

```
CREATE TABLE Students ( 
StudentID int NOT NULL, 
StudentName varchar(255) NOT NULL, 
Age int, 
City varchar(255) CONSTRAINT Stu_Example 
UNIQUE (StudentID,StudentName) );

```

这里，Stu_Example 是应用于 StudentID 和 StudentName 的唯一约束的名称。

#### **变更表的唯一约束**

编写一个查询来修改 Students 表，其中必须向 StudentID 列添加一个唯一约束。

```
ALTER TABLE Students ADD UNIQUE (StudentID);

```

类似地，如果您想在多个列上使用 UNIQUE 约束并命名它，您可以编写如下查询:

```
ALTER TABLE Students ADD CONSTRAINT Stu_Example UNIQUE (StudentID,StudentName);

```

#### **删除唯一约束**

要删除列上指定的约束，您可以使用在添加约束时提到的命名约定。

例如，如果我们必须编写一个查询来删除上面创建的惟一约束，您可以编写如下查询:

```
ALTER TABLE Students DROP CONSTRAINT Stu_Example;

```

接下来，在这篇关于 SQL 约束的文章中，让我们了解如何使用检查约束。

### **检查约束**

检查约束确保一列中的所有值都满足特定的条件。

#### **举例:**

#### **检查创建表的约束**

编写一个查询来创建一个学生表，包含列 StudentID、StudentName、Age 和 City。在这里，城市必须是孟买。

```
CREATE TABLE Students ( 
StudentID int NOT NULL UNIQUE, 
StudentName varchar(255) NOT NULL, 
Age int, 
City varchar(255)CHECK (City==’Mumbai’) );

```

#### **检查多列上的约束**

要在多个列上使用检查约束，您可以编写如下查询:

编写一个查询来创建一个学生表，包含列 StudentID、StudentName、Age 和 City。在这里，城市必须是孟买，学生年龄必须是> 19 岁。

```
CREATE TABLE Students ( 
StudentID int NOT NULL, 
StudentName varchar(255) NOT NULL, 
Age int, 
City varchar(255)CHECK (City==&rsquo;Mumbai&rsquo; AND Age>19));

```

类似地，你也可以将检查约束与 ALTER TABLE 命令一起使用。参考下文。

#### **检查变更表上的约束**

编写一个查询来修改学生表，其中必须将 CHECK 约束添加到 City 列中。在这里，城市必须是孟买。

```
ALTER TABLE Students ADD CHECK (City=='Mumbai');

```

类似地，如果您想通过给 CHECK 约束命名来使用它，您可以编写如下查询:

```
ALTER TABLE Students ADD CONSTRAINT StuCheckExample CHECK (City=='Mumbai');

```

#### **删除检查约束**

要删除列上指定的约束，您可以使用在添加约束时提到的命名约定。

例如，如果我们必须编写一个查询来删除上面创建的检查约束，您可以编写如下查询:

```
ALTER TABLE Students DROP CONSTRAINT StuCheckExample;

```

在这篇关于 SQL 约束的文章中，让我们了解如何使用默认约束。

### **默认约束**

DEFAULT 约束用于在没有指定值的情况下提及一组列的默认值。与其他约束类似，我们可以在 CREATE and ALTER table 命令中使用该约束。

#### **例子**

编写一个查询来创建一个学生表，包含列 StudentID、StudentName、Age 和 City。此外，当城市列中没有插入值时，自动必须包括德里。

```
CREATE TABLE Students ( 
StudentID int NOT NULL, 
StudentName varchar(255) NOT NULL, 
Age int, 
City varchar(255)DEFAULT ‘Delhi’);

```

#### **更改表的默认约束**

要将默认约束与 [ALTER TABLE 命令](https://www.edureka.co/blog/alter-table/)一起使用，您可以编写如下查询:

```
ALTER TABLE Students ADD CONSTRAINT StuDefauExample DEFAULT 'Mumbai' FOR City;

```

#### **删除默认约束**

要删除默认约束，可以使用 ALTER TABLE 命令如下:

```
ALTER TABLE Students ALTER COLUMN City DROP DEFAULT;

```

接下来，在这篇关于 SQL 约束的文章中，让我们了解如何使用索引约束。

### **索引约束**

INDEX 约束用于在表中创建索引，在这些索引的帮助下，您可以非常快速地从数据库中创建和检索数据。

#### **语法**

```
--Create an Index where duplicate values are allowed
CREATE INDEX IndexName
ON TableName (ColumnName1, ColumnName2, ...ColumnName(N));

--Create an Index where duplicate values are not allowed
CREATE UNIQUE INDEX IndexName
ON TableName (ColumnName1, ColumnName2, ...ColumnName(N));

```

#### **例子**

编写一个查询，在存储学生姓名的学生表上创建一个名为 Stu_index 的索引。

```
CREATE INDEX Stu_index ON Students (StudentName);

```

类似地，要从表中删除一个索引，必须使用带有该索引名称的 DROP 命令。

```
DROP INDEX Students.Stu_index;

```

除了上述约束条件，[主键](https://www.edureka.co/blog/primary-key-in-sql/)和外键也被视为约束条件。PRIMARY KEY 约束用于定义特定列如何唯一标识每个元组的约束。[外键](https://www.edureka.co/blog/foreign-key-sql/)约束用于根据关系关联两个表。

到此，我们结束这篇文章。我希望您理解了如何使用数据库中的各种约束。*如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训包含讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

有问题要问我们吗？请在本文关于 SQL 约束的评论部分提到它，我会尽快回复您。