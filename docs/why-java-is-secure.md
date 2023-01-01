# 为什么 Java 是安全语言？

> 原文：<https://www.edureka.co/blog/why-java-is-secure/>

众所周知，Java 是一个广阔的世界。你可以在 Java 中使用很多条款。它是[编程世界](https://www.edureka.co/blog/top-10-programming-languages/)中最流行的语言之一。由于它提供了许多显著的特性，它是开发人员最喜欢的语言。 [Java](https://www.edureka.co/blog/what-is-java/) 是一种非常引人注目的语言，因为它易于理解和学习。在本教程中，我将讨论 Java 最令人惊叹的特性之一——安全性！

*   [![Image-Why Java is secure- Edureka](img/d97c5b99344b5e2d1f20c72f3fda8417.png)Java 为什么安全？](#WhyJavaissecure?)
*   [确保 Java 安全的十大特性](#features)
    *   JVM
    *   [安全 API](#SecurityAPI's)
    *   [安全经理](#Securitymanager)
    *   [指针无效](#pointer)
    *   [内存管理](#memory)
    *   [编译时检查](#compiletime)
    *   [密码安全](#security)
    *   Java 沙箱
    *   [异常处理](#exceptionhandling)
    *   [Java 类加载器](#classloader)

我们开始吧。

## **为什么 Java 是安全的？**

Java 是一种非常安全的语言，因为它有下面描述的各种特性。看一看！

*   在执行之前进行字节码验证，因此程序不能跳转到恶意的或未定义的指令，也不能在指令级犯类型错误。
*   数组的自动边界检查引用的空值检查强制转换的验证防止程序犯任何类型错误。
*   每当加载新代码时，都会进行运行时安全检查。安全管理器和类加载器的使用通过协调对系统资源的访问并防止程序在运行时加载或生成任何任意代码，使得 Java 运行时可以轻松地避免任何任意代码的执行。
*   Java 提供了库级别的安全性。

下面还有一些更具技术性的功能阐述！

## **保证 Java 安全的十大特性**

*   JVM

Java 虚拟机在字节码验证中扮演着重要的角色。JVM 的任务是检查程序没有进行任何不安全的操作。有些情况下，程序会跳转到可能保存恶意数据的错误位置。JVM 保证不存在这种不安全的操作。JVM 有助于减少开发人员遭受内存安全缺陷的可能性。

让我们了解一下安全 API。

*   ### **安全 API**

Java 类库有几个与安全性相关的 API。该 API 涉及加密算法、安全通信和身份验证协议。

让我们继续讨论安全经理

*   ### **Safety Manager**

安全管理器保证可疑代码或某些恶意代码不会达到访问平台和 API 的某些特性的目的

*   ### **Pointer is invalid**

在 [Java 语言](https://www.edureka.co/blog/java-tutorial/)中没有指针的概念。指针唯一的缺点是它可以被用来引用另一个对象进行一些未授权的读写操作。这使得 Java 的安全特性岌岌可危。因此，没有指针！

*   ### **Memory management**

Java 有一个自动垃圾收集系统。它有自己的[内存管理](https://www.edureka.co/blog/java-memory-allocation)机制。当一些对象的使用完成时，用户忘记释放他们的内存。但是在 Java 的情况下，不需要腾出内存。JVM 做你的工作。

*   ### **Check**

    at compile time

例如，如果任何未授权的方法试图访问私有变量，那么在编译时 JVM 获取错误。JVM 捕捉它遇到的尽可能多的错误。

*   ### **Password security**

Java.security.SouceCode 类在 Java 中很有帮助。在从其他网络获取代码的过程中，保留代码记录变得很重要。上面提到的类，维护源信息并保留一个数字签名，以保证加密的安全性。

*   ### Java 沙箱

Java 沙箱基本上是 Java 小程序运行的禁区。这些小程序无法在没有检查的情况下获得系统资源。

*   ### **Exception handling**

在异常处理中，运行时 Java 可以通过异常处理捕捉到不希望的结果并报告给程序员。在程序员纠正它之前，代码不会运行。这个特性增加了 Java 的安全性。

*   ### **Java class loader**

在 [JVM](https://www.edureka.co/blog/java-virtual-machine/) 中有许多类装入器。加载的每个类都有不同的名称。类加载器维护特定类的名称空间。这里的目的是不可信类的行为不应该像可信类一样。

我希望现在你已经有了上述问题的答案，为什么 Java 是安全的！我以此结束本教程。继续阅读，继续探索。

现在你已经理解了 Java 为什么是安全的基础知识了吧？，查看 Edureka 的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate&[Spring](https://spring.io/projects/spring-framework)。*

有问题要问我们吗？在这篇“为什么 Java 是安全的？”的评论部分提到它博客，我们会尽快回复你。