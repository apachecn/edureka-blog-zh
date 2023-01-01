# Java 队列:关于 Java 中的队列，您需要知道的一切

> 原文：<https://www.edureka.co/blog/java-queue/>

Java 是一种强大的编程语言，它支持各种数据结构，让程序员的生活变得简单。在本文中，我们将研究一种这样的数据结构，即 Java 队列。这些是本文关注的要点，

*   [Java 中的队列](#QueueInJava)
*   [Java 队列的实现](#ImplementationOfJavaQueue)
*   [Java 队列中的方法](#MethodsInJavaQueue)
*   [演示队列方法的程序](#ProgramToDemonstrateQueueMethods)
*   [遍历 Java 队列](#IteratingThroughAJavaQueue)

让我们开始吧，

## **Java 中的队列**

队列是一种遵循 FIFO(先进先出)原则的数据结构，即元素被插入列表的末尾，并从列表的开头删除。该接口在 java.util.package 中提供，并扩展了集合接口。

队列支持多种方法，包括插入和删除。java.util.package 中可用的队列称为 ***无界队列*** ，而 java.util.concurrent 包中存在的队列称为 ***有界队列。***

除了 Deques 之外，所有队列都支持在末尾插入和从前面删除。Deques 支持在两端插入和删除元素。

让我们转到本文的下一个主题，Java 队列，

## **Java 队列的实现**

为了使用队列接口，我们需要实例化一个具体的类。以下是可以使用的几种实现方式:

*   util。链接列表
*   使用中。PriorityQueue(优先级队列)

由于这些实现不是线程安全的，PriorityBlockingQueue 充当了线程安全实现的替代方案。

**举例:**

```
Queue q1 = new LinkedList();
```

```
Queue q2 = new PriorityQueue();
```

让我们来看看一些重要的 Java 队列方法，

## **Java 队列中的方法**

*   **add():**add()方法用于在队列的末尾或尾部插入元素。方法是从集合接口继承的。
*   **offer():**offer()方法优于 add()方法，因为它将指定的元素插入到队列中，而不违反任何容量限制。
*   **peek():**peek()方法用于查看队列的前面，而不删除它。如果队列为空，则返回空值。
*   **element():** 如果队列为空，该方法抛出 NoSuchElementException。
*   **remove():**remove()方法移除队列的前端并返回它。如果队列为空，将引发 NoSuchElementException。
*   **poll():**poll()方法删除队列的开头并返回它。如果队列为空，则返回空值。

下面是对以下方法的概述:

| ***操作*** | ***抛出异常*** | ***返回值*** |
| ***插入*** | 添加(元素) | 报价(要素) |
| ***去掉*** | 移除() | 投票() |
| ***考察*** | 元素() | peek() |

现在让我们来看看演示，

## **演示队列方法的程序**

```

import java.util.*;
public class Main {
public static void main(String[] args) {
//We cannot create instance of a Queue since it is an interface, thus we
Queue<String> q1 = new LinkedList<String>();
//Adding elements to the Queue
q1.add("I");
q1.add("Love");
q1.add("Rock");
q1.add("And");
q1.add("Roll");
System.out.println("Elements in Queue:"+q1);
/*
* We can remove an element from Queue using remove() method,
*this removes the first element from the Queue
*/
System.out.println("Removed element: "+q1.remove());
/*
*element() method - this returns the head of the
*Queue.
*/
System.out.println("Head: "+q1.element());
/*
*poll() method - this removes and returns the
*head of the Queue. Returns null if the Queue is empty
*/
System.out.println("poll(): "+q1.poll());
/*
*peek() method - it works same as element() method,
*however, it returns null if the Queue is empty
*/
System.out.println("peek(): "+q1.peek());
//Displaying the elements of Queue
System.out.println("Elements in Queue:"+q1);
}
}

```

**输出:**

队列中的元素:[我，爱，摇滚，还有，滚]

移除的元素:I

头像:爱情

poll():爱情

peek(): Rock

队列中的元素:[摇滚]。在上面的例子中，使用了通用队列。

在这种类型的队列中，我们可以限制插入队列的对象的类型。在我们的例子中，我们只能将字符串实例插入队列。

## **遍历 Java 队列**

可以使用以下代码迭代 java 队列中的元素:

队列 q1 =新建链接列表()；

Q1 . add(" Rock ")；

Q1 . add(" And ")；

Q1 . add(" Roll ")；

*//通过迭代器访问*

迭代器 iterator = Q1 . iterator()；

while(iterator.hasNext(){

String element =(String)iterator . next()；

}

*//通过新的 for 循环访问*

对于(对象对象:q1) {

String element = (String)对象；

}

元素迭代的顺序取决于 queue 的实现。

虽然 Java 队列可以实现多种方法，但是这里已经讨论了最重要的方法。

这样，我们就结束了这篇关于“Java 队列”的文章。如果你想了解更多， 请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。