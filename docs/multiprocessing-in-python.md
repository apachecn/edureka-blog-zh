# 如何在 Python 中最好地实现多重处理？

> 原文：<https://www.edureka.co/blog/multiprocessing-in-python/>

2019 年是全球技术发展的重要一年。从计算机制造商为他们的 CPU 和处理器增加更多的核心到手机中更智能芯片的推出，多处理不再是一个梦想。今天，支持多处理的最著名的编程语言之一是 [Python](https://www.edureka.co/blog/python-tutorial/) 。由于在其版本中引入了并行处理能力，世界各地的编码人员现在可以无缝地创建同时执行的代码，从而大大缩短了它们的运行时间。

本文将涉及以下几点:

*   什么是多重处理？
*   [Python 中的多重处理代码](#CodeForMultiprocessingInPython)
*   [例 1](#Example1)
*   [例 2](#Example2)

让我们开始吧，

## **Python 中的多重处理**

## 什么是多重处理？

多重处理可以简单地定义为系统在任何给定情况下支持一个以上操作的能力。这意味着多处理系统中的应用程序被分解成小块，然后彼此独立运行，以提高效率并减少总的运行时间。系统中的处理器为每一小部分分配一个独立的线程，从而允许它作为一个独立的实体运行。

**多重处理的需求**

想象一个处理器中只有一个内核的计算机系统。如果多个任务被分配给这个单个内核，那么它会中断中间的每个任务，然后切换到下一个。这不会增加完成每项任务所需的时间，但也会降低系统的整体效率。

另一方面，多处理计算机可以有一个处理器，而处理器内部又有多个功能单元，称为独立核心，能够同时独立运行几个不同的任务。这不仅提高了系统的效率，而且从长远来看，大大减少了系统的运行时间。

Python 中的多重处理系统有两种类型。

#### **多处理器系统**

这个系统基本上有多个处理器，每个处理器一次可以执行一项任务，并作为一个独立的组件运行。

#### **多核处理器系统**

该系统在同一个处理器中有多个内核，内核作为一个独立的单元运行，独立执行分配给它的任务。

## **Python 中的多重处理代码**

现在您已经习惯了多处理的基本概念，让我们来探索一下如何在 Python 中实现多处理。

在 Python 中，解释器包含一个非常简单直观的 API，它接受一个单一的任务，将其分解成多个组件，并独立处理它们。

看看下面的程序模块，更好地理解 python 中多处理的这个概念。

## **例 1**

```
# importing the multiprocessing module
import multiprocessing
def print_cube(num):
"""
function to print cube of given num
"""
print("Cube: {}".format(num * num * num))
def print_square(num):
"""
function to print square of given num
"""
print("Square: {}".format(num * num))
if __name__ == "__main__":
# creating processes
p1 = multiprocessing.Process(target=print_square, args=(10, ))
p2 = multiprocessing.Process(target=print_cube, args=(10, ))
# starting process 1
p1.start()
# starting process 2
p2.start()
# wait until process 1 is finished
p1.join()
# wait until process 2 is finished
p2.join()
# both processes finished
print("Done!") 
```

**输出**

平方:100

立方:1000

搞定！

现在让我们分析一下这个程序，以便更好地理解它。

1.  第一步是导入多处理模块。为此，请使用以下语法:导入多重处理。

2.  现在已经导入了多处理模块，让我们继续创建一个流程。为了做到这一点，我们创建一个 Process 类的对象，并为它分配以下参数。Target:这个进程需要执行的函数，args:需要传递给目标函数的参数。

注意:一个流程构造器能够接受多个目标和参数；但是在上面的例子中，我们只给流程分配了两个目标和参数，如下所示。

p1 =多重处理。Process(target=print_square，args=(10，)

p2 =多重处理。Process(target=print_cube，args=(10，)

1.  既然已经创建了流程，让我们编写启动流程的语法。

p1.start()

p2.start()

一旦进程开始，当前程序和已经执行的程序同时运行。如果在某种情况下，你需要停止当前程序的执行，而只专注于已有程序的执行，我们利用 join 函数，如下所示。

p1.join()

p2.join()

一旦你输入了这个语法，解释器将等待程序 p1 完成执行，然后转到程序 p2。

为了进一步理解这个概念，请看下面 Python 中多处理的另一个例子。

## **例 2**

```
# importing the multiprocessing module
import multiprocessing
import os
def worker1():
# printing process id
print("ID of process running worker1: {}".format(os.getpid()))
def worker2():
# printing process id
print("ID of process running worker2: {}".format(os.getpid()))
if __name__ == "__main__":
# printing main program process id
print("ID of main process: {}".format(os.getpid()))
# creating processes
p1 = multiprocessing.Process(target=worker1)
p2 = multiprocessing.Process(target=worker2)
# starting processes
p1.start()
p2.start()
# process IDs
print("ID of process p1: {}".format(p1.pid))
print("ID of process p2: {}".format(p2.pid))
# wait until processes are finished
p1.join()
p2.join()
# both processes finished
print("Both processes finished execution!")
# check if processes are alive
print("Process p1 is alive: {}".format(p1.is_alive()))
print("Process p2 is alive: {}".format(p2.is_alive())) 
```

**输出**

主进程 ID:18938

进程运行工作者 1 的 ID:18939

进程运行工作者 2 的 ID:18940

进程 p1 的 ID:18939

流程编号 p2: 18940

两个进程都执行完毕！

进程 p1 处于活动状态:假

进程 p2 处于活动状态:假

注意，在上面的程序中，进程 p1 和 p2 都独立于它们各自的内存运行。一旦两者都完成执行，程序就被终止。

这就把我们带到了这篇关于 Python 中多重处理的文章的结尾

*要深入了解 Python 及其各种应用，您可以 [**在此**](https://www.edureka.co/python/) 注册参加在线直播培训，全天候支持，终身访问。*

*有问题吗？在文章的评论部分提到它们，我们会给你回复。*