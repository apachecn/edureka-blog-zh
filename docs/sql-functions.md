# SQL 函数:如何用 SQL 写一个函数？

> 原文：<https://www.edureka.co/blog/sql-functions>

结构化查询语言又名 SQL，用于处理数据库中的数据。它提供了各种内置函数和[命令](https://www.edureka.co/blog/sql-commands)来根据我们的需求访问和管理数据库。在这篇关于 SQL 函数的文章中，我将讨论对数据执行不同类型计算的各种内置函数。

本文将涵盖以下主题:

*   [什么是 SQL 函数？](#functions)
*   [聚合函数](#aggregate)
    1.  [SUM()](#sum)
    2.  [计数()](#count)
    3.  [【AVG()】](#avg)
    4.  [【MIN()】](#min)
    5.  [MAX()](#max)
    6.  [()](#first)
    7.  [最后()](#last)
*   [标量函数](#scalar)

1.  1.  [LCASE()](#lcase)
    2.  [UCASE()](#ucase)
    3.  [LEN()](#len)
    4.  [【中旬】](#mid)
    5.  [【圆()】](#round)
    6.  [](#now)
    7.  [格式()](#format)

在我们深入研究 SQL 提供的不同类型的函数之前，让我们了解一下什么是函数。

## **什么是功能？**

函数是用来执行[数据操作](https://www.edureka.co/blog/sql-operators/)的方法。SQL 有许多用于执行字符串连接、数学计算等的内置函数。

SQL 函数分为以下两类:

1.  聚合函数
2.  标量函数

让我们一个接一个地看看它们。

## **聚合 SQL 函数**

SQL 中的聚合函数对一组值执行计算，然后返回单个值。 以下是一些最常用的聚合函数:

| **功能** | **描述** |
| SUM() | 用于返回一组数值的总和。 |
| COUNT() | 根据条件或不根据条件返回行数。 |
| AVG() | 用于计算一个数值列的平均值。 |
| MIN() | 这个函数返回一列的最小值。 |
| MAX() | 返回一列的最大值。 |
| FIRST() | 用于返回列的第一个值。 |
| LAST() | 该函数返回该列的最后一个值。 |

让我们深入研究一下上述每一项功能。为了让你更好地理解，我将考虑下表向你解释所有的例子。

| **StudentID** | **学生名称** | **标记** |
| one | 桑杰（男子名） | Sixty-four |
| Two | 瓦伦 | seventy-two |
| three | 阿卡什 | Forty-five |
| four | rohit！rohit | Eighty-six |
| five | 安佳丽 | Ninety-two |

### **SUM()**

用于返回你选择的数值列的总和。

#### **语法:**

```
SELECT SUM(ColumnName)
FROM TableName;

```

#### **举例:**

编写一个查询，从学生表中检索所有学生的分数总和。

```
SELECT SUM(Marks)
FROM Students;

```

#### **输出:**

```
359

```

### **COUNT()**

根据某种条件或不根据任何条件返回表中的行数。

#### **语法:**

```
SELECT COUNT(ColumnName)
FROM TableName
WHERE Condition;

```

#### **举例:**

编写一个查询来计算学生表中的学生人数。

```
SELECT COUNT(StudentID)
FROM Students;

```

#### **输出:**

```
5

```

#### **举例:**

编写一个查询来计算学生表中得分为> 75 的学生人数。

```
SELECT COUNT(StudentID)
FROM Students
WHERE Marks >75;

```

**输出:**

```
2

```

### **AVG()**

该函数用于返回一个数值列的平均值。

#### **语法:**

```
SELECT AVG(ColumnName)
FROM TableName;

```

#### **举例:**

编写一个查询来计算学生表中所有学生的平均分数。

```
SELECT AVG(Marks)
FROM Students;

```

#### **输出:**

```
71.8

```

### **MIN()**

用于返回数值列的最小值。

#### **语法:**

```
SELECT MIN(ColumnName)
FROM TableName;

```

**举例:**

编写一个查询，从学生表中检索所有学生的最低分数。

```
SELECT MIN(Marks)
FROM Students;

```

#### **输出:**

```
45

```

### **MAX()**

返回数值列的最大值。

#### **语法:**

```
SELECT MAX(ColumnName)
FROM TableName;

```

#### **举例:**

编写一个查询，从学生表中检索所有学生的最高分数。

```
SELECT MAX(Marks)
FROM Students;

```

**输出:**

```
92

```

### **FIRST()**

这个函数返回你选择的列的第一个值。

#### **语法:**

```
SELECT FIRST(ColumnName)
FROM TableName;

```

#### **举例:**

编写一个查询来检索第一个学生的分数。

```
SELECT FIRST(Marks)
FROM Students;

```

**输出:**

```
64

```

### **LAST()**

用于返回你选择的列的最后一个值。

#### **语法:**

```
SELECT LAST(ColumnName)
FROM TableName;

```

#### **举例:**

编写一个查询来检索最后一名学生的分数。

```
SELECT LAST(Marks)
FROM Students;

```

**输出:** 92

好了，SQL 聚合函数到此结束。接下来，在这篇关于 SQL 函数的文章中，让我们了解各种标量函数。

## **标量 SQL 函数**

SQL 中的标量函数用于从给定的输入值返回单个值。 以下是一些最常用的聚合函数:

让我们深入研究一下上述每一项功能。

| **功能** | **描述** |
| LCASE() | 用于将字符串列值转换成小写 |
| UCASE() | 这个函数用来将一个字符串的列值转换成大写。 |
| LEN() | 返回列中文本值的长度。 |
| 中间() | 从具有字符串数据类型的列值中提取 SQL 中的子字符串。 |
| 圆形() | 将数值四舍五入为最接近的整数。 |
| 现在() | 该函数用于返回当前系统日期和时间。 |
| 格式() | 用于格式化一个字段必须如何显示。 |

### **LCASE()**

用于将字符串列的值转换成小写字符。

#### **语法:**

```
SELECT LCASE(ColumnName)
FROM TableName;

```

#### **举例:**

编写一个查询来检索所有学生的小写姓名。

```
SELECT LCASE(StudentName)
FROM Students;

```

#### **输出:**

```
sanjay
varun
akash
rohit
anjali

```

### **UCASE()**

用于将字符串列的值转换成大写字符。

#### **语法:**

```
SELECT UCASE(ColumnName)
FROM TableName;

```

**举例:**

编写一个查询来检索所有学生的小写姓名。

```
SELECT UCASE(StudentName)
FROM Students;

```

#### **输出:**

```

SANJAY
VARUN
AKASH
ROHIT
ANJALI

```

### **LEN()**

用于检索输入字符串的长度。

#### **语法:**

```
SELECT LENGTH(String) AS SampleColumn;

```

#### **举例:**

编写一个查询来提取学生姓名“Sanjay”的长度。

```
SELECT LENGTH(“Sanjay”) AS StudentNameLen;

```

#### **输出:**

```
6

```

### **MID()**

该函数用于从字符串数据类型的列中提取子字符串。

#### **语法:**

```
SELECT MID(ColumnName, Start, Length)
FROM TableName;

```

#### **举例:**

编写一个查询，从 StudentName 列中提取子字符串。

```
SELECT MID(StudentName, 2, 3)
FROM Students;

```

#### **输出:**

```
anj
aru
kas
ohi
nja

```

### **回合()**

该功能用于将数值四舍五入为最接近的整数。

#### **语法:**

```
SELECT ROUND(ColumnName, Decimals)
FROM TableName;

```

#### **举例:**

对于这个例子，让我们考虑学生表中的以下标记表。

| **StudentID** | **学生名称** | **标记** |
| one | 桑杰（男子名） | Ninety point seven six |
| Two | 瓦伦 | Eighty point four five |
| three | 阿卡什 | Fifty-four point three two |
| four | rohit！rohit | Seventy-two point eight nine |
| five | 安佳丽 | Sixty-seven point six six |

编写一个查询，将标记四舍五入为整数值。

```
SELECT ROUND(Marks)
FROM Students;

```

#### **输出:**

```
91
80
54
73
68

```

### **现在()**

用于返回当前日期和时间。日期和时间以“YYYY-MM-DD HH-MM-SS”格式返回。

#### **语法:**

```
SELECT NOW();

```

**举例:**

编写一个查询来检索当前日期和时间。

现在选择()；

**输出:**

| **现在()** |
| 2019-10-14 09:16:36 |

### **格式()**

该函数格式化一个字段必须显示的方式。

**语法:**

格式(输入 *值，格式* )

**举例:**

编写一个查询，以“# #-# # #-# # #”的格式显示数字“123456789”

选择格式(123456789，“# # #-# # #-# # #”；

**输出:**

123-456-789

至此，我们结束了这篇关于 SQL 函数的文章。我希望您理解了如何使用 SQL 中的各种类型的函数。 *如果您希望了解更多关于*[*MySQL*](https://www.edureka.co/blog/what-is-mysql/)*并了解这个开源关系数据库，那么请查看我们的*[*MySQL DBA 认证培训*](https://www.edureka.co/mysql-dba) *，它附带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在“SQL 函数”的评论部分提到它，我会回复您。*