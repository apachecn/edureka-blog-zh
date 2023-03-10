# 除了 Python 之外，Try 是什么，它是如何工作的？

> 原文：<https://www.edureka.co/blog/python-try-except/>

无论你多么擅长编程，在某些脚本中都会有错误。这些错误可能是由于意外的用户输入、错误的服务器响应或任何其他原因而发生的。Try Except in [Python](https://www.edureka.co/blog/what-is-python/) 允许你捕捉错误，而不是死亡，做一些更合理的事情。在本文中，我们将看到 Python 如何使用 try-except 按以下顺序处理异常:

*   除了在 Python 中，Try 是什么？
*   Try 是如何工作的？
*   [Python 异常示例](#example)
*   [异常处理](#exception)
*   [异常错误](#error)

## 除了在 Python 中，Try 是什么？

Try [方法](https://www.edureka.co/blog/python-method-overloading/)用于错误和异常处理。[错误有两种](https://www.edureka.co/blog/indentation-error-in-python/):

*   **语法错误**:也称解析错误。当 Python 解析器无法理解一行代码时，就会出现这种情况。

*   **异常错误**:这些错误是在执行过程中检测到的。

现在，在这些情况下，我们需要在 Python 代码中处理这些错误。这就是 python 中 try-except 派上用场的地方。

**语法:**

```
try:
// Code
except:
// Code
```

**举例:**

```
try:
print(x)
except:
print("An exception occurred")
```

**输出:**

![Output: try except in python - edureka](img/c84443d9d9dfd54a58e346004cf4f4e6.png)

## Try()是如何工作的？

try 工作中涉及的不同步骤有:

*   子句在和  **子句之间执行，但** 子句除外。
*   如果没有异常，那么只有子句会运行，而子句则运行完毕。
*   如果出现任何异常，将跳过  **try** 子句，运行除 子句之外的  **子句。**
*   在出现异常的情况下，如果  **代码内除了** 子句没有处理它，它就被传递给外层的语句。如果异常未得到处理，执行将会停止。
*   一个语句可以有多个子句除外。

## **Python 异常示例**

在第一个示例中，没有异常，因此 try 子句将运行:

```
def divide(x, y):
try:
result = x // y
print("The answer is :", result)
except ZeroDivisionError:
print("Sorry ! Cannot divide by zero ")
divide(10, 5)
```

**输出:**

```
The answer is : 2
```

在第二个示例中，有一个异常，因此只有 except 子句将运行:

```
def divide(x, y):
try:
result = x // y
print("The answer is :", result)
except ZeroDivisionError:
print("Sorry ! Cannot divide by zero ")
divide(4, 0)
```

**输出:**

```
Sorry ! Cannot divide by zero
```

## **异常处理**

Python 中的 **try** 和 **except** 块用于捕捉和处理异常。 [Python](https://www.edureka.co/blog/python-programming-language) 执行代码，将 try 语句视为程序的正常部分。然而，except 语句充当程序对前面 try 子句中任何[异常](https://www.edureka.co/blog/exceptions-in-python/)的响应。

异常便于处理程序中的错误和特殊情况。如果你正在处理一个可能产生错误的代码，那么你可以使用异常处理。此外，您可以通过使用**引发异常语句**在自己的程序中引发异常。引发异常会中断当前的代码执行，并返回异常，直到它被处理。

## **异常错误**

有不同类型的异常错误，例如:

*   **IOError** :如果文件无法打开
*   **键盘中断**:当用户按下不需要的键时
*   **ValueError** :内置函数收到错误参数时
*   **EOFError** :如果在未读取任何数据的情况下点击文件结尾
*   **导入错误**:如果找不到模块

说到这里，我们的文章就到此为止了。我希望你理解了 Python 中的 try except 以及它是如何用于处理异常的。

*要深入了解 Python 及其各种应用，您可以注册参加现场 **[Python 认证培训](https://www.edureka.co/python)** ，该培训提供全天候支持和终身访问。*

*有问题吗？请在这个“除了 Python 之外的尝试”博客的评论部分提到它，我们会尽快回复你。*