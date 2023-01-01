# Python 中的随机数生成器是什么，怎么用？

> 原文：<https://www.edureka.co/blog/generate-random-number-in-python/>

在创建软件时，我们的程序通常需要产生各种项目。这在游戏、OTP 生成、赌博等应用中最为常见。 [Python](https://www.edureka.co/blog/python-tutorial/) 通过其内置的[函数](https://www.edureka.co/blog/python-functions)使生成这些值的任务变得毫不费力。这篇关于 Python 中随机数生成器的文章，您将学习如何使用各种内置函数生成数字。

在继续之前，让我们看一下本教程中讨论的主题:

*   [Python 中的随机数生成器是什么？](#randomgenerators)
*   [生成整数](#integers)
*   [生成浮点数](#float)
*   [从序列中返回值](#sequence)
*   [其他功能](#otherfunctions)

那么让我们开始吧。:)

## **Python 中的随机数生成器是什么？**

[生成器](https://www.edureka.co/blog/generators-in-python/)是无论何时被调用都会产生项目的函数。Python 中的随机数生成器是内置函数，可以帮助您在需要时生成数字。这些函数嵌入在 [Python](https://www.edureka.co/blog/python-anaconda-tutorial/) 的随机模块中。

请看下表，其中包含一些重要的随机数发生器函数以及随机模块中对它们的描述:

| **功能** | **描述** |
| 种子() | 产生的值将是确定的，这意味着当种子号相同时，将产生相同的值序列 |
| 随机范围() | 可以返回指定限制和间隔之间的随机值 |
| randint() | 返回给定限制之间的随机整数 |
| 选择() | 从序列中返回一个随机数 |
| 无序播放() | 打乱给定的序列 |
| 样本() | 从序列中返回随机选择的项目 |
| 统一() | 返回给定范围内的浮点值 |

现在让我们更深入地了解一下其中的每一项。

### **生成整数:**

可以使用 randrange()和 randint()等函数生成随机整数。

让我们先来看看 randint()。

**randint():**

这个函数在给定的范围内产生整数。它有两个参数，第一个参数指定下限，第二个参数指定上限。 *randint(a，b)* 开始生成从 a 到 b 的值，使得:

a <= x <= b(包括 a 和 b)

**举例:**

```
import random
random.randint(2,9)
```

**输出:** 5

上面的代码可以生成从 2 到 9 的数字，包括极限。如果您想在此范围内生成几个值，您可以使用 [循环](https://www.edureka.co/blog/loops-in-python/)的*，如下所示:*

**举例:**

```
import random
for x in range(2):
    print(random.randint(2,9))
```

**输出:**

2 6

如果您想生成区间数，可以使用 randrange()函数。

### **randrange():**

如前所述，randrange()函数允许用户通过步进间隔计数来生成值。

**例如:**

```
import random
for x in range(5):
    print(random.randrange(2,60,2))
```

**输出:**

34 28 14 8 26

如你所见，这里生成的所有数字都是介于 2 和 6 之间的偶数。

还可以使用 random 模块的内置函数生成浮点值。

### **生成浮点值:**

要生成浮点数，可以利用 random()和 uniform 函数。

**random():**

这个函数产生 0.0 到 1.0 之间的浮点值，因此不需要参数。请注意，不包括上限。所以最大值将是 9.999。

**举例:**

```
import random
for x in range(5):
    print(random.random())
```

**输出:**

0.18156025373128404

#### **制服():**

与 random()函数不同，该函数采用两个参数，分别确定下限和上限。

**举例:**

```
for x in range(5):
    print(random.uniform(6))
```

**输出:**

2.33377305633355.56239393256

Python 还允许您从给定的序列中生成随机值。

### **从给定序列中生成值:**

这可以使用 choice()和 sample()函数来完成。

#### **choice():**

这个函数基本上以一个序列作为参数，并从中返回随机值。

**举例:**

```
for x in range(3):
    print(random.choice([1,2,3,4,5,6,7,8,9]))
```

**输出:**

3 1 4

正如您所看到的，在上面的输出中，使用 for 循环返回了三个值，所有的值都是从给定的列表中随机选取的。

#### **sample():**

sample()函数从给定的序列中选取一个随机序列，并将其作为输出返回。它有两个参数，第一个参数是一个序列，第二个参数是指定输出中需要返回多少个值的整数值。

**举例:**

```
print(random.sample([1,2,3,4,5,6,7,8,9],4))
```

**输出:** [1，4，5，9]

正如您所看到的，上例中产生的输出列表由从给定序列中随机选择的四个值组成。

### **其他功能:**

**seed():**

seed()函数将一个名为 seed 的数字作为参数，并在每次使用该数字调用该函数时产生相同的随机数。

**举例:**

```
random.seed(2)
print(random.random(),random.random(),random.random(),end='nn')
random.seed(3)
print(random.random(),random.random(),random.random(),end='nn')
random.seed(2)
print(random.random(),random.random(),random.random())

```

**输出:**

```
0.9560342718892494 0.9478274870593494 0.05655136772680869

0.23796462709189137 0.5442292252959519 0.36995516654807925

0.9560342718892494 0.9478274870593494 0.05655136772680869
```

在上面的例子中，每次调用 seed(2)时，它的输出都是相同的。在需要将相同的随机数传递给不同测试用例的实验中，这个函数非常有用。

**shuffle():**

这个函数用于随机打乱一个给定的序列。

**举例:**

```
mylist=[1,2,3,4,5,6,7,8,9]
random.shuffle(mylist)
print(mylist)
```

**输出:** [6，8，2，4，3，7，1，5，9]

这就把我们带到了“Python 中的随机数生成器”这篇文章的结尾。我希望你已经理解了所有的概念。

***Make sure you practice as much as possible and revert your experience.*  **

*有问题吗？请在这个“Python 中的随机数生成器”博客的评论部分提到它，我们会尽快回复你。*

*要深入了解 Python 及其各种应用，您可以报名参加[最佳 Python 课程](https://www.edureka.co/python-programming-certification-training)，该课程提供全天候支持和终身访问。*