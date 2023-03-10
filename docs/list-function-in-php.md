# 关于 PHP 中的列表函数，你只需要知道

> 原文：<https://www.edureka.co/blog/list-function-in-php/>

PHP 中的函数非常重要，尤其是控制项目流程的函数。因此，在本文中，我们将按以下顺序讨论 PHP 中的 List 函数:

*   [什么是列表功能？](#what)
*   [PHP 中 List 函数的参数](#parameters)
*   [List()函数的例子](#example)

## **什么是列表功能？**

PHP 中的 list 函数是一个内置函数，用于在执行时一次将[数组](https://www.edureka.co/blog/array-search-in-php/)的值赋给多个变量。像 array()一样，这不是一个真正的函数，而是一个语言构造。list()用于在一次操作中分配一个变量列表。

![List Function in PHP](img/bfd78573a5a8544865050ff26afb63d5.png)

这个函数只对数字数组有效。当用户将多个值赋给数组时，数组中的第一个元素是第一个变量，第二个元素将是第二个变量，依此类推，直到变量的数量达到。

变量的数量不能超过数值数组的长度，如果超过，就会产生错误。不写入参数类型和返回类型。没有 return 语句的函数隐式返回 NULL。

**语法:**

```
list($variable1, $variable2....)
```

## **PHP 中 List 函数的参数**

PHP 参数中的 list 函数将接受代码中用空格分隔的变量列表。参数就像变量一样。为了给函数增加更多的功能，我们可以添加参数。参数是在函数名后面的括号内指定的。这些变量由用户赋值。第一个变量对用户是强制性的。

| **名称** | **描述** | **必需/可选** | **类型** |
| **$variable1** | 要赋值的第一个变量 | **必需的** | 混合* |
| **$变量 2..n** | 要分配的下一个变量 | **Optional** | 混合* |

* Mixed: Mixed 表示一个参数可以接受多种(但不一定是所有)类型。

**返回值:**函数将赋值后的数组返回给用户传递的多个变量。如果 m > n，它不会给$变量 m 赋值，其中 n 是数组的长度。

现在让我们看看 PHP 中列表函数的不同例子。

## **List()函数的例子**

**例 1:**

```
<?php
$array = array(1, 2, 3, 4); 
list($a, $b, $c) = $array; 
echo "x =", ($a), "n";
echo " y =", ($b), "n";
echo " z =", ($c), "n"; 
echo "x+y-c =", ($a*$b*$c); 
?>

```

**输出:**

x=1 y =2 z =3 x+y-z =0

**例 2:**

```
<?php
$w3r1_array = array(“php”, “javascript”, “asp”);
list( $x, $y, $z) = $w3r1_array;
echo “We have covered $x, $y and $z. “;
$w3r2_array = array(“php”, “javascript”, “asp”);
list($x, $z) = $w3r2_array;
echo “We have covered $x and $z and so many other topics”;
?>

```

**输出:**

```
We have covered php, javascript and asp. We have covered php and asp and so many other topics
```

至此，我们结束了 PHP 文章中这个列表函数。我希望你明白这里到底发生了什么。

*查看 Edureka 提供的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在 **PHP** 中的“**列表函数”的评论区提及，我会回复您。***