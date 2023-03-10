# PHP 错误处理:您需要知道的一切

> 原文：<https://www.edureka.co/blog/php-error-handling/>

错误处理是发现程序引发的错误并采取措施的过程。这篇文章将帮助你详细探索 PHP 的[错误处理的概念。本文将涉及以下内容，](https://www.edureka.co/blog/php-tutorial-for-beginners/)

*   [错误处理](#ErrorHandling)
*   [使用 die()功能](#Usingdie()function)
*   [样本程序](#SampleProgram)

让我们从 PHP 错误处理文章开始，

## **错误处理**

在 PHP 中处理错误非常容易。 在创建脚本和 web 应用时，错误处理是非常重要的一部分。如果您的代码缺少错误检查代码，您的程序可能看起来非常不专业，并且您可能面临安全风险。

我们将看到不同的错误处理方法:

*简单的" die()"语句

*自定义错误和错误触发器

*错误报告

让我们看看 PHP 错误处理是如何与 die 函数一起工作的，

**使用 die()功能**

编写 PHP 程序时，你应该在开始之前检查所有可能的错误，并采取所需的适当措施。 没有/tmp/test.xt 文件的例子

```
<?php
If(!file_exists (&ldquo;/tmp/test.text&rdquo;))
{
die(&ldquo;File does not founds&rdquo;);
}
else
{
$file = fopen(&ldquo;/tmt/test.txt&rdquo;,&rdquo;r&rdquo;);
Print"opening file successfully&rdquo;;
}
}
?>
```

创建自定义错误处理程序

创建自定义错误处理程序非常简单。我们可以简单地创建一个特殊的函数，只要 PHP 代码中出现错误，就可以调用这个函数。

该函数能够处理最少两个参数，它们可能是错误级别或错误信息，但最多可以接受五个可选参数，它们是文件、行号和错误上下文

**语法**

```
error_function()
Set Error Handler
```

PHP 的默认错误处理程序是软件中内置的错误处理程序。我们将使这个函数在脚本运行期间高于默认的错误处理程序。

可以更改仅适用于某些错误的错误处理程序，这样脚本就可以在代码中以不同的方式处理不同的错误。然而，在本例中，我们将对其中的所有错误使用我们的自定义错误处理程序。

set _ error _ handler(“”)；

让我们来看一个示例程序，

## **样本程序**

通过尝试输出不存在的变量来测试错误处理程序:

```
<?php
//error handler function
function custom error($errno, $errstr)
{
echo "<b>Error:</b> [$errno] $errstr";
}
set_error_handler("customError");
echo($test);
?>
```

**输出**

**错误:**【8】未定义变量:测试

这就把我们带到了本文的结尾。

*如果你发现这个博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在文章的评论部分提到它，我会回复你。*