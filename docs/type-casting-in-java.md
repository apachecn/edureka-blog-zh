# 什么是 Java 中的类型转换，它是如何工作的？

> 原文：<https://www.edureka.co/blog/type-casting-in-java/>

编程就是摆弄数据。在 [Java](https://www.edureka.co/blog/java-tutorial/) 中，有很多数据类型。大多数时候，在编码时，有必要改变数据的类型来理解变量的处理，这被称为类型转换。在本文中，我将讨论 Java 中类型转换的基础知识。

Below topics are covered in this article:

*   [什么是类型转换？](#WhatisTypeCasting?)
*   [加宽铸件](#WideningCasting)
*   [缩小铸件](#NarrowingCasting)

我们开始吧！

## **什么是类型转换？**

类型转换只不过是将一个原始数据类型[的值赋给另一个原始数据类型](https://www.edureka.co/blog/data-types-in-java/)。将一种数据类型的值赋给另一种数据类型时，应该注意数据类型的兼容性。如果它们兼容，那么 [Java](https://www.edureka.co/blog/what-is-java/) 将自动执行转换，称为*自动类型转换*，如果不兼容，那么它们需要被强制转换或显式转换。

Java 中有两种类型的转换，如下所示:

*   **扩大转换(自动)**–这涉及到将较小的数据类型转换为较大的类型大小。

    `byte -> short -> char -> int -> long -> float -> double`

*   **缩小转换(手动)**–这涉及到将较大的数据类型转换成较小的类型。

    `double -> float -> long -> int -> char -> short -> byte`

现在让我们进入类型转换的类型的细节。

## **加宽铸件**

当两种数据类型自动转换时，会发生这种类型的转换。它也被称为隐式转换。当两种数据类型兼容时，以及当我们将较小的[数据类型](https://www.edureka.co/blog/data-types-in-java/)的值赋给较大的数据类型时，就会发生这种情况。

**例如，**数值数据类型相互兼容，但不支持从数值类型到 char 或 boolean 的自动转换。此外，char 和 boolean 是不兼容的。现在让我们为隐式类型转换编写一个逻辑来理解它是如何工作的。

```
public class Conversion{
public static void main(String[] args)
{
int i = 200;

//automatic type conversion
long l = i;

//automatic type conversion
float f = l;
System.out.println("Int value "+i);
System.out.println("Long value "+l);
System.out.println("Float value "+f);
}
}
```

**输出:**

```
Int value 200
Long value 200
Float value 200.0
```

现在让我们进一步了解显式类型转换是如何工作的。

## **缩小铸件**

在这种情况下，如果您想将较大数据类型的值赋给较小的数据类型，可以执行*显式类型转换*或缩小。这对于无法进行自动转换的不兼容数据类型非常有用。

让我们借助一个例子来理解这一点。

```
//Java program to illustrate explicit type conversion
public class Narrowing
{
public static void main(String[] args)
{
double d = 200.06;

//explicit type casting
long l = (long)d;

//explicit type casting
int i = (int)l;
System.out.println("Double Data type value "+d);

//fractional part lost
System.out.println("Long Data type value "+l);

//fractional part lost
System.out.println("Int Data type value "+i);
}
}
```

**输出:**

```
Double Data type value 200.06
Long Data type value 200
Int Data type value 200
```

现在您已经知道了如何执行显式类型转换，让我们进一步了解如何在 Java 表达式上执行显式类型转换。

### **表达式中的显式类型转换**

当你对[表达式求值时，](https://www.edureka.co/blog/java-regex/)输出会自动更新为操作数的较大数据类型。但是，如果将结果存储在任何较小数据类型中，就会产生编译时错误，因此我们需要对输出进行类型转换。

**举例:**

```
//Java program to illustrate type casting int to byte
public class ExplicitTest {
public static void main(String args[])
{
byte b = 70;

//type casting int to byte
b = (byte)(b * 2);
System.out.println(b);
}
}
```

**输出:**

`140`

**注意:** *在单操作数的情况下，结果被转换成 int，然后相应地进行类型转换。*

这就是 Java 中显式类型转换的全部内容。说到这里，我们来结束这篇文章。我 希望你发现它内容丰富。如果你想了解更多，你也可以看看我们的 **[其他 Java 博客](https://www.edureka.co/blog/what-is-java/) [s](https://www.edureka.co/blog/java-tutorial/)** 。

*查看 Edureka 提供的 **[Java 认证培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“Java 中的类型转换”文章的评论部分提到它，我们会尽快回复您。