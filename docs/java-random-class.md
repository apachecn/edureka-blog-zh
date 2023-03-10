# 如何在 Java 中使用 Random 类生成随机数？

> 原文：<https://www.edureka.co/blog/java-random-class/>

Java 随机类的目标是产生一个伪随机数流。Java 中的 Random 类生成不同[数据类型](https://www.edureka.co/blog/data-types-in-java/)的随机数，如 int、float、long、boolean 和 double。让我们再深入一点，详细理解这个概念。

下面提到的指针将是本文讨论的主题:

*   [什么是 Java 中的随机类？](#WhatisaRandomclassinJava?)
*   [Java 随机类中使用的构造函数](#ConstructorsusedinaJavaRandomclass)
*   [Java 随机类中使用的方法](#MethodsusedinaJavaRandomclass)
*   [Java 程序来表示随机类的用法](#Javaprogramtorepresenttheusageofrandomclass)

我们要开始了！

## **什么是 Java 中的随机类？**

在 [Java](https://www.edureka.co/blog/java-tutorial/) 中，随机类是 *java.util 包的一部分。*随机数的生成通过使用 *Java Random 类*的一个实例来实现。这个[类](https://www.edureka.co/blog/java-objects-and-classes/#javaclass)提供了不同的方法来产生整数、双精度、长整型、浮点型等类型的随机数。

## **Java 随机类中使用的构造函数**

这个类包含下面提到的两个[构造函数](https://www.edureka.co/blog/constructor-in-java/):

*   这个构造函数帮助创建一个新的随机生成器
*   **Random(long seed):** 这个构造函数使用指定的种子帮助创建一个新的随机生成器

***注:**每当随机数生成过程发生时，就考虑种子值。如果没有提供种子值，它将从系统 nano time 中创建。如果两个随机实例拥有相同的种子值，将生成相同的随机数序列。*

现在，让我们看看一个方法是如何在一个随机类中使用的。

## **Java 随机类中使用的方法**

一些重要的方法是:

| **方法** | **功能** |
| nextDouble() | 返回下一个伪随机数，它是一个介于 0.0 和 1.0 之间的双精度值。 |
| nextBoolean() | 返回下一个伪随机序列，它是随机数生成器序列中的一个布尔值 |
| nextFloat() | 返回下一个伪随机序列，它是一个介于 0.0 到 1.0 之间的浮点值 |
| nextInt() | 返回下一个伪随机序列，它是随机数生成器序列中的一个整数值 |
| 下一个整数 | 返回下一个伪随机序列，它是一个介于 0 和随机数生成器序列中的指定值之间的整数值 |
| nextbytes(位元组[]位元组) | 生成随机字节，并将它们放入用户提供的字节数组中 |
| 长整型() | 返回伪随机长值的无限流 |
| nextGaussian() | 帮助从该随机数生成器的序列中返回下一个伪随机、高斯(精确)分布双精度值，平均值为 0.0，标准偏差为 1.0 |

还有其他继承自 *java.lang.object* 的方法，比如:notify、notifyAll、wait、toString、finalise、equals、clone、getClass 和 hashCode。

让我们向前看，看看 java 随机类是如何在 Java 程序中实现的。

## **Java 程序来表示随机类的用法**

这里有一个基本的例子来帮助你理解这个概念。

```
package MyPackage;
import java.util.Random;

public class JavaRandomExample {
	public static void main(String[] args) {
		//create random object
		Random random= new Random();
		//returns unlimited stream of pseudorandom long values
		System.out.println("Longs value : "+random.longs());
		// Returns the next pseudorandom boolean value
		boolean val = random.nextBoolean();
		System.out.println("Random boolean value : "+val);
		byte[] bytes = new byte[10];
		//generates random bytes and put them in an array
		random.nextBytes(bytes);
		System.out.print("Random bytes = ( ");
		for(int i = 0;i<bytes.length; i++)
		{
		System.out.printf("%d ", bytes[i]);
		}
		System.out.print(")");
		}

}

```

**输出:**

![Output - Random Class in Java - Edureka](img/05fda1bb6d0c98ce8c331012efdd3622.png)

这就把我们带到了这篇关于 Java 中的[随机类的文章的结尾。希望以上讲解的内容能为你的](https://docs.oracle.com/javase/8/docs/api/java/util/Random.html) [Java 知识](https://www.edureka.co/blog/what-is-java/)增值。我们将继续探索 Java 世界。敬请期待！

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这篇* *文章的评论部分提到它，我们会尽快回复你。*