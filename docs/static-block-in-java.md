# 如何用 Java 实现静态块？

> 原文：<https://www.edureka.co/blog/static-block-in-java/>

本文将介绍另一个有趣的话题，即 [Java](https://www.edureka.co/blog/java-tutorial/) 中的静态块，并以编程方式进行解释。本文将涉及以下几点:

*   [语法](#Syntax)
*   [静态块的例子](#ExampleofaStaticBlock)
*   [在构造函数](#ExampleExecutedbeforeConstructors)之前执行的例子
*   [多个静态块的例子](#ExampleofMultipleStaticBlocks)

Java 为用户提供了一个称为静态块的块，主要用于类的静态初始化。该块由一组在执行 main 方法之前执行的语句组成。这是因为类在使用之前必须加载到主存中，而静态块是在类的加载过程中执行的。在一个程序中定义许多静态块时，这些块从上到下执行。

继续这篇关于 Java 中静态块的文章

**语法:**

```
static
{
........
//Statements
........
}

```

继续这篇关于 Java 中静态块的文章

**静态块的例子**

```
class Static {
static int p;
int q;
// creating the static block
static {
p = 18;
System.out.println("This is the static block!");
}
// end of static block
}
public class Main {
public static void main(String args[]) {
// Accessing p without creating an object
System.out.println(Static.p);
}
}

```

**输出:** 这是静态块！ 18

必须注意，静态块在构造函数之前执行，如下例所示:

```
class Stat {
static int p;
int q;
static {
p = 18;
System.out.println("This is a static block!");
}
Stat(){
System.out.println("Constructor!");
}
}
public class Main {
public static void main(String args[]) {
// Even though we have two objects, static block is executed only once.
Stat s1 = new Stat();
Stat s2 = new Stat();
}
}

```

**输出:**

这是一个静态块！建造师！建造师！

继续这篇关于 Java 中静态块的文章

**多个静态块的例子**

我们也可以在一个程序中定义多个静态块:

```
public class Stat
{
static
{
System.out.println("This is the first static block!");
}
static
{
System.out.println("This is the second static block!");
}
public static void main(String args[])
{
System.out.println("Main!");
}
}

```

**输出:**

这是第一个静态块！这是第二个静态块！主！

这些方法为用户提供了使用静态块的有效方式。

这样，我们就结束了这篇关于“Java 中的静态块”的文章。如果你想了解更多，可以去看看 Edureka 值得信赖的在线学习公司提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。