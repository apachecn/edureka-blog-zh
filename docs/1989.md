# Java 中的布尔类是什么，如何使用？

> 原文：<https://www.edureka.co/blog/java-boolean-class/>

我很确定你一定遇到过布尔这个术语。你们中的许多人也知道它的用法。所以，这篇关于 *[Java](https://www.edureka.co/blog/java-tutorial/)* 中布尔类的文章将帮助你了解这个类的工作原理以及围绕它的一些话题。

我将详细讨论这些主题:

我们开始吧！

## **什么是 Java 中的布尔类？**

Java.lang.package 在 Java 中提供了一个 *[包装类](https://www.edureka.co/blog/wrapper-class-in-java/)* 布尔。Boolean 类将基本类型 Boolean 的值包装在一个对象中。这个类有助于提供在处理布尔变量时将布尔转换成字符串以及将字符串转换成布尔的方法。问题是我们如何创建一个布尔对象？这个类为我们提供了两个构造函数来完成我们的目标。

让我们看看如何！

## **布尔类中的构造函数**

布尔类中有两个 *[构造函数](https://www.edureka.co/blog/constructor-in-java/)* :

```
Boolean b = new Boolean (boolean value);
```

此构造函数创建传递布尔值的布尔对象。

```
Boolean b = new Boolean (String s);
```

这个构造函数有助于创建一个布尔对象，如果字符串参数不为空且相等，则创建值 true。

继续，让我们看看布尔类提供的字段！

## **字段**

**静态布尔真:**引用原始值真的布尔对象。 **静态布尔 FALSE:** 布尔对象所指的原始值 FALSE。 **静态类:**表示原始类型 Boolean 的类对象。

下一部分是关于布尔类中的方法。

## **方法**

Boolean value():Java . lang . Boolean . Boolean value()它将布尔对象的值赋给布尔原语。

```
public class Example
{
public static void main(String[] args)
{
// creating different Boolean objects
Boolean b1 = new Boolean("True");
Boolean b2 = new Boolean("False");
Boolean b3 = new Boolean("EDUREKA");
// getting primitive boolean value
boolean b4 = b1.booleanValue();
boolean b5 = b2.booleanValue();
boolean b6 = b3.booleanValue();
System.out.println(b4);
System.out.println(b5);
System.out.println(b6);
}
}

```

**输出:** 真假假**compare to():**Java . lang . Boolean . compare to(Boolean arg)它将这个布尔实例与传递过来的布尔实例进行比较。**hashCode():**Java . lang . boolean . hashCode()它返回所赋布尔对象的散列码值。

```
public class Example
{
public static void main(String[] args)
{
// creating different Boolean objects
Boolean b1 = new Boolean("True");
Boolean b2 = new Boolean("False");
Boolean b3 = new Boolean("TRue");
Boolean b4 = new Boolean(null);
System.out.println(b1.hashCode());
System.out.println(b2.hashCode());
System.out.println(b3.hashCode());
System.out.println(b4.hashCode());
}
}
```

**输出:**1231123712311237

**toString():**Java . lang . boolean . toString()它根据布尔值返回布尔对象的字符串表示。

```
public class Example
{
public static void main(String[] args)
{
// creating different Boolean objects
Boolean b1 = new Boolean("True");
Boolean b2 = new Boolean("False");
Boolean b3 = new Boolean("EDUREKA");
Boolean b4 = new Boolean(null);
// getting String value of Boolean objects
String str1 = b1.toString();
String str2 = b2.toString();
String str3 = b3.toString();
String str4 = b4.toString();

System.out.println(str1);
System.out.println(str2);
System.out.println(str3);
System.out.println(str4);
}
}
```

**输出:** 真假假假

**Equals():**Java . lang . boolean . Equals()如果没有传递空参数，则返回 true。它应该是一个布尔对象，表示与此对象相同的布尔值。

```
public class Example
{
public static void main(String[] args)
{
// creating different Boolean objects
Boolean b1 = new Boolean("True");
Boolean b2 = new Boolean("False");
Boolean b3 = new Boolean("TrUe");
Boolean b4 = new Boolean(null);
// checking equality of Boolean objects
System.out.println(b1.equals(b2));
System.out.println(b2.equals(b4));
System.out.println(b1.equals(b3));
System.out.println(b1.equals(b4));
}
}
```

**输出:** 假真真假

至此，本教程到此结束。我希望你现在清楚这个话题了。继续阅读，继续探索！

如果您发现这篇文章与“Java 中的布尔类”相关，请查看一下  [*Edureka Java 认证培训*、](https://www.edureka.co/java-j2ee-soa-training) 这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。

我们在这里帮助你踏上旅程的每一步，我们为想成为 Java 开发者的学生和专业人士设计了一套课程。该课程旨在让你在 Java 编程方面有一个良好的开端，并训练你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

如果您遇到任何问题，请在“Java 布尔类”的评论区提出您的所有问题，我们的团队将很乐意回答。