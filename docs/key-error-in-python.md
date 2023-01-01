# Python 中的 KeyError 是什么？字典和处理它们

> 原文：<https://www.edureka.co/blog/key-error-in-python/>

在我们深入研究 Python 中的 KeyError 之前，了解 Python 中的字典是如何设置的是很重要的。本文将讨论以下几点:

*   [Python 中的字典](#dictionary)
*   [Python 中的 key error](#what)
*   [按键错误处理机制](#handling)
*   [通用解决方案](#generic)

## **Python 中的字典**

Python 中的[字典](https://www.edureka.co/blog/dictionary-in-python/)概念是值的随机集合，它像地图一样存储了数据值。它不像其他数据类型只保存一个值作为元素。它保存了键:值对。

![KeyError in Python](img/14c38303d4c9a170a159d4641d6bbe3f.png)

键值使它更有效率。冒号分隔键和值对，逗号分隔每个键。python 中的这个字典的功能类似于普通字典。各个键应该是唯一的，并且是不可变的数据类型，例如字符串、整数和元组，但是键值可以被迭代，并且允许是任何类型。可以有键，键是指数字的字符串，反之亦然。

让我们通过下面的例子来看看字典是如何工作的。

```
# Creating an empty Dictionary 
Dict = {} 
print("Null dict: ") 
print(Dict) 

# Creating Dictionary with Integer Keys 
Dict = {1: 'Fun', 2: 'And', 3: 'Frolic'} 
print("nDictionary with the use of Integer Keys: ") 
print(Dict) 

# Creating Dictionary with Mixed keys 
Dict = {'Name': 'Arun', 1: [12, 23, 34, 45]} 
print("nDictionary with the use of Mixed Keys: ") 
print(Dict) 

# Creating a Dictionary with dict() method 
Dict = dict({1: 'German', 2: 'language', 3:'is fun'}) 
print("nDictionary with the use of dict(): ") 
print(Dict) 

# A Dictionary having each item as a Pair 
Dict = dict([(1, 'Hello'), (2, 'Bye')]) 
print("nDictionary with each item as a pair: ") 
print(Dict)
```

## **Python 中的 key error**

因为我们清楚 python 中的字典是什么以及它是如何工作的。现在让我们看看什么是关键错误。当您试图访问一个不在字典中的键时，Python 中的 KeyError 会被引发。

映射逻辑是一种将一组数据映射到其他重要数据的数据结构。因此，这是一个错误，当访问映射但找不到映射时会引发该错误。这是一个常见的查找错误，其中语义错误会被声明为在内存中找不到您要找的键。下面的代码可以更好地说明这一点。

在这里，我试图访问一个字典中没有的名为“D”的键。因此，一旦发现异常，就会抛出错误。但是，字典中显示的正确打印的其余键具有与之对应的精确值。

```
// 
ages={'A':30,'B':28,'C':33}
print(ages['A'])
print(ages['B'])
print(ages['C'])
print(ages['D'])
//

```

## **Python 中 KeyError 的处理机制**

任何人遇到按键错误都能以负责任的方式处理。他的技能是考虑某个程序的所有可能的输入，并成功地处理任何不稳定的输入。

根据您的使用情况，其中一些解决方案可能更好，也可能不完全是您想要的解决方案。然而，最终目标是阻止意外的关键错误异常的出现。

如果您自己的代码中的字典带来了错误，您可以使用。get()提取指定键的值或默认值。让我们看一下样品。

```
//List of fruits and their prices. 

while(1):
fruits= {'Apple': 300, 'Papaya': 128, 'Kiwi': 233}
fruit= input('Get price for: ')
fruit1 = fruits.get(fruit)
if fruit1:
    print(f'{fruit} is {fruit1} rupees.')
else:
    print(f"{fruit}'s cost is unknown.")
```

## **针对 KeyError** 的通用解决方案

通常的解决方案是，您总是可以使用 try-except 块，通过生成适当的代码并提供备份解决方案来解决此类问题。为了更清楚起见，请查看下面的代码。

```
//
while(1):
 ages = {'Jophi': 12, 'Rao': 20, 'Irvin': 16} 
 person = input('Get age for: ')

 try:
    print(f'{person} is {ages[person]} years old.')
 except KeyError:
    print(f"{person}'s age is unknown.")
//
```

至此，我们结束了 Python 文章中的这个关键错误。我希望这篇文章在揭示 Python 的 KeyError 异常以及如何引发该异常方面提供了信息。另外，您现在可能意识到，如果问题是在您自己的代码中查找字典键，那么您可以从直接在字典上访问键切换到使用。带有默认返回值的 get()方法。

如果问题不是来自您自己的代码，那么使用 try-except 块来更好地控制您的代码流。

*要深入了解 Python 及其各种应用，您现在就可以注册参加实时 [Python 课程](https://www.edureka.co/python-programming-certification-training)培训，该课程提供全天候支持和终身访问。*

*有问题吗？在“Python 中的 KeyError”的评论部分提到它们，我们将会回复您。*