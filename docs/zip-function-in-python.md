# Python 中的 Zip 和 UnZip 函数是什么？

> 原文：<https://www.edureka.co/blog/zip-function-in-python/>

有没有想过如何从两个不同的列表中各取一个元素，并将它们配对，放入一个新的列表中？这个概念除了有趣之外，在许多专业领域也非常有用。让我们按以下顺序介绍 Python 中的 zip 函数:

*   [Python 中的 Zip 函数](#what)
*   [Python 中的 Zip 3](#python3)
*   [在 Python 中解压缩](#unzip)

## **Python 中的 Zip 函数**

![Zip Function in Python](img/ab6a3841d7a8466ce941b0960b5c95c3.png)

zip()函数是一个内置函数，它接受任意数量的 iterables 并返回一个元组列表。元组的第 I 个元素是使用来自每个可迭代对象的第 I 个元素创建的。

```
list_A = [1, 2, 3, 4]
listB = ['a', 'b', 'c', 'd']

zl= zip(listA, listB)

print zl
```

**输出:**

[(1，' a ')，(2，' b ')，(3，' c ')，(4，' d')]

## **Python 3 中的 Zip**

在 Python 3 中，当我们执行上述代码时，我们不会得到相同的结果。相反，我们会得到:

**< zip 对象在 0x01055440 >**

试试吧！

这是因为 zip 方法返回一个 zip 对象而不是一个列表。这个 zip 对象是一个迭代器。换句话说，返回一个迭代器对象，包含所有容器的映射值。因此，为了获取值，我们要么将 zl(来自上面的代码)转换为 list、set 或任何东西。

```
listA = [1, 2, 3, 4]
listB = ['a', 'b', 'c', 'd']

zl= zip(listA, listB)
zl = list(zl)

print(zl)
```

**输出:**

[(1，' a ')，(2，' b ')，(3，' c ')，(4，' d')]

## **在 Python 中解压缩**

解压缩意味着将压缩后的值转换回原来的样子。这是在“*”操作符的帮助下完成的。所以现在，如果我们想把旧值从压缩列表 zl 放入 listA 和 listB，那么我们必须解压缩 zl。

```
listA = [1, 2, 3, 4]
listB = ['a', 'b', 'c', 'd']

#zip listA and listB and put it in one list zl

zl= zip(listA, listB)
zl = list(zl)

print(zl)

#unzip zl and put the values back to listA and listB

listA, listB = zip(*zl)

print(listA)
print(listB)
```

**输出:**

[(1，' a ')，(2，' b ')，(3，' c ')，(4，' d')] (1，2，3，4) ('a '，' b '，' c '，' d ')

为了清楚地理解区别，我们取两个新变量，并将解压缩后的数据放入其中。

```
listA = [1, 2, 3, 4]
listB = ['a', 'b', 'c', 'd']

zl = zip(listA, listB)

zl = list(zl)

print(zl)

listC, listD = zip(*zl)

print(listC)

print(listD)

print(listA)

print(listB)
```

**输出:**

[(1，' a ')，(2，' b ')，(3，' c ')，(4，' d')] (1，2，3，4，5) ('a '，' b '，' c '，' d '，' e ')【1，2，3，4，5】[' a '，' b '，' c '，' d '，' e']

如您所见，listA 和 listB 是列表，listC 和 listD 显示为元组，如输出所示。这是唯一的微小区别。

至此，我们结束了 Python 文章中的这个 Zip 函数。我希望你能很好地理解这些概念，从而更准确地尝试它。

*有问题吗？请在这篇“Python 中的 Zip 函数”博客的评论部分提到它，我们会尽快回复您。*

*要深入了解 Python 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/python/) 注册我们的在线实时培训，该培训提供全天候支持和终身访问。*