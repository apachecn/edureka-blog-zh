# 如何在 PHP 中实现数组合并？

> 原文：<https://www.edureka.co/blog/array-merge-in-php/>

大多数编程语言的一个共同特征是数组。数组对于帮助我们以有组织的方式保存信息非常有用。本文将通过适当的编程演示向您介绍在 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中的数组合并。这里将涉及以下指针，

*   [什么是 array_merge？](#WhatIsarraymerge?)
*   [联合运算符](#UnionOperator)

让我们开始吧，

## **PHP 中的数组合并**

## **什么是数组 _ 合并？**

在 PHP 中， **array_merge** 是一个内置函数，用于将一个或多个数组合并成一个数组。我们使用这个函数将多个元素或值合并到一个数组中，这样一个数组的值被附加到前一个数组中。在一个数组中，如果我们重复使用同一个字符串键，那么这个键的前一个值将被下一个值覆盖。

下面给出的代码说明了上面的语句:

```
<pre>
<?php
$var = array ('p' => 'ashok', 'p' => 'tarun', 'r' =>'charan');
print_r ($var);
?>
</pre>

```

**输出:**

排列

(【p】=>塔伦【r】=>查然)

**“**<前置> 标签”用于以预格式化的方式定义文本，其中保留了制表符、分隔符、文本空格和其他格式化字符。 **array_merge()** 将需要合并的数组列表(用逗号(，)分隔)作为参数，返回一个新的数组，合并后的数组传递给函数

**语法:**

```
array_merge($array1, $array2, $array3, $array4.......$array n);
```

其中

$数组 1，$数组 2，$数组 3，$数组 4

是需要合并的多个数组。

**参数:** 用逗号分隔的数组列表被需要合并的 array_merge()函数作为参数，如语法所示。我们可以在参数中传递 n 个数组。

**返回值:** 返回一个新数组，其中所有数组的元素合并在一起，传入参数。

**例 1:**

```
<pre>
<?php
$var1 = array("php" => "back-end", "javascript"=>"front-ened",89,"ashok");
$var2 = array(56, 31, "html" => "front-end", 65);
$resultarr = array_merge($var1, $var2);
print_r($resultarr);
?>
</pre>

```

**输出:**

数组(

= >后端

= >前端 [0] = > 89 [1] = >阿肖克 [2] = > 56 [3] = > 31

= >前端 [4] = > 65

= >后端，

= >前端，[0] => 89，[1] => ashok，是第一个数组的元素列表，即 $var1 和 [0] = > 56，[1] = > 31，

= >前端，[2] => 65，是 $var2 中的元素列表。

这就把我们带到了本文的下一部分，PHP 中的数组合并

**联符**

联合运算符(+)也可用于合并 2 个数组，但它不会使用先前数组中已定义的关键字。 下面给出的代码说明了上面的语句:

```

<pre>
<?php
$var1 = array("php" => "back-end", "javascript"=>"front-ened",89,"ashok");
$var2 = array(56, 31, "html" => "front-end", 65);
$resultarr = $var1 + $var2;
print_r($resultarr);
?>
</pre>

```

**输出:**

排列

（

= >后端

= >前置的

[0] => 89

[1] = >阿肖克

= >前端

[2] => 65

)

数字键将被重新编号。下面给出的代码说明了上面的语句:

```
<pre>
<?php
$var1 = array();
$var2 = array(1 => "coder");
$resultarr = array_merge($var1, $var2);
print_r($resultarr);
?>
</pre>

```

**输出**

排列

( [0] = >编码器)

关于 PHP 中数组合并的文章到此结束，我希望你已经了解了 PHP 中数组的使用，array_merge 函数和它的一些例子以及合并数组的 Union 操作符。

*如果您发现本文相关，请查看 Edureka 提供的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在 PHP 文章的数组合并的评论部分提到它，我会回复你。*