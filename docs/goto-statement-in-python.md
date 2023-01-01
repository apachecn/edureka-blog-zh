# 关于 Python 中的 Goto 语句，您需要了解的一切

> 原文：<https://www.edureka.co/blog/goto-statement-in-python/>

[Python](https://www.edureka.co/blog/python-tutorial/) 是当今业界最流行的操作系统之一。从业余爱好者到专业用户，每个人都在使用 Python，但即使如此，还有一些方面尚未被发现。Python 的一个这样的方面是本机 goto 语句。因此，在本文中，我们将按以下顺序讨论 python 中的 goto 语句:

*   什么是 Goto 语句？
*   [Goto 语句的迭代](#iterations)
*   [计算 Goto 语句](#computed)
*   [限制](#restrictions)

## 什么是 Goto 语句？

goto 语句可以简单地定义为语法或一段代码，它提供从 goto 语句到同一函数内容中标记为目的地的语句的无条件跳转。通俗地说，如果你想让程序跳过某些函数，你需要使用 goto 语句。

**如果在任何情况下，程序员需要修改程序的内容并作出改变，由于 goto 语句会方便地跳过函数中的某些部分，所以很难定位准确的目的地。**

**语法**

Python 中 goto 语句的语法如下所示。

```
#Syntax-1
goto label;
.
.
.
label:

#Syntax-2
label:
.
.
.
goto label;
```

在上面的例子中，除了关键字 go 之外，标签可以被替换成你需要的任何文本，它可以被设置在程序的任何地方，也可以在 Go 语句的上面或下面。

快速事实:goto 语句最初是在 2004 年 4 月 1 日作为一个笑话发布的，但是全世界的程序员都认真对待它并开始使用它。

## **Goto 语句的迭代**

Python 中另一个与 goto 语句工作原理相同的代码是`comefrom`。`comefrom`和`goto`语句都为 Python 中的整个程序增加了灵活性，从而允许人们控制程序流机制，并且还包括对控制流习惯用法的可访问性，这在以前是不允许的。

为了在 Python 中使用 goto 和`comefrom`语句，需要首先将它们导入主库。为此，请键入下面提到的代码。

`from goto import goto, comefrom, label`

一旦库被导入，你就可以在你的程序中方便地使用这两个函数。

当您在 Python 中使用 goto 语句时，您基本上是在指示解释器直接执行另一行代码，而不是当前行。您希望解释器此时执行的目标代码行需要在名为“标签”的部分进行标记。关于 label 标签需要注意的一点是，它们大多是随机的、任意的 Python 标识符，前缀是一个点。示例`label .myLabel.`

## **计算 Goto 语句**

大多数程序员在 Python 中使用的 goto 语句的最常见变体之一是计算 goto 语句。在这里，您在代码的开头提到了 python 索引，然后通过使用 hashtag 来引用它。例，

```
x = calculateLabelName()
goto *x
```

**注:**上述语句中 x 的值不应包括在此之前的例子中提到的前缀点。

## **来自**

在 Python 中，`comefrom`语句基本上和 goto 语句相反。用最简单的术语来说，它对解释器的功能可以通过下面的语句来解释，“每当到达标签 X 时，改为跳转到这里。”

下面是一个使用中的`comefrom`语句的例子。

`# ...code 1...`

`label .somewhere`

`# ...code 2...`

`comefrom .somewhere`

在上面的语句中，代码 2 不会被执行。当解释器到达行标签时。某处，会直接跳到下一行`comefrom`.某处.

关于`comefrom`语句需要注意的另一个重要方面是，它通常被用作编程中的调试工具。不鼓励在独立编程操作中使用它的,因为它有时可能会导致不方便和支持性的结果。

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

## **Python 中 Goto 语句的限制**

与其他编码平台和代码行类似，Python 也对 goto 和 comefrom 语句所能实现的功能设置了许多限制。下面提到的是 goto 和 comefrom 语句的一些最常见的限制。

1.  不允许使用这两个语句跳转到循环或 [finally](https://www.edureka.co/blog/final-finally-and-finalize-in-java/) 子句中间。

2.  人们不能使用这些语句在函数和或模块之间跳转。

3.  不能用来跳转到 except 行，因为首先没有异常行。

**#例 1:从深度嵌套循环中突围:**

```
from goto import goto, label
for i in range(1, 10):
    for j in range(1, 20):
        for k in range(1, 30):
            print i, j, k
            if k == 3:
                goto .end
label .end
print "Finishedn"
```

**#例 2:出现故障后的清理:**

```
from goto import goto, label

# Imagine that these are real worker functions.
def setUp(): print "setUp"
def doFirstTask(): print 1; return True
def doSecondTask(): print 2; return True
def doThirdTask(): print 3; return False  # This one pretends to fail.
def doFourthTask(): print 4; return True
def cleanUp(): print "cleanUp"

# This prints "setUp, 1, 2, 3, cleanUp" - no "4" because doThirdTask fails.
def bigFunction1():
    setUp()
    if not doFirstTask():
        goto .cleanup
    if not doSecondTask():
        goto .cleanup
    if not doThirdTask():
        goto .cleanup
    if not doFourthTask():
        goto .cleanup

    label .cleanup
    cleanUp()

bigFunction1()
print "bigFunction1 donen"
```

在审计和调试需求方面，goto 语句是 Python 最有用的语句之一。虽然它有时可以在日常编程中使用，但经常使用它有时会导致令人惊讶的结果。

至此，我们结束了 Python 文章中的 goto 语句。 *要深入了解 Python 及其各种应用，您现在就可以报名参加 [Python 课程](https://www.edureka.co/python-programming-certification-training)培训，该课程提供全天候支持和终身访问。*

*有问题吗？在“Python 中的 Goto 语句”的评论部分提到它们，我们会回复你或者加入我们的[Python 编程大师](https://www.edureka.co/masters-program/python-developer-training)课程..*