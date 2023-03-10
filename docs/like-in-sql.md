# 你需要知道的一切，比如 SQL 中的运算符

> 原文：<https://www.edureka.co/blog/like-in-sql/>

[SQL](https://www.edureka.co/blog/sql-commands) 是一种语言，由多个命令和运算符组成。但是，当您必须基于某种模式或字符检索数据时，您将需要 LIKE 操作符。所以，在这篇关于 LIKE in SQL 的文章中，我将讨论以下主题:

![SQL - Like in SQL - Edureka](img/da752ce4512e8070f2ce0a64cdf669c5.png)

## **SQL 是什么样子的？**

该运算符与 WHERE 子句一起使用，根据特定模式检索数据。有两个通配符与 LIKE 运算符一起使用来检索数据。他们是:

*   **%** 【百分号】–匹配 0 个或以上字符。
*   **_** 【下划线】–它只匹配一个字符。

那么，既然我已经告诉了你什么是 LIKE 运算符，接下来，在本文中，让我们来理解 LIKE 运算符的语法。

## **LIKE 运算符的语法**

LIKE 运算符的语法如下:

```
SELECT column1, coulmn2, . . ., columnN
FROM tablename
WHERE columnName LIKE pattern;

```

现在，您已经对 LIKE 操作符的语法有了一个概念，接下来，在这篇关于 SQL 中的 LIKE 的文章中，让我们看看您可以使用 LIKE 操作符检索的不同模式。

## **用 LIKE 运算符检索不同的模式**

用相似运算符提及的不同模式如下:

**查询 1:** 如果要查找以“x”开头的值

**像操作:**

```
WHERE columnname LIKE ‘x%’

```

**查询 2:** 如果要查找以“x”结尾的值

**喜欢操作:**

```
WHERE columnname LIKE ‘%x’

```

**查询 3:** 如果你必须找到在任何位置有“abc”的值

**喜欢操作:**

```
WHERE columnname  LIKE ‘%abc%’

```

**查询 4:** 如果您必须查找第三个位置有“a”的值

**喜欢操作:**

```
WHERE columnname LIKE ‘__a%’

```

这里，字母“a”前有两个下划线。

**查询 5:** 如果您必须查找以“a”开头且长度至少为 5 个字符的值

**喜欢操作:**

```
WHERE columnname LIKE ‘a____%’

```

这里，字母“a”后面有 4 个下划线。

**查询 6:** 如果要找以“g”开头以“v”结尾的值

**喜欢操作:**

```
WHERE columnname LIKE ‘g%v’

```

既然我已经讨论了各种模式，接下来在这篇关于 SQL 中的 LIKE 的文章中，让我们来看一些例子。

## **相似运算符的例子**

考虑下表，我们将在其上应用 LIKE 运算符的各种运算。

| **studentID** | **学生名称** |
| one | 阿卡什 |
| Two | 米塔利 |
| three | 桑杰 |
| four | anuj |
| five | 索尼亚利 |

### **Q1。选择所有以“a”开头的学生**

```
SELECT * FROM students
WHERE studentname LIKE 'a%';

```

#### **输出:**

| **studentID** | **学生名称** |
| 1 | 阿卡什 |
| 4 | anuj |

### **Q2。选择学生名以“I”结尾的所有学生**

```
SELECT * FROM students
WHERE studentname LIKE '%i';

```

#### **输出:**

| **studentID** | **学生名称** |
| 2 | 奖牌 |
| 5 | sonali |

### **Q3。选择学生姓名中任何位置有“li”的所有学生**

```
SELECT * FROM students
WHERE studentname LIKE '%li%';

```

#### **输出:**

| **studentID** | **学生名称** |
| 2 | 奖牌 |
| 5 | sonali |

### **Q4。选择 studentname 第二个位置有“o”的所有学生:**

```
SELECT * FROM students
WHERE studentname LIKE '_o%';

```

#### **输出:**

| **studentID** | **学生名称** |
| 5 | sonali |

### **Q5。选择 studentname 以“a”开头且长度至少为 5 个字符的所有学生**

```
SELECT * FROM students
WHERE studentname LIKE 'a____%';

```

#### **输出:**

| **studentID** | **学生名称** |
| 1 | 阿卡什 |

### **Q6。选择 studentname 以“s”开头并以“y”结尾的所有学生**

```
SELECT * FROM students
WHERE studentname LIKE 's%y';

```

#### **输出:**

| **studentID** | **学生名称** |
| 3 | 桑杰 |

到此，我们结束这篇文章。我希望您理解了如何使用 LIKE 子句来检索各种数据。 *如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在这篇文章的评论部分提到它，我会回复你。*