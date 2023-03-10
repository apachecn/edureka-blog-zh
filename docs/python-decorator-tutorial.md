# Python 装饰者教程:如何在 Python 中使用装饰者

> 原文：<https://www.edureka.co/blog/python-decorator-tutorial/>

python 中的函数提供了任何程序的运行逻辑的优化实现，多次执行都没有麻烦。python 中的装饰者也围绕着 [Python 函数的概念。](https://www.edureka.co/blog/python-functions)在本文中，我们将详细介绍[Python](https://www.edureka.co/data-science-python-certification-course)decorator，包括 python decorator 教程中的各种例子。本博客讨论了以下主题。

*   [Python 中有哪些函数？](#functions)
    *   [一等物体](#first)
    *   [内部函数](#inner)
*   [Python 中的装饰者](#deco)
    *   [带参数的装饰器](#arg)
    *   [返回值](#return)
*   [Python 中奇特的装饰者](#fancy)
    *   [类装饰器](#cls)
    *   [单例类](#single)
    *   [嵌套装饰器](#nested)

## **Python 中有哪些函数？**

Python 中的 Decorators 是一个高级主题。因此，在继续之前，请确保您完全了解 python 函数的概念。在继续学习 Python 中的 decorators 之前，有几个先决条件必须理解。

*   一级[对象](https://www.edureka.co/blog/python-class/)

*   内部函数

### **一等品**

在 python 中，一切都被视为一个对象，包括所有的[数据类型](https://www.edureka.co/blog/variables-and-data-types-in-python/)、[函数](https://www.edureka.co/blog/function-map-filter-reduce/)。因此，函数也被称为一级对象，可以作为参数传递。

让我们看一个例子来理解它是如何工作的。

```
def func1(name):
    return f"Hello {name}"
def func2(name):
    return f"{name}, How you doin?"
def func3(func4):
    return func4('Dear learner')

print(func3(func1))
print(func3(func2))

```

```
Output: Hello Dear learner
        Dear learner, how you doin?
```

在上面的例子中，我们使用了[字符串插值](https://www.edureka.co/blog/strings_in_python/)来获取名称，并将 func1 和 func2 作为参数传递给 func3。

### **内部函数**

在 python 中，可以在函数内部定义函数。这个函数叫做内部函数。这里有一个例子来展示我们如何在 python 中使用内部函数。

```
def func():
     print("first function")
     def func1():
           print("first child function")
     def func2():
           print(" second child function")
     func1()
     func2()
func()

```

```
Output: first function
        first child function
        second child function
```

在上面的程序中，如何声明子函数并不重要。输出取决于子函数的执行方式。它们是用 func()局部限定的，所以不能单独调用。

如果你单独调用它们，你会得到一个错误，因为它们被存储为 func()中的[变量](https://www.edureka.co/blog/variables-and-data-types-in-python/)，并且只有在 func()被调用时才能被调用。

**从函数返回函数**

可以使用另一个函数返回一个函数。看一下下面的例子来理解这一点。

```

def func(n):
      def func1():
          return "edureka"
      def func2():
          return "python"
      if n == 1:
          return func1
      else:
          return func2
a&nbsp; = func(1)
b = func(2)
print(a())
print(b())

```

```
Output: edureka
        python
```

## **Python 中的装饰者**

python 中的 Decorators 非常强大，它可以修改函数的行为，而不用永久地修改它。它基本上包装了另一个函数，因为两个函数都是可调用的，所以它返回一个可调用的。

事后看来，装饰者包装了一个函数并修改了它的行为。让我们看一个简单的例子来理解如何在 python 中使用 decorators。

```
 def function1(function):
      def wrapper():
            print("hello")
            function()
            print("welcome to python edureka")
      return wrapper
def function2():
      print("Pythonista")
function2 = function1(function2)

function2()

```

```
Output: hello
        pythonista
        welcome to python edureka
```

为了让程序员的工作变得简单一些，我们为 python decorators 提供了一个语法糖。看看下面的例子，了解它是如何工作的。

```
def function1(function):
      def wrapper():
           print("hello")
           function()
           print("how are you?")
      return wrapper
@function1
def function2():
      print("pythonista")

function2()

```

```
Output: hello
        pythonista
        how are you?
```

输出将类似于上面的程序，唯一的区别是我们使用了带有@符号的 pie 语法。

### **使用带参数的装饰器**

当你有一个带参数的函数时，修饰函数就变得更棘手了，因为它在声明中也需要参数。为了解决这个问题，我们可以在内部包装函数中使用*args 和**kwargs。看一下下面的例子来理解这一点。

```
def function1(function):
      def wrapper(*args, **kwargs):
            print("hello")
            function(*args, **kwargs)
            print("welcome to edureka")
      return wrapper
@function1 
def function2(name):
      print(f"{name}")

function2("pythonista")

```

```
Output: hello
        pythonista
        welcome to edureka
```

### **从修饰函数返回值**

让我们看一个例子，看看我们如何从一个修饰函数返回值。

```
def function1(function):
     def wrapper(*args, **kwargs):
           function(*args, **kwargs)
           print("it worked")
     return wrapper
@function1 
def function2(name):
      print(f"{name}")

function2("python")

```

```
Output: python
        it worked
```

确保使用参数返回包装函数，以避免任何错误。

## **Python 中的花式装饰师**

现在我们已经知道了装饰器在 python 中是如何工作的，让我们借助一些例子来探索一个相当复杂的特性。

### **类装修工**

在 python 中有两种方法来修饰一个类。第一个是你可以修饰类中的方法，python 中有内置的修饰器，比如@classmethod、@staticmethod 和@property。@classmethod 和@staticmethod 在不连接到类的任何其他实例的类中定义方法。@property 通常用于自定义类属性的 getters 和 setters。让我们看一个例子来理解这一点。

```
class Square:
        def __init__(self, side):
             self._side = side
        @property 
        def side(self):
              return self._side
        @side.setter
         def side(self, value):
               if value &gt;= 0:
                  self._side = value
               else:
                  print("error")
         @property 
          def area(self):
               return self._side ** 2
         @classmethod
          def unit_square(cls):
               return cls(1)
s = Square(5)
print(s.side)
print(s.area)

```

```
Output: 5
        25
```

装饰班级的另一种方法是装饰整个班级。让我们举个例子来理解这一点。

```
from dataclasses import dataclass
@dataclass
class Cards:
       rank: str
       suit: str

```

装饰一个类并不反映它的方法。这几乎类似于编写一个函数的装饰器，唯一的区别是参数中的类而不是函数。

### **单例类**

单例类只有一个实例。python 中有大量的单例，包括 True、None 等。让我们看一个例子来更好地理解这一点。

```
import functools

def singleton(cls):
      @functools.wraps(cls)
       def wrapper(*args, **kwargs):
             if not wrapper.instance:
                wrapper.instance = cls(*args, **kwargs)
             return wrapper.instance
       wrapper.instance = None
       return wrapper

@singleton
class One:
       pass

first = One()
second = One()
print(first is second)

```

```
Output: True
```

使用“is”仅对相同实例的对象返回 true。上面的例子使用了与任何其他函数装饰器相同的方法。唯一的区别是我们使用了 cls 而不是函数。此外，第一个和第二个是完全相同的实例。

### **嵌套装饰工**

你可以通过堆叠多个装饰器来使用它们。让我们举一个例子来理解这是如何工作的。

```
@function1
@function2
def function(name):
      print(f"{name}")

```

这就是我们如何通过将嵌套的装饰器相互堆叠来使用它们。在上面的例子中，这只是一个简单的描述，为了让它工作，你必须定义函数 1 和函数 2，并且在它们中包含包装函数。

### **装饰器中的参数**

在装饰器中传递参数总是有用的。让我们考虑下面的例子。

```
import functools
def repeat(num):
      def decorator_repeat(func):
            @functools.wraps(func)
            def wrapper(*args, **kwargs):
                  for _ in range(num):
                       value = func(*args, **kwargs)
                  return value
             return wrapper
       return decorator_repeat 

@repeat(num=4)
def function(name):
      print(f"{name}")

function("python")

```

```
Output:python
        python
        python
        python
```

这就把我们带到了本文的结尾，在这里我们学习了如何在 Python 中用例子来使用 Decorator。我希望你清楚这篇 Python 装饰教程中与你分享的所有内容

*如果您发现这篇文章与“Python 装饰教程”相关，请查看  [Edureka Python 认证培训，](https://www.edureka.co/data-science-python-certification-course)一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*我们在这里帮助你踏上旅程的每一步，并为想要成为  [Python 开发者](https://www.edureka.co/blog/how-to-become-a-python-developer/)的学生和专业人士设计课程。该课程旨在让您在 Python 编程方面有一个良好的开端，并训练您掌握核心和高级 Python 概念以及各种  [Python 框架](https://www.edureka.co/blog/python-frameworks/) ，如  [Django。](https://www.edureka.co/blog/django-tutorial/)*

如果你遇到任何问题，请在“Python 装饰教程”的评论区自由提问，我们的团队将很乐意回答。