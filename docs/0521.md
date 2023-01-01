# Python 中的命令行参数

> 原文：<https://www.edureka.co/blog/command-line-arguments-in-python>

[//www.youtube.com/embed/ffWcSDzI-o8](//www.youtube.com/embed/ffWcSDzI-o8)﻿

## **Python 中的命令行参数是什么？**

Python 支持创建可以在命令行上运行的程序，包括命令行参数。它提供了一个 getopt 模块，使用该模块可以解析命令行选项和参数。

## **访问命令行参数**

Python sys 模块通过 sys.argv 提供对任何命令行参数的访问。它解决了两个目的:

*   sys.argv 是命令行参数的列表
*   len(sys.argv)是命令行中的命令行参数数
*   sys.argv[0]是程序，即脚本名

## **执行 Python**

您可以通过以下方式执行 Python:

$python Commands.py inp1，inp2 inp3

## 如何用 Python 传递一个参数？

在 Python 中，如果从 shell 中调用脚本，参数将放在脚本名称之后。在这里，参数由空格分隔，在脚本中，这些参数可以通过列表变量 sys 访问。argv。

## **例如**

**内部命令. py:**

导入系统

print '参数个数:'，len (sys.argv)，'参数。

print '参数列表:'，str(sys.argv)

它将产生以下输出:

参数数量:4 个参数。

参数列表:['sample.py '，' inp1 '，' inp2 '，' inp3']

***注意:这里需要记住的一点是，缩进和间距极其重要，否则可能会给出错误或不正确的参数个数。***

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[Python 101:Hello World 程序](https://www.edureka.co/blog/python-101-hello-world-program/ "Python 101: Hello World Program")

[你为什么要去找 Python？](https://www.edureka.co/blog/why-python/ "Why should you go for Python?")

[Python 中的字符串介绍](https://www.edureka.co/blog/strings_in_python/ "Introduction to Strings in Python")

[开始学习 Python 进行大数据分析](https://www.edureka.co/data-science-python-certification-course "Python for Big Data Analytics")