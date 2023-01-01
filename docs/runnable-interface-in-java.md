# Java 中什么是 Runnable 接口，如何实现？

> 原文：<https://www.edureka.co/blog/runnable-interface-in-java/>

当你使用线程时，Java 中的 Runnable 接口是核心元素。任何打算执行线程的 [Java 类](https://www.edureka.co/blog/java-objects-and-classes/)都必须实现 Runnable 接口。通过这篇文章，我将向您全面介绍 Java 中的 Runnable 接口以及如何实现它。

下面是本文涉及的主题:

*   [Java 中的 Runnable 接口是什么？](#runnable)
*   [使用可运行接口的步骤](#steps)
*   [实现可运行接口](#implementing)

## **Java 中的 Runnable 接口是什么？**

java.lang.Runnable 是一种函数接口，旨在为打算在活动状态下执行代码的对象提供标准协议。换句话说，它是希望由线程执行的对象的主要模板。此外，Runnable 接口提供了一种方法，使一个类在不必子类化 Thread 的情况下也是活动的。Java 中实现 Runnable [接口的类可以在不子类化 Thread 的情况下运行。您需要做的就是实例化一个线程实例，并将其作为目标传入。当除了 run()方法之外没有其他方法可以使用时，通常会实现这个接口。](https://www.edureka.co/blog/java-interface/) 这个接口定义了一个没有参数的方法，叫做 run()，它保存了线程需要执行的代码。因此，实现 Runnable 接口的类需要覆盖 run()。

该方法不返回任何内容，因此它是用 void 数据类型定义的。下面是方法声明:

语法:

```
public void run()
```

现在让我们继续，看看在 Java 中使用 Runnable 接口的各个步骤。

## **在 Java 中使用可运行接口的步骤**

下面我列出了用 Java 实现 Runnable 接口的各个步骤:

1.  第一步是创建一个实现 Runnable 接口的类。
2.  现在，您需要在 Runnable 类中覆盖 run 方法。
3.  接下来，你需要在创建线程类对象的时候把 Runnable 对象作为参数传递给它的构造函数。现在，这个[线程对象](https://www.edureka.co/blog/java-thread/)能够执行我们的 Runnable 类。
4.  最后，你需要调用线程对象的 start 方法。

## **实现可运行接口**

下面我展示了一个用 Java 实现 Runnable 接口的演示。

```
package edureka;

public class EduRunnableDemo {

    public static void main(String[] args) {
        System.out.println("From main() : " + Thread.currentThread().getName());

        System.out.println("Creating Runnable Instance...");
        Runnable runnable = new Runnable() {
            @Override
            public void run() {
                System.out.println("From run() : " + Thread.currentThread().getName());
            }
        };

        System.out.println("Creating a Thread Instance...");
        Thread thread = new Thread(runnable);

        System.out.println("Launching a Thread...");
        thread.start();
    }
}
```

该代码将生成以下输出:

```
From main() : main
Creating Runnable Instance...
Creating a Thread Instance...
Launching a Thread...
From run() : Thread-0
```

至此，我们结束了这篇关于 Java 中可运行接口的文章。如果你想了解更多关于 Java 的知识，你可以参考我们的[其他 Java 博客](https://www.edureka.co/blog/what-is-java/)。

*既然您已经了解了 Java 中的 Runnable Interface 是什么，那么就来看看 Edureka 的* [***Java 认证培训***](https://www.edureka.co/java-j2ee-training-course)*吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这篇“Java 中的可运行接口”文章的评论部分提到它，我们会尽快回复您。