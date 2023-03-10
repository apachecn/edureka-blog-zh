# Java 中的瞬态:什么，为什么&如何工作？

> 原文：<https://www.edureka.co/blog/transient-keyword-in-java/>

Java 中的 Transient 用于标记成员变量在被持久化到字节流时不被序列化。这个关键字对于满足 *[Java](https://www.edureka.co/blog/java-tutorial/)* 中的安全约束有重要作用。它忽略一个[变量](https://www.edureka.co/blog/variables-in-java/)的初始值，并保存该变量[数据类型](https://www.edureka.co/blog/data-types-in-java/)的默认值。

以下是本文将要讨论的主题:

*   [Java 中的瞬态关键字是什么？](#What_is_Transient_keyword_in_Java?)
*   [为什么使用瞬态修饰符？](#Why_is_Transient_modifier_used?)
*   【Final 关键字如何使用 Transient？
*   [瞬态和易变之间的差异](#Difference_between_Transient_and_Volatile)

我们开始吧！

## **Java 中的瞬态关键字是什么？**

Transient 基本上是一个用于序列化的变量修饰符。现在，什么是序列化？*[Java 中的序列化](https://www.edureka.co/blog/serialization-in-java/)* 是一种用于将对象的状态转换成字节流的机制。在序列化的时候，如果你不想在一个文件中保存一个特定变量的值，那么使用 transient 关键字。

**语法**:

```
private transient <member variable>;
```

或者

```
 transient private <member variable>; 
```

如果您将任何数据成员定义为瞬态的，它将不会被序列化。这是因为标记为**瞬态**的每个字段都不会被序列化。您可以使用这个 transient 关键字来指示 Java 虚拟机(JVM ),瞬态变量不是对象持久状态的一部分。

让我们写一个非常基本的例子来理解 Java 中的瞬态。

```
 class Demo implements Serializable
{
// Making human transient
private transient String human;
transient int age;
// serialize other fields
private String name, address;
Date dob;
// rest of the code
}
```

在这里，我创建了一个名为 Demo 的类，它实现了 Serializable。Demo 类的 age 数据成员被声明为瞬态的，它的值不会被序列化。但是如果你反序列化这个对象，你将得到一个临时变量的默认值。

## **为什么使用瞬态修饰符？**

Java 中的 Transient 用于指示字段不应该是序列化过程的一部分。

修饰词 Transient 可以套用至类别的成员变数，以关闭这些成员变数的序列化。每个标记为瞬态的字段都不会被序列化。您可以使用这个 transient 关键字向 [Java 虚拟机](https://www.edureka.co/blog/java-virtual-machine/)表明，瞬态变量不是对象持久状态的一部分。

你可能会有这样的疑问。什么时候在 Java 中使用这个瞬态？

这个问题的答案是:

1.  当您有从类实例中的其他字段派生/计算的字段时，可以使用此 Transient 关键字。
2.  将它用于 JDK 或应用程序代码中未标记为“可序列化”的字段。这是因为未实现 Serializable 接口的类在任何可序列化的类中被引用，不能被序列化，并将引发“Java . io . notserializableexception”异常。注意，在序列化主类之前，这些不可序列化的引用应该被标记为“transient”。

## 【Final 关键字如何使用 Transient？

Java 中的 Transient 可以与 *[final 关键字](https://www.edureka.co/blog/final-finally-and-finalize-in-java/)* 一起使用，因为它在不同的情况下表现不同，这与 Java 中的其他 *[关键字](https://www.edureka.co/blog/java-keywords/)的情况不同。*

看看这个例子。

```
private String
firstName;
private String
lastName;

//final field 1

public final transient String pass= "password";

//final field 2

public final transient Lock lock = Lock.getLock("demo");
```

现在，当您再次运行序列化(写/读)时，您将得到以下输出:

肯尼斯塔克密码空

这是因为我们已经将“传递”标记为 transient，并且该字段仍然是序列化的。对于类似的声明，锁没有序列化。原因是，每当任何 final 字段被计算为常量表达式时，就会被 JVM 序列化，而忽略 transient 关键字的存在。

## **瞬态和易变之间的差异**

这是一个在 *[Java 面试](https://www.edureka.co/blog/interview-questions/java-interview-questions/)* 中被问到的重要问题。Java 中的 transient 和 volatile 关键字有什么区别？

*[Volatile](https://www.edureka.co/blog/volatile-keyword-in-java/)* 和 Transient 是两个完全不同的关键词，用在 *[Java](https://www.edureka.co/blog/what-is-java/)* 中。在 Java 对象的序列化过程中使用了 Transient 关键字。Volatile 与多线程修改的变量的可见性有关。

这些关键字之间唯一的相似之处是，它们是较少使用或不常见的关键字，没有 public、static 或 final 那么受欢迎。

这就把我们带到了本文的结尾，我们已经了解了 Java 中的瞬态。希望你清楚本教程中与你分享的所有内容。

如果您发现这篇文章与“Java 中的瞬变”相关，请查看一下  *Edureka 的 [Java 课程](https://www.edureka.co/java-j2ee-training-course)* ，  这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。

如果你刚刚开始，那么看看这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

*我们在这里帮助你踏上成为 java 开发者的每一步。除了这个 Java 面试问题，我们还为想成为 Java 开发者的学生和专业人士设计了一个课程。该课程旨在让你在 Java 编程方面有一个良好的开端，并训练你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

如果您遇到任何问题，请在“Java 中的瞬态”的评论区自由提问，我们的团队将很乐意回答。