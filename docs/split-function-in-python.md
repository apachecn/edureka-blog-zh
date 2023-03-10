# 了解如何在 Python 中使用 Split 函数

> 原文：<https://www.edureka.co/blog/split-function-in-python/>

Python 编程语言有各种[数据类型](https://www.edureka.co/blog/variables-and-data-types-in-python/)包括字符串。即使字符串在本质上是不可变的，我们仍然可以像使用 split 函数一样使用[函数](https://www.edureka.co/blog/python-functions)来操作字符串。它使用不同的参数将较大的字符串分解成较小的字符串。在本文中，我们将了解如何在 python 中使用 split 函数。以下是本博客讨论的主题:

*   [什么是字符串？](#string)
*   [需要拆分功能？](#need)
*   [Python 中如何使用 Split 函数？](#split)
*   [分割参数](#params)
    *   [分隔符](#separator)
    *   [最大](#max)
*   [例子](#example)

## **什么是字符串？**

python 中的字符串表示 unicode 字符值。Python 没有字符数据类型，单个字符也被视为字符串。

我们用单引号或双引号来声明一个字符串。为了访问一个字符串，我们使用索引和方括号。因为字符串本质上是可变的，所以我们不能在声明一个字符串后做任何改变。

```
name = "Edureka"
print(name[0])

```

```
Output: E
```

虽然我们不能在声明后改变字符串，但我们可以在 python 中拆分字符串。

## **需要拆分功能**

Split 函数在根据给定分隔符分割字符串后返回字符串列表。以下是在 python 中使用拆分函数的优势:

*   在某些时候，我们可能不得不将一个大的字符串分解成更小的块或字符串。
*   它与串联相反，串联将两个字符串相加。
*   如果 split 函数中没有提供空格，则空格将被视为分隔符。
*   分析和推断结论变得更加容易。
*   它有助于解码加密字符串。

## **Python 中如何使用 Split 函数？**

Split 函数分解一个较大的字符串，给出一个包含较小块或字符串的列表。下面是一个用 python 拆分字符串的例子。

```
a = "We are Edureka, we have cutting edge tutorials and certification programs to upskill your knowledge"
print(a.split())

```

```
Output: [ 'We' , 'are' , 'Edureka' , 'we' , 'have' , 'cutting' , 'edge' , 'tutorials' , 'and' , 'certification' , 'programs' , 'to' , 'upskill' , 'your' , 'knowledge']
```

上面是一个简单的例子，展示了如何使用 split 函数将整个文本分解成更小的字符串。但是 split 函数有不同的参数来优化执行。

## **分割参数**

1.  分隔符–它的作用类似于分隔符，字符串根据指定的分隔符被分解。它也是可选的，如果没有指定分隔符，默认分隔符将是空白。

2.  max–它也是可选的。它定义了将要发生的拆分次数。默认值为-1，这意味着对拆分次数没有限制。

### **分隔符**

以下示例显示了带分隔符参数的 split 函数:

```
a = "Edureka is the biggest edtech company, it has many cutting edge courses to learn"
print(a.split(" , ")
b = "Sunday*Monday*Tuesday*Wednesday*Thursday*Friday*Saturday"
print(a.split(" * ")

```

```
Output: [ ' Edureka is the biggest edtech company' , 'it has many cutting edge courses to learn' ]
['Sunday' , 'Monday' , 'Tuesday' , 'Wednesday' , 'Thursday' , 'Friday' , 'Saturday' ]
```

在上面的示例中，分隔符是根据将字符串拆分为更小的字符串的方式指定的。

### **Max**

以下示例显示了带有最大参数的分割函数:

```
a = "my*name*is*python"
print(a.split(" * " , 3)

```

```
Output : [ 'my' , 'name' , 'is' , 'python' ]
```

上例中的 max 参数设置为 3，这意味着输出的字符串列表中有 4 个元素。

## **例子**

下面是几个例子，我们可以使用 split 函数将字符串分割成更小的块或字符串。

```
a = "my name is python"
print(a.split())

b = "CatDogAntCarTap"
print([b[ i : i+3] for i in range(0 , len(b) , 3)])

c = "python#was#made#by#Guido#van#rossum"
print(c.split(" #", 6)

d = " this , will , be , in , output, this will be not"
print(d.split(" , " , 4)

```

```
Output: [ 'my' , 'name' , 'is' , 'python' ]
['Cat' , 'Dog' , 'Ant' , 'Car' , 'Tap' ]
['python' , 'was' , 'made' , 'by' , 'Guido' , 'van' , 'rossum' ]
['this' , 'will' , 'be' , 'in' , 'output' ]
```

在这篇博客中，我们学习了如何使用 split 函数将大字符串分解成小块或小串。字符串是一种不可变的数据结构，这意味着一旦你声明了它，它就不能被改变。虽然可以使用分离功能进行操作。Python 编程语言有不同的数据类型，如[列表](https://www.edureka.co/blog/lists-in-python/)、[字典](https://www.edureka.co/blog/dictionary-in-python/)、[元组](https://www.edureka.co/blog/variables-and-data-types-in-python/#7)、[集合](https://www.edureka.co/blog/sets-in-python/)等。

原始数据类型和[专用数据结构](https://www.edureka.co/blog/collections-in-python/)优化你的代码，让 python 比其他编程语言更有优势。要掌握您的技能，请报名参加 [Python 在线培训](https://www.edureka.co/python-programming-certification-training)计划，开始您的学习。

*有什么问题吗？在评论中提到他们，我们会尽快回复你。*