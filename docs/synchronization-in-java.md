# Java 中的同步:什么，如何，为什么？

> 原文：<https://www.edureka.co/blog/synchronization-in-java/>

多线程程序可能会经常出现这样的情况:多个 **[*Java 线程*](https://www.edureka.co/blog/java-thread/)** 试图获得相同的资源，从而产生欺骗性的惊人结果。这可以通过使用 Java 中的同步来解决。只有一个特定的线程可以在给定的时间到达资源。本文将帮助您熟悉同步策略。

我将按以下顺序讨论这些主题:

*   [为什么在 Java 中使用同步？](#Why_use_Synchronization_in_Java?)
*   [同步类型](#Types_of_Synchronization)
*   [Java 中的锁](#Locks_in_Java)
*   [无同步的多线程](#Multi_threading_without_Synchronization)
*   [多线程同步](#Multi_threading_with_Synchronization)
*   [同步关键词](#Synchronized_Keyword)
*   [同步关键字和同步块的区别](#Difference_between_synchronized_keyword_and_synchronized_block)

我们开始吧！

**为什么在 Java 中使用同步？**

如果一个程序中至少有两个线程，那么可能会有多个线程试图访问同一个资源。由于并发性问题，它甚至会产生意想不到的结果。

**语法**:

```
synchronized(objectidentifier) 
{
// Access shared variables and other shared resources;
}
```

例如，[多个线程](https://www.edureka.co/blog/java-thread/#multithreading)试图在一个等价文件中写入。这可能会损坏数据，因为其中一个线程可能会覆盖数据，或者当一个线程同时打开相同的文件时，另一个线程可能会关闭相同的文件。需要同步多个线程的动作。这可以使用一个叫做 ***M** **onitors*** 的概念来实现。

*   *Java*中的每个[对象都与一个监视器相关联，线程可以锁定或解锁该监视器。](https://www.edureka.co/blog/java-tutorial/#obj)
*   一次只有一个线程可以持有监视器上的锁。
*   *Java* 编程语言通过使用  **同步** 块，提供了一种非常方便的创建线程和同步其任务的方法。
*   它还将共享资源保存在这个特定的块中。

Java 中的同步块用 *Synchronized* 关键字标记。Java 中的这个块在某个对象上是同步的。在同一对象上同步的所有块一次只能有一个线程在其中执行。所有其他试图进入同步块的线程都被阻塞，直到同步块内的线程退出该块。

## **同步类型**

基本上有两种类型的同步可用。它们是:

1.  **进程同步:**多个线程或进程的同时执行，以达到一种状态，使得它们提交特定的动作序列。
2.  **线程同步:**当多个线程试图访问一个共享资源时，你需要确保在 一次只有一个线程使用该资源。

让我们不要进入这些类型的细节，试着理解一下 *[Java](https://www.edureka.co/blog/what-is-java/)* 中的锁是什么。

## **Java 中的锁**

正如我前面提到的，同步是围绕一个内部实体构建的，这个内部实体被称为**锁**或**监视器**。每个对象都有一个与之关联的锁。因此，需要一致访问对象字段的线程需要在访问它们之前获取对象的锁，然后在工作完成时释放锁。

从 Java 5 开始，java.util.concurrent.locks 包包含许多锁实现。

这是锁的样子:

```
public class Lock
{
private boolean isLocked = false;
public synchronized void lock() throws InterruptedException
{
while(isLocked)
{
wait();
}
isLocked = true;
}
public synchronized void unlock()
{
isLocked = false;
notify();
}
}
```

lock()方法锁定锁实例，以便所有调用 Lock()的线程都被阻塞，直到 unlock()被执行。

## **无同步的多线程**

下面是一个简单的例子，它按顺序打印计数器值，每次我们运行它时，它都会根据线程的 CPU 可用性产生不同的结果。看看这个。

```

class Multithread
{
public void printCount()
{
try
{
for(int i = 5; i<0; i--)
{
System.out.println("Counter --- " + i );
}
}
catch (Exception e)
{
System.out.println("Thread interrupted.");
}
}
}
class Thread extends Multithread
{
private Thread t;
private String threadName;
Multithread MT;
Thread( String name, Multithread mt)
{
threadName = name;
MT= mt;
}
public void run()
{
MT.printCount();
System.out.println("Thread " + threadName + " exiting.");
}
public void start ()
{
System.out.println("Starting " + threadName );
if (t == null)
{
t = new Thread (this, threadName); t.start ();
}
}
}
public class TestThread
{
public static void main(String args[])
{
Multithread MT = new Multithread();
Thread t = new Thread( "Thread - 1 ", MT);
Thread t1 = new Thread( "Thread - 2 ", MT);
t.start();
t1.start(); // wait for threads to end
try
{
t.join();
t1.join();
} catch ( Exception e)
{
System.out.println("Interrupted");
}
}
}
```

上述程序的结果如下:

![Output- Synchronization in Java- Edureka](img/c71a1b814a2123c882033593ab33cae7.png)

**多线程同步**

这与上面的例子相同，但是它在序列中打印计数器值。每次我们运行它，它都会产生相同的结果。

```
class Multithread
{
public void printCount()
{
try
{
for(int i = 5; i > 0; i--)
{
System.out.println("Counter --- " + i );
}
} catch (Exception e)
{
System.out.println("Thread interrupted.");
}
}
}
class Thread extends Multithread
{
private Thread t;
private String threadName;
Multithread MT;
Thread( String name, Multithread mt)
{
threadName = name;
MT= mt;
}
public void run()
{
synchronized(MT)
{
MT.printCount();
}
System.out.println("Thread " + threadName + " exiting.");
}
public void start ()
{
System.out.println("Starting " + threadName );
if (t == null)
{
t = new Thread (this, threadName);
t.start ();
}
}
}
public class TestThread
{
public static void main(String args[])
{
Multithread MT = new Multithread();
Thread T = new Thread( "Thread - 1 ", MT);
Thread T1 = new Thread( "Thread - 2 ", MT);
T.start();
T1.start(); // wait for threads to end
try
{
T.join();
T1.join();
} catch ( Exception e)
{
System.out.println("Interrupted");
}
}
}
```

输出如下所示:

**![Output1 - Synchronization in Java - Edureka](img/e88a6fe886d73bed555594ad78c1d0ed.png)**

**同步关键字**

**[*Java*](https://www.edureka.co/blog/java-tutorial/)synchronized 关键字** 标记一个块或一个方法的一个关键段。临界段是指一次只有一个线程在执行，并且该线程持有同步段的锁。这个**同步** 关键字有助于编写  并发  部分的任何应用程序。它还保护块内的共享资源。

synchronized 关键字可用于:

*   [一个代码块](#A_code_block)
*   [一种方法](#A_method)

我们来讨论一下代码块。

### **Synchronized 关键字:一个代码块**

**语法**

编写同步块的一般语法是:

```
synchronized ( lockObject)
{
//synchronized statements
}
```

当线程想要在块内执行同步语句时，它必须获取 lockObject 的监视器上的锁。一次只有一个线程可以获取锁对象的监视器。因此，所有其他线程必须等待，直到当前正在执行的线程获得锁并完成其执行。这样， *synchronized* 关键字保证一次只有一个线程执行同步的块语句，从而防止多个线程破坏块中的共享数据。

**注**:

*   如果线程被置于睡眠状态(使用  `sleep()` 方法)，那么它不会释放锁。在这段休眠时间内，没有线程会执行同步块语句。
*   如果“*synchronized(lock)*”中使用的锁对象为空，Java 同步将抛出 **NullPointerException** 。

现在，我们来讨论一下方法。

### **同步关键字:** **一种方法**

**语法**

编写*同步方法*的一般语法是:

```
<access modifier> synchronized method ( parameters)
{
//synchronized code
}
```

这里的**lock object**只是对一个对象的引用，该对象的锁与代表同步语句的监视器相关联。

与 synchronized 块类似，线程必须使用 synchronized 方法获取所连接的 monitor 对象上的锁。在同步方法的情况下，锁对象是:

*   **’。' class ' object**——如果给定的方法是 **static** 。
*   **‘这个’对象**——如果方法是**非静态**。“this”是对调用同步方法的当前对象的引用。

Java synchronized 关键字是  **重入** 本质上是。这意味着，如果一个同步方法调用另一个需要相同锁的同步方法，那么持有该锁的当前线程可以进入该方法，而无需获取该锁。

让我们进入本文的最后一个主题，指出 synchronized 关键字和同步块之间的主要区别。

## **同步关键字和同步块的区别**

*   当您将 synchronized 关键字与一个*方法*一起使用时，它会为整个方法获取一个对象锁。这意味着，在被调用的当前线程完成其执行之前，任何其他线程都不能使用任何同步方法。
*   指定 Synchronized 关键字后，Synchronized *块*仅在括号内获取对象中的锁。这意味着在该块退出之前，任何其他线程都不能获取已锁定对象的锁。但是其他线程将能够访问该方法中的其余代码。

这就把我们带到了本文的结尾，我们已经讨论了 Java 中的同步是如何工作的。希望你清楚本教程中与你分享的所有内容。

*查看 Edureka 提供的 [**Java 认证课程**](https://www.edureka.co/java-j2ee-training-course) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这篇“Java 中的同步*”*文章的评论部分提到它，我们会尽快回复您。*