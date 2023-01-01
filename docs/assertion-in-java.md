# 如何用 Java 实现断言？

> 原文：<https://www.edureka.co/blog/assertion-in-java/>

经常需要验证我们程序中的条件。Java 中的 assert 关键字允许用户验证或测试程序中所做的假设。本文将向您介绍在 [Java](https://www.edureka.co/blog/java-tutorial/) 中的断言。

本文将涉及以下几点:

*   [在 Java 中声明断言](#DeclaringAssertionInJava)
*   [启用断言](#EnableAssertions)
*   [禁用断言](#DisableAssertions)
*   [哪里用断言而不用？](#WhereToUseAssertionAndNot?)
*   [Java 中断言的示例程序](#SampleProgramForAssertionInJava)

让我们从这篇文章开始吧

## **在 Java 中声明断言**

assert 语句与布尔表达式一起使用，可以声明如下:

```
assert expression;
```

声明断言的另一种方式如下:

```
assert expression1 : expression2;
```

**例子**

```

import java.util.Scanner;
public class Test
{
public static void main( String args[] )
{
int value = 18;
assert value >= 20 : " Eligible";
System.out.println("Value: "+value);
}
}

```

**输出**

数值:18

启用断言后的输出如下:

线程“main”Java . lang . assertion 中出现异常错误:合格

继续 Java 文章中的断言，

## **启用断言**

必须注意，默认情况下，断言是禁用的。

启用断言语句的语法如下:

```
java –ea Test
```

启用断言的另一种方法是:

```
java –enableassertions Test
```

继续，让我们看看如何禁用断言，

## **禁用断言**

断言语句可以被禁用，如下所示:

```
java –da Test
```

启用断言的另一种方法是:

```
java -disableassertions Test
```

**使用断言的原因**

用户可能想要使用断言的原因有多种:

*   确保注释中定义的假设是正确的。
*   以确保不会接触到开关盒。
*   检查对象的状态。

继续 Java 文章中的断言

## **哪里用断言而不用？**

#### **在哪里使用断言？**

*   方法开头的条件事例和条件。
*   私有方法的参数。

#### **哪里不使用断言？**

*   不应该使用断言来检查用户提供的公共方法中的参数。
*   断言不应用于命令行参数。
*   不应该使用断言来替换错误消息。

继续 Java 文章中这个断言的最后一点

## **Java 中断言的示例程序**

```

import java.util.Scanner;
public class Test
{
public static void main( String args[] )
{
Scanner scanner = new Scanner( System.in );
System.out.print("Enter the ID ");
int value = scanner.nextInt();
assert value>=15:" Invalid";
System.out.println("Value "+value);
}
}

```

**输出**

输入 ID

线程“main”Java . lang . assertion 中出现异常错误:无效

为了确保程序中所做的假设是正确的，断言被证明是一个重要的关键词。

这样，我们就结束了这篇关于“Java 中的断言”的文章。如果你想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)提供的 [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。