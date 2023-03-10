# Java 中 Trim 方法是什么，如何实现？

> 原文：<https://www.edureka.co/blog/trim-method-in-java/>

[**Java**](https://www.edureka.co/java-j2ee-training-course) 提供了很多方法。在本教程中，我们将讨论其中之一，即 Java 中的 trim 方法。Java trim 方法基本上是一个**内置的**函数，它删除前导和尾随空格。让我们详细研究一下这个题目。本文的议程如下:

*   [Java 中的 Trim 方法是什么？](#Whatistrimmethodinjava?)
*   [语法](#Syntax)
*   [例子](#Example)

从定义开始！

## **Java 中的 Trim 方法是什么？**

Java trim 方法是一个**内置的**函数，可以删除前导和尾随空格。空格字符有一个特定的 **Unicode 值**–**‘u 0020’。**trim 方法定义在 **java.lang** 包的类下。每当调用 trim 方法时，都会返回一个新的 string 对象。

**注意:**这个方法不会消除[字符串](https://www.edureka.co/blog/java-string/)中间的空格。

不同的方法定位空格字符的 Unicode 值，只要它在字符串之前或之后找到它，它就消除它并返回字符串。

继续，让我们看看语法:

## **语法:**

语法非常简单。

```
public String trim()

```

现在让我们通过一个 Java 代码来实现它！

## **举例:**

```
public class Example{
     public static void main(String args[]){
           String s1=" hello Rachel ";
           System.out.println(s1+"green");//without trim()
           System.out.println(s1.trim()+"green");//with trim()
     }
}

```

**输出:** `hello Rachel green` `hello Rachelgreen`

这就是你在 Java 中实现 trim 方法的简单程度。

到此，我们来结束这篇文章*。*希望你已经通过一些实时例子了解了 Java 中的 trim 及其实现。

通过这篇文章，你已经了解了 **trim** 的基础知识，现在来看看 Edureka 的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) *，这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate&[Spring](https://spring.io/projects/spring-framework)。*

有问题要问我们吗？在这个博客的评论部分提到它，我们会尽快回复你。