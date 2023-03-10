# Java 中的 Extends 和 Implements 有什么区别？

> 原文：<https://www.edureka.co/blog/extends-vs-implements/>

关键字*扩展*和*实现，*都是用来执行[面向对象编程](https://www.edureka.co/blog/object-oriented-programming/)的继承概念，然而它们之间还是有细微的区别。这篇关于 Java 中的 extends vs implements 的文章将帮助您理解这些关键字之间的主要区别。

本文讨论的主题是:

*   [扩展关键字](#extends)
*   [实现关键字](#implements)
*   [伸展 vs 机具](#differences)

为了更好的理解扩展和实现的区别，你还需要学习和理解 Java 中[抽象类和接口](https://www.edureka.co/blog/difference-between-abstract-class-and-interface#abstractclassVSinterface)的 区别。

**扩展关键字**

当一个子类`extends`继承另一个[类](https://www.edureka.co/blog/java-objects-and-classes/#javaclass)时，它允许该子类继承(即。重用)并覆盖超类型中定义的代码。简单地说，使用 extends 关键字，新创建的类(子类)可以继承现有类(超类)的特性。此外，它可以覆盖超类中定义的[方法](https://www.edureka.co/blog/java-methods/)。在 Java 中，一个类永远不能扩展一个以上的超类。 这里有一个[示例程序](https://www.edureka.co/blog/java-programs/)演示抽象类:

```
package MyPackage;

class A {
	String s;
	A(String s1)
	{
		s = s1;
	}
	void display()
	{
		System.out.println(s);
	}

}

 class B extends A {
	String l;
	B(String s1, String s2)
	{
		super(s1);
		l = s2;
	}
	void display()
	{
		super.display();
		System.out.println(l);
	}

}

class ExtendsExample{
    public static void main(String args[]) {

    	A ob = new B("Welcome", "To Edureka");
    	ob.display();

    	}
    }
```

欢迎来到爱德华卡

**解释:**在上面的代码中，你可以观察到 B 类扩展了 A 类，它拥有 display()方法的访问权，并且覆盖了 A 类中定义的 display()方法，这种巨大的力量来自于使用 extends 关键字。

## **实现关键字**

当一个类 `implements` 一个接口时，它必须提供一个[接口](https://www.edureka.co/blog/java-interface/)中声明的所有方法的实现。如果该类不希望提供实现，它可以将自己声明为一个抽象类。同样，一个接口永远不能实现另一个接口，因为实现意味着定义方法，而接口总是有抽象方法，所以一个接口永远不能实现另一个接口。 这里有一个演示抽象类的示例程序:

```
package MyPackage;

interface XYZ{

	void display(String s);
	void show(int i);
}

class Demo implements XYZ{

	public void show(int i){
		System.out.println("integer value:" +i);
		}
	public void display(String s){
		System.out.println("string value:" +s);
	}
}

class ImplementExample {
	public static void main(String args[]) {

		XYZ d = new Demo();
		d.display("TechDifferences");
		d.show(2);

	}

}

```

**输出:**

```
string value:TechDifferences
integer value:2

```

在上面的代码中，您可以观察到演示类实现了在接口 XYZ 中声明的两个方法。

从上面的内容，你可能已经注意到了 [Java](https://www.edureka.co/blog/java-tutorial/) 中 extends 和 implements 的关键区别。现在让我们继续列出其他不同之处。

## **伸展 vs 机具**

下表列出了关键字 extends 和 implements 之间的主要区别。

| **比较特征** | **延伸** | **实现** |
| 履行 | 一个类可以继承另一个类，或者一个接口可以使用关键字 extends 继承其他接口 | 一个类可以使用关键字 implements 实现一个接口 |
| 方法 | 扩展超类的子类可能覆盖也可能不覆盖超类中的所有方法 | 实现一个接口的类必须实现该接口的所有方法。 |
| 班级 | 一个类只能扩展一个超类。 | 一个类可以同时实现任意数量的接口 |
| 连接 | 一个接口可以扩展任意数量的接口 | 一个接口永远不能实现任何其他接口 |

好了，现在你来看一下[Java](https://www.edureka.co/blog/java-tutorial/)中扩展和实现的关键区别

这就把我们带到了这篇文章的结尾。我们讨论了 extends 和 implements 关键字之间的主要区别。总之，两者都用于执行 Java 的继承概念，但是方式不同。

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这个“Java 中的扩展 vs 实现”* *的评论部分提到它，我们会尽快回复你。*