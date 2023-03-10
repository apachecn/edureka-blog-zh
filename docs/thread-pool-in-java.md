# 什么是 Java 线程池，为什么使用它？

> 原文：<https://www.edureka.co/blog/thread-pool-in-java/>

每当构建服务器应用程序时，每次请求到达时，都会产生创建新的[线程](https://www.edureka.co/blog/java-thread/)的需求。这个新请求就是创建的新线程。本教程将围绕 Java 中的线程池展开，描述其优点和缺点，并给出定义！

本文讨论的主题是:

*   [Java 中的线程池是什么？](#WhatisthreadpoolinJava?)
*   [Java 线程池中的风险](#Risksinthreadpool)
*   [Java 中线程池的优势](#AdvantagesofthreadpoolinJava)
*   [线程池的缺点](#Disadvantagesofthreadpool)
*   [线程池的实现](#Example)

让我们开始吧！

## **Java 中的线程池是什么？**

顾名思义，Java 中的线程池实际上是一个由[个线程](https://www.edureka.co/blog/java-thread/)组成的池。简单地说，它包含一组等待作业被授予的工作线程。它们在整个过程中被重复使用。

在线程池中，创建一组固定大小的线程。每当一个任务必须被授权时，一个线程被拉出并由服务提供者分配该任务，一旦任务完成，该线程就被返回到线程池。最好使用线程池，因为活动线程会消耗系统资源，当 JVM 同时创建太多线程时，系统可能会耗尽内存。因此，必须限制要创建的线程数量。因此，线程池的概念是首选！

让我们进入下一部分，它陈述了与 Java 中的线程池相关的风险。

## **Java 线程池中的风险**

当你处理线程池的时候，有一些风险，比如；

*   **线程泄漏:**如果一个线程被从池中移除以执行一个任务，但在任务完成时没有返回到池中，则发生线程泄漏。
*   **死锁:**在线程池中正在执行的线程正在等待来自阻塞的输出由于线程不可用而在队列中等待执行的线程，出现了死锁的情况。
*   **资源抖动:**线程数量超过所需的最佳数量会导致资源抖动。

现在，让我们转向线程池的优势。

## **线程池的优势**

用 Java 编程时，使用线程池的一些优点是:

*   更好的性能
*   节省时间
*   不需要一次又一次地创建线程
*   容易接近
*   实时使用

现在，让我们来看看线程池的缺点。

## **线程池的缺点**

编程时使用线程池的一些缺点是:

*   您无法控制正在使用的线程的优先级和状态。
*   没有给线程一个稳定的标识，没有跟踪可以保持。
*   当对线程池的需求很高时，可以删除该进程。
*   当两个线程并行工作时，线程池不能很好地工作。
*   尽管有强大的应用程序隔离，但在一些情况下，应用程序代码可能会受到另一个应用程序代码的影响。

现在让我介绍一下线程池的实现部分。开始了。

**线程池的实现**

查看下面的代码，理解 Java 中线程池的概念

**代码:**

```
package MyPackage;

import java.util.concurrent.LinkedBlockingQueue;

public class ThreadPool {
private final int nThreads;
private final PoolWorker[] threads;
private final LinkedBlockingQueue<Runnable> queue;

public ThreadPool(int Threads) {
this.nThreads = Threads;
queue = new LinkedBlockingQueue<Runnable>();
threads = new PoolWorker[Threads];

for (int i = 0; i < nThreads; i++) {
threads[i] = new PoolWorker();
threads[i].start();
}
}

public void execute(Runnable task) {
synchronized (queue) {
queue.add(task);
queue.notify();
}
}

private class PoolWorker extends Thread {
public void run() {
Runnable task;

while (true) {
synchronized (queue) {
while (queue.isEmpty()) {
try {
queue.wait();
} catch (InterruptedException e) {
System.out.println("An error occurred while queue is waiting: " + e.getMessage());
}
}
task = (Runnable)queue.poll();
}

// If we don't catch RuntimeException,
// the pool could leak threads
try {
task.run();
} catch (RuntimeException e) {
System.out.println("Thread pool is interrupted due to an issue: " + e.getMessage());
}
}
}
}
}

```

这篇“Java 中的线程池”文章到此结束。我已经介绍了 Java 最基本也是最重要的主题之一。我希望 你清楚这篇文章中与你分享的一切。

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这篇“Java 线程池”* *文章的评论部分提到它，我们会尽快回复您。*