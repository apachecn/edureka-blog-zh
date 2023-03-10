# Java 中的 Join 方法:如何连接线程？

> 原文：<https://www.edureka.co/blog/join-method-java>

Java 中的线程被认为是程序中执行的[线程。Java.lang.thread 包含多种方法，有助于同时运行多个线程。Java 中常用的方法之一是 Join 方法。让我们在下面的序列中探索这种方法。](https://www.edureka.co/blog/java-thread/)

*   [Java 中的 join 方法是什么？](#joinmethod)
*   [语法](#syntax)
*   [Java 程序实现 Thread.join()方法](#javaprogram)

我们开始吧。

## **Java 中的 Join 方法是什么？**

Java 中的 Join 方法允许一个线程等待另一个线程完成它的执行。简单地说，这意味着它等待另一个线程死亡。它有 ***无效*** 类型和抛出 ***中断异常*** 。在 Java 中连接线程有三个功能，

*   加入()
*   加入(长距离)
*   join(长毫秒，整数纳米)

| 方法 | 描述 |
| 加入() | 等待该线程终止 |
| 加入(长距离) | 等待该线程终止的时间最多为毫秒 |
| join(长毫秒，整数纳米) | 等待这个线程死亡的时间最多为毫秒加毫微秒 |

## **语法**:

*   公共最终无效联接()
*   公共最终空连接(长毫秒，整数毫微秒)
*   公共最终无效连接(长毫秒)

## **Java 程序实现 Thread.join 方法**

让我们在 [Java](https://www.edureka.co/blog/java-tutorial/) 中逐一实现所有的连接。

**Java 中 join()方法的例子**

```
package Edureka;

import java.io.*; 
import java.util.*; 

public class Threadjoiningmethod extends Thread{  
		 public void run(){  
		  for(int i=1;i<=4;i++){  
		   try{  
		    Thread.sleep(500);  
		   }catch(Exception e){System.out.println(e);}  
		  System.out.println(i);  
		  }  
		 }  
		public static void main(String args[]){  
			Threadjoiningmethod th1=new Threadjoiningmethod ();  
			Threadjoiningmethod th2=new Threadjoiningmethod ();  
			Threadjoiningmethod th3=new Threadjoiningmethod ();  
		 th1.start();  
		 try{  
		  th1.join();  
		 }
		 catch(Exception e){
			 System.out.println(e);
			 }  

		 th2.start();  
		 th3.start();  
		 }  
		}
```

**输出:**

123411223344

**解释:**这里你可以注意到线程 1 首先完成它的任务，然后线程 2 和线程 3 将执行。【T2

**Java 中 join(long millis)方法的例子**

```
package Edureka;

import java.io.*; 
import java.util.*; 

public class Threadjoiningmethod extends Thread{  
		 public void run(){  
		  for(int i=1;i<=4;i++){  
		   try{  
		    Thread.sleep(200);  
		   }catch(Exception e){System.out.println(e);}  
		  System.out.println(i);  
		  }  
		 }  
		public static void main(String args[]){  
			Threadjoiningmethod th1=new Threadjoiningmethod();  
			Threadjoiningmethod th2=new Threadjoiningmethod();  
			Threadjoiningmethod th3=new Threadjoiningmethod();  
		 th1.start();  
		 try{  
		  th1.join(1000);  
		 }
		 catch(Exception e){
			 System.out.println(e);
			 }  

		 th2.start();  
		 th3.start();  
		 }  
		}
```

**输出:**

123411223344

**解释:**这里你可以注意到线程 1 完成任务的时间为 200 毫秒(睡眠时间为 200 的 4 倍)，然后线程 2 和线程 3 将执行。

如果你刚刚开始，那么看看这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

这样，我们就结束了这篇关于“Java 中的 Join 方法”的文章。如果你想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)的 [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在本博客“Java 中的 Join 方法”的评论部分提到它，我们将尽快回复您。