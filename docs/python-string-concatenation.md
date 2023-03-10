# Python 字符串串联:您需要知道的一切

> 原文：<https://www.edureka.co/blog/python-string-concatenation/>

本文将向您介绍在某些情况下具有巨大价值的简单编程概念，即 [Python](https://www.edureka.co/blog/python-tutorial/) 字符串连接。本文将涉及以下几点:

*   [Python 字符串串联](#Pythonstringconcatenation)
*   [Python 中的串联](#ConcatenationinPython)
*   [在 Python 中格式化字符串](#FormattingaStringinPython)
*   [使用%运算符](#Usingthe%operator)
*   [使用{}运算符](#Usingthe%7B%7Doperator)
*   [使用连接方法](#UsingtheJoinMethod)

那么让我们开始吧，

## **Python 字符串串联**

如果您是使用 Python 语言的新手，您可能从未听说过术语字符串连接。无论您使用哪种编程语言，总会有需要将两个或更多字符串的内容合并在一起的时候，这个过程在技术术语中称为串联。解释这个概念最简单的方法是；你把存储在解释器中的两个不同的字符串合并在一起，以达到一个统一的目的。这种操作的一个例子是:Python 中有两个不同的字符串 hello 和 world。你利用连接函数，把它们合成一个，这就是 hello world。

继续这篇关于 Python 字符串连接的文章

## **Python 中的串联**

在 Python 中有几种主要的方法来连接字符串。但首先让我们弄清楚基本情况；两个单独的字符串串联后形成的新字符串称为 string 对象。这是因为，Python 的核心是一种面向对象的语言，因此其中的每个元素，无论是已经存在的还是新创建的，都被称为对象。

在 Python 中连接两个字符串最简单的方法是使用+或+运算符。这方面的一个例子如下。

```
str1 = “Hello”
str2 = “World”
str1 + str2
```

上面代码的最后一行是连接，当这个过程被执行时，一个新的字符串就形成了。

这里需要注意的最重要的一点是，Python 不能连接整数和字符串，因为它们被认为是根本不同的对象。如果你想连接一个字符串和一个整数，你首先需要把它们转换成一个不同的对象，也就是把字符串转换成整数或者把整数转换成字符串。

如果您试图在不转换的情况下连接一个字符串和整数，屏幕上会返回一个错误。为了更好地理解这一点，请看下面的例子。

```
>>> print &lsquo;red&rsquo; + &lsquo;yellow&rsquo;
Redyellow
>>> print &lsquo;red&rsquo; * 3
Redredred
>>> print &lsquo;red&rsquo; + 3
Traceback (most recent call last):
File &ldquo;&rdquo;, line 1, in
TypeError: cannot concatenate &lsquo;str&rsquo; and &lsquo;int&rsquo; objects
>>
```

继续这篇关于 Python 字符串连接的文章

## **在 Python 中格式化字符串**

现在你已经了解了在 Python 中连接字符串的基础知识，让我们讨论更多关于在 Python 中格式化字符串的内容。

在 Python 中，字符串插值主要有两种方法。为了更好地理解这一点，让我们先来看看字符串插值是什么意思。

Python 中的字符串插值可以简单地定义为评估字符串值的过程，该字符串值作为一个或多个占位符包含在解释器内存中。简单地说，字符串插值是一种让开发人员更容易在 Python 中执行字符串格式化和连接的方法。

继续这篇关于 Python 字符串连接的文章

## **使用%运算符**

在 Python 中实现字符串连接的最广泛接受的方法之一是使用%运算符。要理解它在代码中的确切用法，请看下面的例子。

```
x = ‘apples’
y = ‘lemons’
z = “In the basket are %s and %s” % (x,y)
```

在上面的代码中，解释器所做的是用存储在变量 x 和 y 中的值替换%s 的值。当变量 z 被打印出来时，会得到下面的结果。

*篮子里是苹果和柠檬*

继续这篇关于 Python 字符串连接的文章

## **使用{}运算符**

在编码时，如果你使用{}，它将作为一个占位符来存放你想存放在字符串中的变量。但是为了在字符串内部传递变量，首先需要使用 format()函数。

使用 format()函数的一个主要优点是，在连接数据之前，不需要将整数转换成字符串；它会自动为你做同样的事情。这是为什么这种字符串连接方法比其他方法更受欢迎的主要原因之一。

为了更好地理解这个概念，请看下面的例子。

```
Fname = “John”
Lname = “Doe”
Age = “24”
print “{} {} is {} years old.“ format(fname, lname, age)
```

运行这段代码时，解释器将获取适当的值，并将它们作为变量存储在各自的字符串中。

继续这篇关于 Python 字符串连接的文章

## **使用连接方法**

最后但同样重要的是在 Python 中使用 Join 方法。这种方法的最佳用途是在一个结果中将一系列字符串连接在一起。为了更好地理解这一点，请看下面的例子。

```
>>> &lsquo; &lsquo; .join([&lsquo;the&rsquo;, &lsquo;quick&rsquo;, &lsquo;brown&rsquo;, &lsquo;fox&rsquo;, &lsquo;jumps&rsquo;, &lsquo;over&rsquo;, &lsquo;the&rsquo;, &lsquo;lazy&rsquo;, &lsquo;dog&rsquo;])
```

敏捷的棕色狐狸跳过了懒惰的狗

现在让我们创建一个新列表。

```
>>> music = [&ldquo;Metallica&rdquo;, &ldquo;Rolling Stones&rdquo;, &ldquo;ACDC&rdquo;, &ldquo;Black Sabbath&rdquo;, &ldquo;Shinedown&rdquo;]
```

现在我们使用下面的方法来连接这两个字符串。

```
>>> print &lsquo; &rsquo;.join(music)
>>> print &ldquo;
&ldquo;.join(music)
```

这就把我们带到了关于 Python 字符串连接的这篇文章的结尾。

*要深入了解 Python 及其各种应用，您可以 [**在此**](https://www.edureka.co/python/) 注册参加在线直播培训，全天候支持，终身访问。*

*有问题吗？在文章的评论部分提到它们，我们会给你回复。*

这就把我们带到了关于 Python 字符串连接的这篇文章的结尾。