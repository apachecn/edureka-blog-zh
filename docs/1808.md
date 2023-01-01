# 关于 Python 中的打印异常，您需要知道的一切

> 原文：<https://www.edureka.co/blog/print-exception-in-python/>

在当今时代，不管你是否从事编码行业，你可能至少听说过一次 [Python](https://www.edureka.co/blog/python-tutorial/) 。自 1991 年问世以来，这种编程语言凭借其广泛的特性和强大的通用性赢得了大量的声誉和勇气。但即便如此，这种编程语言的某些方面仍然让专业人员和业余程序员感到困惑。其中一个方面是打印例外。因此，在本文中，我们将探索 Python 中的打印异常，并深入探究其核心。

本文将涉及以下几点:

*   [Python 中的错误](#ErrorsinPython)
*   [Python 中的语法错误与异常](#SyntaxErrorsvsExceptionsinPython)
*   [Python 中的异常类型](#TypesofExceptionsinPython)
*   [引发异常](#RaisinganException)
*   [Python 中的异常类型](#TypesofExceptionsinPython)

那么让我们开始吧，

## **Python 中的打印异常**

## **Python 中的错误**

在 Python 操作系统中，有两种主要类型的错误。第一个是语法错误，第二个是异常错误。无论你在 Python 中遇到什么类型的错误，一旦它出现，整个解释器都会中途停止，从而扰乱你的工作流程。在本文中，我们将关注 Python 中的异常，以及如何绕过它们。

继续这篇关于 Python 中打印异常的文章，

**Python 中的语法错误与异常**

当解释器在代码行中检测到不正确的语句时，Python 中就会出现语法错误。为了更好地理解这一点，请看下面的例子。

```
>>> print( 0 / 0 ))
File "<stdin>", line 1
print( 0 / 0 ))
^
SyntaxError: invalid syntax
```

上例中的光标指出了代码中语法错误的确切位置。在上面的例子中，我们使用了太多的括号，从而导致了语法错误。看看下面给出的正确例子。

```
>>> print( 0 / 0)
Traceback (most recent call last):
File "<stdin>", line 1, in <module>
```

ZeroDivisionError:整数除法或以零为模

如果你观察上面的例子，你会很快意识到虽然这里没有语法错误，但是解释器遇到了一个异常错误。这基本上意味着，在运行你的代码时，解释器产生了一个错误，这也被称为异常错误。

在上面的例子中需要注意的另一件事是，代码的最后一行指出了这一行代码中出现的异常错误的类型。

对于 Python 来说，这是最有趣的方面之一。解释器不会只告诉你代码中有一个错误，而是会生成异常并告诉你错误到底是什么。在某些情况下，如果错误对解释器来说是新的，它会创建一个新的异常来方便地为您定义它。

继续这篇关于 Python 中打印异常的文章，

## **引发异常**

在某些情况下，您可能需要手动引发一个异常来帮助进行审计。为此，请使用提升功能。使用 raise 函数的一个优点是，它可以与一个自定义异常一起使用。如果在某种情况下，您希望在 raise 函数中包含某种条件，请遵循下面的示例。

x = 10

如果 x > 5:

引发异常(' x 不应超过 5。x 的值是:{} '。格式(x))

当这段代码运行时，输出如下所示。

回溯(最近一次呼叫):

文件“”，第 4 行，在<module>中</module>

例外:x 不应超过 5。x 的值是:10

当条件满足时，程序会在中间暂停，并在屏幕上显示异常。

继续这篇关于 Python 中打印异常的文章，

## **Python 中的异常类型**

在 Python 中，有几种类型的异常可供使用。一些最重要的问题如下所述。

1.  AssertionError 异常
2.  else 子句
3.  try and except 块
4.  最后的例外

#### **assertion error 异常**

AssertionError 异常是全世界程序员最常用的异常之一。这种方法不是等待程序中途停止，而是在开始时包含一个条件。如果满足条件，则程序继续运行，如果不满足条件，则程序停止运行，并在屏幕上出现异常。为了更好地理解这一点，请看下面的例子。

```
import sys
assert ('linux' in sys.platform), "This code runs on Linux only."
```

#### **else 子句**

在 Python 中，只有当程序内容中缺少异常时，才可以使用 else 子句运行特定的代码块。为了更好地理解这个过程，请看下面的例子。

```
try:
linux_interaction()
except AssertionError as error:
print(error)
else:
print('Executing the else clause.')
```

继续这篇关于 Python 中打印异常的文章，

#### **尝试和排除块**

Python 中 try 和 except 块的主要用途是捕获和处理异常。解释器遵循 try 语句，正常执行程序。如果程序中出现异常，将执行 except 块之后的语句来有效地处理它们。看一下下面的例子来更好地理解这个概念。

```
def linux_interaction():
assert ('linux' in sys.platform), "Function can only run on Linux systems."
print('Doing something.')
try:
linux_interaction()
except:
pass
```

**最后的例外**

在某些情况下，无论是否遇到异常，都需要执行程序。在这些情况下，最终的异常开始起作用。通过使用这个，你可以督促解释器继续运行你的代码，不管条件是否满足。为了更好地理解这一点，请看下面的例子。

```
try:
linux_interaction()
except AssertionError as error:
print(error)
else:
try:
with open('file.log') as file:
read_data = file.read()
except FileNotFoundError as fnf_error:
print(fnf_error)
finally:
print('Cleaning up, irrespective of any exceptions.')
```

这就把我们带到了这篇关于 Python 中打印异常的文章的结尾，

*要深入了解 Python 及其各种应用，您可以 [**在此**](https://www.edureka.co/python/) 注册参加在线直播培训，全天候支持，终身访问。* *有问题吗？在这篇文章的评论部分提到它们，我们会给你回复。*