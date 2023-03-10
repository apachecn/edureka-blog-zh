# 关于 Java 中的帕斯卡三角形，你需要知道的一切

> 原文：<https://www.edureka.co/blog/pascal-triangle-in-java/>

在任何编程语言中创建数学模式都是最重要的概念之一。在 [Java](https://www.edureka.co/blog/java-tutorial/) 的情况下没有什么不同。在本文中，我们将了解如何在 Java 中实现不同类型的 Pascal 三角形。

*   [什么是帕斯卡三角形？](#what)
*   [Java 中不同形式的帕斯卡三角形](#different)

## **什么是帕斯卡三角形？**

一个*帕斯卡三角形*由存储在三角形数组中的二项式系数组成。这是任何编程语言中教授的经典和基本的例子之一。我们从用户那里得到一个输入 n，并打印出帕斯卡三角形的 n 条线。

**帕斯卡三角形的例子**

![Pascal triangle](img/673791175c01013e3012550e8d492990.png)

帕斯卡三角形是这样开始的:首先将数字 1 放在第一行，将两个 1 放在第二行。后面的行通过保持末端元素不变来钻孔，但是中间的元素是任一侧末端元素的总和。

考虑第四排。中间的两个词是由两边的 1 和 2 相加而成的，在两个 1 之间有两个 3。

**换句话说，每个数直接加到其他数上。**

## **Java 中不同形式的帕斯卡三角形**

**考虑代码**

**方法一:**

```
import java.util.Scanner;
public class PascalTri {
   static void printTriangle(int n)
    {

    for (int line = 0; line < n; line++)
    { 
        for (int i = 0; i <= line; i++)         System.out.print(findBinomial(line, i)+" ");                                   System.out.println();     }     }           static int findBinomial(int n, int j)     {         int result = 1;                   if (j > n - j)
        j = n - j;

        for (int i = 0; i < j; ++i)
        {
            result *= (n - i);
            result /= (i + 1);
        }
        return result;
    }

    public static void main(String args[])
    {
    int n;
    Scanner scn= new Scanner(System.in);
    System.out.println("enter the number of rows");
    n=scn.nextInt();
    printTriangle(n);
    }
}
```

**输出:**

## **![Output of Pascal Triangle in Jav](img/d55a7d309ca56034337451d18ffd687d.png)**

**解释**

在这段代码中，我们尝试用 java 打印一个帕斯卡三角形。声明了两个方法，一个方法打印三角形，第二个方法查找二项式系数。

```
static void printTriangle(int n)
    {

    for (int line = 0; line < n; line++)
    { 
        for (int i = 0; i <= line; i++)
        System.out.print(findBinomial(line, i)+" ");

        System.out.println();
    }
    }
```

我们有 printTriangle 函数，用来打印三角形。存在两个 for 循环。一个用于循环，另一个用于打印。调用 findBinomial 函数来查找术语。

findBinomial 用于查找帕斯卡三角形中的所有项。我们有一个 for 循环来执行计算。

该方法具有顺序 **O(n^3)** 的时间复杂度。

**方法二:**

```
import java.io.*;
import java.util.Scanner;
public class PascalTri {

            public static void printPascal(int n)
            {
                for(int line = 1; line <= n; line++)
                {

                int C=1;
                for(int i = 1; i <= line; i++)
                { 

                    System.out.print(C+" ");
                    C = C * (line - i) / i; 
                }
                System.out.println();
                }
              public static void main (String[] args) {
                int n = 5;
                printPascal(n);
            } 
            }
```

**输出:**

**![Pascal Triangle in Java](img/24a25f70894c7ef728ca0d581866f308.png)**

这段代码运行的时间复杂度为 **O(n^2)** 。它类似于第一种方法，但要快得多。重复相同的过程。

至此，我们结束了这篇 Java 文章中的 Pascal 三角形。我希望你了解什么是帕斯卡三角形，以及在 Java 中实现帕斯卡三角形的不同方法。

*查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这个“Java 中的 Pascal 三角”博客的评论部分提到它，我们会尽快回复您。