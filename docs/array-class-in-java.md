# 什么是 Java 中的数组类，如何实现？

> 原文：<https://www.edureka.co/blog/array-class-in-java/>

我相信你们中的许多人已经熟悉了术语数组！在本教程中，我们将学习 [**Java**](https://www.edureka.co/java-j2ee-training-course) 中的数组类。 **java.util.package** 中的 Array 类是 java 集合框架的一部分。让我们详细研究一下这个话题。本文的议程是:

*   [什么是 Java 中的数组类？](#WhatisArrayclassinJava?)
*   [语法](#Syntax)
*   [数组类中的方法](#MethodsinArrayclass)
*   [我们为什么需要一个 Java 数组类？](#WhydoweneedJavaArrayclass?)

## **什么是 Java 中的数组类？**

**数组类**包含在 **java.util.package 中。** Java 数组是通过这个类提供的静态方法创建和访问的。这个类的方法可以通过类名来访问。只存在静态方法和 object 类的方法。这个类包含了各种操作数组的方法。

**类声明** 下面是你如何声明类。

```
public class Arrays
extends Object

```

**阶级阶层**

```
java.langhierarch
java.util.Arrays

```

**方法继承** 方法继承的是 **Java.util** 对象

继续，让我们看看这个类的语法。

**语法:**

```
Arrays.<function name>;

```

这个类中使用了几种方法。看看他们！

## **数组类中的方法**

| **方法** | **描述** |
| 静态 int 二进制搜索(elementToBeSearched) | 此方法使用二分搜索法算法搜索数组中的指定元素。 |
| 比较(数组 1，数组 2) | 它比较作为参数传递的两个数组。 |
| compareUnsigned(数组 1，数组 2) | 它比较两个数组，在数字上将元素视为无符号元素。 |
| 静态布尔值 deepEquals(对象[] a，对象[] b) | 如果两个指定的数组完全相等，则返回 true |
| 静态 int deepHashCode(Object[] a) | 它根据指定数组的“深层内容”返回哈希代码 |
| 等于(数组 1，数组 2) | 它检查两个数组是否相等 |
| fill(originalArray, fillValue) | 它将这个 fillValue 赋给这个数组的每个索引 |
| hashCode(originalArray) | 它返回指定数组的整数 hashCode。 |
| 不匹配(数组 1、数组 2) | 它搜索并返回两个指定数组之间第一个不匹配元素的索引。 |
| 静态列表 asList(T… a) | 它返回由指定数组支持的固定大小的列表 |
| copyOf(原始数组，新长度) | 它复制指定的数组，截断默认值(如果需要)，使副本具有指定的长度。 |
| 并行排序(原始数组) | 它使用并行排序对指定的数组进行排序。 |

现在，让我们来谈谈这个特定类的必要性！

## **为什么我们需要一个数组 Java 类？**

我列举几点来回答这个问题。你会遇到一些情况，你不得不应用循环的概念，但是数组 Java 类为你提供了一些静态方法。这些方法可以帮助你在不使用[循环](https://www.edureka.co/blog/loops-in-java/)的情况下执行任务！你可以排序数组，搜索数组，修改数组等等！

就这样，我们到了这篇文章的结尾。我希望你已经通过一些实时的例子理解了 Java 中的数组类，它们的类型，重要性以及它们的实现。

*既然您已经了解了基础知识，请查看 Edureka 的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate&[Spring](https://spring.io/projects/spring-framework)。*

有问题要问我们吗？在这个博客的评论部分提到它，我们会尽快回复你。