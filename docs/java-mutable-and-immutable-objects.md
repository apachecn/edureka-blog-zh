# Java 中的可变和不可变有什么区别？

> 原文：<https://www.edureka.co/blog/java-mutable-and-immutable-objects/>

Java 是最流行的面向对象编程语言之一为创建应用程序提供了各种概念，其中一个概念在 Java 中是可变和不可变的。这个概念依赖于在对象创建后对字段进行修改，从而简化了 [Java 开发人员](https://www.edureka.co/java-j2ee-training-course)的编程。因此，在这篇关于 Java 中可变和不可变的文章中，我将讨论以下主题:

*   [什么是可变对象？](#Mutableobjects)
*   [什么是不可变对象？](#Immutableobjects)
*   [可变和不可变对象的区别](#DifferenceBetweenMutableandImmutableobjects)
*   如何创建一个可变类？
*   [如何创建不可变的类？](#CreateImmutableClass)
*   [为什么 Java 中的字符串是不可变的？](#StringsImmutableinJava)

**什么是可变对象？**

创建对象后，您可以在其中更改字段和状态的对象称为可变对象。 ***示例*** : java.util.Date、StringBuilder 等。

**什么是不可变对象？**

一旦对象被创建，你就不能改变任何东西的[对象](https://www.edureka.co/blog/java-object/)被称为不可变对象。 ***示例*** :装箱的图元对象，如整数、长整型等。

所以，现在你知道了 java 中什么是可变的和不可变的，让我们向前看，看看两者之间的区别。

**可变对象和不可变对象的区别**

关于 Java 中可变对象和不可变对象的区别，可以参考下表。

| **可变的** | **不可变** |
| 创建对象后，可以更改字段 | 创建对象后，不能更改字段 |
| 通常提供修改字段值的方法 | 没有任何修改字段值的方法 |
| 具有 Getter 和 Setter 方法 | 只有 Getter 方法 |
| 示例:StringBuilder，java.util.Date | 示例:字符串、装箱的原始对象，如整数、长整型等 |

既然您已经知道了可变对象和不可变对象之间的区别，让我们来看看如何创建这些[类。](https://www.edureka.co/blog/java-objects-and-classes/)

## 如何创建一个可变类？

要在 Java 中创建一个可变类，您必须确保满足以下要求:

1.  [提供方法](https://www.edureka.co/blog/method-overloading-and-overriding-in-java/)来修改字段值
2.  Getter 和 Setter 方法

考虑以下代码:

```

package edureka;

public class example {
private String coursename;
example(String coursename) {
this.coursename = coursename;
}
public String getName() {
return coursename;
}
public void setName(String coursename) {
this.coursename = coursename;
}
public static void main(String[] args) {
example obj = new example("Machine Learning");
System.out.println(obj.getName());

// update the name, this object is mutable
obj.setName("Machine Learning Masters");
System.out.println(obj.getName());

}
}

```

您将看到以下输出:

![Mutable Object Output - Mutable and Immutable in Java- Edureka](img/d63e7a19b84594211df2485c68960482.png)

现在你已经知道了如何创建一个可变类，接下来，让我们来看看如何创建一个不可变类。

**如何创建不可变的类？**

要在 Java 中创建一个不可变的类，您必须确保满足以下要求:

1.  一个类应该被声明为 [final](https://www.edureka.co/blog/final-finally-and-finalize-in-java/) ，这样它就不能被扩展。
2.  所有字段都应该是私有的，这样就不允许直接访问
3.  没有 setter 方法
4.  将所有可变字段设为 final，以便它们只能被赋值一次。

```

package edureka;

public class exampleimmutable {
private final String coursename;
exampleimmutable(final String coursename) {
this.coursename = coursename;
}
public final String getName() {
return coursename;
}
public static void main(String[] args) {
example obj = new example("Machine Learning");
System.out.println(obj.getName());

}
}

```

您会看到下面的输出:

好了，现在你知道了可变和不可变对象，让我告诉你在 Java 中字符串是不可变的。现在，我确信这可能提出了一个问题，为什么字符串在 Java 中是不可变的。那么，接下来在这篇文章中，让我们来看看相同的。

**为什么 Java 中的字符串是不可变的？**

Java 使用了[字符串文字](https://www.edureka.co/blog/java-string/)的概念。因此，如果你考虑一个例子，其中有许多引用变量引用一个对象，那么即使一个引用变量改变了[对象](https://www.edureka.co/blog/java-object/)的值，所有其他引用变量也会自动受到影响。另外，根据 [Effective Java](https://www.oracle.com/technetwork/java/effectivejava-136174.html) ，第二版第 4 章第 73 页，以下是使用不可变类的理由:

*   不可变对象很简单
*   这些对象不需要同步，本质上是线程安全的
*   不可变对象是其他对象的很好的构建块

如果我必须用一个例子来解释，那么，

假设你有一个变量 ***samplestring*** ，它存储了字符串“**机器学习**”。现在，如果您将这个字符串与另一个字符串 *" **Masters** "，*连接起来，那么为"**机器学习**创建的对象将不会改变。相反，将为“**机器学习大师**”创建一个新对象。参考下图:

![](img/4a16201e49f90986474a6875d7d44ee9.png)

在上图中可以看到， *samplestring* 引用变量指的是“机器学习”，而不是另一个字符串，即使是在创建了两个对象之后。至此，我们结束了这篇关于 Java 中可变和不可变的文章。我希望你们清楚我上面讨论的每一个方面。

*既然您已经了解了 Java 的基础知识，请查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在“Java 中的可变和不可变”博客的评论部分提到它，我们会尽快回复您。