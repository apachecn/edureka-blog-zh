# 了解如何在 Python 中按值对字典进行排序

> 原文：<https://www.edureka.co/blog/sort-dictionary-by-value-in-python/>

[**Python**](https://www.edureka.co/python-programming-certification-training) 是用 **C** 设计的高级编程语言。它遵循*面向对象编程*方法。在 Python 中按值排序字典是可以做的许多事情之一，在本文中，我将教你如何在 Python 中按值排序字典。

*   [先决条件:在 Python 中按值排序字典](#pre)
*   [问题陈述](#pro)
*   [接近](#app)
*   [实用示例:Python 中按值排序字典](#practical)

## **![python - edureka](img/cc5385298b68d0368f9c93ac4922d8f0.png)先决条件:****Python 中按值排序字典**

## 为了用 Python 创建一个可以按值排序字典的程序，必须满足以下先决条件。

*   **Dictionary:** 在 Python dictionary 中可以定义为一个无组织的数据集合，用于存储数据值，如地图，以及保存**键-值**对的其他元素。
*   **列表:**列表类似于 Python 中的数组；它可能包含各种数据项的集合，如字符串、整数、浮点数等。
*   **合并两个字典:**合并两个字典是 Python 中的一个内部函数，可以相当容易地实现。
*   **字典方法:**字典方法也是一个 Python 内部函数，将在这个程序的上下文中使用。

现在你知道了需要的各种先决条件，让我们开始实际编写这个程序。

## **问题陈述**

![sort-dictionary-by-value-in-python-edureka-problem statement](img/06b4151fb8fdc5346a40ae78d578baff.png)

*   **创建**一个字典，按照字母顺序排列和显示所有的关键字。
*   显示**键值**以及按字母顺序排列的名字并显示。

## **接近**

![sort-dictionary-by-value-in-python-edureka-problem solution](img/c53ceefb7e1ed2b0153225d153ea8e25.png)

为了创建一个解决上述问题陈述的程序，我们将利用以下功能和模块。

*   使用 **key_value.iterkeys()** 函数将所有的键按字母顺序排序。
*   使用排序后的 **(key_value)** 将所有值按字母顺序排序，并打印到用户的屏幕上。
*   使用函数 **key_value.iteritems()，** key = lambda (k，v) : (v，k))对最终的键值列表进行排序。

## **实际例子:Python 中按值排序字典**

![sort-dictionary-by-value-in-python-edureka-problem example](img/63d5c0d12b795a340e18dde910fdff1a.png)

既然已经解释了所有要使用的功能和模块，让我们看几个例子来更好地理解它们的实现。

**例#1**

```
def dictionairy():
key_value ={}

key_value[2] = 56
key_value[1] = 2
key_value[5] = 12
key_value[4] = 24
key_value[6] = 18
key_value[3] = 323
print ("First Taskn")
print ("Keys are")
for i in sorted (key_value.keys()) :
      print(i, end = " ")
def main():
      dictionairy()
if __name__=="__main__":
      main()

```

**//输出:**

`First Task``Keys are`

**例 2**

```
def dictionairy():
key_value ={}
key_value[2] = 56
key_value[1] = 2
key_value[5] = 12
key_value[4] = 24
key_value[6] = 18
key_value[3] = 323
print ("Task 2:-nKeys and Values sorted in", "alphabetical order by the key ")
for i in sorted (key_value) :
      print ((i, key_value[i]), end =" ")
def main():
      dictionairy()
if __name__=="__main__":
      main()

```

**//输出:**

`Task 2: -``Keys and Values sorted in alphabetical order by the key  `

**例 3**

```
def dictionairy():
key_value ={}
key_value[2] = 56
key_value[1] = 2
key_value[5] = 12
key_value[4] = 24
key_value[6] = 18
key_value[3] = 323
print ("Task 3:-nKeys and Values sorted", "in alphabetical order by the value")
print(sorted(key_value.items(), key = lambda kv:(kv[1], kv[0])))
def main():
       dictionairy()
if __name__=="__main__":
       main()

```

**//输出:**

`Task 3:-``Keys and Values sorted in alphabetical order by the value`

**例#4**

```
mydict = {"carl": 40, "alan": 2, "bob": 1, "danny": 3,}
for key in sorted(mydict.keys()):
       print("%s: %s" % (key, mydict[key]))

```

**//输出:**

`alan: 2` `bob: 1` `carl: 40`

**例#5**

```
for key, value in sorted(mydict.items(), key=lambda item: item[1]):
    print("%s: %s" % (key, value))
```

上述程序的输出将是，

`bob: 1` `alan: 2` `danny: 3`

**例#6**

```
#!/usr/bin/env python
from __future__ import print_function
scores = {
   'Foo' : 10,
   'Bar' : 34,
   'Miu' : 88,
}
print(scores) # {'Miu': 88, 'Foo': 10, 'Bar': 34}
sorted_names = sorted(scores)
print(sorted_names)  # ['Bar', 'Foo', 'Miu']
for s in sorted_names:
    print("{}  {}".format(s, scores[s]))
print(sorted(scores.values())) # [10, 34, 88]
print('')
sorted_names = sorted(scores, key=lambda x: scores[x])
for k in sorted_names:
    print("{} : {}".format(k, scores[k]))
print('')
sorted_names = sorted(scores, key=scores.__getitem__)
for k in sorted_names:
    print("{} : {}".format(k, scores[k]))

```

至此，我们结束了这篇文章我希望你已经通过一些实时例子理解了如何用 Python 对字典进行排序。

*现在你已经通过这个Python 中的按值排序字典理解了**排序**的基础知识。"查看 Edureka 的 [**Python 在线培训****g**](https://www.edureka.co/python-programming-certification-training)**，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Python 编程语言培训和认证课程是为想成为 Python 开发者的学生和专业人士设计的。该课程旨在让您在 Python 编程方面有一个良好的开端，并训练您掌握核心和高级 Python 概念以及各种 Python 框架，如[Django](https://www.djangoproject.com/)*

有问题要问我们吗？在这个博客的评论部分提到它，我们会尽快回复你。