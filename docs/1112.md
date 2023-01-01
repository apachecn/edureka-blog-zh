# Python 移除列表:如何从列表中移除元素

> 原文：<https://www.edureka.co/blog/python-list-remove/>

[Python 编程硕士](https://www.edureka.co/masters-program/python-developer-training)认证是市场上最受欢迎的认证之一。原因在于 Python 提供的一系列功能。列表在很大程度上简化了程序员的生活。在本文中，我们将学习如何从列表中移除元素。

在继续之前，让我们快速浏览一下这篇文章所涉及的内容:T2

[为什么要使用列表？](#whyuselists) [有哪些列表？](#whatarelists) [从列表中删除元素使用:](#removeelements)

*   [remove()](#remove())
*   [pop()](#pop())
*   [德尔()](#pop())

所以让我们开始吧。:)

## 为什么要使用列表？

有时，你可能需要同时处理不同类型的数据。比如说，你需要在同一个集合中有一个字符串类型的元素，一个整数和一个浮点数。现在，对于其他编程语言如 C & C++中可用的默认数据类型来说，这几乎是不可能的。简单地说，如果你定义了一个整数类型的数组，你只能在里面存储整数。这是 Python 有优势的地方。通过它的列表集合数据类型，我们可以将不同数据类型[的元素](https://www.edureka.co/blog/python-programming-language#DataTypes)存储为一个有序集合！

现在你知道了列表的重要性，让我们继续看看什么是列表，以及如何从列表中移除元素！

## 什么是列表？

列表是 **有序的** **序列** 可以容纳多种对象类型。换句话说，列表是由 **有序** 和 **可变** 的元素组成的集合。列表也允许重复成员。我们可以将 Python 中的列表与其他编程语言中的数组进行比较。但是，有一个主要的区别。数组包含相同数据类型的元素，而 Python 列表可以包含不同类型的项目。单个列表可能包含字符串、整数、浮点数等数据类型。列表支持 **索引** 和 **切片** ，就像字符串一样。列表也是可变的，这意味着它们可以在创建后被修改。除此之外，列表也可以嵌套，也就是说，你可以在列表中包含一个列表。

列表在 [Python 编程](https://www.edureka.co/blog/python-programming-language)中是一个重要工具的主要原因是因为它附带了种类繁多的[内置函数](https://www.edureka.co/blog/python-functions)。列表对于在 Python 中实现堆栈和队列也非常有用。列表中的所有元素都用方括号括起来，每个元素都用逗号分隔。

**举例:**

```

myList = ["Bran",11,3.14,33,"Stark",22,33,11]

print(myList)

```

**输出:** ['布兰'，11，3.14，33，'斯塔克'，22，33，11]

在上面的例子中，我们定义了一个名为*'****my list****'*的列表。如您所见，所有元素都被括在方括号内，即[ ]，每个元素都用逗号分隔。这个列表是一个有序序列，包含不同数据类型的元素。

在索引 0 处，我们有字符串元素“Bran”。

在索引 1 处，我们有一个整数 11。

在索引 2 处，我们有一个浮点数 3.14。

这样，我们可以在一个列表中存储不同类型的元素。

现在你已经清楚如何创建列表了，让我们继续看如何在 Python 中从列表中移除元素。

## **从列表中删除元素:**

有三种方法可以从列表中删除元素:

1.  使用 **清除()** 的方法
2.  使用列表对象的 **pop()** 方法
3.  使用运算符

让我们详细看看这些。

### **列表对象的 remove()方法:**

remove()方法是最常用的列表对象方法之一，用于从列表中删除一个项目或元素。使用此方法时，您需要指定要删除的特定项目。请注意，如果指定的项目出现多次，那么它的第一次出现将从列表中删除。我们可以把这种方法看作是 **【按项取值】** 。如果没有找到要删除的特定项目，则产生一个 *值错误* 。

考虑以下例子:

**例 1:**

```

myList = ["Bran",11,22,33,"Stark",22,33,11]

myList.remove(22)

myList

```

**输出** **:** ['布兰'，11，33，'斯塔克'，22，33，11]

在这个例子中，我们定义了一个名为***【myList】***的列表。注意，如前所述，我们将列表文字放在方括号中。在 **例 1** 中，我们使用 **remove()** 方法将元素 *22* 从*myList*中移除。因此，当使用 **print()、** 打印列表时，我们可以看到 *22* 元素已经从*myList*中移除。

**例二** :

```

 myList.remove(44)

```

**输出** **:**

【回溯】(最近一次调用 **最后一次调用** ):

文件< stdin >，第 1 行 **中**

value error:list . remove(x):x**不是** list2 中的

在 **例 2** 中，我们用 **remove()** 来删除元素 *44* 。但是，我们知道，list '*myList*'中没有整数 *44* 。结果，Python 解释器抛出一个'*value error*'。

(不过，这是一种的慢术，因为它涉及到在列表中搜索物品。)

### **列表对象的 pop()方法:**

pop()方法是另一种常用的列表对象方法。该方法从列表中移除一个项目或元素， *将其返回* 。该方法与 remove()方法的区别在于，我们应该在 remove()方法中指定要移除的项目。但是，当使用 pop()时，我们将项目 的 **索引指定为参数，因此，它将弹出指定索引处要返回的项目。如果没有找到要移除的特定项目，则引发** *索引错误* 。

考虑下面的例子:

**例 1:**

```

 myList = ["Bran",11,22,33,"Stark",22,33,11]

 myList.pop(1)

```

**输出** **:** 11

在这个例子中，我们定义了一个名为'***【my list】****'*的列表。在 **例 1** 中，我们使用的是**【pop()】**的方法，而传递实参' *1'* ，其中无非是 *索引位置 1* 。从输出中可以看到，pop()移除元素，并返回它，是整数' *11* '。

**例 2:**

```

myList

```

**输出** **:** ['布兰'，22，33，'斯塔克'，22，33，11]

注意，在 **例 2** 中，当我们在调用 pop()后打印 list*my list*时，之前出现在*my list*中的整数 *11* 已经被删除。

**例 3:**

```

myList.pop(8)

```

**输出:**

【回溯】(最近一次调用 **最后一次调用** ):

文件< stdin >，第 1 行 **中**

IndexError:弹出指数 **超出** 范围

在 **例 3** 中，我们使用 pop()移除位于 *索引位置 8* 的元素。由于这个位置没有元素，python 解释器抛出一个*IndexError*，如输出所示。

(这是一种 **快速** **技术** ，因为它非常简单明了，并且不涉及对列表中的项目进行任何搜索。)

### **Python****delT5**运算符:****

这个操作符类似于 List 对象的 pop()方法，但有一个重要的区别。del 操作符从列表中移除指定索引位置的项或元素，但与 pop()方法一样， **移除的项不会返回** 。所以本质上，这个操作符把要删除的项的索引作为参数，并删除该索引处的项。运算符还支持删除列表中的一系列项目。请注意，这个操作符就像 pop()方法一样，当指定的索引超出范围时，会引发一个*IndexError*。

考虑以下例子:

**例 1:**

```

myList = ["Bran",11,22,33,"Stark",22,33,11]

del myList[2]

myList

```

**输出** **:** ['布兰'，11，33，'斯塔克'，22，33，11]

在上面的例子中，我们定义了一个名为'***【myList】****'*的列表。 **在例 1** 中，我们用运算符删除了*myList*中 *索引位置 2* 的元素。因此，当您打印*my list*时，位于 *索引位置 2* 的整数'*22 '*被删除，如输出所示。

**例 2:**

```

del myList[1:4]

myList

```

**输出** **:** 【布兰’，22，33，11】

在 **示例** **2** 中，我们使用 **del** 运算符从一系列索引中删除元素，即从 *索引位置 1 到索引位置 4(但不包括 4)。* 随后，当您打印*my list*时，您可以看到 *索引位置 1、2 和 3* 的元素被删除。

**例三:**

```

del myList[7]

```

**输出** **:**

回溯(最近一次叫 **最后一次叫** ):

文件】，第 1 行， 中的

IndexError:列表赋值指标 **超出** 范围

在 **例 3** 中，当你使用 **del** 运算符删除 *索引位置 7* (该位置不存在)的一个元素时，python 解释器抛出一个*value error*。

(当用户清楚列表中的项目时，这种移除项目的技术是优选的。同样，这是一个 **快速从列表中删除物品的方法** 。)

总结一下， **remove()** 方法删除了 *第一个匹配值* ，以及 *未指定的索引*； **pop()** 方法 *删除指定索引处的项，并返回；* 最后 **del** 运算符只需 *删除指定索引* (或一系列索引)处的项目。

## **脚注——与从列表中删除元素相关的最常见问题**

### 如何在 Python 中从列表中移除特定元素？

remove()方法从列表中移除第一个匹配的元素(作为参数传递)。pop()方法移除给定索引处的元素，并将返回移除的项目。还可以在 Python 中使用 del 关键字从列表中删除元素或片段。

**了解我们在顶级城市/国家的 Python 培训**

| **印度** | **美国** | **其他城市/国家** |
| [班加罗尔](https://www.edureka.co/python-programming-certification-training-bangalore) | [纽约](https://www.edureka.co/python-programming-certification-training-new-york-city) | [英国](https://www.edureka.co/python-programming-certification-training-uk) |
| [海德拉巴](https://www.edureka.co/python-programming-certification-training-hyderabad) | [芝加哥](https://www.edureka.co/python-programming-certification-training-chicago) | 伦敦 |
| [德里](https://www.edureka.co/python-programming-certification-training-delhi) | 亚特兰大 | [加拿大](https://www.edureka.co/python-programming-certification-training-canada) |
| [钦奈](https://www.edureka.co/python-programming-certification-training-chennai) | [休斯顿](https://www.edureka.co/python-programming-certification-training-houston) | [多伦多](https://www.edureka.co/python-programming-certification-training-toronto) |
| [孟买](https://www.edureka.co/python-programming-certification-training-mumbai) | 洛杉矶 | [澳大利亚](https://www.edureka.co/python-programming-certification-training-australia) |
| [浦那](https://www.edureka.co/python-programming-certification-training-pune) | [波士顿](https://www.edureka.co/python-programming-certification-training-boston) | 阿联酋 |
| 加尔各答 | [迈阿密](https://www.edureka.co/python-programming-certification-training-miami) | [迪拜](https://www.edureka.co/python-programming-certification-training-dubai) |
| 艾哈迈达巴德 | [旧金山](https://www.edureka.co/python-programming-certification-training-san-francisco) | [菲律宾](https://www.edureka.co/python-programming-certification-training-philippines) |

### 如何用 Python 删除列表中的第一个元素？

我们可以通过以下四个选项做到这一点:

1.  list . pop()–最简单的方法是使用 list 的 pop([i])方法，该方法移除并返回列表中指定位置的项目。
2.  list . remove()–这是另一种方法，其中 remove(x)方法从列表中删除与指定值匹配的第一个项目。
3.  切片–要删除第一项，我们可以通过获取一个包含列表中除第一项之外的所有项的子列表来使用切片。
4.  del 语句–使用 Del 语句，我们可以通过索引从列表中删除一个条目。与 pop()方法的区别在于，它不返回被移除的元素。

### 如何在 Python 中删除列表的最后一个元素？

pop()方法可用于移除和返回列表中的最后一个值或给定的索引值。如果没有给出索引，那么最后一个元素被弹出并删除。

### 如何在 Python 中从一个列表中移除多个元素？

即使为了这个目的，也可以使用 Del 关键字。如果我们提供一个索引范围，它将从一个列表中删除多个元素。要从索引位置 2 到 5 的列表中删除多个元素，我们应该使用 del 方法，该方法将删除从索引 2 到索引 5 范围内的元素。

我希望你能够通读这篇文章，并对从列表中删除元素的各种技术有一个合理的理解。

***Make sure you practice as much as possible and revert your experience.*  **

*有问题吗？请在这个“从列表中删除元素”博客的评论部分提到它，我们会尽快回复您，或者今天就参加我们在钦奈的 [Python 培训。](https://www.edureka.co/python-programming-certification-training-chennai)*

*要深入了解 Python 及其各种应用，您可以注册参加实时 [**Python 课程**](https://www.edureka.co/python-programming-certification-training) ，该课程提供全天候支持和终身访问。*