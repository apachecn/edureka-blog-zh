# 如何在 Python 中求列表长度？

> 原文：<https://www.edureka.co/blog/python-list-length/>

Python 中的列表是一种有序且可变的集合数据类型。一个列表也可以有重复条目。Python 的 len()方法用于查找任何对象的长度。在本文中，我们将按照以下顺序学习如何在 [python 编程](https://www.edureka.co/blog/python-programming-language)中找到列表的长度:

*   [Python 中的列表](#list)
*   [如何在 Python 中求列表的长度？](#length)
    *   [Len()方法](#len)
    *   [天真的方法](#naive)

## **Python 中的列表**

Python 中的[列表用于存储各种类型数据的序列。然而，Python](https://www.edureka.co/blog/lists-in-python/) 中有六种[数据类型能够存储序列，但最常见和最可靠的类型是列表。要了解更多关于 python 的知识，你可以加入我们的](https://www.edureka.co/blog/python-data-types/)[Python 编程大师](https://www.edureka.co/masters-program/python-developer-training)课程。

![list in python - length of list in python - edureka](img/a39aca7a5e737f73ff2b6922bccc2d37.png)

列表被定义为不同类型的值或项目的集合。列表中的项目用逗号(，)分隔，并用方括号[]括起来。

其定义如下:

```
list1 = ['edureka', 'python', 2019];
list2 = [1, 2, 3, 4, 5 ];
list3 = ["a", "b", "c", "d"];
```

*如果你想深入学习人工智能和机器学习，来找我们，报名参加这个研究生文凭 [AI 和 ML 课程](https://www.edureka.co/executive-programs/machine-learning-and-ai)。*

## **如何在 Python 中求列表的长度？**

在 Python 中，有两种最常用和最基本的方法用于查找列表的长度:

*   Len()方法
*   朴素方法

## **Len()方法**

有一个名为 len()的内置函数，用于获取列表、元组、[数组、](https://www.edureka.co/blog/arrays-in-python/)字典等的总项数。len()方法接受一个参数，您可以在其中提供一个列表，它返回给定列表的长度。

len() [方法](https://www.edureka.co/blog/python-method-overloading/)是 Python 中查找列表长度最常用和最方便的方法之一。这是当今所有程序员采用的最常规的技术。

**了解我们在顶级城市/国家的 Python 培训**

| **印度** | **美国** | **其他城市/国家** |
| [班加罗尔](https://www.edureka.co/python-programming-certification-training-bangalore) | [纽约](https://www.edureka.co/python-programming-certification-training-new-york-city) | [英国](https://www.edureka.co/python-programming-certification-training-uk) |
| [海德拉巴](https://www.edureka.co/python-programming-certification-training-hyderabad) | [芝加哥](https://www.edureka.co/python-programming-certification-training-chicago) | 伦敦 |
| [德里](https://www.edureka.co/python-programming-certification-training-delhi) | 亚特兰大 | [加拿大](https://www.edureka.co/python-programming-certification-training-canada) |
| [钦奈](https://www.edureka.co/python-programming-certification-training-chennai) | [休斯顿](https://www.edureka.co/python-programming-certification-training-houston) | [多伦多](https://www.edureka.co/python-programming-certification-training-toronto) |
| [孟买](https://www.edureka.co/python-programming-certification-training-mumbai) | 洛杉矶 | [澳大利亚](https://www.edureka.co/python-programming-certification-training-australia) |
| [浦那](https://www.edureka.co/python-programming-certification-training-pune) | [波士顿](https://www.edureka.co/python-programming-certification-training-boston) | 阿联酋 |
| 加尔各答 | [迈阿密](https://www.edureka.co/python-programming-certification-training-miami) | [迪拜](https://www.edureka.co/python-programming-certification-training-dubai) |
| 艾哈迈达巴德 | [旧金山](https://www.edureka.co/python-programming-certification-training-san-francisco) | [菲律宾](https://www.edureka.co/python-programming-certification-training-philippines) |

**语法:**

```
len(list)
```

List 参数是一个要计算元素个数的列表。它返回列表中元素的数量。

**举例:**

```
ListName = ["Hello", "Edureka", 1, 2, 3]
print ("Number of items in the list = ", len(ListName))
```

**输出:** 5

## **天真的方法**

len()方法是在 [Python](https://www.edureka.co/blog/python-programming-language) 中查找列表长度最常用的方法。但是有另一个基本方法可以提供列表的长度。

在简单的方法中，只需运行一个[循环](https://www.edureka.co/blog/videos/python-loops/)并增加计数器，直到列表的最后一个元素知道它的计数。这是在没有其他有效技术的情况下可以使用的最基本的策略。

**举例:**

```
ListName = [ "Hello", "Edureka", 1,2,3 ]
print ("The list is : " + str(ListName))
counter = 0
for i in ListName:
counter = counter + 1
print ("Length of list using naive method is : " + str(counter))
```

**输出:**

```
The list is : ["Hello", "Edureka", 1,2,3]
Length of list using naive method is : 5
```

这一切都是为了在 Python 中找到列表的长度。len()方法是最常用的方法。然而，你也可以使用基本的方法，在朴素方法的帮助下找到长度。

说到这里，我们的文章就到此为止了。我希望你明白如何在 Python 中找到任何列表的长度。

*要深入了解 Python 及其各种应用，您可以注册参加现场 [**Python 认证**](https://www.edureka.co/python-programming-certification-training) 培训，该培训提供全天候支持和终身访问。*

*有问题吗？请在这个“Python 列表长度”博客的评论部分提到它，我们会尽快回复你，或者参加我们在钦奈的 [Python 培训](https://www.edureka.co/python-programming-certification-training-chennai)。*