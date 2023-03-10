# PHP 中的数组排序:你需要知道的一切

> 原文：<https://www.edureka.co/blog/array-sort-in-php/>

排序是指根据数据项之间的某种线性关系，将数据按特定的顺序排列，可以是字母、数字、升序或降序。也提高了搜索的效率。本文关注的是 [PHP 中的数组排序。](https://www.edureka.co/blog/php-tutorial-for-beginners/)

本文将涉及以下几点，

*   [sort()](#sort())
*   [rsort()](#rsort())
*   [arsort()](#arsort())
*   [krsort()](#krsort())
*   [asort()](#asort())
*   [ksort()](#ksort())
*   [natsort()](#natsort())
*   [natcasesort()](#natcasesort())
*   [uasort()](#uasort())
*   [uksort()](#uksort())
*   [usort()](#usort())

让我们开始吧，

## **Sort():PHP 中的数组排序**

使用这种方法，默认情况下，数组按升序排序。

```

<pre>
<?php
$var_array = array(10,20,30,40);
sort($var_array);
print_r($var_array);
?>
</pre>

```

**输出:**

数组

([0]=>10[1]=>20[2]=>30[3]=>40)

进一步让我们来看看这个，

## **rsort():PHP 中的数组排序**

数组按降序排序。

```

<pre>
<?php
$alphabets = array('a','h','c','f');
rsort($alphabets);
foreach ($alphabets as $key => $val) {
echo "$key = $valn";
}
?>
</pre>

```

**输出:**

0 = h

1 = f

2 = c

3 = a

本主题中的第三种方法是排序

关联数组按照值降序排列。

```

<pre>
<?php
$friends = array("a" => "Tarun", "q" => "ashok", "b" => "charan", "l" => "sabid");
arsort($friends);
foreach ($friends as $key => $val) {
echo "$key = $valn";
}
?>
</pre>

```

**输出:**

l =萨比德 b =查伦 q =阿肖克 a =塔伦

让我们试着理解 krsort 是如何工作的，

## **krsort():PHP 中的数组排序**

关联数组根据键按降序排序。

```

<pre>
<?php
$var_array= array("1"=>"Ashok", "2"=>"Tarun", "3"=>"charan","4"=>"sabid","5"=>"adarsh","6"=>"chintan","7"=>"vaibhav");
krsort($var_array);
print_r($var_array);
?>
</pre>

```

**输出:**

排列

(【7】=>瓦伊巴夫【6】=>钦坦【5】=>阿达什【4】=>萨比德【3】=>查兰【2】=>塔伦【1】=>阿肖克)

让我们进入本文的下一个主题，

## **asort():PHP 中的数组排序**

关联数组根据值按升序排序。

```

<pre>
<?php
$var_array= array("1"=>"Ashok", "2"=>"Tarun", "3"=>"charan","4"=>"sabid","5"=>"adarsh","6"=>"chintan","7"=>"vaibhav");
asort($var_array);
print_r($var_array);
?>
</pre>

```

**输出:**

排列

(【1】=>阿肖克【2】=>塔伦【5】=>阿达什【3】=>查兰【6】=>钦坦【4】=>萨比德【7】=>瓦伊巴夫)

是时候进入本文的下一个主题了。

## **ksort()**

关联数组根据键按升序排序

```

<pre>
<?php
$var_array= array("7"=>"vaibhav","6"=>"chintan","1"=>"Ashok","5"=>"adarsh", "2"=>"Tarun", "3"=>"charan","4"=>"sabid");
ksort($var_array);
print_r($var_array);
?>
</pre>

```

**输出:**

排列

(【1】=>阿肖克【2】=>塔伦【3】=>查兰【4】=>萨比德【5】=>阿达什【6】=>钦坦【7】=>瓦伊巴夫)

让我们看看 natsort 的作品，

## **【NAT Sort():PHP 中的数组排序**

使用“自然顺序”算法对数组进行排序。它的排序方式是以人类维护键或值关联的方式对字母数字字符串进行排序。

```

<pre>
<?php
$var_files=array("file1.php","file2.php", "file3.php", "file0.php");
natsort($var_files);
print_r($var_files);
?>
</pre>

```

**输出:**

排列

([3]=>file0.php[0]=>file1.php[1]=>file2.php[2]=>file3.php)

让我们继续前进，

## **natcasesort()**

使用不区分大小写的“自然顺序”算法对数组排序。

```

<pre>
<?php
$var_files = array("file12.php", "File22.txt","file2.php", "file3.php", "File1.php");
natcasesort($var_files);
print_r($var_files);
?>
</pre>

```

**输出:**

排列

([4]=>File1.php[2]=>file2.php[3]=>file3.php[0]=>file12.php[1]=>file 22 . txt)

接下来我们要看一看 uasort

## **uasort():PHP 中的数组排序**

使用用户定义的比较函数对数组进行排序并维护索引关联。

```

<pre>
<?php
function fun($a, $b)
{
if ($a== $b) return 0;
return ($a > $b) ? -1 : 1;
}
$array = array('a' => -1, 'b' => 6, 'c' => 8, 'd' => -9, 'e' => 1, 'f' => 5, 'g' => 3);
uasort($array, 'fun');
print_r($array);
?>
</pre>

```

**输出:**

排列

（

= > 8[b]=>6[f]=>5[g]=>3[e]=>1[a]=>-1[d]=>-9

这给我们带来了 PHP 文章中数组排序的最后一点

## **uksort():**

使用用户定义的比较函数按关键字对数组进行排序

```

<pre>
<?php
function fun($a, $b)
{
if ($a== $b) return 0;
return ($a > $b) ? -1 : 1;
}
$array = array('a' => -1, 'b' => 6, 'c' => 8, 'd' => -9, 'e' => 1, 'f' => 5, 'g' => 3);
uksort($array, 'fun');
print_r($array);
?>
</pre>

```

**输出:**

排列

([g]=>3[f]=>5[e]=>1[d]=>-9

= > 8[b]=>6[a]=>-1

**usort():PHP 中的数组排序**

使用用户定义的比较函数按值对数组进行排序。

```

<pre>
<?php
function fun($a, $b)
{
if ($a== $b) return 0;
return ($a > $b) ? -1 : 1;
}
$array = array('a' => -1, 'b' => 6, 'c' => 8, 'd' => -9, 'e' => 1, 'f' => 5, 'g' => 3);
usort($array, 'fun');
print_r($array);
?>
</pre>

```

**输出:**

排列

([0]=>8[1]=>6[2]=>5[3]=>3[4]=>1[5]=>-1[6]=>-9)

至此，我们结束了这篇文章，我希望你已经了解了 PHP 中使用的所有数组排序函数。如果你觉得这篇文章相关，请查看 Edureka 的 [**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。

*有问题吗？请在这篇文章的评论部分提到它，我会回复你。*