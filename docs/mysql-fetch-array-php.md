# 如何在 PHP 中实现 Mysql_fetch_array

> 原文：<https://www.edureka.co/blog/mysql-fetch-array-php/>

对于 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) ，获取数据是一个重要的方面。在本文中，我们将按照以下顺序理解 mysql_fetch_array 方法:

*   [什么是 Mysql_fetch_array？](#what)
*   [代码为 Mysql_fetch_array](#code)
*   [通过 mysql_fetch_array 获取行数据](#row)

## **什么是 Mysql_fetch_array？**

该函数将记录集中的一行作为关联数组和/或数值数组返回。 该函数从 mysql_query()函数中获取一行，如果为真，则返回一个数组，如果失败，则返回 FLASE。

![sql_mysql](img/a6acae804cd4eaf94c4a6a1edcc96fa7.png)

Mysql 没有获取数组的功能。mysql_fetch_array 是一个 PHP 函数，如果你想知道当你使用 mysql_query 函数查询一个 mysql 数据库时返回了什么，它将允许你访问存储在真正的 mysql_query 返回的结果中的数据。这不是你可以直接操纵的。

**语法**

`mysql_fetch_array(data,array_type)`

指定要使用的数据指针的必需数据，该数据指针是 mysql_query()函数的结果

**数组类型**

可能的值有:

*   *mysql_assoc 这是一个关联数组
*   *mysql_num 这是一个数值数组
*   *mysql_both 这是默认的还是 both

## **代码**

```
<?php
$con=mysql_connect(“local12”,”AAAA”,zzzz12”);
If (!$con)
{
Die(‘could not connect: ‘ .mysql_error());
}
$db_selected=mysql_select_db(“test_db”,$con);
$sql=”CHOOSE*from person where lastname=’ Refsnes’ ’’ ;
$result=mysql_query($sql,$con);
Print_r(mysql_fetch_array($result));
Mysql_close($con);?>

```

**输出:**

`Array`

`{`

`[0] => Refsnes`

`[lastname] => Refsnes`

`[1] =>seesee`

`[FirstName] => seesee`

`}`

**一行数据**

mysql _ fetch _ array 函数将一个 Mysql 查询资源作为参数

($result)，它将返回 mysql_query 返回的第一行数据。

![mysql_fetch_array-table](img/bc3215a0580854754f75aad18a9dc8a8.png)

## **通过 mysql_fetch_array 获取行数据**

Mysql_fetch_array 将以关联数组的形式返回 Mysql 资源中的第一行，并且可以使用表的列名来访问 Mysql 结果的列。

**上表的 PHP 和 MySQL 代码**

```
>?php
$query=”choose*from example”;
$result=mysql_query($query) or die (mysql_error());
$row=mysql_fetch_array($result) or die(mysql_error());
Echo$row[‘name’].”-“.$row[‘age’];
?>

```

**输出:**

`asasas-23`

至此，我们结束了这篇 mysqql_fetch_array 文章。我希望您已经了解了如何在 PHP 中使用 mysql_fetch_array 方法来获取所需的数据。

*查看 Edureka 提供的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在这篇文章的评论部分提到它，我会回复你。*