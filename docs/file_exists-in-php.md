# 如何在 PHP 中实现 file_exists 函数？

> 原文：<https://www.edureka.co/blog/file_exists-in-php/>

文件是一种存储数据的资源，PHP 有丰富的内置函数集合，可以简化您的文件工作。 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中的 **file_exists()** 函数是一个内置函数，用于检查文件或目录是否存在。在本文中，我们将看到如何按照以下顺序在 PHP 中实现 file_exists:

*   [PHP 中的 file _ exists()](#file)
*   [clearstatcache()](#cache)

## **PHP 中的 file_exists()**

这是一个内置函数，可以用来检查文件是否存在。 当我们想在处理之前知道一个文件是否存在时，它就派上了用场。 你也可以在创建新文件时使用这个功能，并且你想确保服务器上还没有[文件](https://www.edureka.co/blog/write-a-file-in-php/)。

**![PHP- file_exists in php - edureka](img/953089c36f0fefceac064aecf52d5a22.png)**

**语法:**

```
file_exists(path)
```

它只接受一个参数。即 path，它指定了我们想要检查的文件的目录或路径。它将在成功执行时返回 true，在执行失败时返回 false。

如果 path 指定指向不存在的文件，file_exists()返回 false。对于大于 2GB 的文件，一些文件系统函数可能会产生意外的结果，因为 PHP integer 类型是有符号的，并且许多平台使用 32 位整数。

## **clearstatcache()**

通常情况下，file_exists()的结果是缓存的。为了清除缓存，我们使用 clearstatcache()，如果要在脚本中多次检查一个文件，您需要避免缓存以获得正确的结果。为了实现这一点，我们清除 statcache()函数。

**语法:**

```
clearstatcache(clear_realpath_cache, filename)
```

这两个参数都是可选的，其中Clear _ realpath _ cache表示是否清除 real path 缓存。默认为 FALSE，表示不清除实路径缓存， 文件名 指定[文件](https://www.edureka.co/blog/file-handling-in-php/)的名称，只清除该文件的实路径和缓存。

下面的例子演示了在 PHP: 中**文件存在**的工作方式

```
<?php
if (file_exists('create_file.txt'))
{    
    echo 'file found!';
} 
else
{     
    echo 'create_file.txt does not exist';
} 
?>

```

**输出:**

![](img/db2b2a7b2bbf9c6ea847300b25059af6.png)

由于文件不存在，这意味着指定的路径指向不存在的文件，所以它返回 false 并执行 else 部分。

到此，我们结束这篇文章。我希望你已经了解了 PHP 中的内置函数 file_exists()和 clearstatcache()。

*如果您发现这个 PHP 博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在“**文件 _ 存在于 PHP** 中”的评论部分提及，我会回复你。*