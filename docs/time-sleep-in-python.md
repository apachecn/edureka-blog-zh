# 如何在 Python 中实现时间睡眠？

> 原文：<https://www.edureka.co/blog/time-sleep-in-python/>

今天，你环顾四周，就会发现各种应用。虽然所有这些应用程序都是用各种不同的编程语言编写的，但迄今为止最流行的语言之一是 [Python 编程](https://www.edureka.co/blog/python-programming-language)语言。在本文中，我们将按以下顺序了解 Python 中著名的模块 time sleep:

*   [Python 中的时间睡眠介绍](#timesleep)
*   [睡眠模块应用](#application)
*   [多线程程序 Python 中的时间睡眠](#multithread)

## **Python 中的时间睡眠介绍**

在日常编程中，经常需要暂停一个程序，以便进行其他操作。虽然在中间暂停一个程序可以达到特定的目的，但它也可以简单地增加整个操作的效率。无论需要什么，Python 中的 **sleep()** 模块都可以用来实现这一点。

sleep()模块的使用提供了一种准确而灵活的方法来实现这一点。在 Python 的最新版本(Python 2 和 3)中，睡眠模块已经被时间模块所取代，两者具有相同的功能。

**语法:**

```
sleep(sec)
```

在上面的语法中，sec 用于定义暂停执行的秒数。

为了更好地理解睡眠[功能](https://www.edureka.co/blog/python-functions)的使用，请看下面的例子:

```
# Python code to demonstrate
# working of sleep()

import time

# printing the start time
print("The time of code execution begin is : ", end ="")
print(time.ctime())

# using sleep() to hault the code execution
time.sleep(6)

# printing the end time
print("The time of code execution end is : ", end ="")
print(time.ctime())
```

**输出:**

![Output 1 - time sleep in python - edureka](img/b99e210bbd3ccd5b1dda6cc2f716172b.png)

让我们举另一个例子来理解 Python 中延迟函数的工作原理:

```
import time
print("Printed immediately.")
time.sleep(2.4)
print("Printed after 2.4 seconds.")
```

在上面的程序中，第一个[字符串](https://www.edureka.co/blog/python-string-concatenation/)被立即打印，然后第二个字符串在 time.sleep 模块中提到的 2.4 秒的延迟后被打印。

**输出:**

![Output 2 - time sleep in python - edureka](img/bed575fc633c390c1147ca15cac56636.png)

## **睡眠模块的应用**

与 Python 接口中的所有其他模块类似，sleep 函数适用于多种应用。睡眠功能最重要的用途之一是定期执行后台线程。睡眠功能的另一个很好的用途是[一个字母一个字母地打印字符串](https://www.edureka.co/blog/strings-in-python)，以获得更好的用户体验。

为了更好地理解这个应用程序，请看下面的例子:

```
# Python code to demonstrate
# application of sleep()

import time

# initializing string
strn = "Edureka says Hello!"

# printing geeksforgeeks after delay
# of each character
for i in range(0, len(strn)):
print(strn[i], end ="")
time.sleep(2)
```

**输出:**

![](img/329fb043f1831a238a1b83066ffdf2bf.png)

让我们来看另一个例子，我们使用 Python 中的 time.sleep 模块创建了一个数字时钟:

```
import time
while True:
localtime = time.localtime()
result = time.strftime("%I:%M:%S %p", localtime)
print(result)
time.sleep(1)
```

如果你看到上面的程序，你会发现我们在无限循环中多次打印了本地时间，这是通过 time.sleep 函数实现的。第一次迭代后，程序等待 1 秒钟，计算本地时间，然后打印出来，除非提示停止，否则重复计算无限次。

**输出:**

![](img/cb518d3365d116481050d4531ed6bfba.png)

下面提到的是上述程序的一个稍加修改的版本:

```
import time
while True:
localtime = time.localtime()
result = time.strftime("%I:%M:%S %p", localtime)
print(result, end="", flush=True)
print("r", end="", flush=True)
time.sleep(1)
```

## **Python 多线程程序中的时间和睡眠模块**

时间和睡眠模块也可以在[多线程 python](https://www.edureka.co/blog/what-is-mutithreading/) 程序中使用，以实现某些结果。它在单线程和多线程程序中使用的主要区别在于，在单线程程序中，sleep 函数挂起线程和进程的执行。另一方面，在多线程程序中，单个线程而不是整个进程被挂起。

为了更好地理解这个概念，请看下面的例子:

```
import threading
import time

def print_Edureka():
for i in range(4):
time.sleep(0.5)
print("Edureka ")

def print_Python():
for i in range(4):
time.sleep(0.7)
print("Python")
t1 = threading.Thread(target=print_ Edureka)
t2 = threading.Thread(target=print_ Python)
t1.start()
t2.start()
```

在上面的程序中，有两个线程，每个线程的延迟分别为 0.5 秒和 0.75 秒。当程序在解释器中运行时，这些是同时执行的，不需要停止整个过程。

**输出:**

![](img/eaa82075a8660129ac1363f96d590b3e.png)

Python 中的时间和睡眠模块可以用于实现许多不同的目的。从上面的例子中，我们希望你已经了解了它们各自的功能、区别以及如何在日常使用中使用它们。

*现在您已经了解了什么是 Python，请查看 Edureka 的 [Python 编程认证](https://www.edureka.co/python-programming-certification-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

有问题要问我们吗？请在这个“Python 中的时间睡眠”博客的评论部分提到它，我们会尽快回复你。