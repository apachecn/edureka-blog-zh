# Java 中的 Deque 是什么，如何实现它的接口？

> 原文：<https://www.edureka.co/blog/deque-in-java/>

Java 中的 Deque 是一个双头队列。用于添加或删除 ***头部*** 或 ***尾部*** 的数据元素。Java.util.Dequeue 接口由 [Java](https://www.edureka.co/blog/java-tutorial/) 中的 deque 使用，它是 java.util.Queue 接口的子类型。让我们详细研究一下这个概念。

下面提到的要点将是本文的议程:

1.  [Java 里的 Deque 是什么？](#deque)
2.  [在队列中使用的方法](#methods)
3.  [Java 程序显示队列的工作方式](#program)

我们开始吧！

## **Java 里的 Deque 是什么？**

双端队列是一个双端队列。它有助于从头或尾添加和删除数据结构中的数据元素。它既可以用作 FIFO，也可以用作 LIFO。先进先出和后进先出的例子分别是[队列](https://www.edureka.co/blog/java-queue/)和[堆栈](https://www.edureka.co/blog/stack-class-in-java/)。![Deque in Java](img/5ac010726d007aaa7c52c726d7801659.png)

这是工作原理的示意图。继续，我们有几个[方法](https://www.edureka.co/blog/java-methods/)包含在 deque 中。让我们来看看。

## **方法中使用的反队列**

deque 中使用的方法如下:

1.  **addFirst(element)** :这个方法在头部添加一个元素。
2.  **addLast(element):** 这个方法在尾部添加一个元素。
3.  **add(element)** :这个方法在尾部添加一个元素。
4.  **removeFirst()** :这个方法从头部移除元素。
5.  **removeLast():** 这个方法从尾部移除元素。
6.  **push(element)** :这个方法在头部添加一个元素。
7.  **pop(element)** :这个方法从头部移除一个元素。
8.  **offerFirst(element)** :这个方法在头部添加一个元素，如果插入成功，将返回一个布尔值来描述。
9.  **offerLast(element)** :该方法从尾部移除一个元素，并返回一个布尔值来描述插入是否成功。
10.  **descendingIterator()** :这个方法返回一个迭代器，它的顺序与这个队列相反。
11.  **poll()** :这个方法检索并删除 dequee 的头，如果 dequee 为空，它将返回 null。
12.  **pollFirst()** :该方法检索并删除该队列的第一个元素，如果该队列为空，则返回 null。
13.  **pollLast()** :该方法检索并删除该队列的最后一个元素，如果该队列为空，则返回 null。
14.  **iterator()** :这个方法返回一个用于队列的迭代器。

嗯，这是一些方法。我通过一个 [Java](https://www.edureka.co/blog/what-is-java/) 代码给大家展示一下实现过程。

## **Java 程序显示队列的工作方式**

看看下面的[示例程序](https://www.edureka.co/blog/java-programs/):

```

import java.util.ArrayList;
import java.util.List;
public class DoubleEndedQueueImpl {
private List<Integer> deque = new ArrayList<Integer>();
public void insertFront(int item){
//add element at the beginning of the queue
System.out.println("element added at front: "+item);
deque.add(0,item);
System.out.println(deque);
}
public void insertRear(int item){
//add element at the end of the queue
System.out.println("element added at rear: "+item);
deque.add(item);
System.out.println(deque);
}
public void removeFront(){
if(deque.isEmpty()){
System.out.println("Deque underflow, unable to remove.");
return;
}

//remove an item from the beginning of the queue
int rem = deque.remove(0);
System.out.println("element removed from front: "+rem);
System.out.println(deque);
}

public void removeRear(){
if(deque.isEmpty()){
System.out.println("Deque underflow, unable to remove.");
return;
}

//remove an item from the beginning of the queue
int rem = deque.remove(deque.size()-1);
System.out.println("element removed from front: "+rem);
System.out.println(deque);
}

public int peakFront(){
//gets the element from the front without removing it
int item = deque.get(0);
System.out.println("Element at first: "+item);
return item;
}

public int peakRear(){
//gets the element from the rear without removing it
int item = deque.get(deque.size()-1);
System.out.println("Element at rear: "+item);
return item;
}

public static void main(String a[]){
DoubleEndedQueueImpl deq = new DoubleEndedQueueImpl();
deq.insertFront(34);
deq.insertRear(45);
deq.removeFront();
deq.removeFront();
deq.removeFront();
deq.insertFront(21);
deq.insertFront(98);
deq.insertRear(5);
deq.insertFront(43);
deq.removeRear();
}
}

```

**输出**

```
adding at front: 34

[34]

adding at rear: 45

[34, 45]

removed from front: 34

[45]

removed from front: 45

[]

Deque underflow!! unable to remove.

adding at front: 21

[21]

adding at front: 98

[98, 21]

adding at rear: 5

[98, 21, 5]

adding at front: 43

[43, 98, 21, 5]

removed from front: 5

[43, 98, 21]

```

至此，我们已经接近了本文的结尾。我希望上面解释的内容对您的 Java 知识有所帮助。继续阅读，继续探索！

*查看 Edureka 提供的  **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这个“Java 中的 Deque”博客的评论部分提到它，我们会尽快回复您。