# 关于 Python 中的 Eval，您需要知道的是

> 原文：<https://www.edureka.co/blog/eval-in-python/>

环顾四周，您会发现一个专门为满足您的需求而构建的应用程序。虽然有许多编程语言可以用来开发这些应用程序，但大多数都是使用 [Python](https://www.edureka.co/blog/python-tutorial/) 构建的。Python 及其强大的特性和不断增加的通用性带来了独一无二的产品，这些产品在任何时候都非常强大和有用。在这篇 Python 中的 Eval 文章中，我们将讨论以下几点:

*   [Python 中的 Eval 是什么？](#what)
*   [评估的缺点](#drawbacks)
*   [用 Python 制作 Eval safe](#safe)
*   [评估的用途](#uses)

## **Python 中的 Eval 是什么？**

Python 中的 eval 函数是最有趣的选项之一。有人称之为黑客，有人称之为捷径，但无论哪种方式，你都可以利用它，在 Python 代码中运行 Python 程序。很酷吧？

当你使用 eval 函数时，你基本上是在催促解释器运行，这个解释器包含在 eval 函数的括号内。

![PythonLogo- Eval in Python](img/14c38303d4c9a170a159d4641d6bbe3f.png)在 Python 中使用 eval 函数的语法是:

`eval(expression, globals=None, locals=None)`

在上面的语法中，

1.  **表达式:** 它是在 Python 程序本身内部被解析和评估为 Python 表达式的字符串或代码段。

2.  **全局:** 它是用来定义所有可用于执行上述表达式的全局方法的字典。这是一个可选实体，其用途取决于您的需要。

3.  **Locals:** 类似于 globals，这是另一个用于指定可用局部方法和变量的字典。

为了更好地理解这个函数的用法，请看下面的例子。

```
from math import *

def secret_function(): 
	return "Secret key is 1234"

def function_creator(): 

	# expression to be evaluated 
	expr = raw_input("Enter the function(in terms of x):") 

	# variable used in expression 
	x = int(raw_input("Enter the value of x:")) 

	# evaluating expression 
	y = eval(expr) 

	# printing evaluated result 
	print("y = {}".format(y)) 

if __name__ == "__main__": 
	function_creator()
```

在上面的例子中，function_creator 是一个函数，当程序执行时，它将评估用户创建的数学表达式。

**输出:**

`Enter the function(in terms of x):x*(x+1)*(x+2)`

`Enter the value of x:3`

`y = 60`

**分析**

既然您已经查看了上面分享的代码，让我们进一步分析一下。

1.  上面的函数将把表达式 x 中的任何变量作为它的输入。

2.  一旦执行，将提示用户输入 x 值，只有在此之后才会生成程序结果。

3.  最后，Python 程序将通过解析作为参数的`expr`来执行 eval 函数。

## **评估的缺点**

与 Python 的其他内置函数类似，eval 也有一些缺点，如果不加以考虑，可能会造成问题。

看一下上面的例子，function_creator 函数的一个主要漏洞是它可以暴露程序中任何隐藏的值，还可以调用一个有害的函数，因为默认情况下 eval 会执行括号内的任何内容。

为了进一步理解这一点，请看下面的例子。

**用户输入**

`Enter the function(in terms of x):secret_function()`

`Enter the value of x:0`

**输出:**

`y = Secret key is 1234`

使用 eval 函数的另一个危险情况是导入 os 模块。当您导入 os 模块时，它允许 Python 读取和写入您的本地系统上存在的任何文件，而无需来自用户的认证。在这种情况下，如果您错误地输入了一行代码，那么您所有的本地文件都可能被删除。

所有这些缺点的解决方案在于限制 eval 函数的功能。

## **在 Python 中实现 Eval 安全**

默认情况下，Eval 提供了解析其有权访问的任何函数或任何已定义函数的选项。在编写代码时记住这一点，将在很大程度上限制 eval 的功能，从而确保不会出错。

为了进一步理解这个概念，请看下面的例子。

```
from math import *

def secret_function(): 
	return "Secret key is 1234"

def function_creator(): 

	# expression to be evaluated 
	expr = raw_input("Enter the function(in terms of x):") 

	# variable used in expression 
	x = int(raw_input("Enter the value of x:")) 

	# passing variable x in safe dictionary 
	safe_dict['x'] = x 

	# evaluating expression 
	y = eval(expr, {"__builtins__":None}, safe_dict) 

	# printing evaluated result 
	print("y = {}".format(y)) 

if __name__ == "__main__": 

	# list of safe methods 
	safe_list = ['acos', 'asin', 'atan', 'atan2', 'ceil', 'cos', 
				'cosh', 'degrees', 'e', 'exp', 'fabs', 'floor', 
				'fmod', 'frexp', 'hypot', 'ldexp', 'log', 'log10', 
				'modf', 'pi', 'pow', 'radians', 'sin', 'sinh', 'sqrt', 
				'tan', 'tanh'] 

	# creating a dictionary of safe methods 
	safe_dict = dict([(k, locals().get(k, None)) for k in safe_list]) 

	function_creator()
```

**用户输入**

`Enter the function(in terms of x):secret_function()`

`Enter the value of x:0`

**输出:**

`NameError: name 'secret_function' is not defined`

正如您所看到的，通过限制对 eval 的访问，可以证明有害的错误输出的机会已经被消除。

## **评估的用途**

如以上章节所述，出于多种安全原因，eval 并不常用。但是，仍然有一些特殊的用例证明使用 eval 是有帮助的。其中一些最重要的是。

1.  如果你希望用户输入他们自己的 scriptlets 来修改程序的输出，那么使用 eval 函数将被证明是有帮助的。

2.  在编写表达式来解决数学查询时，你可以使用 eval，因为它比编写表达式解析器容易得多。

现在您已经了解了 eval 的所有知识，我们希望您在日常编程中也能使用它，同时记住它的优点和缺点。

至此，我们结束了这篇 Python 中的 Eval 文章。 *要深入了解 Python 及其各种应用，您可以 [**在此**](https://www.edureka.co/python/) 注册参加在线直播培训，全天候支持，终身访问。*

*有问题吗？请在“Python 中的 Eval”的评论部分提及它们，我们会尽快回复您。*