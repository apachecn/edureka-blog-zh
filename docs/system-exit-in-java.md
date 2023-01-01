# 如何在 Java 中退出一个函数？

> 原文：<https://www.edureka.co/blog/system-exit-in-java/>

Java 是一种很棒的编程语言，有很多应用。当[为这些应用程序中的一个编程](https://www.edureka.co/blog/java-programs/)时，你可能会在这个程序的某个接合点卡住。在这种情况下，人们会怎么做？在这一点上有出路吗？如果这些问题困扰着你，那你就来对地方了。您可以做的是，简单地使用 System.exit()方法来终止当前在系统上运行的 Java 虚拟机。在本文中，我将带您了解 Java 中的 exit 函数，并帮助您彻底理解它。

我们开始吧。

## 如何在 Java 中退出一个函数？

可以使用 java.lang.System.exit()方法退出函数。该方法终止当前运行的 [Java 虚拟机(JVM)](https://www.edureka.co/blog/java-virtual-machine/) 。它采用一个参数“状态码”，非零状态码表示异常终止。如果你使用的是 [Java 循环](https://www.edureka.co/blog/loops-in-java/)或 switch 语句，你可以使用 break 语句来中断/退出一个循环，而不是整个程序。

在本文中，让我们更深入地研究 Java exit()方法，并了解它是如何使用的。

## **什么是 System.exit()方法？**

System.exit()方法调用类运行时的 exit 方法。它通过终止 Java 虚拟机退出当前程序。正如方法名所定义的，exit()方法从不返回任何东西。

调用 System.exit(n)实际上相当于调用:

```
Runtime.getRuntime().exit(n)

```

System.exit 函数有状态代码，它说明了终止情况，例如:

*   **退出(0)** :表示*成功终止。*
*   **退出(1)** 或**退出(-1)** 或任何**非零值**–表示*未成功终止*。

现在，让我们看看 System.exit()方法中的参数和异常抛出。

**参数:**退出状态。

**异常:**抛出一个*安全异常*。

继续讨论 System.exit 方法()，让我们看看它的一些实际实现。

## **Java 系统 exit()方法示例**

```

package Edureka;

import java.io.*;
import java.util.*;

public class ExampleProgram{

public static void main(String[] args)
{
int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

for (int i = 0; i < arr.length; i++) { if (arr[i] >= 4)
{
System.out.println("Exit from the loop");

System.exit(0); // Terminates JVM
}
else
System.out.println("arr["+i+"] = " +
arr[i]);
}
System.out.println("End of the Program");
}
}

```

**输出:**arr[0]= 1arr[1]= 2arr[2]= 3 退出循环

**说明:**在上面的程序中，执行一遇到 System.exit()方法就停止或退出循环。它甚至不打印第二个打印语句，即“程序结束”。它只是在那里终止程序本身。

**例 2:**

```

package Edureka;

import java.io.*;
import java.util.*;

public class ExampleProgram{

public static void main(String[] args)
{
int a[]= {1,2,3,4,5,6,7,8,9,10};
for(int i=0;i<a.length;i++)
{
if(a[i]<=4)
{
System.out.println("array["+i+"]="+a[i]);
}
else
{
System.out.println("Exit from the loop");
System.exit(0); //Terminates jvm
}
}
}
}

```

**输出**:array[0]= 1array[1]= 2array[2]= 3array[3]= 4 退出循环

**解释:**在上面的程序中，它打印元素，直到条件为真。一旦条件为假，它就打印语句，程序终止。

这样，我们就结束了这篇关于“Java 中的出口函数”的文章。我希望你明白本教程中分享的内容。如果您想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)提供的 [Java 在线课程](https://www.edureka.co/java-j2ee-training-course)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate Spring。

如果你刚刚开始，那么看看这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

有问题吗？请在本博客“Java 中的退出函数”的评论部分提到它，我们会尽快回复您。