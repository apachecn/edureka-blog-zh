# 关于 Python 中的线性搜索，您需要知道的是

> 原文：<https://www.edureka.co/blog/linear-search-in-python/>

[PYTHON](https://www.edureka.co/blog/python-tutorial/) 是现在流行的编程应用之一。与 C 语言不同，它不需要很多下面的命令，并且尽可能的对用户友好。在本文中，我们将按以下顺序理解 python 中的线性搜索:

*   [搜索类型](#type)
*   什么是线性搜索？
*   [线性搜索代码](#code)

## **搜索类型**

基本上，有两种类型的搜索。

*   线性搜索
*   [二分搜索法](https://www.edureka.co/blog/binary-search-in-c/)

在这篇博客中，只讨论线性搜索。线性搜索是初学者学习的最流行和最基本的程序之一。下面给出的程序执行线性搜索。 线性搜索是在用户给出的数字数组中搜索一个给定的数字，并打印出该数字在所有给定输入中的给定位置。

## 什么是线性搜索？

线性搜索，也称为顺序搜索，是一种在列表中查找元素的方法。

![Linear Search in Python](img/4c6f99f56333f713cda7948445645f94.png)

它按顺序检查列表中的每个元素，直到找到一个匹配项，或者整个列表都被搜索完。

## **线性搜索代码**

```
lst = []

num = int(input("Enter size of list: t"))
for n in range(num):

    numbers = int(input("Enter the array of numbers: t"))
    lst.append(numbers)
x = int(input("nEnter number to search: t"))
found = False
for i in range(len(lst)):
    if lst[i] == x:
        found = True
        print("n%d found at position %d" % (x, i+1))
        break
if not found:
    print("n%d is not in list" % x)
input()

```

## **功能说明**

*   输入数组的大小。

*   输入每个输入后，按回车键。

*   输入数字数组。

*   输入要搜索的号码。

*   将显示从数字 1 开始的给定位置。

*   如果号码不在列表中，将执行“号码不在列表中”语句。

*   给定程序的结果可以在程序执行结束时看到。

至此，我们结束了这篇关于 Python 中线性搜索的文章。我希望你已经清楚如何使用线性搜索。

*如果您发现这篇文章与“Python 中的线性搜索”相关，请查看  [Edureka Python 认证培训，](https://edureka.co/python)一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*我们在这里帮助你踏上旅程的每一步，并为想要成为  [Python 开发者](https://www.edureka.co/blog/how-to-become-a-python-developer/)的学生和专业人士设计课程。该课程旨在让您在 Python 编程方面有一个良好的开端，并训练您掌握核心和高级 Python 概念以及各种  [Python 框架](https://www.edureka.co/blog/python-frameworks/) ，如  [Django。](https://www.edureka.co/blog/django-tutorial/)*

如果您遇到任何问题，请在“Python 中的线性搜索”的评论部分提出您的所有问题，我们的团队将很乐意回答。