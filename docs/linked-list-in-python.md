# 如何用 Python 实现链表？

> 原文：<https://www.edureka.co/blog/linked-list-in-python/>

Python 编程语言是一种开源语言，具有各种现成的实现，这使得它独一无二且更容易学习。虽然 [Python](https://www.edureka.co/blog/python-programming-language) 不支持链表的概念，但是有一种方法可以绕过它，通过不同的实现来获得链表。在这篇文章中，我们将学习如何用 Python 制作一个链表。以下是本博客涵盖的主题:

*   [什么是链表？](#WhatisLinkedList)
*   [实现链表](#ImplementingaLinkedList)
*   [链表的方法](#Methodsoflinkedlist)

让我们开始吧！！

## **什么是链表？**

链表是具有相似数据类型的节点序列，每个节点包含一个数据对象和指向下一个节点的指针。

链表是由多个节点集合而成的线性数据结构。其中 e 每个元素存储自己的数据和一个指向下一个元素位置的指针。链表中的最后一个链接指向 null，表示链的结束。链表中的一个元素称为**节点** 。第一个节点叫做 **头** 。 最后一个节点叫做。 ![linked list - linked list in python - edureka](img/bfd78573a5a8544865050ff26afb63d5.png)标准 python 库没有链表。我们可以通过使用节点的概念来实现链表数据结构的概念。

既然我们已经了解了什么是关联的。所以让我们继续实现一个链表。

## **实现链表**

为了创建一个链表，我们创建一个节点对象，并创建另一个类来使用这个节点对象。创建节点类的代码。上面的程序创建了一个包含三个数据元素的链表。

```
class Node(object):
# Constructor to initilize class variables
def __init__(self, data=None, next_node=None):
self.data = data
self.next_node = next_node
#get data
def get_data(self):
return self.data
# get next value
def get_next(self):
return self.next_node
# set next data
def set_next(self, new_next):
self.next_node = new_next

```

链表的实现由链表中的以下功能组成 1。 **Insert** :这个方法会在链表中插入一个新的节点。 2。 **Size** :该方法将返回链表的大小。 3。 **Search** :这个方法将返回一个包含数据的节点，否则将引发一个错误 4。 **Delete** :该方法将删除包含数据的节点，否则将引发错误

让我们看看链表的方法

### **链表中的 Init 方法**

```
class LinkedList(object):
def __init__(self, head=None):
self.head = head

```

Init 方法用于初始化一个[类](https://www.edureka.co/blog/python-class/)变量，如果列表中没有节点，则将其设置为 none。

**插入:**

```
def insert(self, data):
new_node = Node(data)
new_node.set_next(self.head)
self.head = new_node

```

这个插入方法获取数据，用给定的数据初始化一个新节点，并将其添加到列表中。从技术上讲，您可以在列表中的任何位置插入一个节点，但是最简单的方法是将它放在列表的头部，并将新节点指向旧的头部(类似于将其他节点向下推)。

**尺寸**

```
# Returns total numbers of node in list
def size(self):
current = self.head
count = 0
while current:
count += 1
current = current.get_next()
return count

```

size 方法非常简单，它基本上是计数节点，直到再也找不到为止，并返回找到了多少个节点。该方法从首节点开始，沿着节点线行进，直到到达末端(当到达末端时，当前将是零)，同时跟踪它已经看到了多少个节点。

**搜索**

```
# Returns the node in list having nodeData, error occured if node not present
def search(self, nodeData):
current = self.head
isPresent = False
while current and isPresent is False:
if current.get_data() == nodeData:
isPresent = True
else:
current = current.get_next()
if current is None:
raise ValueError("Data not present in list")
return current

```

Search 实际上非常类似于 size，但是它不是遍历整个节点列表，而是在每次停止时检查当前节点是否有请求的数据。如果是，则返回保存该数据的节点。如果该方法遍历了整个列表，但仍然没有找到数据，它将引发一个值错误，并通知用户数据不在列表中。

**删除**

```
# Remove the node from linked list returns error if node not present
def delete(self, nodeData):
current = self.head
previous = None
isPresent = False
while current and isPresent is False:
if current.get_data() == nodeData:
isPresent = True
else:
previous = current
current = current.get_next()
if current is None:
raise ValueError("Data not present in list")
if previous is None:
self.head = current.get_next()
else:
previous.set_next(current.get_next())

```

delete 方法以与 search 相同的方式遍历列表，但是除了跟踪当前节点之外，delete 方法还记得访问的最后一个节点。当 delete 最终到达它想要删除的节点时。它只是通过“跳过”将该节点从链中删除。

我的意思是，当 delete 方法到达它想要删除的节点时，它会查看它访问过的最后一个节点(“前一个”节点),并重置前一个节点的指针。而不是指向即将被删除的节点。

它将指向下一个节点。因为没有节点指向被删除的差节点，所以它被有效地从列表中删除了！

这就把我们带到了本文的结尾，在这里我们学习了如何用 python 制作一个具有类似实现的链表，即使 python 并不真正支持链表的概念。我希望你清楚本教程中与你分享的所有内容。

*如果您发现这篇文章与“Python 中的链表”相关，请查看  [Edureka Python 认证培训。](https://edureka.co/python)一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*我们在这里帮助你踏上旅程的每一步，并为想要成为  [Python 开发者](https://www.edureka.co/blog/how-to-become-a-python-developer/)的学生和专业人士设计课程。该课程旨在让您在 Python 编程方面有一个良好的开端，并训练您掌握核心和高级 Python 概念以及各种  [Python 框架](https://www.edureka.co/blog/python-frameworks/) ，如  [Django。](https://www.edureka.co/blog/django-tutorial/)*

如果您遇到任何问题，请在“Python 中的链表”的评论区提出您的所有问题，我们的团队将很乐意回答。