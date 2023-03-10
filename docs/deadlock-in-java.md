# Java 中如何处理死锁？

> 原文：<https://www.edureka.co/blog/deadlock-in-java/>

Java 编程语言支持[多线程](https://www.edureka.co/blog/java-thread/)。它涉及多个线程同时运行进行多任务处理。但是在某些情况下或者由于某些缺点，线程发现自己永远处于等待状态。在本文中，我们将了解 [Java](https://www.edureka.co/java-j2ee-training-course) 中的死锁情况以及避免死锁的不同方法。以下是本博客讨论的主题:

*   [Java 里什么是死锁？](#deadlock)
*   [死锁示例](#example)
*   [Java 中如何避免死锁？](#avoid)

## **Java 中什么是死锁？**

Java 中的死锁是两个或多个线程被永远阻塞，互相等待的情况。

当多个线程需要相同的锁，但以不同的顺序获得它们时，通常会发生这种情况。[Java 中的多线程编程](https://www.edureka.co/blog/java-thread/)因为 synchronized 关键字而遭遇死锁情况。

它导致正在执行的线程在等待与指定的[对象](https://www.edureka.co/blog/java-objects-and-classes/)相关联的锁或监视器时阻塞。

## **![Deadlock in Java - Edureka](img/2f200c1b83cc3256ccab1a01148228d6.png)**

## **死锁示例**

```
public class Example{
 public static void main(String[] args){
   final String r1 = "edureka";
   final String r2 = "java";

   Thread t1 = new Thread() {
     public void run(){
       synchronized(r1){
        System.out.println("Thread 1: Locked r1");
        try{ Thread.sleep(100);} catch(exception e) {}
      synchronized(r2){
        System.out.println("Thread 1: Locked r2");
        }
     }
  }
};
 Thread t2 = new Thread() {
      public void run(){
       synchronized(r1){
        System.out.println("Thread 2: Locked r1");
        try{ Thread.sleep(100);} catch(exception e) {}
      synchronized(r2){
       System.out.println("Thread 2: Locked r2");
      }
    }
  }
};

t1.start();
t2.start();
}
}

```

```
Output: Thread 1: Locked r1
        Thread 2: Locked r2
```

## **Java 中如何避免死锁？**

虽然不可能完全避免死锁情况，但我们可以遵循某些措施或指针来避免它们:

*   避免嵌套锁–你必须避免给多线程加锁，这是死锁的主要原因。这通常发生在您给多个线程加锁的时候。

*   **避免不必要的锁**–锁应该给重要的线程。给导致死锁情况的不必要的线程加锁。

*   **使用线程连接**–死锁通常发生在一个线程等待另一个线程完成的时候。在这种情况下，我们可以使用 Thread.join 和一个线程将花费的最大时间。

至此，我们已经了解了 Java 中的死锁以及如何避免死锁。我希望你清楚本教程中与你分享的所有内容。

*如果你发现这篇文章与“Java 中的死锁”有关，请查看一下  Edureka 的 [Java 认证](https://www.edureka.co/java-j2ee-training-course)培训，这是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

我们在这里帮助你踏上旅程的每一步，并为想成为 Java 开发人员的学生和专业人士设计课程。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种  [Java 框架](https://www.edureka.co/blog/java-frameworks/) ，如[Hibernate](https://www.edureka.co/blog/what-is-hibernate-in-java/)&[Spring](https://www.edureka.co/blog/spring-tutorial/)。

如果您遇到任何问题，请在“Java 死锁”的评论区提出您的所有问题，我们的团队将很乐意回答。