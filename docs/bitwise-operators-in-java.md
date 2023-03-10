# 关于 Java 中的按位运算符，你需要知道的一切

> 原文：<https://www.edureka.co/blog/bitwise-operators-in-java/>

按位运算符用于对一个数的各个位进行操作，这是任何编程语言的一个基本方面，因为最终一切都归结为 0 和 1。以下指针将在这篇 Java 文章中的**位操作符**中讨论:

*   [按位运算符和类型](#BitwiseOperatorsandTypes)
*   [按位运算符示例](#ExampleofBitwiseOperators)
*   [移位操作符](#ShiftOperators)
*   [移位运算符示例](#ExampleofShiftOperators)

很多时候，程序员发现需要处理数字。通过使用 java 提供的按位运算符，可以修改或操作数字的各个位。这些运算符可以与 char、short、int 或任何整数类型一起使用。它们不能应用于 double 和 float。

![BITWISE OPERATORS IN JAVA](img/9f0c5504eeb89420759e7dcc32cc3847.png)

继续这篇关于 Java 中的位操作符的文章。

## **Java 中按位运算符的类型**

*   ***&(二进制与运算符)***

二元&运算符非常类似于逻辑&运算符，唯一的区别是它们使用两位而不是两个表达式。如果两个操作数都等于 1，二元 AND 运算符返回值 1，否则返回 0。

*   ***|【二进制或运算符】***

二元 OR 运算符类似于逻辑||运算符。它处理两位而不是两个表达式，如果其中一个操作数的值为 1，则返回 1。即使两个操作数的计算结果都为 1，结果也是 1。

*   ***【^(二元异或运算符)***

XOR 代表“异或”。如果恰好有一个操作数的值为 1，则该运算符返回 1。如果两个操作数的计算结果都为 1 或 0，则结果为 0。

*   ***~(二进制补码运算符)***

输入值的补码由该运算符返回。简而言之，它将位反转，即它将 0 转换为 1，反之亦然。

继续这篇关于 Java 中的位操作符的文章。

## **Java 中按位运算符的例子**

```
public class bitwiseExample {
public static void main(String[] args) {
//Variables Definition and Initialization
int n1 = 18, n2 = 28, n3 =0;
//Bitwise AND
System.out.println("num1 & num2 = " + (n1 & n2));
//Bitwise OR
System.out.println("num1 | num2 = " + (n1 | n2) );
//Bitwise XOR
System.out.println("num1 ^ num2 = " + (n1 ^ n2) );
//Binary Complement Operator
System.out.println("~num1 = " + ~n1 );
}
}

```

**输出:**

num1 和 num2 = 16

数字 1 |数字 2 = 30

num 1≤num 2 = 14

~num1 = -19

继续这篇关于 Java 中的位操作符的文章。

## **移位操作符**

这些运算符将数字向左或向右移位，分别进行乘法和除法运算。

*   ***> >(签右移符):***

该运算符将数字向右移动。它在结果留下的空白空间中填充 0。最左边的位取决于初始数字的符号。类似于将一个数除以 2 的某个幂。

*   ***> > >(无符号右移运算符):***

该运算符将数字向右移动。它在结果留下的空白空间中填充 0。最左边的位设置为 0。

*   ***> >(左移运算符):***

该运算符将数字左移。它在结果留下的空白空间中填充 0。类似于将一个数乘以 2 的某个幂。

*   ***> >(无符号左移运算符):***

与无符号右移不同，Java 不提供任何这样的运算符。

接下来继续讨论 Ja 中的按位运算符va

班组长**E****x****am****pl****E**

```
public class bitwiseExample { 
public static void main(String[] args) 
{ 
int n1 = 8; 
int n2 = -10; 
// left shift operator 
System.out.println("n1<<2 = " + (n1 << 2)); // right shift operator System.out.println("n2>>2 = " + (n2 >> 2)); 
// unsigned right shift operator 
System.out.println("n2>>>2 = " + (n2 >>> 2)); 
} 
}

```

***输出:***

n1<<2 = 32

n2>>2 = -3

n2>>>2 = 1073741821

****

至此，我们结束了这篇关于 Java 中按位运算符的文章。本文中讨论的运算符允许用户有效地操作数字或单个数据位。C *查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在“Java 中的位操作符”博客的评论部分提到它，我们会尽快回复您。