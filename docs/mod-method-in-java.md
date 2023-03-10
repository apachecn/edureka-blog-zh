# Java 中的模数是什么，它是如何工作的？

> 原文：<https://www.edureka.co/blog/mod-method-in-java/>

我相信你对模数这个术语很熟悉。也是 C、C++、Java 或 Python 最常被问到的 *[面试问题](https://www.edureka.co/blog/interview-questions/)* 之一。在这篇文章中，我将通过 [*Java*](https://www.edureka.co/blog/what-is-java/) 向您重温模数的定义以及实现过程。

看看这篇文章的议程:

*   [Java 中什么是模数运算符？](#What_is_a_modulus_operator?)
*   [语法](#Syntax)
*   [Java 中模数的例子](#Example_of_Modulus_in_Java)

我们开始吧！

## **Java 中什么是模数运算符？**

模数运算符返回两个数相除后的余数。如果你有两个数，比如 X 和 Y，X 是被除数，Y 是除数，X mod Y 是 X 除以 Y 的余数。

让我让你们熟悉一下这个操作符的技术表示。

## **Java 中的模数:语法**

X%Y

其中 X 是被除数，Y 是除数。

这么简单，不是吗？

既然你已经熟悉了语法，我将在 Java 程序的 *[中使用它。](https://www.edureka.co/blog/java-programs/)*

## **Java 中的模数示例**

```
class ModulusOperator{
public static void main(String[] args){
int num1,num2,result;
num1=26;
num2=15;
System.out.println("num1=26; num2=15");
result=num1%num2;
System.out.println("The result after modulus operation is : "+result);
}
}

```

**输出:**

num 1 =26num 2 =15

模数运算后的结果是: 11

在这里，你可以看到在 Java 程序中实现这个概念是多么容易。

你也可以使用模数运算符来确定一个数是奇数还是偶数。让我们看看如何！

```
package com.nullbeans.basics; 
public class Main {
public static void main(String[] args) {
int userInput = 32232;
isEvenNumber(userInput);
}
public static boolean isEvenNumber(int userInput){
if(userInput%2 == 0){
System.out.println("Input is an even number");
return true;
}else {
System.out.println("Input is an odd number");
return false;
}
}
}

```

因此，您可以看到模数运算符可以在许多情况下使用。Java 中的这个*模数*也可以用来检查一个数是否是质数，或者计算余数总和的应用程序等等。

说到这里，我们来结束这篇关于 Java 中的*模数*的文章。我希望你们清楚分享的话题，我相信现在不会让你们有任何模糊不清。继续阅读，继续探索！

如果你刚刚开始，那么看看这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/aqHhpahguVY](https://www.youtube.com/embed/aqHhpahguVY)

*还可以查看 Edureka 的 **[Java 在线课程](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate Spring。加入我们在 Jalandhar的 [Java 培训](https://www.edureka.co/java-j2ee-training-course-jalandhar)*