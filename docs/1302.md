# 如何在 Python 中求平方根？

> 原文：<https://www.edureka.co/blog/square-root-in-python/>

我们都遇到过数学中的平方根。不可否认，它是最重要的基础之一，因此需要嵌入到各种应用中。Python 通过使在我们的程序中集成平方根变得非常简单，来方便地服务于这个目的。在本文中，您将学习如何在 Python 中求平方根。

在继续之前，让我们看一下这里涵盖的主题:

*   [什么是平方根？](#whatissquareroot)
*   [Python 中如何计算平方根:](#calculatingsquarerootinpython)
    *   [使用 sqrt()函数](#sqrt)
    *   [使用 pow()函数](#pow)
*   [Python 中平方根的一个工作示例](#workingexample)

## **什么是平方根？**

平方根是任意数字 y，使得 **x <sup>2</sup> = y** 。数学上表示为 **x = √y** 。Python 提供了计算平方根的内置方法。既然我们对什么是一个数的平方根以及如何表示它有了一个基本的概念，那么让我们来看看如何用 Python 来得到一个数的平方根。

## **Python 中如何计算平方根？**

要在 **[Python](https://www.edureka.co/blog/learn-python-3/)** 中计算平方根，需要导入**数学**模块。这个模块由内置方法组成，即 **sqrt()** 和 **pow()** ，使用它们可以计算平方根。您可以简单地使用 **import** 关键字来导入它，如下所示:

```
import math
```

一旦导入了这个模块，您就可以使用其中的任何函数。

### **使用 sqrt()函数**

sqrt()函数基本上接受一个参数并返回它的平方根。这个函数的语法是:

**语法:**

*sqrt(x)* # x 是需要计算平方根的数。

现在，让我们来看看这个函数的一个例子:

**举例:**

```
from math import sqrt   #absolute importing
print(sqrt(25))
```

**输出:** 5.0

如您所见，25 的平方根，即 5，已经返回。

**注意:**在上面的例子中，已经使用 absolute 方法导入了 sqrt()函数。但是，如果导入完整的数学模块，则可以执行如下操作:

**举例:**

```
import math
print(math.sqrt(25))
```

**输出:** 5.0

### **使用 pow()函数**

另一种计算任意数字平方根的方法是使用 pow()函数。这个函数基本上接受两个参数，并将它们相乘来计算结果。这样做是为了数学方程式中，

x <sup>2</sup> = y **或**y = x * * 5。

该函数的语法如下:

**语法:**

*【pow(x，y)】*#其中 y 是 x 或 x**y 的幂 现在让我们来看看这个函数的一个例子:

**举例:**

```
from math import pow
print(pow(25,.5))
```

**输出:** 5.0

这些函数可以用来解决许多数学问题。现在让我们来看看这些函数的一个这样的应用的工作例子。

## **Python 中平方根的一个工作示例**

让我们尝试使用这些[函数](https://www.edureka.co/blog/python-functions)来实现非常著名的**毕达哥拉斯定理**。

### **问题陈述:**

接受三角形两条边的值，并计算其斜边的值。

### **解决方案:**

毕达哥拉斯定理指出，在直角三角形中，与直角相对的一条边叫做斜边，它的测量值是其他两条边的测量值的平方和的平方根，也就是说

c =√(a2+b2)#其中 c 为斜边

下面是 Python 中的解决方案:

```
from math import sqrt  #Imported the square root function from math module
from math import pow     #Imported the power function from math module

a=int(input("Enter the measure of one side of a right angled triangle:"))    
b=int(input("Enter the measure of another side of a right angled triangle:"))    
#input function is used to take input from user and is stored as string
# which is then typecasted into an integer using the int() function.
c=sqrt(pow(a,2)+pow(b,2))       #we have implemented the formula c=√(a2+b2)
print(f"The measure of the hypotenuse is: {c} based on the measures of the other two sides {a} & {b}")      

```

**输出:**

输入直角三角形一边的尺寸:3 输入直角三角形另一边的尺寸:4

斜边的尺寸是:基于另外两条边的尺寸 3 & 4 的 5.0

这就把我们带到了这篇关于 Python 中平方根的文章的结尾。我希望你已经明白了一切。

***Make sure you practice as much as possible and revert your experience.*  **

*要深入了解 Python 及其各种应用，您可以注册在线直播的 [**Python 认证课程**](https://www.edureka.co/python-programming-certification-training) ，全天候支持，终身访问。*

*有问题吗？请在这个“Python 中的平方根”博客的评论部分提到它，我们会尽快回复您。*