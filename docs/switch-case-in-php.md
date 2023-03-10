# 关于 PHP 中的开关大小写，你需要知道的就是

> 原文：<https://www.edureka.co/blog/switch-case-in-php/>

如果我们谈论任何编程语言，Switch case 都是不可缺少的。以下指针将在 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 文章中的这个开关案例中涉及，

*   [什么是开关盒？](#what)
*   [开关箱代码](#SwitchcaseinPHP)

## **什么是开关盒？**

在这篇文章中，我们将讨论 PHP 中的 switch case，switch case 背后的基本思想是，我们将根据我们可能得到的某种答案在浏览器中做一些不同的事情。它是一系列 if 语句的替代，后者几乎做同样的事情。

通过 switch-case 语句对一系列值进行测试，直到找到匹配项，然后执行与匹配项对应的代码块。

继续这篇关于 php 中 switch case 的文章

## **代码:PHP 中的 Switch case**

在我们的例子中，答案是赋给某个变量的值。所以我们写出 switch 的方式是通过 switch() { } 虽然它看起来像 if 语句，但并不完全相同，因为在 if 语句中，你实际上有不同的条件，在 switch 中，你把所有不同的可能答案写在花括号里。所以让我们继续写一个不同的例子

```
<?php
$x=1;
switch($x)
{
case 1:
echo "This answer is case 1";
break;
}

```

![Example- switch case in php- Edureka](img/df3e8056408ed44c154f48c283f73a83.png)

我们也可以将字符串赋给变量。

```
<?php
$x="number";
switch($x)
{
case 1:
echo "This answer is case 1";
break;
case "number";
echo "This answer is case number";
break;
}

```

![Example- switch case in php- Edureka](img/83a5ac51d0f286d96a1baf28c4100080.png)

基本上，我们使用 break 来防止代码自动进入下一个案例。如果没有找到匹配，我们使用默认语句。

```
<?php 
$company = "amazon"; 
switch($company) 
{ 
case "simplilearn": echo "Company choosed: simplilearn"; 
break; 
case "edureka": echo "Company choosed: edureka";
break; 
case "intellipaat": echo "company choosed: intellipaat"; 
break; 
default: echo "Company not found"; 
break;
 }
 ?>
```

![Example- switch case in php- Edureka](img/2ace2719ad1124a1cd16fcecc8a0de9b.png)

到此，我们结束这篇文章。我希望你已经了解了 PHP 中的 switch case，以及 switch case 背后的基本思想，即我们在浏览器中根据某种场景做了一些不同的事情。

*查看 Edureka 提供的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在“ **PHP 教程**的评论区提及，我会回复你。*