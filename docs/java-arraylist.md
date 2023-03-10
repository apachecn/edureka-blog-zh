# Java 数组列表:初学者完全指南

> 原文：<https://www.edureka.co/blog/java-arraylist/>

我们都知道数组是 [Java](https://www.edureka.co/blog/cheatsheets/java-cheat-sheet/) 中的一个重要结构，可以用来存储静态数据。但是，如果您的数据需要动态存储呢？为了做到这一点， [Java](https://www.edureka.co/blog/what-is-java/) 提供了一个叫做 Java ArrayList 的特殊集合框架，专门用来存储动态数据。在本文中，我将向您介绍这种高级数组，并向您展示它们与静态数组的不同之处。以下是本教程将涉及的主题:

## **数组列表简介**

ArrayList 是 List 接口的实现，可以动态地在列表中添加或删除元素。此外，如果添加的元素超过初始大小，列表的大小会动态增加。虽然它可能比标准数组慢，但在需要对数组进行大量操作的程序中，它会很有帮助。

**![Vector - Java Collections - Edureka](img/fd7372442d32f7eb872851d3272a1022.png)**

**那么如何声明一个数组列表呢？**

很简单。声明一个数组列表如下。 *声明:***ArrayList al = new ArrayList()；** al - >是对保存对象引用的数组列表的引用。

**数组列表有什么用？**

*   Java 中的 ArrayList 用于 **存储** 一个动态大小的元素集合。
*   ArrayList 由一个大小初始化。但是，如果集合增长，大小会增加，如果从集合中移除对象，大小会缩小。
*   Java ArrayList 允许我们随机访问列表。

**Java ArrayList 教程| Java ArrayList 示例| Java 初学者教程| Edureka**



[https://www.youtube.com/embed/gmm7062i-tI?rel=0&showinfo=0](https://www.youtube.com/embed/gmm7062i-tI?rel=0&showinfo=0)

上的这段视频将通过一个例子简要介绍 Java 中的数组列表及其各种构造函数和方法。

**集合框架中数组列表的层次结构**

ArrayList 使用一个动态数组来存储元素。它继承了 AbstractList 类并实现了 List 接口。List 接口以层次顺序扩展了集合和可迭代接口。

![Hirerarchy of ArrayList-Java ArrayList-Edureka](img/5c4171f01f545c5262841bef5956df12.png)

*   **Iterable:** 它是 Java 集合类的根接口之一。该接口扩展了集合 Iterable，因此集合的所有子类型也实现了接口 Iterable。
*   **集合:**[***Java . util . Collection*s**](https://www.edureka.co/blog/java-collections/)类专门由操作或返回集合的静态方法组成。
*   **List:*****Java . util . List***是集合的子接口。它是一个有序的对象集合，其中可以存储重复的值。 ***List*** 接口由 ArrayList、LinkedList、Vector 和 Stack 类实现。
*   **抽象列表:** AbstractList 类是一个抽象类，扩展了类 AbstractCollection，实现了接口列表。
*   **ArrayList:** ArrayList 是 List 接口的实现，可以在其中动态地添加或删除列表中的元素。

#### 订阅我们的 YouTube 频道获取新的更新..！