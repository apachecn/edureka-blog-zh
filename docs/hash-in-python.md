# 关于 Python 中 Hash 的所有知识

> 原文：<https://www.edureka.co/blog/hash-in-python/>

在现代商业动态中，你能想象到的每一种需求都有一个应用程序。无论是记录你每周的游泳时间还是寻找镇上最好的餐馆。Python 是一种语言，其中许多应用程序都是在这种语言中构建的，因为它拥有广泛的特性。本文将展示 Python 中的 Hash 这样一个概念。

本文将涉及以下几点:

*   [Python 中的 Hash 方法是什么？](#WhatIsHashMethodInPython?)
*   [哈希方法的示例程序](#SampleProgramForHashMethod)
*   [对不可变元组对象使用哈希方法](#UsingHashMethodForImmutableTupleObjects)
*   [自定义对象的哈希方法](#HashMethodForCustomObjects)
*   [样本程序 1](#SampleProgram1)
*   [样本程序 2](#SampleProgram2)

那么，让我们开始吧，

## **Python 中的哈希**

Python 是当今业界最流行的高级编程语言之一。Python 建立在 C 平台上，是一种面向对象的编程语言，它不仅具有高度的通用性，而且具有大量的特性，使开发人员能够创建高级应用程序。作为一种编程语言，Python 附带了一个内置库，其中有数百个模块和函数。其中之一是哈希模块。在这篇文章中，我们将讨论更多关于 hash 模块的内容，它的特性，以及如何在日常编程中使用它。

在我们进入 Python 文章中的散列细节之前，让我们快速理解下面的主题，

## **Python 中的 Hash 方法是什么？**

Python 中的 Hash method 是一个模块，用来返回对象的哈希值。在编程中，hash 方法用于返回整数值，这些整数值用于使用字典查找功能来比较字典键。使用时，它调用对象的 __hash__()值，默认情况下，该值是在用户创建对象的过程中设置的。

使用哈希方法的语法如下。

```
hash(object)
```

**哈希方法的参数**

hash 方法作为一个模块只接受单个参数。

**Object:** 这表示用户需要返回其哈希值的对象，可以是整数、字符串或浮点的形式。

**散列方法的返回值**

使用时，hash 方法返回一个对象的哈希值(如果存在的话)。如果在某种情况下，对象有一个自定义的哈希值，那么该方法将哈希值截断为 Py_ssize_t.

让我们继续 Python 文章中的 Hash，看看一个示例程序，在此之前，我们会给出一个建议，以确保您已经安装了所有必需的[软件](https://www.python.org/downloads/)，

## **哈希方法的示例程序**

为了更好地理解 hash 方法的功能和用途，我们来看几个例子。

```
# hash for integer unchanged
print('Hash for 181 is:', hash(181))
# hash for decimal
print('Hash for 181.23 is:',hash(181.23))
# hash for string
print('Hash for Python is:', hash('Python'))
```

**输出**

181 的哈希是:181

181.23 的哈希是:530343892119126197

Python 的哈希是:3607259692854166150

继续这篇文章，让我们看看下一个方法

**对不可变元组对象使用哈希方法**

```
# tuple of vowels
vowels = ('a', 'e', 'i', 'o', 'u')
print('The hash is:', hash(vowels))
```

运行时，上述程序的输出将如下所示。

哈希是:-7033539107181453990

【hash 如何为自定义对象工作？

如前所述，当使用 hash 方法时，调用对象的 __hash__()。这意味着任何对象都可以覆盖对象的自定义哈希值。

但是为了得到正确的散列值，该方法总是需要返回一个整数，因此需要同时使用 __eq__()和 __hash__()来找到相同的值。

参考下表，了解自定义哈希值的实现。

| **__eq__** **()** | **_ _ 哈希 __()** | **描述** |
| ***(如果可变)定义了*** | 不应被定义 | 这要求密钥哈希值是不可变的。 |
| (默认)定义 | 已定义(默认) | 所有的物体都是不平等的。 |
| ***未定义*** | 不应被定义 | 如果 __eq__()没有定义，那么 hash 也不需要定义。 |
| ***定义了*** | 未定义 | __hash__()将被设置为无。引发了 TypeError。 |
| ***定义了*** | 从父项保留 | _ _ 哈希 __ = <父类>。__ 哈希 __ |
| ***定义了*** | 不想哈希 | _ _ 哈希 __ =无引发了 TypeError。 |

关于 Python 中的 Hash，本文中另一个有趣的地方是为定制对象实现 Hash 方法，

**自定义对象的哈希方法**

```
class Person:
def __init__(self, age, name):
self.age = age
self.name = name
def __eq__(self, other):
return self.age == other.age and self.name == other.name
def __hash__(self):
print('The hash is:')
return hash((self.age, self.name))
person = Person(23, 'Adam')
print(hash(person))
```

运行时，上面程序的输出会是这样的，

哈希为:

5445254133660435902

注意:对于上面的程序，不需要实现 __eq__()方法，因为默认情况下它是为所有对象创建的。

现在让我们看几个示例程序，

**样本程序 1**

```
# Python 3 code to demonstrate
# working of hash()
# initializing objects
int_val = 4
str_val = 'PythonIsBest'
flt_val = 24.56
# Printing the hash values.
# Notice Integer value doesn't change
# You'l have answer later in article.
print ("The integer hash value is : " + str(hash(int_val)))
print ("The string hash value is : " + str(hash(str_val)))
print ("The float hash value is : " + str(hash(flt_val)))
```

上述程序的输出将是，

整数哈希值为:4

字符串哈希值为:2063534490514258345

浮点哈希值为:1291272085159665688

这就把我们带到了这篇关于 Python 中散列的文章的最后一点，

**样本程序 2**

```
# Python 3 code to demonstrate
# property of hash()
# initializing objects
# tuple are immutable
tuple_val = (1, 2, 3, 4, 5)
# list are mutable
list_val = [1, 2, 3, 4, 5]
# Printing the hash values.
# Notice exception when trying
# to convert mutable object
print ("The tuple hash value is : " + str(hash(tuple_val)))
print ("The list hash value is : " + str(hash(list_val))) 
```

上述程序的输出将是，

**![Output - Hash In Python - Edureka](img/0d08ab1173715093a704d4c7c56951ae.png)**

**结论**

hash 方法是 Python 库中最有用的模块之一。现在你已经知道了它的功能和用途，我们希望你能在日常编码中更多地使用它。所以这篇文章到此结束，我希望你学到了一些新的好东西。

*要深入了解 Python 及其各种应用，您现在就可以注册参加实时 [Python 课程](https://www.edureka.co/python-programming-certification-training)培训，该课程提供全天候支持和终身访问。*

*有问题吗？在这篇文章的评论部分提到它们，我们会给你回复。*