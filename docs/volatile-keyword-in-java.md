# 如何用 Java 实现 Volatile 关键字？

> 原文：<https://www.edureka.co/blog/volatile-keyword-in-java/>

Java 是一种拥有大量特性的编程。在本文中，我们将探索这样一个特性，即 Java 中的 volatile 关键字。本文将涉及以下几点:

*   [挥发性关键字](#VolatileKeyword)
*   [同步和 Volatile 关键字的区别](#DifferencebetweenSynchronizationandVolatileKeyword)
*   [例子](#Example)

继续这篇关于 Java 中 Volatile 关键字的文章。

volatile 关键字用于通过不同的线程修改变量的值。它也用于使类线程安全。这意味着多个线程可以毫无问题地同时使用这些类的一个方法和实例。volatile 关键字可以用于基本类型或对象。

### 例子

```
class Test
{
static int var=5;
}

```

在上面的例子中，假设两个线程在同一个类上工作。两个线程都运行在不同的处理器上，其中每个线程都有其 var 的本地副本。如果任何一个线程修改了它的值，这种改变将不会反映在主存储器中的原始线程中。这会导致数据不一致，因为另一个线程不知道修改后的值。

```
class Test
{
static volatile int var =5;
}

```

在上面的例子中，静态变量是所有对象共享的类成员。主存里只有一份拷贝。可变变量的值永远不会存储在缓存中。所有的读写都将在主存中完成。

继续这篇关于 Java 中 Volatile 关键字的文章。

## 同步和 volatile 关键字的区别

Volatile 关键字不是 synchronized 关键字的替代品，但在某些情况下，它可以作为替代。有如下不同之处:

| **挥发性关键字** | **同步关键字** |
| Volatile 关键字是一个字段修饰符。 | Synchronized 关键字修改代码块和方法。 |
| 在 volatile 的情况下，线程不能被阻塞等待。 | 在同步的情况下，线程可以被阻塞等待。 |
| 它提高了线程性能。 | 同步方法会降低线程性能。 |
| 它在线程内存和主内存之间一次同步一个变量的值。 | 它在线程内存和主内存之间同步所有变量的值。 |
| 易变字段不受编译器优化的影响。 | 同步受到编译器优化的影响。 |

继续这篇关于 Java 中 Volatile 关键字的文章。

**举例:**

```
public class VolatileTest {
private static final Logger LOGGER = MyLoggerFactory.getSimplestLogger();
private static volatile int MY_INT = 0;
public static void main(String[] args) {
new ChangeListener().start();
new ChangeMaker().start();
}
static class ChangeListener extends Thread {
@Override
public void run() {
int local_value = MY_INT;
while ( local_value < 5){
if( local_value!= MY_INT){
LOGGER.log(Level.INFO,"Got Change for MY_INT : {0}", MY_INT);
local_value= MY_INT;
}
}
}
}
static class ChangeMaker extends Thread{
@Override
public void run() {
int local_value = MY_INT;
while (MY_INT <5){
LOGGER.log(Level.INFO, "Incrementing MY_INT to {0}", local_value+1);
MY_INT = ++local_value;
try {
Thread.sleep(500);
} catch (InterruptedException e) { e.printStackTrace(); }
}
}
}
}

```

![Image- Volatile-Edureka](img/3d2ec8d42254abceda6cf49cf920b1ed.png)

至此，我们已经结束了这篇关于“Java 中的 Volatile 关键字”的文章。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 [Java J2EE 和 SOA 培训和认证](https://www.edureka.co/java-j2ee-soa-training/)课程旨在培训你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。