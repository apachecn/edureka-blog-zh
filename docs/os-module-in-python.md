# Python 中的操作系统模块:您需要知道的一切

> 原文：<https://www.edureka.co/blog/os-module-in-python>

Python 是当今业界最强大的编程语言之一。得益于其广泛的特性和强大的通用性，许多复杂的编程目标都可以在 Python 中轻松实现。在本文中，我们将按以下顺序讨论 Python 中的 OS 模块:

*   [Python 中的 OS 模块是什么？](#what)
*   [操作系统模块的功能](#functions)

**Python 中的 OS 模块是什么？**

Python 中的 OS 模块是编程语言标准库的一部分。导入时，它允许用户与 Python 当前运行的本地操作系统进行交互。简而言之，它为用户提供了一种简单的方式来与一些在日常编程中派上用场的操作系统功能进行交互。

![OS Module in Python](img/4c6f99f56333f713cda7948445645f94.png)

OS 模块和 os.path 模块是相同的，可以很容易地从标准库中导入，只需一会儿通知。

**操作系统模块的功能**

现在你已经知道了操作系统模块的定义，让我们来看看它的一些功能。

*   **os.name:** 如果你想知道 Python 当前运行的操作系统的名称和凭证，那么使用 os.name 函数。看一下下面的例子，以便更好地理解它的实现。

```
import os 
print(os.name) 
```

**输出:**

`posix`

**注意:** 以上程序会根据你当前使用的操作系统给出不同的输出。

*   **os.getcwd():** 如果你想知道当前的工作目录或者已经用来运行你的代码的 cwd，那么你可以利用这个函数。与 os.name 函数类似，它的输出会根据安装它的系统而有所不同。

```
import os 
print(os.getcwd()) 
# To print absolute path on your system 
# os.path.abspath('.') 

# To print files and directories in the current directory 
# on your system 
# os.listdir('.')
```

**输出:**

`C:UsersGFGDesktopModuleOS`

**注意:** 如果你使用的是 GFG 解释器，那么默认使用的目录将是/root。

*   **os.error:** 每当您在 Python 中使用从标准库导入的模块或函数时，如果您使用了不正确的路径和文件名，或者使用了具有正确类型但不被您当前使用的操作系统接受的参数，它将引发 OSError。这个函数是 Python 中内置 OSError 异常的别名。为了更好地理解这一点，请看下面的例子。

```
import os 
try: 
	# If the file does not exist, 
	# then it would throw an IOError 
	filename = 'GFG.txt'
	f = open(filename, 'rU') 
	text = f.read() 
	f.close() 

# Control jumps directly to here if 
#any of the above lines throws IOError.	 
except IOError: 

	# print(os.error) will <class 'OSError'> 
	print('Problem reading: ' + filename) 

# In any case, the code then continues with 
# the line after the try/except
```

**输出:**

`Problem reading: GFG.txt`

*   **os.popen():** 该函数是文件对象操作的一部分，用于打开与命令之间的管道。根据您使用 r 或 w，可以读取或写入此函数的返回值。此函数的语法如下，os.popen(command[，mode[，bufsize]])。考虑的参数有模式和缓冲区大小。为了更好地理解这一点，请看下面的例子。

```
import os 
fd = "GFG.txt"

# popen() is similar to open() 
file = open(fd, 'w') 
file.write("Hello") 
file.close() 
file = open(fd, 'r') 
text = file.read() 
print(text) 

# popen() provides a pipe/gateway and accesses the file directly 
file = os.popen(fd, 'w') 
file.write("Hello") 
# File not closed, shown in the next function.
```

**输出:**

`Hello`

*   **os.close():** 如果你想关闭文件目录 fd，那么你可以利用这个功能。使用时，首先需要使用 open()函数打开文件，然后使用 close()函数关闭文件。为了更好地理解这一点，请看下面的例子。

```
import os 
fd = "GFG.txt"
file = open(fd, 'r') 
text = file.read() 
print(text) 
os.close(file)
```

**输出:**

`Traceback (most recent call last):`

`  File "C:UsersGFGDesktopGeeksForGeeksOSFile.py", line 6, in `

`    os.close(file)`

`TypeError: an integer is required (got type _io.TextIOWrapper)`

*   **os.rename():** 如果在某种情况下你需要重命名一个已经存在的旧文本文件，你可以利用这个功能。注意:仅当文件已经存在于目录中，并且用户具有相应的权限时，才更改上下文中的文件名。为了更好地理解这一点，请看下面的例子。

```
import os 
fd = "GFG.txt"
os.rename(fd,'New.txt') 
os.rename(fd,'New.txt')
```

**输出:**

`Traceback (most recent call last):`

`  File "C:UsersGFGDesktopModuleOSGeeksForGeeksOSFile.py", line 3, in `

`    os.rename(fd,'New.txt')`

`FileNotFoundError: [WinError 2] The system cannot find the`

`file specified: 'GFG.txt' -> 'New.txt'`

Python 中的 os 模块可以用来访问很多操作系统功能。现在你已经知道了它的用途，我们希望你能在你的日常编程中使用它。

至此，我们结束了 Python 中的这个 OS 模块。我希望你对 OS 模块的所有疑虑现在都消除了。

*要深入了解 Python 及其各种应用，您可以 [**在此**](https://www.edureka.co/python/) 注册参加在线直播培训，全天候支持，终身访问。*

*有问题吗？在“Python 中的成员操作符”的评论部分提到它们，我们会回复您。*