# 如何在 Java 中实现 thread.yield():示例

> 原文：<https://www.edureka.co/blog/thread-yield-in-java/>

理论上,“屈服”意味着放手、放弃、投降。让步线程告诉虚拟机，它愿意让其他线程代替它被调度。这表明它没有做太关键的事情。注意 *只是一个提示* 虽然如此，并不能保证有任何效果。在本 [Java](https://www.edureka.co/blog/java-tutorial/) 中的 thread.yield()中，我们将涉及以下主题:

*   [Java 中的 thread.yield()简介](#intro)
*   [Java 中等待、睡眠、加入和让步的区别](#difference)
*   [Java 中 thread.yield()的例子](#example)

## **Java 中的 thread.yield()简介**

在 Thread.java，收益率()的定义如下。 给调度程序的一个提示，表明当前线程愿意让出它当前使用的一个处理器。调度程序可以随意忽略 这个提示。

Yield 是一种试探性的尝试，旨在改善[线程](https://www.edureka.co/blog/java-thread/)之间的相对进程，否则会过度利用 CPU。 它的使用应该与详细的剖析和基准测试相结合，以确保它确实具有预期的效果。

**语法:**

```

```
public static native void yield();
```

```

## **Java 中等待、睡眠、加入和让步的区别**

### **屈服()** **vs** **等待()**

*   当 *yield()* 在当前线程的上下文中被调用时，*wait()*只能在同步块或方法内显式获取的锁上被调用
*   与 *yield()* 不同，wait*()*可以指定在再次尝试调度线程之前等待的最小时间段
*   使用 *wait()* 也可以通过调用相关锁对象上的*notify()*或*notify all()*来随时唤醒线程

### **屈服()** **vs** **睡眠()**

*   虽然 *yield()* 只能试探性地尝试暂停当前线程的执行，而不能保证它将在何时被调度回来，*【sleep()*可以强制调度程序至少将当前线程的执行暂停一段作为其参数的时间。

### **屈服()** **vs** **加入()**

*   当前线程可以在任何其他线程上调用 *join()* ，这使得当前线程在继续执行之前等待其他线程死亡
*   可选地，它可以提及一个时间段作为其参数，该参数指示当前线程在恢复 之前应该等待的最大时间

## **Java 中 thread.yield()的例子**

```

```
public class JavaYieldExp extends Thread  
{  
public void run()  
{  
        for (int i=0; i&amp;amp;amp;amp;lt;3 ; i++)  
            System.out.println(Thread.currentThread().getName() + " in control");  
    }  
    public static void main(String[]args)  
    {  
        JavaYieldExp t1 = new JavaYieldExp();  
        JavaYieldExp t2 = new JavaYieldExp();  
        // this will call run() method  
        t1.start();  
        t2.start();  
        for (int i=0; i&amp;amp;amp;amp;lt;3; i++)  
        {  
            // Control passes to child thread  
            t1.yield();  
            System.out.println(Thread.currentThread().getName() + " in control");  
        }  
    }  
}  
```

```

**输出:**

![thread.yield() in Java](img/bae1458c39a5ce0a48d0eb90e43148bc.png)

下一个例子展示了 java.lang.Thread.yield()方法的用法:

```

```
import java.lang.*;
public class ThreadDemo implements Runnable {
   Thread t;
   ThreadDemo(String str) {
      t = new Thread(this, str);
      // this will call run() function
      t.start();
   }
   public void run() {
      for (int i = 0; i &amp;amp;amp;amp;amp;amp;lt; 5; i++) {
         // yields control to another thread every 5 iterations
         if ((i % 5) == 0) {
            System.out.println(Thread.currentThread().getName() + "
            yielding control...");
            /* causes the currently executing thread object to temporarily 
            pause and allow other threads to execute */
            Thread.yield();
         }
      }
      System.out.println(Thread.currentThread().getName() + " has finished executing.");
   }
   public static void main(String[] args) {
      new ThreadDemo("Thread 1");
      new ThreadDemo("Thread 2");
      new ThreadDemo("Thread 3");
   }
}
```

```

**输出:**

![](img/cda16d38a1033d5288b7df622d58b598.png)

说到这里，我们的文章就到此为止了。我希望您了解 Java 中的 thread.yield()是如何工作的，以及它是如何在编程语言中使用的。

*查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这篇“Thread.yield() in Java”博客的评论部分提到它，我们会尽快回复您。