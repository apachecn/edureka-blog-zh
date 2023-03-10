# 如何在 Xampp 中运行一个 PHP 程序？

> 原文：<https://www.edureka.co/blog/how-to-run-a-php-program-in-xampp/>

PHP 是最流行的 web 后端编程语言。PHP 代码将作为 web 服务器模块或命令行界面运行。要运行 PHP for the，你需要安装一个像 Apache 这样的 web 服务器，还需要一个像 [MySQL](https://www.edureka.co/blog/mysql-tutorial/) 这样的数据库服务器。有各种运行 PHP 程序的网络服务器，如 WAMP XAMPP 的 T4。WAMP 服务器在 windows 中受支持，XAMP 在 Windows 和 Linux 中都受支持。在这篇文章中，你将学习如何在 Xampp 服务器上运行 PHP 程序。

本文涵盖以下主题:

*   [什么是 Xampp？](#whatisxampp)
*   [安装 Xampp](#installxampp)
*   [如何在 Xampp 中运行 PHP 程序？](#howtorunphpprogram)

让我们开始吧。

**什么是 Xampp，为什么使用它？**

Xampp 是 Windows、OS X 和 Linux 平台上最流行的 PHP 开发环境。

Xampp stands for **Cross platform(x), Apache(a), Maria db(m), PHP(p), Pearl(p)** which is a software distribution server which makes developer’s work eaiser for testing and deploying by creating a local web server.

## **如何安装 Xampp？**

安装包含 MySQL、PHP 和 Perl 的 Apache 发行版是完全免费和容易的。首先从[【https://www.apachefriends.org/download.html】](https://www.apachefriends.org/download.html)下载 XAMP。 在第一页，选择你要安装的组件。

![Xamp - how to run php program - Edureka](img/0bd82f91ee2b7c539f09146081532607.png)

选择安装目录，这样您选择的所有组件都将安装在该目录中。

![Xamp Installation - how to run php program - Edureka](img/51436e0fc979caa9282da7ef88200f55.png)

XAMP 还允许你轻松地安装基于 PHP 的应用程序。Bitnami 模块提供了在 XAMP 上安装 WordPress、Drupal 或 Joomla 等最简单的方法，安装后你会看到控制面板。

一旦您完成了 xampp 安装，让我们继续，看看如何在 Xampp 服务器中运行 PHP 文件。

## **如何在 Xampp 中一步步运行 PHP 程序？**

*   在记事本上写下这个程序，并另存为 file.php 或其他名字。

```
<?php echo " hello ashok" ?>
```

*   安装完成后，您可以使用 XAMPP 控制面板启动/停止所有服务器。

*   启动 Mysql 和 Apache 服务器。

![Xamp Control Panel - how to run php program - Edureka](img/77a1a57b782c0de9820cea581fd07bf3.png)

*   将 file.php 复制到 htdocs(C:/Program Files/XAMPP/htdocs)

*   您也可以在 htdocs 文件夹中创建任何文件夹，并将我们的代码保存在那里。

为了获得 localhost 的仪表板:在任意浏览器中搜索[http://localhost](http://localhost)。

![Xamp UI- how to run php program - Edureka](img/0a37f0478b7cf2ad64f52604a9f9abcf.png)

*   现在要运行你的代码，打开 localhost/file.php，然后它就会被执行。

![output - how to run php program - Edureka](img/c9335684b6d4b4fd98b0d5f2cea1b948.png)

至此，我们结束了这篇文章。我希望你已经了解了 XAMP，XAMP 的安装以及如何在 Xampp 中运行一个 PHP 程序。

*如果你发现这个教程博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在“**如何在 xampp** 中运行 php 程序”的评论部分提到它，我会回复你。*