# Java 中的 Scanner 类是什么？

> 原文：<https://www.edureka.co/blog/scanner-class-in-java/>

如果您正在编写一个 [Java 程序](https://www.edureka.co/blog/java-programs/)并希望读取用户的输入，您可以使用 [Java](https://www.edureka.co/blog/java-tutorial/) 中的 Scanner 类。在本文中，我将向您简要介绍 Scanner 类及其各种方法。在这篇文章中，我将涉及以下主题:

*   [什么是扫描仪类？](#WhatistheScannerClass?)
*   [扫描仪类的方法](#MethodsofScannerClass)
*   [例题](#Examples)

## **什么是扫描仪类？**

Scanner 类主要用于获取用户输入，它属于 java.util 包。为了使用 Scanner 类，您可以创建该类的对象，并使用任何 Scanner 类方法。在下面的例子中，我使用了 *nextLine()* 方法，该方法用于读取[字符串](https://www.edureka.co/blog/cheatsheets/java-string-cheat-sheet/)。

```
import java.util.Scanner;// Import the Scanner class

public class Example {
public static void main(String[] args) {
Scanner s = new Scanner(System.in);// Create a Scanner object
System.out.println("Enter username");

String name = s.nextLine();// Read user input
System.out.println("name is: " + name);;// Output user input
}
}
```

这就是你如何在 Java 中使用 Scanner 类。现在让我们进一步看看 Scanner 类的各种方法。

## **扫描仪类方法**

Scanner 类有各种方法可用于各种[数据类型](https://www.edureka.co/blog/data-types-in-java/)，看看下表就知道这些[方法](https://www.edureka.co/blog/java-methods/)。

| 方法 | 描述 |
| nextBoolean() | 从用户处读取一个布尔值 |
| 下一字节() | 从用户处读取一个字节值 |
| nextDouble() | 从用户处读取一个双精度值 |
| nextFloat() | 从用户处读取一个浮点值 |
| nextInt() | 从用户处读取一个 int 值 |
| nextLine() | 从用户处读取字符串值 |
| nextLong() | 从用户处读取一个长值 |
| nextShort() | 从用户处读取一个短值 |

现在我们举个例子来演示一下上面的方法。

## **例题**

```
import java.util.Scanner;

public class Example {
public static void main(String[] args) {
Scanner s = new Scanner(System.in);

System.out.println("Enter name, age and salary");

// String input
String name = s.nextLine();

// Numerical input
int age = s.nextInt();
double salary = s.nextDouble();

// Output input by user
System.out.println("Name: "+ name);
System.out.println("Age: "+ age);
System.out.println("Salary: "+ salary);
}
}
```

当您运行上述代码时，它会要求您输入姓名、年龄和工资等详细信息。它将显示输出。这就是 Java 中的扫描器类。说到这里，我们来结束这篇文章。我 希望你发现它内容丰富。如果你想了解更多，你也可以看看我们的 **[其他 Java 博客](https://www.edureka.co/blog/what-is-java/) [s](https://www.edureka.co/blog/java-tutorial/)** 。

*查看 Edureka 提供的 **[Java 认证培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“Java 中的 Scanner 类”文章的评论部分提到它，我们会尽快回复您。