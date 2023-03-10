# 如何在 Python 中寻找质数

> 原文：<https://www.edureka.co/blog/python-program-prime-number/>

质数是大于 1 的自然数，除了 1 和它本身之外，它没有任何除数。你可以用 Python 写一个[代码，帮助你找到所有的质数。在本文中，我们将看到如何按照以下顺序用 Python 编写一个素数程序:](https://www.edureka.co/blog/python-basics/)

*   什么是质数？
*   [Python 程序检查质数](#prime)
    *   [优化方法](#optimize)

让我们开始吧。

## 什么是质数？

一个大于 1 的正整数，除了 1 和这个数本身之外没有其他因数，称为素数。数字 2、3、5、7 等。是质数，因为它们没有任何其他因素。要在 Python 中找到一个质数，你必须使用循环的[从头到尾迭代该值，对于每个数字，如果它大于 1，检查它是否除以 n，如果我们找到任何其他可以除的数字，打印该值。](https://www.edureka.co/blog/loops-in-python/#Whatisforloopandwhileloop?)

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

## **Python 程序检查质数**

质数总是正数，它将在程序开始时被检查。这里你会把输入的数除以所有的数，看看有没有除了 1 和数本身以外的正约数。如果找到了任何除数，那么我们显示“这个数不是一个质数”，否则我们显示“这个数是一个质数”。

**Python 程序:**

```
num = 13
if num &gt; 1:
for i in range(2, num//2):
if (num % i) == 0:
print(num, "is not a prime number")
break
else:
print(num, "is a prime number")
else:
print(num, "is not a prime number")
```

**输出:** 13 是一个素数

### **优化方法**

在 Python 中有不同的方法来优化质数程序:

*   我们可以检查到√n，而不是检查到 n，因为 n 的较大因子必须是已经检查过的较小因子的倍数。
*   通过观察除了 2 和 3 之外，所有的素数都是 6k 1 的形式，可以进一步改进算法。这是因为对于某个整数 k，对于 i =，所有的整数都可以表示为(6k + i)？1、0、1、2、3 或 4；2 除(6k + 0)，(6k + 2)，(6k+4)；和 3 除(6k + 3)。因此，更有效的方法是测试 n 是否能被 2 或 3 整除，然后检查所有 6k 1 形式的数字。

**举例:**

```
def isPrime(n) :
if (n &lt;= 1) :
return False
if (n &lt;= 3) :
return True
if (n % 2 == 0 or n % 3 == 0) :
return False
i = 5
while(i * i &lt;= n) :
if (n % i == 0 or n % (i + 2) == 0) :
return False
i = i + 6
return True
if (isPrime(11)) :
print(" true")
else :
print(" false")
if(isPrime(15)) :
print(" true")
else :
print(" false")
```

说到这里，我们的文章就到此为止了。我希望你理解了如何用 [Python 编程](https://www.edureka.co/blog/python-programming-language)写一个质数程序。

*要深入了解 Python 及其各种应用，您可以注册参加现场 [**Python 认证**](https://www.edureka.co/python-programming-certification-training) 培训，该培训提供全天候支持和终身访问。*

*有问题吗？请在这个“Python 中的质数程序”博客的评论部分提到它，我们会尽快回复你，或者今天就加入我们的[Python 编程大师](https://www.edureka.co/masters-program/python-developer-training)课程。*

与瓦朗加尔国家技术学院的 E & ICT 学院合作，提供人工智能和机器学习方面的研究生课程，保持技术领先。这门[人工智能课程](https://www.edureka.co/executive-programs/machine-learning-and-ai)旨在提供最好的结果。