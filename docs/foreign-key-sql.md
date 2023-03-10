# 外键 SQL:关于外键操作您需要知道的一切

> 原文：<https://www.edureka.co/blog/foreign-key-sql/>

在当今市场中，许多跨国公司使用关系数据库来处理数据，了解每个表如何相互关联非常重要。因此，在这篇关于外键 [SQL](https://www.edureka.co/blog/sql-commands/) 的文章中，我将讨论表中的外键，以使您理解表之间的关系。

本文将涵盖以下主题:

1.  [什么是外键约束？](#ForeignkeyConstraint)
2.  [外键规则](#RulesforForeignKey)
3.  [外键操作:](#ForeignKeyOperations)
    *   [创建表上的 SQL 外键](#ForeignKeyonCreateTable)
    *   [变更表上的 SQL 外键](#ForeignKeyonAlterTable)
    *   [掉落外键](#DropForeignKey)

**什么是外键约束？**

外键是一种用于链接数据库中两个表的键。因此，外键是一个表中引用另一个表中主键的属性或属性集合。

例如，如果表 A 和表 B 彼此相关，那么如果表 A 由主键组成，则该表将被称为被引用表或父表。类似地，如果表 B 由一个外键组成，那么该表就是引用表或子表。 参考下图:

![Foreign Key - Foreign Key SQL - Edureka](img/b69d906c78daa0f2ea60daf4e35238f9.png)

既然你知道什么是外键，接下来在这篇关于外键 SQL 的文章中，让我们了解外键的规则。

**外键规则**

外键的规则如下:

1.  带有外键的表称为子表，被外键引用的表称为父表。
2.  外键中允许空值
3.  外键可以复制
4.  一个表中可以有多个外键
5.  表之间建立的关系被称为参照完整性

现在你已经知道了外键的规则，接下来在这篇关于外键 SQL 的文章中，让我们看看外键的操作。

**外键操作:**

为了理解外键上的各种操作，考虑下面两个表:

### **客户表:**

| **客户 ID** | **客户名称** | **电话号码** |
| 1 | 罗汉 | 9876543210 |
| 2 | Sonali | 9876567864 |
| 3 | ajay | 9966448811 |
| 4 | 吉塔 | 9765432786 |
| 5 | 舒巴姆 | 9944888756 |

### **课程表:**

| 跑 | **CourseName** | **客户 ID** |
| c01 | DevOps | 2 |
| c02 | 机器学习 | 4 |
| c03 | 南非 | 1 |
| c04 | 表 | 3 |
| c05 | AWS | 2 |

现在，如果您观察一下，courses 表中的 customerID 列引用了 customers 表中的 customerID 列。customers 表中的 customerID 列是主键，courses 表中的 customerID 列是该表的外键。

从第一道工序开始:

### **创建表上的外键**

在创建“courses”表时，可以使用以下语法在“customerID”列上创建外键:

```
#For SQL Server/ MS Access/ Oracle
CREATE TABLE courses (
courseID varchar NOT NULL PRIMARY KEY,
courseName varchar NOT NULL,
customerID int FOREIGN KEY REFERENCES customers(customerID)
);
#For MySQL
CREATE TABLE courses (
courseID varchar NOT NULL PRIMARY KEY,
courseName varchar NOT NULL,
customerID int
PRIMARY KEY (courseID),
FOREIGN KEY (customerID) REFERENCES customers(customerID)
);

```

#### **在多个列上应用外键**

在[创建表](https://www.edureka.co/blog/create-table-in-sql/)时，要在多个列上应用外键，请参考以下示例:

```
CREATE TABLE courses (
courseID varchar NOT NULL,
courseName varchar NOT NULL,
customerID int, PRIMARY KEY (courseID),
CONSTRAINT FK_CustomerCourse FOREIGN KEY (customerID)
REFERENCES customers(customerID)
);

```

接下来，在这篇关于外键 SQL 的文章中，让我们看看如何在 Alter Table 上使用外键。

### **变更表上的外键**

当已经创建了“courses”表，并且您只想改变该表时，您可以使用以下语法在“customerID”列上创建外键:

```
ALTER TABLE courses
ADD FOREIGN KEY (customerID) REFERENCES customers(customerID);

```

如果您希望向外键约束添加一个名称，并在多个列上定义它，请使用以下 SQL 语法:

```
ALTER TABLE courses
ADD CONSTRAINT FK_CustomerCourse
FOREIGN KEY (customerID) REFERENCES Customers(customerID);

```

接下来，在这篇关于外键 SQL 的文章中，让我们了解如何删除外键

### **删除外键**

要删除外键，可以参考下面的例子:

```
#For SQL Server/ MS Access/ Oracle
ALTER TABLE courses
DROP CONSTRAINT FK_CustomerCourse;
For MYSQL
ALTER TABLE courses
DROP FOREIGN KEY FK_CustomerCourse;

```

到此，我们结束这篇文章。我希望您了解如何在 SQL 中使用外键。 *如果您希望了解更多关于*[*MySQL*](https://www.edureka.co/blog/what-is-mysql/)*并了解这个开源关系数据库，那么请查看我们的*[*MySQL DBA 认证培训*](https://www.edureka.co/mysql-dba) *，它附带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

有问题要问我们吗？请在本文“外键 SQL”的评论部分提到它，我会尽快回复您。