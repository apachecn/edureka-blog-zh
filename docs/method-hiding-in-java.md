# 如何在 Java 中实现方法隐藏

> 原文：<https://www.edureka.co/blog/method-hiding-in-java/>

在 [java](https://www.edureka.co/blog/java-tutorial/) 中，你需要小心方法隐藏的可能性。在子类中用相同类型和签名创建的方法可以隐藏超类中的变量。在本文中，我们将通过以下方式理解 Java 中的方法隐藏:

*   [什么是方法隐藏？](#what)
*   [隐藏 Java 代码的方法](#code)
*   [总结](#summary)

## **什么是方法隐藏？**

方法隐藏在功能上非常类似于方法重写。在重写中，如果你在子类中创建一个具有相同类型和签名的方法，那么它允许基于实例的类型调用方法。

![Java Logo](img/1ebba2dd90ef6924482a727cdd99861a.png)

在超类和子类中具有相同类型和签名的静态方法的情况下，子类中的方法隐藏超类中的方法。

## **隐藏 Java 代码的方法**

```
package com.test;

class Parent {

	public static void foo() {
		System.out.println("Inside foo method in parent class");
	}

	public void bar() {
		System.out.println("Inside bar method in parent class");
	}
}

class Child extends Parent {
	// Hiding
	public static void foo() {
		System.out.println("Inside foo method in child class");
	}

	// Overriding
	public void bar() {
		System.out.println("Inside bar method in child class");
	}
}

public class Code {

	public static void main(String[] args) {
		Parent p = new Parent();
		Parent c = new Child();
		System.out.println("****************Method Hiding*******************");
		p.foo(); // This will call method in parent class
		c.foo(); // This will call method in parent class
		System.out.println("****************Method overriding*******************");
		p.bar(); // This will call method in parent class
		c.bar(); // This will call method in child class

	}
}
```

**输出:**

![Method-Hiding-in-Java](img/956dd6a7b88ff04fe14f34a31e1e1962.png)

在上面的例子中，子类 Child 的静态方法 foo()与超类 Parent 中的静态方法具有相同的名称和签名。当我们调用 p.foo()和 c.foo()时，它调用父类中的 foo()方法

不像在方法覆盖中，p.bar()调用父类中的方法，而 c.bar()调用子类中的方法。

由于静态方法在编译时被解析，编译时首先编译父类，然后编译子类，我们不能有两个同名的静态方法，两个 foo 方法都被解析为父类的 foo()方法。

## **总结**

如果一个子类有一个与超类中的静态方法具有相同名称和签名的静态方法，那么超类中的方法将被调用，而不管它是从子类还是从父类调用。

在方法覆盖的情况下，我们覆盖来自父类的方法，即，如果子类具有与超类中的非静态方法具有相同名称和签名的非静态方法，则根据使用的引用调用相应的方法，即，如果父类的对象用于调用父类中的非静态方法，则使用来自父类的方法，如果子类的对象用于调用子类中的非静态方法，则使用来自子类的方法。

至此，我们结束了 Java 文章中的方法隐藏。*查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。*

有问题要问我们吗？请在这篇“隐藏在 Java 中的方法”博客的评论部分提到它，我们会尽快回复您。