# 您需要了解的重要 Python 数据类型

> 原文：<https://www.edureka.co/blog/python-data-types/>

在 [Python 编程语言](https://www.edureka.co/blog/python-programming-language)中，一切都是对象。因此，数据类型被视为类，变量是这些类的实例或对象。Python 中有各种数据类型来表示值类型。在本文中，我们将了解不同的 Python 数据类型，以及如何按以下顺序将它们分配给变量:

*   [Python 数据类型](#python)
*   [Python 中的标准数据类型](#datatypes)
    *   [数字](#number)
    *   [列表](#list)
    *   [字符串](#string)
    *   [元组](#tuple)
    *   [字典](#dictionary)

我们开始吧。

## **![python- python data types - edureka](img/14c42aab2ee56b8f5a16db5eb14d7115.png) Python 数据类型**

[变量](https://www.edureka.co/blog/variables-and-data-types-in-python/)用于保存不同数据类型的值。因为 Python 是一种动态类型语言，所以在声明变量时不需要定义变量的类型。解释器将值与其类型隐式绑定。Python 使我们能够检查程序中使用的变量的类型。借助 type() [函数](https://www.edureka.co/blog/python-functions)，可以找出被传递变量的类型。

**举例:**

```
x = 24
y = 14.7
z = "Welcome to Edureka"
print(type(x));
print(type(y));
print(type(z));
```

**输出:**

```
<type 'int'>
<type 'float'>
<type 'str'>
```

## **Python 中的标准数据类型**

变量用于保存不同类型的值。例如，一个人的名字必须存储为字符串，而一个雇员的 ID 必须存储为整数。

Python 提供了各种标准数据类型，定义了每种数据类型的存储方法。Python 中的标准数据类型包括:

*   **数字**
*   [**弦**](https://www.edureka.co/blog/what-is-string-in-python/)
*   [**列表**](https://www.edureka.co/blog/lists-in-python/)
*   **元组**
*   **字典**

现在您已经了解了标准的 python 数据类型，让我们继续深入了解每一种数据类型。

### **数字**

Number 用于存储数值。当一个数字被赋给一个变量时，Python 创建数字对象。有 4 种类型的数值数据:

*   **int**–用于 12、2、7 等有符号整数。
*   **long**–该整数用于更大范围的值，如 908090800L，-0x1929292L 等。
*   **float**——用于存储浮点数，如 1.5、701.89、15.2 等。
*   **复数**–用于 2.14j、2.0 + 2.3j 等复数。

在 [Python](https://www.edureka.co/blog/python-programming-language) 中，可以对长整数使用小写 L。然而，使用大写字母 l 更方便。

**举例:**

```
a = 12
print(a, "is of type", type(a))

b = 5.05
print(b, "is of type", type(b))

c = 1+2j
print(c, "is complex number?", isinstance(1+2j,complex))
```

**输出:**

```
12 is of type <class 'int'>
5.05 is of type <class 'float'>
(1+2j) is complex number? True
```

### **字符串**

一个[字符串](https://www.edureka.co/blog/what-is-string-in-python/)被定义为一个用引号表示的字符序列。在 python 中，可以使用单引号、双引号或三引号来定义字符串。

python 中的字符串处理可以使用各种内置函数和[操作符](https://www.edureka.co/blog/operators-in-python/)来完成。在字符串处理的情况下，运算符+用于连接两个字符串。

**举例:**

```
str1 = 'Welcome to Edureka' #string str1
str2 = 'Python Programming' #string str2
print (str1[0:3])
print (str1[4])
print (str1 + str2)
```

**输出:**

```
Wel
c
Welcome to Edureka Python Programming
```

### **列表**

列表类似于 C 中的[数组，但是在 Python 中它可以包含不同类型的数据。列表中存储的项目用逗号(，)分隔，并用方括号[]括起来。](https://www.edureka.co/blog/arrays-in-c/)

您可以使用 slice [:]运算符来访问列表中的数据。串联运算符(+)类似于字符串中的运算符。

**举例:**

```
list = [20, "welcome", "edureka", 40]
print (list[3:]);
print (list);
print (list + list);
```

**输出:**

```
[40]
[20, 'welcome']
[20, "welcome", "edureka", 40]
[20, "welcome", "edureka", 40, 20, "welcome", "edureka", 40]
```

### **元组**

元组在许多方面类似于列表。像列表一样，[元组](https://www.edureka.co/blog/tuple-in-python/)也包含不同数据类型的项的集合。元组的各项用逗号(，)分隔，并用括号()括起来。

元组是只读数据结构，您不能修改元组中各项的大小和值。

**举例:**

```
tuple = ("welcome", "edureka", 40)
print (tuple[1:]);
print (tuple);
print (tuple + tuple);
```

**输出:**

```
('edureka', 40)
('welcome', 'edureka', 40)
('welcome', 'edureka', 40, 'welcome', 'edureka', 40)
```

### **字典**

字典是项目的键值对的有序集合。它就像一个关联数组或哈希表，其中每个键存储一个特定的值。键可以保存任何原始数据类型，而值是任意的 Python 对象。

字典中的条目用逗号分隔，并用大括号{}括起来。

**举例:**

```
dict = {1:'John', 2:'Rachel', 3:'Nancy', 4:'Daniel'};
print("1st name is "+dict[1]);
print (dict.keys());
print (dict.values());
```

**输出:**

```
1st name is John
[1, 2, 3, 4]
['John', 'Rachel', 'Nancy', 'Daniel']
```

这些是用于保存不同值的标准 python 数据类型。说到这里，我们的文章就到此为止了。

*现在，请查看 Edureka 提供的 **[Python 认证培训](https://www.edureka.co/python)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。* *Python 认证培训将帮助您获得定量分析、数据挖掘和数据呈现方面的专业知识，通过将您的职业转变为数据科学家角色来超越数字。*

有问题要问我们吗？请在“Python 数据类型”的评论部分提到它，我们会回复您。