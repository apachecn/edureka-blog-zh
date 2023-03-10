# Java 中如何求数字的和？

> 原文：<https://www.edureka.co/blog/java-program-for-sum-of-digits/>

Java 是一种通用的编程语言。在 Java 中，有各种各样的方法可以用来计算数字的和。让我们详细讨论这些方法。下面给出了一个列表，我们可以用它来解决我们的问题。

*   [通过使用 for 循环](#Byusingforloop)
*   [通过使用静态方法](#Byusingstaticmethod)
*   [通过使用递归](#Byusingrecursion)
*   [通过使用命令行参数](#Byusingcommandlinearguments)

让我们开始吧！

## **通过使用 for 循环**

程序员通常使用 [循环](https://www.edureka.co/blog/control-statements-in-java/#Loopingstatemenets) 来执行一组语句。 ***For*** 循环用于需要多次迭代 [程序的一部分](https://www.edureka.co/blog/java-programs/) 时。它特别适用于迭代次数固定的情况！

**代码:**

```

class SumOfDigits
{
public static void main(String arg[])
{
long n,sum;
Scanner sc=new Scanner(System.in);
System.out.println("Enter a number ");
n=sc.nextLong();
for(sum=0 ;n!=0 ;n/=10)
{
sum+=n%10;
}
System.out.println("Sum of digits "+sum);
}
}

```

**输出:** 输入一个数字 456 位数总和 15

下一部分告诉你如何用静态方法来完成目标。

## **通过使用静态方法**

在 Java 中，[静态方法](https://www.edureka.co/blog/java-static-method/)是属于一个类的方法，而不是一个类的实例。一个[类](https://www.edureka.co/blog/java-objects-and-classes/)的每个实例都可以访问该方法，但是在一个实例中定义的方法只能被该类成员访问。

**代码:**

```

class SumOfDigits
{
public static void main(String arg[])
{
long n,s;
Scanner sc=new Scanner(System.in);
System.out.println("Enter a number ");
n=sc.nextLong();
s=sum(n);
System.out.println("Sum of digits "+s);
}
static int sum(long num)
{
int sum=0;
while(num!=0)
{
sum+=num%10;
num/=10;
}
return sum;
}
}

```

**输出:** 输入一个数字 678 位数总和 21

现在让我们转向另一种方法，那就是递归。

## **通过使用递归**

**代码:**

```

import java.util.Scanner;
class SumOfDigits

{
int sum=0;
int sum(long num)
{

if(num!=0)
{
sum+=num%10;
num/=10;
sum(num);
}
return sum;
}

public static void main(String arg[])
{
long n,res;
SumOfDigits s=new SumOfDigits();
Scanner sc=new Scanner(System.in);
System.out.println("Enter a number ");
n=sc.nextLong();

System.out.println("Sum of digits "+s.sum(n));

}
}

```

**输出:** 输入一个数字 345 位数总和 12

最后，我们将使用命令行参数来计算一个数字的位数之和。

## **通过使用命令行参数**

**代码:**

```

class SumOfDigits
{
public static void main(String arg[])
{
long n,sum=0;
System.out.println("Enter a number ");
n=Long.parseLong(arg[0]);
while(n!=0)
{
sum+=n%10;
n/=10;
}
System.out.println("Sum of digits &ldquo; +sum);

}
}

```

**输出:** 输入一个数字 123 数字总和 6

至此，我们已经接近本教程“Java 中数字总和”的尾声。希望对你有所帮助。继续阅读，继续探索！我们将继续一起挖掘 Java 世界。敬请期待！

***确保你尽可能多的练习，恢复你的经验。***

*这就把我们的博客“Java 程序在 Java 中寻找数字和”带到了最后。我希望你发现这个博客信息丰富，增加了你的知识价值。* *查看 Edureka 提供的 [**Java 认证培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & [Spring](https://spring.io/) 。*

*有问题吗？请在这篇“Java 中的数字总和”* *文章的评论部分提到它，我们会尽快回复您。*