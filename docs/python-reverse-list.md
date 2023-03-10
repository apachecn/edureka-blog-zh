# 如何在 Python 中反转列表:学习 Python List Reverse()方法

> 原文：<https://www.edureka.co/blog/python-reverse-list/>

随着 Python 编程的兴起，想要学习 Python 的人数激增以获得更好的职业机会。在浏览 [Python 基础，](https://www.edureka.co/blog/python-programming-language)时，你会意识到偶尔在 Python 中反转一个字符串会使访问数据更容易。在本文中，我们将看一个使用各种方法在 Python 中反转列表的分步教程。

本文将关注以下几点:

*   [用 list.reverse()方法反转列表](#reversingalist)
*   [使用切片技巧反转一个 Python 列表](#slicing)
*   [用 reversed()内置函数创建反向迭代器](#reverseiterator)

让我们开始吧。

## **用 list.reverse()方法反转列表**

Python 中的每个 list 都有一个内置的 reverse()方法，你可以调用这个方法来就地反转 list 对象的内容。就地反转列表意味着它不会创建现有元素并将其复制到新列表中。相反，它直接修改原始列表对象。

在我们继续之前，请确保您的系统上安装了 Python。

这里有一个例子:

**例 1:**

```
number_list = [10, 20, 30, 40, 50]
reversed_list = number_list.reverse()
print(reversed_list)
number_list = [10, 20, 30, 40, 50]
reversed_list = number_list.reverse()
print(reversed_list)
```

**输出:**

无

**例 2:**

```
string_list = [“One”, “Two”, “Three”, “Four”, “Five”]
reversed_list = string_list.reverse()
print(reversed_list)
```

**输出:**

无

**例 3:**

```
def reverse_list(list):
    print(‘Old list:’, list)
    list.reverse()
    print(‘New list:’, list)

number_list = [10, 20, 30, 40, 50]
string_list = [“One”, “Two”, “Three”, “Four”, “Five”]
reverse_list(number_list)
reverse_list(string_list)
```

**输出:**

旧单:[10，20，30，40，50] 新单:[50，40，30，20，10] 旧单:['一'，'二'，'三'，'四'，'五'] 新单:['五'，'四'，'三'，'二'，'一']

**解释**

正如你所看到的，调用 **reverse()** 返回了‘None ’,但是修改了原来的列表对象。开发人员就是这样开发 Python 标准库的。

**reverse()**方法在反转一个大的序列时，为了节省空间，就地修改序列。这样做的副作用是，它不返回一个反向列表，而是返回“None”

就地反转有一些好处，也有一些坏处。这样做的好处是，它操作非常快，因为它打乱了列表元素，并且不创建新的列表，因此节省了存储反转列表所需的内存。因为它覆盖了原始列表，这可能是一个缺点。但是，我们可以再次反转列表，使其恢复到原始状态。

语法简单易行。这意味着来自另一种语言或背景的初学者或开发人员会发现代码是可读的。

## **使用切片技巧反转一个 Python 列表**

Python 为列表提供了一个有趣的特性，叫做切片。其中您可以使用带有“[::-1]”的切片功能来生成列表的反向副本。

**这里有一个例子:**

```
def reverse_list(list):
    reversed_list = list[::-1]
    print(‘Old list:’, list)
    print(‘New list:’, reversed_list)

number_list = [10, 20, 30, 40, 50]
string_list = [“One”, “Two”, “Three”, “Four”, “Five”]
reverse_list(number_list)
reverse_list(string_list)
```

**输出:**

旧单:[10，20，30，40，50] 新单:[50，40，30，20，10] 旧单:['一'，'二'，'三'，'四'，'五'] 新单:['五'，'四'，'三'，'二'，'一'

**解释**

与就地反转相比，它创建了原始列表的浅层副本，占用了更多的内存。当它创建一个副本时，它需要更多的空间来保存所有现有的元素。

这里要注意的一点是，列表的结构是复制的，而不是包含的对象，即列表中的元素。因此，元素不会重复，从而节省了空间。此外，仅更新保存对象地址的结构中的引用。因为可变性适用于列表中包含的元素。如果对象被修改，它也将反映在其他副本中。

切片快。但是，当您浏览代码时，很难理解代码可读性的降低。因为根据场景使用合适的选项是开发者的责任。

理解使用切片编写的脚本可能非常耗时，并且难以可视化。语法很复杂，没有给出它在做什么的清晰图像。

## **用 reversed()内置函数创建反向迭代器**

reversed()函数将返回一个迭代器，我们可以用它以逆序访问元素。如果需要逆序访问列表中的单个元素，可以使用这个[函数](https://www.edureka.co/blog/python-functions)。它不会就地反转列表，也不会创建副本。

**这里有一个例子:**

```
def reverse_list(list):
    reversed_list = []
        for o in reversed(list):
            reversed_list.append(o)
    print(‘Old list:’, list)
    print(‘New list:’, reversed_list)

number_list = [10, 20, 30, 40, 50]
string_list = [“One”, “Two”, “Three”, “Four”, “Five”]
reverse_list(number_list)
reverse_list(string_list)
Output:
Old list: [10, 20, 30, 40, 50]
New list: [50, 40, 30, 20, 10]
Old list: [‘One’, ‘Two’, ‘Three’, ‘Four’, ‘Five’]
New list: [‘Five’, ‘Four’, ‘Three’, ‘Two’, ‘One’]
```

**输出:**

旧单:[10，20，30，40，50] 新单:[50，40，30，20，10] 旧单:['一'，'二'，'三'，'四'，'五'] 新单:['五'，'四'，'三'，'二'，'一']

**解释**

这个函数所做的就是，使用迭代器模式以逆序返回列表元素，这样列表元素就可以以逆序遍历。

使用列表构造函数和反向函数获得反向列表的另一种方法是压缩代码，如下所示。

```
mylist = [1, 2, 3, 4, 5]
list(reversed(mylist))
```

**输出**

[5, 4, 3, 2, 1]

**解释**

列表构造器以相反的顺序遍历列表。这种情况一直持续到到达最后一个元素。它还以给出期望输出的相反顺序创建了原始列表的浅层副本。

这段代码可读性强，易于可视化。它清楚地显示了背景中正在发生的事情。迭代器是一个重要的概念，深入理解它会有所帮助，但不是每次都要用到。

这就把我们带到了本文的结尾。在本文中，我们介绍了在 python 中反转列表的不同方法。我们已经看到了它们的利弊。如果您希望获得 Python 及其各种应用的深入知识，您可以立即注册参加实时 [Python 在线培训](https://www.edureka.co/python-programming-certification-training)，获得全天候支持和终身访问。

*有问题吗？在“用 Python 反转列表”的评论部分提到它们，我们会回复你。*