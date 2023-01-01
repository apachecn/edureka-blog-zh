# Java 中信号量是什么及其用途？

> 原文：<https://www.edureka.co/blog/semaphore-in-java/>

Java 中的信号量通过计数器控制对共享资源的访问。它是一个[线程同步](https://www.edureka.co/blog/synchronization-in-java/)构造，用于在线程之间发送信号，以避免错过信号或保护关键部分。在这篇关于 Java 信号量的博客中，我们将详细理解这个概念。本博客将涵盖以下主题:

*   [什么是 Java 中的信号量？](#semaphores)
*   [信号量的类型](#types)
*   [信号量工作](#working)
*   [信号量的实现](#implement)

## **什么是 Java 中的信号量？**

信号量是用于进程同步的变量，用于管理并发进程。它还用于控制多个并发进程对公共资源的访问，并避免竞争情况。

## **信号量的种类—**

*   **二元信号量:**二元信号量只取 0 和 1 作为值，用于实现互斥以及同步并发进程。

*   **计数信号量:**一个计数信号量在任意一点的值表示恰好同时可以进入临界区的最大进程数。

## **信号量的工作**

*   如果信号量计数> 0，线程获得一个许可，减少信号量的计数。

*   否则，[线程](https://www.edureka.co/blog/java-thread/)被阻塞，直到可以获得许可。

*   当线程不再需要访问共享资源时，它释放许可证，增加信号量计数。

*   如果另一个线程正在等待一个许可，那么那个线程将在那时获得一个许可。

## **信号量的实现**

```

import java.util.concurrent.*; 

//Will take Resource as  shared class
class Resource 
{ 
	static int count = 0; 
} 

class MyDemo extends Demo 
{ 
	Semaphore sem; 
	String threadName; 
	public MyDemo(Semaphore sem, String threadName) 
	{ 
		super(threadName); 
		this.sem = sem; 
		this.threadName = threadName; 
	} 

	@Override
	public void run() { 

		// Run By X
		if(this.getName().equals("X")) 
		{ 
			System.out.println("Starting " + threadName); 
			try
			{ 
				// Will get the permit to access shared resource
				System.out.println(threadName + " waiting for a permit."); 

				// acquiring the lock 
				sem.acquire(); 

				System.out.println(threadName + " gets a permit."); 

				// Now, accessing the shared resource and rest will wait  

				for(int i=0; i < 7; i++) 
				{ 
					Resource.count++; 
					System.out.println(threadName + ": " + Resouce.count); 

					// Now thread Y will try  to execute 
					Thread.sleep(20); 
				} 
			} catch (InterruptedException exc) { 
					System.out.println(exc); 
				} 

				// Release the permit. 
				System.out.println(threadName + " releases the permit."); 
				sem.release(); 
		} 

		// run by thread Y 
		else
		{ 
			System.out.println("Starting " + threadName); 
			try
			{ 
				// First, Y will try to get permit
				System.out.println(threadName + " waiting for a permit."); 

				// acquiring the lock 
				sem.acquire(); 

				System.out.println(threadName + " gets a permit."); 

				// Now, accessing the shared resource and others will wait

				for(int i=0; i < 7; i++) 
				{ 
					Resource.count--; 
					System.out.println(threadName + ": " + Resource.count); 

					// Now, allowing a context switch -- if possible. 
					// for thread X to execute 
					Thread.sleep(20); 
				} 
			} catch (InterruptedException exc) { 
					System.out.println(exc); 
				} 
				// Release the permit. 
				System.out.println(threadName + " releases the permit."); 
				sem.release(); 
		} 
	} 
} 

public class SemTest 
{ 
	public static void main(String args[]) throws InterruptedException 
	{ 
		// creating a Semaphore object 
		// with number of permits 1
		Semaphore sem = new Semaphore(1); 

		// creating two threads with name X and Y 
		// Here thread X will increment and Y will decrement the counter
		MyDemo md1 = new MyDemo(sem, "X"); 
		MyDemo md2 = new MyDemo(sem, "Y"); 

		// stating threads X and Y 
		md1.start(); 
		md2.start(); 

		// waiting for threads X and Y 
		md1.join(); 
		mtd.join(); 

		System.out.println("count: " + Resource.count); 
	} 
} 

```

**输出-** 启动 X 启动 Y X 等待许可 Y 等待许可 X:1X:2X:3X:4X:5X:6X:7X 释放许可 Y 获得许可 Y:6Y:5Y:4Y:3

至此，我们结束了这篇关于“Java 中的信号量”的博客。如果你想学习更多关于 Java 的知识，请查看 Edureka 的 [Java 认证](https://www.edureka.co/java-j2ee-training-course)培训，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让你在 Java 编程方面有一个良好的开端，并训练你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在“什么是 Java 中的信号量”博客的评论部分提到它，我们会尽快回复你。