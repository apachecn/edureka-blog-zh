# Java 中的 PrintWriter 是什么，它是如何工作的？

> 原文：<https://www.edureka.co/blog/printwriter-class-in-java/>

Java 中 writer [类的实现是 PrintWriter 类。对象的格式化表示被打印到文本输出流。让我们再深入一点，详细理解这个概念。本文的议程如下:](https://www.edureka.co/blog/types-of-classes-in-java/)

*   [Java 中的 PrintWriter 类是什么？](#WhatisprintwriterclassinJava?)
*   [PrintWriter 类的构造函数](#Constructorsofprintwriterclass)
*   [类方法](#Methodsofprintwriterclass)
*   [例子](#Example)

让我们开始吧！

从 Java 中 PrintWriter 类的定义开始！

## **Java 中的 PrintWriter 类是什么？**

Java.io.PrintWriter 类将对象的格式化表示打印到文本输出流中。这个类实现了 printstream 中的所有打印方法。

有了这个简单的定义，让我给你看看类声明。

```
public class PrintWriter
extends Writer

```

这个类[从下面的类 ● Java.io.Object 继承了](https://www.edureka.co/blog/inheritance-in-java/) [方法](https://www.edureka.co/blog/java-methods/)

现在，下一部分将告诉你 PrintWriter [类](https://www.edureka.co/blog/java-objects-and-classes/)中使用的构造函数。

## **Java 中 PrintWriter 类的构造函数**

以下是 PrintWriter 类的构造函数列表:

| **构造器** | **描述** |
| **PrintWriter(文件 File，字符串 csn)** | 此构造函数有助于创建一个没有自动行刷新的新 PrintWriter。它用指定的文件和字符集创建它。 |
| **PrintWriter(输出流输出，布尔自动刷新)** | 此构造函数有助于从现有的输出流创建新的 PrintWriter。 |
| **PrintWriter(output stream out)** | 它有助于从现有的 OutputStream 创建新的 PrintWriter |
| **PrintWriter(字符串文件名，字符串 csn)** | 它有助于创建一个新的 PrintWriter，它指定了文件名和字符集。 |
| **PrintWriter(字符串文件名)** | 它用指定的文件名创建一个新的 PrintWriter，而不自动刷新行。 |
| **PrintWriter(Writer out)** | 它创建一个新的 PrintWriter，不自动刷新行。 |
| **PrintWriter(Writer out，boolean autoFlush)** | 这将创建一个新的 PrintWriter。 |
| **PrintWriter(文件 file)** | 它用指定的文件创建一个新的 PrintWriter，不自动刷新行。 |

了解了这个类的构造函数之后，让我们来研究一下 PrintWriter 类提供的[方法](https://www.edureka.co/blog/java-methods/)。

## **类方法**

| **方法** | **描述** |
| **PrintWriter append(char sequence csq)** | 它有助于将指定的字符序列追加到这个编写器中。 |
| **PrintWriter append(char sequence csq，int start，int end)** | 它有助于将指定字符序列的子序列追加到这个编写器中。 |
| **作废关闭()** | 它关闭了溪流 |
| **boolean checkError()** | 如果流没有关闭，它就关闭它并检查它的错误状态。 |
| **受保护的 void clearError()** | 它清除该流的错误状态。 |
| **无效冲洗()** | 它冲走了溪流。 |
| **PrintWriter 格式(字符串格式，Object… args)** | 它使用指定的格式字符串和参数将格式化字符串写入此编写器。 |
| **PrintWriter 格式(区域设置 l，字符串格式，对象…参数)** | 此方法使用指定的格式字符串和参数将格式化字符串写入此编写器。 |
| **作废打印(字符 c)** | 它打印一个字符。 |
| **无效打印(浮点 f)** | 它打印一个浮点数。 |
| **作废打印(双 d)** | 它打印一个双精度浮点数。 |
| **作废打印(布尔 b)** | 它打印一个布尔值。 |
| **void print(int i)** | 它打印一个整数。 |
| **作废打印(长 l)** | 它打印一个长整数。 |
| **作废打印(对象对象)** | 它打印一个物体。 |
| **作废打印(字符串 s)** | 这个方法打印一个字符串。 |
| **void println()** | 它通过写入行分隔符字符串来终止当前行。 |
| **PrintWriter printf(字符串格式，对象…参数)** | 这是一种使用指定的格式字符串和参数将格式化字符串写入此编写器的简便方法。 |
| **PrintWriter printf(区域设置 l，字符串格式，对象…参数)** | 它使用指定的格式字符串和参数将格式化字符串写入此编写器。 |
| **void println(布尔 x)** | 它打印一个布尔值，然后终止该行。 |
| **void println(char x)** | 它打印一个字符，然后终止该行。 |
| **void println(char[] x)** | 它打印一个字符数组，然后终止该行。 |
| **void println(双 x)** | 它打印一个双精度浮点数，并因此终止该行。 |
| **void println(long x)** | 它打印一个长整数，然后终止该行。 |
| **void println(int x)** | 它打印一个整数，然后终止该行。 |
| **void println(浮点 x)** | 它打印一个浮点数，然后终止该行。 |
| **void println(对象 x)** | 它打印一个对象，然后终止该行。 |
| **void println(字符串 x)** | 它打印一个字符串，然后终止该行。 |
| **void write(char[] buf)** | 它写了一个字符数组。 |
| **void write(char[] buf，int off，int len)** | 它写入字符数组的一部分。 |
| **受保护的 void setError()** | 它表示发生了错误。 |
| **void write(int c)** | 它只写一个字符。 |
| **void write(字符串 s)** | 它写一个字符串 |

现在，让我们进入实施流程

**例子**

代码:

```
import java.io.File;
import java.io.PrintWriter;
public class Example {
public static void main(String[] args) throws Exception {
//Data to write on Console using PrintWriter
PrintWriter writer = new PrintWriter(System.out);
writer.write("Welcome to Edureka!");
writer.flush();
writer.close();
//Data to write in File using PrintWriter
PrintWriter writer1 =null;
writer1 = new PrintWriter(new File("D:testout.txt"));
writer1.write("Learn different technologies.");
writer1.flush();
writer1.close();
}
}

```

**输出:** 学习不同的技术。

至此，我们已经接近本教程的结尾。我希望你现在已经清楚这个概念了。继续阅读，继续探索！

*如果您发现这篇文章与“Java 中的 PrintWriter class”相关，请查看一下  [**Edureka Java 认证培训**](https://www.edureka.co/java-j2ee-soa-training) ，这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

我们在这里帮助你踏上旅程的每一步，并为想成为 Java 开发人员的学生和专业人士设计课程。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种  [Java 框架](https://www.edureka.co/blog/java-frameworks/) ，如[Hibernate](https://www.edureka.co/blog/what-is-hibernate-in-java/)&[Spring](https://www.edureka.co/blog/spring-tutorial/)。

如果您遇到任何问题，请在“Java 中的 PrintWriter 类”的评论部分随意提问，我们的团队将很乐意回答。