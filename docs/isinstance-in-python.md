# Python 中 Isinstance 是什么，如何实现？

> 原文：<https://www.edureka.co/blog/isinstance-in-python/>

Python 是当今市场上最强大的编程语言之一。Python 还支持在其生态系统中实现其他编程语言，如 Java、C 以及 C++。在 Python 生态系统中可用的许多模块和函数中，最突出的一个是 Python 中的 isinstance。因此，在本文中，我们将详细讨论 isinstance、它的用途以及它带来的特性。

本文将涉及以下几点:

*   [Python 中的 Isinstance 是什么？](#%20WhatisIsinstanceinPython?)
*   [is instance 的参数和返回值](#ParameterandReturnValueofIsinstance)
*   [在 Python 中使用类型](#UseeofTypeinPython)
*   [类型()和 Isinstance 之间的差异](#DifferencebetweenType()andIsinstance)

我们开始吧！

## **Python 中的 Isinstance 是什么？**

Python isinstance 用于检查作为参数的第一个对象是否是作为第二个参数的 classinfo 类的实例或子类。

Python 中 isinstance 的语法如下。

```
isinstance(object, classinfo)
```

让我们看看 Python 中 Isinstance 有哪些参数和返回值，

## **is instance 的参数和返回值**

**参数**

现在你已经知道了 isinstance 的语法，让我们仔细看看它所考虑的参数。

1.  对象:这是需要检查的对象。
2.  Classinfo:这是对象需要检查的类、信息或类元组。

**返回值**

当在程序中使用 isinstance 时，返回值取决于许多条件，如下面的指针中所解释的。

1.  如果对象是 classinfo 或类元组的子类，则返回 True。
2.  如果对象不是 classinfo 或类元组的子类，则返回 False。

如果在特定的情况下，classinfo 不是一个类型或一组类型，那么用户的屏幕上会出现一个 typeerror 异常。

**例题**

为了更好地理解 isinstance 的用法，让我们看几个例子。

**例#1**

```
class Foo:
  a = 5
fooInstance = Foo()
print(isinstance(fooInstance, Foo))
print(isinstance(fooInstance, (list, tuple)))
print(isinstance(fooInstance, (list, tuple, Foo)))
```

**输出**

真

假

真

**是 Python 中的实例:例 2**

```
numbers = [1, 2, 3]
result = isinstance(numbers, list)
print(numbers,'instance of list?', result)
result = isinstance(numbers, dict)
print(numbers,'instance of dict?', result)
result = isinstance(numbers, (dict, list))
print(numbers,'instance of dict or list?', result)
number = 5
result = isinstance(number, list)
print(number,'instance of list?', result)
result = isinstance(number, int)
print(number,'instance of int?', result)
```

**输出**

[1，2，3]列表实例？真

[1，2，dict 的实例？假

[1，2，3]字典或列表的实例？真

列表的 5 个实例？假

5 int 的实例？真

**例 3**

```
# Python code for isinstance()
class Test:
a = 5
TestInstance = Test()
print(isinstance(TestInstance, Test))
print(isinstance(TestInstance, (list, tuple)))
print(isinstance(TestInstance, (list, tuple, Test))) 
```

**输出**

真

假

真

让我们继续“Python 中的 Isinstance”这篇文章，并理解类型方法的使用，

## **Python 中类型的使用**

与 isinstance 类似，Python 中还有另一个内置方法，用于检查运行时使用的 pf 变量的类型。如果通过 type 方法传递单个参数或对象，它将返回运行时使用的对象的类型。

为了更好地理解这一点，请看下面的例子。

#### **是 Python 中的实例:示例#1.1**

```
# Python code type() with a single object parameter
x = 5
s = "sampleoutput"
y = [1,2,3]
print(type(x))
print(type(s))
print(type(y)) 
```

**输出** 输出

类‘int’

类‘str’

类‘列表’

**例 1.2**

```
# Python code for type() with a name,
# bases and dict parameter
o1 = type('X', (object,), dict(a='Foo', b=12))
print(type(o1))
print(vars(o1))
class test:
a = 'Foo'
b = 12
o2 = type('Y', (test,), dict(a='Foo', b=12))
print(type(o2))
print(vars(o2)) 
```

**输出**

{'b': 12，' a': 'Foo '，' __dict__ ':，' __doc__ ':无，' __weakref__': }

{'b': 12，' a': 'Foo '，' __doc__ ':无}

让我们比较一下 Python 中的 Type 和 Isinstance，

## **类型()和 Isinstance 之间的差异**

Python 中的 Type 和 isinstance 有两种截然不同的功能。看看下面的指针，更好地理解它们之间的区别。

1.  如果你需要检查一个对象是否有某种类型，那么最好使用 isinstance。这是因为 isinstance 将能够检查第一个参数中传递的对象是否与第二个参数中传递的对象类型相同。
2.  另一方面，当你需要简单地检查一个特定对象的类型，而不是与另一个对象进行比较时，使用 type 更好。

**例题**

```
#Python code to illustrate duck typing
class User(object):
def __init__(self, firstname):
self.firstname = firstname
@property
def name(self):
return self.firstname
class Animal(object):
pass
class Fox(Animal):
name = "Fox"
class Bear(Animal):
name = "Bear"
# Use the .name attribute (or property) regardless of the type
for a in [User("SampleOutput"), Fox(), Bear()]:
print(a.name) 
```

**输出**

样本输出

福克斯

熊

不使用类型方法的另一个原因是缺少继承。看一下下面分享的例子可以更好地理解这一点。

```
#python code to illustrate the lack of
#support for inheritance in type()
class MyDict(dict):
"""A normal dict, that is always created with an "initial" key"""
def __init__(self):
self["initial"] = "some data"
d = MyDict()
print(type(d) == dict)
print(type(d) == MyDict)
d = dict()
print(type(d) == dict)
print(type(d) == MyDict) 
```

**输出** 输出

假

真

真

假

所以这个 it 家伙，这就把我们带到了这篇文章的结尾。我希望你已经理解了 Python 中的 Isinstance 及其作用。

*要深入了解 Python 及其各种应用，您可以 [**在此**](https://www.edureka.co/python/) 注册参加在线直播培训，全天候支持，终身访问。*

*有问题吗？在这篇文章的评论部分提到它们，我们会给你回复。*