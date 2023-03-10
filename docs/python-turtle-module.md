# 使用 Python 的 Turtle 模块构建游戏简介

> 原文：<https://www.edureka.co/blog/python-turtle-module/>

小时候，我相信每个人都玩过著名的贪吃蛇游戏。事实上，这是最早上市的手机游戏之一。自己建岂不是很酷？太好了。在本文中，我将使用 Python 的 Turtle 模块从头开始构建它。

议程:

*   [Python 的海龟模块是什么？](#WhatIsPython'sTurtleModule?)
*   [开始构建游戏](#StartBuildingTheGame)
    *   [设置屏幕](#SetUpTheScreen)
    *   [创建蛇头](#CreateSnake'sHead)
    *   [移动蛇的功能](#FunctionsToMoveTheSnake)
    *   [加点食物](#AddSomeFood)
    *   [打造蛇的身体](#BuildSnake'sBody)
    *   [添加边界碰撞](#AddBorderCollisions)
    *   [添加身体碰撞](#AddBodyCollisions)
    *   [添加分数](#AddScores)

**Python 的海龟模块是什么？**

我相信每个人小时候都用过画板。现在，想象一下，你可以命令系统为你画图，而不是手动在板上画图。那不是很酷吗？Python 的 turtle 模块可以让你做到这一点。它基本上让你创建一个画板，命令一只乌龟为你画画。

为了更好地理解这篇博客，请看下面的 python 编程博客:

*   [Python 教程——学习 Python 编程的完整指南](https://www.edureka.co/blog/python-tutorial/)
*   [用 Python 编程教程](https://www.edureka.co/blog/programming-with-python-tutorial/)
*   [Python 编程语言——Python 基础入门](https://www.edureka.co/blog/python-programming-language/)

让我们继续前进，开始构建游戏。在本文中，我使用了 Python 版的 PyCharm。

**开始建造游戏**

在开始构建之前，让我们先了解一下这个游戏。这个游戏有两个元素——蛇和食物。玩家必须移动蛇，让它接触(吃掉)食物，然后变大。如果蛇接触到自己的身体或窗户的边界，它就会死亡。显而易见，玩家需要获胜，从而避免死亡。

**设置屏幕**

要开始使用该模块，您需要像 python 中的任何其他模块一样导入它。

`import turtle`

**龟的功能。Screen()** 用来创建一个窗口。在这种情况下，我们的窗口是*为游戏赢得*。用函数 **window.title("卡尔基的蛇游戏")**给这个窗口起个名字。使用函数 **window.bgcolor("Color")** 设置窗口的背景颜色。使用功能 **window.setup(width=X，height=Y)** 设置窗口高度和宽度。函数 **window.tracer()** 关闭屏幕更新。除了记分牌，我们不需要任何屏幕更新，因此设置为 0。

```
#set up the screen
win = turtle.Screen()
win.title("Kalgi's snake game")
win.bgcolor("blue")
win.setup(width=600,height=600)
win.tracer(0)
```

**![win - Python Turtle Module - Edureka](img/d431849ee80d44ea83f64fabb6e5a283.png)**

**创造蛇头**

一旦你创建了窗口，我们需要的下一件事是一个蛇头。Snake 基本上就是一只四处活动的乌龟(用 python 语言来说)。用函数 **turtle 创建一只乌龟。龟()**并给它取名为*头。*我们将机头速度设置为 0，因为我们只是在这一部分进行初始化，机头不需要移动。为此，我们使用了函数 **turtle_name.speed()** 。接下来，我们需要初始化头部的形状和颜色。我们使用函数 **turtle_name.shape()** 和 **turtle_name.color()** 。

我们需要画出蛇走过的路吗？不要！函数 **turtle_name.penup()** 确保不画出蛇走过的路线。我希望我的蛇头的位置是窗口的中心，方向是“停止”。我们为它使用了函数 **turtle_name.goto()** 和 **turtle_name.direction()** 。

```
#Snake Head
head = turtle.Turtle()
head.speed(0)
head.shape("square")
head.color("black")
head.penup()
head.goto(0, 100)
head.direction = "stop"
```

一旦头部被创建，我需要一个主游戏循环，它总是被设置为真。我将使用函数 **window.update()** 更新我的窗口。这个函数基本上是随着循环不断更新我的屏幕。

```
# Main game loop
while True:
    win.update()
```

**![snakehead - Python Turtle Module - Edureka](img/e174b3e6593b9e840ecda36156661334.png)**

**移动蛇的功能**

现在我们已经创建了一条蛇，让它动起来。我们定义了一个叫做 **move()的函数。**如果机头*上升*，‘y’坐标增加，如果机头*下降*，‘y’坐标减少，如果机头*向右*，‘x’坐标增加，如果机头*向左*，‘x’坐标减少。

```
def move():
    if head.direction == "up":
        y = head.ycor() #y coordinate of the turtle
        head.sety(y + 20)

    if head.direction == "down":
        y = head.ycor() #y coordinate of the turtle
        head.sety(y - 20)

    if head.direction == "right":
        x = head.xcor() #y coordinate of the turtle
        head.setx(x + 20)

    if head.direction == "left":
        x = head.xcor() #y coordinate of the turtle
        head.setx(x - 20)
```

这个函数在被调用之前什么都不做。所以我们需要在每次更新屏幕或窗口时调用这个函数。按如下方式更新主游戏循环:

```
#Main Game Loop
while: True
    win.update()
    move()
```

您可以尝试执行到目前为止的代码，您会注意到蛇移动的速度非常快。这是 move 函数的默认行为。为了放慢速度，我们需要使用时间模块。转到代码的导入部分，导入时间模块。我们将名为*的变量延迟*初始化为 0.1。然后调用函数 **time.sleep(delay)** 来降低龟速。

```
import turtle
import time
delay=0.1
# Main game loop
while True:
    wn.update()
    move()
    time.sleep(delay)
```

我们做了让乌龟上下左右移动的函数。但是计算机怎么知道什么是上、下、左、右呢？我们需要为这些方向中的每一个定义一个函数，并将**头方向**设置为*向上、* *向下*、*向右*和*向左。*

注意:蛇不能从左往右，从左往右，从下往上，从上往下。

```
def go_up():
    if head.direction != "down":
        head.direction = "up"

def go_down():
    if head.direction != "up":
        head.direction = "down"

def go_right():
    if head.direction != "left":
        head.direction = "right"

def go_left():
    if head.direction != "right":
        head.direction = "left"
```

我们需要系统来监听我们的控制键。我们添加了一个名为 **win.listen()** 的函数来监听按键。每一次按键都需要绑定到一个执行动作的函数。我们使用函数 **win.onkeypress(function，" key")** 来进行同样的操作。

```
# keyboard bindings
win.listen()
win.onkey(go_up, "w")
win.onkey(go_down, "s")
win.onkey(go_right, "d")
win.onkey(go_left, "a")
```

![snakemove - Python Turtle Module](img/26be2aeede908bac2223556eba0fc2dc.png)

**加点食物**

食物也是一只静止不动的乌龟，直到它被触摸(吃掉)。一旦蛇吃了食物，它会占据另一个随机位置，游戏继续。让我们继续以类似的方式创建一只乌龟作为食物。我们将使用与创建蛇头相同的函数。

```
# Snake food
food = turtle.Turtle()
food.speed(0)
food.shape("circle")
food.color("red")
food.penup()
food.shapesize(0.50, 0.50)
food.goto(0, 0)
```

![food - Python Turtle Module - Edureka](img/50e2e45c8b380f71e3f671370910a4bc.png)

现在我们已经创建了蛇头和食物，并赋予了移动的功能，蛇应该在接触食物时吃掉食物，而食物需要占据一个新的位置。我将使用函数 **head.distance(food)** 来计算两个对象之间的距离。如果距离小于 15(食物和头部接触)，食物被重新放置到窗口内的任意位置。让我们继续在主游戏循环中添加这个特性。

```
if head.distance(food) <15:
# move the food to a random position on screen
x = random.randint(-290, 290)
y = random.randint(-290, 290)
food.goto(x, y)
```

**打造蛇的身体**

现在我们需要一种功能，它能在蛇每次接触食物时增加蛇的身体。为此，我们使用数组。我们创建一个名为 segments 的数组，它被初始化为空。

```
segments = []
```

我们需要在蛇每次接触食物的时候给它的身体添加一段。我们已经有了检查头部与食物碰撞的条件。创建一个新的海龟，命名为 *new_segment，*定义它的速度、形状和颜色，并将其添加到 segments 数组中。

```
# add a segment
        new_segment = turtle.Turtle()
        new_segment.speed(0)
        new_segment.shape("square")
        new_segment.color("grey")
        new_segment.penup()
        segments.append(new_segment)

```

把段加到蛇头身上还不够。当蛇头移动时，这些部分也需要移动。我使用的逻辑是将位置 x 的最后一段移动到 x-1 和 x-1 到 x-2，依此类推。

```
# move the end segment in reverse order
    for index in range(len(segments)-1, 0, -1):
        x = segments[index-1].xcor()
        y = segments[index-1].ycor()
        segments[index].goto(x, y)

```

但是头部正上方的部分是一个特例。那通向哪里？它在头部的位置。

```
# Move segment 0 to where the head is
    if len(segments) &amp;gt; 0:
        x = head.xcor()
        y = head.ycor()
        segments[0].goto(x, y)

```

**![point - Python Turtle Module - Edureka](img/c025403c07419f128bf96d53b08aa73f.png)**

**添加边界碰撞**

我们需要确保蛇在与边界相撞时死亡。我们已经有了边界的坐标，我们只需要在蛇头触及这些坐标时重置它的位置。此外，蛇需要停止移动，因此改变方向停止。

```
# Check for collision
    if head.xcor() > 290 or head.xcor() < -290 or head.ycor() > 290 or head.ycor() < -290:
        time.sleep(1)
        head.goto(0, 0)
        head.direction = "stop"

```

此外，当蛇死亡时，这些部分需要消失。为此，我们需要做的就是，将线段的位置设置在窗口坐标之外。现在，当游戏重新开始时，我们需要新的片段，因此清除片段列表。

```
# Hide the segments
        for segment in segments:
           segment.goto(1000, 1000)

        # clear segment list
        segments = []

```

**![wallcollide - Python Turtle Module - Edureka](img/b20a40621e29532c8fc6ec641acd3290.png)**

**添加身体碰撞**

蛇碰到自己就需要死。所以我们要遍历整个段列表，检查段和头之间的距离是否小于 20。如果是，重置磁头位置和磁头方向。

```
# Check for head collision
    for segment in segments:
        if segment.distance(head) < 20:
            time.sleep(1)
            head.goto(0, 0)
            head.direction = "stop"

# Hide the segments
            for segment in segments:
                segment.goto(1000, 1000)

# clear segment list
            segment.clear()

```

**![selfcollide - Python Turtle Module - Edureka](img/0b907714bee60fc011d065b27e43e075.png)**

**添加分数**

Turtle module 有一个惊人的功能，可以让你在屏幕上写字。我将从创建一只乌龟开始，把它当作钢笔使用。

```
pen = turtle.Turtle()
pen.speed(0)
pen.shape("square")
pen.color("white")
pen.penup()
pen.hideturtle()
pen.goto(0, 260)
pen.write("Score: 0 High Score: {}".format(high_score), align="center", font=("Courier", 24, "normal"))

```

让我们将名为*的变量 score* 初始化为 0，并将 *high_score* 也初始化为 0。

```
# score
score = 0
high_score = 0

```

我们需要分析分数增加时的情况。第一个是当头部与食物碰撞时。增加*分数*并更新*高分*。我们使用 **pen.write()** 在屏幕上写下分数。

```
# Increase the score
        score = score+10

        if score > high_score:
            high_score = score

```

当蛇头与边界和自己的线段发生碰撞时，我们需要重置分数。在这两个地方添加以下行

```
# reset score
            score = 0

    # update score
            pen.clear()
            pen.write("score: {} High Score: {}".format(score, high_score), align="center", font=("Courier", 24, "normal"))

```

还有 Tadaaaaa！！你的游戏准备好了。Python 是一种广泛使用的编程语言，有 820 万开发人员在使用它。你会惊讶地发现它能创造什么奇迹。另一个让你开发游戏的很酷的模块是 [Pygame](https://www.edureka.co/blog/pygame-tutorial/) 。

我希望这个 Python 的 turtle 模块已经帮助你了解了如何用它来构建游戏。请用它来制作更多这样的游戏，并在下面的评论区告诉我。我很想玩。

*要深入了解 Python 及其各种应用，您现在就可以报名参加 [Python 课程](https://www.edureka.co/python-programming-certification-training)培训，该课程提供全天候支持和终身访问。*