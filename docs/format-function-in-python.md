# Python 中的 Format 函数是什么，是如何工作的？

> 原文：<https://www.edureka.co/blog/format-function-in-python/>

Python 中的 Format 函数( **str.format()** )是字符串类的技术，允许你尝试做变量替换和数据格式化。它使您能够通过点数据格式以所需的间隔连接字符串的各个部分。这篇文章将引导你了解在 [Python](https://www.edureka.co/blog/python-tutorial/) 中格式化程序的一些常见用法，这将有助于你的代码和程序对用户友好。

以下是这里讨论的所有要点:

*   [单一格式化程序](#SingleFormatter)
*   [多重格式化程序](#MultipleFormatter)
*   [使用位置和关键字参数的格式化程序](#FormattersusingPositionalandKeywordArguments)
*   [型号规格](#TypeSpecification)
*   [使用格式化程序](#SpacingandAlignmentsusingformatter)进行间距和对齐
*   [组织数据](#Organizing%20data)

让我们开始吧:)

## **1)单一格式化程序:**

格式化程序的工作方式是将一个或多个由一对花括号 **"{}"** "括起来的替换字段或占位符固定成一个字符串，并调用 str.format()技术。您需要向 format()方法传递希望与字符串连接的值。运行程序时，该值将打印在占位符{}所在的位置。单格式器可以定义为只有一个占位符的格式器。在下面的示例中，您将能够看到 print 语句中格式的实现。

除了在 [print 语句中直接使用](https://www.edureka.co/blog/print-in-python/)之外，我们还可以使用 format()对变量:

**举例:**

```
print("{} is a good option for beginners in python".format("Edureka"))

```

**输出:** Edureka 对于 python 初学者来说是个不错的选择

除了在打印语句中直接使用，我们还可以对变量使用 format():

**例如:**

```
my_string = "{} is a good option for beginners in python"
print(my_string.format("Edureka"))

```

**输出:** Edureka 对于 python 初学者来说是个不错的选择

## **2)多重格式化程序:**

假设在一个句子中需要另一个变量替换，这可以通过在需要替换的地方添加另一组花括号并向 format()传递第二个值来实现。然后 Python 会用作为参数传递的值来替换占位符。

**举例:**

```
my_string = "{} is a good option for beginners in {}"
print(my_string.format("Edureka","Machine Learning"))

```

**输出:** Edureka 是初学者在[机器学习](https://www.edureka.co/blog/machine-learning-and-big-data/) 中的一个很好的选择

您可以根据需要在给定变量中添加任意数量的占位符或花括号，并为格式()添加相同数量的输入。

**例如:**

```
my_string = "{} is an {} option for {} in {}"
print(my_string.format("Edureka","excellent","experienced","Machine Learning"))

```

**输出:** 对于有机器学习经验的人来说，Edureka 是一个极好的选择

因此，继续使用 Python 中的格式函数

## **3)使用位置和关键字参数的格式化程序:**

当占位符为空{}时，Python 解释器将通过 str.format()按顺序替换这些值。

str.format()方法中存在的值主要是 [tuple](https://www.edureka.co/blog/tuple-in-python/) ( **“一个 tuple 是一个不可变的 Python 对象序列”** ) [数据类型](https://www.edureka.co/blog/python-data-types/)，tuple 中包含的每一个单独的项通常由它的索引号引用，索引号从零开始。然后，这些索引号被传递到原始字符串中的花括号中。

您可以使用花括号中的位置参数或索引号，以便将特定值从格式()中获取到变量中:

**举例:**

```
my_string = "{0} is a good option for beginners in {1}"
print(my_string.format("Edureka","Machine Learning"))

```

**输出:** Edureka 对于机器学习初学者来说是一个很好的选择

关键字参数通过调用花括号内的变量名来帮助调用 format()中的变量:

**举例:**

```
my_string = "{0} is a good option for beginners in {domain}"
print(my_string.format("Edureka",domain = "Machine Learning"))

```

**输出:** Edureka 对于机器学习初学者来说是一个很好的选择

我们可以同时使用关键字和位置参数:

**举例:**

```
my_string = "{domain} is a good option for beginners in {0}"
print(my_string.format("Edureka",domain = "Artificial Intelligence"))

```

**输出:**

my_string = "{domain}对于{0}" 的初学者来说是个不错的选择

print(my _ string . format(" edu reka "，domain = "人工智能"))

[人工智能](https://www.edureka.co/blog/top-15-hot-artificial-intelligence-technologies/)对于 Edureka 的初学者来说是一个不错的选择

## **4)型号规格:**

通过使用格式代码语法，我们的语法的花括号中包含了更多的参数。在这个语法中，无论 field_name 在哪里，它都指定了参数或关键字对 str.format()技术的指示符，而 conversion 指的是数据类型的转换代码。一些转换类型包括:

s-字符串

d–十进制整数(以 10 为基数)

f–浮动

c-字符

b–二进制

o-八进制

x–16 进制，9 后面有小写字母

e–指数符号

**举例:**

```
my_string = "The Temperature in {0} today is {1:d} degrees outside!"
print(my_string.format("Vizag",22))

```

**输出:** 今天维扎格的室外温度是 22 度！

确保使用正确的转换。如果您使用不同的转换代码，将会出现以下错误:

**举例:**

```
my_string = "The Temperature in {0} today is {1:d} degrees outside!"
print(my_string.format("Vizag",22.025))

```

**输出:**

————————————————————————————

值错误回溯(最近一次调用最后一次)

<ipython-input-12-4 ce 31 DC 07 a 23>在<模块>

1 my_string = "今天{0}的温度是室外{1:d}度！"

——>2 打印(my_string.format("Vizag "，22.025))

值错误:类型为“float”的对象的未知格式代码“d”

您甚至可以限制浮点整数中的小数位数:

**例如:**

```
my_string = "The Temperature in {0} today is {1:.2f} degrees outside!"
print(my_string.format("Vizag",22.025))

```

**输出:** 维扎格今天外面气温 22.02 度！

## **5)使用格式化程序的间距和对齐:**

我们可以使用 format()将空格或对齐方式应用到占位符的右侧、左侧或两侧。对齐代码是:

:左对齐文本

^:居中文本

> :右对齐

**举例:**

```
my_string = "The Temperature in {0:20} today is {1:d} degrees outside!"
print(my_string.format("Vizag",22))

```

**输出:** 今天维扎格的室外温度是 22 度！

**举例:**

```
my_string = "The Temperature in {0} today is {1:20} degrees outside!"
print(my_string.format("Vizag",22))

```

****输出:****

今天维扎格的室外温度是 22 度！

我们可以看到字符串是左对齐的，数字是右对齐的。通过使用 format()，我们可以改变以下两种情况:

**例如:**

```
my_string = "The Temperature in {0:>20} today is {1:d} degrees outside!"
print(my_string.format("Vizag",22))

```

**输出:**

今天维扎格的室外温度是 22 度！

## **6)组织数据:**

我们倾向于在 Excel 表中组织数据，我们可以用各种方法调整列的大小，但是我们如何在程序中应用同样的东西，一列中的值以指数方式递增，一列中的项目进入另一列，或者最终用户可能会发现很难理解哪个值属于哪个列。

## **举例:**

```
for i in range(4,15):
	print(i,i*i,i*i*i)

```

**输出:**

4 16 645 25 1256 36 2167 49 3438 64 5129 81 72910 100 100011 121 1331

在这里，我们可以使用 format()来定义每一列之间的间距，以便最终用户可以轻松地区分不同列的值。

**举例:**

```
for i in range(4,15):
	print("{:6d} {:6d} {:6d}".format(i,i*i,i*i*i))

```

## 输出:

4 16 645 25 1256 36 2167 49 3438 64 5129 81 72910 100 100011 121 133112 144 172813 169 219714 196 2744

从上面的使用中，我们可以说，用于变量替换的格式化程序是连接字符串、转换值、组织值和数据的有效方法。格式化程序代表了一种简单但非描述性的方式，用于将变量替换传递到字符串中，并有助于创建可理解且用户友好的输出。今天就加入我们的[Python 编程大师](https://www.edureka.co/masters-program/python-developer-training)课程，成为一名专家。

这就把我们带到了这篇关于 Python 中格式函数的文章的结尾。我希望你清楚已经与你分享的一切。 ***确保你尽可能多的练习，恢复你的经验。***

*有问题吗？请在这篇“Python 中的格式函数”博客的评论部分提到它，我们会尽快回复您。*

*要深入了解任何趋势技术及其各种应用，您可以注册参加现场 **Edureka 的 [Python 在线培训](https://www.edureka.co/python-programming-certification-training)** ，全天候支持，终身访问。*