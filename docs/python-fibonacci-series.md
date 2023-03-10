# 如何在 Python 中显示斐波那契数列？

> 原文：<https://www.edureka.co/blog/python-fibonacci-series/>

斐波那契数列是以意大利数学家命名的一系列数字，被称为**斐波那契**。它只是一系列数字，从 0 和 1 开始，然后加上前面的两个数字。在这篇文章中，你将学习如何编写一个 [Python 程序](https://www.edureka.co/blog/python-basics/)来使用多种方法实现斐波那契数列。下面将讨论指针:

*   [什么是斐波那契数列？](#fibonacciseries)
*   [Python Program to write Fibonacci Sequence](#pythonprogram)
    *   [使用循环](#loop)
    *   [使用递归](#recursion)

我们开始吧。

## **什么是斐波那契数列？**

斐波那契数列是数列中前面两个数相加形成的数列。

**斐波那契数列示例:** 0，1，1，2，3，5

在上面的例子中，0 和 1 是数列的前两项。这两个术语是直接打印的。第三项的计算方法是将前两项相加。在这种情况下是 0 和 1。所以，我们得到 0+1=1。因此，1 被打印为第三项。通过使用第二和第三项而不使用第一项来生成下一项。这样做，直到你想要的或用户要求的条款的数量。在上面的例子中，我们使用了五个术语。

接下来，让我们写一个 Python 程序来实现它。

## **Python 程序实现斐波那契数列**

用 [Python 编程语言](https://www.edureka.co/blog/python-programming-language)实现斐波那契数列最简单！现在有多种方法来实现它，即:

*   使用循环
*   使用递归

让我们一个一个地看这两个代码。

### **斐波那契数列使用循环**

Python 中的 [**循环**](https://www.edureka.co/blog/loops-in-python/) 允许我们多次执行一组语句。让我们写一个 python 程序，用循环实现斐波那契数列。

```
# Enter number of terms needed                   #0,1,1,2,3,5....
a=int(input("Enter the terms"))
f=0                                         #first element of series
s=1                                         #second element of series
if a<=0:
    print("The requested series is
",f)
else:
    print(f,s,end=" ")
    for x in range(2,a):
        next=f+s                           
        print(next,end=" ")
        f=s
        s=next

```

**输出:**输入术语 5 0 1 1 2 3

另一种编程斐波那契数列生成的方法是使用递归。让我们深入探讨一下。

### **Python 程序使用递归写斐波那契数列**

递归是基本的 [Python 编程技术](https://www.edureka.co/blog/python-programming-language)，其中函数直接或间接调用自身。相应的函数称为**递归函数**。使用递归算法，某些问题可以很容易地解决。让我们看看如何在 Python 中使用递归打印 Fibonacci 数列的前 n 个数字。

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

**Python 代码:**

```
def FibRecursion(n):  
   if n <= 1:  
       return n  
   else:  
       return(FibRecursion(n-1) + FibRecursion(n-2))  
 nterms = int(input("Enter the terms? "))  # take input from the user

if nterms <= 0:  # check if the number is valid 
   print("Please enter a positive integer")  
else:  
   print("Fibonacci sequence:")  
   for i in range(nterms):  
       print(FibRecursion(i))
```

**输出:**多少项:5 0 1 1 2 3

**说明:**在上面的 Python 程序中，我们使用递归来生成斐波那契数列。函数 FibRecursion 被递归调用，直到我们得到输出。在函数中，我们首先检查数字 n 是零还是一。如果是，我们返回 n 的值。如果不是，我们用值 n-1 和 n-2 递归调用 fibonacci。

这就把我们带到了“Python 中的斐波那契数列”这篇文章的结尾。我们已经学习了如何使用循环语句或递归以编程方式打印第 n 个斐波那契数。

*如果您希望学习 Python，并通过将您的职业生涯转变为数据科学家角色来获得定量分析、数据挖掘和数据呈现方面的专业知识，以超越数字，请查看我们的互动在线直播 [**Python 培训**](https://www.edureka.co/python-programming-certification-training) 。您将使用 Pandas、Numpy、Matplotlib、Scipy、Scikit、Pyspark 等库，并掌握 Python 机器学习、脚本、序列、web 抓取和利用 Apache Spark 的大数据分析等概念。培训提供 24*7 支持，在整个学习期间为您提供指导。*

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你，或者加入我们的[Python 编程](https://www.edureka.co/masters-program/python-developer-training)硕士课程。