# 什么是 JavaBeans？JavaBeans 概念介绍

> 原文：<https://www.edureka.co/blog/what-is-javabeans/>

可重用性是任何编程语言的主要概念。JavaBean 是一个软件组件，它被设计成可以在各种环境中重用。让我们深入主题，理解这篇“什么是 JavaBeans”文章中的概念。

以下几点将是我们讨论的主题:

*   [什么是 JavaBeans？](#java-bean)
*   [JavaBean 有哪些属性？](#properties)
*   [示例程序:JavaBeans 的实现](#demo)
*   [JavaBean s 的优势](#advantages)
*   [JavaBean s 的缺点](#disadvantages)

我们开始吧！

## **什么是 JavaBeans？**

JavaBeans 是一个用 Java 编程语言编写的可移植的、独立于平台的模型。它的组件被称为 beans。

简单来说，JavaBeans 是将几个[对象](https://www.edureka.co/blog/java-object/)封装成一个对象的[类](https://www.edureka.co/blog/java-objects-and-classes/#javaclass)。它有助于从多个位置访问这些对象。JavaBeans 包含几个元素，比如构造函数、Getter/Setter 方法等等。

JavaBeans 有几个应该遵守的约定:

*   Beans 应该有一个默认的[构造函数](https://www.edureka.co/blog/constructor-in-java/)(没有参数)
*   Beans 应该提供 getter 和 setter 方法
    *   一个 *getter 方法*被用来读取一个可读属性的值
    *   为了更新该值，应该调用一个 *setter 方法*
*   Bean 应该实现 *java.io.serializable* ，因为它允许保存、存储和恢复您正在处理的 JavaBean 的状态

现在您已经熟悉了基础知识，让我们详细了解 JavaBeans 的属性。

## **什么是 JavaBean 属性？**

对象的用户可以访问 JavaBean 属性。该特性可以是任何 Java 数据类型，包含您定义的类。可以是以下几种模式:*读、写、只读或只写*。JavaBean 特性通过两个[方法](https://www.edureka.co/blog/java-methods/)来访问:

**1。*****getEmployeeName()***

例如，如果雇员的名字是 firstName，那么方法名应该是 getFirstName()来读取该雇员的名字。这个方法被称为 ***访问器。*** 属性的吸气剂方法如下:

1.  必须是公开的
2.  返回类型不应为空
3.  getter 方法应该以单词 *get* 为前缀
4.  这不需要任何争论

**2。*****setEmployeeName()***

例如，如果雇员的名字是 firstName，那么方法名应该是 setFirstName()来写雇员的名字。这种方法被称为 ***变异器。*** 属性的 setter 方法:

1.  必须是公开的
2.  返回类型应该为空
3.  setter 方法必须以单词 *set* 为前缀
4.  这需要一些争论

现在您已经获得了一些关于 JavaBeans 的理论知识，让我们继续并理解实现过程。

## **示例程序:JavaBeans 的实现**

下面显示的示例程序演示了如何实现 JavaBeans。

```
public class Employee implements java.io.Serializable 
{ 
private int id; 
private String name; 
public Employee() 
    { 
    } 
public void setId(int id) 
    { 
        this.id = id; 
    } 
public int getId() 
    { 
        return id; 
    } 
public void setName(String name) 
    { 
        this.name = name; 
    } 
public String getName() 
    { 
        return name; 
    } 
} 
```

编写下一个程序是为了访问我们在上面创建的 JavaBean 类:

```
public class Employee1 {
public static void main(String args[])
{
	Employee s = new Employee(); 
    s.setName("Chandler"); 
    System.out.println(s.getName()); 
}
}

```

**输出:**

钱德勒

这就是如何实现一个访问 JavaBean 类的 Java 程序。

## **JavaBean s 的优势**

下面的列表列举了 JavaBeans 的一些优点:

**便携式**

JavaBeans 组件完全是用 Java 构建的，因此完全可以移植到任何支持 [Java 运行时环境](https://www.edureka.co/blog/what-is-java/#ComponentsinJava)的平台。所有平台细节以及对 JavaBeans 的支持都是由 Java 虚拟机实现的。

**小巧方便**

JavaBeans 组件易于创建和使用。这是 JavaBeans 架构的一个重要的焦点部分。写一个简单的 Bean 并不需要太多的努力。此外，bean 是轻量级的，因此，它不必携带大量继承的行李来支持 bean 环境。

**承载了 Java 平台的优势**

JavaBeans 非常兼容，没有任何新的复杂机制向运行时系统注册组件。

虽然这些听起来都不错，但是使用 JavaBeans 也有一些缺点。现在，让我们来看看这些是什么。

## **JavaBean s 的缺点**

1.  JavaBeans 是可变的，因此缺乏不可变对象所提供的优势。
2.  JavaBeans 在构建过程中会处于不一致的状态。

至此，我们已经结束了这篇“什么是 JavaBeans”的文章。我希望这里讨论的内容能够增加您的 Java 知识。那么，继续探索 Java 世界吧。敬请期待！

*查看 Edureka 提供的* [***Java 认证课程***](https://www.edureka.co/java-j2ee-training-course) *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这个“什么是 JavaBeans”博客的评论部分提到它，我们会尽快回复您。