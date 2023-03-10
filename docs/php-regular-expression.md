# 如何在 PHP 中构建正则表达式？

> 原文：<https://www.edureka.co/blog/php-regular-expression/>

为了通过使用单个函数简化字符串中模式的识别，从而节省大量编码时间。它们被用于各种各样的事情，比如创建一个定制的 [HTML](https://www.edureka.co/blog/what-is-html/) 模板，验证用户输入，比如电话号码、电子邮件地址等等，在搜索结果中高亮显示关键词。在 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 的这篇正则表达式文章中，你将按以下顺序学习不同的函数:

*   [**什么是正则表达式？**](#regularexpression)
*   **[PHP 中的正则表达式](#regexphp)**
*   [**什么是 preg_match？**](#whatispreg_match)
*   [**什么是 preg_split？**](#whatispreg_split)
*   [**什么是 preg_replace？**T3](#whatispreg_replace)

让我们开始吧。

## **什么是正则表达式？**

**正则表达式** 是构成搜索模式的字符序列。当您在文本中搜索数据时，您可以使用这种搜索模式来描述您要查找的内容。

![regular expression - php regex - edureka](img/e2639ef979f249f26202bba33382f7f6.png)

正则表达式可以是一个  **单字符** 或更复杂的模式。它可用于任何类型的文本搜索和文本替换操作。正则表达式模式由简单字符组成，如/abc/，或者由简单字符和特殊字符组合组成，如**/ab * c/**或  **/example(d+)。d*/。**

## **PHP 中的正则表达式**

PHP 有内置函数，允许我们使用常规函数。PHP 中一些常用的正则表达式函数有:

*   **怀孕匹配**
*   **怀孕 _ 分裂**
*   **怀孕 _ 更换**

现在让我们继续学习 PHP 中的正则表达式，并详细看看这三个函数。

**什么是 preg_match？**

该函数用于对字符串执行模式匹配，如果找到匹配则返回 true，否则返回 false。

**语法:**

```
preg_match(pattern,input,matches,flags,offset)

```

**模式:** 用于字符串搜索的模式。

**输入:** 是输入字符串

**匹配:** 如果提供了一些匹配，用于填充搜索结果。$matches[0]将包含与完整模式匹配的文本，$matches[1]将包含与第一个捕获的带括号子模式匹配的文本，依此类推。

**举例:**

```

<pre>
<?php $var= 'ashokiscoder'; preg_match('/(ashok)(is)(coder)/', $var, $matches, PREG_OFFSET_CAPTURE); print_r($matches); ?> 
</pre>

```

**输出:**

阵列(【0]=阵列>(【0]=阵列> = >是>)【3]=>阵列

现在你知道 preg_match 是如何工作的了，让我们继续学习 PHP 中的正则表达式，看看下一个函数。

## **什么是 preg_split？**

该函数用于对字符串执行模式匹配，然后将结果拆分为一个数字数组。

**语法:**

```

array preg_split(pattern,subject,limit, flag)

```

**模式:** 它是字符串类型，用于搜索模式，否则它分隔元素。

**subject:** 它是一个变量，用来存储输入的字符串。

**极限:** 表示极限。如果指定了限制，则返回的子字符串必须达到限制。如果 limit 为 0 或-1，则表示标志使用“无限制”。

**标志:** 标志可以是以下任何一种标志:

*   **PREG_SPLIT_NO_EMPTY**

*   **PREG_SPLIT_DELIM_CAPTURE**

*   **PREG _ SPLIT _ OFFSET _ CAPTURE**

如果你想用任意数量的逗号或空格字符分割短语:

```

<pre>
<?php $variable = preg_split("/[s,]+/", "ashok tarun, charan sabid"); print_r($variable); ?>
</pre>

```

**输出:**

数组(【0】=>阿肖克【1】=>塔伦【2】=>【3】=>萨比德 )

用这种方法，我们将一个字符串分割成组成字符。

```

<pre>
<?php $var_string = 'ashok'; $var_char = preg_split('//', $var_string, -1, PREG_SPLIT_NO_EMPTY); print_r($var_char); ?>
</pre>

```

**输出:**

数组(【0】=>a【1】=>s【2】=>【3】=>o【4】=>k)

这样，我们把一个字符串分成匹配项和它们的偏移量

```

<pre>
<?php $var_string = 'ashok is a student'; $var_char = preg_split('/ /', $var_string, -1, PREG_SPLIT_OFFSET_CAPTURE); print_r($var_char); ?>
</pre>

```

**输出:**

阵列(【0]=阵列>(【0]=阵列> =>a【1]=>)【3]=>阵列

现在让我们继续，看看 PHP 中正则表达式的最后一个函数。

## **什么是 preg_replace？**

该函数用于对字符串执行模式匹配，然后用指定的文本替换匹配。

**语法:**

```

preg_replace( pattern, replacement, subject, limit, count )

```

**模式:** 包含用于搜索内容的字符串，可以是字符串或字符串数组

**替换:** 指定要替换的字符串或字符串数组。

**Subject:** 是要查找或替换的字符串或字符串数组。

**极限:** 它规定了每种模式的最大可能替换

**count:** 可选参数，可以填入完成的替换次数

为了通过数字文字使用反向引用:

```
<?php $string = 'July 07, 2019'; $pattern = '/(w+) (d+), (d+)/i'; $replacement = '${1}1,$3'; echo preg_replace($pattern, $replacement, $string); ?>

```

**输出:**

2019 年 7 月 1 日

为了与 preg_replace()一起使用索引数组

```

<pre>
<?php $var_string = 'ashok'; $var_char = preg_split('//', $var_string, -1, PREG_SPLIT_NO_EMPTY); print_r($var_char); ?>
</pre>

```

**输出:**

鱼在海里游泳。

本文到此结束，我希望你已经了解了 PHP 中常用的正则表达式函数，它们是 preg_match，preg_split，preg_replace。

至此，我们已经到了 php 正则表达式的末尾。我希望你们喜欢这篇文章，并且理解 PHP 中的正则表达式。因此，随着本 PHP 教程的结束，您不再是脚本语言的新手。

*如果你在 PHP 博客中发现了这个相关的正则表达式，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在“PHP 中的正则表达式”的评论部分提到它，我会回复你。*