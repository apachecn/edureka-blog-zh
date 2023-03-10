# SQL GROUP BY 语句有什么用？

> 原文：<https://www.edureka.co/blog/sql-group-by/>

当存在大量数据时，我们经常会看到根据我们的要求操纵数据的可能性。GROUP BY 子句是 SQL 中的一个这样的[语句，用于根据几列或条件对数据进行分组。在这篇关于 SQL GROUP BY 语句的文章中，我将按以下顺序讨论使用 GROUP BY 语句的几种方法:](https://www.edureka.co/blog/sql-commands)

1.  [分组通过报表](#groupby)
2.  [语法](#syntax)
3.  [例子:](#examples)
    *   [在单列上使用分组方式](#groupbyonsinglecolumn)
    *   [按多列分组](#groupbyonmultiplecolumn)
    *   [使用分组依据与排序依据](#groupbywithorderby)
    *   [GROUP BY with HAVING 子句](#groupbywithhaving)
    *   [使用 GROUP BY with 联接](#groupbywithjoins)

在我们开始讨论如何使用 GROUP BY 子句的例子之前，让我们先了解一下 SQL 中的 GROUP BY 及其语法。

## **SQL GROUP BY 语句**

该语句用于对具有相同值的记录进行分组。GROUP BY 语句通常与聚合函数一起使用，按一列或多列对结果进行分组。 除此之外，GROUP BY 子句还与 HAVING 子句一起使用，[与](https://www.edureka.co/blog/sql-joins-types)连接，根据条件对结果集进行分组。

## **SQL GROUP BY 语法**

```
SELECT Column1, Column2,..., ColumnN
FROM TableName
WHERE Condition
GROUP BY ColumnName(s)
ORDER BY ColumnName(s);

```

在这里，您可以在列名之前添加聚合函数，还可以在语句末尾添加 HAVING 子句来提及条件。 接下来，在这篇关于 SQL GROUP BY 的文章中，让我们了解一下如何实现这条语句。

## **例子:**

为了让您更好地理解，我将示例分成了以下几个部分:

我将考虑下表向你解释的例子:

| **EmpID** | **EmpName** | **帝国邮件** | **电话号码** | **工资** | **城市** |
| 1 | Nidhi | nidhi@sample.com | 9955669999 | 50000 | 孟买 |
| 2 | 阿奈 | anay@sample.com | 9875679861 | 55000 | 浦那 |
| 3 | 拉胡尔 | rahul@sample.com | 9876543212 | 35000 | 德里 |
| 4 | 索尼娅 | sonia@sample.com | 9876543234 | 35000 | 德里 |
| 5 | 阿卡什 | akash@sample.com | 9866865686 | 25000 | 孟买 |

让我们来看看他们每一个人。

### **对单个列使用 SQL GROUP BY**

#### **举例:**

编写一个查询来检索每个城市的雇员人数。

```
SELECT COUNT(EmpID), City
FROM Employees
GROUP BY City;

```

#### **输出:**

您将看到以下输出:

| **计数(EmpID)** | **城市** |
| 2 | 德里 |
| 2 | 孟买 |
| 1 | 浦那 |

### **在多个列上使用 SQL GROUP BY**

#### **举例:**

编写一个查询来检索每个城市中拥有不同薪水的雇员人数。

```
SELECT City, Salary, Count(*)
FROM Employees
GROUP BY City, Salary;

```

#### **输出:**

该表将有以下数据:

| **城市** | **工资** | **计数(*)** |
| 德里 | 35000 | 2 |
| 孟买 | 25000 | 1 |
| 孟买 | 50000 | 1 |
| 浦那 | 55000 | 1 |

### **使用 SQL GROUP BY 和 ORDER BY**

当我们将 SQL GROUP BY 语句与 [ORDER BY 子句](https://www.edureka.co/blog/order-by-in-sql)一起使用时，值按升序或降序排序。

#### **举例:**

编写一个查询来检索每个城市的雇员人数，按降序排列。

```
SELECT COUNT(EmpID), City
FROM Employees
GROUP BY City
ORDER BY COUNT(EmpID) DESC;

```

#### **输出:**

该表将包含以下数据:

| **计数(EmpID)** | **城市** |
| 2 | 德里 |
| 2 | 孟买 |
| 1 | 浦那 |

### **使用 SQL GROUP BY with HAVING 子句**

SQL GROUP BY 语句与‘HAVING’子句一起使用，表示组的条件。 同样，因为我们不能在 WHERE 子句中使用聚合函数，所以我们必须使用‘HAVING’子句在 GROUP BY 子句中使用聚合函数。

#### **例如:**

编写一个查询来检索每个城市的雇员人数，工资为> 15000

```
SELECT COUNT(EmpID), City
FROM Employees
GROUP BY City
HAVING SALARY > 15000;

```

#### **输出:**

由于雇员表中的所有记录都有薪水> 15000，我们将看到下表作为输出:

| **计数(EmpID)** | **城市** |
| 2 | 德里 |
| 2 | 孟买 |
| 1 | 浦那 |

### **使用 GROUP BY 和 JOINS**

[联接](https://www.edureka.co/blog/sql-joins-types)是 [SQL](https://www.edureka.co/blog/what-is-sql/) 语句，用于根据两个或多个表之间的相关列来组合这些表中的行。我们可以使用 SQL GROUP BY 语句根据一列或多列对结果集进行分组。 考虑下面的表，用 SQL GROUP BY 子句执行 JOIN 语句。

#### **项目表:**

| **项目 ID** | **EmpID** | **ClientID** | **项目日期** |
| 2345 | 1 | 4 | 2019 年 1 月 26 日 |
| 9876 | 2 | 5 | 2019 年 2 月 28 日 |
| 3456 | 3 | 6 | 2019 年 12 月 3 日 |

#### **客户表:**

| **ClientID** | **客户名称** |
| 4 | 桑吉娜 |
| 5 | 罗汉 |
| 6 | 阿伦 |

#### **例子**

编写一个查询，列出每个客户请求的项目数量:

```
SELECT Clients.ClientName, COUNT(Projects.ProjectID) AS RequestedProjects FROM Projects
LEFT JOIN Clients ON Projects.ProjectID = Clients.ProjectID
GROUP BY ClientName;

```

#### **输出:**

该表将包含以下数据:

| **客户名称** | **请求的项目** |
| 阿伦 | 1 |
| 罗汉 | 1 |
| 桑吉娜 | 1 |

至此，我们结束了 SQL 的逐条分组。 *来看看这个* [*MySQL DBA 认证培训*](https://www.edureka.co/mysql-dba) *由 Edureka，一个值得信赖的在线学习公司与网络*o*f 超过 250，000 名满意的学习者遍布全球。* *本课程训练你掌握管理数据和 MySQL 数据库的核心概念&高级工具和技术。它包括对 MySQL 工作台、MySQL 服务器、数据建模、MySQL 连接器、数据库设计、MySQL 命令行、MySQL 函数等概念的实践学习。培训结束后，您将能够创建和管理自己的 MySQL 数据库并管理数据。*

*有问题吗？请在这篇“SQL GROUP BY”文章的评论部分提到它，我们会尽快回复您。*