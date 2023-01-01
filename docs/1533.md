# java 中的 for 循环是什么，如何实现？

> 原文：<https://www.edureka.co/blog/java-for-loop>

在编程时，如果出现了这样一种情况，即您明确知道要在代码中迭代特定语句块多少次，那么就使用“for”循环。在本文中，让我们学习如何用 Java 编程语言实现 for 循环。

本文涵盖的主题如下:

*   [什么是 for 循环？](#Whatisforloop?)
*   [流程图](#Flowdiagram)
*   [语法](#Syntax)
*   [for 循环的例子](#Exampleofforloop)
*   [Java 嵌套 for 循环](#Javanestedforloop)
*   [嵌套 for 循环的 Java 示例](#ExampleofJavanestedforloop)
*   [金字塔示例:案例 1](#Pyramidexample:Case1)
*   [金字塔示例:案例 2](#Pyramidexample:Case2)

让我们开始吧！

## **什么是 for 循环？**

程序员通常使用[循环](https://www.edureka.co/blog/control-statements-in-java/#Loopingstatemenets)来执行一组语句。 ***对于*** 循环是在需要多次迭代[程序](https://www.edureka.co/blog/java-programs/)的一部分时使用的。它特别适用于迭代次数固定的情况！

为了更好地理解，让我给你一个图示吧！

## **流程图**

![For-In Loop - Swift Tutorial - Edureka](img/aee9595e112c3a9cea1b787f4eeb4b46.png)

这里，在初始化之后，扫描您在代码中指定的条件，如果条件为真，它将增加/减少(根据您的代码)值，并根据您指定的条件再次迭代代码。但是，如果你的条件为假，它将退出循环。

在这个理论解释之后，让我给你展示一下 ***对于*** 循环的语法！

**语法**

```

for (statement 1; statement 2; statement 3) {
// code block to be executed
}

```

语法非常简单。其内容如下: **语句 1:** 代码块执行前的条件 **语句 2:** 指定代码执行的条件 **语句 3:** 条件一旦代码被执行

为了使事情更清楚，让我们用 Java 代码实现上面解释的语法。

**for 循环的例子**

下面写的代码描述了如何用 Java 语言[实现 for 循环](https://www.edureka.co/blog/what-is-java/)

```
public class MyClass {
{
public static void main(String[] args) {
{for (int i = 0; i < 5; i++) {
System.out.println(i);
}
}
}}

```

**输出:**01234

我用了一个简单的代码来让你们熟悉 for 循环的概念。在 for 循环中，有三个语句，我在上一节已经讲过了。我希望你现在能很容易地理解它们！

*   首先，Int i=0，是一个整型变量的初始化，它的值被赋值为 0。
*   其次，i<5 是我在代码中应用的条件
*   第三，i++意味着我希望变量的值递增。

了解了 for 循环的工作原理后，让我带你去了解另一个概念，那就是 Java 嵌套的 ***for*** 循环！

## **Java 嵌套 for 循环**

如果在 for 循环中有一个 for 循环，那么就遇到了一个嵌套的 Java for 循环。当外循环执行时，内循环完全执行。

我将通过一个例子向你展示 Java 嵌套 for 循环的工作原理。

## **例子**

嵌套 for 循环的 Java 代码:

```
public class Example{
public static void main(String[] args) {
for(int i=1;i<=3;i++){
for(int j=1;j<=3;j++){
System.out.println(i+" "+j);
}
}
}
}
```

**输出:**1 11 21 32 12 22 33 13 23 3

现在你已经理解了嵌套 for 循环的概念，让我给你看一个你可能听说过的非常著名的例子！金字塔的例子！

## **金字塔示例:案例 1**

```
public class PyramidExample {
public static void main(String[] args) {
for(int i=1;i<=5;i++){
for(int j=1;j<=i;j++){
System.out.print("* ");
}
System.out.println();//new line
}
}
}

```

**输出:**

** ** * ** * ** * * * * *

继续下一个例子。

## **金字塔示例:案例 2**

```
package MyPackage;
public class Demo {
public static void main(String[] args) {
int term=6;
for(int i=1;i<=term;i++){ for(int j=term;j>=i;j--){
System.out.print("* ");
}
System.out.println();//new line
}
}
}
```

**输出:**

* * ** * ** * ** **

我相信您会熟悉这两种模式。

“Java 中的 For 循环”这篇文章到此结束。我希望你现在已经清楚“Java 中 for 循环”的概念了。我们将继续一起挖掘 Java 世界。敬请期待！

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这篇“Java Map interface”**文章的评论部分提到它，我们会尽快回复您。*