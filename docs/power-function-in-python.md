# 如何在 Python 中实现幂函数

> 原文：<https://www.edureka.co/blog/power-function-in-python>

在当今时代， [Python](https://www.edureka.co/blog/python-tutorial/) 无疑是最突出和最流行的编程语言之一。Python 附带了许多不同的函数，每个函数都是专门构建的，为界面增加了比以前更多的功能。Python 生态系统的一个这样的函数是 power 函数，也表示为 pow()。在本文中，我们将讨论 Python 中的幂函数。

*   [Python 中的幂函数介绍？](#intro)
*   [幂函数的参数](#parameters)
*   [返回值为 Pow()](#return)
*   [示例代码](#code)

## **Python 中的幂函数介绍？**

Python 中的 power 函数可用于计算变量 x 对变量 y 的幂。如果在特定情况下，用户将第三个变量 z 包含在等式中，则 pow()函数会将 x 返回到 y 的幂，即 z 的模数。从数学术语来说，类似于 pow(x，y) % z。

幂函数的语法:

`pow(x, y[, z])`

如果你正在计算 pow (x，y)，那么输出将是，x * * y。

## **幂函数的参数**

现在，您已经熟悉了 Python 中 Power 函数的基础知识，让我们来研究一下创建 Power 函数所涉及的各种参数。

使用幂法时，需要考虑三个参数。

1.  X: x 表示需要供电的数字。

2.  Y: y 表示要用 x 乘方的数字。

3.  Z: z 是可选变量，用于导出 x 和 y 的幂模数。

**功率法的参数情况**

1.  X: X 可以是非负整数，也可以是负整数。

2.  Y: Y 在等式中使用时也可以是非负整数或负整数。

3.  Z:在大多数情况下，Z 是可选变量，可以出现也可以不出现。

## **返回值为 Pow()**

根据使用的情况，幂法返回几个不同的变量。一些最重要的问题如下所述。

| **X** | **Y** | **Z** | **返回值** |
| 非负整数 | 非负整数 | 不适用的 | **整数** |
| 非负整数 | 负整数 | 不适用的 | **浮动** |
| 负整数 | 非负整数 | 不适用的 | **整数** |
| 负整数 | 负整数 | 不适用的 | **整数** |
| 负/非负整数 | 非负整数 | 负/非负整数 | **整数** |

## **示例代码**

*   **例 1:**

```
# positive x, positive y (x**y)
print(pow(2, 2))

# negative x, positive y
print(pow(-2, 2))

# positive x, negative y (x**-y)
print(pow(2, -2))

# negative x, negative y
print(pow(-2, -2))
```

**输出:**

![Power-Function-in-Python-Output](img/123a51da3f2c07d824f78db5546fa8a8.png)

*   **例 2:**

```
x = 7
y = 2
z = 5

print(pow(x, y, z))
```

**输出:**

`4`

*   **例 3:**

```
# Python code to demonstrate naive method 
# to compute power 
n = 1
for i in range(1,5): 
	n=3*n 

print ("The value of 3**4 is : ",end="") 
print (n)
```

**输出:**

`The value of 3**4 is : 81`

*   **例 4:**

```
# Python code to demonstrate pow() 
# version 1 

print ("The value of 3**4 is : ",end="") 

# Returns 81 
print (pow(3,4))
```

**输出:**

`The value of 3**4 is : 81.0`

*   **例 5:**

```
# Python code to demonstrate pow() 
# version 2 

print ("The value of (3**4) % 10 is : ",end="") 

# Returns 81%10 
# Returns 1 
print (pow(3,4,10))
```

**输出:**

![Output-Power](img/ce7382a2cc37d6ddaeba9faafbadf66a.png)

Python 中的 power 函数，如果使用正确，可以消除很多压力和困惑。我们希望通过这篇文章，你已经学会了如何正确使用 Python 中的 power 函数，从而在你的日常编程中使用它。

*至此，我们结束了 Python 文章*中的这个幂函数。 *要深入了解 Python 及其各种应用，您现在就可以注册参加实时 [Python 课程](https://www.edureka.co/python-programming-certification-training)培训，该课程提供全天候支持和终身访问。*

*有问题吗？在这篇文章的评论部分提到它们，我们会给你回复。*