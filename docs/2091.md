# SQL 视图:如何在 SQL 中使用视图？

> 原文：<https://www.edureka.co/blog/sql_view/>

您执行的任何数据库操作都应该有一个正确的视图。SQL 中的视图基本上是虚拟表。当我说 *[表](https://www.edureka.co/blog/create-table-in-sql/)* 时，它必须包含行和列。因此，本文将帮助您了解如何创建一个视图，以及您可以对它们执行的不同操作。

本文讨论的主题是:

*   [什么是视图？](#What_is_a_View?)
*   [如何创建视图？](#How_to_create_a_View?)
*   [操作](#Operations)
    *   [更新](#Update)
    *   [插入](#Insertion)
    *   [删除](#Deletion)
    *   [下降](#Drop)
*   [优势](#Advantages)

我们开始吧！

## **什么是视图？**

SQL 中的视图是虚拟表。即使这些也有行和列，就像它们在普通数据库表中一样。这些是表格,通过这些表格可以查看一个或多个表格中的部分数据。

视图不包含自己的数据。它们主要用于限制对数据库的访问或隐藏数据的复杂性。一个视图被存储为数据库中的 *[选择](https://www.edureka.co/blog/sql-select)* 语句。一个视图是基于 DML 的操作，对一个视图像 *[插入](https://www.edureka.co/blog/insert-query-sql/)* ， *[更新](https://www.edureka.co/blog/sql-update/)* ，删除会影响到原表中的数据。

现在，让我们继续前进，了解如何创建视图。

## **如何创建视图？**

创建视图是一项简单的任务。只需遵循语法并了解表格内容。

**语法**

```
CREATE VIEW view_name
AS
SELECT column_list
FROM table_name [WHERE condition];
```

这里，

*视图名称*是视图的名称，而和*选择*命令用于定义行和列。

现在，这方面的一个例子是:

```
CREATE VIEW view_product
AS
SELECT product_id, product_name
FROM product;
```

这里，view_name 是 product，并从表 product 中选择 product_id 和 name。

| **名称** | **ID** |
| 汽车 | fifty-six |
| 自行车 | Twenty-five |
| 人力车 | Nineteen |

**从多个表格中创建视图**

只需在 SELECT 语句中包含多个表，就可以创建多个表的视图。

```
CREATE VIEW MarksView
AS
SELECT StudentDetails.NAME, StudentDetails.ADDRESS, StudentMarks.MARKS
FROM StudentDetails, StudentMarks
WHERE StudentDetails.NAME = StudentMarks.NAME;
```

在这里，您可以选择视图标记

从 MarksView 中选择*

| **名称** | **地址** | **标记** |
| 约翰 | 加尔各答 | Seventy |
| 瓦坎达 | 金奈 | Eighty |
| 吉姆(人名) | 班加罗尔 | Sixty-five |

在这里，选择标记、地址和名称。我们将寻找 MarksName =StudentName 的条件，这意味着可以选择视图。现在要显示数据，使用查询 Select * From MarksView

现在，让我们继续，了解执行的操作

## **操作**

### **更新**

您可以遵循以下规则更新视图:

*   该视图是基于一个且仅一个表定义的。
*   视图必须包含创建视图所基于的表的主键。
*   它不应该有任何由集合函数构成的字段。
*   视图的定义中不能有任何 DISTINCT 子句。
*   在其定义中不能有任何 GROUP BY 或 HAVING 子句。
*   视图的定义中不能有任何子查询。
*   如果要更新的视图基于另一个视图，则应该稍后更新。
*   视图的任何选定输出字段不得使用常量、字符串或值表达式。

**语法:**

```
UPDATE < view_name > SET<column1>=<value1>,<column2>=<value2>,.....
WHERE <condition>;
```

### **插入**

可以在视图中插入多行数据。适用于更新命令的相同规则也适用于插入命令。您可以像在数据库表中一样插入视图。

### **删除**

一旦您学习了如何在 SQL 中插入和更新视图，让我们了解如何删除视图。

可以从视图中删除数据行。适用于 Update 和 Insert 命令的规则同样适用于 Delete 命令。

**举例:**

假设您有一个客户列表表，其中包含 ID、姓名、年龄、地址和薪水。这里的查询将帮助您从表中删除特定的行。

```
SQL > DELETE FROM CUSTOMERS_VIEW
WHERE age = 20;
```

这将最终从基表 CUSTOMERS 中删除一行，这同样会反映在视图本身中。

现在，如何删除 SQL 中的视图？

### **下降**

每当你有一个视图时，很明显你需要一种方法来删除不再需要的视图。以下是如何在 SQL 中删除视图的语法。

**语法:**

```
DROP VIEW view_name;
```

只需选择视图并添加这个命令来删除它。

现在，让我们看看在 SQL 中使用视图有什么好处。

## **优势**

*   **安全性:**您可以限制用户直接访问表，并允许他们通过视图访问数据的子集。
*   **简单:**就是很多关系和表格。
*   一致性: Y 你可以在视图中隐藏复杂的查询逻辑和计算。

至此，我们结束了这篇关于 SQL 视图的文章。我希望你清楚这个博客讨论的话题。

*如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这个开源的关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/databases-certification-courses)** ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在“SQL 中的**视图”的评论部分提到它，我会回复您。***