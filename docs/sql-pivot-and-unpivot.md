# SQL Pivot–知道如何将行转换为列

> 原文：<https://www.edureka.co/blog/sql-pivot-and-unpivot/>

关系数据库以表格的形式存储海量数据。这些表格可以有任意数量的行和列。但是，如果您必须将行级别的数据更改为列数据，该怎么办呢？在这篇关于 SQL Pivot 的文章中，我将向您展示如何在 SQL Server 中将行转换为列。

本文将涵盖以下主题:

*   [SQL 中的 PIVOT 是什么？](#whatispivot)
*   [语法](#syntax)
*   [例子](#example)
*   [PIVOT 子句的工作](#workingofpivot)
*   [SQL UNPIVOT](#sqlunpivot)

## **SQL 中的 PIVOT 是什么？**

PIVOT 用于通过将单个列的唯一值转换为多个列来旋转表值。它用于将行旋转为列值，并在需要时对剩余的列值运行聚合。

另一方面，UNPIVOT 用于执行相反的操作。因此，它用于将特定表的列转换为列值。

继续阅读本文，让我们理解 SQL Pivot 的语法。

## **语法:**

```
SELECT NonPivoted ColumnName,  
    [First Pivoted ColumnName] AS ColumnName,  
    [Second Pivoted ColumnName] AS ColumnName, 
    [Third Pivoted ColumnName] AS ColumnName,	
    ...  
    [Last Pivoted ColumnName] AS ColumnName  
FROM  
    (SELECT query which produces the data)   
    AS [alias for the initial query]  
PIVOT  
(  
    [AggregationFunction](ColumName)  
FOR   
[ColumnName of the column whose values will become column headers]   
    IN ( [First Pivoted ColumnName], [Second Pivoted ColumnName],  [Third Pivoted ColumnName]
    ... [last pivoted column])  
) AS [alias for the Pivot Table];

```

在这里，您还可以使用 [ORDER BY 子句](https://www.edureka.co/blog/order-by-in-sql)对值进行升序或降序排序。现在，您已经知道了 SQL 中什么是 PIVOT 及其基本语法，让我们向前看，看看如何使用它。

## **例题**

为了让你更好的理解，我将考虑下表来解释所有的例子。

#### **供应商表:**

| **供应商 ID** | **制造天数** | **成本** | **客户 ID** | **购买 ID** |
| one | Twelve | One thousand two hundred and thirty | Eleven | 第一亲代 |
| Two | Twenty-one | One thousand five hundred and forty-three | Twenty-two | P2 |
| three | Thirty-two | Two thousand three hundred and forty-five | Eleven | P3 |
| four | Fourteen | Eight thousand seven hundred and sixty-five | Twenty-two | 第一亲代 |
| five | forty-two | Three thousand four hundred and fifty-two | Thirty-three | P3 |
| six | Thirty-one | Five thousand four hundred and thirty-one | Thirty-three | 第一亲代 |
| seven | Forty-one | Two thousand three hundred and forty-two | Eleven | P2 |
| eight | Fifty-four | Three thousand six hundred and fifty-four | Twenty-two | P2 |
| nine | Thirty-three | One thousand two hundred and thirty-four | Eleven | P3 |
| Ten | fifty-six | Six thousand eight hundred and thirty-two | Thirty-three | P2 |

让我们编写一个简单的查询来检索每个客户花费的平均成本。

```
SELECT CustomerID, AVG(Cost) AS AverageCostofCustomer   
FROM Suppliers  
GROUP BY CustomerID;  

```

#### **输出:**

| **客户 ID** | **客户平均成本** |
| Eleven | One thousand seven hundred and eighty-seven point seven five |
| Twenty-two | Four thousand six hundred and fifty-four |
| Thirty-three | Five thousand two hundred and thirty-eight point three three |

现在，假设我们想要旋转上面的表。这里，CustomerID 列值将成为列标题。

```

-- Create Pivot table with one row and three columns
SELECT 'AverageCostofCustomer' AS Cost_According_To_Customers,
[11], [22], [33]
FROM
(SELECT CustomerID, Cost
FROM Suppliers) AS SourceTable
PIVOT
(
AVG(Cost)
FOR CustomerID IN ([11], [22], [33])
) AS PivotTable;

```

**输出:**

| **根据客户成本** | Eleven | Twenty-two | Thirty-three |
| **客户平均成本** | One thousand seven hundred and eighty-seven point seven five | Four thousand six hundred and fifty-four | Five thousand two hundred and thirty-eight point three three |

**注意:**当您将[聚合函数](https://www.edureka.co/blog/sql-functions#aggregate)与 PIVOT 一起使用时，在计算聚合时不考虑空值。

好吧，这是一个基本的例子，但是现在让我们来了解一下 PIVOT 子句是如何工作的。

## **PIVOT 子句的工作**

如上所述，要创建数据透视表，您需要遵循以下步骤:

*   选择要透视的列
*   然后，选择一个源表。
*   应用 PIVOT 运算符，然后使用聚合函数。
*   提及枢纽价值。

### **选择要旋转的列**

最初，我们必须指定要包含在结果中的字段。在我们的示例中，我考虑了数据透视表中的 AverageCostofCustomer 列。然后，我们创建了另外三个列，列标题分别为 11、22 和 33。示例-

```
SELECT 'AverageCostofCustomer' AS Cost_According_To_Customers, [11], [22], [33]

```

### **选择源表**

接下来，您必须指定 SELECT 语句，该语句将返回数据透视表的源数据。在我们的例子中，我们从供应商表中返回 CustomerID 和 Cost。

```
(SELECT CustomerID, Cost FROM Suppliers) AS SourceTable

```

### **应用透视运算符，然后使用聚合函数**

接下来，您必须指定创建数据透视表时要使用的聚合函数。在我们的例子中，我使用了 AVG 函数来计算平均成本。

```
PIVOT ( AVG(Cost)

```

### **提及枢轴值**

最后，你必须提到结果数据透视表中必须包含的值。这些值将被用作数据透视表中的列标题。

```
FOR CustomerID IN ([11], [22], [33]) ) AS PivotTable;

```

这就是 PIVOT 运算符的工作方式。在这篇关于 SQL PIVOT 的文章中，让我们了解它与 SQL UNPIVOT 的不同之处。

## **SQL UNPIVOT**

SQL UNPIVOT 运算符用于执行与 PIVOT 相反的操作。它用于将列数据旋转为行级数据。UNPIVOT 的语法类似于 PIVOT 的语法。唯一的区别是您必须使用 [SQL 关键字](https://www.edureka.co/blog/sql-commands)“**UNPIVOT”**。

### **举例:**

让我们创建一个包含 SupplierID、AAA、BBB 和 CCC 列的表。另外，插入几个值。

```
CREATE TABLE sampletable (SupplierID int, AAA int, BBB int, CCC int);  
GO  
INSERT INTO sampletable VALUES (1,3,5,6);  
INSERT INTO sampletable VALUES (2,9,2,8);  
INSERT INTO sampletable VALUES (3,8,1,7);  
GO  

```

#### **输出:**

| **供应商 ID** | AAA | **BBB** | **CCC** |
| one | three | five | six |
| Two | nine | Two | eight |
| three | eight | one | seven |

现在，让我们说，我们想 unpivot 表。为此，您可以参考下面的代码:

```
SELECT SupplierID, Customers, Products
FROM
(SELECT SupplierD, AAA, BBB, CCC
FROM sampletable) p
UNPIVOT
(Products FOR Customers IN
(AAA, BBB, CCC)
)AS example;
GO

```

| **供应商 ID** | **客户** | **产品** |
| one | 美国汽车协会 | three |
| one | 日本商务改善协会(Better Business Bureau) | five |
| one | 控制台控制电路(Console Control Circuits) | six |
| Two | 美国汽车协会 | nine |
| Two | 日本商务改善协会(Better Business Bureau) | Two |
| Two | 控制台控制电路(Console Control Circuits) | eight |
| three | 美国汽车协会 | eight |
| three | 日本商务改善协会(Better Business Bureau) | one |
| three | 控制台控制电路(Console Control Circuits) | seven |

这就是你如何使用 SQL 透视和反透视。到此，我们结束这篇文章。我希望你明白，如何使用 SQL。 *如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

有问题要问我们吗？请在这篇关于 SQL Pivot 的文章的评论部分提到它，我会尽快回复您。