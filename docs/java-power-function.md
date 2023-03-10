# Java 中的幂函数是什么？–了解其用途

> 原文：<https://www.edureka.co/blog/java-power-function/>

Java 中的幂函数用于计算一个数的其他幂。该函数接受两个参数，并返回第一个参数的值乘以第二个参数的值。在这篇文章中，我将告诉你一个幂函数的用法。

本文涵盖以下主题:

*   [Java 中的幂函数介绍](#IntroductiontoPowerfunctioninJava)
*   [幂函数示例](#ExamplesofPowerfunction)

我们开始吧！

## **Java 中的幂函数介绍**

[Java](https://www.edureka.co/blog/advanced-java-tutorial) 中的![Java Pow() - Power Function in Java - Edureka](img/f91ed0af776cf98cb1b54b35f87faf55.png) Power 函数属于类型 *java.lang.Math.pow()* 库。它主要用于返回第一个参数的值乘以第二个参数的幂。它的工作原理类似于我们在数学中使用的指数。

**语法:**

```
***double pow(double base, double exponent)*** 
```

*   **base**—任何原始数据类型。
*   **指数**—任何原始数据类型

**返回:**该方法返回*基数<sup>指数</sup>T5。*

*   如果第二个参数为正  **零**或负 **1.0** 。
*   如果第二个参数不是数字  **(NaN)** ，该方法将返回  **NaN** 。
*   如果第二个参数是  **1** ，该方法将返回与第一个参数**相同的结果。**

至此，现在让我们进一步借助下面的例子来看看使用 pow()的各种方法。

## **幂函数示例**

**例 1:** 演示 java.lang.Math.pow()方法的工作原理。

```
import java.lang.Math;
public class Example1 {
public static void main(String args[]) {
double x = 60;
double y = 3;
System.out.println(Math.pow(x, y));
x = 3;
y = 4;
System.out.println(Math.pow(x, y));
x = 2;
y = 5;
System.out.println(Math.pow(x, y));
}
}
```

**输出:**

216000 81 32

**例 2:**

```
public class Example2 {
public static void main(String[] args) {
double a = 18.0;
double b = -3;
//return (18) power of -3
System.out.println(Math.pow(a, b));
}
}
```

**输出:**

1 . 33 e-4。56660.66666666661

**例 3:**

```
public class Example3 {
public static void main(String[] args) {
double a = -107;
double b = 0.6;
//returns NaN
System.out.println(Math.pow(a, b));
}
}
```

**输出:**

圆盘烤饼

至此，我们结束了这篇关于 [Java](https://www.edureka.co/blog/what-is-java/) 中的幂函数的文章。我希望您发现它内容丰富，并理解 pow()方法的各种用法。如果你想深入学习 [Java](https://docs.oracle.com/javase/tutorial/) 的基础知识，请查看 Java 上的 **[其他博客。](https://www.edureka.co/blog/java-tutorial/)**

*查看 Edureka 的 [**Java 在线课程**](https://www.edureka.co/java-j2ee-training-course) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题吗？请在这篇“Java 中的幂函数”文章的评论部分提到它，我们会尽快回复您。