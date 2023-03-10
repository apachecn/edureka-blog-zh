# Java 中的错误介绍

> 原文：<https://www.edureka.co/blog/introduction-to-errors-in-java/>

[//www.youtube.com/embed/N4YwDM_zDX0](//www.youtube.com/embed/N4YwDM_zDX0)

## **Java 中的错误**

**![Java Logo - Edureka](img/782786b3664a3479e7f4d29ad0cc4a11.png)设计时错误**–这些是设计程序时出现的错误，例如语法错误。

这些错误将在 eclipse IDE 中用一个红色标记显示出来，这样人们可以很容易地找到并纠正它们。

让我们看一个示例程序:

包 com . edu reka . error . design error；

公共类设计错误{

公共**静态**无效**主** (String[] args) {

System.out.printIn("这是设计时错误")；

；

}

}

这里，在 main 方法中，如果 t he m in Main i s capital，它会给出一个错误，如果 static 关键字的 s 是 capital，它也会这样做。

此外，在 print 语句的末尾和下面还放置了一个分号。

**逻辑错误**——这些是程序员犯的错误。出现这些错误的程序会运行，但不会产生预期的结果。一个常见的例子是将两个数相除作为输出，但期望的是两个数相乘。

在这里，如果语法是正确的，但逻辑是错误的，那么这是一个逻辑错误，这将反过来给出错误的结果。这通常发生在用户不知道逻辑的复杂程序中。

示例:

一个程序有打印数字 1 到 5 的指令，但是打印 6。

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[Hadoop&Java 专业人士的大数据](https://www.edureka.co/blog/videos/free-webinar-on-hadoop-for-java-professionals/)

[JAVA/J2EE & SOA 课程](https://www.edureka.co/java-j2ee-soa-training)