# Java 中交换两个数的方法

> 原文：<https://www.edureka.co/blog/ways-for-swapping-two-numbers-in-java/>

处理数据时，交换数字可能至关重要。在本文中，我们将探索在 Java 中交换两个数的方法。本文将涉及以下几点:

*   [使用临时变量交换两个数](#SwappingtwonumbersusingaTemporaryVariable)
*   [不使用临时变量交换两个数](#SwappingtwonumberswithoutusingaTemporaryVariable)

在 Java 中交换两个数是每个程序员都必须知道的事情。交换号码主要有两种方法。本文对这些方法进行了详细的讨论。

继续这篇关于在 Java 中交换两个数的文章。

## **使用临时变量交换两个数**

```
public class Main {
public static void main(String[] args) {
float a = 1.18f, b = 2.69f;
System.out.println("Before swapping");
System.out.println("First number = " + a);
System.out.println("Second number = " + b);
// Value of a is assigned to temporary
float temp = a;
// Value of b is assigned to first
a = b;
// Value of temp (which contains the initial value of first) is assigned to second
b = temp;
System.out.println("After swapping");
System.out.println("First number = " + a);
System.out.println("Second number = " + b);
}
}

```

这里，要交换的数字被分配给变量 a 和 b。第一个变量(即 a)存储在变量 temp 中，第二个变量(即 b)的值存储在第一个变量中。然后将 temp 的值存储在 b 中。

该程序的输出如下:

## **输出:**

对换前第一个数字= 1.18 第二个数字= 2.69 对换后第一个数字= 2.69 第二个数字= 1.18

继续这篇关于在 Java 中交换两个数的文章。

## **不使用临时变量交换两个数**

```
public class Main {
public static void main(String[] args) {
float a = 18.0f, b = 28.5f;
System.out.println("Before swapping:");
System.out.println("First number = " + a);
System.out.println("Second number = " + b);
a = a - b;
b = a + b;
a = b - a;
System.out.println("After swapping:");
System.out.println("First number = " + a);
System.out.println("Second number = " + b);
}
}

```

在这个例子中，我们没有使用临时变量。取而代之的是使用简单的数学公式:a = a–b 即(18.0 f–28.5 f)然后将第二个数字加入其中: b = a + b 即(18.0 f–28.5 f)+28.5 f = 18.0 f 为了交换，使用以下逻辑:a = b–a 即 18.0 f-(18.0 f–28.5 f)= 28.5 f

该程序的输出如下:

## **输出:**

对换前:首数= 18.0 次数= 28.5 对换后:首数= 28.5 次数= 18.0

因此，通过使用所讨论的方法，可以有效地交换数字。

这样，我们就结束了这篇关于“在 Java 中交换两个数”的文章。如果你想了解更多，可以去看看 Edureka 值得信赖的在线学习公司提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。