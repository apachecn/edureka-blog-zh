# 通过示例了解 SQL 中的连接

> 原文：<https://www.edureka.co/blog/concatenate-sql/>

一般来说，连接是指将一串字符串绑定到一个字符串中。在 [SQL](https://www.edureka.co/blog/sql-tutorial/) 中，这是通过一个名为 CONCAT()的函数实现的。它接受多达 255 个输入字符串并将它们连接在一起。在本文中，我们将学习如何在 SQL 中使用 CONCAT()函数。本博客涵盖了以下主题:

*   [SQL 中的 CONCAT 函数](#concat)
*   [如何在 SQL 中使用 CONCAT？](#use)
*   [串联参数](#params)
*   [CONCAT 函数示例](#eg)
    *   [使用 CONCAT 与表格值](#table)
    *   [使用空值串联](#null)

## **SQL 中的 CONCAT 函数**

在 SQL 中，字符串的连接是通过 CONCAT()函数实现的。在使用 CONCAT 函数时，您应该记住一些事情。

*   如果只有一个字符串作为输入传递，CONCAT 函数将引发错误。至少要有两个字符串作为输入，CONCAT 函数才能顺利工作。

*   如果有的话，非字符串值作为输入被传递。CONCAT 函数将在连接之前隐式转换这些值。

*   CONCAT 函数最多可以连接 255 个输入字符串。

## **![CONCAT Function In SQL](img/80515ec0aa9e1a724b66677ada959e6f.png)**

## **如何在 SQL 中使用 CONCAT**

为了理解如何在 SQL 中使用 CONCAT，让我们举一个简单的例子。理想情况下，串联的工作方式是这样的，假设我们有两个字符串，“edureka”，“SQL”。如果我们连接这两个字符串，我们将得到一个结果字符串或连接字符串作为“edureka SQL”。对于 CONCAT 函数也是如此。

假设我们有相同的字符串“edureka”和“SQL”，为了连接这两个字符串，我们将编写以下命令。

```
SELECT CONCAT("edureka", "SQL");

```

**输出:** `edurekaSQL`

我们可以使用加法“+”[运算符](https://www.edureka.co/blog/sql-operators/)将两个或多个字符串相加。

```
SELECT "edureka" + "SQL";

```

**输出:** `edurekaSQL`

为了用分隔符分隔字符串，我们也可以使用 CONCAT_WS()函数。看看下面的例子，了解它是如何工作的。

```
SELECT CONCAT_WS("-" , "EDUREKA", "SQL");

```

**输出:** `EDUREKA-SQL`

因此，您可以使用这些方法中的任何一种来连接 SQL 中的字符串。让我们再看一下传递给 CONCAT 函数的参数。

## **串联参数**

*   CONCAT 参数–唯一必需的参数是需要用逗号分隔的字符串值。

*   加法运算符参数——除了需要连接的逗号分隔的字符串之外，它不需要任何东西。

*   CONCAT_WS 参数——第一个参数是您想要使用的分隔符，在此之后，所有被连接的字符串被添加，所有字符串用逗号分隔。

## **CONCAT 函数示例**

让我们举一个使用字符串的简单例子。

```
SELECT 'edureka' + 'SQL' as full_name;

```

**输出:** `edurekaSQL`

让我们再举一个例子

```
SELECT CONCAT('edureka', 'sql');

```

**输出:** `edurekasql`

现在让我们试着理解连接是如何处理表值的。

### **使用 CONCAT 与表格值**

让我们考虑一个具有以下值的表。

![table - concatenate sql - edureka](img/add1b6d996dd2fb27e4ebc51f2996ae8.png)

现在让我们试着把名和姓连接起来。

```
SELECT first_name,last_name, 
CONCAT(first_name,' ',last_name)full_name 
FROM N
ORDER BY full_name

```

**输出:![table 2 - concatenate sql - edureka](img/56b4b5d5b84e6fa512a100f6b8697bae.png)**

考虑表中的空值，让我们理解连接如何处理空值。

### **使用空值连接**

让我们假设表中有几个空值。当值为 NULL 时，CONCAT 函数使用 empty 进行串联。

```
SELECT first_name,last_name,phone, 
CONCAT(first_name,' ',last_name,phone)full_name 
FROM N
ORDER BY full_name

```

**输出:![table 3 - concatenate sql - edureka](img/decfe3435cd16a7173fa23d38a6a60bc.png)**

以上是关于 SQL 中的串联的所有内容，我希望这篇文章能够帮助您增加知识的价值。更多关于 SQL 或者数据库的信息，可以参考我们这里的综合阅读清单:  [**数据库 Edureka**](https://www.edureka.co/blog/category/databases/) 。

*如果您希望获得有关 MySQL 的结构化培训，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，它附带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

有问题要问我们吗？请在“**连接 SQL** ”的评论部分提到它，我会给你回复。