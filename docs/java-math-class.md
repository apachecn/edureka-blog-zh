# Java 中的数学类是什么，怎么用？

> 原文：<https://www.edureka.co/blog/java-math-class/>

**[Java](https://www.edureka.co/java-j2ee-soa-training)Java 中的数学类**包含了某些执行不同数值运算的方法，例如，*指数、* s *平方根、对数、三角函数*等。让我们深入挖掘，详细理解这个概念。

*   [什么是 Java 数学课？](#WhatisJavamathclass?)
*   [Java 数学方法有哪些？](#WhataretheJavamathmethods?)
*   [对数数学方法](#Logarithmicmathmethods)
*   [三角数学方法](#Trigonometricmathmethods)
*   [角度数学方法](#Angularmathmethods%20)
*   [双曲线数学方法](#Hyperbolicmathmethods)
*   [字母开头解释 Java 数学课](#LetterstartwithexplanationofJavamathclass)

让我们开始吧！

## **什么是 Java 数学课？**

为了在 [**Java**](https://www.edureka.co/blog/java-tutorial/) 中执行不同的数值计算，math class 提供了几种方法，您将进一步学习。一些方法有 min()、max()、avg()、sin()、cos()等。

现在让我们仔细研究一下这些方法。

## **Java 数学方法有哪些？**

下面的列表描述了 Java math class 提供的几种方法:

**Math.min():** 该方法返回两个值中最小的。 **Math.max():** 此方法返回两个值 **中最大的**math . ABS():**此方法返回所提供值的**绝对值**值。 **Math.round():** 该方法用于将**的小数四舍五入到最接近的数值。 **Math.sqrt():** 该方法返回给定数字的**平方根**。 **Math.cbrt():** 该方法返回给定数字的**立方根**。 **Math.floor():** 该方法用于求小于或等于自变量且等于一个数学整数的双精度值的**最大整数**值。 **Math.pow():** 该方法返回所提供的**第一个参数**的[幂第二个参数](https://www.edureka.co/blog/java-power-function/)的值。 **Math.ceil():** list 方法用于查找大于或等于自变量的**最小整数**值。 **Math.floorDiv():** 此方法用于找出小于或等于商的**最大整数**值。 **Math.random():** 这个 java [random](https://www.edureka.co/blog/java-random-class/) 方法返回一个 **double** 值，该值带有一个大于等于 0.0 且小于 1.0 的正号 **Math.rint():** 该方法返回最接近给定参数的 **double** 值。 **Math.ulp():** 该方法返回参数的 **ULP** 的大小。 **Math.addExact():** 该方法用于返回其参数的总和，如果结果溢出一个整数或长值，则抛出一个**异常**。**math . subtract exact():**该方法返回所提供参数的差值，如果结果溢出并且是一个整数值，则抛出**异常**。**math . multiplyexact():**该方法返回参数的乘积，如果结果溢出并且是整数或长值，则抛出**异常**。**math . increment exact():**该方法返回递增 1 的参数，如果结果溢出并为整数值，则抛出**异常**。**math . decrement exact():**该方法返回递减 1 的参数，如果结果溢出，则抛出**异常**。**math . negate exact():**该方法返回参数的取反，如果结果溢出并且是整数或长值，则抛出**异常**。****

这些是执行基本数字运算的几种方法。现在让我们向前看，理解对数数学方法的概念。

## **对数数学方法**

下面是解释这些方法的列表: **Math.log():** 此方法用于返回双精度值的**自然对数****math . log 10():**此方法用于返回双精度值的**以 10 为底**对数 **Math.exp():** 此方法返回 E **(欧拉值)**的双精度值幂。 **Math.log1p():** 该方法返回自变量和 1 之和的**自然对数**。 **Math.expm1():** 该方法计算欧拉的数的**次方，并从中减去 1。**

这些是一些对数数学方法，可以帮助你在使用 Java math class 时简化计算过程。

本教程的下一个主题是三角数学方法。

**三角数学方法**

下面提到的是这些方法的列表: **Math.sin():** 这个方法返回给定 double 值的**正弦值**。 **Math.asin():** 该方法返回给定 double 值的 **arc** **sin** 值 **Math.cos():** 该方法返回给定 double 值的 **cos 值**。 **Math.acos:** 该方法返回给定 double 值的圆弧**余弦值**。 **Math.tan():** 该方法返回给定 double 值的**正切值**。 **Math.atan():** 该方法返回给定 double 值的圆弧**正切值**。

下一部分由角度数学方法组成。

**角度数学方法**

下面解释两种角度数学方法: **Math.toRadians:** 该方法用于将指定的**度**角度转换为以**弧度测量的角度。** **Math.toDegrees:** 该方法用于将**弧度**角度转换为以**度为单位的等效角度。**

接下来我们有双曲线数学方法。

**双曲线数学方法**

这个段由下面提到的三个方法组成: **Math.sinh():** 这个方法用于返回一个 double 值的**三角双曲正弦值**。 **Math.cosh():** 此方法用于返回 double 值的**三角双曲余弦值**。 **Math.tanh():** 此方法用于返回双精度值的**三角双曲正切值**。

我希望双曲数学方法的概念现在对你已经很清楚了。

现在让我给你展示一个在 Java 程序中使用这些方法的例子:

**显示 Java 数学类方法用法的 Java 程序:**

```
public class JavaMathExample1{
      public static void main(String[] args){
          double x = 28;
          double y = 4;
          System.out.println("Maximum number of x and y is: " +Math.max(x, y));
          System.out.println("Square root of y is: " + Math.sqrt(y));
          System.out.println("Power of x and y is: " + Math.pow(x, y));
          System.out.println("Logarithm of x is: " + Math.log(x));
          System.out.println("Logarithm of y is: " + Math.log(y));
          System.out.println("log10 of x is: " + Math.log10(x));
          System.out.println("log10 of y is: " + Math.log10(y));
          System.out.println("log1p of x is: " +Math.log1p(x));
          System.out.println("exp of a is: " +Math.exp(x));
          System.out.println("expm1 of a is: " +Math.expm1(x));
      }
}

```

**输出:**

`Maximum number of x and y is: 28.0``Square root of y is: 2.0``Power of x and y is: 614656.0``Logarithm of x is: 3.332204510175204``Logarithm of y is: 1.3862943611198906``log10 of x is: 1.4471580313422192``log10 of y is: 0.6020599913279624``log1p of x is: 3.367295829986474``exp of a is: 1.446257064291475E12``expm1 of a is: 1.446257064290475E12`

至此，我们已经接近本教程的结尾。我希望这些内容解释了上述对您的 Java 知识的附加价值。我们将继续探索 Java 世界。敬请期待！

如果您发现与本文相关的任何疑问，请在下面的评论部分写下，我们将尽快回复您。

*既然您已经了解了 Java 的基础知识，请查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate&[Spring](https://spring.io/projects/spring-framework)。*