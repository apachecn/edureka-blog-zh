# Java HashMap vs Hashtable:有什么区别？

> 原文：<https://www.edureka.co/blog/differences-between-hashmap-and-hashtable/>

在初级阶段，最常被问到的 *[面试问题](https://www.edureka.co/blog/interview-questions/java-interview-questions/)* 之一是关于 Java HashMap vs Hashtable。所以你必须做好充分准备，回答任何与 *[HashMap](https://www.edureka.co/blog/java-hashmap/)* 或者 Hashtable 相关的问题。Java 利用 HashMap 和 Hashtable 以*键*和*值*的形式存储数据。因此，本文将帮助您了解这两者之间的主要区别。

我将按以下顺序讨论这些主题:

*   [什么是 HashMap？](#What_is_a_Hashmap?)
*   什么是哈希表？
*   [散列表 vs 散列表](#Java_HashMap_vs_Hashtable)
*   [什么时候使用 HashMap 和 Hashtable？](#When_to_use_HashMap_and_Hashtable?)

我们开始吧！

## **什么是 HashMap？**

*[HashMap](https://www.edureka.co/blog/java-hashmap/)* 是 *[Java](https://www.edureka.co/blog/java-tutorial/)* 中基于映射的集合类，用于存储键和值对中的数据。它有助于在 Java 中实现 Map 接口。它基本上是从 Java 版本 1.2 开始的 *[Java 的集合](https://www.edureka.co/blog/java-collections/)* 的一部分，提供了 Java 中 Map 接口的基本实现。要访问 HashMap 中的值，必须知道它的*键*。

它之所以被称为 HashMap，是因为它使用了一种叫做*散列*的技术。哈希是通过保持字符串的值不变，将大的 *[字符串](https://www.edureka.co/blog/java-string/)* 转换为较小的字符串的过程。产生的压缩值有助于索引和更快的搜索。

![HashMap in Java-JavaHashMap vs Hashtable-Edureka](img/2fe1b09b3b7bc85122f3bbec50f6e8f0.png)

## 什么是哈希表？

哈希表是一种 *[数据结构](https://www.edureka.co/blog/data-structures-algorithms-in-java/)* ，用于存储键/值对。在哈希表中，数据以数组格式存储，其中每个数据值都有自己唯一的索引值。如果您知道所需数据的索引，就可以非常快速地访问数据。

Java 哈希表类实现了一个哈希表，将键映射到值。它继承了 Dictionary 类并实现了 Map 接口。

![Hashtable-Java HashMap vs Hashtable-Edureka](img/aa2de14ffaacc905e903164e0b14bbc7.png)

### **哈希表声明**

公共类哈希表<k>扩展字典<k>实现映射<k>，可克隆，可序列化</k></k></k>

**K:** 它是被映射的键的类型。 **V:** 这是映射值的类型。

既然你们已经理解了 HashMap 和 Hashtable 在 Java 中是如何工作的，那么让我们看一下参数来理解 HashMap 和 Hashtable 之间的区别。

现在让我们指出 HashMap 和 Hashtable 之间的主要区别。

## **Java 哈希表 vs 哈希表**

| **参数** | **HashMap** | **哈希表** |
| **同步** | 非同步意味着它不是线程安全的，没有合适的同步代码就不能在多个线程之间共享。 | 同步的，可以被许多线程共享 |
| **空键** | 只允许一个空键和多个空值 | 不允许空键或其值 |
| **遗留系统** | 这是 Java 集合的一部分 | Hashtable 是一个遗留类，不是初始 [Java 集合](https://www.edureka.co/blog/java-collections/)的一部分 |
| **迭代器** | 迭代器是快速失败的，如果任何其他线程试图修改映射，它会抛出 concurrentModificationException | 枚举器不是故障快速的 |
| **继承类** | 继承 *AbstractMap* 类 | 继承字典类 |

现在，什么时候可以使用 Java HashMap 和 Hashtable？

## **什么时候使用 HashMap 和 Hashtable？**

*   *[同步](https://www.edureka.co/blog/synchronization-in-java/)* 是 Java HashMap 和 Hashtable 的主要区别。但是如果需要线程安全的操作，那么可以使用 Hashtable，因为它的所有方法都是同步的。但是，这是一个遗留类，必须避免它们。HashMap 不可能做到这一点。
*   对于多线程环境，可以使用 ConcurrentHashMap，它几乎类似于 Hashtable。在这里，您甚至可以显式地同步散列表
*   同步操作会导致性能下降，因此除非需要，否则应该避免使用同步操作。因此，对于非线程环境，HashMap 无疑是必不可少的。

这就把我们带到了本文的结尾，我们已经了解了 Java HashMap 和 Hashtable 之间的*差异。希望你们清楚这个话题。*

如果您觉得这篇文章与“Java HashMap vs Hashtable”相关，请查看一下 [*Edureka Java 认证培训*，](https://www.edureka.co/java-j2ee-training-course)这是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。

本课程旨在让你在 [Java 编程](https://www.edureka.co/blog/cheatsheets/java-cheat-sheet/)方面有一个良好的开端，并训练你掌握核心和高级 Java 概念以及各种 [Java 框架](https://www.edureka.co/blog/java-frameworks/)，如 Hibernate & Spring。

如果你遇到任何问题，请在“Java HashMap vs Hashtable”的评论区自由提问，我们的团队会很乐意回答。