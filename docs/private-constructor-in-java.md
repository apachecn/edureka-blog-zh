# 如何在 Java 中实现私有构造函数

> 原文：<https://www.edureka.co/blog/private-constructor-in-java>

[构造函数](https://www.edureka.co/blog/constructor-overloading-in-java/)用于初始化对象的状态。与方法类似，构造函数也可以保存一组语句，这些语句只能称为指令。在本文中，我们将按以下顺序讨论 [Java](https://www.edureka.co/blog/java-tutorial/) 中的私有构造函数:

*   [Java 中的构造函数简介](#intro)
*   [单例类](#singleton)
*   [Java 中私有构造函数的影响](#impact)
*   [内部构造函数链接](#internal)
*   [单例类设计模式](#design-pattern)

## **Java 中的构造函数简介**

构造函数在对象创建时执行。为了更好地理解构造函数及其应用程序，只需将一个盒子看作一个类。假设一个盒子类有一些类变量(即长度、宽度和高度)。然而，在创建其对象时(即，盒子存在于计算机的存储器中)，也可以存在没有为其尺寸量定义值的盒子。

很明显，没有。

因此，引入了一个构造函数来在对象创建时给类变量赋值。这可以由程序员或 Java 本身明确完成。当由 Java 自己完成时，它被称为默认构造函数。

必须理解，任何拥有由编码者提供给构造函数的访问说明符的方法，都是私有的，只能在类本身内部访问。

![Private Constructor in Java](img/f310a753a911602b1f1c80acb3953b05.png)

## **单例类**

从名字本身来看，我们可以称一个类为 singleton，如果它将该类的对象数量限制为一个的话。在这种情况下，一个类不能有多个对象。在像网络和数据库连接这样的概念中，单例类被广泛使用。单例类是一个**私有类**。

必须有另一种方法来提取该类的实例，并有一个返回方法来取回结果。下面是一个恰当的例子。第一个象形图描述了可能的结果，其中“a.x”的值等于 20,“b . x”的值也等于 20。在代码中，当我们定义单例私有类时，它的构造函数不能在类外被访问。

`Value of a.x = 20`

`Value of b.x = 20`

```
// Java program to demonstrate implementation of Singleton 
// pattern using private constructors. 
import java.io.*; 

class MySingleton 
{ 
	static MySingleton instance = null; 
	public int x = 10; 

	// private constructor can't be accessed outside the class 
	private MySingleton() { } 

	// Factory method to provide the users with instances 
	static public MySingleton getInstance() 
	{ 
		if (instance == null)		 
			instance = new MySingleton(); 

		return instance; 
	} 
} 

// Driver Class 
class Main 
{ 
public static void main(String args[])	 
{ 
	MySingleton a = MySingleton.getInstance(); 
	MySingleton b = MySingleton.getInstance(); 
	a.x = a.x + 10; 
	System.out.println("Value of a.x = " + a.x); 
	System.out.println("Value of b.x = " + b.x); 
}	 
}
```

## **Java 中私有构造函数的影响**

私有构造函数不能访问另一个类的派生类。因此，我们必须给出一个调用私有构造函数的公共函数。万一对象没有初始化，或者如果对象已经初始化，我们必须向它发送回一个实例。这对无法初始化的对象尤其有用。私有构造函数用于以下情况:

*   各自的类，它们只有静态方法和成员。
*   特定的类，只有广泛使用的静态最终成员(常量)。
*   并入单件。
*   融入工厂方法。

使用类型安全的枚举。

## **内部构造函数链接**

内部构造函数链接是当一个构造函数调用同一个类的另一个构造函数时，它可以被称为构造函数链接。我们有责任使用这个关键字来调用该类的另一个构造函数。在某些情况下，它用于定义类变量的一些默认值。请记住，另一个构造函数调用必须是代码块中的第一条语句。

另外，不要有递归调用，会造成死循环。现在让我们看一个 java 程序中构造函数链接的例子。

```
package com.journaldev.constructor;
public class Employee {
	private int id;
	private String name;
	public Employee() {
		this("John Doe", 999);
		System.out.println("Default Employee Created");
	}
	public Employee(int i) {
		this("John Doe", i);
		System.out.println("Employee Created with Default Name");
	}
	public Employee(String s, int i) {
		this.id = i;
		this.name = s;
		System.out.println("Employee Created");
	}
	public static void main(String[] args) {
		Employee emp = new Employee();
		System.out.println(emp);
		Employee emp1 = new Employee(10);
		System.out.println(emp1);
		Employee emp2 = new Employee("Pankaj", 20);
		System.out.println(emp2);
	}
	@Override
	public String toString() {
		return "ID = "+id+", Name = "+name;
	}
	public int getId() {
		return id;
	}
	public void setId(int id) {
		this.id = id;
	}
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
}
```

## **单例类设计模式**

![Singleton-Design-Pattern](img/1e8fb29139cdf45f106833071e5e0ad1.png)

*   **类级成员(急切初始化方法):**

1.  首先，创建一个 singleton 类的私有常量静态实例。

2.  然后，编写一个静态方法，它返回一个单例类的对象，我们将它创建为一个类成员实例。

3.  可以将一个静态成员标记为 public 来直接访问常量静态实例。

4.  单例类在实例化方面不同于普通的 Java 类。在一个普通的类中，使用一个构造函数，但是对于单例类，我们使用 get Instance()方法。

*   **类级成员(惰性初始化方法):**

1.  首先，初始化一个私有的构造函数。

2.  然后创建这个单例类的私有静态实例。记住不要实例化它。

3.  然后，编写一个静态方法，检查静态实例成员是否为空，并初始化实例。最后，它返回 singleton 类的一个对象。

*   **类级成员(用双锁方法进行惰性初始化):**

考虑两个线程同时运行，当实例为空时，两个线程同时进入“if”语句。其中，一个线程进入同步块创建实例，而另一个线程被阻塞。当第一个线程驻留在 synchronized 块中时，队列中的线程创建另一个 singleton 对象。请注意，当第二个线程进入 synchronized 块时，它无法检查实例是否为非空。

*   **【使用嵌套内部类(惰性加载方法)】**

这里，它基于 Java 语言规范(JLS)。Java 虚拟机仅按需加载静态数据成员。因此，单例类首先由 JVM 加载。因此，在一个类中没有静态数据成员；

Singleton 类持有者不加载 SINGLE_INSTANCE。当我们调用 getIntance 方法时，只会发生这种情况。JLS 保证类初始化的执行。为静态 getInstance()方法的加载和初始化提供显式同步。由于初始化是以连续的方式创建静态变量 SINGLE_INSTANCE 的，所以 getInstance()的所有并发调用将返回相同的结果，而没有同步开销。

*   **利用枚举**

并非所有上述方法在所有情况下都是完整的解决方案。使用反射可以创建上述实现的多个实例。在这两种情况下，我们都可以绕过私有构造函数，创建多个实例。因此，一种新的方法是通过使用枚举来创建单例类。因为枚举字段是编译的时间常数，所以它们是其枚举类型的实例。它们是在首次引用枚举类型时构造的。

至此，Java 文章中的私有构造函数到此结束。我希望您已经理解了私有构造函数以及如何在 Java 中使用它们。

*查看 Edureka 提供的  [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这个“Java 教程”博客的评论部分提到它，我们会尽快回复您。