# 通过示例了解如何使用 Python 中的地图功能

> 原文：<https://www.edureka.co/blog/map-function-in-python/>

Python 编程语言在过去十年中加快了步伐。 [python](https://www.edureka.co/data-science-python-certification-course) 编程的日益流行，为 [python 开发者](https://www.edureka.co/blog/how-to-become-a-python-developer/)在[机器学习](https://www.edureka.co/blog/videos/python-machine-learning/)、[数据科学](https://www.edureka.co/blog/learn-python-for-data-science/)等领域带来了大量需求。这种增长的主要原因之一是 python 自带的开箱即用特性。python 中的 map function 就是这样一个函数，它可以优化带有多个参数的函数的执行。在本文中，我们将详细讨论地图功能。本博客讨论了以下主题。

*   [什么是地图功能？](#mapfunction)
*   [语法](#syntax)
*   [参数](#params)
*   [例题](#examples)

## **什么是地图功能？**

map 函数提供了一个函数，iterable 中的每一项都可以作为参数传递。例如，假设我们有一个计算字符串长度的函数。使用 map 函数，我们可以用包含一串字符串的列表来指定这个函数。输出将具有列表中每个项目的长度。

## **![map function - map function in python - edureka](img/e3e3d28b001acc195d79545bdb17f7bf.png)**

## **语法**

下面是一个简单的程序，使用 map 函数来计算列表中字符串的长度。

```

def func(x):

     return len(x)

a = [ 'Sunday' , 'Monday' , 'Tuesday' , 'Wednesday' , 'Thursday' , 'Friday' , 'Saturday' ]

b = map( func , a )

print(list(b))

```

```
Output: [ 6 , 6 , 7 , 9 , 8 , 6 , 8 ]
```

## **参数**

*   [功能](https://www.edureka.co/blog/python-functions)–这是一个强制参数，存储将使用地图功能执行的功能。

*   Iterable–它存储 iterable，该 iterable 将作为函数中的参数传递。这也是一个强制参数。

```

res = map(function , iterable)

```

## **例子**

*   一次传递两个 iterables。

```

def add(a , b):

      return a + b

x = [1,3,5,7,9]

y = [2,4,6,8,10]

res = map(add , x , y)

print(list(res))

```

```
Output: [ 3 , 7 , 11 , 15 , 19]
```

*   使用 map 函数打印前 10 个自然数的立方的程序。

```

def cube(n):

      return n*n*n

a = list(range(1,11))

res = map(cube , a)

print(list(res))

```

```
Output: [1, 8, 27, 64, 125, 216, 343, 512, 729, 1000]
```

*   程序使用[λ功能](https://www.edureka.co/blog/python-lambda/)和映射功能

```

a = list(range(1,10))

res = map(lambda x : x*x , a)

print(list(res))

```

```
Output: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

我们可以在可迭代参数中使用任何数据类型，包括[集合](https://www.edureka.co/blog/sets-in-python/)、[元组](https://www.edureka.co/blog/variables-and-data-types-in-python/)、[字符串](https://www.edureka.co/blog/strings_in_python/)等。

在本文中，我们通过各种例子学习了如何在 python 中使用 map 函数。通过查看示例，可以想象 python 编程语言中的代码是多么的整洁和易读。可读性和简单的语法是 python 在过去十年中变得如此流行的众多原因之一。随着越来越受欢迎，在机器学习、人工智能、数据科学等领域的需求也在增加。要掌握您的技能，请注册 edureka 的 [python 认证计划](https://www.edureka.co/data-science-python-certification-course)，开始您的学习。

*有什么问题吗？请在评论中提及它们。我们会尽快回复你。*