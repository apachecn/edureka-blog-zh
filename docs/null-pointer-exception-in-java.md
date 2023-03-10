# Java 中的空指针异常:实现和示例

> 原文：<https://www.edureka.co/blog/null-pointer-exception-in-java/>

代码的顺利运行需要异常，并让程序员知道要解决的错误。在本文中，我们将按照以下顺序关注 Java 中的空指针异常:

*   [Java 中什么是空指针异常？](#what)
*   为什么我们需要空值？
*   [如何避免空指针异常？](#how)
*   [检查一个方法的参数](#keeping)
*   [使用三元运算符](#ternary-operator)

**Java 中什么是空指针异常？**

Java 中的空指针异常是一个运行时异常。在 Java 世界中，一个特殊的空值被赋给一个对象引用。当程序试图使用具有空值的对象引用时，会引入空指针异常。可以是:

*   从空对象中调用某个方法。
*   访问或修改空对象的字段。
*   通过考虑 null 的长度，好像它是一个数组。
*   访问或修改空对象的槽时。
*   像可抛出值一样抛出 null。
*   试图通过空对象进行同步。

为什么我们需要空值？

Null 是 Java 中使用的唯一值。Null 用于表示没有给引用变量赋值。null 的主要应用在于实现像链表和树这样的数据结构。其他一些应用程序包括空对象模式和单例模式。单例模式规定一个类只能有一个实例，目的是提供一个全局的对象访问点。

创建类的至少一个实例的最好和最简单的方法是将所有的构造函数声明为私有的。然后，他们创建一个公共方法，返回该类的唯一实例。

```
// To use randomUUID function. 
import java.util.UUID; 
import java.io.*; 
class Singleton 
{ 
	// Here we Initialize the values of single and ID to null. 
	private static Singleton single = null; 
	private String ID = null; 
	private Singleton() 
	{ 
		/* Make it private, in order to prevent the 
		creation of new instances of the Singleton 
		class. */
		// Create a random ID 
		ID = UUID.randomUUID().toString(); 
	} 
	public static Singleton getInstance() 
	{ 
		if (single == null) 
			single = new Singleton(); 
		return single; 
	} 
	public String getID() 
	{ 
		return this.ID; 
	} 
} 

// Driver Code 
public class TestSingleton 
{ 
	public static void main(String[] args) 
	{ 
		Singleton s = Singleton.getInstance(); 
		System.out.println(s.getID()); 
	} 
}
//
```

**输出:**

![null-pointer](img/2ad9f9a6cc942127e73ae84c9abb007d.png)

上面的例子是 singleton 类的静态实例。实例在 Singleton get 实例方法中最多初始化一次。

**Java 中如何避免空指针异常？**

为了避免 Java 中的空指针异常，我们必须确保所有对象在使用之前都被正确初始化。当一个引用变量被声明时，我们必须验证一个对象不为空，在我们从对象请求方法或字段之前也是如此。以下是一些问题以及克服这些问题的相应解决方案。

```
//  program to demonstrate the invoking of a method 
// on null causes NullPointerException 
import java.io.*; 

class GFG 
{ 
	public static void main (String[] args) 
	{ 
		// Initializing String variable with null value 
		String ptr = null; 

		// Checking if ptr.equals null or works fine. 
		try
		{ 
			// This line of code throws NullPointerException 
			// because ptr is null 
			if (ptr.equals("gfg")) 
				System.out.print("Same"); 
			else
				System.out.print("Not Same"); 
		} 
		catch(NullPointerException e) 
		{ 
			System.out.print("NullPointerException Caught"); 
		} 
	} 
}
```

**输出:**

![null-pointer-exception](img/c401051efaed9d6b9d5c307563146f04.png)

**检查方法的参数**

永远记住，在执行新方法的主体之前，我们应该确保它的参数为空值，并继续执行该方法。当且仅当参数被正确检查时。否则会抛出“IllegalArgumentException”并调出调用方法，说明传递的参数有问题。

```
// program to check if parameters are null or not before 
// using them. 
import java.io.*; 
class GFG 
{ 
	public static void main (String[] args) 
	{ 
		// String s set an empty string and calling getLength() 
		String s = ""; 
		try
		{ 
			System.out.println(getLength(s)); 
		} 
		catch(IllegalArgumentException e) 
		{ 
			System.out.println("IllegalArgumentException caught"); 
		} 

		// String s set to a value and calling getLength() 
		s = "GeeksforGeeks"; 
		try
		{ 
			System.out.println(getLength(s)); 
		} 
		catch(IllegalArgumentException e) 
		{ 
			System.out.println("IllegalArgumentException caught"); 
		} 

		// Setting s as null and calling getLength() 
		s = null; 
		try
		{ 
			System.out.println(getLength(s)); 
		} 
		catch(IllegalArgumentException e) 
		{ 
			System.out.println("IllegalArgumentException caught"); 
		} 
	} 

	// Function to return length of string s. It throws 
	// IllegalArgumentException if s is null. 
	public static int getLength(String s) 
	{ 
		if (s == null) 
			throw new IllegalArgumentException("The argument cannot be null"); 
		return s.length(); 
	} 
}
```

**输出:**

![Null Pointer Exception in Java](img/2dda2dc84869cc5eda6fdad3b236d49e.png)

**使用三元运算符**

三元运算符用于避免 NullPointerException。检查布尔表达式，如果表达式为真，则返回值 1，否则，返回值 2。可以使用三元运算符来处理空指针:右图是相应的输出。

```
// A Java program to demonstrate that we can use 
// ternary operator to avoid NullPointerException. 
import java.io.*; 
class GFG { 
	public static void main (String[] args) 
	{ 
		// Initializing String variable with null value 
		String str = null; 
		String message = (str == null) ? "" : 
						str.substring(0,5); 
		System.out.println(message);  
		str = "Edureka_Java_Blog"; 
		message = (str == null) ? "" : str.substring(0,5); 
		System.out.println(message); 
	} 
}
```

**输出:**

`Edurek`

至此，我们结束了 Java 中的空指针异常。我希望您对空指针异常有所了解。

*查看 Edureka 提供的  [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在“Java 中的空指针异常”博客的评论部分提到它，我们会尽快回复您。