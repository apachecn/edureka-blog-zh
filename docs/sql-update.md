# SQL 更新:了解如何更新表中的值

> 原文：<https://www.edureka.co/blog/sql-update/>

使用数据库时，我们可能经常想要更新单个记录或多个记录中的一些数据值。[结构化查询语言(SQL)](https://www.edureka.co/blog/sql-basics/) 提供各种访问、检索和管理数据库的命令。其中一个这样的[命令](https://www.edureka.co/blog/sql-commands)就是更新命令。UPDATE 命令用于更新表中现有的数据。 本文将涉及以下主题:

1.  [更新声明](#updatestatement)
2.  [语法](#updatesyntax)
3.  [例子:](#example)
    *   [更新单记录](#updatesinglerecord)
    *   [对多条记录使用语句](#updatemultiplerecords)
    *   [通过省略 WHERE 子句更新数据](#omitwhereclause)
    *   [使用该语句更新另一个表中的数据](#updatefromanothertable)

## **SQL 更新语句**

UPDATE 命令用于修改表格中的一条或多条记录。

## **语法:**

```
UPDATE TableName
SET Column1 = Value1, Column2 = Value2, …, ColumnN = ValueN
WHERE Condition;

```

在这里， **WHERE 子句**指定了哪些记录必须被更新。为了以防万一，您省略了 WHERE 子句，表中现有的所有记录都将被更新。

既然你已经理解了语法，现在让我们通过例子来讨论使用它的各种方法。

## **例子:**

为了让您更好地理解，我将示例分成了以下几个部分:

*   [更新单记录](#updatesinglerecord)
*   [对多条记录使用语句](#updatemultiplerecords)
*   [通过省略 WHERE 子句更新数据](#omitwhereclause)
*   [使用该语句更新另一个表中的数据](#updatefromanothertable)

我将考虑下表向你解释的例子:

| **EmpID** | **EmpName** | **帝国邮件** | **电话号码** | **城市** |
| 1 | Mohan | mohan@xyz.com | 9966449966 | 德里 |
| 2 | 索尼娅 | sonia@abc.com | 9746964799 | 孟买 |
| 3 | 桑杰 | sanjay@pqr.com | 9654323456 | 孟加拉鲁鲁 |
| 4 | 名 | 名称@xyz.com | 9876543678 | 孟买 |
| 5 | 拉胡尔 | rahul@abc.com | 9542456786 | 德里 |

让我们来看看他们每一个人。

### **更新单笔记录**

#### **举例:**

编写一个查询，用新的电话号码和城市更新第三个雇员(雇员 ID)。

```
UPDATE Employees
SET PhoneNumber ='9646879876', City= 'Kolkata'
WHERE EmpID = 3;

```

#### **输出:**

您将看到下表作为输出:

| **EmpID** | **EmpName** | **帝国邮件** | **电话号码** | **城市** |
| 1 | Mohan | mohan@xyz.com | 9966449966 | 德里 |
| 2 | 索尼娅 | sonia@abc.com | 9746964799 | 孟买 |
| 3 | 桑杰 | sanjay@pqr.com | 9646879876 | 加尔各答 |
| 4 | 名 | 名称@xyz.com | 9876543678 | 孟买 |
| 5 | 拉胡尔 | rahul@abc.com | 9542456786 | 德里 |

接下来，在本文中，让我们了解如何更新多个记录中的数据值。

### **更新多条记录**

要更新表中的多条记录，我们必须使用 WHERE 子句。 WHERE 子句确定将被更新的记录的数量。

#### **举例:**

编写一个查询，将雇员 empe mail to sample@abc.com 的所有记录更新为城市名 Delhi。

```
UPDATE Employees
Set EmpEmail = 'sample@abc.com’
WHERE City =‘Delhi’;

```

#### **输出:**

您将看到下表作为输出:

| **EmpID** | **EmpName** | **帝国邮件** | **电话号码** | **城市** |
| 1 | Mohan | sample@abc.com | 9966449966 | 德里 |
| 2 | 索尼娅 | sonia@abc.com | 9746964799 | 孟买 |
| 3 | 桑杰 | sanjay@pqr.com | 9646879876 | 加尔各答 |
| 4 | 名 | 名称@xyz.com | 9876543678 | 孟买 |
| 5 | 拉胡尔 | sample@abc.com | 9542456786 | 德里 |

继续阅读本文，让我们了解如何通过省略 WHERE 子句来更新表中的数据。

### **通过省略 WHERE 子句**更新数据

当我们在使用 [SQL](https://www.edureka.co/blog/what-is-sql/) 中的 UPDATE 语句时省略了 WHERE 子句，那么对于必须更新的记录数量就没有限制。所以，所有的记录都会自动更新。

#### **举例:**

编写一个查询来更新员工给 example@xyz.com 的电子邮件。

```
UPDATE Employees
Set EmpEmail = 'example@xyz.com’;

```

#### **输出:**

您将看到下表作为输出:

| **EmpID** | **EmpName** | **帝国邮件** | **电话号码** | **城市** |
| 1 | Mohan | example@xyz.com | 9966449966 | 德里 |
| 2 | 索尼娅 | example@xyz.com | 9746964799 | 孟买 |
| 3 | 桑杰 | example@xyz.com | 9646879876 | 加尔各答 |
| 4 | 名 | example@xyz.com | 9876543678 | 孟买 |
| 5 | 拉胡尔 | example@xyz.com | 9542456786 | 德里 |

接下来，让我们了解如何从另一个表中更新特定表的数据。

### **更新另一个表中的数据**

考虑到另一个表的数据，我们可以使用 UPDATE 语句来更新特定表的数据。

让我们考虑下面的表格:

| **联系人 ID** | **联系人姓名** | **联系人电子邮件** | **电话号码** | **城市** |
| 1 | 莫汉·夏尔马 | 联系莫汉@xyz.com | 9962449966 | 德里 |
| 2 | 索尼娅·卡纳 | contactsonia@xyz.com | 9461964799 | 孟买 |
| 3 | 桑杰·卡普尔 | contactsanjay@xyz.com | 9719879876 | 加尔各答 |
| 4 | 阿夫尼·米什拉 | contactavni@xyz.com | 9889743678 | 孟买 |
| 5 | 拉胡尔·罗伊 | contactahul @ XYZ . com | 9818256786 | 德里 |

#### **举例:**

编写一个查询，通过从 contacts 表中获取数据来更新雇员的姓名。

```
UPDATE Employees
SET EmpName = (SELECT EmpName
                  FROM Contacts
                  WHERE Contacts.City = Employees.City);

```

#### **输出:**

您将看到下表作为输出:

| **EmpID** | **EmpName** | **帝国邮件** | **电话号码** | **城市** |
| 1 | 莫汉·夏尔马 | example@xyz.com | 9966449966 | 德里 |
| 2 | 索尼娅·卡纳 | example@xyz.com | 9746964799 | 孟买 |
| 3 | 桑杰·卡普尔 | example@xyz.com | 9646879876 | 加尔各答 |
| 4 | 阿夫尼·米什拉 | example@xyz.com | 9876543678 | 孟买 |
| 5 | 拉胡尔·罗伊 | example@xyz.com | 9542456786 | 德里 |

我们也可以将上面的查询改写如下:

```
UPDATE Employees
SET Employees.EmpName = Contacts.EmpName
FROM Employees
INNER JOIN Contacts
ON (Employees.City = Contacts.City);

```

伙计们，这就是在 SQL 中使用 UPDATE 语句的方法。 到此，我们结束这篇关于 SQL 更新的文章。我希望你发现这篇文章信息丰富。

*如果您希望了解有关*[*MySQL*](https://www.edureka.co/blog/what-is-mysql/)*的更多信息，并了解这款开源关系数据库，请查看我们的*[*MySQL DBA 认证培训*](https://www.edureka.co/mysql-dba) *，它附带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在这篇关于“SQL 更新”的文章的评论部分提到它，我会尽快回复您。*