# 如何使用 Python 将字符串转换为整数

> 原文：<https://www.edureka.co/blog/string-to-integer/>

在本主题中，我们将学习如何使用和不使用内置数据类型将字符串转换为整数。我们知道，字符串是用引号括起来的按顺序排列的字符的集合，整数是没有小数点的数字，也没有任何类型的引号。

![String to integer python](img/84d1f1f76a98d2e134707249e460b723.png)

但是当问题涉及到如何将一种数据类型转换成另一种数据类型时，Python 提供了一种简单的方法来相互转换。在这种情况下，我们看到如何按照以下顺序将字符串转换为整数:

*   [使用内置数据类型](#inbuilt)
*   [常规方式](#conventional)

**使用内置数据类型**

假设当我出于某种原因接受用户的输入时，Python 接受它并将其作为字符串本身返回。换句话说，即使有人键入一个数字作为输入，Python 也会将其作为字符串返回。

```
name = input(" What is your name : ")
print(name)
print(type(name))

age = input("What is your age : ")
print(age)
print(type(age))
```

**输出:**

`What is your name : Tyra`

`Tyra`

`<class 'str'>`

`What is your age : 20`

`20`

`<class 'str'>`

所以你看，作为输入的姓名和年龄的类型是‘String’。

现在，假设我们想给年龄加 5，我们将做如下操作:

```
name = input(" What is your name : ")
print(name)
print(type(name))

age = input("What is your age : ")
print(age)
print(type(age))

print(age+5)
```

**输出:**

`What is your name : Tyra`

`Tyra`

`<class 'str'>`

`What is your age : 20`

`20`

`Traceback (most recent call last):`

`<class 'str'>`

`  File "C:/Users/prac.py", line 9, in <module>`

`    print(age+5)`

`TypeError: must be str, not int`

我们不能给年龄加 5，因为年龄是字符串类型，我们不能用字符串做直接的数学运算。所以我们必须将年龄改为一个整数，因为我们将年龄作为输入，Python 将其作为字符串返回。

**因此。**

```
name = input(" What is your name : ")
print(name)
print(type(name))

age = input("What is your age : ")
print(age)
print(type(age))

age = int(age)

print(age+5)
```

**输出:**

`What is your name : Tyra`

`Tyra`

`<class 'str'>`

`What is your age : 20`

`20`

`<class 'str'>`

`25`

**常规方式**

假设我们不想使用内置函数 int()将 string 转换成整数。 只好用 **的常规方式** 来转换。

这里有一个不使用 int()进行转换的简单方法。

```
"""
    "123" -> 123
    "-12332" -> -12332

"""

def str_to_int(input_str):

    output_int = 0
    if input_str[0] == '-':
        start_idx = 1
        is_negative = True
    else:
        start_idx = 0
        is_negative = False

    for i in range(start_idx, len(input_str)):
        place = 10**(len(input_str) - (i+1))
        digit = ord(input_str[i]) - ord('0')
        output_int += place * digit

    if is_negative:
        return -1 * output_int
    else:
        return output_int

s = "554"
x = str_to_int(s)
print(type(x))

s = "123"
print(str_to_int(s))

s = "-123"
print(str_to_int(s))
```

**输出:**

`<class 'int'>`

`123`

`-123`

*   首先，我们将检查用户提供的数字是否包含任何负号，即它是否是负数。 如果它在第一个位置包含一个负号，我们就从第二个位置开始我们的转换，其中包含数字。

*   任何数字，比如说 123，都可以写成这样的形式——10 * * 2 * 1+10 * * 1 * 2+10 * * 0 * 3

*   同样，我们用**【ord(argument)**拆分每个输入的数字。

*   order(' 0 ')将返回 48，order(' 1 ')将返回 49 等等。

*   这里我们用的逻辑是 order(' 1 ')–order(' 0)= 1，order(' 2 ')–order(' 0 ')= 2 等等。它给出了从给定的输入数字中获取的有效数字。

*   最后，我们从函数中得到的输出是一个合法的整数，它是由给定的输入字符串转换而来的。

如你所见，我们可以使用 int()函数或传统方法将任何字符串转换成整数。

我希望你已经很好地学习了这些概念，因此可以更准确地尝试一下。至此，我们将结束这篇关于使用 Python 将字符串转换为 int 的文章。

*有问题吗？请在这个字符串到整数教程的评论部分提到它，我们会尽快回复你。*

*要深入了解 Python 及其各种应用，您可以注册参加实时 **[Python 在线培训](https://www.edureka.co/python)** ，该培训提供全天候支持和终身访问。*