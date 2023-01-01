# Java 中检查和未检查的异常是什么？

> 原文：<https://www.edureka.co/blog/java-checked-and-unchecked-exceptions/>

异常是任何编程语言不可或缺的一部分。在本帖中，我们将探究异常，并深入理解 [Java](https://www.edureka.co/blog/java-tutorial/) 中检查和未检查异常的概念。所以，跟我来，我们有很多东西要看，要思考。

本文将涉及以下几点:

*   [Java 中有哪些异常？](#Exception)
*   [检查异常](#Checked%20Exceptions)
*   [未检查的异常](#Unchecked%20Exceptions)

继续这篇关于 java 中已检查和未检查异常的文章。

**Java 中有哪些异常？**

在了解已检查和未检查异常的概念之前，首先让我们了解一下一般情况下什么是异常。如果你的程序包含一个依赖于某些东西的代码——假设你有一个依赖于用户输入的参数的方法。编译器会毫无问题地编译程序，因为它在语法上是正确的，但是如果用户输入的格式与您编写的方法不兼容呢？这些被称为[异常](https://www.edureka.co/blog/java-exception-handling)，作为预防措施，程序员可以在程序中对这些异常做些什么。如果你处于你无法准备的情况下，那么这被称为**错误**。

有 2 种类型的异常

1.  检查异常
2.  未检查的异常

继续这篇关于 java 中已检查和未检查异常的文章。

## **检查异常**

现在我们确切地知道什么是例外。为了理解常规形式的检查异常，让我们考虑一个例子。考虑到你正在计划一次国外旅行，你列了一张要随身携带的物品清单。除了第一份清单，你还列了一份清单，上面列有去机场前必须携带的所有必需品，如机票、护照等，你还在手机里设置了提醒，提醒你出发前必须携带的物品清单。

如果由于某种原因提醒失败，而你忘记携带机票和护照，该怎么办？在那种情况下，你将错过航班或者你将不得不回家收集物品并且返回机场。好了，现在可以解释了。现在把你的提醒当做你的[编译器](https://www.edureka.co/blog/just-in-time-compiler/)，把你在机场的状态当做运行时。编译器确保你有所有必要的项目。换句话说，它提醒你人们在出发去旅行之前最常见的错误类型，这可能会在运行时导致问题，就像你在机场的情况一样。这也能确保你在这种情况下做好准备。

如果你编写的程序包含可能产生常见的[类异常](https://www.edureka.co/blog/java-exception-handling#ExceptionTypes)的代码，编译器会提醒你运行时可能出现的异常，并告诉你用 try-catch 块或 throws 关键字处理异常。

所有的异常都属于异常类，异常类继承自 Throwable 类。

为了便于理解，我们举一个简单的例子

```
class Demo {
public static void main(String[] args)
{
FileReader file = new FileReader("Ourfile.txt");
}
}
```

## **输出**–

java:未报告异常 Java . io . file not found exception；必须被捕捉或声明被抛出

当我们试图运行这个程序时，我们得到了上面的消息。该消息指出，要么使用 try-catch 块捕获异常，要么使用 throws 关键字处理异常。

**注意-** 这里需要注意的一件重要事情是，被检查的异常不会在编译时发生。只有当我们没有处理可能发生的异常时，编译器才会提醒我们。被检查的异常只在运行时发生。

继续这篇文章，让我们了解一下 Java 中未检查的异常。

## **未检查的异常**

为了理解什么是未检查的例外，让我们考虑同一个国外旅游的例子。因此编译器会提醒您最常出现的异常。如果你到达机场后发现你的航班延误了，该怎么办？

编译器没有检查你是否准备好处理航班延误的情况。编译器不检查这种情况是很合乎逻辑的，因为这不是一个常见的异常，即使它发生了，你也不能在这种情况下做任何事情。

没有被编译器检查的异常被称为未检查异常。

我们举一个经典的例子来详细理解这个概念。

```
class Demo {

public static void main(String args[]) {
int FirstNumber = 0;
int SecondNumber = 10;
int z = SecondNumber/FirstNumber;
}
}
```

当我们编译上面的程序时，我们绝对没有错误。当我们试图**运行**编译好的程序时，问题就出现了。

```
class Demo {

   public static void main(String args[]) {
       int FirstNumber = 0;
       int SecondNumber = 10;
       int z = SecondNumber/FirstNumber;
   }
}

```

## **输出-**

线程“main”中的异常 Java . lang . arithmetic Exception:/by zero

在 Demo.main(Demo.java:10)

当我们试图运行程序时，我们收到了上述异常，因此我们可以得出结论，未检查的异常也发生在**运行时**。

在这篇文章中，我们了解了不同的异常情况。要了解如何处理这些异常，请参考这篇[帖子](https://www.edureka.co/blog/java-exception-handling)。它以简单而详细的方式解释了所有与事件处理相关的概念。

这样，我们就结束了这篇关于“Java 中检查和未检查的异常”的文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念，以及各种 [Java 框架](https://www.edureka.co/blog/java-frameworks/)，如 Hibernate & Spring。

有问题要问我们吗？请在本博客“Java 中已检查和未检查的异常”的评论部分提到它，我们会尽快回复您。