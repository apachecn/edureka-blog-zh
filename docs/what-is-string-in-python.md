# Python 中的字符串函数:如何通过例子使用它

> 原文：<https://www.edureka.co/blog/what-is-string-in-python/>

本文将告诉你什么是 Python 函数中的字符串，并详细介绍一下 Python 字符串函数的概念。本文将涉及以下几点:

*   [如何创建字符串？](#Howtocreateastring?)
*   如何从字符串中访问一个字符？
*   [格式化字符串](#FormattingaString)

那么让我们开始吧，

## **Python 中的 String 是什么？**

我们中的许多人都熟悉 C、C++等编程语言。会有类似“字符串是字符的集合或数组”的答案

在 Python 中，我们对字符串数据类型也有同样的定义。 Python String 是有序字符的数组，写在单引号、双引号或三引号内。另外，Python 没有字符数据类型，所以当我们写' a '时，它被当作长度为 1 的字符串。

继续这篇文章，什么是 Python 中的字符串函数？

**如何创建字符串？**

```
s = 'Hello'
print(s)
s1 = "Hello"
print(s1)
s2 = ''' Hello
How is the <span style="font-weight: 400;" data-mce-style="font-weight: 400;">weather</span> today? '''
print(s2)

```

**输出:**

你好你好你好今天天气怎么样？

当我们在字符串中既有单引号又有双引号时，以及当我们想写多行句子时，通常会使用三重引号。

**注**

我们需要注意的是，在使用单引号时，字符串中不应该包含单引号，因为如果发生这种情况，Python 会认为该行在出现第二个引号时结束，并且不会获取所需的输出。同样的符号后面应该加上双引号和三引号。

现在让我们进入 Python 字符串函数的文章

如何从字符串中访问一个字符？

假设我们想从字符串中访问一个字符，比如说最后一个字符，我们需要知道它在字符串中的位置。

![Image- Python String Function - Edureka](img/7a198dc9245864ad1d10a684f706d747.png)

这是一个字符串以及分配的位置。所以如果我们想从字符串中访问' n ',我们必须到第 5 个位置。

编号或索引从 0 开始，比字符串长度小 1。

这里有一个 python 程序可以让我们更清楚地理解这一点。

```
str = 'Antarctica is really cold.'
print('str = ', str)
#first character
print('str[0] = ', str[0])
#last character
print('str[-1] = ', str[-1])
#slicing 2nd to 5th character
print('str[1:5] = ', str[1:5])
#slicing 6th to 2nd last character
print('str[5:-2] = ', str[5:-2])

```

**输出:**

str =南极洲真的很冷。 str[0] =一个 str[-1] =。str[1:5]= ntarstr[5:-2]= ctica 真的是 col

现在，如果在索引中从左到右遵循升序模式，则从右到左遵循降序模式，即从-1、-2、-3 等等。所以如果你想访问最后一个字符，你可以用两种方法。

```
str = 'Antarctica is really cold.'
a = len(str)
print('length of str ', a)
#last character with the help of length of the string
print('str[a] ', str[a-1])
#last character with the help of indexing
print('str[-1] ',str[-1])

```

**输出:**

str 26 的长度 str[a]。 str[-1]。

Python 字符串本质上是不可变的，这意味着一旦字符串被声明，其中的任何字符都不能改变。

```
s = "Hello Batman"
print(s)
s[2] = 'P'
print(s)

```

**输出:**

Hello Batman Traceback(最近一次调用 last): 文件" C:/Users/prac.py "，第 3 行，在 s[2] = 'P' TypeError: 'str '对象不支持项赋值

过程结束，退出代码为 1

但是你可以用 del 操作符删除整个字符串。

```
s = "Hello Batman"
print(s)
del s
print(s)

```

**输出:**

Hello Batman Traceback(最近一次呼叫 last): 文件" C:/Users/prac.py "，第 4 行，在 print(s)name 错误:name 's '未定义

过程结束，退出代码为 1

如果你不希望 s 是“你好蝙蝠侠”，而希望它是某个其他的字符串，那么你可以直接更新整个字符串。

```
&amp;nbsp; 
s = "Hello Batman"
print(s)
s = "Hello Spiderman"
print(s)

```

**输出:**

你好蝙蝠侠你好蜘蛛侠

继续这篇关于什么是 Python 中的字符串的文章。

## **格式化字符串:**

格式化字符串意味着将字符串动态地分配到您想要的任何地方。

Python 字符串可以使用 format()方法进行格式化，这是一个非常通用和强大的字符串格式化工具。String 中的 Format 方法包含花括号{}作为占位符，这些占位符可以根据位置或关键字保存参数以指定顺序。

```
String1 = "{} {} {}".format('Hello', 'to', 'Batman')
print("Default order: ")
print(String1)
# Positional Formatting
String1 = "{1} {0} {2}".format('Hello', 'to', 'Batman')
print("nPositional order: ")
print(String1)
# Keyword Formatting
String1 = "{c} {b} {a}".format(a='Hello', b='to', c='Spiderman')
print("nString in order of Keywords: ")
print(String1)
# Formatting of Integers
String1 = "{0:b}".format(20)
print("binary representation of 20 is ")
print(String1)
# Formatting of Floats
String1 = "{0:e}".format(188.996)
print("nExponent representation of 188.996 is ")
print(String1)
# Rounding off Integers
String1 = "{0:.2f}".format(1 / 6)
print("none-sixth is : ")
print(String1)
# String alignment
String1 = "|{:&lt;10}|{:^10}|{:&gt;10}|".format('Hello', 'to', 'Tyra')
print("nLeft, centre and right alignment with Formatting: ")
print(String1)

```

**输出:**

默认顺序:蝙蝠侠你好

位置顺序:到你好蝙蝠侠

按关键字顺序串:蜘蛛侠你好

20 的二进制表示是 10100

188.996 的指数表示为 1.889960e+02

六分之一是: 0.17

格式:左、中、右对齐: |Hello | to | Tyra|

通过格式方法，字符串可以左对齐()或居中(^)。

{:<10}.format(“Hello”)意味着 Python 将为字符串保留 10 个空间，字符串将从左边开始。这同样适用于右对齐和居中对齐。

我希望你已经很好地学习了 Python 字符串函数的概念，并因此尝试更准确地使用它。

这就把我们带到了这篇文章的结尾，什么是 Python 中的字符串？当这种情况发生时，不要袖手旁观，掌握你的技能，报名参加 Edureka 的  [python 认证项目](https://edureka.co/python) ，成为一名领导者。

*有什么问题吗？请在评论中提及它们。我们会尽快回复你。*