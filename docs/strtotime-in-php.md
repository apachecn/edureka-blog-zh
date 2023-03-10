# PHP 中的 strtotime:您需要知道的一切

> 原文：<https://www.edureka.co/blog/strtotime-in-php/>

PHP 有一个日期函数来处理日期时间，在 web 应用程序中实现。我们可以将人类可读的日期转换成 Unix 时间戳。这个函数是 strtotime。在这篇文章中，我们将探索在 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中的 strtotime。本文将涉及以下几点:

*   [什么是 strtotime()？](#Whatisstrtotime()?)
*   [什么是 UNIX 时间戳？](#WhatisUNIXtimestamp?)
*   [PHP 中 strtotime()的使用](#Useofstrtotime()inPHP)

让我们从这篇 PHP 文章开始，

## **PHP 中的 strtotime**

## **什么是 strtotime()？**

这是一个内置函数，在 PHP 中用来将英文文本日期时间转换成 UNIX 时间戳。当我们在 PHP 中查看日期时，有一个系统叫做 UNIX 时间戳。如果我们想重复功能时间，我们将得到一个与日期完全无关的奇怪数字。

```
<?php
echo time()
?>

```

**输出:** 1562486153

让我们从 PHP 文章的下一部分开始，

## **什么是 UNIX 时间戳？**

上面的输出中是 UNIX 时间戳，它只不过是一个线性数字，从 1970 年 1 月 1 日开始计算秒数，但它是一个有用的数字，因为我们可以将它格式化为不超过秒。我们可以使用 PHP 将字符串处理成我们想要的样子。如果我使用 date 函数，date 函数需要两个参数，第一个是日期的格式，第二个是时间源。

```
<?php
echo date('m-d-y',time());
?>

```

**输出:** 07-07-19

这就是本文的最后一点

## **PHP 中 strtotime()的使用**

当我们要回显 strtotime()时，它将显示该消息的 UNIX 时间戳。假设年份以两位数格式指定，0-69 之间的值映射到 2000-2069，70-100 之间的值映射到 1970-2000。

```
<?php
echo strtotime('July 7th 2019');
?>

```

**输出:** 1562472000

```
<?php
echo strtotime('July 7th 2019 2:10 pm');
?>

```

**输出:** 1562523000

本质上，它只是将一串文本转换成一个实际的时间戳。这根据 UTC 显示年、月、日，但不根据我的时区

```
<?php
echo date('Y-m-D',time());
?>

```

**输出:**2019-07-孙

我们还可以使用 date_default_timezone_set()将时区设置为最近的服务器。为了获得准确的月份、日期、年份和时间，我们使用 date('M-dS-Y at h:i A '，time())

```
<?php
date_default_timezone_set("Asia/Calcutta");
echo date('M-dS-Y at h:i A',time());
?>

```

**输出:**

2019 年 7 月 7 日下午 03:22

关于 PHP 中的 srttotime 的这篇文章到此结束，我希望你已经了解了 **s** trtotime()，UNIX 时间戳，以及 strtotime()在 PHP 中的使用示例。

如果你觉得这篇文章相关，请查看 Edureka 的[](https://www.edureka.co/php-mysql-self-paced)PHP 认证培训，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。

*有问题吗？请在文章的评论部分提到它，我会回复你。*