# SQL Union——关于 Union 操作符的综合指南

> 原文：<https://www.edureka.co/blog/sql-union/>

在处理数据库中的数据时，我们通常倾向于在 [SQL](https://www.edureka.co/blog/what-is-sql/) 中使用集合运算符，通过组合两个或多个 SELECT 语句来根据我们的需求检索数据。在这篇关于 SQL UNION 的文章中，我将按以下顺序讨论用于检索数据的 UNION 运算符:

*   [什么是 SQL UNION 运算符？](#unionoperator)
*   [语法:](#syntax)
    1.  [联合语法](#unionsyntax)
    2.  [UNION ALL 语法](#unionallsyntax)
*   [UNION 和 UNION ALL 的区别](#unionvsunionall)
*   [SQL 联合示例:](#examples)
    1.  [联算符示例](#unionexample)
    2.  [UNION ALL 运算符示例](#unionallexample)
    3.  [与 SQL 别名的联合](#unionwithaliases)
    4.  [与 WHERE 子句的联合](#unionwithwhere)
    5.  [UNION ALL with WHERE 子句](#unionallwithwhere)
    6.  [带连接的并集](#unionwithjoins)
    7.  [UNION ALL with JOINS](#unionallwithjoins)

让我们开始吧！

## **什么是 SQL UNION 运算符？**

顾名思义，这个操作符/子句用于组合两个或多个 SELECT 语句的结果。这里，UNION 语句中使用的每个 SELECT 语句必须具有相同顺序的相同数量的列。此外，SELECT 语句中出现的所有列必须具有相似的数据类型。

UNION 子句只输出唯一的值。为了以防万一，您需要重复的值，那么您必须使用 UNION ALL 子句。

在这篇关于 SQL UNION 的文章中，让我们理解一下语法。

## **SQL 联合语法**

### **联合语法**

```
SELECT Column1, Column2, Column3, ..., ColumnN FROM Table1
UNION
SELECT Column1, Column2, Column3, ..., ColumnN FROM Table2;

```

### **联盟所有语法**

```
SELECT Column1, Column2, Column3, ..., ColumnN FROM Table1
UNION ALL
SELECT Column1, Column2, Column3, ..., ColumnN FROM Table2;

```

继续这篇文章，让我们来理解 UNION 和 UNION ALL 之间的区别。

**SQL UNION 和 UNION ALL 的区别**

| **联盟** | **工会所有人** |
| 合并两个或多个结果集，并且不保留重复值。 | 合并两个或多个结果集并保留重复值。 |
| 

```
Syntax: UNION
```

 | 

```
Syntax: UNION ALL
```

 |
| ![SQL UNION -SQL UNION -Edureka](img/c0a821cc487327c59c5e7c2dc749b6a9.png) | ![SQL UNION ALL-SQL UNION -Edureka](img/7a00db75e9380e302db2f9c9b44bfe91.png) |

接下来，在这篇关于 SQL UNION 的文章中，让我们了解使用这个操作符的不同方法。

## **SQL UNION 和 UNION ALL 的例子**

为了让您更好地理解，我将考虑下面的表格，向您展示不同的示例。

### **员工表**

| **EmpID** | **名称** | 开动 | **城市** | **邮政编码** | **国家** |
| one | 女子名 | Twenty-three | 柏林 | Twelve thousand one hundred and nine | 德国 |
| Two | 拉胡尔 | Twenty-six | 孟买 | Four hundred thousand and fifteen | 印度 |
| three | 艾拉 | Twenty-four | 纽约 | Ten thousand and fourteen | 美利坚合众国 |
| four | 约翰 | Thirty-two | 伦敦 | E1 7AE | 英国 |
| five | 德里克(男名) | Twenty-nine | 纽约 | Ten thousand and twelve | 美利坚合众国 |

### **项目表**

| **项目 ID** | **名称** | **工作日** | **城市** | **邮政编码** | **国家** |
| one | 项目 1 | Ten | 柏林 | Twelve thousand one hundred and nine | 德国 |
| Two | 项目 2 | seven | 孟买 | Four hundred thousand and fifteen | 印度 |
| three | 项目 3 | Twenty | 德里 | One hundred and ten thousand and six | 印度 |
| four | 项目 4 | Fifteen | 孟买 | Four hundred thousand and fifteen | 印度 |
| five | 项目 5 | Twenty-eight | 柏林 | Twelve thousand one hundred and nine | 德国 |

让我们从例子开始。

## **SQL 联合示例**

### **联合运算符示例**

编写一个查询，从雇员和项目表中检索不同的城市。

```
SELECT City FROM Employees
UNION
SELECT City FROM Projects
ORDER BY City;

```

### **输出:**

| **城市** |
| 柏林 |
| 德里 |
| 伦敦 |
| 孟买 |
| 纽约 |

### **UNION ALL 运算符示例**

编写一个查询，从 Employees 和 Projects 表中检索城市。这里，必须包括重复的值。

```

SELECT City FROM Employees
UNION ALL
SELECT City FROM Projects
ORDER BY City; 

```

### **输出:**

| **城市** |
| 柏林 |
| 柏林 |
| 柏林 |
| 德里 |
| 伦敦 |
| 孟买 |
| 孟买 |
| 孟买 |
| 纽约 |
| 纽约 |

接下来，在本文中，让我们了解如何使用带有 SQL 别名的 UNION 子句。

### **与 SQL 别名的联合**

SQL 别名用于给一个表或列一个临时名称。因此，让我们编写一个查询来列出所有独特的雇员和项目。

```
SELECT 'Employee' AS Type, Name, City, Country
FROM Employees
UNION
SELECT 'Project', Name, City, Country
FROM Projects;

```

### **输出:**

| **类型** | **名称** | **城市** | **国家** |
| 雇员 | 女子名 | 柏林 | 德国 |
| 雇员 | 拉胡尔 | 孟买 | 印度 |
| 雇员 | 艾拉 | 纽约 | 美利坚合众国 |
| 雇员 | 约翰 | 伦敦 | 英国 |
| 雇员 | 德里克(男名) | 纽约 | 美利坚合众国 |
| 项目 | 项目 1 | 柏林 | 德国 |
| 项目 | 项目 2 | 孟买 | 印度 |
| 项目 | 项目 3 | 德里 | 印度 |
| 项目 | 项目 4 | 孟买 | 印度 |
| 项目 | 项目 5 | 柏林 | 德国 |

**与 WHERE 子句的联合**

编写一个查询，从 Employees 和 Projects 表中检索不同的印度城市及其邮政编码。

```
SELECT City, PostalCode, Country FROM Employees
WHERE Country='India'
UNION
SELECT City, PostalCode, Country FROM Projects
WHERE Country='India'
ORDER BY City;

```

### **输出:**

| **城市** | **邮政编码** | **国家** |
| 德里 | One hundred and ten thousand and six | 印度 |
| 孟买 | Four hundred thousand and fifteen | 印度 |

**UNION ALL with WHERE 子句**

编写一个查询，从 Employees 和 Projects 表中检索印度城市及其邮政编码，这两个表中允许有重复值

```
SELECT City, PostalCode, Country FROM Employees
WHERE Country='India'
UNION ALL
SELECT City, PostalCode, Country FROM Projects
WHERE Country='India'
ORDER BY City;

```

### **输出:**

| **城市** | **邮政编码** | **国家** |
| 德里 | One hundred and ten thousand and six | 印度 |
| 孟买 | Four hundred thousand and fifteen | 印度 |
| 孟买 | Four hundred thousand and fifteen | 印度 |
| 孟买 | Four hundred thousand and fifteen | 印度 |

在本文中，让我们了解如何使用带有连接的 UNION 和 UNION ALL 子句。SQL 中的连接是[命令](https://www.edureka.co/blog/sql-commands)，用于根据两个或多个表之间的相关列来组合这些表中的行。

### **带连接的并集**

SQL UNION 操作符可以和 [SQL 连接](https://www.edureka.co/blog/sql-joins-types)一起使用，从两个不同的表中检索数据。对于这个例子，我将考虑下面的表和 Employees 表。

#### **项目明细表**

| **PID** | **工作日** | **EmpID** | **CostforProject** |
| Eleven | Twelve | four | Twenty thousand |
| Twenty-two | Sixteen | three | Thirty-five thousand |
| Thirty-three | Thirty | one | Sixty thousand |
| forty-four | Twenty-five | three | Forty-five thousand |
| Fifty-five | Twenty-one | one | Fifty thousand |

```
SELECT  EmpID, Name, CostforProject
   FROM Employees
   LEFT JOIN ProjectDetails
   ON Employees.EmpID = ProjectDetails.EmpID
UNION
   SELECT  EmpID, Name, CostforProject
   FROM Employees
   RIGHT JOIN ProjectDetails
   ON Employees.EmpID = ProjectDetails.EmpID;

```

### **输出:**

| **EmpID** | **名称** | **CostforProject** |
| one | 艾玛 | Sixty thousand |
| one | 艾玛 | Fifty thousand |
| Two | 拉胡尔 | 空 |
| three | 阿伊拉 | Thirty-five thousand |
| three | 阿伊拉 | Forty-five thousand |
| four | 约翰 | Twenty thousand |
| five | 德里克 | 空 |

### **UNION ALL with JOINS**

编写一个查询，从 Employees 和 ProjectDetails 表中检索 EmpID、Name 和 CostforProject，其中允许有重复值。

```
SELECT  EmpID, Name, CostforProject
   FROM Employees
   LEFT JOIN ProjectDetails
   ON Employees.EmpID = ProjectDetails.EmpID
UNION ALL
   SELECT  EmpID, Name, CostforProject
   FROM Employees
   RIGHT JOIN ProjectDetails
   ON Employees.EmpID = ProjectDetails.EmpID;

```

### **输出:**

| **EmpID** | **名称** | **CostforProject** |
| one | 艾玛 | Sixty thousand |
| one | 艾玛 | Fifty thousand |
| Two | 拉胡尔 | 空 |
| three | 阿伊拉 | Thirty-five thousand |
| three | 阿伊拉 | Forty-five thousand |
| four | 约翰 | Twenty thousand |
| five | 德里克 | 空 |
| four | 约翰 | Twenty thousand |
| three | 阿伊拉 | Thirty-five thousand |
| one | 艾玛 | Sixty thousand |
| three | 阿伊拉 | Thirty-five thousand |
| one | 艾玛 | Fifty thousand |

至此，我结束了这篇关于 SQL UNION 的文章。我希望您喜欢阅读这篇关于 SQL UNION 的文章。我们已经看到了使用 UNION 和 UNION ALL 命令来帮助您编写查询的不同方法。 *如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训包含讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在“SQL UNION”的评论部分提及，我会回复您。*