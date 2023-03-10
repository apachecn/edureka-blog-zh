# Python Tuple 与示例:您需要知道的一切

> 原文：<https://www.edureka.co/blog/tuple-in-python/>

Python 编程语言有各种各样的[数据类型](https://www.edureka.co/blog/variables-and-data-types-in-python/)，包括[列表](https://www.edureka.co/blog/lists-in-python/)、[集合](https://www.edureka.co/blog/sets-in-python/)、[字典](https://www.edureka.co/blog/dictionary-in-python/)等。Python 还附带了一个具有专门数据结构的[集合](https://www.edureka.co/blog/collections-in-python/)包。 [python](https://www.edureka.co/data-science-python-certification-course) 中的 Tuple 也是流行的集合数据类型之一。在本文中，我们将通过示例详细了解 Python 元组函数。以下是本博客涵盖的主题:

*   [什么是元组？](#tuple)
*   [访问元组中的项目](#accessing)
    *   [索引](#indexing)
    *   [切片](#slicing)
*   [改变一个元组](#changing)
*   [连接两个元组](#concat)
*   [删除元组](#deleting)
*   [元组方法](#methods)
*   [列表 vs 元组](#list)
*   [遍历一个元组](#iterating)
*   [元组构造器](#constructor)
*   [元组中的成员资格测试](#membership)

## **什么是元组？**

在 python 中，tuple 是一种不可变的数据类型,在索引和拥有重复成员方面几乎类似于 python 中的 list。它是一种集合数据类型，存储用逗号分隔的 python 对象。下面是一个如何用 python 创建或声明元组的例子。

```
#creating a tuple
a = ('python', 'edureka')
#another approach
b = 'python' , 'edureka' 
print(a)
print(b)

```

```
Output: ('python' , 'edureka')
        ('python' , 'edureka')
```

## **访问 Python 元组中的项目**

访问元组中的项目的工作方式类似于列表，我们可以使用索引来访问列表中的元素。我们可以指定索引值，它将返回存储在该特定索引值的项目。

### **索引**

它是一种从数据结构中有效检索信息的数据结构技术。在 python 中，有几种数据类型支持索引，如[列表](https://www.edureka.co/blog/lists-in-python/)、[字符串](https://www.edureka.co/blog/what-is-string-in-python/)等。

例如，假设我们有一个元组，成员是 5 个自然数。因此，索引将从值 0 开始，其中 1 将被存储，并且它将一直进行到元组的末尾，即 5，并且 5 处的索引值将是 4。

看一下下面的例子，了解我们如何使用索引来访问 python 元组中的元素

```
a = ('edureka', 'python' , 'data structure' , 'collections')
print(a[1])
print(a[3])

```

```
Output: python
        collections
```

正如您在上面的例子中看到的，我们能够获得存储在索引值 1 和 3 处的元素。类似地，我们可以使用索引值访问元组中的任何值。

**负分度**

在 python 中，我们也可以使用负索引来访问元组中的元素或任何其他支持索引的数据类型。

```
a = (1,2,3,4,5,6,7,8,9,10)
print(a[-4])
print(a[-1])

```

```
Output: 7
        10
```

### **切片**

在这种技术中，我们使用切片[操作符](https://www.edureka.co/blog/operators-in-python/)':'从 python tuple 或任何其他支持访问元素的索引的数据类型中获取一系列元素。

```
a = (1,2,3,4,5,6,7,8,9,10)
print(a[1:8])
print(a[1:])
print(a[:5])

```

```
Output: (2,3,4,5,6,7,8)
        (2,3,4,5,6,7,8,9,10)
        (1,2,3,4,5)
```

在上面的 Python Tuple 示例中，切片运算符之前的索引值是起始索引，切片运算符之后的索引值是不会包含在输出中的值。

直到结束索引之前的值才会包含在输出中。我们甚至可以通过切片操作符使用负索引值来从元组中获取值的范围。

```
a = (1,2,3,4,5,6,7,8,9,10)
print(a[-8:])

```

```
Output: (3,4,5,6,7,8,9,10)
```

## **改变一个 Python 元组**

尽管 python 中的元组本质上是不可变的，但是元组中嵌套的[对象](https://www.edureka.co/blog/python-class/)是可以改变的。或者一般来说，python 元组可以被重新分配不同的值。

```
a = (1,2,3,[4,5])
a[3][0] = 14
print(a)
#reassigning the value
a = ('edureka', 'python')
print(a)

```

```
Output: (1,2,3,[14,5])
        ('edureka', 'python')
```

## **串联二元组**

连接两个元组是一件非常容易的事情。您只需将两个元组的相加赋值给另一个变量，它将返回包含两个元组值的连接元组。考虑下面的例子来理解这一点。

```
a = (1,2,3,4,5)
b = (6,7,8,9,10)
c = a + b
print(c)

```

```
Output: (1,2,3,4,5,6,7,8,9,10)
```

正如您在示例中看到的，串联元组包含元组 a 和 b 的值。

## **删除一个 Python 元组**

作为一种不可变的数据类型，python 中的 tuple 不允许任何改变，甚至不能在声明之后从 tuple 中移除元素。但是有一个关键字‘del’会将元组一起删除。

```
a = (1,2,3,4,5)
del a
print(a)

```

如果您运行上面的程序，您将会得到一个名称错误，因为没有名为 present 的元组，因为我们已经删除了它。

## **元组方法**

下面是我们在 python 中处理元组时可以使用的元组方法。

*   count:返回项目的计数。
*   index:返回指定项目的索引。

```
a = (1,2,1,3,1,3,1,2,1,4,1,5,1,5)
print(a.count(1))
print(a.index(5))

```

```
Output: 7
        11
```

## **列表 vs 元组**

| **列表** | **元组** |
| 用于同质数据类型 | 通常用于异构数据类型 |
| 本质上易变 | 本质上不可变，这有助于更快的迭代 |
| 没有不可变的元素 | 不可变元素可以用作字典的键 |
| 不保证数据写保护 | 用不变的数据实现元组可以保证它是写保护的 |

## **遍历一个 Python 元组**

使用 for 循环，我们可以遍历 python 中的元组。下面的例子展示了我们如何使用循环的[来遍历一个元组。](https://www.edureka.co/blog/loops-in-python/)

```
a = ("edureka", "for data science", "for Artificial Intelligence")
for i in a:
    print("python", i)

```

```
Output: python edureka
        python for data science
        python for artificial intelligence
```

## **Python 元组构造器**

也可以使用 tuple() [构造函数](https://www.edureka.co/blog/object-oriented-programming-python/)创建一个元组。我们甚至可以使用 tuple 构造函数将一个列表变成一个元组。

```
a = [1,2,3,4,5]
b = tuple(a)
print(b)
c = tuple(('edureka', 'python'))
print(c)

```

```
Output: (1,2,3,4,5)
        ('edureka', 'python')
```

## **元组中的成员测试**

在 python 中使用[成员操作符](https://www.edureka.co/blog/operators-in-python/)‘in ’,我们可以检查一个元素是否存在于一个元组中。下面的例子展示了我们如何检查一个元素是否存在于一个元组中。

```

a = (1,2,3,4,5,6,7,8,9,10)

print(6 in a)

print(15 in a )

```

```
Output: True 
        False
```

在本文的最后，我们学习了如何在 python 中使用 tuple，以及如何通过各种其他示例使用索引来访问 tuple 中的元素。我希望你清楚本教程中与你分享的所有内容。

*如果您发现这篇文章与“Python 中的元组”相关，请查看一下  Edureka [Python 认证](https://www.edureka.co/python-programming-certification-training)培训，这是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*我们在这里帮助你踏上旅程的每一步，并为想要成为  [Python 开发者](https://www.edureka.co/blog/how-to-become-a-python-developer/)的学生和专业人士设计课程。该课程旨在让您在 Python 编程方面有一个良好的开端，并训练您掌握核心和高级 Python 概念以及各种  [Python 框架](https://www.edureka.co/blog/python-frameworks/) ，如  [Django。](https://www.edureka.co/blog/django-tutorial/)*

如果您遇到任何问题，请在“Python 中的 Tuple”的评论部分提出您的所有问题，我们的团队将很乐意回答。