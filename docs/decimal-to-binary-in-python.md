# 如何在 Python 中将十进制转换成二进制

> 原文：<https://www.edureka.co/blog/decimal-to-binary-in-python/>

Python 是一种高度通用且功能强大的编程语言。在人们可以做的许多事情中，从十进制到二进制的转换是最突出的。因此，在本文中，我们将更多地讨论如何在 [Python](https://www.edureka.co/blog/python-tutorial/) 中将十进制转换成二进制，反之亦然。

本文将涉及以下几点:

*   [在 Python 中把十进制转换成二进制](#ConvertingDecimalToBinaryInPython)
*   [样本程序](#SampleProgram)
*   [利用 Bin 函数](#MakingUseOfBinFunction)
*   [Python 中的二进制到十进制](#BinaryToDecimalInPython)

让我们开始吧！

要理解这个操作的意思，请看下面的例子。

从十进制到二进制

输入:8 个

输出:1 0 0 0

从二进制到十进制

输入:100

输出:4 个

让我们看看如何在 Python 中将十进制转换成二进制，

## **在 Python 中把十进制转换成二进制**

为了将十进制转换成二进制，请看下面的例子。

继续用 n/2 调用转换函数，直到 n > 1，

稍后执行 n % 1 以获得转换后的二进制数的 MSB。

**举例:** 7

1)。7/2 =商= 3(大于 1)，余数= 1。

2)。3/2 =商= 1(不大于 1)，余数= 1。

3)。1%2 =余数= 1。

因此，答案是 111。

让我们看一个示例程序，

## **样本程序**

```
# Function to print binary number for the
# input decimal using recursion
def decimalToBinary(n):
if(n > 1):
# divide with integral result
# (discard remainder)
decimalToBinary(n//2)
print(n%2, end=' ')
# Driver code
if __name__ == '__main__':
decimalToBinary(8)
print("n")
decimalToBinary(18)
print("n")
decimalToBinary(7)
print("n")&nbsp;
```

上面程序的输出看起来会像这样。

One thousand

Ten thousand and ten

One hundred and eleven

在 Python 中，我们也可以使用 bin 函数将十进制转换成二进制，让我们看看如何实现，

**利用 Bin 函数**

```
#Function to convert Decimal number 
# to Binary number 
def decimalToBinary(n): 
return bin(n).replace("0b","") 
# Driver code 
if __name__ == '__main__': 
print(decimalToBinary(8)) 
print(decimalToBinary(18)) 
print(decimalToBinary(7))
```

上面程序的输出看起来会像这样

One thousand

Ten thousand and ten

One hundred and eleven

现在你已经知道了如何在 Python 中从十进制转换成二进制，让我们来看看如何做二进制到十进制的逆运算。

## **Python 中的二进制到十进制**

为了更好地理解这一点，请参考下面的例子。

**举例:** 1011

1)。用 10 取给定二进制数的模。

(1011 % 10 = 1)

2)。将 rem 乘以 2 的幂

从右端开始的位置。

(1 * 2^0)

注意，我们从 0 开始计算位置。

3)。将结果与先前生成的结果相加。

    decimal = decimal + (1 * 2^0)

4)。通过将二进制数除以 10 来更新它。

(1011 / 10 = 101)

5)。不断重复上面的步骤，直到二进制> 0。

最终转换-: (1 * 2^3) + (0 * 2^2) +

(1 * 2^1) + (1 * 2^0) = 11

让我们看一个示例程序，

#### **样本程序**

执行上面的程序时，输出会是这样的。

four

five

nine

让我们转到 Python 文章中十进制到二进制的最后一位。

#### **样本程序**

```
# Function to convert Binary number 
# to Decimal number 
def binaryToDecimal(n): 
return int(n,2) 
# Driver code 
if __name__ == '__main__': 
print(binaryToDecimal('100')) 
print(binaryToDecimal('101'))
print(binaryToDecimal('1001'))
```

上述程序的输出将是

four

five

nine

这就把我们带到了这篇关于 Python 中十进制到二进制的文章的结尾。

*要深入了解 Python 及其各种应用，您现在就可以注册参加[最佳 Python 在线课程](https://www.edureka.co/python-programming-certification-training)培训，该培训提供全天候支持和终身访问。*

*有问题吗？在这篇文章的评论部分提到它们，我们会给你回复。*