# 如何在 Python 中对字典进行排序:按键排序，按值排序

> 原文：<https://www.edureka.co/blog/how-to-sort-a-dictionary-in-python/>

Python 编程语言由原始数据类型组成，如[列表](https://www.edureka.co/blog/lists-in-python/)、[字典](https://www.edureka.co/blog/dictionary-in-python/)、[集合、元组](https://www.edureka.co/blog/variables-and-data-types-in-python/)等。它还附带了一个[集合模块](https://www.edureka.co/blog/collections-in-python/)，该模块有专门的数据结构，如 ChainMap、deque 等。使用这些数据类型变得很容易，因为它们由函数组成，这使得代码很有效。对于 python 中的字典来说，排序函数就是这样一个函数。在本文中，我们将讨论如何对字典进行排序。以下是本博客中讨论的概念:

*   什么是字典？
*   [字典中的各种操作](#operations)
*   [需要整理字典](#need)
*   [如何给字典排序？](#howtosort)

## **什么是字典？**

Dictionary 是一种集合数据类型，它包含键值对，就像其他编程语言中的映射一样。

*   Dictionary 本质上是可变的，这意味着即使在 python 中声明了 dictionary 之后也可以进行更改。
*   它是无序的，允许重复条目，只在值中，因为键必须是不同的。
*   使用关键字作为字典中的索引来访问这些值。
*   字典是用花括号声明的。

```
mydictionary = { 'key1' : 'value 1' , 'key2' : 'value 2' , 'key3' : 'value 3'}
print(mydictionary)

```

```
Output : { 'key1' : 'value 1' , 'key2' : 'value 2' , 'key3' : 'value 3'}
```

## **字典中的各种操作**

下面是我们可以在 python 中对字典执行的操作。

1.  清楚的
2.  复制
3.  fromkeys
4.  得到
5.  项目
6.  键
7.  popitem
8.  流行音乐
9.  setdefault
10.  更新
11.  价值观念

## **整理字典的需要**

*   字典具有 O(1)的搜索时间复杂度，而列表具有 O(n)的搜索时间复杂度，这使得字典在任何需要的地方都是可行的选择。
*   经过排序的字典在处理操作时会产生更好的理解和清晰度。
*   排序有助于在处理任何数据结构时进行有效的分析。

## **如何给字典排序？**

1.  按关键字排序
2.  按值排序
3.  自定义排序算法–字符串、数字
4.  颠倒排序顺序

### **按键排序**

我们可以使用内置的排序函数，它接受任何 iterable 并返回一个排序列表。我们可以使用这些键来得到一个升序排列的字典。

```
a = {1:2 ,2:1 ,4:3 ,3:4 ,6:5 ,5:6 }
#this will print a sorted list of the keys
print(sorted(a.keys()))
#this will print the sorted list with items.
print(sorted(a.items()))

```

```
Output: [1,2,3,4,5,6]
[(1,2),(2,1),(3,4),(4,3),(5,6),(6,5)]
```

### **按值排序**

就像键一样，我们也可以使用值。

```
a = {1:2 ,2:1 ,4:3 ,3:4 ,6:5 ,5:6 }
print(sorted.values()))
#this will print a sorted list of values.

```

**输出:** [ 1，2，3，4，5，6]

### **自定义排序算法–字符串，数字**

为了执行更复杂的排序，我们可以在 sorted 方法中使用其他参数。

```
day = { 'one' : 'Monday' , 'two' : 'Tuesday' , 'three' : 'Wednesday' , 'four' : 'Thursday' , 'five': 'Friday' , 'six' : 'Saturday' , 'seven': 'Sunday'}
print(day)
number = { 'one' : 1 , 'two' : 2 , 'three' : 3 , 'four' : 4 , 'five' : 5 , 'six' : 6 , 'seven' : 7}
print(sorted(day , key=number.__getitem__))
print([day[i] for i in sorted(day , key=number.__getitem__)])

```

```
Output: { 'one' : 'Monday' , 'two' : 'Tuesday' , 'three' : 'Wednesday' , 'four' : 'Thursday' , 'five': 'Friday' , 'six' : 'Saturday' , 'seven': 'Sunday'}
['one', 'two' , 'three' , 'four' , 'five' , 'six' , 'seven']
['Monday' , 'Tuesday', 'Wednesday' , 'Thursday' , 'Friday' , 'Saturday' , 'Sunday' ]
```

通过使用其他参数，我们能够使用字符串和数字以最佳方式对字典进行排序。我们也可以颠倒顺序，下面是一个颠倒排序字典顺序的例子。

### **颠倒排序顺序**

我们可以颠倒字典的排序。下面是一个颠倒排序字典顺序的例子。

```
a = {1:2 ,2:1 ,4:3 ,3:4 ,6:5 ,5:6 }
print(sorted(a.values() ,  reverse= True))

```

```
Output: [6,5,4,3,2,1]
```

在这篇博客中，我们讨论了如何用 python 对字典进行排序。字典是处理涉及键值对的数据的最佳方式。使用字典变得更加容易，因为它们在本质上是可变的，并且搜索时间的复杂度低于列表。

python 中的数据类型是一个重要的基本概念，它使 python 与众不同。由于易于访问和可读性提高，它有助于其他 python 应用程序，如[分析和数据科学](https://www.edureka.co/blog/learn-python-for-data-science/)。要掌握 python，报名参加 Edureka 的 [Python 认证](https://www.edureka.co/python-programming-certification-training)项目，开始你的学习。

*有什么问题吗？在评论中提到他们，我们会尽快回复你。*