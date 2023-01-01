# 通过示例了解 Python 中的范围

> 原文：<https://www.edureka.co/blog/range-in-python/>

Python 编程语言自带内置的[数据类型](https://www.edureka.co/blog/collections-in-python/)像[列表](https://www.edureka.co/blog/lists-in-python/)、[字典](https://www.edureka.co/blog/dictionary-in-python/)、[集合](https://www.edureka.co/blog/sets-in-python/)、[元组](https://www.edureka.co/blog/videos/python-list-tuple-string-set-dictonary/)等。python[中的 range](https://www.edureka.co/data-science-python-certification-course)是另一种内置的 python 数据类型，主要用于 python 中的循环。它返回函数参数中指定的一系列数字。在本文中，我们将通过各种示例详细了解 python 中的范围。以下是本博客涵盖的主题:

*   [Python 中的 Range 是什么？](#range)
*   [范围参数](#params)
*   [带 For 循环的范围](#forloop)
*   [以正负步长递增](#steps)
*   [范围内的浮点数](#float)
*   [Python 中的反向范围](#reverse)
*   [范围 vs 范围](#xrange)
*   [连接两个距离函数](#concat)
*   [使用索引号访问范围](#index)
*   [将范围转换为列表](#list)
*   [点记](#pointstorem)

## **Python 中的范围是什么？**

它是 Python 中内置的[函数](https://www.edureka.co/blog/python-functions)，返回一个数字序列，从 0 开始递增到 1，直到达到指定的数字。range 函数最常见的用途是迭代序列类型。它最常用于 [for 和 while 循环](https://www.edureka.co/blog/loops-in-python/)。

## **范围参数**

以下是我们在 python 中使用的范围函数参数:

*   start–这是起始参数，它指定范围函数中数字序列的开始。
*   Stop–这是序列的终点，数字将在到达 stop 参数时停止。
*   步长–序列中每个数字之前的步长或增量数由步长参数决定。

```
range(start, stop, step)

```

## **带 For 循环的范围**

下面是一个如何在 for 循环中使用 range 函数的例子。这个程序将打印从 2 到 20 的偶数。

```
for i in range(2,20,2):
     print(i)

```

```
Output: 2
        4
        6
        8
        10
        12
        14
        16
        18
```

## **以正负步长递增**

我们可以在 python 中使用 range 来使用正整数和负整数递增和递减步长值，下面的程序展示了我们如何使用正步长值和负步长值获得两种顺序的数字序列。

```
for i in range(2, 20, 5):
     print(i, end=", ")
for j in range(25, 0 , -5):
     print(j , end=", ")

```

```
Output: 2, 7, 12, 17, 25, 20, 15, 10, 5
```

## **范围内的浮点数**

range 函数不支持函数中的浮点数或非整数，但是有一些方法可以解决这个问题，并且仍然可以获得一个具有浮点值的序列。下面的程序显示了一种方法，我们可以遵循使用浮动范围。

```
def frange(start , stop, step):
     i = start
     while i < stop:
             yield i
             i += step

for i in frange(0.6, 1.0, 0.1):
     print(i , end=",")

```

```
Output: 0.6, 0.7, 0.8, 0.9
```

## **Python 中的反向范围**

下面的程序展示了如何在 python 中反转范围。它将返回[反向](https://www.edureka.co/blog/how-to-reverse-a-string-in-python/)中前 5 个自然数的列表。

```
for i in range(5, 0, -1):
    print(i, end=", ")

```

```
Output: 5, 4, 3, 2, 1, 0
```

## **射程 vs XRange**

*   range 和 xrange 的主要区别在于，range 返回 python 列表对象，而 xrange 返回 xrange 对象。
*   在很大程度上，range 和 xrange 基本上执行相同的功能，按照用户喜欢的顺序提供数字序列。
*   xrange 不像 range 在运行时那样生成静态列表。它使用一种称为让步的特殊技术来创建我们需要的值，这种技术被称为生成器的对象所使用。
*   如果需要多次迭代一个序列，最好使用 range 而不是 xrange。
*   在 python 3 中，xrange 已经不存在了，所以用 range 代替比较理想。我们可以使用 python 提供的 2to3 工具来转换您的代码。

**串联两个测距函数**

在下面的程序中，两个范围函数之间有一个连接。

```
from itertools import chain 

res = chain(range(10) , range(10, 15))
for i in res:
    print(i , end=", ")

```

```
Output: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14
```

## **使用索引值访问范围**

下面的程序展示了我们如何使用索引来访问 range。

```
a = range(0,10)[3]
b = range(0,10)[5]
print(a)
print(b)

```

```
Output: 3
        5
```

## **将范围转换为列表**

下面的程序展示了如何使用类型转换将范围转换为列表。

```
a = range(0,10)
b = list(a)
c = list(range(0,5))
print(b)
print(c)

```

```
Output: [0,1,2,3,4,5,6,7,8,9]
        [0,1,2,3,4]
```

## **点记**

*   python 中的 range 函数只能处理整数或整数。
*   range 函数中传递的参数不能是除整数数据类型以外的任何其他数据类型。
*   传递的三个参数都可以是正整数或负整数。
*   步骤参数值不能为零，否则将引发 ValueError 异常。
*   python 中的 range 函数也是数据类型之一。
*   您可以使用索引值访问 range 函数中的元素，就像列表数据类型一样。

本文的最后，我们通过几个例子学习了如何在 python 中使用 range，包括 python 中的 for 循环和 python 中 range 与 xrange 的区别。我希望你清楚本教程中与你分享的所有内容。

*如果您发现这篇文章与“Python 中的范围”相关，请查看  [Edureka Python 认证培训，](https://www.edureka.co/data-science-python-certification-course)一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*我们在这里帮助你踏上旅程的每一步，并为想要成为  [Python 开发者](https://www.edureka.co/blog/how-to-become-a-python-developer/)的学生和专业人士设计课程。该课程旨在让您在 Python 编程方面有一个良好的开端，并训练您掌握核心和高级 Python 概念以及各种  [Python 框架](https://www.edureka.co/blog/python-frameworks/) ，如  [Django。](https://www.edureka.co/blog/django-tutorial/)*

如果您遇到任何问题，请在“Python 中的范围”的评论部分提出您的所有问题，我们的团队将很乐意回答。