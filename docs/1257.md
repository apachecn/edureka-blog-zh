# PHP 中的 split:str _ split()函数是什么

> 原文：<https://www.edureka.co/blog/php-str-split/>

一种 **脚本语言** 是一种在运行时解释脚本的语言。脚本的目的通常是增强应用程序的性能或执行日常任务。 [PHP](https://www.edureka.co/) 文章中的 **split 将按以下顺序为您提供关于 split 函数替代方法的详细知识:**

*   [在 PHP 中拆分](#splitphp)
*   [什么是 preg_split()？](#pregsplit)
*   [什么是 explode()？](#explode)
*   [什么是 str_split()？](#strsplit)

## **在 PHP 中拆分**

split 函数在 PHP 5.3.0 中不被认可，在 [PHP 7](https://www.php.net/downloads.php) 中被移除。此功能还有其他选择，它们是:

*   **preg_split()**
*   **爆炸()**
*   **str_split()。**

## **什么是 preg_split()？**

这是 PHP 中的一个内置函数，用于将给定的字符串转换成数组。字符串被分割成长度由用户使用该函数指定的更小的子字符串。比方说，指定了限制，然后子字符串通过数组返回，直到限制。今天就来看看这个[全栈开发者课程](https://www.edureka.co/masters-program/full-stack-developer-training)，了解更多关于 PHP 的知识。

**语法:**

数组 preg_split(模式、主题、限制、标志)

*   **模式:**为字符串类型，用于搜索模式，否则分隔元素。
*   **subject:** 是用来存储输入字符串的变量。
*   **极限:**表示极限。如果指定了限制，则返回的子字符串必须达到限制。如果限制为 0 或-1，则表示该标志使用“无限制”。
*   **flag:****PREG _ SPLIT _ NO _ EMPTY**——PREG _ SPLIT()**PREG _ SPLIT _ DELIM _ CAPTURE**——分隔符模式中带括号的表达式将被捕获并返回。**PREG _ SPLIT _ OFFSET _ CAPTURE**—对于每个出现的匹配，还将返回附加字符串偏移量。

如果你想用任意数量的逗号或空格字符分割短语:

```

<pre>
<?php $variable = preg_split("/[s,]+/", "ashok tarun, charan sabid"); print_r($variable); ?>
</pre>

```

**输出:**

```
Array
(
    [0] => ashok
    [1] => tarun
    [2] => charan
    [3] => sabid
)

```

这样，我们将一个字符串分割成**个组成字符**:

**输出:**

```
Array
(
    [0] => a
    [1] => s
    [2] => h
    [3] => o
    [4] => k
)
```

这样，我们将一个字符串分成**个匹配项**和它们的偏移量:

**输出:**

```
Array
(
    [0] => Array
        (
            [0] => ashok
            [1] => 0
        )

    [1] => Array
        (
            [0] => is
            [1] => 6
        )

    [2] => Array
        (
            [0] => a
            [1] => 9
        )

    [3] => Array
        (
            [0] => student
            [1] => 11
        )

)
```

**什么是 explode()？**

这是一个内置函数，它将一个字符串分解成一个数组。

**语法:**

分解(分隔符、字符串、限制)

*   **分隔符:**该字符决定要拆分的字符串。
*   **String:** 这个输入的字符串会拆分成一个数组。
*   **Limit:** 这是可选的，指定数组中元素的数量。

**举例:**

```
<pre>
<?php $var_str = 'sunday,monday,tuesday,wednesday'; print_r(explode(',',$var_str,0)); //zero limit print_r(explode(',',$var_str,2));// positive limit print_r(explode(',',$var_str,-1));// negative limit ?>
</pre>

```

**输出:**

```
Array
(
    [0] => sunday,monday,tuesday,wednesday
)
Array
(
    [0] => sunday
    [1] => monday,tuesday,wednesday
)
Array
(
    [0] => sunday
    [1] => monday
    [2] => tuesday
)

```

## **什么是 str_split()？**

该函数用于使用**长度参数**将字符串拆分成数组。

**语法:**

str_split(string，length())。

*   **String:** 指定要拆分的字符串。
*   **Length:** 它指定了每个单独数组元素的长度。默认值为 1。

**举例:**

```

<pre>
<?php print_r(str_split("ashok",4)); ?>
</pre>

```

**输出:**

```
Array
(
    [0] => asho
    [1] => k
)
```

本文到此结束，我希望你已经了解了所有三个 split 函数 preg_split()、explode()、str_split()和示例。

*如果你在 PHP 博客中发现了这种分裂，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在“**在 PHP** 中拆分”的评论部分提及，我会回复你。*