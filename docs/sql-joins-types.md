# 理解 SQL 连接–关于 SQL 连接您需要知道的一切

> 原文：<https://www.edureka.co/blog/sql-joins-types>

结构化查询语言是关系数据库的核心，在它的帮助下我们可以处理数据。它为我们提供了各种各样的特性，比如触发器、注入、托管和连接，这是[掌握 SQL](https://www.edureka.co/mysql-dba) 最重要的概念之一。在这篇关于 SQL 连接的文章中，我将讨论 SQL 中使用的各种类型的连接。

本文将涵盖以下主题

## **什么是联接？**

SQL 中的连接是用于根据两个或多个表之间的相关列来组合这些表中的行的命令。当用户试图从具有一对多或多对多关系的表中提取数据时，主要使用。

现在，您已经知道了联接的含义，接下来让我们学习不同类型的联接。

## **SQL 中有多少种联接类型？**

您需要了解的主要有四种类型的连接。他们是:

*   [内部加入](#INNER%20JOIN)
*   [完全加入](#FULL%20JOIN)
*   [左加入](#LEFT%20JOIN)
*   [右加入](#RIGHT%20JOIN)

你可以参考下图。

![Types Of Joins In SQL - SQL Joins - Edureka](img/36b3a4e323e6d1112b8186fd54ec08a7.png)

## 我如何知道在 SQL 中使用哪个连接？

让我们逐一研究一下。为了让您更好地理解这个概念，我将考虑下面三个表，向您展示如何在这些表上执行连接操作。

### **员工表:**

| **【empid】** | **EmpFname** | **官名** | **年龄** | **EmailID** | **手机** | **地址** |
| one | Vardhan | 库马尔 | Twenty-two | vardy@abc.com | Nine billion eight hundred and seventy-six million five hundred and forty-three thousand two hundred and ten | 德里 |
| Two | 希马尼 | 夏尔马 | Thirty-two | 喜马拉雅山@abc.com | Nine billion nine hundred and seventy-seven million five hundred and fifty-four thousand four hundred and twenty-two | 孟买 |
| three | Aayushi | 什雷思 | Twenty-four | aayushi@abc.com | Nine billion nine hundred and seventy-seven million five hundred and fifty-five thousand one hundred and twenty-one | 加尔各答 |
| four | Hemanth | 夏尔马 | Twenty-five | hemanth@abc.com | Nine billion eight hundred and seventy-six million five hundred and forty-five thousand six hundred and sixty-six | 本加卢鲁 |
| five | 毛衣 | 卡普尔 | Twenty-six | swatee@abc.com | Nine billion five hundred and forty-four million five hundred and sixty-seven thousand seven hundred and seventy-seven | 海得拉巴 |

### **项目表:**

| **ProjectID** | **【empid】** | **ClientID** | **项目名称** | **项目开始日期** |
| One hundred and eleven | one | three | 项目 1 | 2019-04-21 |
| Two hundred and twenty-two | Two | one | 项目 2 | 2019-02-12 |
| Three hundred and thirty-three | three | five | 项目 3 | 2019-01-10 |
| Four hundred and forty-four | three | Two | 项目 4 | 2019-04-16 |
| Five hundred and fifty-five | five | four | 项目 5 | 2019-05-23 |
| Six hundred and sixty-six | nine | one | 项目 6 | 2019-01-12 |
| Seven hundred and seventy-seven | seven | Two | 项目 7 | 2019-07-25 |
| Eight hundred and eighty-eight | eight | three | 项目 8 | 2019-08-20 |

**客户端表:**

| **ClientID** | **ClientFname** | **ClientLname** | **年龄** | **ClientEmailID** | **手机** | **地址** | **【empid】** |
| one | 苏珊(女子名) | 史密斯（姓氏） | Thirty | susan@adn.com | Nine billion seven hundred and sixty-five million four hundred and eleven thousand two hundred and thirty-one | 加尔各答 | three |
| Two | 莫伊斯 | 阿里 | Twenty-seven | 月@jsq.com | Nine billion eight hundred and seventy-six million five hundred and forty-three thousand five hundred and sixty-one | 加尔各答 | three |
| three | 身体 | 保罗 | Twenty-two | soma@wja.com | Nine billion nine hundred and sixty-six million three hundred and thirty-two thousand two hundred and eleven | 德里 | one |
| four | 扎伊娜卜 | 达吉纳瓦拉 | Forty | zainab@qkq.com | Nine billion nine hundred and fifty-five million eight hundred and eighty-four thousand four hundred and twenty-two | 海得拉巴 | five |
| five | 巴斯卡尔 | 雷迪 | Thirty-two | bhaskar@xyz.com | Nine billion six hundred and thirty-six million nine hundred and sixty-three thousand two hundred and sixty-nine | 孟买 | Two |

### **内部加入**

这种类型的连接返回那些在两个表中都有匹配值的记录。因此，如果您在 Employee 表和 Projects 表之间执行内部连接操作，那么在这两个表中具有匹配值的所有元组都将作为输出给出。

#### **语法:**

```
SELECT Table1.Column1,Table1.Column2,Table2.Column1,....
FROM Table1
INNER JOIN Table2
ON Table1.MatchingColumnName = Table2.MatchingColumnName;
```

*NOTE: You can either use the keyword INNER JOIN or JOIN to perform this operation.*

#### ****例如:****

```
 **SELECT Employee.EmpID, Employee.EmpFname, Employee.EmpLname, Projects.ProjectID, Projects.ProjectName
FROM Employee
INNER JOIN Projects ON Employee.EmpID=Projects.EmpID;** 
```

#### ****输出:****

| **【empid】** | **EmpFname** | **官名** | **ProjectID** | **项目名称** |
| one | Vardhan | 库马尔 | One hundred and eleven | 项目 1 |
| Two | 希马尼 | 夏尔马 | Two hundred and twenty-two | 项目 2 |
| three | Aayushi | 什雷思 | Three hundred and thirty-three | 项目 3 |
| three | Aayushi | 什雷思 | Four hundred and forty-four | 项目 4 |
| five | 毛衣 | 卡普尔 | Five hundred and fifty-five | 项目 5 |

### ****完全加入****

**全连接或全外连接返回在左表(表 1)或右表(表 2)中匹配的所有记录。**

#### ****语法:****

```
**SELECT Table1.Column1,Table1.Column2,Table2.Column1,....
FROM Table1
FULL JOIN Table2
ON Table1.MatchingColumnName = Table2.MatchingColumnName;**
```

#### ****例如:****

```
 **SELECT Employee.EmpFname, Employee.EmpLname, Projects.ProjectID
FROM Employee
FULL JOIN Projects
ON Employee.EmpID = Projects.EmpID;** 
```

#### ****输出:****

| **EmpFname** | **官名** | **ProjectID** |
| Vardhan | 库马尔 | 111 |
| 希马尼 | 夏尔马 | Two hundred and twenty-two |
| Aayushi | 什雷思 | Three hundred and thirty-three |
| Aayushi | 什雷思 | Four hundred and forty-four |
| Hemanth | 夏尔马 | 空 |
| 毛衣 | 卡普尔 | Five hundred and fifty-five |
| 空 | 空 | Six hundred and sixty-six |
| 空 | 空 | Seven hundred and seventy-seven |
| 空 | 空 | Eight hundred and eighty-eight |

### ****左加入****

**LEFT JOIN 或 LEFT OUTER JOIN 返回左表中的所有记录以及右表中满足条件的记录。此外，对于右表中没有匹配值的记录，输出或结果集将包含空值。**

#### ****语法:****

```
**SELECT Table1.Column1,Table1.Column2,Table2.Column1,....
FROM Table1
LEFT JOIN Table2
ON Table1.MatchingColumnName = Table2.MatchingColumnName;**
```

#### ****举例:****

```
 **SELECT Employee.EmpFname, Employee.EmpLname, Projects.ProjectID, Projects.ProjectName
FROM Employee
LEFT JOIN
ON Employee.EmpID = Projects.EmpID ;** 
```

#### ****输出:****

| **EmpFname** | **官名** | **ProjectID** | **项目名称** |
| Vardhan | 库马尔 | One hundred and eleven | 项目 1 |
| 希马尼 | 夏尔马 | Two hundred and twenty-two | 项目 2 |
| Aayushi | 什雷思 | Three hundred and thirty-three | 项目 3 |
| Aayushi | 什雷思 | Four hundred and forty-four | 项目 4 |
| 毛衣 | 卡普尔 | Five hundred and fifty-five | 项目 5 |
| Hemanth | 夏尔马 | 空 | 空 |

### ****右加入****

**右连接或右外连接返回右表中的所有记录，以及满足左表中某个条件的记录。此外，对于左侧表中没有匹配值的记录，输出或结果集将包含空值。**

#### ****语法:****

```
**SELECT Table1.Column1,Table1.Column2,Table2.Column1,....
FROM Table1
RIGHT JOIN Table2
ON Table1.MatchingColumnName = Table2.MatchingColumnName;**
```

#### ****举例:****

```
 **SELECT Employee.EmpFname, Employee.EmpLname, Projects.ProjectID, Projects.ProjectName
FROM Employee
RIGHT JOIN
ON Employee.EmpID = Projects.EmpID;** 
```

#### ****输出:****

| **EmpFname** | **官名** | **ProjectID** | **项目名称** |
| Vardhan | 库马尔 | One hundred and eleven | 项目 1 |
| 希马尼 | 夏尔马 | Two hundred and twenty-two | 项目 2 |
| Aayushi | 什雷思 | Three hundred and thirty-three | 项目 3 |
| Aayushi | 什雷思 | Four hundred and forty-four | 项目 4 |
| 毛衣 | 卡普尔 | Five hundred and fifty-five | 项目 5 |
| 空 | 空 | Six hundred and sixty-six | 项目 6 |
| 空 | 空 | Seven hundred and seventy-seven | 项目 7 |
| 空 | 空 | Eight hundred and eighty-eight | 项目 8 |

**现在，让我们继续本文的下一部分，即在您的访谈中关于 SQL 连接的最常见问题。**

## ****关于加入**最常见的问题问 **

### ****问题 1:什么是自然连接，在什么情况下使用自然连接？****

### ****解:****

**自然连接也是一种连接操作，用于根据两个表中的列提供输出，这种连接操作必须在两个表之间实现。为了理解使用自然联接的情况，您需要理解自然联接和内部联接之间的区别。**

**自然联接和内部联接的主要区别取决于返回的列数。例如，参见下文。**

**![Tables Example - SQL Joins - Edureka](img/101b1a70c5bec28cf84ed9343eade4b9.png)**

**现在，如果对这两个表应用内部连接，您将看到如下输出:**

**![Tables Inner Join Example - SQL Joins - Edureka](img/e790fc0ab56ea7e6cced911396bf7ddb.png)**

**如果在上面两个表上应用自然连接，输出将如下所示:**

**![Tables Natural Join Example - SQL Joins - Edureka](img/b12fe40d797bfe7a46e757f7bb3bea13.png)从上面的例子中，你可以清楚地看到，从 Inner Join 返回的列数多于从 Natural Join 返回的列数。因此，如果您希望获得较少列数的输出，那么您可以使用自然连接**

### ****问题 2:如何使用 joins 映射多对多关系？****

### ****解:****

**要使用连接映射多对多关系，您需要使用两个连接语句。**

**例如，如果我们有三个表(员工、项目和技术)，让我们假设每个员工都在一个项目上工作。因此，一个项目不能分配给一个以上的员工。所以，这基本上是一对多的关系。**

**现在，类似地，如果你考虑到，一个项目可以基于多种技术，任何技术都可以在多个项目中使用，那么这种关系就是多对多关系。**

**要对这种关系使用连接，您需要用两个外键来构建数据库。为此，您必须创建以下三个表:**

***   项目*   技术*   项目到技术**

**project_to_technologies 表在每一行中都保存了项目技术的组合。此表将“项目”表中的项目映射到“技术”表中的项目，以便可以将多个项目分配给一项或多项技术。**

**一旦创建了表，就使用下面两个 JOIN 语句将上面所有的表链接在一起:**

***   项目到技术到项目*   项目对技术对技术**

### ****问题 3:什么是哈希连接？****

### ****解:****

**散列连接也是一种连接类型，用于连接大型表，或者在用户需要大部分连接的表行的情况下。**

**哈希连接算法是一个两步算法。请参考下面的步骤:**

***   **构建阶段:** C 在左侧输入中创建一个内存中散列索引*   **探测阶段:**遍历右侧输入，每次查找一行，使用上一步创建的索引找到匹配项。**

### ****问题四:什么是自我&交叉加入？****

### ****解:****

#### ****自加入****

**换句话说，自连接是一个表与自身的连接。这意味着表中的每一行都与其自身连接。**

#### ****交叉连接****

**交叉联接是一种联接类型，其中一个联接子句应用于一个表的每一行和另一个表的每一行。此外，当使用 WHERE 条件时，这种类型的连接表现为内部连接，而当 WHERE 条件不存在时，它表现为笛卡尔乘积。**

### ****问题 5:可以用 SQL 连接 3 个表吗？****

### ****解:****

**是的。要对 3 个表执行 JOIN 操作，需要使用 2 个 JOIN 语句。你可以参考第二个问题，通过一个例子来理解如何连接 3 个表。**

***NOTE: To apply a JOIN operation between ‘n‘ tables, you have to use ‘n-1‘ JOIN statements.*******Now that you know SQL Joins, I’m sure you’re curious to learn more about SQL. Here’s a list of articles that you can refer to:

1.  [SQL 命令](https://www.edureka.co/blog/sql-commands)
2.  [SQL 数据类型](https://www.edureka.co/blog/sql-data-types)
3.  [Spark SQL](https://www.edureka.co/blog/spark-sql-tutorial/)
4.  [SQL 面试问题](https://www.edureka.co/blog/interview-questions/sql-interview-questions)
5.  [什么是 MYSQL？](https://www.edureka.co/blog/what-is-mysql/)

至此，我结束了这篇关于 SQL 连接的文章。我希望您喜欢阅读这篇关于 SQL 连接的文章。我们已经看到了帮助您编写查询和处理数据库的不同命令。 *如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训包含讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在“ **SQL Joins** ”的评论部分提及，我会回复您。*****