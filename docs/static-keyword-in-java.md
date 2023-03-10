# Java 中的静态关键字是什么？

> 原文：<https://www.edureka.co/blog/static-keyword-in-java/>

在 [Java](https://www.edureka.co/blog/what-is-java/) 中，关键字是不能作为标识符的保留字。Java 中总共有 57 个关键字。其中之一就是“**静**”。在本文中，我将向您简要介绍 Java 中的 static keyword 如何适用于编程的各个方面。

本文涵盖以下主题:

*   [Java 中静态关键字介绍](#IntroductiontostatickeywordinJava)
*   [静态关键字的应用](#ApplicationsofStatickeyword)
    *   [静态块](#StaticBlock)
    *   [静态变量](#StaticVariable)
    *   [静态方法](#StaticMethod)
    *   [静态类](#StaticClasses)

## **Java 中静态关键字介绍**

在 Java 中，**静态关键字**主要用于内存管理。可以和[变量](https://www.edureka.co/blog/java-tutorial/#variables)，方法，块，嵌套[类](https://www.edureka.co/blog/java-tutorial/#obj)一起使用。它是一个关键字，用于共享给定类的相同变量或方法。基本上，static 用于一个常量变量或者一个对于类的每个[实例都相同的方法。类的 main 方法通常标记为 static。](https://www.edureka.co/blog/instance-variable-in-java/)

为了创建一个静态成员(块、变量、方法、嵌套类)，你需要在声明之前加上关键字  *static* 。当类的成员被声明为静态时，它可以在创建其类的对象之前被访问，并且没有任何对象引用。

在 Java 编程语言中，static 关键字是一个非访问修饰符，可用于以下用途:

*   [静态块](#StaticBlock)
*   [静态变量](#StaticVariable)
*   [静态方法](#StaticMethod)
*   [静态类](#StaticClasses)

让我们借助一个例子来深入了解每种方法的细节。

## **静态关键字的应用**

我们先来了解一下 [Java 编程语言中静态块是如何使用的。](https://www.edureka.co/blog/java-tutorial/)

### **静态块**

如果你需要计算来初始化你的  **静态变量**，你可以声明一个静态块，当类第一次被加载时，这个静态块被执行一次。看看下面的 Java 程序来理解静态块的用法。

```
// Java program to demonstrate the use of static blocks
import java.util.*;
public class BlockExample{
// static variable
static int j = 10;
static int n;

// static block
static {
System.out.println("Static block initialized.");
n = j * 8;
}

public static void main(String[] args)
{
System.out.println("Inside main method");
System.out.println("Value of j : "+j);
System.out.println("Value of n : "+n);
}
}
```

当您执行上述程序时，静态块被初始化并显示初始化变量的值。

**输出** :

```
Static block initialized
Inside main method
Value of j:10
Value of n : 80
```

现在您已经知道了静态块是如何工作的，让我们进一步看看什么是静态变量以及它是如何有帮助的。

### **静态变量**

当您将一个变量声明为静态变量时，就会创建该变量的一个副本，并在[类级别](https://www.edureka.co/blog/java-objects-and-classes/)的所有[对象](https://www.edureka.co/blog/java-tutorial/#obj)中进行分配。静态变量本质上是全局变量。基本上，该类的所有实例共享同一个静态变量。静态变量只能在类级别创建。

现在让我们借助一个例子来理解这一点。

```
// Java program demonstrate execution of static blocks and variables

import java.util.*;

public class VariableExample
{
// static variable
static int j = n();

// static block
static {
System.out.println("Inside the static block");
}

// static method
static int n() {
System.out.println("from n ");
return 20;
}

// static method(main !!)
public static void main(String[] args)
{
System.out.println("Value of j : "+j);
System.out.println("Inside main method");
}
}
```

当您执行上述程序时，它将按照上述程序中定义的顺序执行静态块和变量。

**输出:**

```
from n
Inside the static block
Value of j: 20
Inside main method
```

理解了这一点，让我们更深入地阅读这篇关于 Java 中的 Static keyword 的文章，并了解什么是静态方法和嵌套类。

### **静态方法**

当一个方法用*静态* 关键字声明时，它被称为静态方法。静态方法最常见的例子是*main()*方法。声明为静态的方法可能有以下限制:

*   它们只能直接调用其他静态方法。

*   他们可以直接访问静态数据。

现在让我们借助一个例子来理解静态方法

```
// java program to demonstrate restriction on static methods
public class StaticMethodExample
{
// static variable
static int j = 100;

// instance variable
int n = 200;

// static method
static void a()
{
a = 200;
System.out.println("Print from a");

// Cannot make a static reference to the non-static field b
n = 100; // compilation error

// Cannot make a static reference to the
// non-static method a2() from the type Test
a2(); // compilation error

// Cannot use super in a static context
System.out.println(super.j); // compiler error
}

// instance method
void a2()
{
System.out.println("Inside a2");
}

public static void main(String[] args)
{
// main method
}
}
```

在上面的例子中，您可以看到如何对静态方法施加限制，以及如何允许您在静态上下文中使用 super 关键字。那都是关于静态方法的。现在让我们看看什么是嵌套类。

### **静态类**

只有当一个类是嵌套类时，它才可以成为。嵌套的静态类不需要外部类的引用。在这种情况下，静态类不能访问外部类的非静态成员。让我们举个例子来理解它是如何工作的

```
public class NestedExample{
private static String str= "Edureka"
//Static class
static class MyNestedClass{
//non-static method
public void disp(){
System.out.println(str);
}
}
public static void main(String args[]){
NestedExample.MyNestedClass obj = new NestedExample.MyNestedClass();
obj.disp();

}
```

当您执行上面的代码时，您的输出看起来像:

`Edureka`

以上就是静态关键字在 Java 中的各种应用。就这样，我们到了这篇文章的结尾。我希望你发现它信息丰富。如果你想了解更多，你也可以看看我们的 **[其他 Java 博客](https://www.edureka.co/blog/what-is-java/) [s](https://www.edureka.co/blog/java-tutorial/)** 。如果您刚刚开始，那么请阅读这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

*查看 Edureka 提供的 **[Java 认证培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“Java 中的静态关键字”文章的评论部分提到它，我们会尽快回复您，或者您也可以参加在望加锡举办的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-makassar)