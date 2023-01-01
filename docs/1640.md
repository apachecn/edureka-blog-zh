# 了解如何在 SQL 中使用 CASE 语句

> 原文：<https://www.edureka.co/blog/case-in-sql>

在当今世界，每天都会产生海量数据，我们必须确保能够根据条件检索数据。因此，在这篇关于 [SQL](https://www.edureka.co/blog/sql-commands) 中的 CASE 的文章中，我将讨论用于基于条件检索数据的 CASE 语句。

![SQL-CASE In SQL-Edureka](img/e888e54d815fbc07928f76a520a1d494.png)本文将涉及以下主题:

## **SQL 中的 CASE 是什么？**

CASE 语句用于根据一些条件检索数据。所以，一旦条件满足，那么它将停止读取数据并返回所需的结果。在不满足任何条件的情况下，它将返回 ELSE 子句中的值。除此之外，如果没有 ELSE 部分，那么不满足任何条件，将返回 NULL。

## **案例语法**

```
CASE
	    WHEN Condition1 THEN Result1
	    WHEN Condition2 THEN Result2
		WHEN Condition3 THEN Result3
	    WHEN ConditionN THEN ResultN
	    ELSE Result;

```

现在，既然我已经告诉你了，SQL 中的 CASE 语句的语法是什么。让我们看看如何使用 CASE 语句、值或搜索条件。

以下面的表格为例:

| **StudentID** | **名字** | **年龄** | **城市** |
| 1 | 罗汉 | 14 | 海德拉巴 |
| 2 | Sonali | 21 | 孟加拉鲁鲁 |
| 3 | ajay | 13 | 勒克瑙 |
| 4 | 吉塔 | 25 | 勒克瑙 |
| 5 | 舒巴姆 | 20 | 德里 |

## **简单案例表达示例**

简单事例用于 SQL 中，根据几个条件返回数据，当第一个条件满足时返回值。

```
SELECT StudentID, City,
CASE
    WHEN Age > 20 THEN "Age is greater than "
    WHEN Age = 20 THEN "Age is equal to 20"
    ELSE "Age is below 20"
END AS AgeValue
FROM Students;

```

在执行上面的查询时，您将看到下面的输出:

| **StudentID** | **城市** | **AgeValue** |
| 1 | 海德拉巴 | 年龄小于 20 岁 |
| 2 | 孟加拉鲁鲁 | 年龄大于 20 |
| 3 | 勒克瑙 | 年龄小于 20 岁 |
| 4 | 勒克瑙 | 年龄大于 20 |
| 5 | 德里 | 年龄等于 20 |

## **搜索案例表达式示例**

在 SQL 中使用 Search CASE，根据 CASE 语句中的条件返回数据。 考虑这样一个场景，你必须按年龄给学生排序。然而，如果年龄在 15 到 18 岁之间，那么你必须按城市订购

```
SELECT FirstName, Age, City FROM Students
ORDER BY (
CASE
WHEN Age BETWEEN 15 AND 18 THEN City
ELSE Age
END
);

```

由于上面的表“Students”没有空值，在执行上面的查询时，您将看到下面的输出:

| **名字** | **年龄** | **城市** |
| ajay | 13 | 勒克瑙 |
| 罗汉 | 14 | 海德拉巴 |
| 舒巴姆 | 20 | 德里 |
| Sonali | 21 | 孟加拉鲁鲁 |
| 吉塔 | 25 | 勒克瑙 |

至此，我们结束了这篇关于 SQL 中的 CASE 的文章。我希望您理解了如何使用 CASE 语句根据条件检索数据.. *如果您希望了解更多关于*[*MySQL*](https://www.edureka.co/blog/what-is-mysql/)*并了解这个开源关系数据库，那么请查看我们的*[*MySQL DBA 认证培训*](https://www.edureka.co/mysql-dba) *，它附带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在“SQL 中的 CASE”这篇文章的评论部分提到它，我会尽快回复您。*