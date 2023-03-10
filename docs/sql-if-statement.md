# 如何在 SQL 中执行 IF 语句？

> 原文：<https://www.edureka.co/blog/sql-if-statement/>

SQL Server 允许您对查询中的值执行实时编程逻辑。基于这些逻辑评估，您可以生成值作为返回数据集的一部分。在这篇博客中，你将通过例子学习如何用 SQL 实现 if 语句。以下是本博客涵盖的主题——

*   [SQL 中的 IF 条件](#IfconditioninSQL)
*   [语法](#syntax)
*   [If 条件整数示例](#int)
*   [If 条件字符串示例](#string)

## **SQL 中的 IF 条件**

IF()函数用两个参数传递，一个为 true，另一个为 false。如果条件为真，函数返回一个值，如果条件为假，则返回另一个值。

### **SQL 中 IF 语句的语法:**

IF(条件，值 _ IF _ 真，值 _ IF _ 假)

### **参数值**

| *条件* | 必选。要测试的值 |
| *值 _ 如果 _ 真* | 可选。如果 *条件* 为真则返回值 |
| *value_if_false* | 可选。如果 *条件* 为假则返回值 |

## ****If 条件整数例子****

**例 1:**

条件为真则返回 0，条件为假则返回 1:

选择 如果 (100 < 500，0，1)；

**输出:**

![IF Statement in SQL | Edureka](img/b06483937f64d5ba738097aabb641921.png)

**例 2:**

选择 如果 (900 < 500，0，1)；

**输出:**

![IF Statement in SQL | Edureka](img/3b661dd1673d20a83b779e4763ee7f55.png)

继续 SQL 中的 IF 语句，让我们看一些字符串示例。

## **If 条件字符串示例**

**例 3:**

使用字符串测试 If 条件

如果 两个字符串相同，查询返回“是”，否则返回“否”

选择 如果 (STRCMP( 【你好】【学习者】 ) = 0， 【是】 ， 【否】【T20)；

**输出:**

![IF Statement in SQL | Edureka](img/a4bf866b08d60106b2851fb531e27d50.png)

**例 4:**

选择 如果 (STRCMP( 【你好】【你好】 ) = 0， 【是】 ， 【否】【T20)；

**输出:**

![Results | Edureka](img/257ebd90a9b6f875ae620bd98d240d1c.png)

*说到这里，我们结束这篇关于“SQL 中的 If 语句”的博客。我希望它增加了你的知识。如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这个开源的关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*