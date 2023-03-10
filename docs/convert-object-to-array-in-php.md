# PHP 中如何把对象转换成数组？

> 原文：<https://www.edureka.co/blog/convert-object-to-array-in-php/>

由类定义的数据结构的单个实例是一个对象。我们也将对象命名为实例。一般我们定义一个类一次，然后做很多属于它的对象。在单个名称中存储一个或多个相似类型值的数据结构之一是数组，但是 PHP 中的关联数组与简单的 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 数组有所不同。关联数组通常用于存储键值对。在这篇文章中，我们将学习“如何在 PHP 中将对象转换为数组？”

本文将涉及以下几点，

*   [将对象类型转换为一个数组](#TypeCastingObjectToAnArray)
*   [使用 Json 解码和 Json 编码](#UsingJsonDecodeAndJsonEncode)

那么让我们开始吧

**PHP 中如何将对象转换成数组？**

**类型向一个数组中施放对象**

为了将一个数据类型变量转换成不同的数据类型，我们可以使用类型转换，这只是一种数据类型的显式转换。通过使用 PHP 支持的类型转换规则，

它将把一个 PHP 对象转换成一个数组。

**语法:** $Array_var =(数组)$ Obj

下面的例子演示了在 PHP 中如何将对象类型转换成数组

```
<?php
class hotel
{
var $item1;
var $item2;
var $item3;
function __construct( $food1, $food2, $food3)
{
$this->item1 = $food1;
$this->item2 = $food2;
$this->item3 = $food3;
}
}
// Create object for class(hotel)
$food = new hotel("biriyani", "burger", "pizza");
echo "Before conversion : ";
echo "<br>";
var_dump($food);
echo "<br>";
// Coverting object to an array
$foodArray = (array)$food;
echo "After conversion :";
var_dump($foodArray);
?>
```

继续这篇关于如何在 PHP 中将对象转换成数组的文章？

**使用 Json 解码& Json 编码**

JSON 编码的字符串被 json_decode 函数接受，并将其转换成 PHP 变量，另一方面，json_encode 返回给定值的 JSON 编码的字符串

**语法:**$ Array _ var = JSON _ decode(JSON _ encode($ obj)，true)

下面的例子演示了在 PHP 中使用 json_decode & json_encode 将对象转换成数组。

```
<?php
class hotel
{
var $var1;
var $var2;
function __construct( $bill, $food )
{
$this->var1 = $bill;
$this->var2 = $food;
}
}
// Creating object
$food = new hotel(500, "biriyani");
echo "Before conversion:";
echo "<br>";
var_dump($food);
echo "<br>";
// Converting object to associative array
$foodArray = json_decode(json_encode($food), true);
echo "After conversion:";
var_dump($foodArray);
?>
```

这就把我们带到了这篇关于如何在 PHP *中将对象转换成数组的文章的结尾。*

*如果您发现这篇 PHP 文章相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在“如何在 PHP 中将对象转换为数组”文章的评论部分提到它，我会回复您。*