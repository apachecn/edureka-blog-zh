# 如何在 PHP 中实现 Intval？

> 原文：<https://www.edureka.co/blog/intval-in-php/>

PHP 拥有各种各样的函数，让程序员的生活变得简单，在本文中，我们将探索 PHP 中的 Intval 函数。本文将涉及以下几点:

*   [PHP 中的 Intval](#IntvalInPHP)
*   [Intval](#ExampleForIntval)的示例

那么让我们开始吧

**Intval** **在 PHP 中**

这是一个内置函数，用来获取变量的整数值。使用指定的转换基数，它返回所提供变量的整数值。默认基数是 10。不应该在对象上使用它，否则它将返回 E_NOTICE 级别错误并返回 1。

**语法** 带引号(var_name，base)

**Var_name:** 它指定将提供的标量值转换成整数

**基数:** 它指定了转换为其对应整数的基数。

关于基地的一些重要要点:

*   如果基数为 0，则使用的基数由 var: 的格式决定
*   如果字符串包含前缀“0x”(或“0X”)，则基数为 16(十六进制)
*   基数取为 8(八进制)，如果字符串以“0”开头
*   其他基数取 10(小数)。

成功时返回 var 的整数值，否则失败时返回 0。非空数组返回 1，空数组返回 0。 一般来说，最大值取决于系统。32 位系统的最大有符号整数范围是-2147483648 到 2147483647，64 位系统的最大有符号整数值是 9223372036854775807。

最有可能的字符串将返回 0，即使这取决于字符串最左边的字符。整数转换的通用规则适用于此。

现在让我们来看看一些程序，

**Intval**的示例

```
<?php $var = "81"; echo intval($var)." ".intval($var, 9); ?>

```

**输出:**

![Output - Intval In PHP - Edureka](img/f36142ab8e02f9b9d8378f428c267cfd.png)

```
<?php $var = '9.236886'; $var1 = intval($var); echo $var1; ?>

```

**输出:**

![Output - Intval In PHP - Edureka](img/d4cc2e9ea0a59327d5748731ba431216.png)

```
<?php $var = 0x1A; $var1 = intval($var); echo $var1; ?>
```

**输出:**

![Output - Intval In PHP - Edureka](img/40a1bdcd1beca0d79eed1eef2b532425.png)

至此，我们结束了这篇文章，我希望你理解了 php 中的内置函数 intval。如果你觉得这篇博客相关，可以看看 Edureka 的 [**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。

*有问题吗？请在 PHP 的“ **Intval** **的评论区提出来，我会回复你的。***