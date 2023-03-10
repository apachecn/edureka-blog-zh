# 如何用 Java 实现完全数？

> 原文：<https://www.edureka.co/blog/perfect-number-program-in-java/>

如果一个数的除数之和等于该数，则称该数为完全数。听起来很有趣，不是吗？在本文中，让我们看看如何在 java 中实现一个完美的数字。

本文的议程如下:

*   [Java 里什么是完全数？](#WhatisaperfectnumberinJava?)
*   [时间复杂度](#Timecomplexity)
*   [Java 程序实现一个完全数](#Javaprogramtoimplementperfectnumber)

让我们开始吧！

## **Java 里什么是完全数？**

简单来说，完全数等于它的真约数之和，不包括这个数本身。让我举一个例子来帮助你更好地理解它。我们来考虑几个例子: **例 1:** 6 积极因素有；1，2，3，6 在这里，除去数字本身的所有因子之和等于 6。 **例 2:** 28 积极因素有；1，2，4，7，14，28 再一次，不包括数字本身的所有因素的总和是 28。

既然你已经清楚了完全数的含义，让我们进入下一部分。

## **时间复杂度**

完全数的时间复杂度是√n。

现在让我们看看一个完全数在 Java 中的实现过程。

## **Java 程序实现一个完全数**

**代码**:

```
import java.util.Scanner;
public class Perfect
{
public static void main(String[] args) 
{
int n, sum = 0;
Scanner s = new Scanner(System.in);
System.out.print("Enter an integer:");
n = s.nextInt();
for(int i = 1; i &lt; n; i++)
{
if(n % i == 0)
{
sum = sum + i;
}
}
if(sum == n)
{
System.out.println("The number is Perfect");
}
else
{
System.out.println("The number is not Perfect");
}    
}
int divisor(int x)
{
return x;
}
}

```

**输出:**

```
Enter an integer: 46
The number is not Perfect

```

这篇“Java 中的完美数字”文章到此结束。我已经介绍了 Java 最基本也是最重要的主题之一。 希望你清楚本文与你分享的一切。

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 提供的 [**Java 课程**](https://www.edureka.co/java-j2ee-training-course) 培训，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这篇* *文章的评论部分提到它，我们会尽快回复你。*