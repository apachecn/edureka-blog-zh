# Python 简介——关于 Python 你需要知道的一切

> 原文：<https://www.edureka.co/blog/introduction-to-python/>

随着人工智能、机器学习和数据科学的应用，IT 行业正在蓬勃发展。随着新时代的应用，对 python 开发者 T2 的需求也增加了。易于访问和可读性使 python 成为当今最流行的编程语言之一。现在是切换到 python 并释放 python 编程带来的无限可能性的时候了。这篇介绍 python 的文章将向您介绍 python 编程的基础和基本概念。

在本文中，我将向您介绍 python。以下是本博客将涉及的主题:

*   [Python 简介](#a)
*   [关键词&标识符](#b)
*   [变量&数据类型](#c)
*   [操作员](#d)
*   [Python 中的循环](#e)
*   [功能](#f)
*   [阶级&对象](#g)
*   [哎呀概念](#h)
*   [异常处理](#i)
*   [文件处理](#j)

## **Python 简介**

Python 是一种通用编程语言。它非常容易学习，简单的语法和可读性是开发者从其他编程语言转向 python 的原因之一。

我们可以使用 python 作为面向对象和面向过程的语言。它是开源的，有大量用于各种实现的库。

![features-introduction to python-edureka](img/b1404f18dcabc5190aa349992d4357df.png)

python 是一种高级解释语言，最适合编写自动化和代码重用的 Python 脚本。

它由 Guido Van Rossum 于 1991 年创建。它的名字来源于名为“巨蟒剧团”的喜剧系列。

![Guido Van Rossum - Introduction to python - Edureka](img/dc880d8f3731b35f3c86eb73055dc93f.png)使用 python 给了我们无限的可能性。我们可以在数据科学中使用[python](https://www.edureka.co/blog/learn-python-for-data-science/)、[机器学习](https://www.edureka.co/blog/scikit-learn-machine-learning/)、[人工智能](https://www.edureka.co/blog/deep-learning-with-python/)、 [web 开发](https://www.edureka.co/blog/django-tutorial/)、[软件开发](https://www.edureka.co/blog/tkinter-tutorial/)等。

![applications of python-introduction to python-edureka](img/6265907ee003fec085829f3fa97d5e4f.png)

为了使用任何编程语言，你必须熟悉 IDE。您可以在“python.org”上找到 python IDE 的安装程序，并将其安装到您的系统上。安装看起来很简单，并且附带了编写 python 程序的 IDLE。

![installation-introduction to python-edureka](img/2e195d3826ee5d951a3ff0dacd66a2fd.png)

在你的系统上安装了 python 之后，你就可以用 python 编程语言编写程序了。

让我们从关键字和标识符的 python 介绍开始。

## **关键词&标识符**

关键字不过是 python 中已经存在的特殊名称。在编写 python 程序时，我们可以将这些关键字用于特定的功能。

以下是我们在 python 中拥有的所有关键字的列表:

![keywords-introduction to python-edureka](img/74668e14c59047429230892db3cdb22b.png)

```

import keyword
keyword.kwlist
#this will get you the list of all keywords in python.
keyword.iskeyword('try')
#this will return true, if the mentioned name is a keyword.

```

标识符是用户定义的名称，我们用来表示变量、类、函数、模块等。

```
name = 'edureka'
my_identifier = name

```

## **变量&数据类型**

变量就像一个存储位置，你可以在那里存储一个值。这个值，你以后可能改也可能不改。

```
x = 10
y = 20
name = 'edureka'

```

到 在 python 中声明一个变量，你只需要给它赋值。在 python 中声明变量不需要额外的命令。

### **Python 中的数据类型**

1.  数字
2.  字符串
3.  列表
4.  字典
5.  设置
6.  元组

### **数字**

Numbers 或 numeric 数据类型用于数值。我们有 4 种数值数据类型。

```
#integers are used to declare whole numbers.
x = 10
y = 20
#float data types is used to declare decimal point values
x = 10.25
y = 20.342
#complex numbers denote the imaginary values
x = 10 + 15j
#boolean is used to get categorical output
num = x < 5
#the output will be either true or false here.

```

### **弦**

字符串数据类型用来表示字符或字母。您可以使用单引号或双引号""来声明字符串。

```
name = 'edureka'
course = "python"

```

要访问字符串中的值，我们可以使用索引。

```
name[2]
# the output will be the alphabets at that particular index.

```

### **列表**

python 中的 List 就像一个集合，可以存储不同的值。它不必是一致的，可以有不同的值。

列表是有索引的，也可以有重复值。要声明一个列表，你必须使用方括号。

```
my_list = [10, 20, 30, 40, 50, 60, 'edureka', 'python']
print(my_list)

```

为了访问列表中的值，我们使用索引，下面是一些可以在列表上执行的操作:

*   追加
*   清除
*   复制
*   计数
*   延长
*   插入
*   砰然一声
*   反转
*   移除
*   排序

下面是使用列表进行一些操作的代码:

```
a = [10,20,30,40,50]
#append will add the value at the end of the list
a.append('edureka')
#insert will add the value at the specified index
a.insert(2,'edureka')
#reverse will reverse the list
a.reverse()
print(a)
#the output will be
['edureka', 50, 40, 30, 'edureka', 20, 10]

```

### **字典**

字典是无序和可变的，我们在字典中使用键值对。因为键是惟一的，所以我们可以用它们作为索引来访问字典中的值。

以下是您可以对字典执行的操作:

*   清除
*   复制
*   来自按键
*   获取
*   项
*   键
*   砰然一声
*   getitem
*   setdefault
*   更新
*   值

```
my_dictionary = { 'key1' : 'edureka' , 2 : 'python'}
mydictionary['key1']
#this will get the value 'edureka'. the same purpose can be fulfilled by get().
my_dictionary.get(2)
#this will get the value 'python'.

```

### **元组**

Tuple 是另一种有序且不可改变的集合。我们用圆括号声明 python 中的元组。 以下是您可以对元组执行的操作:

*   计数
*   索引

```
mytuple = (10,20,30,40,50,50,50,60)
mytuple.count(40)
#this will get the count of duplicate values.
mytuple.index(20)
#this will get the index for the vale 20.

```

### **设定**

集合是一个无序且无索引的集合。集合也没有任何重复的值。以下是您可以在器械组上执行的一些操作:

*   添加
*   复制
*   清除
*   差异
*   差异 _ 更新
*   丢弃
*   路口
*   交集 _ 更新
*   工会
*   更新

```
myset = { 10 ,20,30,40,50,60,50,60,50,60}
print(myset)
#there will be no duplicate values in the output

```

在任何编程语言中，运算符的概念都起着至关重要的作用。让我们来看看 python 中的运算符。

## **操作员**

python 中的运算符用来做两个值或变量之间的运算。下面是 python 中不同类型的操作符:

*   算术运算符
*   逻辑运算符
*   赋值运算符
*   比较运算符
*   隶属运算符
*   身份运算符
*   按位运算符

### **算术运算符**

算术运算符用于在两个值或变量之间进行算术运算。

![arithmetic operaotrs-introduction to python-edureka](img/c22492f16b576cd5395ae78e27727fe7.png)

```
#arithmetic operators examples
x + y
x - y
x ** y

```

### **赋值运算符**

赋值运算符用于给变量赋值。

![](img/5b7da3908751338d89ee52d8800763aa.png)

### **逻辑运算符**

逻辑运算符用于比较 python 中的条件语句。

**![](img/3518a374dbfc0aa1d3428a87d2019705.png)**

### **比较运算符**

比较运算符用于比较两个值。

![](img/0ab62f15c23ff079f9e0adaef2604b24.png)

### **会员操作符**

成员运算符用于检查一个序列是否存在于一个对象中。

![](img/0f7b4d84c8812cbedd01c20162320a90.png)

### **身份符**

恒等运算符用于比较两个对象。

![](img/03c899879e192f59d9ff64ed48d8cc4b.png)

### **按位运算符**

位运算符用于比较二进制值。

![](img/e8cbffc172f3d92727f2c3510c669637.png)

现在我们已经理解了 python 中的操作符，让我们来理解 python 中循环的概念以及我们为什么使用循环。

## **Python 中的循环**

循环允许我们多次执行一组语句。为了理解[我们为什么使用循环](https://www.edureka.co/blog/loops-in-python/)，让我们举个例子。

假设你想打印所有偶数的和，直到 1000。如果你不使用循环来编写这个任务的逻辑，这将是一个漫长而令人厌倦的任务。

但是如果我们使用循环，我们可以写出寻找偶数的逻辑，给出一个条件迭代直到数达到 1000 并打印出所有数的和。这将降低代码的复杂性，并使其可读性更好。

python 中有以下几种循环:

1.  为循环
2.  while 循环
3.  嵌套循环

### **为循环**

A‘for 循环’用于每次迭代执行一次语句。我们已经知道将要执行的迭代次数。

![](img/92a0979ccc2e4f63be223e85c264db5b.png)

一个 for 循环有两个块，一个是我们指定条件的地方，另一个是我们指定语句的主体，它在每次迭代中被执行。

```
for x in range(10):
    print(x)

```

### **而循环**

只要条件为真，while 循环就会执行语句。我们在循环开始时指定条件，一旦条件为假，执行就会停止。

![](img/28b024f9e68675fe8eb38046122af6d2.png)

```
i = 1
while i < 6:
     print(i)
     i += 1
#the output will be numbers from 1-5.

```

### **嵌套循环**

嵌套循环是循环的组合。如果我们将 while 循环合并到 for 循环或 vis-a-vis 中。

后面是一些嵌套循环的例子:

```
for i in range(1,6):
   for j in range(i):
       print(i , end = "")
   print()
# the output will be
1
22
333
4444
55555

```

### **条件和控制语句**

python 中的条件语句支持 python 中逻辑语句的通常逻辑。

后面是 python 中的条件语句:

1.  如果
2.  elif
3.  否则

**如果陈述**

```
x = 10
if x > 5:
   print('greater')

```

if 语句测试条件，当条件为真时，执行 if 块中的语句。

**elif 语句**

```
x = 10
if x > 5:
   print('greater')
elif x == 5:
     print('equal')
#else statement

x =10
if x > 5:
   print('greater')
elif x == 5:
     print('equal')
else:
     print('smaller')

```

当 if 和 elif 语句都为假时，执行将移至 else 语句。

### **控制语句**

控制语句用来控制程序中的执行流程。

跟在后面的是 python 中的控制语句:

1.  突破
2.  继续
3.  通过

**破**

```

name = 'edureka'
for val in name:
    if val == 'r':
       break
    print(i)
#the output will be
e
d
u

```

一旦循环遇到中断，执行就会停止。

**继续**

```

name = 'edureka'
for val in name:
    if val == 'r':
       continue
    print(i)
#the output will be
e
d
u
e
k
a

```

当循环遇到 continue 时，当前迭代被跳过，其余迭代被执行。

**过关**

```
name = 'edureka'
for val in name:
    if val == 'r':
       pass
    print(i)

#the output will be
e
d
u
r
e
k
a

```

pass 语句是一个空操作。这意味着该命令在语法上是必需的，但是您不希望执行任何命令或代码。

现在我们已经完成了 python 中不同类型的循环，让我们来理解 python 中函数的概念。

## **功能**

python 中的函数是一段代码，无论何时被调用都会执行。我们也可以在函数中传递参数。为了理解函数的概念，让我们举一个例子。

假设你想计算一个数的阶乘。只需执行计算阶乘的逻辑就可以做到这一点。但是如果你一天要做十次呢，一遍又一遍地写同样的逻辑将会是一个漫长的任务。

相反，你能做的是，把逻辑写在一个函数里。每当你需要计算阶乘的时候就调用这个函数。这将降低代码的复杂性，并节省您的时间。

### **如何创建函数？【T2**

```
# we use the def keyword to declare a function

def function_name():
#expression
    print('abc')

```

### **如何调用函数？**

```
def my_func():
    print('function created')

#this is a function call
my_func()

```

### **功能参数**

我们可以使用参数在函数中传递值。我们也可以在函数中使用给定参数的默认值。

```
def my_func(name = 'edureka'):
    print(name)

#default parameter

my_func()
#userdefined parameter
my_func('python')

```

**λ函数**

一个 lambda 函数可以接受尽可能多的参数，但是有一个问题。它只能有一个表达式。

```

# lambda argument: expressions
lambda a,b : a**b
print(x(2,8))
#the result will be exponentiation of 2 and 8.

```

既然我们已经理解了函数调用、参数以及我们为什么使用它们，让我们来看看 python 中的类和对象。

## **阶级&对象**

### **什么是类？**

类就像是创建对象的蓝图。我们可以在一个类中存储各种方法/函数。

```

class classname:
      def functionname():
          print(expression)

```

### **什么是物体？**

我们创建对象来调用类中的方法，或者访问类的属性。

```

class myclass:
     def func():
         print('my function')

#<span style="color: #ff6600;">creating</span> an object

ob1 = myclass()

ob.func()

```

### **__init__ 函数**

这是一个内置函数，当一个类被初始化时被调用。所有的类都有 __init__ 函数。我们使用 __init__ 函数将值赋给对象或创建对象时需要的其他操作。

```

class myclass:
      def __init__(self, name):
          self.name = name
ob1 = myclass('edureka')
ob1.name
#the output will be- edureka

```

现在我们已经理解了类和对象的概念，让我们看看 python 中的一些概念。

## **哎呀概念**

Python 可以作为一种面向对象的编程语言。因此，我们可以在 python 中使用以下概念:

1.  抽象
2.  封装
3.  继承
4.  多态性

### **抽象**

数据抽象是指只显示必要的细节，隐藏后台任务。python 的抽象类似于任何其他编程语言。

就像我们打印报表时，我们不知道后台发生了什么。

### **封装**

封装是对数据进行包装的过程。在 python 中，类可以是封装的一个例子，其中成员函数和变量等被包装到一个类中。

### **传承**

继承是一个面向对象的概念，其中子类继承父类的所有属性。下面是 python 中的继承类型:

1.  单一继承
2.  多重继承
3.  多级继承

### **单继承**

在单一继承中，只有一个子类继承父类的属性。

```

class parent:
     def printname(name):
         print(name)

class child(parent):
      pass
ob1 = child('edureka')
ob1.printname

```

### **多重继承**

在多重继承中，我们有两个父类和一个继承两个父类属性的子类。

### **多级继承**

在多级继承中，我们有一个继承父类属性的子类。同一个子类充当另一个子类的父类。

### **多态性**

多态性是一个对象可以以多种形式使用的过程。最常见的例子是当父类引用被用来引用子类对象时。

我们已经理解了 python 中的 oops 概念，让我们来理解 python 中的异常和异常处理的概念。

## **打赏处理**

当我们编写程序时，如果出现错误，程序就会停止。但是我们可以使用 python 中的 **try，except，finally** 块来处理这些错误/异常。

当错误发生时，程序不会停止并执行 except 块。

```

try:
    print(x)
except:
       print('exception')

```

### **最后**

当我们指定一个 finally 块时。即使有错误或者 try except 块没有引发错误，它也会被执行。

```
try :
    print(x)

except:
      print('exception')
finally:
      print('this will be executed anyway')

```

既然我们已经理解了异常处理的概念。让我们看看 python 中的文件处理概念。

## **文件处理**

文件处理是 python 编程语言的一个重要概念。Python 有各种函数来创建、读取、写入、删除或更新文件。

### **创建文件**

```
import os
f = open('file location')

```

### **看文件**

```
f = open('file location', 'r')
print(f.read())
f.close()

```

### **追加一个文件**

```
f = open('filelocation','a')
f.write('the content')
f.close()
f = open('filelocation','w')
f.write('this will overwrite the file')
f.close()

```

### **删除一个文件**

```
import os
os.remove('file location')

```

这些都是我们在 python 中可以执行的文件处理功能。

我希望这篇介绍 python 的博客能帮助你学习 python 编程语言入门所需的所有基本概念。

当你使用 python 编程语言时，这将非常方便，因为这是学习任何编程语言的基础。一旦你掌握了 python 的基本概念，你就可以开始成为 python 开发者了。要深入了解 python 编程语言，您可以[在此](https://www.edureka.co/data-science-python-certification-course)注册**在线直播 python 培训**，全天候支持，终身访问。

*有什么疑问吗？你可以在评论中提到它们，我们会给你回复。*