# Java 中的 JIT 是什么？–了解 Java 基础知识

> 原文：<https://www.edureka.co/blog/just-in-time-compiler/>

每一种编程语言都使用编译器将高级语言代码转换成机器级别的二进制代码，因为系统只理解二进制代码。根据编程语言的类型，编译器会有所不同。现在说的是 [Java 编程语言](https://www.edureka.co/blog/java-tutorial/)，它使用了 Java 中这个叫 ***JIT (Just-in-Time)的神奇编译器。这个博客将告诉你关于 JIT Java 编译器的一切。***

以下是本文涉及的话题:

*   [Java JIT 编译器——概述](#JavaJITCompiler%E2%80%93Overview)
*   [Java 中 JIT 编译器的工作](#WorkingofJITCompiler)
*   [Java 中 JIT 的安全方面](#SecurityaspectsofJITinJava)
*   [Java 中 JIT 的利弊](#ProsandConsofJITinJava)

那么，我们开始吧！

## **Java JIT 编译器–概述**

***实时编译器*** 是 [Java 运行时环境](https://www.edureka.co/blog/what-is-java/#ComponentsinJava)的组成部分之一。它主要负责基于 Java 的应用程序在运行时或执行时的性能优化。一般来说，编译器的主要宗旨是为最终用户和应用程序开发人员提高应用程序的性能。

### **深入研究 Java 中的 JIT**

*   字节码是 Java WORA 环境的主要潜力。Java 应用程序的速度取决于字节码转换成本机代码的方式。字节码可以被解释或编译成本机代码，或者直接在处理器上执行。但是，如果字节码被解释，它会直接影响应用程序的速度。

*   为了加快执行速度，JIT 编译器在执行时与 JVM 通信，以便将字节码序列编译成本机代码。基本上，当使用 JIT 编译器时，与 JVM 解释器相比，本机代码更容易被硬件执行。通过这样做，执行速度将会大大提高。

*   JIT 编译器在编译该系列字节码时，还会进行一定的优化，如数据分析、从堆栈操作到寄存器操作的翻译、消除子表达式等。这使得 [Java](https://www.edureka.co/blog/java-tutorial/) 在执行和性能方面非常高效。

现在你已经知道了 JIT 编译器的基础，让我们进一步了解它的工作原理。

## Java 中 JIT 编译器的工作方式

JIT 编译器在运行时提高了 Java 应用程序的性能。由于 Java 是一种面向对象的方法，它由[类和对象](https://www.edureka.co/blog/java-tutorial/#obj)组成。基本上，它构成了一个独立于平台的字节码，由 JVM 跨不同的架构执行。

**工作流程:**

下图描述了编译的实际工作是如何在 Java 运行时环境中进行的。

![JIT Compiler - JIT in Java - Edureka](img/66810584ed7a08a5a66185f65ff0a288.png)

1.  当你编写 [Java 程序](https://www.edureka.co/blog/30-pattern-programs-in-java/)时，JRE 使用 javac 编译器将高级 ***源代码编译成字节码*** 。此后，JVM 在运行时加载字节代码，并转换成机器级二进制代码，以便使用解释器进一步执行。

2.  正如我上面已经提到的，与本机应用程序相比，Java 字节码的解释降低了性能。这就是 JIT 编译器通过将字节码编译成本机代码 **【即时】** 来帮助提升性能的地方。

3.  在 Java 中调用方法时，默认情况下 JIT 编译器被激活并启用。当一个方法被编译时，Java 虚拟机直接调用该方法编译后的代码，而不解释它。因此，它不需要太多的内存使用和处理器时间。这基本上提高了 Java 本地应用程序的性能。

原来如此，这就是它的工作原理。现在让我们更深入地研究这篇文章，理解 Java 中 JIT 编译器的安全性。

## **Java 中 JIT 的安全方面**

JIT 编译器将字节码编译成机器码是直接在内存中完成的。即编译器将机器代码直接输入内存并执行。在这种情况下，在调用类文件并执行它之前，它不会将机器代码存储到磁盘中。基本上，内存应该被标记为可执行。出于安全考虑，这应该在代码写入内存后完成。它还应该标记为只读，因为可执行内存是一个安全漏洞。如果你想了解更多，你可以看看这篇关于 [JIT 编译器安全方面的文章](https://en.wikipedia.org/wiki/Just-in-time_compilation) 。

现在，让我们进一步了解 Java 中的**实时编译器**的利与弊。

## **Java 中 JIT 的利与弊**

### **优点** :

1.  你几年前编写的 Java 代码即使在今天也会运行得更快，从而提高 Java 程序的性能。

2.  原生图像也执行得更快，因为它们不具有启动活动并且需要更少的内存。

### **缺点:**

1.  增加了 [Java 程序](https://www.edureka.co/blog/java-programs/)的复杂性。

2.  代码较少的程序无法从即时编译中获益。

这就把我们带到了这篇关于 Java 中 JIT 的文章的结尾。我希望你发现它信息丰富。

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“Java 中的 JIT”文章的评论部分提到它，我们会尽快回复您。