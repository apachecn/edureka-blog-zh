# 如何用 Python 实现 Decorators？

> 原文：<https://www.edureka.co/blog/decorators-in-python/>

Python 中的 [**装修工**](https://www.edureka.co/data-science-python-certification-course)是 Python 中的有力工具。它允许程序员修改函数或类的行为。 **装饰者** 允许包装另一个函数来扩展被包装函数的行为，而无需修改它。本文将简要介绍以下主题。

*   [Python 中的装饰者](#DecoratorsinPython)
    *   [函数可以作为参数传递](#Functioncanbepassedasanargument)
    *   [函数可以在函数](#Functionscanbedefinedwithinfunctions%20)中定义
    *   [函数也可以返回函数](#Functionscanreturnfunctionsaswell)
    *   [功能可以分配给一个变量](#Functioncanbeassignedtoavariable)
*   [我们在 Python 中的第一批装饰者](#OurFirstDecorator)

让我们开始吧！

## **Python 中的装饰者**

今天，我们将讨论 python 中不可或缺的部分，即装饰者。记叙文可以被认为是一个非常有用和强大的工具，但前提是使用得当。简而言之:它们是修改其他功能的功能的功能。它们有助于使我们的代码更短，更有 Pythonic 风格。

**定义:** 装饰器是 Python 中的**设计模式**，允许用户在不修改现有对象结构的情况下向其添加新功能。装饰器通常在你想要装饰的函数定义之前被调用。

![Python Logo- decorators- in-python](img/4c6f99f56333f713cda7948445645f94.png)

**警告:**它们乍一看是如此令人迷惑，所以，勒紧你的腰带，因为我们要进行一次深潜！

在直入主题之前，我们将看看在理解装饰者之前你应该知道的一些事情。Python 中的函数是**一等公民。**这意味着它们支持像作为参数传递、从函数返回、修改和赋给变量这样的操作。

现在，让我们看看可以作为参数传递的函数

## **函数可以作为参数传递**

你必须知道这一点，如果你不知道，那么首先访问下面的 [**链接**](https://www.edureka.co/blog/python-functions) ，然后再回来。

现在，由于函数是对象，并且函数接受对象作为参数，我们可以得出结论，我们可以将函数传递给函数。让我们用一些代码来更好地理解它。

由于函数的每个参数都是对对象的引用，函数也是对象，我们可以将**函数**——或者更好的“**对函数**的引用”——作为参数传递给函数。

```
def greet(name):
      return &ldquo;Hey {}&rdquo;.format(name)
def i_will_greet(greet,name=&rdquo;Avikar):
      print(greet(name))
      print(&ldquo;Welcome to the world of edureka&rdquo;)
i_will_greet(greet)

```

我们可以清楚地看到，函数 greet()已经作为参数传递给了函数 i_will_greet()。

**//输出:**

`Hey Pallavi`

**注意**:函数 greet 已经传递给了 **i_will_greet** 没有括号。因为如果你使用括号，那么它传递的不是函数，而是它的定义。

让我们再考虑一个例子来使我们的**基础具体化。**

```
from math import sin,cos
def calculate(func):
       res=0
       for i in [1,2,3,4,5]:
              res+=func(i)
       return res
print(&ldquo;the value of sin is {}&rdquo;.format(calculate(sin)))
print(&ldquo;the value of cos is {}&rdquo;.format(calculate(cos)))

```

**//输出:** `The value of sin is 0.1761616497223787` `the value of cos is -1.2358184626798336`

让我们看看可以在函数中定义的第二个函数

## **函数可以在函数**中定义

对于 C 或 C++程序员来说，在函数中拥有或定义函数的概念是全新的。我们已经知道了**嵌套**，令人惊讶的是我们也可以嵌套我们的函数，也就是说，我们可以在一个函数中定义任意多的函数。

```
def tell_me():
      def question():
            print("is python boring")
     def answer():
            print("Definintely not. Silly!")
     question()
     answer()
     return "look now you know what to learn"

```

**//输出:** `is python boring?` `Definitely not. Silly!` `look now you know what to learn`

很容易理解，当调用 tell_me()时

*   首先，函数问题和答案被定义但没有被调用。
*   后面的函数在函数本身内部被调用，一个字符串在最后被返回给 **print()。**

为了更好地理解，让我们再考虑一个例子，在这个例子中，我们需要将温度从**摄氏度**转换为**华氏度。**

```
def temperature(t):
      def celsius2fahrenheit(x):
             return 9 * x / 5 + 32
      return (&ldquo;It&rsquo;s &rdquo;+str(celsius2fahrenheit(t)+&rdquo; degrees! &rdquo;
print(temperature(35))

```

**//输出:** `95.0 degrees`

让我们来看看第三个也可以返回函数的函数。

## **函数也可以返回函数**

没有必要在另一个函数中执行一个函数，我们也可以将它作为输出返回。

```
def bake_cake(flavor="chocolate"):
      print("place the base of cake and decorate it with {} and fruits".format(flavor))
      def cherry():
            return "place cherry at the top of your {} cake".format(flavor)
      return cherry
tasty = bake_cake("butterscotch")
print(tasty())

```

**输出:** `place the base of the cake and decorate it with butterscotch and fruits` `place cherry at the top of your butterscotch cake`

让我们考虑一个有用的例子，我们假设可以传递任意数量的参数(*args)。为了更好地理解，请访问 Edureka 社区。

我们可以推广我们的工厂函数，使其适用于任意次的多项式

![Image- Decorators in Python- Edureka](img/d8d2eb3f5d63fcf29de26dd86e2d2fdd.png)

```
def polynomial_creator(*coeff):
      def polynomial(x):
             for index,c in enumerate(coeff[::-1]):
                     res+=c*x**index
             return res
      return polynomial

```

当与二次方程的系数一起传递时，

*   定义多项式()函数。
*   返回多项式函数。

现在，如果我们可以将这个返回的函数赋给一个变量(如前所述)，我们就可以直接使用我们的**包装函数。**

```
p1 = polynomial_creator(2, 3,-1)
p2 = polynomial_creator(1, 8, -1, 3, 2)
for x in range(-2, 2, 1):
       print(x, p1(x), p2(x))

```

注意当 p1(x)被称为 coeff 时。是 2，3 和-1，表示多项式()是在 polynomial_creator()被赋值给 p1 或 p2，但未被调用时定义的。

所以当我们调用 **p1()** 或 **p2()，**时，我们会将参数传递给**多项式(x)。**

正如我们从输出中看到的，

*   首先，polynomial_creator 已经为 **p1** 和 p2 调用了两次。
*   后来，对于每个 print 语句，多项式()被分别调用。

**//输出:**`-2   1  -56``-1  -2   -9`` 0  -1    2`` 1   4   13`

现在让我们看看最后一个可以赋给变量的函数

## **该功能可以分配给一个变量**

你注意到上面代码中的**tasty = bake _ cake(" butterscotch ")**了吗？是的，没错！我们也可以将函数分配给变量，即我们创建函数的别名。上述赋值的用处是:

即使您删除了该函数，您仍然可以通过您创建的变量来使用它。试试 **del bake_cake**

有了这些知识，我们就可以开始潜水了。但是，如果我们没有潜水面罩(非常小但很重要的部分)，这种驱动力不会持续很久。关闭(我们的潜水面罩)

Python 允许嵌套函数访问封闭函数的外部范围。这是装饰者的一个重要概念。

例如，让我们考虑一个外部和内部函数及其变量。

```
def outer():
     var =10
     def inner():
           varb=30
           print(&ldquo;value of var inside inner {}&rdquo;.format(var))
           print(&ldquo;value of varb inside inner is {}&rdquo;.format(varb))
     inner()
     print(&ldquo;value of var outside inner {}&rdquo;.format(var))
     print(&ldquo;value of var_b outside inner is {}&rdquo;.format(varb))

```

**//输出:**`value of var inside inner 10``value of var_b inside inner is 30``value of var outside inner 10``Traceback (most recent call last):``File “<pyshell#5>”, line 1, in <module>``outer()`

继续我们的第一个装饰师

## **我们的第一个装潢师**

要创建装饰器:

*   我们有一个需要装饰的函数或类。
*   一个**装饰器**功能。
*   一个将被返回的**包装器**函数。

为了正确理解它，让我们首先考虑一个例子:

```
def outer(func):
     print(&ldquo;inside outer&rdquo;)
     def inner()
            print("inside inner function&rdquo;)
            func()
            print(&ldquo;inside inner again&rdquo;)
     return inner

```

我们在这里定义了 **inner() inside outer()。**函数 **func** 将作为参数传递给该函数。

现在，

```
def need_decoration():
       print("inside function call")
need_decoration=outer(need_decoration)
inside outer
need_decoration()
inside inner function
inside function call
inside inner again

```

很好理解。对！

这里我们调用了函数 **need_decoration()** 作为参数的 **outer()** 。因此，当 outer 被调用时，第一个 print 语句被执行，函数 **inner()** 被定义为 need_decoration，函数 **func** 被返回。

这个返回的函数存储在 **need_decoration 中。**

现在，当需要装饰时，通过圆括号调用内部函数。

你需要明白两件重要的事情:

1.函数调用和函数定义的区别。

```
import math
temp=math.sin #temp is assigned the function definition
temp(4)
-0.7568024953079282
temp=math.sin(4) #temp is assigned the value returned by function
print(temp)
-0.7568024953079282

```

2.有人可能会认为，由于 need_decoration 已经失去了原来的定义，被赋给了 **inner()，**当从 i **n** ner()调用 **need_decoration** 时会发生什么？

如果你认为它可能会陷入一个死循环，其中 **inner()** 调用 **func()** 作为 **need_decoration()** ，而 need_decoration 又相当于调用 inner()，那么相信我，你不是唯一一个处于这种困境的人。

这就是为什么装饰者变得有点笨拙和难以理解。

所以，这根本不会发生。当你通过调用 outer 定义 inner 为**need _ decoration = outer(need _ decoration)inner()**自动将 **need_decoration** 的定义存储在那里。我们稍后将对此进行更深入的研究。

你一定在想“ **@** ”在哪里，装修工的荣耀。你会很高兴你已经使用了它，但是是以一种隐藏的方式。**need_decoration = outer(need _ decoration)**以上 need _ decoration 的定义可以替换为 **@outer** 。所以在重写了上面的代码之后

```

@outer
def need_decoration():
      print("inside function call")
inside outer
need_decoration()
inside inner function
inside function call
inside inner again

```

我们可以用 decorator 做很多事情，比如多个 decorator 可以应用到一个函数中。但是我们将在下一篇文章中研究这个问题。

这就把我们带到了本文的结尾，我们已经通过几个例子了解了如何在 *python* 中使用 ***装饰器。我希望你清楚本教程中与你分享的所有内容。***

*如果您发现这篇文章与“**Python 装饰者**”相关，请查看  [Edureka Python 认证培训，](https://edureka.co/python)一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*我们在这里帮助你踏上旅程的每一步，并为想要成为  [Python 开发者](https://www.edureka.co/blog/how-to-become-a-python-developer/)的学生和专业人士设计课程。该课程旨在让您在 Python 编程方面有一个良好的开端，并训练您掌握核心和高级 Python 概念以及各种  [Python 框架](https://www.edureka.co/blog/python-frameworks/) ，如  [Django。](https://www.edureka.co/blog/django-tutorial/)*

*如果您遇到任何问题，请随时在 Python 的“ **Decorators”的评论区提出您的所有问题，我们的团队将很乐意回答。***