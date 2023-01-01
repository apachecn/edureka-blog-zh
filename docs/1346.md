# 如何在 PHP 中实现 str_replace？

> 原文：<https://www.edureka.co/blog/str_replace-in-php/>

近来，随着大量数据处理的发生，使用字符模式变得非常重要。在这篇文章中，我们将看一看 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中的 str_replace，试图详细理解这个概念。

本文将涉及以下几点，

*   [什么是 str_replace()？](#Whatisstr_replace()?)
*   [什么是 str_ireplace()？](#Whatisstr_ireplace()?)

所以让我们从这篇关于 PHP 中 str_replace 的文章开始吧，

## **PHP 中的 str _ replace**

为了用字符串中的一些其他字符替换一些字符，我们在 PHP 中提供了一些功能，这些功能遵循一些特定的规则。他们是:

*   如果需要在数组中查找字符串，则返回一个数组。
*   如果需要在数组中查找字符串，则对每个数组元素进行查找和替换。
*   如果查找和替换都是数组，并且替换的元素比查找的少，则使用空字符串。
*   如果查找是一个数组，替换是一个字符串，替换字符串将用于每个查找值

继续这篇关于 PHP 中 str_replace 的文章，让我们看看下面的函数，

## **什么是 str_replace()？**

str_replace()是一个内置函数，用于将字符串中的一些字符替换为另一些字符。即替换一个单词在字符串中的所有出现。

**语法:** str_replace(查找、替换、字符串、计数)；

**Find** :该参数可以是字符串，也可以是数组类型，指定要查找和替换的字符串。

**Replace:** 该参数也可以是字符串或数组类型，指定我们要替换的字符串。

**String:** 该参数指定了我们要搜索和替换的字符串或字符串数组。

**计数:** 该参数是可选的，其值设置为替换操作的总次数。

让我们看一个例子，其中用于查找和替换的参数是字符串类型:

```
<?php
$str = 'ashok love to code because ashok wants to get placed in a good product based company';
echo str_replace("ashok", "sushma", $str);
?>

```

```
sushma love to code because sushma wants to get placed in a good product based company
```

在上面的例子中，每次出现“ashok”都被替换为“sushma”。

让我们看另一个例子，其中用于查找和替换的参数是一个数组类型:

```
<?php
$str = "Your friends are Tarun, Charan, Adarsh, Sabid";
// Array that contains the elements to be searched
$find = array("Tarun", "Charan", "Sabid");
// Array that contains the string s tor replaced with searched string
$replace= array("Sushma", "Vaibhav", "Chintan");
$output = str_replace($find, $replace, $str);
print_r($output);
?>

```

## **输出**

你的朋友是苏希玛，瓦伊巴夫，阿达什，钦坦

当参数为数组类型时，在字符串中搜索查找参数的所有元素，并用替换参数中的相应元素替换。如果 replace 参数中的元素数量少于 find 数组中的元素数量，那么如果 find 参数的附加元素在字符串参数中出现，那么它们将被替换为空字符串。如果字符串参数也是一个数组而不是字符串，那么将搜索字符串的所有元素。

这个函数是区分大小写的，为了解决这个问题，我们使用 str_ireplace()来执行不区分大小写的匹配。

继续这篇关于 PHP 中 str_replace 的文章，让我们看看下面的函数，

## **什么是 str_ireplace()？**

str_ireplace()是一个类似于 str_replace()的内置函数，即替换字符串中区分大小写的字符。

**语法:** str_ireplace(查找、替换、字符串、计数)；

让我们看一个例子，其中用于查找和替换的参数是字符串类型(不考虑字符串的大小写):

```
<?php
$str = 'ashok love to code because Ashok wants to get placed in a good product based company';
echo str_ireplace("ashok", "sushma", $str);
?>

```

## **输出:**

sushma 喜欢编码，因为 sushma 想进入一家以产品为基础的好公司

让我们看另一个例子，其中用于查找和替换的参数是一个数组类型(不考虑字符串的大小写):

```
<?php
$str = "Your friends are Tarun, Charan, Adarsh, Sabid";
// Array that contains the elements to be searched
$find = array("tarUn", "ChaRan", "saBiD");
// Array that contains the string s tor replaced with searched string
$replace= array("Sushma", "Vaibhav", "Chintan");
$output = str_ireplace($find, $replace, $str);
print_r($output);
?>

```

## **输出**

你的朋友是苏希玛，瓦伊巴夫，阿达什，钦坦

本文到此结束，我希望你已经了解了 PHP 中的两个内置函数，即**str _ replace()**和 **str_ireplace()** ，并给出了合适的例子。

如果您发现本文中的 str_replace 与 PHP 相关，请查看 Edureka 提供的  [**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，该公司是一家值得信赖的在线学习公司，拥有遍布全球的 25 万多名满意学习者。

*有问题吗？请在这篇文章的评论部分提到它，我会回复你。*