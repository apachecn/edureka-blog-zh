# 类和接口的区别是什么？

> 原文：<https://www.edureka.co/blog/what-are-the-difference-between-class-and-interface/>

Java 中的类和接口是奠定 [Java](https://www.edureka.co/java-j2ee-soa-training) 基础的两个最重要的概念。但是人们经常对他们的工作感到困惑。通过这篇文章，我将让你全面了解 Java 中类和接口的区别。

以下是我将在本文中涉及的主题:

*   Java 中的[类](#class)
*   [Java 中的界面](#interface)
*   [Java 中类和接口的区别](#classvsinterface)

## Java 中的**类**

Java 中的类是创建对象的蓝图。每个 Java 类都必须属于一些包，这些包无非是 一组相似类型的类、[接口](https://www.edureka.co/blog/java-collections/)，以及捆绑在一起的 **子包。**类是定义对象行为和属性的逻辑实体。换句话说，Java 中的一个  *[类](https://www.edureka.co/blog/java-objects-and-classes/)* 用于创建和定义  [对象](https://www.edureka.co/blog/java-object/)、对象数据类型、  [方法](https://www.edureka.co/blog/java-methods/)。它只能通过其对象从外部访问。类作为一个整体是类别，而对象是每个类别中的项目。类声明通常由以下部分组成:

*   修饰语
*   类别名
*   关键词
*   花括号{}内的类主体

一个类可以被任意数量的类继承，使用下面的扩展，我已经展示了一个类的框架:

```
modifier class class_name{
/*
fields
...
methods
*/
}
```

如果你想了解更多关于类的知识，你可以参考我们关于 Java 中 [**类的文章。现在让我们在这篇文章中更进一步，学习什么是 Java 中的接口。**](https://www.edureka.co/blog/java-objects-and-classes/)

## Java 中的**接口**

Java 中的[接口](https://www.edureka.co/blog/java-interface/)是 Java 中定义的引用类型之一。它在语法上类似于一个类，但是只包含方法声明，而忽略了它们的实现。引入这个概念是为了消除 Java 类一次只能继承一个类的限制。要创建一个接口，使用关键字 interface。除了抽象方法，*接口*还可以包括 *[常量](https://www.edureka.co/blog/what-is-java-constant/)、[静态方法](https://www.edureka.co/blog/static-keyword-in-java/)、嵌套接口*和*默认方法。*任何数量的类都可以通过使用 [**实现**](https://www.edureka.co/blog/implements-in-java/) 关键字来实现一个接口。但是您必须确保实现接口的类提供该接口中声明的所有方法的实现。此外，就像类一样，一个接口也可以使用 [**extend**](https://www.edureka.co/blog/extends-vs-implements/) 关键字继承其他接口。但是实现类需要提供两个接口中所有方法的实现。 同样，一个接口中的方法必须总是被声明为公共的，以提供实现类的可访问性。下面我创建了一个界面的框架 :

```
interface interface_name {

/*
modifier type var_name= value;
modifier type method1(parameter-list);
modifier type method2(parameter-list);
.
.
*/
}
```

如果你想了解更多关于接口的知识，可以参考我们关于 Java 中 **[接口的文章。现在，让我们在本文中更进一步，看看 Java 中类和接口之间的表格差异。](https://www.edureka.co/blog/java-interface/)**

## **Java 中类和接口的区别**

| **类** | **界面** |
| 可以实例化一个类 | 接口永远不能被实例化 |
| **类**关键字用于声明它 | 使用了**接口**关键字 |
| 一个类的成员可以被声明为私有的、公共的或受保护的 | 接口的成员总是被声明为公共的 |
| 包含具体的方法，即带有主体的方法 | 包含抽象方法，即没有主体的方法 |
| **扩展了**关键字用于继承一个类 | **实现**关键字用于使用一个接口 |
| 可以包含 [final](https://www.edureka.co/blog/final-finally-and-finalize-in-java/) 和静态方法 | 不能包含最终方法或静态方法 |
| Java 类可以有构造函数 | 接口不能有构造函数 |
| 一个类只能扩展一个类，但可以实现任意数量的接口 | 一个接口可以扩展任意数量的接口，但不能实现任何接口 |

这就把我们带到了这篇关于 Java 中类和接口的区别的文章的结尾。我希望我能够保持概念的清晰和简洁。如果你想了解更多关于 Java 的知识，你可以参考我们的[其他 Java 博客](https://www.edureka.co/blog/what-is-java/)。

*既然你已经了解了 Java 中类和接口的区别，那就来看看 Edureka 的* [***Java 认证培训***](https://www.edureka.co/java-j2ee-soa-training)*吧，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在“类和接口的区别”这篇文章的评论部分提到它，我们会尽快回复您。*