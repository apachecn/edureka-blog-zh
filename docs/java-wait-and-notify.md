# Java 中的等待和通知是什么？

> 原文：<https://www.edureka.co/blog/java-wait-and-notify/>

*[多线程](https://www.edureka.co/blog/java-thread/)*Java 中的特性允许同时执行一个程序的两个或多个部分。每一部分都是一根线。这些线程经常需要协调它们的动作。这是通过使用 Java 中的 Wait 和 Notify 等一些最终方法来完成的。本文将帮助您详细了解这些方法。

我将按以下顺序讨论这些话题:

*   [什么是线程同步？](#What_is_Thread_Synchronization?)
*   [什么是 Wait()和 Notify()方法？](#What_are_Wait()_and_Notify()_methods?)
*   [为什么以及如何在 Java 中使用 Wait()和 Notify()。](#Why_and_how_to_use_Wait()_and_Notify()_in_Java?)
*   [例题](#Example)

我们开始吧！

## **什么是线程同步？**

多线程程序可能会经常出现这样的情况:多个 **[*Java 线程*](https://www.edureka.co/blog/java-thread/)** 试图获得相同的资源，从而产生欺骗性的惊人结果。有时，多个线程可能试图访问一个共享资源，您需要确保一次只有一个线程使用该资源。这可以使用 Java 中的 ***[同步来完成。](https://www.edureka.co/blog/synchronization-in-java/)***

现在谈谈投票。轮询是一个反复测试条件直到它为真的过程。这种方法是借助 ***[循环](https://www.edureka.co/blog/loops-in-java/)*** 来检查某个特定条件是否成立。你可以对线程使用这种方法，但是这种方法浪费了大量的 CPU 周期，而且使得执行过程非常低效。为了避免这类错误，Java 中引入了 Wait 和 Notify 之类的方法。

## **什么是 Wait()和 Notify()方法？**

为了解决多线程问题，使用了类似于 Java 中的 Wait 和 Notify 的方法。Object 类使用这三个最终方法，允许线程就资源的锁定状态进行通信。它们也被称为保护块。

### **等待()**

该方法使线程等待，直到另一个线程调用该对象的 notify()和 notifyAll()方法。这个 Wait()方法告诉调用线程释放一个锁并进入睡眠状态，直到另一个线程进入同一个监视器并调用 notify()。该方法在等待之前释放锁，并在从 wait()方法返回之前重新获取锁。

Wait()方法与同步锁紧密集成。这是通过使用不能直接从同步机制获得的特征来完成的。

**语法:**

```
synchronized( lockObject )
{
while( ! condition )
{
lockObject.wait();
}
//take the action here;
}
```

当前线程必须拥有其对象的监视器。它必须只能从 synchronized 方法中调用，否则将引发异常。

### **通知()**

该方法用于通知[线程](https://www.edureka.co/blog/java-thread/)它需要运行。它唤醒一个线程，该线程在同一个对象上调用了 *wait()* 方法。

注意，调用 *notify()* 最终不会放弃锁。它告诉一个等待的线程它可以被唤醒。但是，直到通知程序的同步块完成后，锁才真正被放弃。现在假设，如果您在一个资源上调用 *notify()* ，但是通知程序仍然需要在其同步块内执行 10 秒钟的动作，那么一直在等待的线程将不得不至少再等待 10 秒钟，以便通知程序释放对象上的锁，即使已经调用了 notify()。

**语法:**

```
synchronized(lockObject)
{
//establish_the_condition;
lockObject.notify();
//any additional code if needed
}
```

### **NotifyAll()**

这个方法用于唤醒所有在同一个对象上调用 wait()的线程。在大多数情况下，优先级最高的线程将首先运行，尽管这并不能保证。其他的和 notify()方法一样。

## **为什么以及如何在 Java 中使用 Wait()和 Notify()。**

你应该在 [Java](https://www.edureka.co/blog/java-tutorial/) 中使用 Wait 和 Notify，因为它们与锁相关，并且对象有锁。尽管 Java 中的等待和通知是一个非常基本的概念，但是它们是在[对象类](https://www.edureka.co/blog/java-objects-and-classes/)中定义的。令人惊讶的是，使用等待和通知编写代码并不容易。您可以通过编写代码来测试这一点，使用等待和通知来解决生产者-消费者问题。 ![Producer consumer example-Wait and Notify in Java-Edureka](img/9014fca8b5c68453ce99d62fa23ec859.png)这里，我有一个共享的[队列](https://www.edureka.co/blog/java-queue/)和两个线程叫做 *生产者* 和 *消费者* 。**生产者**线程将数字放入共享队列，而**消费者**线程从共享桶中消费数字。

条件是一旦产生了一个项目，必须通知消费者线程，类似地，在消费之后需要通知生产者线程。这个线程间的 通信 是用 Java 中的 wait 和 notify 实现的。

***注意*** : W ait 和 No tify 方法是在对象类中定义的，必须在 synchronized 块内部调用。

## **例子**

```
public class Thread1
{
public static void main(String[] args)
{
Thread2 b = new Thread2();
b.start();
synchronized(b)
{
try
{
System.out.println("Waiting for 2 to complete...");
b.wait();
}
catch(InterruptedException e)
{
e.printStackTrace();
}
System.out.println("Total is: " + b.total);
} } }
class Thread2 extends Thread1
{
int total;
@Override public void run()
{
synchronized(this)
{
for(int i=0; i<=100 ; i++)
{
total += i;
}
notify();
}}}
```

注意，在上面的例子中，Thread2 的一个对象，即 b，是同步的。这个 b 在主线程输出其总值之前完成计算。

**输出:**

![Output- Wait and Notify in Java-Edureka](img/e7d9fd1caa0cd260db0eda8d7174ed01.png)

这就把我们带到了本文的结尾，在这里我们学习了 Java 中关于等待和通知的。希望上述内容被证明有助于增强你的*[Java](https://www.edureka.co/blog/what-is-java/)*知识。继续阅读，继续探索！

另外，请查看 Edureka 提供的 [Java 培训](https://www.edureka.co/java-j2ee-training-course)，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架[如 Hibernate&Spring](https://www.edureka.co/blog/java-frameworks/)。