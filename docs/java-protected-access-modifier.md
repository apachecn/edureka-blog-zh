# Java 中保护什么，如何实现？

> 原文：<https://www.edureka.co/blog/java-protected-access-modifier/>

Java 提供了一组关键字 [**访问修饰符**](https://www.edureka.co/blog/access-modifiers-in-java/) 帮助我们设置类的可见性、 接口、变量、数据成员、方法、构造函数等。在 [Java](https://www.edureka.co/blog/java-tutorial/) 中支持 4 种类型的访问修饰符，默认、公共、私有和受保护。在本文中，我将只关注 Java 中的 protected，并帮助您对它有一个清晰的认识。

以下是我将在本文中讨论的主题:

*   [Java 里保护的是什么](#protected)
*   [受保护实现](#implementation)

## **Java 里保护什么？**

如前所述，Java 中的 protected 是一个访问修饰符，帮助程序员指定类的可见性，它的成员，[接口](https://www.edureka.co/blog/java-interface/)等等。当类成员在 Java 中被声明为 protected 时，它们只能在同一个[包](https://www.edureka.co/blog/packages-in-java/)中 访问，也只能被基类的直接子类访问。在 Java 中使用 protected 关键字时，必须记住只有类成员可以声明为 protected。在 Java 中，类和接口不能被声明为 protected。

现在你可能会想为什么类和接口不能被保护起来？

嗯，如果你从逻辑上思考，答案就很清楚了。如果一个类被保护，那么它将只对同一个包中的类可见。现在，正如我之前提到的，当任何东西在 Java 中被保护时，它对它的子类也是可见的。

但是，这里有一个模糊之处。对于扩展受保护类的其他类，父类必须是可见的。你将如何扩展一开始就不可见的东西？因此，这导致了模糊性，并且在 [Java](https://www.edureka.co/blog/java-tutorial/) 中不允许创建受保护的类。

现在让我们理解为什么接口不能被保护。嗯，在 Java 中，元素通常是受保护的，这样它们的实现就可以在其他人之间共享。但是在[接口](https://www.edureka.co/blog/java-interface/)的情况下，它们没有实现，所以共享它们没有意义。因此，接口中的所有方法都必须是公共的，这样任何类或 struts 都可以轻松实现它们。

因此，你可以在 Java 中只声明受保护的[方法](https://www.edureka.co/blog/java-methods/)和数据成员，而不是[类](https://www.edureka.co/blog/java-objects-and-classes/)或接口 。这有助于通过限制类成员的可访问性来封装代码。它还有助于防止数据滥用。

## **受保护的实现**

现在让我们试着实施我们到目前为止所学的内容。因此，在这里我将创建两个类，每个类属于一个单独的包。

***EduProtected.java 在包 edu 1***

```
package edu1;

public class EduProtected {
		 protected void message(String disp){
		     System.out.println("Package 1 message recieved: "+ disp);
		 }
}
```

***EduSubClass.java 在包 edu 2***

```
package edu2;
import edu1.EduProtected;

public class EduSubClass extends EduProtected {
	public static void main(String[] args) {
		EduProtected show = new EduProtected();
        // invokes message() from EduProtected class
        show.message("Hello from package2 subclass");
	}
}

```

**输出:**

收到包 1 消息:来自包 2 子类的 Hello

这就把我们带到了本文的结尾。如果你想了解更多关于 Java 的知识，你可以参考我们的[其他 Java 博客](https://www.edureka.co/blog/what-is-java/)。

*现在您已经了解了 Java 中受保护的内容，请查看 Edureka 提供的* [***Java 认证培训***](https://www.edureka.co/java-j2ee-soa-training)*，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这篇文章的评论部分提到它，我们会尽快回复你。*