# Java 中的守护线程:知道它的方法是什么

> 原文：<https://www.edureka.co/blog/daemon-thread-in-java>

线程是一个轻量级的进程。线程通过防止 CPU 周期的浪费来降低效率。Java，作为一种流行且简单的编程语言，提供了对[多线程](https://www.edureka.co/blog/java-thread/)的内置支持。每个线程都有自己的优先级，优先级高的线程执行得更快。与其他线程不同，Java 中的守护线程是一个在后台运行的低优先级线程。

本博客将按以下顺序向您介绍 Java 守护线程。

让我们开始吧。:-)

## **![Java - daemon thread in Java - Edureka](img/85c6ac6106a1b9480b0dd1d9fa54bbd8.png)**

## **Java 中什么是守护线程？**

## 

Java 中的守护线程为后台运行的用户线程提供服务。它被认为是一个低优先级线程，用于执行垃圾收集等任务。在 java 中，每个线程都有自己的优先级，优先级高的线程执行得更快。另外， [Java 虚拟机(JVM)](https://www.edureka.co/blog/java-virtual-machine/) 自动终止这个线程。它不能阻止 JVM 在所有用户线程完成执行时退出，即使守护线程本身正在运行。

接下来，让我们看看守护进程线程与用户线程(非守护进程)有什么不同。

## **守护线程 vs 用户线程**

守护线程和用户线程的主要区别在于 JVM。如上所述，Java 虚拟机在等待用户线程完成时，并不等待守护线程完成其执行。让我们借助下表来探究守护线程和用户线程之间的更多差异:

| **守护线程** | **用户线程(非守护进程)** |
| 守护线程是由 JVM 创建的 | 用户线程是由应用程序本身创建的 |
| JVM 不会等待它的执行 | JVM 一直等到执行完成 |
| 低优先级线程 | 高优先级线程 |
| 用于后台任务(非关键) | 用于前台任务(关键) |
| 生活依赖于用户线程 | 生活是独立的 |

既然您已经清楚了守护进程和用户线程之间的区别，那么让我们看一个示例程序来检查一个线程是守护进程还是非守护进程线程。

```
public class ExampleThread extends Thread {

	    @Override
	    public void run() 
	    { 
	        System.out.println("User Thread or Non-Daemon Thread"); 
	    }	  
	    public static void main(String[] args) 
	    { 

	    	ExampleThread obj = new ExampleThread(); 
	        obj.start(); 

	        System.out.println("is " + obj.getName() 
	                           + " a Daemon Thread: "
	                           + obj.isDaemon()); 

	        System.out.println("is " + Thread.currentThread().getName() 
	                           + " a Daemon Thread: "
	                           + Thread.currentThread().isDaemon()); 
	    } 
} 
```

**输出:**是 Thread-0 a 守护线程:false 用户线程或非守护线程 是 main a 守护线程:false

接下来，让我们看看 Java 中守护线程的不同方法。

## **Java 守护线程中的方法**

Java 中有两种主要的守护线程方法，即:

| **方法** | **描述** |
| 公共 void setDaemon(布尔状态) | 将该线程标记为守护进程线程或用户线程(非守护进程线程)。 |
| public boolean isDaemon() | 用于测试该线程是否为守护线程。如果线程是守护进程，则返回 true，否则返回 false。 |

```
Consider the below code for practical implementation:

```

```
public class Demothread extends Thread {

// Java program to demonstrate the usage of  
// setDaemon() and isDaemon() method. 
  public Demothread(String name){ 
      super(name); 
  } 

  public void run() 
  {  
      // Checking whether the thread is Daemon or not 
      if(Thread.currentThread().isDaemon()) 
      {  
          System.out.println(getName() + " is Daemon thread");  
      }  

      else
      {  
          System.out.println(getName() + " is User thread");  
      }  
  }  
  public static void main(String[] args) 

  {  

	  Demothread thread1 = new Demothread("thread1"); 
	  Demothread thread2 = new Demothread("thread2"); 
	  Demothread thread3 = new Demothread("thread3"); 

      // Setting user thread thread1 to Daemon 
  	thread1.setDaemon(true); 

      // starting first 2 threads  
  	thread1.start();  
  	thread2.start(); 

      // Setting user thread thread3 to Daemon 
  	thread3.setDaemon(true);  
  	thread3.start();         
  }  
} 
```

**输出:** thread2 是用户线程 thread1 是守护线程

“Java 守护线程”博客到此结束。我希望你们清楚我上面讨论的内容。请务必阅读我的下一篇博客关于 **[Java 面试问题](https://www.edureka.co/blog/interview-questions/java-interview-questions/)** ，我在这里列出了 75 个面试问题和答案，它们将帮助你在面试过程中脱颖而出。

*既然您已经了解了 Java 系列，请查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这个“Java守护进程线程”博客的评论部分提到它，我们会尽快回复你。