# 如何在 Java 中练习字符串串联？

> 原文：<https://www.edureka.co/blog/string-concatenation-in-java/>

在这篇文章中，我们将告诉你在 [Java](https://www.edureka.co/blog/java-tutorial/) 中字符串连接是如何工作的，以及如果没有正确连接，它会如何影响字符串。以及如何有效地连接字符串。

本文将涉及以下几点:

*   [Java 中的字符串串联](#StringConcatenationinJava)
*   [连接字符串的不同方式](#DifferentwaystoConcatenateString)
*   [使用 StringBuffer 和 StringBuilder 类连接字符串](#ConcatenateStringusingStringBufferandStringBuilderclass)
*   [用 Java 编写不同方式的字符串连接程序](#ProgramForDifferentwaysofStringConcatenationinJava)
*   [Java 中字符串连接的性能](#PerformanceofStringconcatenationinJava)

让我们从这篇文章开始吧，

## **Java 中的字符串串联**

串联是指将一个或多个字符串附加到其他字符串上，形成一个大字符串。假设我们想要连接名字和姓氏来创建全名，我们可以使用连接来实现。

Java 中连接字符串有不同的方法，但最简单的方法是使用'+'运算符。尽管 Java 不支持操作符重载，但在字符串和+操作符的情况下，这一点是不同的。+运算符用于将两个数字相加，如果两个操作数都是整数，那么仍然是字符串，我们可以用它来连接字符串。让我们看一个连接字符串的例子

```
String fname = "Jon";
String lname = "Doe";
String newString = fname + " " + lname;
System.out.println(newString);

```

**输出**

乔恩·多伊

通过这种方式，我们可以使用+运算符连接字符串。 我们也可以通过使用 StringBuffer 和 StringBuilder 连接 String，与 String 不同，这些类是可变的，用于就地修改 String。但是，在字符串类的情况下，如果我们添加两个字符串，我们总是会得到一个新的字符串对象。

如果每次添加两个字符串时都使用+操作符添加字符串，它将在堆中创建新的对象，假设如果使用+操作符在循环中连接字符串，它可能会填满堆空间，导致内存问题。 为了解决这个问题，Java 中提供了两个类 StringBuilder 和 StringBuffer，它们是可变的，所以如果我们添加两个字符串，它不会创建一个新的 String 对象，而是会向同一个对象添加新的 String。在本文中，我们将进一步深入这个主题。

串联字符串的另一种方法是使用 String.concat()方法。现在，让我们更深入地了解使用不同方式的连接是如何工作的。

继续这篇关于 Java 中字符串连接的文章，

**连接字符串的不同方式**

*   串联运算符(+)
*   StringBuffer 类
*   StringBuilder 类
*   String.concat()函数

让我们看看如何通过不同的方法连接字符串:

继续这篇关于 Java 中字符串连接的文章，

## **使用+运算符的字符串串联**

最简单的连接方式是使用+运算符。

**例题**

```
&ldquo;hello&rdquo;+&ldquo; &rdquo; +&ldquo;edureka&rdquo;+&ldquo;!&rdquo;
```

这个例子将创建一个新的字符串:

你好，爱德华卡！

使用这个操作符，你可以添加任意数量的字符串，这将创建一个全新的字符串。我们也可以使用字符串文字或字符串变量，这两种情况都适用。这里需要注意的重要一点是，每次添加一个字符串，都会创建一个新的字符串，而不会修改任何字符串。

在字符串文字的情况下，如果该字符串已经存在于池中，它将给出该字符串的引用，但不会创建新的字符串。此外，无论何时使用+运算符进行连接，都要确保引用一个新的字符串对象。强烈建议不要在循环中使用+运算符进行连接，否则会用不必要的字符串对象填充堆空间。

继续这篇关于 Java 中字符串连接的文章，

**使用 StringBuffer 和 StringBuilder 类连接字符串**

连接多个字符串的有效方法是使用 StringBuffer 和 StringBuilder，因为这些对象是可变的，构建和追加字符串花费的时间更少。使用这些类，如果我们连接多个字符串，它不会创建任何新的对象，因为它更新相同的字符串节省内存和节省垃圾收集执行时间。此外，如果你想让执行更有效，你可以使用 StringBuilder 类，因为这个类是不同步的。下面是使用 StringBuilder 的代码:

```
String result = new StringBuilder(20).append("Hello").append(" ").append("Edureka").toString();
```

要记住的要点是，我们需要用所需的容量初始化 StringBuilder，即结果字符串中的字符数，这将通过有效分配内存和节省执行时间来节省内存。

继续这篇关于 Java 中字符串连接的文章，

**用 Java 编写不同方式的字符串连接程序**

下面是一个示例 Java 程序，它将向你展示如何使用这三种方法在 Java 中连接字符串。在第一个例子中，我们使用了+运算符，而在第二个和第三个例子中，我们使用了 StringBuilder 和 StringBuffer 类来连接 Java 中的字符串。

```
public class Concatenation
{
public static void main(String args[])
{
String stringOne = "Hello";
String stringTwo = "Edureka!";
//By using + operator
String finalString = stringOne + " " + stringOne;
System.out.println(finalString)
//by using StringBuilder
StringBuilder sb = new StringBuilder(14);
sb.append(stringOne).append(" ").append(stringTwo);
System.out.println(sb.toString())
//by using StringBuffer
StringBuffer sBuffer = new StringBuffer(15);
sBuffer.append(stringOne).append(" ").append(stringTwo);
System.out.println(sBuffer.toString());
}
}

```

继续这篇关于 Java 中字符串连接的文章，

## **Java 中字符串连接的性能**

正如我们已经看到的，我们可以在 Java 中使用+运算符轻松添加字符串。如果您想要连接固定大小的字符串，这种方法很好。但是，如果您使用+运算符添加数千个字符串，它将影响性能和内存利用率，因为它将创建多个没有引用的字符串堆，因为它们不是可变的，这将增加垃圾收集的执行时间。使用 StringBuffer 或 StringBuilder 更好，这取决于您可以使用这些类的需求，因为 StringBuffer 是线程安全的，而 StringBuilder 不是。

**总结**

在本文中，我们介绍了如何使用不同的方法连接字符串。我们使用不同的方法连接字符串，也知道哪种方法是有效的。最后，需要记住的几点如下:

在循环中串联时不要使用+运算符。

*   总是尝试使用 StringBuilder 来连接多个字符串。
*   一定要给 StringBuilder 初始容量。