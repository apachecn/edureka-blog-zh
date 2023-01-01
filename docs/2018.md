# Java 中如何求一个数组中最大的数？

> 原文：<https://www.edureka.co/blog/java-program-find-largest-number-array/>

**Java 程序寻找数组中最大的数**

在本教程中，我将帮助你构建一个 [Java 代码](https://www.edureka.co/blog/java-tutorial/)，通过它你可以找出一个数组中的最大数。在您输入数组的数字作为输入之后，程序将开始相互比较这些数字并得出结论。要讨论的要点如下:

*   [如何在 Java 中找到数组中的最大数](#HowtofindthelargestnumberinanarrayinJava)
*   [Java 程序寻找数组中最大的数字](#javaprogram)

让我们看看这是怎么做到的！

## 如何在 Java 中找到数组中最大的数？

很简单。你需要在程序开始时声明一个数组。程序将使用 for 循环扫描代码，并从最初声明的数组中得出结果(最大的数字)。请参考下面的 coed 片段:

```

arr[]= {5, 45,20,80,4,160,90,86}

```

**输出:160**

## **Java 程序寻找数组中最大的数字**

**代码:**

```

public class Example
{
public static void main(String[] args)
{
int n, max;
Scanner s = new Scanner(System.in);
System.out.print("Enter the number of elements in the array:");
n = s.nextInt();
int a[] = new int[n];
System.out.println("Enter the elements of array:");
for(int i = 0; i < n; i++)
{
a[i] = s.nextInt();
}
max = a[0];
for(int i = 0; i < n; i++)
{
if(max < a[i])
{
max = a[i];
}
}
System.out.println("Maximum value in the array is:"+max);
}
}

```

**输出:** 输入数组中的元素个数:5 输入数组中的元素个数: 10 4 8 1 3 数组中的最大值为:10

**代码 2**

继续采用更简单的方法。

```

class LargestNumber
{
public static void main(String args[])
{
int[] a = new int[] { 22, 3, 550, 4, 11, 100};
int max = a[0];
for(int i = 1; i < a.length;i++) { if(a[i] > max)
{
max = a[i];
}
}

System.out.println("The Given Array is:");
for(int i = 0; i < a.length;i++)
{
System.out.println(a[i]);
}

System.out.println("The Largest Number is:" + max);
}
}

```

**输出:** 给定数组为:223550411100 最大数为:550

在这个例子中，我们使用了 for 循环来达到我们的目的。希望你现在已经明白用法了！

这就是我们如何通过 [Java 代码](https://www.edureka.co/blog/java-tutorial/)完成我们的目标。我希望你清楚这个概念。继续阅读，继续探索！

如果你刚刚开始，那么看看这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

*现在您已经了解了 Java 的基础知识，请查看 Edureka 提供的  [**Java 在线课程**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & [Spring](https://spring.io/) 。*

有问题要问我们吗？请在“Java 程序寻找数组中最大的数”博客的评论部分提到它，我们会尽快回复您。