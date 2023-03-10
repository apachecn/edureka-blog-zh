# 关于 Java 中的 ToString，您需要知道的一切

> 原文：<https://www.edureka.co/blog/tostring-in-java/>

Java 是一种通用的编程语言，它激励了许多人将实现 Java 作为职业。想学 Java 的人通常从基础开始，并迷失在它提供的各种概念中。这篇关于 Java 中 toString 的文章将向您介绍一个基本但相当重要的主题。

以下是本文将要讨论要点:

*   [toStringInJava](#toStringInJava)
*   【toString 的例子
*   [必要的超驰](#NecessaryOverriding)

让我们从本文的第一个主题开始，

## **Java 中的 toString**

那么这个方法到底是什么呢？对象类是 Java 中的父类。它包含 toString 方法。toString 方法用于返回对象的字符串表示形式。如果打印任何对象，toString()方法由 java 编译器在内部调用。否则，调用用户实现或重写的 toString()方法。

以下是使用这种方法的一些优点。

**优势**

如果你覆盖了 Object 类的 toString()方法，它会返回对象的值，因此你不需要写很多代码。

## 【toString 的例子

```
public class Employee{
int id;
String name;
String city;
Employee(int id, String name, String city){
this.id=id;
this.name=name;
this.city=city;
}
public static void main(String args[]){
Employee e1=new Employee(01,"Ari","NewYork");
Employee e2=new Employee(02,"Jon","Chicago");
System.out.println(e1);//compiler writes here s1.toString()
System.out.println(e2);//compiler writes here s2.toString()
}
}

```

**输出:**

员工@6d06d69c

员工@7852e922

该代码打印示例中对象的 HashCode 值。

在本文的下一部分，让我们试着调整我们的方法，

## **必要的超驰**

要返回用户指定的值，必须进行覆盖:

```
public class Employee{
int id;
String name;
String city;
Employee(int id, String name, String city){
this.id=id;
this.name=name;
this.city=city;
}
public String toString(){//overriding the toString() method
return id+" "+name+" "+city;
}
public static void main(String args[]){
Employee e1=new Employee(01,"Ari","NewYork");
Employee e2=new Employee(02,"Jon","Chicago");
System.out.println(e1);
System.out.println(e2);
}
}

```

**输出:**

1 纽约阿里

乔恩·芝加哥

因此，这是在 Java 中使用 toString 方法时要遵循的过程。

这样，我们就结束了这篇关于“Java 中的 toString”的文章。如果您想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 在线课程](https://www.edureka.co/java-j2ee-training-course)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。