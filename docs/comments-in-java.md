# Java 中的注释是什么？–了解其类型

> 原文：<https://www.edureka.co/blog/comments-in-java/>

[Java](https://www.edureka.co/blog/java-tutorial/) 中的注释是编译器和解释器不执行的语句。它可以用来提供关于变量、方法、类或任何语句的信息或解释。它还可以用于在特定时间内隐藏程序代码。让我们通过这篇文章来理解 Java 注释。

本文涵盖以下主题:

*   [Java 中有哪些注释？](#WhatareCommentsinJava?)
*   [评论类型](#TypesofComments)
    *   [单行注释](#Single-linecomments)
    *   [多行注释](#Multi-linecomments)
    *   [文档注释](#Documentationcomments)

我们开始吧！

## **Java 中有哪些注释？**

![Java - Comments in Java - Edureka](img/4c72af600551b300de29014b6eab051b.png)注释在 Java 中通常是不可执行的语句，用来更好地理解代码并使其更具可读性。如上所述，在测试替代代码时，它还有助于防止代码执行。总之，*Java 注释* 都是不可执行语句，用来更好的理解代码。

现在让我们进一步了解 Java 中各种类型的注释。

## **评论类型**

基本上，Java 中有三种类型的注释。它们如下:

*   [单行注释](#Single-linecomments)
*   [多行注释](#Multi-linecomments)
*   [文档注释](#Documentationcomments)

现在让我们进入这些评论的细节。

## **1。单行注释**

这类注释主要是用于描述代码功能。这是最容易输入的注释。单行注释以两个正斜杠(//)开始。//和行尾之间的任何文本都会被 [Java](https://www.edureka.co/blog/java-architecture/) 忽略，这意味着它不会被执行。现在，让我们举一个小例子来了解如何使用单行注释。

```
public class Example1 {
public static void main(String[] args) {
int u=100; //Here, u is a variable
System.out.println(u); // Prints the value of the variable u
}
}
```

你可以在上面的例子中看到，我已经用单行注释对程序中的特定行进行了注释。事情就是这样的。现在，我们来了解一下什么是多行注释。

## **2。多行注释**

在代码中描述一个完整的方法或者一个复杂的代码片段单行注释可能很乏味，因为我们必须在每一行都加上“//”。因此，要克服这一点，可以使用多行注释。多行注释以/*开头，以*/结尾。任何/*和*/之间的文本都会被 [Java](https://www.edureka.co/blog/advanced-java-tutorial/) 忽略。它用于注释多行代码。

现在，我们举一个小例子，了解一下多行注释的使用方法。

```
public class Example2 {
public static void main(String[] args) {
/* Here, let's declare and print
 a variable in java. */
int u=100;
System.out.println(u);
}
}
```

你可以在上面的例子中看到，我使用了多行注释来注释程序中的行。事情就是这样的。现在，让我们了解什么是文档注释。

**3。文档注释**

这种类型的注释通常在你为一个项目/软件包写代码时使用。它帮助您生成一个参考文档页面，该页面可用于获取关于现有方法及其参数等的信息。想了解更多，参考这个[链接](https://docs.oracle.com/javase/7/docs/api/java/util/Scanner.html)。

这就把我们带到了这篇关于 Java 注释的文章的结尾。我希望你发现它信息丰富。

*查看 Edureka 的 [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“Java 注释”文章的评论部分提到它，我们会尽快回复您。