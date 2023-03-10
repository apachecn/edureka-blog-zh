# 如何最好地利用 PHP 中的 Unlink 函数？

> 原文：<https://www.edureka.co/blog/unlink-function-in-php/>

本文将向您介绍一个简单而重要的概念，即 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) Unlink 函数，并提供详细的实践演示。本文将涉及以下几点:

## **PHP Unlink 函数**

在 PHP 中，有两个函数在执行撤销操作时是相同的，但是它们在执行撤销功能时应用的数据类型不同。它们是 unlink()和 unset()，其中 unlink 充当将完全删除文件的 drop 操作，unset 删除文件内容以清空文件。在本文中，我们将讨论 php 中的 unlink()。

**unlink()**

这是 PHP 的内置函数，用来删除文件。它类似于 UNIX 的 unlink()函数。文件名作为需要删除的参数发送，函数在成功执行时返回 True，而在不成功执行时返回 false。

*   **语法:** unlink(文件名，上下文)
*   **文件名:** 指定要删除的文件的名称。
*   **context:** 可选参数，指定文件句柄的上下文，可用于修改流的性质。

Web 服务器用户必须对目录具有写权限，才能使用 unlink()功能。它 在失败时产生一个 E_WARNING 级别错误。它返回布尔值 False，但很多时候它会返回一个非布尔值，该值的计算结果为 False。

继续这篇关于 PHP 中的 Unlink 函数的文章

## **样本程序**

现在，我们来看一个使用 like()函数删除名为 file.txt 的文件的示例演示

```
<?php
$filepoint = "file.txt";
if (!unlink($filepoint))
{
echo ("$filepoint cannot be deleted due to an error");
}
else
{
echo ("$filepoint has been deleted");
}
?>&nbsp;
```

让我们来看一个例子，如果我们想用掩码删除文件，

```
<?php
$mask = "*.txt";//extension
array_map( "unlink", glob( $mask ) );
?>
```

Glob()返回与指定模式匹配的目录或文件名的数组。array_map()向用户自定义函数发送数组中的每个值，并返回一个包含用户自定义函数给定的新值的数组。

至此，我们结束了这篇关于 PHP Unlink 函数的文章。我希望你已经了解了 unlink() & unset()之间的基本区别，特别是 PHP 中的内置函数 unlink()和一些例子。

*如果您发现这个 PHP 博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在这篇文章的评论部分提到它，我会回复你。*