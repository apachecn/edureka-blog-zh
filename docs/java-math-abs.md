# 关于 Java 数学 abs()你需要知道的一切

> 原文：<https://www.edureka.co/blog/java-math-abs/>

本文将向您介绍 [Java](https://www.edureka.co/blog/java-tutorial/) Math Abs()方法，并在此过程中告诉您如何生成一个参数的绝对值。本文将涉及以下几点:

*   [Java Math abs()](#JavaMathabs())
*   [ABS()](#Examplesofabs())的例子

让我们开始吧！！

## **Java 数学** abs( **)**

*   由于我们不能在应用程序或数据中硬编码所有的对数和三角函数表，Java 提供了 Math——一个非常有用的类。
*   Math 是 java.lang 的最终类，使用静态方法执行指数、对数、根和三角方程等运算
*   数学中两个最基本的元素是 e 和 pi。在上述计算/运算中经常需要这两个常数
*   “e”(自然对数的底数)和“pi”(圆的周长与直径之比)作为具有以下值的双精度字段提供
*   数学。e–2。56860 . 88888888861
*   数学。圆周率–3。38860 . 38638686861
*   abs()方法用于计算自变量的绝对(正)值，其中自变量可以是 int、long、double 和 float

以下是数学类中重载的 abs 方法

*   公共静态 int abs(int a)
*   公共静态双 abs(双 b)
*   公共静态浮动 abs(浮动 c)
*   公共静态长 abs(长 d)

a，b，c 或 d 可以是负值，而返回将是正值，但如果参数是整数。MIN_VALUE 或 Long。MIN_VALUE，最负的可表示 int 值或 long 值，结果是相同的值，即负值。上述方法可以将 infinity 和 NaN 作为参数，并分别返回相同的值

继续这篇关于 Java 数学 abs()的文章

—

继续这篇关于 Java 数学 abs()的文章

```
int
```

```
public class Example1{
public static void main(String args[]){
int a = 56;
int b = -47;
//printing absolute value of int and Integer.MIN_VALUE
System.out.println(Math.abs(a));
System.out.println(Math.abs(b));
System.out.println(Math.abs(Integer.MIN_VALUE));
}
}

```

**输出****t**–5647-2147483648

继续这篇关于 Java 数学 abs()的文章

**double—**

```
public class Example2
{
public static void main(String args[])
{
double x = -27.64;
double y = -394.27;
//printing absolute value of double type
System.out.println(Math.abs(x));
System.out.println(Math.abs(y));
System.out.println(Math.abs(7.0 / 0)); //infinity
}
}

```

```
Output –
27.64
394.27
Infinity

Moving on with this article on Java Math abs()

float- 

```

```
public class Example3
{
public static void main(String args[])
{
float x = -63.02f;
float y = -438.0f;
//printing absolute value of float type
System.out.println(Math.abs(x));
System.out.println(Math.abs(y));
}
}

```

**输出****t**–63.02438.0

继续这篇关于 Java 数学 abs()的文章

**龙-**

```
public class Example4
{
public static void main(String args[])
{
long x = 78730363;
long y = -4839233;
//printing absolute value of long type
System.out.println(Math.abs(x));
System.out.println(Math.abs(y));
System.out.println(Math.abs(Long.MIN_VALUE));
}
}

```

**输出****t**–787303634839233-9223372036854775808

现在，在执行了上面的程序之后，您应该已经理解了 Java Math abs()方法。这样我们就结束了这篇文章。如果你想了解更多，请查看由 Edureka 提供的  [Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。](https://www.edureka.co/java-j2ee-training-course)

有问题吗？请在这篇文章的评论部分提到它，我们会尽快回复你。