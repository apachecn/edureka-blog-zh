# python time sleep()–time . sleep()方法的一站式解决方案

> 原文：<https://www.edureka.co/blog/python-time-sleep/>

有时，我们要求我们的程序或部分程序在一小段时间后执行。 [Python](https://www.edureka.co/blog/python-programming-language) 通过 **time.sleep()函数**让这个任务变得毫不费力。T 他的文章涵盖了这个函数的功能及其应用。

在继续之前，让我们快速浏览一下本文涉及的主题:

让我们开始吧。:)

## **为什么要用 Python time.sleep()？**

当我们想暂停程序流程，让其他程序执行时，睡眠功能起着非常重要的作用。这个函数在 python 的两个版本中都有定义，即版本 2 和版本 3。 它属于 Python 的时间模块。它基本上增加了执行的延迟，它只会暂停当前线程而不是整个程序。

## **时间模块**

Python time.sleep()函数存在于 Python 的时间模块中。在使用这个 [Python 函数](https://www.edureka.co/blog/python-functions)之前，您需要使用以下命令导入这个模块:

```

import time

```

一旦这个模块被导入，您就可以使用 time.sleep()函数了。语法如下:

### **语法:**

*【睡眠(秒)*

它有一个参数，如你所见，是秒。这基本上会在执行过程中导致几秒钟的延迟。该函数的**返回值**为 **void** 。

现在让我们举一些例子来理解这个函数的工作原理。

## **Python time.sleep()示例:**

考虑以下导致输出之间延迟一秒的示例。

**举例:**

```
import time # import time module
sleep_time = 1  # time to add delay after first print statement
print('Hello')
time.sleep(sleep_time)  # sleep time
print('Edureka!')

```

**输出:**

如果执行上述代码，它将在程序中增加一个延迟，因此，下一条语句将在 1 秒钟后执行。 为了精确的延迟，你也可以将浮点值传递给函数。例如，如果经过了 0.1 秒，那么它将产生 100 毫秒的延迟。

下面是另一个例子，它将返回程序执行前后的系统时间。

**举例:**

```
# sleep demonstration
import time
# Start time
print("The time of code execution begin is : ", end ="")
print(time.ctime())
# haulting program
time.sleep(6)
# end time
print("The time of code execution end is : ", end ="")
print(time.ctime())

```

**输出:**

代码执行开始时间为:孙俊 23 22:36:19 2019 代码执行结束时间为:孙俊 23 22:36:25 2019 进程返回 0 (0x0)执行时间:6.089 s 按任意键继续。。。

### **睡眠示例:**

下面是睡眠功能的一个例子:

```
import time
startTime = time.time()
for i in range(5, 10):
  print(i)
  # making delay for 1 second
  time.sleep(1)
endTime = time.time()
elapsedTime = endTime - startTime
print("Elapsed Time = %s" % elapsedTime)

```

**输出:**

56789

经过时间= 5.006335258483887 进程返回 0 (0x0)执行时间:5.147 秒

每次执行暂停 1 秒，整个执行过程耗时 5 秒。此外，执行所需的额外时间是系统为程序做后台操作的时间。

**python 睡眠的不同延迟时间()**

根据所需的输出，可以在 [Python](https://www.edureka.co/blog/learn-python-3/) 中添加不同的程序执行延迟时间。 下面的代码演示了如何做到这一点:

**举例:**

```
import time
for i in [1, 0.1, 2, 0.3]:
  print("I will sleep for %s" % i, end='')
  print(" seconds")
  time.sleep(i)

```

**输出:**

我会睡 1 秒 我会睡 0.1 秒 我会睡 2 秒 我会睡 0.3 秒

进程返回 0 (0x0)执行时间:3.538 秒

### **懒人打印:**

如果你想以一种奇特的方式打印一些东西，你可以使用如下的 sleep()函数:

```
# importing time module
import time
message = "Some fancy character printing!"
for i in message:
   print(i)
   time.sleep(0.3)

```

如果你执行上面的代码，你会看到每个看起来很漂亮的字符打印延迟。

## **Python 线程休眠**

在多线程环境中，sleep()被证明是非常重要的，因为当执行时，它可以在正在执行的当前线程中增加延迟。

**举例:**

```
import time
from threading import Thread
class Runner(Thread):
   def run(self):
       for x in range(0, 7):
           print(x)
           time.sleep(2)
class Delay(Thread):
   def run(self):
       for x in range(106, 109):
           print(x)
           time.sleep(7)
print("Staring Runner Thread")
Runner().start()
print("Starting Delay Thread")
Delay().start()
print("Done")

```

下面是上面线程示例的输出:

**![python thread sleep- Python Sleep - Edureka](img/f35d29aa858a6bae26b30c375752987c.png)输出:**

如果你执行程序，你会注意到整个程序并没有停止，只是当前正在执行的线程停止了，试一试吧。

**应用:**

这种方法有许多应用，例如，我们可以用它来创建一个漂亮的用户界面，以某种奇特的方式打印菜单或标题，然而，其中一个重要的应用是暂停一个将在某个时间间隔执行的后台进程。

**应用示例:**

```
import time
string = "Edureka!"
print_string = ""
for i in range(0, len(string)):
   print_string = print_string + string[i]
   print(print_string)
   time.sleep(2)

```

**输出:**

EEdedu爱德华 爱德华 爱德华 爱德华 爱德华！

正如我们已经看到的，睡眠功能暂停程序一段时间，这正是 Python 的时间模块派上用场的地方。让我们来看看如何从用户那里获取输入，并动态地使用相同的函数。

## **动态睡眠示例**

这是一个睡眠示例，它接受用户的输入，在两个打印功能之间添加延迟，并打印执行打印功能所用的时间，以下示例基于 Python 3.x.

```
import time
def sleeper():
	while True:
		num = input('Enter wait time: ')
		try:
			num = float(num)
		except ValueError:
			print('Number only.n')
			continue
			# Run our time.sleep() command,
			# and show the before and after time
		print('Before: %s' % time.ctime())
		time.sleep(num)
		print('After: %sn' % time.ctime())

try:
	sleeper()
except KeyboardInterrupt:
	print('nnException Exiting.')
	exit()

```

**输出:**

输入等待时间:1 前:孙俊 23 22:44:13 2019 后:孙俊 23 22:44:14 2019 输入等待时间:3 前:孙俊 23 22:44:16 2019 后:孙俊 23 22:44:19 2019

**精度**

如果您想在更短的时间内停止执行，此功能会受到操作系统的限制，因为此功能使用操作系统的 sleep()功能，与 windows 相比，Linux 中的等待时间会更短。

**总结**

在上面的文章中，我们介绍了 python 中的 sleep()方法，该方法主要用于增加程序执行的延迟，这个包在 Python 中的时间模块中，它主要使用底层操作系统的 sleep()函数。我们还介绍了一些如何使用该函数的代码示例，并研究了睡眠的应用程序。演示了使用这个函数的奇特方法以及它在线程环境中的工作方式。

*要深入了解 Python 及其各种应用，您可以注册参加实时 **[Python 在线培训](https://www.edureka.co/python-programming-certification-training)** ，该培训提供全天候支持和终身访问。*

*有问题吗？请在这篇“Python 中的 Python 时间睡眠方法”博客的评论部分提到它，我们会尽快回复你。*