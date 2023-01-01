# Python 中的 Init:您需要知道的一切

> 原文：<https://www.edureka.co/blog/init-in-python/>

Python 是当今业界最流行的编码平台之一。从业余爱好者到专业人士，每个人都使用 Python 来编写和制作移动和 web 应用程序。作为一个如此多功能的平台，有些方面并不为用户所熟知。其中最重要的是 Python 中的 Init。本文将帮助您探索这一概念，并详细遵循以下要点，

*   [Python 中的 Init](#InitinPython)
*   [初始化函数介绍](#IntroductionToInitFunction)
*   [Python 中 Init 的使用](#UseofInitinPython)

那么让我们开始吧，

## **Python 中的 Init**

## **初始化函数介绍**

如果你使用 Python 已经有一段时间了，你会很清楚 Python 是一种面向对象的编程语言。这基本上意味着您在 Python 环境中创建的所有东西都被称为对象。现在，在我们开始探索 Python 中的 __init__ 函数之前，让我们先了解一下基础知识。

**类**

Python 中的类是由不同元素组成的类别或集合，这些元素彼此之间有一个或多个相似之处，但通过类型、质量和种类与其他类不同。在技术术语中，我们可以将 Python 中的类定义为具有相同或精确行为的单个对象的蓝图。

**物体**

Python 中的对象是类的一个实例，它可以被编程来执行类中定义的功能。

**自我**

Python 中的 self in 关键字用于一个类中的所有实例。通过使用 self 关键字，可以很容易地访问一个类中定义的所有实例，包括它的方法和属性。

**初始化**

__init__ 是 Python 中的保留方法之一。在面向对象编程中，它被称为构造函数。从类创建对象时，可以调用 __init__ 方法，并且需要访问权限来初始化类的属性。

继续这篇关于 Python 中的 Init 的文章，

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

## **Python 中 init 的使用**

从上面分享的 __init__ 的定义中，您现在对这个方法到底做什么有了一些概念。为了进一步明确这个概念，我们来看一个例子。

**#1 示例**

目标:用 Python 编写一个名为“NFS”的赛车游戏

**解决方案:**如果你想用 Python 创建一个名为“NFS”的赛车游戏，你需要创建的基本对象之一就是一辆辆赛车。你在游戏中创造的每辆车都有不同的属性，例如颜色、速度等。以及换挡、加速、刹车等方法。

当您将这个概念编码到 Python 解释器中时，它应该是这样的。

```
class Car(object):
"""
blueprint for car
"""
def __init__(self, model, color, company, speed_limit):
self.color = color
self.company = company
self.speed_limit = speed_limit
self.model = model
def start(self):
print("started")
def stop(self):
print("stopped")
def accelarate(self):
print("accelarating...")
"accelarator functionality here"
def change_gear(self, gear_type):
print("gear changed")
" gear related functionality here"
Now that we have created the objects, let’s move on to create the individual cars in the game.
maruthi_suzuki = Car("ertiga", "black", "suzuki", 60)
audi = Car("A6", "red", "audi", 80)
```

在上面的例子中，我们创建了两种不同的汽车模型；一辆是铃木 Ertiga，另一辆是奥迪 A6。一旦成功创建了这些对象，我们就可以利用 __init__ 方法进行初始化，从而为接下来的步骤做准备。

在这个例子中，我们还可以利用 self 方法来表示类的不同实例，并使用给定的参数绑定属性。使用 self 方法将允许我们基本上访问我们在类中创建的属性和方法。

继续这篇关于 Python 中的 Init 的文章，

**#2 示例**

**目的:**找出一个具有尺寸、宽度(b=120)、长度(l=160)的矩形区域的开发成本。1 平方米的成本是 2000 印度卢比。

**解决方案:**记住前面示例中共享的步骤，这个特定示例的代码如下所示。

```
class Rectangle:
def __init__(self, length, breadth, unit_cost=0):
self.length = length
self.breadth = breadth
self.unit_cost = unit_cost
def get_perimeter(self):
return 2 * (self.length + self.breadth)
def get_area(self):
return self.length * self.breadth
def calculate_cost(self):
area = self.get_area()
return area * self.unit_cost
# breadth = 120 cm, length = 160 cm, 1 cm^2 = Rs 2000
r = Rectangle(160, 120, 2000)
print("Area of Rectangle: %s cm^2" % (r.get_area()))
print("Cost of rectangular field: Rs. %s " %(r.calculate_cost()))
```

正如在前面的例子中所讨论的，self 方法代表了类的实例和属性。如果你仔细观察，你会发现我们使用了 self.length 方法来导出属性 length 的值。属性 length 已经在类中绑定，我们使用 self 方法在同一个类中表示对象。

我们还使用了方法 def get_area(self):作为上面代码中的参数。每次我们调用这个方法时，它都会自动传递第一个参数和方法中的其他参数。虽然这种自动化乍看起来很小，但从长远来看，它将节省大量时间并提高效率。

为了进一步阐明这个讨论，请看下面的例子。

r =矩形(160，120，2000)

注意:“r”是类外对象的表示，“self”是类内对象的表示。

这就把我们带到了这篇关于 Python 中的 Init 的文章的结尾。

*要深入了解 Python 及其各种应用，您可以立即注册参加在线直播的 [Python 培训](https://www.edureka.co/python-programming-certification-training)，该培训提供全天候支持和终身访问。* *有问题吗？在“Python 教程”的评论部分提到它们，我们会回复你或者加入我们的 Python 课程的[大师。](https://www.edureka.co/masters-program/python-developer-training)*

如果你想在这个令人兴奋的领域拓展你的业务，试试我们的[人工智能课程](https://www.edureka.co/executive-programs/machine-learning-and-ai)。它是与瓦朗加尔的国家技术学院 E & ICT 学院合作提供的。这个执行硕士课程为学生提供了推进职业发展所需的工具、技术和工具的信息。