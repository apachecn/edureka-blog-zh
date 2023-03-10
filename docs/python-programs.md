# Python 程序:应该关注哪些 Python 基础知识？

> 原文：<https://www.edureka.co/blog/python-programs/>

技术进步导致工作量减少。这使得 [Python 编程语言](https://www.edureka.co/blog/python-tutorial/)因其易于访问和可读性而成为最受欢迎的编程语言之一。这也意味着尝试 Python 代码的人数激增。在这个博客中，我们将介绍几个最受欢迎的基础 [python](https://www.edureka.co/data-science-python-certification-course) 程序。以下是相同的列表:

*   [Python 中的回文程序](#1)
*   [Python 中的阶乘程序](#2)
*   [斐波那契数列程序](#3)
*   [Python 中的阿姆斯特朗数程序](#4)
*   [计算器程序](#5)
*   [Python 中的模式程序](#6)
*   [闰年程序](#7)
*   [Python 中的质数程序](#8)
*   [Python 中查找区域的程序](#9)
*   [程序反转列表](#10)

## **Python 中的回文程序**

A palindrome is a number, string or a sequence which will be the same even after we reverse the order. For example: MADAM, if spelled backwards will be same as MADAM.![palindrome-python programs-edureka](img/401e62be14d7838273ef31a627d7a4e9.png)Following is the python program to check whether the input [string](https://www.edureka.co/blog/variables-and-data-types-in-python/) is a palindrome or not.

```

def pal(num):
     x1 = num[::-1]
     if x1 == x:
       print('palindrome')
    else:
       print('not a palindrome')

print(pal('edureka'))

```

## **Python 中的阶乘程序**

一个数的阶乘是所有小于或等于该数的正数的乘积。一个数 n 的阶乘用 n 表示！。

![factorial-python programs-edureka](img/8efc7e1710c1824d142085e2890ea03f.png)

下面是计算一个数的阶乘的程序。

```

def fact(num):
    if num == 0:
       return num
    else:
       return num * fact(num - 1)
print(fact(5))

```

## **斐波那契数列**

A series in which the next term is the sum of the preceding two terms is called a fibonacci series. Fibonacci series is asked frequently in interviews.

![fibbonacci series-edureka](img/9b734b68349d5de22907cb78c4fa3819.png)

下面是一个打印斐波那契数列的程序。

```

a = int(input('enter the first element'))
b = int(input('enter the second element'))
n = int(input('enter the number of elements '))
print(a,b, end=" ")

while n-2:
       c = a + b
       a = b
       b = c
       print(c, end=" ")
       n = n-1

```

## **Python 中的阿姆斯特朗数程序**

它是一个特殊的数字，如果我们把阿姆斯特朗数中每个数字的立方相加，它就等于这个数本身。

![armstrong number-edureka](img/1a1a9d8362758bec6db72f10232e9a3e.png)

下面是检查一个数是否是阿姆斯特朗数的程序。

```
num = int(input('enter the nuber'))
s = 0
temp = num
while temp &amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;gt; 0:
c = temp % 10
s += c**3
temp //= 10
if s == num:
print('armstrong number')
else:
print('not an armstrong number')

```

## **Python 中的计算器程序**

When we think about a calculator, [operations](https://www.edureka.co/blog/operators-in-python/) like addition, subtraction, multiplication and division comes into our mind. We will try to build a calculator using python. We will add a few more operations in the program for better understanding.

![calculator-edureka](img/8c12b92deff8f9e329ff949748382482.png)

下面是创建计算器的程序

```

def add(a,b):
     return a+b

def sub(a,b):
     return a-b

def prod(a,b):
     return a * b

def div(a,b):
     return a / b

def si(p, r, t):
    return (p*r*t) / 100

def ci(p, r ,t):
    return p * pow((1 + r/100), t)

def sqr(num):
    return num**2

def sqrt(num)
    return num**0.5

print(add(10,15))
#to add two numbers, similarly you can use other functions for other operations.

```

## **花样程序**

We can use [for loop](https://www.edureka.co/blog/loops-in-python/) to print various patterns in python. We will print a pyramid and a half pyramid pattern using the asterisk in a program.

![patterns-python programs-edureka](img/9cc44775e15a043d127b3253a81c9410.png)

以下是模式的程序。

```

num = 5
a = (2 * num) - 2
for i in range(0, num):
     for j in range(0, a ):
         print(end=" ")
     for j in range(0, i+1)
     print('*' , end=" ")
print(" ")

```

## **闰年计划**

A leap year has 366 days with an extra day in the month of February. It occurs every four years. We will make a program to check if a year is a leap year or not?

![leap year-python programs-edureka](img/7850afeebc70bb275d4fa1d46e6c3d13.png)

下面是检查一年是否是闰年的程序

```
year = int(input('enter year'))
if year % 400 == 0:
  print('it is a leap year')
elif year % 4 == 0:
  print('it is a leap year')
elif year % 100 == 0:
  print('not a leap year')
else:
  print('not a leap year')

```

## **素数程序**

A prime number has only two factors, 1 and the number itself. We will make a program to check whether a number is a prime number or not.Following is the program to check if the number is a prime number or not.

```
num = int(input('enter number'))
for i range(2, num):
    if&amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;amp;nbsp; num% i == 0:
       print('not a prime number")
       break
   else:
       print('prime number')
       break

```

## **程序打印区域**

我们将采用以下形状，并尝试在 python 中计算所有这些形状的面积。

![areas-python programs-edureka](img/cd83c30d56651c852539ff0bbfdfb3b1.png)

下面是计算面积的程序

```

import math
pi = math.pi
def circle(radius):
     return pi * radius**2

def cube(side):
     return side**3

def cylinder(radius, height):
     return 2*pi*radius + 2*pi*height

def sphere(radius):
     return 2*pi*(radius**2)

print(circle(10))
#You can use other functions to calculate the areas of other shapes.

```

**Program To Reverse A List **A [list is a collection data type](https://www.edureka.co/blog/lists-in-python/) which is mutable and can contain duplicate elements as well. We will make a program to reverse a list.

![list-reverse-python programs-edureka](img/12e5088b2b62ddfceff1f41f484fbfae.png)

下面是反转列表的程序

```
a = [1,2,3,4,5,6,7,8,9,10]
print(a[: : -1])
#this will print the list in reverse.

```

In this blog, we have covered quite few logical topics in python. It is evident enough to prove how python differs from other languages and provides a much more efficient and easy to read coding platform.This brings us to the end of this blog on python programs. To master your skills in this language and kickstart your learning, enroll to [python certification program](https://www.edureka.co/data-science-python-certification-course) and discover the endless possibilities and applications of python programming language.

*有什么问题吗？在评论中提到他们，我们会回复你。*