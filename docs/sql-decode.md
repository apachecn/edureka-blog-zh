# SQL 中的 DECODE 函数有什么用？

> 原文：<https://www.edureka.co/blog/sql-decode/>

在 Oracle 中，DECODE 函数允许我们向查询添加过程性的 [if-then-else](https://www.edureka.co/blog/sql-if-statement/) 逻辑。在这篇博客中，我们将试图全面了解 [SQL](https://www.edureka.co/mysql-dba) 中的解码功能。我们将学习使用 DECODE 的各种方法，它的语法，并用例子来理解它。请继续关注我们，直到博客结束。

将要涉及的主题有:

*   [SQL 中的 DECODE 函数是什么？](#DECODEfunction)
*   [解码功能的语法](#SyntaxforDECODEfunction)
*   [解码功能的例子](#ExamplesDECODEfunction)

让我们一个一个地开始。

## **SQL 中的解码函数是什么？**

在 Oracle 中，DECODE 函数允许我们在查询中添加过程性的 if-then-else 逻辑。DECODE 将表达式与每个搜索值逐一进行比较。如果表达式等于一个搜索，那么相应的结果将由 Oracle 数据库返回。如果没有找到匹配，则返回默认值。如果省略 default，则 Oracle 返回 null。

自变量的类型可以是:

*   (NUMBER、BINARY_FLOAT 或 BINARY_DOUBLE)

如果第一个搜索结果对是数字，那么 Oracle 将比较所有搜索结果表达式和第一个表达式，以找到具有最高数字优先级的参数，将剩余的参数隐式转换为该数据类型，并返回该特定数据类型。

*   **字符类型**

如果 expr 和 search 是字符数据，那么 Oracle 使用非填充比较语义对它们进行比较。expr、search，结果可以是 CHAR、VARCHAR2、NCHAR 或 NVARCHAR2 中的任何一种数据类型。返回的字符串的数据类型为 VARCHAR2，并且与第一个结果参数使用相同的字符集。

Oracle 数据库使用 **短路评估。** 仅在与表达式比较之前评估搜索值，而不是评估所有搜索值。如果先前的搜索等于表达式，则终止求值。

Oracle 在比较之前将表达式和搜索值转换为第一个搜索值的数据类型。并将返回值转换为与第一个结果相同的数据类型。

**示例:**如果第一个结果的数据类型为 CHAR 或者第一个结果为 null，则 Oracle 会将返回值转换为 VARCHAR2 数据类型。

Oracle 认为两个空值是等价的。如果 expr 为 null，那么 Oracle [返回 NULL](https://www.edureka.co/blog/sql-commands#NULL%20Functions) ，这是第一次搜索的结果。

解码功能中可包含的最大分量数为 255。这包括表达式、搜索和结果参数。

DECODE 函数可用于以下版本的 Oracle 或 PLSQL:

甲骨文 12c、甲骨文 11g、甲骨文 10g、甲骨文 9i

**一个基本的例子:**

在以下示例中，Oracle DECODE()函数将第一个参数与第二个参数进行比较。因为它们相等，所以函数返回第二个参数，即字符串“One”。

```
SELECT
DECODE(1, 1, 'One')
FROM
dual;

```

## **解码函数的语法是:**

DECODE(表达式，搜索，结果[，搜索，结果]……[，默认(可选)])

**![DECODE in SQL - Edureka](img/449d2f270997aa1a030c0c54cd6abefc.png)表情**

需要比较的值。在比较之前，它会自动转换为第一个搜索值的数据类型。

**搜索**

与表达式进行比较的值。

**结果**

如果 expression=search，返回的值。

**默认**

如果没有匹配，解码函数将返回默认值，如果省略默认值，则该函数将返回 NULL。

**解码功能示例**

*   解码功能可在 Oracle/PLSQL 中使用，如下所示

```
SELECT bank_name,
DECODE(bank_id, 001, 'SBI',
                    002, 'ICICI',
                    003, ‘Dena',
                    'Gateway') result
FROM banks;

```

等价于上述 DECODE()语句的 [IF-THEN-ELSE 语句](https://www.edureka.co/blog/sql-if-statement/):

```
IF bank_id = 001 THEN
   result := 'SBI';

ELSIF bank_id = 002 THEN
   result := 'ICICI';

ELSIF bank_id = 003 THEN
   result := 'Dena';

ELSE
   result := 'Gateway';

END IF;

```

解码功能将逐个比较每个 bank_id 值。

*   解码函数比较两个日期(日期 1 和日期 2)，其中，如果日期 1 >日期 2，解码函数应该返回日期 2。否则，解码函数应该返回日期 1

```
DECODE((date1 - date2) - ABS(date1 - date2), 0, date2, date1)

```

如果日期 1 大于日期 2，则下面的公式等于 0:

```
(date1 - date2) - ABS(date1 - date2)

```

上述日期示例也可以修改如下:

```
DECODE(SIGN(date1-date2), 1, date2, date1)

```

*   解码将返回以下内容的语句:

如果 hours_of_work < 1 则返回 0.04 如果 hours_of_work > = 1 且< 5 则返回 0.04 如果 hours_of_work > 5 则返回 0.06

这里，您需要创建一个公式，它将为您的每个范围计算出一个数字。

```
SELECT emp_name,
DECODE(TRUNC (( hours_of_work + 3) / 4), 0, 0.04,
                                          1, 0.04,
                                          0.06) as perc_value
FROM employees;

```

这都是关于 DECODE 函数的，现在你一定已经清楚它是如何工作的，以及这个函数有多有用。现在，当[处理 SQL](https://www.edureka.co/blog/sql-tutorial/) 时，只要需要 IF-ELSE 逻辑，就试着使用它们。我希望这篇文章能帮助您理解 DECODE 语句的概念。

*如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/mysql-tutorial/) 的信息，并了解这个开源的关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在**【SQL 解码】**的评论区提及，我会回复你。*