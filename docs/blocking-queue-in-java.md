# Java 中什么是 BlockingQueue，如何实现？

> 原文：<https://www.edureka.co/blog/blocking-queue-in-java/>

[**Java**](https://www.edureka.co/java-j2ee-soa-training) 因其全面的内置特性而极受程序员欢迎。大多数时候，甚至在问题出现之前，你就已经有了专门的解决方案。Java 集合[中非常有用和重要的部分](https://www.edureka.co/blog/java-collections/)就是 Java 中的 BlockingQueue 接口。通过这篇文章，我将介绍一下 Java 中的 BlockingQueue 以及实现它的方法。

下面是本文涉及的主题:

*   [Java 中的 BlockingQueue 接口](#blockingqueue)
*   [Java 中阻塞队列的构造函数类型](#types)
*   [阻塞队列界面中的方法](#methods)
*   [阻塞队列实现](#implementation)

## **阻塞 Java 中的队列接口**

[Java 中的 blocking queue](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/BlockingQueue.html)是 Java 1.5 中添加的一个接口，以及其他几个并发实用程序类，如 ConcurrentHashMap、CopyOnWriteArrrayList 等。BlockingQueue 接口属于**Java . util . concurrent**包。此接口通过激活阻塞来增强流控制，以防线程试图将空队列出队或将满队列入队。无论哪种情况，这个接口都很方便。 简单来说，假设一个[线程](https://www.edureka.co/blog/java-thread/)试图将元素添加到一个已经满了的队列中。在程序的这一点上，BlockingQueue 将被调用，这将阻塞那个特定的线程，直到另一个线程释放队列来腾出空间。这可能是元素出队或整个队列的清除的结果。类似地，BlockingQueue 将被调用来阻塞一个试图将一个已经为空的队列出队的线程，直到其他线程将一个元素插入或添加到空的[队列](https://www.edureka.co/blog/java-queue/)中。

在 Java 中使用 BlockingQueue 接口时，你必须记住它不接受空值。如果你试图这样做，它会立即抛出一个 NullPointerException。下图显示了 Java 中 BlockingQueue 接口的工作方式。

这个[接口](https://www.edureka.co/blog/java-interface/)主要用于生产者-消费者之间，因为它是线程安全的。我的意思是阻塞队列接口可以用来创建一个生产者和消费者都可以共享的队列

为了在 Java 中使用 BlockingQueue，首先，你需要熟悉它的类型。让我在本文的下一部分向您介绍他们。

## **Java 中 BlockingQueue 的构造函数类型**

Java 中 BlockingQueue 接口的构造函数有两种:

*   **无界队列:**对于这种类型的队列，容量会设置为整数。MAX_VALUE。无限队列永远不会被阻塞，因为它可以在每次插入元素时动态增长。下面是创建无限队列的语法:

```
BlockingQueue bq = new LinkedBlockingDeque();
```

*   **有界队列:** 对于这种队列，需要在创建时传递队列的容量，即作为[构造函数](https://www.edureka.co/blog/constructor-in-java/)的参数。一旦指定了大小，就不能更改。下面是创建有界队列的语法:

```
BlockingQueue bq = new LinkedBlockingDeque(10);
```

现在您已经熟悉了用 Java 实现 BlockingQueue 的方法，让我列出它的一些方法。

## **阻塞队列接口中的方法**

| **方法** | **描述** |
| *布尔加法(E e)* | 这个方法有助于将指定的元素插入到这个队列中，如果队列中有空间的话，否则 将抛出一个 `IllegalStateException` |
| *布尔包含(对象 o)* | 如果队列包含指定的元素，此方法返回 true |
| *int drainTo(收藏<？超 E > c)* | 此方法将从队列中移除所有可用的元素，并将它们添加到指定的集合中 |
| *int drainTo(收藏<？超级 E > c，int maxElements)* | 该方法将从队列中移除给定数量的可用元素，并将它们添加到指定的[集合](https://www.edureka.co/blog/java-collections/) |
| *booloean offer(E e)* | 如果队列未满，此方法会将指定的元素插入队列，并返回 true，否则将返回 false |
| *布尔报价(E e，长超时，时间单位单位)* | 这个方法将指定的元素插入到队列中。如果队列已满，它将等待指定的等待时间，等待空间变得可用。 |
| *E poll(长超时，时间单位单位)* | 这个方法有助于检索和删除队列的头部。如果队列为空，它将等待指定的等待时间，等待一个元素变得可用 |
| *void put(E e)* | 如果队列已满，此方法将通过等待空间变得可用来将指定的元素插入队列 |
| *int remainingCapacity()* | 该方法有助于返回该队列在不被阻塞的情况下可以接受的额外元素的数量 |
| *布尔删除(对象 o)* | 仅当指定元素的单个实例存在时，此方法才会将其从队列中移除 |
| *E 取()* | 如果队列为空，该方法将通过等待元素变得可用来帮助检索和移除队列的头部。 |

## **阻塞队列实现**

这里我将用 Java 实现一个简单的阻塞队列的例子，其中类 EduProducer 将生成数据并将其插入到[队列](https://www.edureka.co/blog/java-queue/)中，同时，另一个类 EduConsumer 将从同一队列中删除数据。

为此，我将创建 3 个类，即:

1.  *教育制作人*
2.  *教育消费者*
3.  *利益相关者*

现在让我们逐个创建这些类。

**EduProducer.java**

```
package edureka;

import java.util.concurrent.BlockingQueue;

public class EduProducer implements Runnable {

	private final BlockingQueue<Integer> queue;

    @Override
    public void run() {

        try {
            process();
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        }

    }

    private void process() throws InterruptedException {

        // Put 10 ints into Queue
        for (int i = 0; i < 10; i++) {
            System.out.println("[Producer] Add : " + i);
            queue.put(i);
            System.out.println("[Producer] Queue's Remaining Capacity : " + queue.remainingCapacity());
            Thread.sleep(150);
        }

    }

	public EduProducer(BlockingQueue<Integer> queue) {
		        this.queue = queue;		    
	}

}
```

**EduConsumer.java**

```
package edureka;

import java.util.concurrent.BlockingQueue;

public class EduConsumer implements Runnable {
	private final BlockingQueue<Integer> queue;

    @Override
    public void run() {

        try {
            while (true) {
                Integer take = queue.take();
                process(take);
            }
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        }

    }

    private void process(Integer take) throws InterruptedException {
        System.out.println("[Consumer] Remove : " + take);
        Thread.sleep(500);
    }

    public EduConsumer(BlockingQueue<Integer> queue) {
        this.queue = queue;
    }

}

```

**利益相关者。java**

```
package edureka;

import java.util.concurrent.BlockingQueue;
import java.util.concurrent.LinkedBlockingQueue;

public class EdurekaMain {

	public static void main(String[] args) {

		BlockingQueue<Integer> queue = new LinkedBlockingQueue<>(10);

        new Thread(new EduProducer(queue)).start();
        new Thread(new EduConsumer(queue)).start();

	}

}
```

编写完代码后，执行程序以获得以下输出:

```
[Producer] Add : 0
[Consumer] Take : 0
[Producer] Queue's Remaining Capacity : 9
[Producer] Add : 1
[Producer] Queue's Remaining Capacity : 9
[Producer] Add : 2
[Producer] Queue's Remaining Capacity : 8
[Producer] Add : 3
[Producer] Queue's Remaining Capacity : 7
[Consumer] Take : 1
[Producer] Add : 4
[Producer] Queue's Remaining Capacity : 7
[Producer] Add : 5
[Producer] Queue's Remaining Capacity : 6
[Producer] Add : 6
[Producer] Queue's Remaining Capacity : 5
[Consumer] Take : 2
[Producer] Add : 7
[Producer] Queue's Remaining Capacity : 5
[Producer] Add : 8
[Producer] Queue's Remaining Capacity : 4
[Producer] Add : 9
[Producer] Queue's Remaining Capacity : 3
[Consumer] Take : 3
[Consumer] Take : 4
[Consumer] Take : 5
[Consumer] Take : 6
[Consumer] Take : 7
[Consumer] Take : 8
[Consumer] Take : 9
```

这就把我们带到了这篇关于 Java 中的 BlockingQueue 的文章的结尾。如果你想更详细地学习 Java，你也可以参考我们的  **[其他 Java 文章](https://www.edureka.co/blog/what-is-java/)** 。

*现在，您已经了解了 Java 中阻塞队列的基本知识，请查看 Edureka 提供的  [**Java 认证培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这篇“用 Java 阻塞队列”的评论部分提到它，我们会尽快回复您。