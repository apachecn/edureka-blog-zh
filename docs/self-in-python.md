# Python 中的 self 有什么用？

> 原文：<https://www.edureka.co/blog/self-in-python/>

如果你在用 [Python](https://www.edureka.co/blog/python-tutorial/) 工作，那就逃不过“自我”这个词。它用于方法定义和变量初始化。每当我们定义一个方法时，self 方法就会被明确地使用。在本文中，我们将按照以下顺序深入探讨 Python 中的自我:

*   [在 Python 中 self 有什么用？](#what)
*   [Python 类自身构造函数](#self)
*   [Python 中的 self 是关键字吗？](#keyword)

## **在 Python 中 Self 有什么用？**

## **![Python - self in python - edureka](img/1f832a49255567a01424e2bf3684583c.png)**

self 用来表示类的[实例](https://www.edureka.co/blog/isinstance-in-python/)。使用这个关键字，您可以访问 python 中[类的属性和方法。它将属性与给定的参数绑定在一起。我们使用 self 的原因是 Python 不使用' @ '语法来引用实例属性。加入我们的](https://www.edureka.co/blog/python-class/)[Python 编程大师](https://www.edureka.co/masters-program/python-developer-training)课程，了解更多。在 Python 中，我们有一些方法可以自动传递实例，但不能自动接收。

**举例:**

```
class food():

# init method or constructor
def __init__(self, fruit, color):
self.fruit = fruit
self.color = color

def show(self):
print("fruit is", self.fruit)
print("color is", self.color )

apple = food("apple", "red")
grapes = food("grapes", "green")

apple.show()
grapes.show()
```

**输出:**

```
Fruit is apple
color is red
Fruit is grapes
color is green
```

## **Python 类自构造函数**

self 也用于引用类中的[变量](https://www.edureka.co/blog/variables-and-data-types-in-python/)字段。让我们举个例子，看看它是如何工作的:

```
class Person:

# name made in constructor
def __init__(self, John):
self.name = John

def get_person_name(self):
return self.name
```

在上面的例子中，self 指的是整个 Person 类的名称变量。在这里，如果我们在一个方法中有一个变量，self 将不起作用。该变量只在该方法运行时存在，因此是该方法的局部变量。为了定义整个类的全局字段或变量，我们需要在类方法之外定义它们。

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

## **自我是关键词吗？**

self 用于不同的地方，通常被认为是一个关键字。但与在 [C++](https://www.edureka.co/blog/object-oriented-programming-in-cpp/) 中不同，self 在 Python 中并不是一个关键字。

self 是函数中的一个参数，用户可以使用不同的参数名来代替它。虽然建议使用 self，因为它增加了代码的可读性。

**举例:**

```
class this_is_class:
def show(in_place_of_self):
print("It is not a keyword "
"and you can use a different keyword")

object = this_is_class()
object.show()
```

**输出:**

```
It is not a keyword and you can use a different keyword
```

说到这里，我们的文章就到此为止了。我希望您理解了 self 的用法以及它在 Python 中是如何工作的。

*查看 Edureka 的 [Python 认证课程](https://www.edureka.co/python-programming-certification-training)* *。这个* *培训课程是为想成为 Python 程序员的学生和专业人士设计的。该课程旨在让你在 [Python 编程](https://www.edureka.co/blog/python-programming-language)方面有一个良好的开端，并训练你掌握核心和高级概念。*

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你，或者今天就参加我们在钦奈的 [Python 培训..](https://www.edureka.co/python-programming-certification-training-chennai)