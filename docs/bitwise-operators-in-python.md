# 关于 Python 中的按位运算符，您需要知道的一切

> 原文：<https://www.edureka.co/blog/bitwise-operators-in-python/>

[Python](https://www.edureka.co/blog/python-tutorial/) 是当今世界最流行的编程语言之一。Python 可以实现很多功能，这要归功于它强大的通用性和它带来的众多特性。在这篇文章中，我们将探索 Python 中的按位操作符以及下面的指针，

*   [Python 中的按位运算符是什么？](#WhatareBitwiseOperatorsinPython?)
*   [Python 中的按位运算符](#BitwiseOperatorsinPython)
*   [按位运算符示例](#ExampleofBitwiseOperators)

那么让我们开始吧，

按位运算符是 Python 编程的一个重要方面，在本文中，我们将讨论各种类型的按位运算符、它们的用途以及如何在日常编码中使用它们。我们开始吧！

继续这篇关于 Python 中的按位运算符的文章，

## **Python 中的按位运算符是什么？**

Python 中的按位运算符是用于执行位运算的函数和或方法。简单来说，它是将整数和字符串转换为 0 和 1 的过程。通过使用这些操作符，您正在敦促 Python 要么将它们从左向右移位，要么将它们转换成 0 和 1 的序列。比如 0100，1100，1000，1001。

为了更好地理解这一点，请看下面的例子。

x = 6，y = 8

转换时，其二进制形式的值将为 x = 0110，y = 1000。

继续这篇关于 Python 中的位操作符的文章，

## **Python 中的按位运算符**

下面提到的是 Python 中一些最重要的位运算符及其用法。

1.  &:通称按位与。例，X & Y = 0000。
2.  ^:被称为按位异或。例如，X ^ Y = 1110。
3.  |:通称按位或。例如，X | Y = 1110。
4.  ~:通称按位补码。例如，~X = 00001001。
5.  <<:通称左移。例，X << 1 = 00001100。这里，这些位将向左移动 1 步。
6.  >> :通称右移。例如，Y >> 1 = 00000100。

Python 中的按位运算符执行真值表中列出的任务。为了更好地理解这一点，请看下面不同操作符的真值表。

**x**yx&yx | yx ^ y

00000

0T2 1T4 011

1T2 0T4 011

1T2 1T4 110

继续这篇关于 Python 中的位操作符的文章，

## **按位运算符示例**

现在，您已经理解了位运算符功能背后的基本概念，让我们举一个例子来进一步阐明这个概念。 在下面分享的例子中，我们考虑了两个变量 a 和 b，并将值 9 和 65 插入其中。

```
a = 9
b = 65
print("Bitwise AND Operator On 9 and 65 is = ", a & b)
print("Bitwise OR Operator On 9 and 65 is = ", a | b)
print("Bitwise EXCLUSIVE OR Operator On 9 and 65 is = ", a ^ b)
print("Bitwise NOT Operator On 9 is = ", ~a)
print("Bitwise LEFT SHIFT Operator On 9 is = ", a << 1) print("Bitwise RIGHT SHIFT Operator On 65 is = ", b >> 1)
```

在上面的例子中，我们声明了两个变量 a 和 b，并与它们共享值 9 和 65。转换成二进制时，9 = 00001001，65 = 01000001。

**计算**

对于上面的程序，让我们手动计算结果可能是什么。

1.  按位 AND 运算= a & b .分析:00001001&01000001 = 0000001 = 1
2.  按位或运算= a | b .分析:00001001 | 01000001 = 01001001 = 73
3.  python 中的按位异或运算= a ^ b .解析:00001001 ^ 01000001 = 01001000 = 72
4.  Python 中的右移操作= b>1。分析:01000001>T5 1 = 00100000 = 32

010000001>1 = 00100000 = 32

这就把我们带到了本文的结尾。

*要深入了解 Python 及其各种应用，您可以 [**在此**](https://www.edureka.co/python/) 注册参加在线直播培训，全天候支持，终身访问。*

*有问题吗？在“Python 文章”的评论部分提到它们，我们会回复您。*