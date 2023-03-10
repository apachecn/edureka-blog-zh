# Python 构造器:你需要知道的一切

> 原文：<https://www.edureka.co/blog/python-constructors/>

这篇文章将向你介绍一个有趣的话题，这个话题简单却是编程的核心，我指的是 [Python](https://www.edureka.co/blog/python-tutorial/) 构造函数。本文将涉及以下几点:

*   [Python 构造函数](#PythonConstructors)
*   [Python 中什么是构造函数？](#WhatisaConstructorinPython?)
*   [在 Python 中创建构造函数](#CreatingaConstructorinPython)
*   [参数化和非参数化构造函数的区别](#DifferencebetweenParameterizedandNonParameterizedConstructor)
*   [在 Python 中内置的类函数](#InBuiltClassFunctionsinPython)
*   [内置类属性](#InbuiltClassAttributes)

那么让我们开始吧，

## **Python 构造函数**

如果你从事编程已经有一段时间了，你可能会多次遇到 Python 这个名字。Python 作为一种编程语言遵循面向对象，这意味着在平台上创建的每个实例都被定义为一个对象。尽管 Python 中的大多数组件都有大量的在线信息，但一个被反复研究的主题是 Python 中的构造函数。因此，在本文中，我们将讨论 Python 中的所有构造函数，如何利用它们以及它们带来的好处。我们开始吧！

继续这篇关于 Python 构造函数的文章，

## **Python 中什么是构造函数？**

构造函数可以简单地定义为一种特殊类型的方法或函数，可以用来初始化类中各种成员的实例。

在 Python 中，有两种不同类型的构造函数。

*   非参数化构造函数:Python 中没有参数的构造函数称为非参数化构造函数。
*   参数化构造函数:具有预定义参数的构造函数称为参数化构造函数。

当我们在一个类中创建一个对象时，构造函数就被定义了。构造函数的存在也验证了有足够的资源存在，因此可以通过类的对象轻松执行启动任务。

继续这篇关于 Python 构造函数的文章，

## **在 Python 中创建构造函数**

现在，您已经熟悉了 Python 中构造函数的定义和类型，让我们来探索如何在 Python 中创建构造函数。

在 Python 中，如果你需要创建一个结构，你需要使用 __init__ 函数和 or 方法。在实例化一个类时，您需要调用这个方法。一旦定义并调用了 __init__ 函数，我们就可以根据您的需要在创建类对象时传递任意数量的参数。Python 中构造函数最常见的用途是初始化类的属性。

**注:**

在 Python 中创建的每个类都需要有一个构造函数才能运行，即使它是默认的构造函数。

为了更好地理解这个概念，请看下面的例子。

```
class Employee:
def __init__(self,name,id):
self.id = id;
self.name = name;
def display (self):
print("ID: %d nName: %s"%(self.id,self.name))
emp1 = Employee("John",101)
emp2 = Employee("David",102)
#accessing display() method to print employee 1 information
emp1.display();
#accessing display() method to print employee 2 information
emp2.display();
```

当您运行上面的程序时，输出将如下所示。

编号:101

姓名:约翰

编号:102

姓名:大卫

继续这篇关于 Python 构造函数的文章，

## **参数化和非参数化构造函数的区别**

正如在上面的定义中提到的，参数化的构造函数有一个预定义的值，而非参数化的构造函数没有被赋值。在编程时，用例根据上下文的不同而不同，为了更好地理解这一点，请看下面的例子。

```
class Student:
#Constructor - non parameterized
def __init__(self):
print("This is non parametrized constructor")
def show(self,name):
print("Hello",name)
student = Student()
student.show("John")
```

上面是一个非参数化构造函数的例子，它的输出如下。

这是非参数化的构造函数

你好约翰

```
class Student:
#Constructor - parameterized
def __init__(self, name):
print("This is parametrized constructor")
self.name = name
def show(self):
print("Hello",self.name)
student = Student("John")
student.show()
```

上面是一个参数化构造函数的例子，它的输出如下。

这是参数化的构造函数

你好约翰

继续这篇关于 Python 构造函数的文章，

## **在 Python 中内置的类函数**

现在 Python 中构造函数的基础已经很清楚了，让我们来探索 Python 中的各种内置类。

1.  getattr(obj，name，default):Python 中的这个内置函数用于访问类的属性。
2.  delattr(obj，name):如果你需要删除一个类中的特定属性，那么就使用这个内置函数。
3.  setattr(obj，name，value):在某种情况下，如果您决定为一个特定的属性设置一个特定的值，那么就使用 Python 中内置的这个函数。
4.  hasattr(obj，name):最后但同样重要的是，如果您需要查看某个特定对象是否包含属性，那么就使用这个函数。执行时，如果函数中存在属性，将返回 true。

要理解 Python 中内置类函数的概念，请看下面的代码。

```
class Student:
def __init__(self,name,id,age):
self.name = name;
self.id = id;
self.age = age
#creates the object of the class Student
s = Student("John",101,22)
#prints the attribute name of the object s
print(getattr(s,'name'))
# reset the value of attribute age to 23
setattr(s,"age",23)
# prints the modified value of age
print(getattr(s,'age'))
# prints true if the student contains the attribute with name id
print(hasattr(s,'id'))
# deletes the attribute age
delattr(s,'age')
# this will give an error since the attribute age has been deleted
print(s.age)
```

上面的输出将是。

约翰

Twenty-three

真实的

AttributeError:“学生”对象没有属性“年龄”

继续这篇关于 Python 构造函数的文章，

## **内置类属性**

除了内置的类函数，Python 还带有内置的类属性，这有时会派上用场。下面给出了一些最重要的内置类属性。

1.  __dict__:通过使用它，您可以查看包含关于类名称空间的信息的字典。
2.  __name__:如果需要查看当前类的名称，请使用此属性。
3.  __doc__:该属性包含一个字符串，该字符串包含当前类的文档。
4.  __module__:如果您需要访问定义该类的模块，请使用这个内置属性。
5.  __bases__:如果你需要查看包含所有基类的元组，那么使用这个函数。

下面给出了一个阐明所有内置类属性的例子。

```
class Student:
def __init__(self,name,id,age):
self.name = name;
self.id = id;
self.age = age
def display_details(self):
print("Name:%s, ID:%d, age:%d"%(self.name,self.id))
s = Student("John",101,22)
print(s.__doc__)
print(s.__dict__)
print(s.__module__)
```

这就把我们带到了这篇关于 Python 构造函数的文章的结尾。

*要深入了解 Python 及其各种应用，您可以 [**在此**](https://www.edureka.co/python/) 注册参加在线直播培训，全天候支持，终身访问。*

*有问题吗？在“Python 教程”的评论部分提到它们，我们会回复你。*