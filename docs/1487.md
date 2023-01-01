# 关于 PHP 中的数组搜索，你需要知道的就是

> 原文：<https://www.edureka.co/blog/array-search-in-php/>

作为最好的脚本语言之一， [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 当然也很好地利用了数组。因此，在本文中，我们将按以下顺序理解 PHPin 中的数组搜索:

*   [数组搜索](#array_search)
*   [无严格参数](#Output1)

在 PHP 中搜索一个值的方法之一是使用一个循环来检查每个元素的值，但这是低效的。有各种内置函数可用于搜索数组，如 array_search、in_array、array_keys 和 array_key_exists。在这篇博客中，我们将讨论 PHP 中的 array_search

![Introduction to PHP - Array Search in PHP - Edureka](img/73cb2fcc881262d192058530c3b9285b.png)

继续这篇关于 PHP 中数组搜索的文章。

## **数组搜索**

array_search 是 PHP 内置的函数。为了在数组中搜索特定的值，我们使用这个函数来搜索特定的值并返回键。如果没有找到匹配，则返回 false。它几乎类似于 in_array()。这两个函数的主要区别在于 array_search()通常返回 key 或 index，而 in_array()根据在 search 中找到的匹配返回 TRUE 或 FALSE。

语法:array_search(value，array，strict)

**Value** :指定需要在数组中查找的值。 **数组**:指定需要查找的数组 **严格:**可选参数，查找数组中严格相同的元素，可设置为 TRUE 或 FALSE。默认情况下，它被设置为 FALSE。如果设置为 true，它将检查相同的元素。也就是说，整数 3 不同于字符串 3。

当我们将参数(搜索值& array)传递给 array_search()时，它返回带有匹配值的键，如上所述。如果没有找到匹配，则返回 false。如果找到多个匹配项，它将返回第一个匹配的键。

继续这篇关于 PHP 中数组搜索的文章

**输出 1:**

让我们看一个不使用 strict 参数的例子，

```
<?php $var=array('ashok','hanish','aravind','naveen','manikanta'); 
$val=array_search('aravind',$var); 
echo $val; ?>

```

继续这篇关于 PHP 中数组搜索的文章

**输出:2 个**

它返回 2，因为 aravind 位于数组的第二个位置。

如果找到不止一个匹配，

```
<?php $var=array('ashok','hanish','aravind','naveen','manikanta','naveen'); 
$val=array_search('naveen',$var); 
echo $val; ?>

```

继续这篇关于 PHP 中数组搜索的文章

**输出:3 个**

当在第三个索引中找到 naveen 的第一个匹配时，它返回 3。

让我们看另一个使用严格参数的例子，

```
<?php $var=array(1,2,3,4,11,22,33,44); 
$val=array_search("11",$var,true); 
echo $val; ?>

```

继续这篇关于 PHP 中数组搜索的文章

**输出 4:**

它返回时没有输出，因为数组中值的数据类型和搜索值的数据类型不属于同一类型。如果设置为 false，则忽略数据类型，默认情况下，设置为 false。

让我们通过将 strict 参数设置为 false 来查看相同的示例。

```
<?php $var=array(1,2,3,4,11,22,33,44); 
$val=array_search("11",$var,false); 
echo $val; ?>

```

本文到此结束，我希望你理解了 PHP 中的内置函数 array_search。****

*如果你发现这个博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在“**PHP 中的数组搜索**”的评论部分提出来，我会回复你的。*