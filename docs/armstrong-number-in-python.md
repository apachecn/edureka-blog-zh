# 如何在 Python 中最好地实现阿姆斯特朗数？

> 原文：<https://www.edureka.co/blog/armstrong-number-in-python/>

[Python](https://www.edureka.co/blog/python-tutorial/) 无疑是最受欢迎和最容易识别的编码平台之一。由于 Python 的强大特性和多功能性，从业余爱好者到专业人士，每个人都将 Python 作为编程的首选语言。也就是说，我们从顾客那里得到的最常见的请求之一是如何用 Python 为 Armstrong number 编写一个程序。虽然这对于熟悉这门语言的人来说似乎很容易，但是有一些技术细节可能会被忽略。因此，在本文中，我们将更多地讨论 Python 中的阿姆斯特朗数，以及如何用 Python 编写同样的程序。

本文将涉及以下几点:

*   [Python 中的阿姆斯特朗数](#ArmstrongNumberInPython)
*   什么是阿姆斯特朗号码？
*   [程序检查阿姆斯特朗数的 N 位数](#ProgramToCheckArmstrongNumberOfNDigits)

那么让我们开始吧，

## **Python 中的阿姆斯特朗数**

## 什么是阿姆斯特朗号码？

现在你已经知道什么是阿姆斯特朗数，让我们来探索如何用 Python 写一个同样的程序。

用最简单的术语来说，阿姆斯特朗数可以被定义为一个整数，其位数的立方之和等于该数本身。阿姆斯特朗数的一个例子可以是 371，计算时可以分解为 3**3 + 7**3 + 1**3 = 371。

继续这篇关于 Python 中的阿姆斯特朗数的文章，

**Python 中的阿姆斯特朗数程序**

为了用 Python 编写阿姆斯特朗数的程序，你首先需要了解 Python if…else 语句以及 Python while 循环。

1.  **Python if…else 语句:**Python if…else 语句可以简单定义为一段代码，只在满足一定条件需要生成结果时使用。例如，如果 a 等于 b，则打印 c.
2.  **Python while Loop:** 另一方面，Python while Loop 是一段代码，当某段代码需要反复运行，直到某个条件为真时使用。例如，如果 a 等于 be，则打印 c 10 次。

现在你已经知道 Python if…else 语句和 Python while 循环是什么了，让我们探索一下用 Python 为 Armstrong number 编写的程序会是什么样子。

```
# Python program to check if the number provided by the user is an Armstrong number or not
# take input from the user
num = int(input("Enter a number: "))
# initialize sum
sum = 0
# find the sum of the cube of each digit
temp = num
while temp > 0:
digit = temp % 10
sum += digit ** 3
temp //= 10
# display the result
if num == sum:
print(num,"is an Armstrong number")
else:
print(num,"is not an Armstrong number")
```

为了更好地探究上面的例子，让我们取两个输入。

**输入 1:** 提示时输入 663。

**结果:** 663 不是阿姆斯壮数。

**输入 2:** 提示时输入 407。

**结果:** 407 是阿姆斯壮数。

在上述两个输入中，我们可以选择让用户输入他们选择的数字，然后分析它是否是阿姆斯特朗数字。

为了分析某个输入是否是阿姆斯特朗数，我们需要将输入分解成单个的数，计算每个数的立方，然后将它们加在一起。为了在编码的上下文中实现这一点，我们使用了模数操作符(% operator)。在上面的例子中，一个数除以 10 的余数是这个数的最后一位。我们用指数算子来取立方体。

在最后一步，我们将我们的结果与最初输入的数字进行比较，并判断它是否是阿姆斯特朗的数字。

继续这篇关于 Python 中的阿姆斯特朗数的文章，

```
Program to check Armstrong number of n digits
num = 1634
# Changed num variable to string,
# and calculated the length (number of digits)
order = len(str(num))
# initialize sum
sum = 0
# find the sum of the cube of each digit
temp = num
while temp > 0:
digit = temp % 10
sum += digit ** order
temp //= 10
# display the result
if num == sum:
print(num,"is an Armstrong number")
else:
print(num,"is not an Armstrong number")
```

在上面的程序中，我们已经将输入共享为 1634。因此，程序现在将检查 1634 是否是一个阿姆斯特朗数。正如您可能已经猜到的，数字 1634 不是阿姆斯特朗数字，因此上面的程序打印出，1634 不是阿姆斯特朗数字。

这就把我们带到了这篇关于 Python 中的阿姆斯特朗数的文章的结尾。

*要深入了解 Python 及其各种应用，您可以在此注册参加在线直播的 [Python 认证课程](https://www.edureka.co/python-programming-certification-training)，该课程提供全天候支持和终身访问。* *有问题吗？在这篇文章的评论部分提到它们，我们会给你回复。*