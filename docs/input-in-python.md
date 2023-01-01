# Python 中的输入简介

> 原文：<https://www.edureka.co/blog/input-in-python>

[//www.youtube.com/embed/qJjyVW5xNPs](//www.youtube.com/embed/qJjyVW5xNPs)

## **从键盘获取用户输入**

python 中有两个函数可用于从用户处读取数据或输入:raw_input()和 input()。结果可以存储在一个变量中。

**raw _ input()**–它读取输入或命令并返回一个字符串。

**input()**–读取输入并返回一个 python 类型，如 list、tuple、int 等。

## **例如**

```
name =    raw_input (“what is your name?    
”)   #  return type of raw input is always string
age =    input (“what is your age 
”)  #  This can be different from string
print  “user entered name as:    ”  +  name
print  “The type of the name is:   ”,
print   type (name)
print   “user entered age as:    ”  +  str (age)
print   “The type of age is:   ”,
print   type (age)
```

**运行后赋值:**

你叫什么名字？

字母表

你多大了？

Twenty-one

**它将给出如下结果:**

用户输入的名称为:abc

名称的类型为:

用户输入的年龄为:21

年龄的类型为:

输入时，上面没有给出数据的类型。Name 采用字符串类型，而 age 采用整数类型 Python。基本上，raw_input 和 input 的区别在于，raw_input 的返回类型始终是 string，而 input 的返回类型不必仅仅是 string。Python 将判断哪种数据类型最适合它。如果你输入了一个数字，它会把它作为一个整数。但是如果它是 raw_input，那么它肯定是 string。

注意:每当你写很多代码时，最好把它写在一个 ide 中，因为它非常有用。如果你没有得到适当的缩进，它会直接显示错误。如果您也有任何问题，在 PyCharm 或您可能想使用的任何其他 IDE 中进行调试是非常容易的。

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子**

[Python 中命令行参数](https://www.edureka.co/blog/command-line-arguments-in-python "Command Line Arguments in Python")

[Python 101:Hello World 程序](https://www.edureka.co/blog/python-101-hello-world-program/ "Python 101: Hello World Program")

[开始您的 Python 大数据分析培训](https://www.edureka.co/data-science-python-certification-course)