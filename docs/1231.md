# If Else In Python 与示例:你需要知道的一切

> 原文：<https://www.edureka.co/blog/if-else-in-python/>

Python 编程语言极其简单易学。代码行越少，复杂性就越低。它提供了可读性和改进的效率。当用户想要测试多个表达式时，像[控制语句](https://www.edureka.co/blog/loops-in-python/#Loopcontrolstatements)和条件语句这样的概念有助于清晰明了。在本文中，我们将讨论在 [python](https://www.edureka.co/data-science-python-certification-course) 中 if 和 else 的概念。以下是本文讨论的主题。

*   [什么是 Python 条件？](#conditions)
*   [Python 中的‘if’和‘else’是什么？](#ifelse)
*   [控制流程和语法](#syntax)
*   [速记‘if’和‘else’](#shorthand)
*   [用例-嵌套的‘if else’](#usecase)

## **什么是 Python 条件？**

python 中的条件是我们在 if 和 else 语句中使用的逻辑条件。以下是 python 中的一些逻辑条件。

1.  等于–x = = y
2.  不等于–x！= y
3.  小于–x < y
4.  小于或等于–x < = y
5.  大于–x > y
6.  大于或等于–x > = y

这些是我们在 python 中为 if 和 else 语句声明测试表达式时经常使用的条件。

## **Python 中的‘if’和‘else’是什么？**

if 语句用于测试表达式并相应地执行某些语句。一个程序中可以有许多 if 语句。接下来的或者倒数第二条语句是 else 语句，它在程序中所有测试表达式都为假的情况下执行一条语句。要理解 if 和 else 语句的控制流，请看一下执行过程的流程图。

## **流量控制和语法**

如果你仔细观察，你会发现执行从测试表达式开始，当它为真时，执行将进入 If 的主体并执行所有的语句。但是当表达式为 false 时，执行将移动到 else 的主体，并执行 else 块中的语句。

就像 if 语句一样，我们可以在 python 中添加 else if 或 elif 语句来测试更多的表达式，以便优化代码并提高代码的效率。让我们看一下语法，以理解我们如何在 python 中声明 if else 语句块。

**语法:**

```

if (test expression) :
  # statement to be executed
elif (test expression 2):
  # statements of elif block
else:
  # final statement

```

为了理解如何在 python 中使用 if else，让我们看一个程序，看看一个数是偶数还是奇数。

```
x = 10
if x % 2 == 0:
  print('even number')
elif x % 2 == 1:
  print('odd number')
else:
  print('enter a number')

```

```
Output : even number
```

为了检查这个数字，我们在测试表达式中使用了一个逻辑条件，它将检查余数，如果余数为 0，它将在 if 块中打印该语句。否则，它将转到下一个表达式，即 elif 语句。因为 10 除以 2 的余数是 0，所以输出是“偶数”。

让我们举另一个例子，用 if else 找出一个质数。

```
x = 9
for i in range(2,x):
if i % 2 == 0:
print('not a prime number')
else:
print('prime number')

```

在这个程序中，我们还使用了一个循环的[。If else 也可以用在各种循环中。](https://www.edureka.co/blog/loops-in-python/)

## **速记‘if’和‘else’**

如果你只有一个要执行的语句，你可以把它放在一行中。

```
if a > b: print("greater ")

```

**短手扬手**

```
print("greater") if a > b else print("smaller")

```

您也可以使用多个 else 语句。

```
print("greater") if a > b else print("equal")  if a ==b else print("smaller")

```

**在 if else 中使用逻辑运算符**

```
a = 10
b = 20
if a > b and a > 10 :
  print("greater")
elif a < b or a < 10:
  print("smaller")
else:
  print("not a valid number")

```

## **用例——嵌套 if else**

```

x = 10
if x != 0:
   if x % 2 == 0:
      print('even number')
   else:
      print('odd number')
elif x == 0:
   print('equal to zero')
elif x > 0:
  for i in range(2,x):
     if i % 2 == 0:
        print('not a prime number')
     else:
        print('prime number')
else:
   print('less than zero')

```

在这个程序中，我们在 if 语句中使用了多个测试表达式。这就是我们如何在 python 中使用嵌套 if else。

本文涵盖了 python 中与 if else 语句相关的所有概念。通过使用 python 中的条件和控制语句，代码变得高效和优化。 [Python 编程语言](https://www.edureka.co/blog/learn-python-3/)提供了一种简单的语法，提高了可读性，节省了编写复杂代码的工作量。随着像[人工智能](https://www.edureka.co/blog/artificial-intelligence-with-python/)和[机器学习](https://www.edureka.co/blog/scikit-learn-machine-learning/)等领域的发展，python 变得越来越受公司和开发者的欢迎。要掌握与 python 编程相关的所有技能，请注册 edureka 的 [python 认证计划](https://www.edureka.co/data-science-python-certification-course)并开始学习。

*有什么问题吗？在评论中提到他们，我们的团队会尽快回复你。*