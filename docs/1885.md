# 如何在 Python 中实现成员运算符

> 原文：<https://www.edureka.co/blog/membership-operators-in-python>

Python 是当今市场上最受欢迎的编程语言之一。从业余爱好者到专业人士，每个人都使用 Python，这要归功于它的大量特性以及它带来的巨大的多功能性。Python 中的 not 运算符是 Python 中成员运算符的一部分。为了更好地理解它的操作，让我们先看一下目录:

*   [Python 中的隶属运算符是什么？](#what)
*   [Python 中的身份运算符](#identity)
*   [不是](#is-not)

## **Python 中的隶属运算符是什么？**

Python 中的成员资格运算符可以定义为用于验证值的成员资格的运算符。该运算符用于测试变量中的成员资格，如字符串、整数以及元组。

![Membership Operators in Python](img/4c6f99f56333f713cda7948445645f94.png)

成员资格运算符作为一个整体包含许多不同的运算符。一些最重要的定义如下:

*   **In 运算符:**Python 中的 In 运算符用于检查值是否存在于变量中。求值时，如果运算符找到一个值，则返回 true，否则返回 false。为了更好地理解这一点，请看下面的例子。

```
# Python program to illustrate 
# Finding common member in list 
# using 'in' operator 
list1=[1,2,3,4,5] 
list2=[6,7,8,9] 
for item in list1: 
	if item in list2: 
		print("overlapping")	 
else: 
	print("not overlapping")
```

**输出:**

`not overlapping`

现在让我们修改上面的例子，去掉 in 操作符。

```
# Python program to illustrate 
# Finding common member in list 
# without using 'in' operator 

# Define a function() that takes two lists 
def overlapping(list1,list2): 

	c=0
	d=0
	for i in list1: 
		c+=1
	for i in list2: 
		d+=1
	for i in range(0,c): 
		for j in range(0,d): 
			if(list1[i]==list2[j]): 
				return 1
	return 0
list1=[1,2,3,4,5] 
list2=[6,7,8,9] 
if(overlapping(list1,list2)): 
	print("overlapping") 
else: 
	print("not overlapping")
```

**输出:**

`not overlapping`

*   **Not In 运算符:** 这个运算符与 In 运算符正好相反。计算时，如果没有找到值，该运算符返回 true，如果找到了值，则返回 false。为了更好地理解这一点，请看下面的例子。

```
# Python program to illustrate 
# not 'in' operator 
x = 24
y = 20
list = [10, 20, 30, 40, 50 ]; 

if ( x not in list ): 
 print ("x is NOT present in given list")
else: 
print ("x is present in given list")

if ( y in list ): 
 print ("y is present in given list")
else: 
 print ("y is NOT present in given list")
```

**输出:**

`x is NOT present in given list`

`y is present in given list`

## **Python 中的恒等运算符**

除了成员资格运算符，Python 中还有另一种类型的运算符，称为 ad Identity 运算符。在 Python 中，标识运算符用于检查特定值是否属于某个类或类型。在大多数情况下，恒等运算符用于定义某个变量包含的数据类型。Python 中有两种主要类型的标识运算符。

*   **Is 运算符:** 在求值时，Python 中的 Is 运算符如果运算符两边的变量都指向同一个变量，则返回 true，否则返回 false。为了更好地理解这一点，请看下面的例子。

```
# Python program to illustrate the use 
# of 'is' identity operator 
x = 6
if (type(x) is int): 
	print ("true") 
else: 
	print ("false")
```

**输出:**

`True`

让我们再举一个“in”运算符的例子。

```
x = ["apple", "banana"]

print("banana" is x)

# returns True because a sequence with the value "banana" is in the list
```

**输出:**

`True`

## **不是操作员**

Python 中的 is not 运算符与 is 运算符完全相反。计算时，如果运算符两边的变量指向同一个对象，则运算符返回 false，否则返回 false。为了更好地理解这一点，请看下面的例子。

```
# Python program to illustrate the 
# use of 'is not' identity operator 
x = 7.2
if (type(x) is not int): 
	print ("true") 
else: 
	print ("false")
```

**输出:**

`True`

让我们再举一个这个运算符的例子。

```
x = ["apple", "banana"]

print("pineapple" not in x)

# returns True because a sequence with the value "pineapple" is not in the list
```

**输出:**

`True`

Python 中的标识操作符和成员操作符都可以交替使用，从长远来看，这样可以使你的程序更加高效。因此，建议您在日常编程中同时使用这两种方法，至此，我们结束了这篇“Python 中的成员操作符”文章。

*要深入了解 Python 及其各种应用，您现在就可以注册参加[最佳 Python 在线课程](https://www.edureka.co/python-programming-certification-training)培训，该培训提供全天候支持和终身访问。*

*有问题吗？在“Python 中的成员操作符”的评论部分提到它们，我们会回复您。*