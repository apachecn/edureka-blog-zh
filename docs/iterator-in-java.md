# Java 中迭代器是什么，如何使用？

> 原文：<https://www.edureka.co/blog/iterator-in-java/>

如果你正在编写一个 [*数字程序*](https://www.edureka.co/blog/java-programs/#CalculatorPrograminJava) ，并且说你想打印一个序列，这就是 Java 中迭代器的用处。这样，即使不为每一行添加 print 语句，也可以得到序列。那么，我们来学习一下[中的迭代器 *Java*](https://www.edureka.co/blog/what-is-java/) 。

以下是我将在本模块中涉及的主题:

*   [什么是迭代器？](#What_is_an_iterator_in_Java?)
*   [Java 迭代器方法](#Java_Iterator_Methods)
*   [Java 迭代器的优点](#Advantages_of_Java_Iterator)
*   [Java 迭代器的局限性](#Limitations_of_Java_Iterator)

我们开始吧！

## **什么是迭代器？**

Java 主要支持四种不同的游标。它们是:

*   列举
*   迭代程序
*   列表迭代器
*   分裂器

这些 Java 游标各有优缺点。在本文中，我们将重点讨论迭代器。

那么，Java 中的迭代器是什么？

**迭代器**是一个属于集合框架的接口。它允许您遍历集合，访问数据元素并删除集合中的数据元素。

它也被认为是一个通用迭代器，因为你可以将它应用于任何一个 *[集合](https://www.edureka.co/blog/java-collections/)* 对象。通过使用迭代器，您可以执行读取和移除操作。这是对 *[枚举](https://www.edureka.co/blog/enumeration-in-java/)* 的改进版本，增加了移除元素的功能。

## **Java 迭代器方法**

Java 迭代器总共有 4 个方法。下面我们来详细了解一下。

| 方法 | 描述 |
| forEachRemaining(消费者 super E>行动) | 它对每个元素执行操作，直到所有元素都被处理。直到操作引发异常。 |
| 哈斯下一步() | 如果在迭代过程中遇到大量的元素，这个**返回**一个真值。 |
| 下一个() | 这个**返回**迭代中的下一个指定元素。 |
| 移除() | 这个方法移除当前元素。如果试图调用之前没有调用 next()的 remove()，则会引发 *IllegalStateException* 。 |
| 布尔 hasNext() | 如果迭代有更多元素，则返回 true。 |

示例:

```
class Method{ public static void main(String[] args)
ArrayList<String> list = new ArrayList<String>();
list.add("E");
list.add("D");
list.add("U");
list.add("R");
list.add("E");
list.add("K");
list.add("A");
// Iterator to traverse the list
Iterator iterator = list.iterator();
System.out.println("List elements : ");
while (iterator.hasNext())
System.out.print(iterator.next() + " ");
System.out.println();
}
}
```

输出:EDUREKA

我们来看看 Java 中的 ListIterator。

**Java 中的 list iterator**

Java 中的 ListIterator 是一个迭代器，允许用户双向遍历集合。它包含以下方法:

| 方法 | 方法和描述 |
| **void add(对象 obj)** | 将 obj 插入到列表中下次调用 next()将返回的元素的前面。 |
| **布尔型 hasNext( )** | 如果有下一个元素，则返回 true。否则，返回 false。 |
| **布尔 hasPrevious( )** | 如果有前一个元素，则返回 true。否则，返回 false。 |
| **下一个对象()** | 返回下一个元素。如果没有下一个元素，将引发 NoSuchElementException。 |
| **int nextIndex( )** | 返回下一个元素的索引。如果没有下一个元素，返回列表的大小。 |
| **对象上一个()** | 返回上一个元素。如果没有前一个元素，将引发 NoSuchElementException。 |
| **int previousIndex( )** | 返回前一个元素的索引。如果没有前一个元素，则返回-1。 |
| **void remove( )** | 从列表中移除当前元素。如果在调用 next()或 previous()之前调用 remove()，则会引发 IllegalStateException。 |
| **空集合(对象 obj)** | 将 obj 赋给当前元素。这是调用 next()或 previous()最后返回的元素。 |

示例:

```
public class Lists
{
public static void main(String args[])
{
// Create an array list
ArrayList al = new ArrayList();
// add elements to the array list
al.add("E");
al.add("D");
al.add("U");
al.add("R");
al.add("E");
al.add("K");
al.add("A");
// Use iterator to display contents of al
System.out.print("Original contents of al: ");
Iterator itr = al.iterator();
while(itr.hasNext())
{
Object element = itr.next();
System.out.print(element + " ");
}
System.out.println();
// Modify objects being iterated
ListIterator litr = al.listIterator();
while(litr.hasNext())
{
Object element = litr.next();
litr.set(element + "+");
}
System.out.print("Modified contents of al: ");
itr = al.iterator();
while(itr.hasNext())
{
Object element = itr.next();
System.out.print(element + " ");
}
System.out.println();
// Now, display the list backwards
System.out.print("Modified list backwards: ");
while(litr.hasPrevious())
{
Object element = litr.previous();
System.out.print(element + " ");
}
System.out.println();
}
}
```

**输出:**

原文 内容 al:E D U R E K A修改 内容 al:E+D+++R+ A+K+++R+++D+E+

现在，我们来看看 Java 中这个迭代器接口的优点和局限性。

## **Java 中迭代器的优势**

Java 中的迭代器有以下优点。

*   您可以对任何集合类使用这些迭代器。
*   Java 中的迭代器既支持**读取**操作，也支持**移除**操作。
*   如果你使用  **进行循环** ，你不能  更新(添加/删除)集合，而在迭代器的帮助下你可以很容易地更新集合。
*   它是集合 API 的通用游标。
*   方法名称非常简单，也非常容易使用。

## **Java 中迭代器的局限性**

Java 中的迭代器有以下缺点:

*   你只能执行正向迭代，也就是单向迭代器。
*   迭代器不支持新元素的替换和添加。
*   ListIterator 是最强大的迭代器，但它只适用于 List 实现的类。所以它不是通用迭代器。
*   当您使用 CRUD 操作时，它不支持创建和更新操作。
*   与 Spliterator 相比，它不允许并行迭代元素。这意味着它只支持顺序迭代。
*   它不支持迭代大量数据的更好性能。

这就把我们带到了本文的结尾，我们已经了解了 Java 中的迭代器是如何工作的。希望你清楚本教程中与你分享的所有内容。

如果您发现这篇文章与“Java 中的迭代器”相关，请查看一下  [*Edureka Java 认证培训*、](https://www.edureka.co/java-j2ee-training-course) 这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。

我们在这里帮助你踏上旅程的每一步，除此之外，我们还为想成为 Java 开发人员的学生和专业人士设计了一套课程。该课程旨在让你在 Java 编程方面有一个良好的开端，并训练你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

如果你遇到任何问题，请在“Java 迭代器”的评论区自由提问，我们的团队将很乐意回答。