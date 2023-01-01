# Python 中的字符串切片:您需要知道的一切

> 原文：<https://www.edureka.co/blog/string-slicing-in-python/>

切片是 [Python](https://www.edureka.co/blog/python-tutorial/) 中一个很酷的特性。就像其他编程语言一样，python 也使我们能够通过使用类似数组的索引语法技术来访问字符串中的单个字符。在本文中，我们将了解 Python 中的字符串切片:

*   [什么是切片？](#what)
*   [Python 中的字符串切片](#code)
*   [切一个带负索引的字符串](#negative)
*   [在元组和列表中实现的切片概念](#tuples)

## **什么是切片？**

切片的主要方面是切片函数。它允许程序员从一串数据中提取信息。在这篇文章中，我们可以有机会观察到许多这样做的方法。切片不仅限于字符串，还可以应用于元组和列表。

![String Slicing in Python](img/dcc6150d1b8a9a4bd7be28059168a270.png)

python 中的切片是从主字符串中派生出一个子字符串。考虑下面的代码示例:

## **Python 中的字符串切片**

```
print("nWelcome to Edurekan")
String1=input("Enter string of your choice = " )
print("nn The output is = n")
print(String1[slice(0,3)])
print("nThank you! have a nice day ") 

```

在下面的例子中，“ICC WORLDCUP”是一个字符串，它是用户输入的。程序派生的子串是“ICC”。这是怎么发生的？负责此功能的主语句是 slice 函数的索引，它从索引 0 (起始索引)中挑选字符，并一直到索引 2。在[0，3]的范围内，字母 ICC 成为一个新的字符串，这是输出。

## **对索引为负的字符串进行切片**

另一种切片方式是关于负指数。这也是子串反转的好方法。字符串切片函数的参数增加到 3。第一个是从字符串末尾开始的起始索引，第二个是结束索引，第三个是间隔。让我们看一看。

```
print("nWELCOME TO EDUREKA n")
String1=input("Enter string of your choice =")
print("n nThe output is = n")
print(String1[slice(-1,-5,-1)])
print("nThank You ! Have a nice day")
```

在' slice '函数中，第一个-1 指向字符串的最后一个字母“M”。光标以 1 为间隔向后计数，并在 4 个计数后停止，这导致输出“MARG ”,即最后 4 个字母“GRAM”被反转。

## **在元组和列表中实现的切片概念**

在下面的代码示例中。我们看到列表和元组包含 EDUREKA 的字母等元素。其中每一个的起始索引都是零。前三个索引[0、1 和 2]指的是字母 E、D 和 u。因此，slice 函数提取前三个。

这个值 3 存储在一个变量中，在列表中传递并打印出来。当我们看代码的第二部分时，我们看到考虑了一个间隔。因此，每隔一个索引就对列表和元组进行一次索引。

```
List1 = ['E', 'D', 'U', 'R', 'E', 'K', 'A']
Tuple1 = ('e', 'd', 'u', 'r', 'e', 'k', 'a')
Obj = slice(3) print("nThe Output is n")
print(List1[Obj]) Obj = slice(1, 5, 2)
print("nThe output is n")
print(Tuple1[Obj])
```

## **用元组和列表中的负索引实现的切片概念**

这里，代码的功能保持不变，只是元素的选择方式相反。当我们谈论字符串中的负索引时，它总是指从末尾选择它的字符串元素。让我们看一看。同样的事情在后半段也可以看到，在后半段进行了反转，但是考虑到了音程。

```
List1 = ['E', 'D', 'U', 'R', 'E', 'K', 'A']
Tuple1 = ('e', 'd', 'u', 'r', 'e', 'k', 'a') 
Obj = slice(-1, -5, -1) print("nThe output list isn")
print(List1[Obj])
Obj = slice(-1, -6, -2)
print("nThe output tuple isn")
print(Tuple1[Obj])
```

至此，我们结束了 Python 中的字符串切片。 *要深入了解 Python 及其各种应用，您可以 [**在此**](https://www.edureka.co/python/) 注册参加在线直播培训，全天候支持，终身访问。*

*有问题吗？请在“Python 中的字符串切片”的评论部分提及它们，我们会尽快回复您。*