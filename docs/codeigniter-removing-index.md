# 如何在 CodeIgniter 中从 URL 中删除 index.php？

> 原文：<https://www.edureka.co/blog/codeigniter-removing-index/>

在 CodeIgniter 项目中，默认情况下，index.php 文件将包含在 URL 中，但为了使它对搜索引擎和用户友好，我们需要删除它。在本文中，我们将学习如何在 Codeigniter 中删除 index.php。

本文将涉及以下几点:

*   [什么是 CodeIgniter？](#codeigniter)

*   [为什么除掉 index.php？](#whyremoveindex)

*   [如何除去 index.php？](#howtoremoveindex)

我们开始吧。

## **什么是 CodeIgniter？**

CodeIgniter 是一个 [PHP 驱动的框架](https://www.edureka.co/blog/php-frameworks/)，用于快速开发应用程序。在构建 web 应用程序时，我们花费大量时间反复编写相同的代码。框架为我们提供了一个起点，并最小化了构建网站所需的代码量。CodeIgniter 是一个免费、开源、易用、[面向对象的 PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) web 应用框架。CodeIgniter 是基于 MVC 的，它有连接数据库和执行各种操作的库，如发送电子邮件，上传文件等。

对于使用 Codeigniter 来说，最好有 一些 PHP 语法的基础知识，以及如何与数据库和 HTML 交互。

## **为什么除掉 index.php？**

去掉 index.php 让网址看起来更干净专业。Codeigniter 框架通过一个文件 index.php 服务于所有视图。没有这个文件，任何模型/视图/控制器都不能工作。我们需要从正确的配置网址删除 index.php，否则它会显示 404 页。

## **如何去除 index.php？**

**1。创建一个. htaccess 文件**

首先，我们需要在项目的根目录或 CodeIgniter 目录下创建一个. htaccess 文件。创建一个. htaccess 文件将允许我们在不访问服务器配置文件的情况下修改我们的重写规则。因为这个原因，。htaccess 对我们的 web 应用程序的安全性至关重要，因此可以确保文件是隐藏的。htaccess 是超文本访问的缩写，它是一个控制目录的配置文件。htaccess”。

创建后。htaccess 文件，将以下代码添加到该文件中。

```
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ index.php/$1 [L]

```

**2。移除 index.php 文件**

在你的文本编辑器中打开 config.php 文件，并从这里删除 index.php。

变化:

```
$config['index_page'] = "index.php";

```

到:

```
$config['index_page'] = '';
```

但在少数情况下，url_protocol 的默认设置可能无法正常工作。为了解决这个问题，我们需要打开 config.php 和

变化:

```
$config['uri_protocol'] = "AUTO";
```

至:

```
$config['uri_protocol'] = "REQUEST_URI";

```

大多数时候它已经被设置为 REQUEST_URI，在那种情况下，我们不需要改变它。

**3。启用 apache 模式重写**

现在，我们需要借助以下命令激活 mod_rewrite。

```
$ sudo a2enmod rewrite

```

**4。重启 Apache**

现在我们需要重启 Apache，为此我们编写以下命令。

```
$ sudo service apache2 restart
```

这将激活模块或提醒我们模块已经生效。

至此，我们已经到了文章的结尾。我希望你们喜欢它并理解 PHP 的概念。因此，随着本教程的结束，您不再是脚本语言的新手。

*如果您发现这个 PHP 教程博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在“如何在 Codeigniter 中删除 index.php”的评论部分提到它，我会回复您。*