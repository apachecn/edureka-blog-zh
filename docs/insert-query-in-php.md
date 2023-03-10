# 如何在 PHP 中实现插入查询？

> 原文：<https://www.edureka.co/blog/insert-query-in-php/>

在开始这篇**插入查询的 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/)** 文章之前，你必须了解[如何在 MySQL](https://www.edureka.co/blog/data-retrieval-in-php/#HowToCreateADatabase) 中创建数据库。因此，不再拖延，让我们从这篇文章开始吧，

为了在数据库表中插入新行，我们在 PHP 中使用了 INSERT INTO 语句。我们通过传递 mysqli_query()在 PHP 中执行插入查询。如果您想在一次调用中执行多个查询，我们使用 mysqli_multi_query，因为 mysqli_query 不会执行多个查询来防止 SQL 注入。在我们继续下一步之前，请注意以下语法，

**INSERT INTO TABLE 语法:**INSERT INTO TABLE _ NAME(column 1，column2，… columnN) VALUES (value1，value2，…valueN)；

**mysqli _ query()的语法:** mysqli_query(connection，query，result mode)；

**mysqli _ multi _ query():**mysqli _ multi _ query(连接，查询)；

现在基础知识已经介绍完毕，让我们来看看 PHP 中插入查询所涉及的指针，

*   [如何使用 MYSQL 面向对象的程序将数据插入 MYSQL？](#HowtoinsertdataintoMYSQLusingMySQLiObject-orientedProcedure?)
*   [如何使用 MYSQL 过程化过程将数据插入 MYSQL？](#HowtoinsertdataintoMYSQLusingMySQLiProceduralProcedure?)
*   [如何使用 MySQL 面向对象的程序将多条记录插入 MySQL？](#HowtoinsertmultiplerecordsintoMySQLusingMySQLiObject-orientedProcedure?)
*   [如何使用 MySQL 过程化程序在 MySQL 中插入多条记录？](#HowtoinsertmultiplerecordsintMySQLusingMySQLiProceduralProcedure?)

那么让我们开始吧，

**如何使用 MySQLi** **面向对象的程序插入数据？**

```
<?php
$server= "localhost";
$user = "root";
$password = "";
$db = "feedback";
// Create connection
$conn = new mysqli($server, $user, $password, $db);
// Check connection
if ($conn->connect_error)
{
die("Connection failed: " . $conn->connect_error);
}
$sql =INSERT INTO data VALUES(&lsquo;ashok','you are awesome bro')";
if ($conn->query($sql) === TRUE)
{
echo "feedback sucessfully submitted";
}
else
{
echo "Error: " . $sql . "<br>" . $conn->error;
}
$conn->close();
?>

```

继续 PHP 文章中的插入查询，

**如何使用 MySQLi** **程序化过程插入数据？**

继续 PHP 文章中的插入查询，

```
<?php
$server= "localhost";
$user = "root";
$password = "";
$db = "feedback";
// Create connection
$conn = mysqli_connect($server, $user, $password, $db);
// Check connection
if (!$conn)
{
die("Connection failed: " . mysqli_connect_error());
}
$sql =INSERT INTO data VALUES(&lsquo;ashok','you are awesome bro')";
if (mysqli_query($conn, $sql))
{
echo "feedback sucessufully submitted";
}
else
{
echo "Error: " . $sql . "<br>" . mysqli_error($conn);
}
mysqli_close($conn);
?>

```

**如何使用 MySQLi** **面向对象的程序插入多条记录？**

```
<?php
$server= "localhost";
$user = "root";
$password = "";
$db = "feedback";
// Create connection
$conn = new mysqli($server, $user, $password, $db);
// Check connection
if ($conn->connect_error)
{
die("Connection failed: " . $conn->connect_error);
}
$sql =INSERT INTO data VALUES(&lsquo;ashok','you are awesome')";
$sql =INSERT INTO data VALUES(&lsquo;sushma','you are mad')";
$sql =INSERT INTO data VALUES(&lsquo;charan','you are an idiot')";
$sql =INSERT INTO data VALUES(&lsquo;tarun','you are scanner')";
if ($conn->multi_query($sql) === TRUE)
{
echo "feedbacks successfully submitted";
}
else
{
echo "Error: " . $sql . "<br>" . $conn->error;
}
$conn->close();
?>

```

继续 PHP 文章中的插入查询，

**如何使用 MySQLi** **程序过程插入多条记录？**

```
<?php
$server= "localhost";
$user = "root";
$password = "";
$db = "feedback";
// Create connection
$conn = mysqli_connect($server, $user, $password, $db);
// Check connection
if (!$conn)
{
die("Connection failed: " . mysqli_connect_error());
}
$sql =INSERT INTO data VALUES(&lsquo;ashok','you are awesome')";
$sql =INSERT INTO data VALUES(&lsquo;sushma','you are mad')";
$sql =INSERT INTO data VALUES(&lsquo;charan','you are an idiot')";
$sql =INSERT INTO data VALUES(&lsquo;tarun','you are scanner')";
if (mysqli_multi_query($conn, $sql))
{
echo "feedbacks succesfully submitted";
} else
{
echo "Error: " . $sql . "<br>" . mysqli_error($conn);
}
mysqli_close($conn);
?>

```

本文到此结束，我希望你已经了解了如何使用 MySQL面向对象&过程将数据插入 MYSQL，以及如何使用 MYSQL面向对象&过程将多条记录插入 MYSQL。

关于 PHP 中插入查询的这篇文章到此结束，我希望你已经学会了如何创建一个数据库，存储从用户输入的表单中获得的数据，并从数据库中获取用户数据。

如果您在 PHP 文章中找到了相关的数据检索，请查看 Edureka 的  [**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。

*有问题吗？请在这篇文章的评论部分提到它，我会回复你。*