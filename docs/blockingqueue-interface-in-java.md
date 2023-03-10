# 如何用 Java 实现 BlockingQueue 接口

> 原文：<https://www.edureka.co/blog/blockingqueue-interface-in-java/>

队列是任何编程语言的一个重要方面。尤其是我们说到 [Java](https://www.edureka.co/blog/java-tutorial/) 的时候。在本文中，我们将按以下顺序讨论 Java 中的 BlockingQueue 接口:

*   [Java 中什么是 BlockingQueue 接口？](#what)
*   [阻塞队列类型](#types)
*   [阻塞队列接口中的方法](#methods)
*   [阻塞 Java 中的队列接口示例:服务](#code)

## **Java 中什么是 BlockingQueue 接口？**

Java 中的 BlockingQueue 接口是一个队列，当您试图从队列中出列并且队列为空时，或者当您试图向队列中加入项目并且队列已经满了时，它会阻塞。试图从空队列中出列的线程被阻塞，直到其他线程将一个项目插入到队列中。试图将项目排入满队列的线程会被阻塞，直到其他线程通过将一个或多个项目出队或完全清除队列而在队列中腾出空间。

![priority queue in c++](img/5997b4fb2c10995ce28bafde5c62b84a.png)

Java 中的 BlockingQueue 接口不接受 null 值，如果试图在队列中存储 null 值，会抛出NullPointerException。 Java BlockingQueue 实现有 **线程安全** 。所有排队方法本质上都是原子的，并使用内部锁或其他形式的并发控制。

**Java 队列类图**

Java 队列接口扩展了集合接口。集合接口扩展了 Iterable 接口。一些常用的队列实现类有 LinkedList、PriorityQueue、ArrayBlockingQueue、DelayQueue、LinkedBlockingQueue、PriorityBlockingQueue、等..AbstractQueue 提供了队列接口的框架实现，以减少实现队列的工作量。

## **阻塞队列类型**

阻塞队列有两种类型:

*   **无界队列:** 阻塞队列的容量将被设置为整数。MAX_VALUE。在无限阻塞队列的情况下，队列将永远不会阻塞，因为它可能会变得非常大。当你添加元素时，它的大小会增加。

**语法:** `BlockingQueue blocking queue = new LinkedBlockingDeque();`

*   **有界队列:** 第二种队列是有界队列。在有界队列的情况下，您可以在 queues 构造函数中创建一个绕过队列容量的队列: **语法:** `// Creates a Blocking Queue with capacity 5`

`BlockingQueue blocking queue = new LinkedBlockingDeque(5);`

**阻塞队列接口中的方法**

| **修改器类型** | **方法语法** | **用于** | **描述** |
| **布尔** | **加【戊】** | **插入** | 如果可以在不违反容量限制的情况下立即将指定元素插入此队列，则成功时返回 true，如果当前没有可用空间，则引发 IllegalStateException。 |
| **布尔** | **包含** (对象 o) | **考察** | 如果此队列包含指定的元素，则返回 true。 |
| **int** | **【收藏 c】** | **检索或删除** | 从该队列中移除所有可用元素，并将它们添加到给定集合中。 |
| **int** | **drainTo(集合 c，int maxElements)** | **检索或删除** | 从该队列中移除最多给定数量的可用元素，并将它们添加到给定的集合中。 |
| **布尔** | **【提供(E E)** | **插入** | 如果可以在不违反容量限制的情况下立即将指定的元素插入到此队列中，如果成功，则返回 true，如果当前没有可用空间，则返回 false。 |
| **布尔** | **【报价(E e，长超时，时间单位单位)** | **插入** | 将指定的元素插入到此队列中，等待指定的等待时间，如果需要的话，等待空间变得可用。 |
| **E** | **【轮询(长超时，时间单位单位)** | **检索或删除** | 检索并移除该队列的头，如果有必要，等待指定的等待时间，以便某个元素变得可用。 |
| **作废** | **放(戊戊)** | **插入** | 将指定的元素插入此队列，如有必要，等待空间变得可用。 |
| **int** | 剩余容量() | **考察** | 返回该队列在理想情况下(在没有内存或资源限制的情况下)可以无阻塞接受的附加元素的数量，或者是整数。MAX_VALUE 如果没有内在限制。 |
| **布尔** | **(对象 o)+** | **检索或删除** | 从该队列中移除指定元素的单个实例，如果它存在的话。 |
| **E** | **乘()** | **检索或删除** | 检索并移除该队列的头部，如有必要，等待直到某个元素可用。 |

## **阻塞 Java 中的队列接口示例:服务**

```
package com.journaldev.concurrency;

import java.util.concurrent.ArrayBlockingQueue;

import java.util.concurrent.BlockingQueue;

public class ProducerConsumerService {

    public static void main(String[] args) {

        //Creating BlockingQueue of size 10

        BlockingQueue<Message> queue = new ArrayBlockingQueue<>(10);

        Producer producer = new Producer(queue);	

        Consumer consumer = new Consumer(queue);

        //starting producer to produce messages in queue

        new Thread(producer).start();

        //starting consumer to consume messages from queue

        new Thread(consumer).start();

        System.out.println("Producer and Consumer has been started");

    }

}
```

![BlockingQueue Interface in Java](img/698363aa6ab7b8a7d453fcb5e04169d3.png)

至此，我们结束了 Java 文章中的 BlockingQueue 接口。我希望你所有的概念现在都清楚了。

*查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这篇“用 Java 阻塞队列接口”博客的评论部分提到它，我们会尽快回复您。