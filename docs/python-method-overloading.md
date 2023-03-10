# 什么是 Python 中的方法重载，它是如何工作的？

> 原文：<https://www.edureka.co/blog/python-method-overloading/>

Python 中的两个方法不能同名。Python 中的方法重载是一个允许同一个操作符有不同含义的特性。在这篇文章中，我们将看看 Python 中的方法重载特性，以及它是如何用于重载方法的，顺序如下:

*   [什么是超载？](#overloading)
*   [Python 中的方法重载](#methodoverloading)
*   [方法重载示例](#example)

## **什么是超载？**

[重载](https://www.edureka.co/blog/method-overloading-and-overriding-in-java/)是函数或操作符基于传递给[函数](https://www.edureka.co/blog/python-functions)的参数或操作符操作的操作数以不同方式表现的能力。

使用霸王的一些优势有:

*   重载一个方法可以提高可重用性。例如，我们可以编写一个方法并重载它，而不是编写多个只有细微差别的方法。

*   重载还提高了代码的清晰度，消除了复杂性。

重载是一个非常有用的概念。然而，它也有许多与之相关的缺点。

*   当跨[继承](https://www.edureka.co/blog/inheritance-in-python/)边界使用时，重载会造成混乱。如果过度使用，管理过载的函数会变得很麻烦。

## **Python 中的方法重载**

在 Python 中，您可以创建一个可以以不同方式调用的方法。所以，你可以有一个方法有零个，一个或多个参数。根据方法定义，我们可以用零个、一个或多个参数来调用它。

给定一个方法或函数，参数的数量可以由你指定。这个以不同方式调用同一个方法的过程叫做方法重载。

## **方法重载示例**

现在你已经知道 Python 中什么是方法重载，让我们举个例子。在这里，我们用一个[方法](https://www.edureka.co/blog/python-main-function/) **Hello()** 创建一个类。此方法的第一个参数设置为 None。这将为我们提供带或不带参数调用它的选项。

一个对象也是基于类创建的，我们将使用 0 和 1 个参数调用它的方法。

### **例 1:**

```

#!/usr/bin/env python
class Person:
def Hello(self, name=None):
if name is not None:
print('Hello ' + name)
else:
print('Hello ')
# Create instance
obj = Person()
# Call the method
obj.Hello()
# Call the method with a parameter
obj.Hello('Edureka')

```

**输出:**

```
Hello
Hello Edureka
```

为了澄清方法重载，我们现在可以用两种方式调用方法 Hello():

```
obj.Hello()
obj.Hello('Edureka')
```

在上面的例子中，我们已经创建了一个方法，调用它的参数比定义的要少。此外，它不局限于两个[变量](https://www.edureka.co/blog/variables-and-data-types-in-python/)，你的方法可以有更多的可选变量。

现在让我们以另一个**例子**来理解 [python](https://www.edureka.co/blog/python-programming-language/) 中的方法重载。

### **例 2:**

在下面的例子中，我们将重载 area 方法。如果没有参数，则返回 0。如果我们有一个参数，那么它返回这个值的平方，并假设你在计算一个平方的面积。此外，如果我们有两个参数，那么它返回两个值的乘积，并假设您正在计算一个矩形的面积。

```

# class
class Compute:
# area method
def area(self, x = None, y = None):
if x != None and y != None:
return x * y
elif x != None:
return x * x
else:
return 0
# object
obj = Compute()
# zero argument
print("Area Value:", obj.area())
# one argument
print("Area Value:", obj.area(4))
# two argument
print("Area Value:", obj.area(3, 5))

```

上面的代码将给出下面的**输出:**

```
Area Value: 0
Area Value: 16
Area Value: 15
```

说到这里，我们的文章就到此为止了。我希望你理解什么是 python 中的方法重载，以及它是如何工作的。

*要深入了解 python 及其各种应用，您可以注册 Edureka 提供的实时 [**Python 在线课程**](https://www.edureka.co/python-programming-certification-training) ，该课程提供全天候支持和终身访问。*

*有问题吗？请在“Python 中的方法重载”博客的评论部分提到它，我们会尽快回复您。*