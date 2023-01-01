# 如何在 PHP 中更改忘记的密码

> 原文：<https://www.edureka.co/blog/password-in-php>

登录系统是忘记密码恢复是强制性的。忘记的帐户密码由用户通过使用登录系统来更新。通过“忘记密码”链接，可以轻松重置重音密码。在本文中，我们将按照以下顺序了解关于 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中的密码:

*   [忘记密码](#forgot)
*   [重置密码的方法](#reset)
*   [重设密码](#resetting)

## **忘记密码**

在 PHP 登录系统中实现忘记密码邮件功能的忘记密码恢复过程和创建脚本。

![password-in-php](img/ad4478498d9c9ec1958dab7fffcb9205.png)

测试的文件可用于恢复忘记的密码。在 PHP 中提供密码时，需要考虑以下几点:

*   ***style . CSS:***忘记了，休息形式和造型登录

*   ***休息密码. php:*** 显示休息密码表单

*   ***User account . PHP:***处理忘记密码、重置密码、邮件发送。

*   忘记了密码。php:显示忘记密码表单

*   ***user . PHP:***处理数据库相关工作

*   ***index . PHP:***显示忘记密码行的登录表单

## **在 PHP 中重置密码的方法**

用户可以使用下面列出的 3 种方法重置密码:

*   ***发送密码:*** 由于数据库的数据库是明文密码(不推荐这些类型)

*   ***生成一个随机字符串作为密码*** 。用户已经以电子邮件的形式收到了它。数据库将使用哈希密码进行密码更新。

*   ***使用密码重置令牌:*** 随机生成哈希字符串。数据库存储在散列字符串中，但它们可能不存储在密码列中。用户会收到电子邮件形式的链接。将要求用户输入密码。在此之前，可以使用旧密码登录。

这两个脚本允许修复忘记的 PHP 密码脚本。 允许用户输入他们的电子邮件地址来保存他们的新密码，他们可能需要访问通过电子邮件发送的链接

**举例:**

写忘记密码的 php。在文本编辑器或 IDE 中创建一个新文档，命名为忘记密码 php。

代码是:

```
&amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;lt;?php #script 18.10-
forgot password.php
require(“include config.inc.php”);
$page_title =”forgot your password”;
include(“include/header.html”);
Check whether the form is submitted, it has also include database connection and create
The flag variable:
if ($-server (“request method”);=”post”)(
require (MYSQL);
$u.d=false;
```

## **在 PHP 中重置密码**

在一个网站中，人们忘记密码是不可避免的，这是很常见的，因此有必要为这种情况和场合制定一个应急计划。当这个额外的有足够的困难来管理网站

这将是一个用于重置密码的脚本。存储在数据库中的密码是使用 PHP 密码 hash()函数加密的，没有办法和未加密版本相抗衡

另一种方法是创建一个新密码，并将现有密码更改为该值。新密码将会通过电子邮件发送到用户注册的地址，而不仅仅是显示在浏览器中。

就这样，我们到了这篇文章的结尾。我希望你已经让 ann 了解了重设密码的各种方法。

*查看 Edureka 提供的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

有问题要问我们吗？请在评论区提到它，我会回复你。