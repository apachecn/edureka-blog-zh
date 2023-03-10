# SQL 中如何使用 Alter Table 语句？

> 原文：<https://www.edureka.co/blog/alter-table/>

你是否尝试过在表格中添加、删除或[修改列？如果是，那么 ALTER TABLE 是您必须使用的命令。因此，在这篇关于 Alter Table 的文章中，我将讨论如何使用这个命令来修改表中的列。](https://www.edureka.co/blog/mysql-tutorial/)

本文将涉及以下主题:

*   [什么是 Alter Table 语句？](#sqlstatement)
*   [更改表格操作:](#operations)
    1.  [更改表格添加列](#addcolumn)
    2.  [更改表格下拉栏](#dropcolumn)
    3.  [修改表格修改列](#modifycolumn)

## **什么是 Alter Table 语句？**

该语句用于添加、修改或删除现有表中的列。此外，该语句可用于在现有表上添加/删除约束。ALTER TABLE 语句可以在 [SQL](https://www.edureka.co/blog/sql-commands) 中与以下语句一起使用:

*   [添加列](#addcolumn)
*   [降柱](#dropcolumn)
*   [修改列](#modifycolumn)

让我们根据下表逐一讨论这些问题:

如果你想知道，如何用 SQL 创建表，可以参考[我关于创建表的文章。](https://www.edureka.co/blog/create-table-in-sql/)

| **studentID** | **名字** | **姓氏** | **电话号码** |
| 1 | 罗汉 | 拉索尔 | 9876543210 |
| 2 | Sonali | 萨克森 | 9876567864 |
| 3 | ajay | 阿加瓦尔 | 9966448811 |
| 4 | 吉塔 | 调节 | 9765432786 |
| 5 | 舒巴姆 | 辛哈 | 9944888756 |

**操作:**

### **更改表格添加列**

该语句用于在现有表中添加一列或多列。

**语法:**

```
#Add Single Column
ALTER TABLE TableName
ADD ColumnName datatype;
#Add Multiple Columns
ALTER TABLE TableName 
ADD ColumnName datatype,
ADD ColumnName datatype,
ADD ColumnName datatype
;

```

**举例:**

```
ALTER TABLE students
ADD dob date;

```

您将看到一个输出，列(dob)被添加到表中，如下所示:

| **studentID** | **名字** | **姓氏** | **电话号码** | **出生日期** |
| 1 | 罗汉 | 拉索尔 | 9876543210 |  |
| 2 | Sonali | 萨克森 | 9876567864 |  |
| 3 | ajay | 阿加瓦尔 | 9966448811 |  |
| 4 | 吉塔 | 调节 | 9765432786 |  |
| 5 | 舒巴姆 | 辛哈 | 9944888756 |  |

您可以继续，通过使用 SQL 中的 [insert 查询将数据插入到列中。](https://www.edureka.co/blog/insert-query-sql/)

### **更改表格下拉栏**

该语句用于删除现有表中的一列或多列。

#### **语法:**

```
ALTER TABLE TableName
DROP ColumnName datatype;

```

### **举例:**

```
ALTER TABLE students
DROP dob date;

```

您将看到一个输出，该列从表中删除，如下:

| **studentID** | **名字** | **姓氏** | **电话号码** |
| 1 | 罗汉 | 拉索尔 | 9876543210 |
| 2 | Sonali | 萨克森 | 9876567864 |
| 3 | ajay | 阿加瓦尔 | 9966448811 |
| 4 | 吉塔 | 调节 | 9765432786 |
| 5 | 舒巴姆 | 辛哈 | 9944888756 |

### **修改表格修改列**

该语句用于修改现有表中某列的[数据类型](https://www.edureka.co/blog/sql-data-types/)。

#### **语法:**

```
#SQL Server 
ALTER TABLE TableName
ALTER COLUMN ColumnName datatype;
#MySQL
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;

```

#### **举例:**

我们把 **dob 列**加回去，把那一列的数据类型改成**year；**

要添加回列，请参考以下查询:

```
ALTER TABLE Persons
ALTER COLUMN dob year;

```

现在，要更改列的数据类型，请参考下面的代码:

```
ALTER TABLE Persons
ALTER COLUMN dob year;

```

您将看到一个输出，dob 列被添加回表中，数据类型为“year”。参考下文。

| **studentID** | **名字** | **姓氏** | **电话号码** | **出生日期** |
| 1 | 罗汉 | 拉索尔 | 9876543210 |  |
| 2 | Sonali | 萨克森 | 9876567864 |  |
| 3 | ajay | 阿加瓦尔 | 9966448811 |  |
| 4 | 吉塔 | 调节 | 9765432786 |  |
| 5 | 舒巴姆 | 辛哈 | 9944888756 |  |

到此，我们结束这篇文章。我希望你明白，如何使用上述命令。 *如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

有问题要问我们吗？请在这篇文章的评论部分提到它，我会回复你。