# 如何用 Java 编写 Hello World 程序？

> 原文：<https://www.edureka.co/blog/hello-world-program-in-java/>

任何一个 Java 程序员学习编写的第一个程序是 Java 的 Hello World 程序。但是很多时候我们错过了基本语法的本质。通过这篇文章，我将深入了解 Java 中 Hello World 程序的细节。

下面是本文涉及的主题:

*   [Java 中的 Hello World 程序](#helloworld)
*   [语法分析](#syntax)
*   [编译程序](#compile)
*   [执行程序](#execute)

让我们开始吧。

## **Java 的 Hello World 程序**

在我们进入细节之前，让我们先从编码开始，看看一个基本的 Hello World 程序是如何用 [Java](https://www.edureka.co/blog/java-tutorial/) 编写的。

```
public class HelloWorldDemo {
	public static void main(String[] args) {
		System.out.println( "Hello World!" );
        System.exit( 0 ); //success
	}
}
```

既然你已经完成了编码，现在让我们深入分析程序的语法。

## **语法分析**

**第 1 行:公共类 HelloWorldDemo {**

这一行使用关键字 [class](https://www.edureka.co/blog/java-objects-and-classes/) 来声明一个名为 HelloWorldDemo 的新类。由于 Java 是一种[面向对象编程(OOP)](https://www.edureka.co/blog/object-oriented-programming/) 语言，整个类定义，包括它的所有成员，必须包含在左花括号{和右花括号}之间。此外，它使用 public 关键字来指定该类在包外部的可访问性。

**第 2 行:public static void main(String[]args){**

这一行声明了一个名为 main(String[])的方法。 它被称为 **main** 方法，充当 [Java 编译器](https://www.edureka.co/blog/just-in-time-compiler/)开始执行程序的入口点。换句话说，每当在 Java 中执行任何程序时，main 方法都是第一个被调用的函数。然后从 main 方法调用应用程序中的其他函数。在标准的 Java 应用程序中，一个 main 方法是强制触发执行的。

现在让我们分解这一整行并分析每个单词:

***public*** :它是一个 访问修饰符，指定可见性。它允许 JVM 从任何地方执行该方法。

***静态*** :这是一个帮助任何类成员静态化的关键字。main 方法是静态的，因为不需要创建一个对象来调用 Java 中的静态方法。因此，JVM 可以调用它，而不必创建有助于节省内存的对象。

***void*** :表示方法的返回类型。因为 Java main 方法不返回任何值，所以它的返回类型被声明为 void。

***main()*** :是已经在 JVM 中配置好的方法的名称。

***String[]*** :表示 Java main 方法可以接受类型 [String array](https://www.edureka.co/blog/string-array-in-java/) 的单行参数。这也称为 java 命令行参数。下面我列出了一些有效的 java main 方法签名:

*   public static void main(String[]args)
*   public static void main(String[]args)
*   public static void main(String args[])
*   public static void main(String…args)
*   静态公共 void main(String[] args)
*   public static final void main(String[]args)
*   final public static void main(String[]args)

**第 3 行:System.out.println( "Hello World！");**

***系统* :** 它是 java.lang 包中预定义的类，保存了各种有用的方法和变量。

***out** :* 是 PrintStream 类型的静态成员字段。

***println:*** 它是 PrintStream 类的一个方法，用于打印传递给标准控制台的参数和一个换行符。也可以用 print()方法代替 println()。

**第 4 行:system . exit(0)；**

Java . lang .**系统** 。 **exit** ()方法用于通过终止当前正在执行的 Java 虚拟机来退出当前程序。该方法采用一个状态码作为输入，它通常是一个非零值 。它指示任何异常终止发生的情况。

*   *退出(0):* 用于表示终止成功。
*   *退出(1)或退出(-1)或任意非零值:*表示终止不成功。

这就是关于程序语法的全部内容。现在让我们看看如何用 Java 程序编译 Hello World。

## **编译程序**

现在你需要在你的文本编辑器中输入这个程序，用你在程序中用过的类名保存它。在我的情况下，我会将其保存为 HelloWorldDemo.java。

下一步是，转到控制台窗口，导航到保存程序的目录。

现在为了[编译程序](https://www.edureka.co/blog/how-to-compile-run-java-program/)键入下面的命令:

```
javac HelloWorldDemo.java 
```

注意:Java 是区分大小写的，因此要确保以正确的格式输入文件名。

如果成功执行，该命令将生成一个 HelloWorldDemo.class 文件，该文件将独立于机器并具有可移植性。

既然您已经成功地编译了程序，让我们试着用 Java 执行我们的 Hello World 程序并获得输出。

## **执行程序**

为了在命令行上执行你的 HelloWorld 中的 [Java 程序](https://www.edureka.co/blog/java-programs/)，你需要做的就是输入下面的代码:

```
java HelloWorldDemo
```

瞧吧！你已经成功地执行了你的第一个 Java 程序。

如果您使用的是 IDE，您可以跳过所有这些麻烦，只需按下 IDE 中的 execute 按钮，用 Java 程序编译并执行您的 Hello World。

这就把我们带到了这篇关于 JavaHello World 程序的文章的结尾。如果你想了解更多关于 Java 的知识，可以参考我们的 [**其他 Java 博客**](https://www.edureka.co/blog/java-tutorial/) 。

既然您已经了解了什么是 Java 的 Hello World 程序，那么就来看看 Edureka 的 [**Java 认证培训**](https://www.edureka.co/java-j2ee-training-course) 吧，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题吗？请在这篇“ Hello World Program in Java ”文章的评论部分提到它，我们会尽快回复您。