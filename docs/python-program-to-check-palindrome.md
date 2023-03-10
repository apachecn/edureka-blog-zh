# Python 中如何检查一个数是回文？

> 原文：<https://www.edureka.co/blog/python-program-to-check-palindrome/>

小时候，阅读反向字符串很有趣，当我们稍微长大一点时，我们知道以任何一种方式阅读的[字符串](https://www.edureka.co/blog/strings_in_python/)被称为回文。好奇心让我们留在那里，所以我们希望我们的机器学习什么是回文，对于所有 Python 爱好者来说，没有其他语言能以更好的方式做到这一点。如果您是 python 爱好者和编码爱好者，请继续阅读，学习如何用 Python 创建回文。

*   [什么是回文？](#palindromeinjava)
*   [回文程序使用 while 循环](#palindromeprogram)
*   [回文程序使用内置函数](#palindromeprogramusingfunction)

我们开始吧。

## **什么是回文？**

回文只不过是一个数字或者一个字符串，当它被颠倒的时候保持不变。

**例:**12321**输出:**是的，一个回文数

**举例:**赛车 输出:是的，一个回文串

很明显，字母在反转时会形成镜像。

现在你已经理解了这个概念，让我们简单地进入一个用 Python 检查回文的程序。

**了解我们在顶级城市/国家的 Python 培训**

| **印度** | **美国** | **其他城市/国家** |
| [班加罗尔的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-bangalore) | [纽约的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-new-york-city) | [英国数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-uk) |
| [海德拉巴的 Python 数据科学培训](https://www.edureka.co/data-science-python-certification-course-hyderabad) | [夏洛特的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-charlotte) | [迪拜的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-dubai) |
| [德里的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-delhi) | [奥斯汀的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-austin) | [加拿大数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-canada) |
| [钦奈的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-chennai) | [西雅图的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-seattle) | [新加坡的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-singapore) |
| [加尔各答的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-chennai) | [达拉斯的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-dallas) | [圣何塞的数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course-san-jose) |

## **回文程序使用 While 循环**

这是在 Python 编程中使用 while [循环找到回文程序最简单的程序之一。让我们深入一个例子来检查给定的输入是否是回文。](https://www.edureka.co/blog/loops-in-python/)

```
num=int(input("Enter a number:"))
temp=num
rev=0
while(num&gt;0):
    dig=num%10
    rev=rev*10+dig
    num=num//10
if(temp==rev):
    print("The number is palindrome!")
else:
    print("Not a palindrome!")

```

**输出:**

输入一个数字:121 数字是回文！

继续 Python 回文程序的例子，让我们看看如何使用内置函数检查一个字符串是否是回文。

## **使用内置方法的回文程序(字符串)**

```
string=input(("Enter a string:"))
if(string==string[::-1]):
      print("The string is a palindrome")
else:
      print("Not a palindrome")
```

**输出:**

![Palindrome in Python - Edureka](img/68d7ece648c2c5ee23c6c9c3d69cae6c.png)

**解释:**在上面的程序中，首先从用户处获取输入(使用 input 或 raw_input()方法)来检查回文。然后使用切片操作[start:end:step]，检查字符串是否反转。这里，步长值为-1 会反转一个字符串。如果是，它打印一个其他的回文，而不是一个回文。

This brings us to the end of this article where we have learned how to find palindrome in Python. I hope you are clear with all that has been shared with you in this tutorial.

确保你尽可能多地练习，恢复你的经验。

有问题吗？请在这个“Python 中的回文程序”博客的评论部分提到它，我们会尽快回复你，或者你可以加入我们的[数据科学与 Python 课程](https://www.edureka.co/data-science-python-certification-course)。

要深入了解 Python 及其各种应用程序，您可以注册参加现场 [**Python 培训**](https://www.edureka.co/python-programming-certification-training) ，该培训提供全天候支持和终身访问。

通过我们的[人工智能课程](https://www.edureka.co/executive-programs/machine-learning-and-ai)，发现你成为人工智能和人工智能专家的全部能力。了解各种人工智能相关技术，如机器学习、深度学习、计算机视觉、自然语言处理、语音识别和强化学习。