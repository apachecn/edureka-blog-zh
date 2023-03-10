# 如何在 java 中反转一个数？

> 原文：<https://www.edureka.co/blog/java-program-to-reverse-a-number/>

**[Java](https://www.edureka.co/blog/what-is-java/)** 是一种通用的编程语言，具有不同的应用。其主要原因是它在粒度级别提供的灵活性和易用性。这篇文章将帮助你编写 Java 程序来反转一个数字。本文将涉及以下几点:

*   [使用 While 循环](#UsingWhileLoop)
*   [使用 For 循环](#UsingAForLoop)
*   [使用递归](#UsingRecursion)

让我们开始吧，

## **Java 程序反转一个数字**

在 Java 中，可以用不同的方法反转数字，让我们来看看第一种方法，

## **使用 While 循环**

可以使用 while 循环来反转一组数字。这是节目单，

```
public class Main {
public static void main(String[] args){
int number=4321,reverse=0;
while(number!=0){
int dig=number%10;
reverse=reverse*10+dig;
number/=10;
}
System.out.println("Reversed Number: " + reverse);
}
}

```

**输出:**

反向编号:1234

**说明:**

*   本例中声明了一个整数。
*   该数除以 10，余数存储在变量 dig 中。
*   因此，数字的最后一位，即 1，存储在变量 dig 中。
*   变量 reverse 乘以 10(这在数字上增加了一个新的位置)，dig 被加到其中。这里，0*10+1=1。
*   然后这个数字除以 10，这样它就包含了前三个数字:432。
*   所有的数字都以同样的方式迭代。

让我们继续这篇“Java 程序反数”的文章，

## **使用 For 循环**

在下面的示例中，我们使用 for 循环，而不是 while 循环:

```
public class Main {
public static void main(String[] args) {
int number = 764321, reverse = 0;
for(;number != 0; number /= 10) {
int dig = number % 10;
reverse = reverse * 10 + dig;
}
System.out.println("Reversed Number: " + reverse);
}
}

```

必须注意的是，这里没有使用初始化表达式。

**输出:**

反向编号:1234567

这是本文的最后一部分，让我们看看递归是如何帮助我们的，

## **使用递归**

当一个方法不断地调用自己时，这个过程就叫做递归。

```
import java.util.Scanner;
class Main
{
//Reverse Method
public static void recurse(int number) {
if(number < 10) {
System.out.println(number);
return;
}
else{
System.out.print(number % 10);
//Method calling itself
recurse(number/10);
}
}
public static void main(String args[])
{
int num=987654321;
System.out.print("Reversed Number:");
recurse(num);
System.out.println();
}
}

```

**输出:**

反向号码:123456789

***这些方法提供了一种在 java 编程语言中反转数字的整体方法。***

这样我们就结束了这篇关于“Java 程序反数”的文章。如果你想了解更多，请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。