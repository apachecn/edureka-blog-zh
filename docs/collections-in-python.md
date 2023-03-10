# Python 中的集合:关于 Python 集合你需要知道的一切

> 原文：<https://www.edureka.co/blog/collections-in-python/>

Python 编程语言有四种集合数据类型——[list](https://www.edureka.co/blog/lists-in-python/)、 [tuple、sets](https://www.edureka.co/blog/variables-and-data-types-in-python/) 和 [dictionary](https://www.edureka.co/blog/dictionary-in-python/) 。但是 python 还附带了一个称为集合的内置模块，它具有专门的数据结构，基本上弥补了四种数据类型的缺点。在这篇博客中，我们将详细介绍每一种专门的数据结构。以下是这篇博客中的主题:

*   [Python 中的集合是什么？](#1)
*   [专用集合数据结构](#2)
    *   [namedtuple( )](#namedtuple)
    *   [德克](#deque)
    *   [链目录](#chainmap)
    *   [计数器](#counter)
    *   [已订购商品](#ordereddict)
    *   [defaultdict](#defaultdict)
    *   [用户词典](#userdict)
    *   [UserList](#userlist)

## **Python 中有哪些集合？**

python 中的集合基本上是容器数据类型，即列表、集合、元组、字典。基于声明和使用，它们具有不同的特征。

*   列表在方括号中声明，它是可变的，存储重复的值，并且可以使用索引访问元素。

*   一个元组本质上是有序的和不可变的，尽管在一个元组中可以有重复的条目。

*   集合是无序的，用方括号声明。它没有索引，也没有重复的条目。

*   字典有键值对，本质上是可变的。我们用方括号声明一个字典。

这些是 python 的通用内置容器数据类型。但是众所周知，python 总是能提供一些额外的东西。它附带了一个名为 collections 的 python 模块，该模块具有专门的数据结构。

## **专门收集数据结构**

python 中的 Collections [模块实现了专门的数据结构，为 python 的内置容器数据类型提供了替代方案。以下是集合模块中的专用数据结构。](https://www.edureka.co/blog/python-modules/)

1.  命名元组( )
2.  双端队列
3.  主席
4.  计数器
5.  有序直接
6.  defaultdict(预设字典)
7.  用户词典
8.  UserList
9.  用户字符串

### **名为 duple()**

它返回一个带有命名条目的元组，这意味着元组中的每个值都有一个指定的名称。它克服了使用索引值访问元素的问题。使用 namedtuple()可以更容易地访问这些值，因为您不必记住索引值来获取特定的元素。

### 它是如何工作的？

首先，你必须导入收藏模块，它不需要安装。

```

from collections import namedtuple

```

查看以下代码，了解如何使用 namedtuple。

```
a = namedtuple('courses' , 'name , tech')
s = a('data science' , 'python')
print(s)

#the output will be courses(name='python' , tech='python')

```

如何使用列表创建命名元组？

```

s._make(['data science' , 'python'])
#the output will be same as before.

```

### **德克**

发音为“deck”的 deque 是一个优化的列表，可以轻松地执行插入和删除操作。

它是如何工作的？

```

#creating a deque
from collections import deque

a = ['d' , 'u' , 'r' , 'e' , 'k']
a1 = deque(a)
print(a1)
#the output will be deque([ 'd' , 'u' , 'r' , 'e' , 'k' ])

```

现在让我们来看看如何在 deque 中插入和删除条目。

```

a1.append('a')
print(a1)
# the output will be deque([ 'd' , 'u' , 'r' , 'e' , 'k' , 'a' ])
a1.appendleft('e')
print(a1)
# the output will be deque(['e' , 'd' , 'u' , 'r' , 'e' , 'k' , 'a' ])

```

显而易见，使用 deque 可以增强组件的插入，也可以删除组件。

```

a1.pop()
print(a1)
#the output will be deque([ 'e' , 'd' , 'u' , 'r' , 'e' , 'k' ])
a1.popleft()
print(a1)
#the output will be deque([ 'd' , 'u' , 'r' , 'e' , 'k' ])

```

与内置数据类型类似，我们还可以对 deque 执行其他一些操作。像计数元素或清除队列等。

### **链图**

这是一个类似字典的类，它能够创建多个映射的单一视图。它基本上返回其他几个字典的列表。假设您有两个包含几个键值对的字典，在这种情况下，ChainMap 将创建一个包含这两个字典的列表。

它是如何工作的？

```

from collections import ChainMap
a = { 1: 'edureka' , 2: 'python'}
b = {3: 'data science' , 4: 'Machine learning'}
c = ChainMap(a,b)
print(c)
#the output will be ChainMap[{1: 'edureka' , 2: 'python'} , {3: 'data science' , 4: 'Machine learning'}]

```

为了访问或插入元素，我们使用键作为索引。但是要在链表中添加一个新的字典，我们使用下面的方法。

```

a1 = { 5: 'AI' , 6: 'neural networks'}
c1 = c.new_child(a1)
print(c1)
#the output will be ChainMap[{1: 'edureka' , 2: 'python'} , {3: 'data science' , 4: 'Machine learning'}, { 5: 'AI' , 6: 'neural networks'}]

```

### **计数器**

它是一个字典子类，用于统计可散列对象。

它是如何工作的？

```

from collections import Counter
a = [1,1,1,1,2,3,3,4,3,3,4]
c = Counter(a)
print(c)
#the output will be Counter = ({1:4 , 2:1 , 3:4 , 4:2})

```

除了可以在字典计数器上执行的操作之外，我们还可以执行另外 3 个操作。

1.  element 函数–它返回一个包含计数器中所有元素的列表。
2.  most _ common()–它返回一个排序列表，其中包含计数器中每个元素的计数。
3.  subtract()–它接受一个 iterable 对象作为参数，并减去计数器中元素的计数。

### **命令下达**

它是一个字典子类，记住条目添加的顺序。基本上，即使你改变了键的值，位置也不会因为它在字典中的插入顺序而改变。

它是如何工作的？

```

from collections import OrderedDict
od = OrderedDict()
od[1] = 'e'
od[2] = 'd'
od[3] = 'u'
od[4] = 'r'
od[5] = 'e'
od[6] = 'k'
od[7] = 'a'
print(od)
#the output will be OrderedDict[(1 , 'e'), (2 , 'd') , (3 , 'u'), (4 , 'r'), (5 , 'e'), (6 , 'k'), (7 , 'a')]

```

在字典中插入什么值并不重要，OrderedDict 会记住它的插入顺序，并相应地获得输出。即使我们改变了键值。比方说，如果我们将键值 4 更改为 8，输出中的顺序不会改变。

### **【default dict】**

它是一个字典子类，调用工厂函数来提供缺失的值。通常，当在字典中调用缺少的键值时，它不会引发任何错误。

它是如何工作的？

```

from collections import defaultdict
d = defaultdict(int)
#we have to specify a type as well.
d[1] = 'edureka'
d[2] = 'python'
print(d[3])
#it will give the output as 0 instead of keyerror.

```

### **用户词典**

这个类充当字典对象的包装器。对这个类的需求来自于直接从 dict 继承子类的需要。随着底层字典成为一个属性，使用这个类变得更加容易。

```

class collections.UserDict([initialdata])

```

这个类模拟了一个字典。实例的内容保存在一个常规的字典中，可以通过 UserDict 类的“data”属性来访问它。不保留原始数据的参考，以便用于其他目的。

### **UserList**

这个类就像是列表对象的包装器。对于其他类似 list 的类来说，它是一个有用的基类，可以从它们继承并覆盖现有的方法，甚至添加一些新的方法。

对这个类的需求来自于直接从 list 派生子类的需要。随着底层列表成为一个属性，使用这个类变得更加容易。

```

class collections.UserList([list])

```

它是一个模拟列表的类。实例的内容保存在一个习惯列表中。依赖列表的子类来提供一个构造函数，这个构造函数可以在没有或只有一个争用的情况下被调用。

在这篇博客中，我们学习了 python 中集合模块的专用数据结构。优化会带来更好的性能和增强的结果。这同样适用于我们自己的职业和技能。如果你想开始你的学习并优化你对编程的理解，注册 Edureka 的 [Python 在线课程认证](https://www.edureka.co/python-programming-certification-training)计划，释放 Python 的无限可能。

*有任何疑问吗？请在评论中提及它们，我们会尽快回复您。*