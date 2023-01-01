# 通过示例了解如何使用 SQL SELECT

> 原文：<https://www.edureka.co/blog/sql-select>

数据库以各种格式存储大量数据。但是你想过如何从[数据库](https://www.edureka.co/blog/what-is-a-database/)中选择数据吗？SQL SELECT 语句用于从数据库中检索数据。在这篇关于 SQL SELECT 的文章中，我将讨论如何在 SQL 中使用 SELECT 语句和其他各种[命令](https://www.edureka.co/blog/sql-commands)。

本文将涵盖以下主题:

*   [什么是 SELECT？](#select)
*   [语法](#syntax)
*   [例子:](#examples)
    *   [选择列示例](#columnexample)
    *   [选择*例子](#asteriskexample)
    *   [使用选择与](#distinctexample)截然不同的
    *   [按](#orderbyexample) 的顺序选择
    *   [使用](#groupbyexample)与一起选择分组
    *   [选择 Having 子句](#havingexample)
    *   [使用选择进入](#intoexample)

## **什么是 SQL SELECT？**

SELECT 语句用于从数据库中选择一组特定的数据。SELECT 语句返回的数据存储在名为结果集的结果表中。

## **SQL 选择语法:**

```
--To select few columns
SELECT ColumnName1, ColumnName2, ColumnName(N) FROM TableName; 

-- To select complete data from the table 
SELECT * FROM TableName; 

--To select the top N records from the table 
SELECT TOP N * FROM TableName;

```

在这篇关于 SQL SELECT 的文章中，让我们了解如何以各种方式使用 SELECT 语句。

## **例题** :

为了让您更好地理解，我将考虑下表。

| **StudentID** | **学生名称** | **年龄** | **城市** | **国家** |
| 1 | 罗汉 | 23 | 孟买 | 印度 |
| 2 | 同一个时代 | 22 | 孟买 | 印度 |
| 3 | 安娜 | 21 | 伦敦 | 英国 |
| 4 | 约翰 | 19 | 纽约 | 美国 |
| 5 | 爱丽丝 | 22 | 柏林 | 德国 |

让我们一个一个地看看它们。

### **SQL 选择列示例**

在这里，您可以输入想要检索数据的列名。

**示例:**编写一个查询，从学生表中检索学生 ID、学生姓名和年龄。

```
SELECT StudentID, StudentName, Age FROM Students;

```

#### **输出:**

| **StudentID** | **学生名称** | **年龄** |
| 1 | 罗汉 | 23 |
| 2 | 同一个时代 | 22 |
| 3 | 安娜 | 21 |
| 4 | 约翰 | 19 |
| 5 | 爱丽丝 | 22 |

### **SQL 选择*示例**

星号(*)用于选择数据库/表/列中的所有数据。

**示例:**编写一个查询，从学生表中检索所有详细信息。

```
SELECT * FROM Students;

```

#### **输出:**

| **StudentID** | **学生名称** | **年龄** | **城市** | **国家** |
| 1 | 罗汉 | 23 | 孟买 | 印度 |
| 2 | 同一个时代 | 22 | 孟买 | 印度 |
| 3 | 安娜 | 21 | 伦敦 | 英国 |
| 4 | 约翰 | 19 | 纽约 | 美国 |
| 5 | 爱丽丝 | 22 | 柏林 | 德国 |

这是使用 SELECT 语句的简单方法。让我们在这篇关于 SQL SELECT 的文章中向前看，并理解如何将 SELECT 语句与 SQL 中的其他命令一起使用。

### **使用 SELECT with DISTINCT**

您可以将 SELECT 语句与 DISTINCT 语句一起使用，以便只检索不同的值。

#### **语法**

```
SELECT DISTINCT ColumnName1, ColumnName2,ColumnName(N) FROM TableName;

```

#### **例子**

```
SELECT DISTINCT Age FROM Students;

```

**输出:**

| **年龄** |
| 23 |
| 22 |
| 21 |
| 19 |

继续阅读本文，让我们了解如何将 SQL SELECT 与 ORDER BY 子句一起使用。

### **使用 SELECT 和 ORDER BY**

众所周知， [ORDER BY 语句](https://www.edureka.co/blog/order-by-in-sql)用于对结果进行升序或降序排序。我们可以将 ORDER BY 语句与 SELECT 语句结合使用，以升序或降序检索特定数据。

##### **语法**

```
SELECT ColumnName1, ColumnName2, ColumnName(N) 
FROM TableName 
ORDER BY ColumnName1, ColumnName2, ... ASC|DESC;

```

#### **仅使用 ORDER BY** 的示例

编写一个查询，从按城市排序的学生表中选择所有字段。

```
SELECT * FROM Students ORDER BY City;

```

**输出:**

| **StudentID** | **学生名称** | **年龄** | **城市** | **国家** |
| 5 | 爱丽丝 | 22 | 柏林 | 德国 |
| 3 | 安娜 | 21 | 伦敦 | 英国 |
| 1 | 罗汉 | 23 | 孟买 | 印度 |
| 2 | 同一个时代 | 22 | 孟买 | 印度 |
| 4 | 约翰 | 19 | 纽约 | 美国 |

### **以降序使用 ORDER BY 的示例**

编写一个查询，从按城市降序排序的学生表中选择所有字段。

```
SELECT * FROM Students ORDER BY City DESC;

```

| **StudentID** | **学生名称** | **年龄** | **城市** | **国家** |
| 4 | 约翰 | 19 | 纽约 | 美国 |
| 1 | 罗汉 | 23 | 孟买 | 印度 |
| 2 | 同一个时代 | 22 | 孟买 | 印度 |
| 3 | 安娜 | 21 | 伦敦 | 英国 |
| 5 | 爱丽丝 | 22 | 柏林 | 德国 |

接下来，在本文中，让我们了解如何将 SQL SELECT 与 GROUP BY 语句一起使用。

### **使用 SELECT 和 GROUP BY**

[GROUP BY 语句](https://www.edureka.co/blog/sql-group-by/)与 SELECT 语句一起使用，按一列或多列对结果集进行分组。

##### **语法**

```
SELECT ColumnName1, ColumnName2,..., ColumnName(N) 
FROM TableName 
WHERE Condition
GROUP BY ColumnName(N) 
ORDER BY ColumnName(N);

```

**举例:**

编写一个查询，列出每个年龄段的学生人数。

```
SELECT COUNT(StudentID), City FROM Students GROUP BY City;

```

**输出:**

| **计数(学生 ID)** | **城市** |
| 2 | 孟买 |
| 1 | 伦敦 |
| 1 | 纽约 |
| 1 | 柏林 |

接下来，在本文中，让我们了解如何将 SQL SELECT 与 GROUP BY 语句一起使用。

### **将 SELECT 与 HAVING 子句一起使用**

HAVING 子句可以与 SELECT 语句一起使用，根据某些条件检索数据。

##### **语法**

```
SELECT ColumnName1, ColumnName2, ColumnName(N) 
FROM TableName 
WHERE Condition 
GROUP BY ColumnName(N) 
HAVING Condition 
ORDER BY ColumnName(N);

```

#### **例子**

编写一个查询，检索学生人数为> 1 的每个城市的学生人数，并按降序排序。

```
SELECT COUNT(StudentID), City 
FROM Students 
GROUP BY City 
HAVING COUNT(StudentID) > 1 
ORDER BY COUNT(StudentID) DESC;

```

#### **输出:**

| **计数(学生 ID)** | **城市** |
| Two | 孟买 |

### **使用 SELECT with INTO 子句**

当你想把数据从一个表复制到另一个表时，使用这个语句。

#### **语法**

```
SELECT * INTO NewTableName [IN DatabaseName] 
FROM OldTableName 
WHERE Condition;

```

#### **例子**

编写一个查询来创建学生数据库的备份。

```
SELECT * INTO StudentBackup FROM Students;

```

#### **输出:**

您将看到 StudentBackup 表将包含 Students 表中的所有字段。

| **StudentID** | **学生名称** | **年龄** | **城市** | **国家** |
| one | 罗汉 | Twenty-three | 孟买 | 印度 |
| Two | 萨梅拉 | Twenty-two | 孟买 | 印度 |
| three | 安娜；安那（anna 旧时印度货币名） | Twenty-one | 伦敦 | 联合王国 |
| four | 约翰 | Nineteen | 纽约 | 美利坚合众国 |
| five | 爱丽丝 | Twenty-two | 柏林 | 德国 |

**示例:**编写一个查询，通过选择学生表中的几列来创建备份。

```
SELECT StudentName, Age INTO StudentBackup FROM Students;

```

#### **输出:**

您将看到 StudentBackup 表将包含来自 Students 表的以下字段。

| **学生名称** | **年龄** |
| 罗汉 | Twenty-three |
| 萨梅拉 | Twenty-two |
| 安娜；安那（anna 旧时印度货币名） | Twenty-one |
| 约翰 | Nineteen |
| 爱丽丝 | Twenty-two |

**示例:**编写一个查询，通过插入在城市“孟买”学习的所有学生的所有详细信息来创建备份。

```
SELECT * INTO StudentsBackup FROM Students WHERE City = 'Mumbai';

```

| **StudentID** | **学生名称** | **年龄** | **城市** | **国家** |
| 1 | 罗汉 | 23 | 孟买 | 印度 |
| 2 | 同一个时代 | 22 | 孟买 | 印度 |

这些是使用选择命令的几种方法。为了获得更多的知识，继续练习用 [SQL 命令](https://www.edureka.co/blog/sql-tutorial/)编写查询。 关于 SQL SELECT 的这篇文章到此结束。

*如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训包含讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

有问题要问我们吗？请在本文关于 SQL SELECT 的评论部分提到它，我会尽快回复您。