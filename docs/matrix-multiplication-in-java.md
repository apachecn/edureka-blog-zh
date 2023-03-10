# 如何用 Java 实现矩阵乘法？

> 原文：<https://www.edureka.co/blog/matrix-multiplication-in-java/>

本文将向您介绍一个非常常见的问题，如果解决了这个问题，将会简化许多任务。本文将讨论 Java 中的[矩阵乘法](https://www.edureka.co/community/30564/how-to-do-matrix-multiplication-in-python)。本文将讨论以下几点:

*   [Java 中的矩阵乘法](#MatrixMultiplicationInJava)
*   [使用 For 循环](#UsingForLoop)
*   [通过键盘](#SpecifyInputThroughKeyboard)指定输入

让我们从这篇文章开始吧，

## **Java 中的矩阵乘法**

通过使用二元运算从两个矩阵的元素中获得单个矩阵称为矩阵乘法。更简单地说，如果将 a*b 和 b*c 阶的两个矩阵 R 和 S 相乘，所获得的矩阵是 a*c 阶的。在 java 中，可以通过使用各种方法来高效地完成矩阵的乘法。下面讨论最有效的方法。

继续这篇文章

**使用 For 循环**

在这种方法中，我们使用 for 循环。

```
public class Main{
public static void main(String args[]){
//creating two matrices
int m1[][]={{1,2,3},{4,5,6},{2,3,4}};
int m2[][]={{1,2,3},{4,5,6},{2,3,4}};
int m[][]=new int[3][3]; //3 rows and 3 columns
//multiplying
for(int i=0;i<3;i++){
for(int j=0;j<3;j++){
m[i][j]=0;
for(int k=0;k<3;k++)
{
m[i][j]+=m1[i][k]*m2[k][j];
}
//end of k loop
System.out.print(m[i][j]+" "); //printing matrix
}
//end of j loop
System.out.println();
}
}}

```

**输出**

15 21 27

36 51 66

22 31 40

继续这篇关于 Java 中矩阵乘法的文章，

## **通过键盘**指定输入

```
import java.util.Scanner;
public class Main
{
public static void main(String args[])
{
int n;
Scanner input = new Scanner(System.in);
System.out.println("Enter base of matrices");
n = input.nextInt();
int[][] m1 = new int[n][n];
int[][] m2 = new int[n][n];
int[][] mat = new int[n][n];
System.out.println("Enter the elements of 1st matrix row wise : n");
for (int i = 0; i < n; i++)
{
for(int j = 0; j < n; j++)
{
m1[i][j] = input.nextInt();
}
}
System.out.println("Enter the elements of 2nd matrix row wise : n");
for (int i = 0; i < n; i++)
{
for(int j = 0; j < n; j++)
{
m2[i][j] = input.nextInt();
}
}
System.out.println("Multiplying the matrices : ");
for(int i = 0; i < n; i++)
{
for(int j = 0; j < n; j++)
{
for(int k = 0; k < n; k++)
{
mat[i][j] = mat[i][j] + m1[i][k] * m2[k][j];
}
}
}
System.out.println("Product :");
for (int i = 0; i < n; i++)
{
for(int j = 0; j < n; j++)
{
System.out.print(mat[i][j] + " ");
}
System.out.println();
}
input.close();
}
}

```

**输出**

**输入矩阵的基数:**

three

**按行输入第一个矩阵的元素:**

one

Two

three

six

five

four

seven

eight

nine

**按行输入第二矩阵的元素:**

three

Two

one

four

five

six

nine

eight

seven

**矩阵相乘:**

**产品:**

38 36 34

270 314 358

134 126 118

***这样，在 java 中使用 for 循环就可以高效地求出两个矩阵的乘积。***

这样，我们就结束了这篇关于“Java 中的矩阵乘法”的文章。如果您希望了解更多，请查看 Edureka(一家值得信赖的在线学习公司)提供的 [Java 认证课程](https://www.edureka.co/java-j2ee-training-course)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。