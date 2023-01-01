# 如何用 Python 实现 GCD？

> 原文：<https://www.edureka.co/blog/gcd-in-python/>

在学校和大学里，我们都学过数学基础。在三角学和算术的所有复杂概念中，编程中最常用的一个概念是 GCD 或最大公约数。类似于所有的编程语言， [Python](https://www.edureka.co/blog/python-tutorial/) 也支持创建能够找到用户给定的两个数的 GCD 的代码，在本文中我们将学习如何做到这一点。让我们看看如何用 Python 实现 GCD，

*   [什么是 GCD？](#WhatIsGCD?)
*   [使用递归的 GCD](#GCDUsingRecursions)
*   [使用循环的 GCD](#GCDUsingLoops)
*   [使用欧几里德算法的 GCD](#GCDUsingTheEuclideanAlgorithm)
*   [使用数学 GCD 函数的 GCD](#%20GCDUsingMathGCDFunction)
*   [常见异常](#CommonExceptions)

让我们开始吧，

## **什么是 GCD？**

GCD 是最大公约数的缩写，这是一个数学等式，用于找出可以将用户给定的两个数相除的最大数。有时这个等式也被称为最大公因式。例如，数字 20 和 15 的最大公因数是 5，因为这两个数字都可以被 5 整除。这个概念也可以很容易地扩展到多于 2 个数字的集合，其中 GCD 将是除以用户给定的所有数字的数字。

GCD 的概念在数论中有广泛的应用，特别是 RSA 和模运算等加密技术。它有时也用于简化方程式中的分数。

现在您已经知道了 GCD 的基本概念，让我们看看如何用 Python 编写一个程序来执行同样的操作。

## **Python 中的 GCD**

为了在 Python 中计算 GCD，我们需要使用 Python 库中内置的数学函数。让我们通过几个例子来更好地理解这一点。

让我们看看如何使用递归在 Python 中找到 GCD

## **使用递归的 GCD**

```
# Python code to demonstrate naive 
# method to compute gcd ( recursion ) 
def hcfnaive(a,b): 
	if(b==0): 
		return a 
	else: 
		return hcfnaive(b,a%b) 
a = 60
b= 48
# prints 12 
print ("The gcd of 60 and 48 is : ",end="") 
print (hcfnaive(60,48)) 

```

当上面的程序运行时，输出将如下所示。

60 和 48 的 gcd 是:12

我们也可以使用循环来开始 GCD，

**使用循环的 GCD**

```
# Python code to demonstrate naive 
# method to compute gcd ( Loops ) 

def computeGCD(x, y): 
	if x > y: 
		small = y 
	else: 
		small = x 
	for i in range(1, small+1): 
		if((x % i == 0) and (y % i == 0)): 
			gcd = i 	
	return gcd 
a = 60
b= 48
# prints 12 
print ("The gcd of 60 and 48 is : ",end="") 
print (computeGCD(60,48)) 

```

当执行上面的程序时，输出将如下所示。

60 和 48 的 gcd 是:12

让我们看看下一个方法，

**使用欧几里德算法的 GCD**

```
# Python code to demonstrate naive 
# method to compute gcd ( Euclidean algo ) 
def computeGCD(x, y): 
   while(y): 
       x, y = y, x % y 
   return x 
a = 60
b= 48  
# prints 12 
print ("The gcd of 60 and 48 is : ",end="") 
print (computeGCD(60,48))

```

上述程序的输出将是，

60 和 48 的 gcd 是:12

继续，下面是 Python 中查找 GCD 的第四种方法，

**使用数学 GCD 函数的 GCD**

在使用 math.gcd()函数计算 Python 中数字的 gcd 之前，我们先来看看它的各种参数。

```
Syntax: math.gcd( x,y)
```

**参数**

x:是需要计算 gcd 的非负整数。

y:是需要计算 gcd 的第二个非负整数。

返回值:在计算了用户输入的两个数字的 GCD 之后，这个参数将返回一个绝对正的返回值。

例外:如果在某种情况下，用户输入的两个数字都是零，那么函数将返回零；如果输入是一个字符，那么函数将返回一个错误。

让我们看看示例代码，

```
# Python code to demonstrate gcd()
# method to compute gcd
import math
# prints 12
print ("The gcd of 60 and 48 is : ",end="")
print (math.gcd(60,48))
```

上述程序的输出将是，

60 岁和 48 岁的 gcd 是:12

**常见异常**

以下是使用该函数最常见的例外情况。

1.  如果用户输入的任何一个数字是零，那么函数将返回零。
2.  如果任何一个输入是字符，那么函数将返回一个类型错误。

为了更好地理解这一点，请看下面的例子。

```
# Python code to demonstrate gcd() 
# method to compute gcd 
import math 
# prints 12 
print ("The gcd of 60 and 48 is : ",end="") 
print (math.gcd(60,48)) 

```

上述程序的输出将是，

0 和 0 的 gcd 为:0

a 和 13 的 gcd 为:

运行时，上面的程序还会返回一个运行时错误，看起来像这样。

回溯(最近一次呼叫):

文件“/home/94493 cdfb 3c 8509146254862d 12 bcc 97 . py”中的第 12 行

print (math.gcd('a '，13))

type error:“str”对象不能被解释为整数

所以这就把我们带到了这篇关于 Python 中的 GCD 的文章的结尾。

*要深入了解 Python 及其各种应用，您现在就可以注册参加[最佳 Python 在线课程](https://www.edureka.co/python-programming-certification-training)培训，该培训提供全天候支持和终身访问。* *有问题吗？在这篇文章的评论部分提到它们，我们会给你回复。*