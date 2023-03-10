# 关于 Python 中的 Substring，您需要了解的一切

> 原文：<https://www.edureka.co/blog/substring-in-python/>

[字符串](https://www.edureka.co/blog/what-is-string-in-python/)是一系列 Unicode 字符。字符串由一系列或一系列可能包含字母数字和特殊字符的字符组成。在本文中，我们将理解 [python](https://www.edureka.co/blog/python-tutorial/) 中的 substring，以及它是如何以如下方式工作的:

*   [Python 中的子串是什么？](#what)
*   [在 Python 中切片字符串](#slicing)
*   [验证一个子字符串是否存在于另一个字符串中](#validate)

## **Python 中的子串是什么？**

在 python 中，substring 是另一个字符串中的字符序列，在 python 中，它也被称为字符串切片。

![](img/9237382b5a654190a0eb054f2ddc40b1.png)

## **在 Python 中切片字符串**

*   使用起始索引和结束索引进行切片

`s= s[ startIndex : endIndex]`

请注意:索引在字符串中从 0 开始。

*   使用起始索引而不使用结束索引进行切片

`s= s[ startIndex :]`

```
# Slicing or substring using start, without end index
s= 'This is to demonstrate substring functionality in python.'
s[5:]
Output : 'is to demonstrate substring functionality in python.'
```

从从索引位置 5 开始到字符串末尾的字符串中返回一个切片字符串。

*   使用结束索引而没有开始索引的切片

s= s[: endIndex]

```
# Slicing or substring without start index
s= 'This is to demonstrate substring functionality in python.'
s[:7]
Output: 'This is'
```

返回从开始到结束的切片字符串-index-1。

*   切片完整字符串

`s= s[:]`

```
# Slicing or substring without start or end index
s= 'This is to demonstrate substring functionality in python.'
s[:]
Output: 'This is to demonstrate substring functionality in python.'
```

返回完整的字符串。

*   从字符串中截取单个字符

`s= s[index]`

```
# Slicing or substring single character
s= 'This is to demonstrate substring functionality in python.'
s[9]
Output: ‘o’
```

返回单个字符。

使用起始索引、结束索引和步进进行切片

s= s[startIndex : endIndex: step]

```
# Slicing or substring with start-index, end-index and step.
s= 'This is to demonstrate substring functionality in python.'
s[12:22:1]
Output: ‘emosntrate’
```

当步长为 1 时，它类似于普通切片。

```
# Slicing or substring with start-index, end-index and step.
s= 'This is to demosntrate substring functionality in python.'
s[12:22]
Output: ‘emosntrate’
```

当步长为 2 时，它以 2 为步长进行切片

```
# Slicing or substring with start-index, end-index and step.
s= 'This is to demonstrate substring functionality in python.'
s[12:22:2]
Output: ‘eonrt’
```

例如，步长为 1 的切片字符串是 **emosntrate**

步长为 2 的切片串是e**m**o**s**n**t**r**a**te，显示步长为 2 的切片。

类似地，对于步长 3，在 e 将是 e **mo** s **nt** r

```
# Slicing or substring with start-index, end-index and step.
s= 'This is to demonstrated substring functionality in python.'
s[12:22:3]
Output: ‘esre’
```

*   使用负步长反转字符串

```
# Reverse a string using Slicing or substring with negative step.
s= 'This is to demonstrated substring functionality in python.'
s[::-1]
Output: ‘.nohtyp ni ytilanoitcnuf gnirtsbus etartnsomed ot si sihT’
```

使用负步进

![Substring in Python](img/acc81f75b370193225a85bbc421978f8.png)

字符串中的索引从 0 到 5，或者我们也可以使用负索引。

```
# Slicing or substring a string using negative index.
s= 'PYTHON'
s[0:-3]
Output: ‘PYT’
```

*   也可以使用正索引对相同的字符串进行切片

```
# Slicing or substring a string using positive index.
s= 'PYTHON'
s[0:3]
Output: ‘PYT’
```

*   使用列表理解检索所有子字符串

```
# Get all substrings of string using list comprehension and string slicing 
s= 'PYTHON'
str=[s[i: j]
for i in range(len(s)) 
      for j in range(i + 1, len(s) + 1)] 
print (str)

Output: ['P', 'PY', 'PYT', 'PYTH', 'PYTHO', 'PYTHON', 'Y', 'YT', 'YTH', 'YTHO', 'YTHON', 'T', 'TH', 'THO', 'THON', 'H', 'HO', 'HON', 'O', 'ON', 'N']
```

*   使用`itertools.combinations()`方法检索所有子字符串

```
# Get all substrings of string using list comprehension and string slicing 
s= 'PYTHON'
str=[s[i: j]
for i in range(len(s)) 
     print (str)

Output: ['P', 'PY', 'PYT', 'PYTH', 'PYTHO', 'PYTHON', 'Y', 'YT', 'YTH', 'YTHO', 'YTHON', 'T', 'TH', 'THO', 'THON', 'H', 'HO', 'HON', 'O', 'ON', 'N']
```

## **验证一个子字符串是否存在于另一个字符串中**

*   使用 in 运算符

```
# Check if string is present within another string using in operator
s= 'This is to demonstrated substring functionality in python.'
print("This" in s)
print("Not present" in s)

Output: 
True
False
```

如果一个子字符串存在于另一个字符串中，In 运算符将返回 true，否则将返回 false。

*   使用查找方法

```
# Check if string is present within another string using find method
s= 'This is to demonstrated substring functionality in python.'
print(s.find("demonstrate"))
print(s.find("Not present")) 

Output: 
11
-1
```

如果一个子字符串存在于另一个字符串中，Find 方法将打印索引，否则如果一个字符串不存在，将返回-1。

至此，我们结束了 Python 文章中的这个子串。我希望您对切片有所了解，并且知道它如何帮助您在 python 中创建不同类型的子字符串。

*要深入了解 Python 及其各种应用，您可以立即注册参加在线直播的 [Python 培训](https://www.edureka.co/python-programming-certification-training)，该培训提供全天候支持和终身访问。*