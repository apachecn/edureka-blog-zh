# Java 中如何把 Char 转换成 Int？

> 原文：<https://www.edureka.co/blog/java-char-to-int/>

在 [Java](https://www.edureka.co/blog/java-tutorial/) 中，一种数据类型中包含的值可以根据转换需求转换成另一种数据类型，char 到 int 的转换也是如此。将 char 转换为 int 相当于查找给定字符的 ASCII 值。在这篇关于“在 Java 中将 char 转换成 int”的文章中，我们将借助例子来学习如何将一个 Char 转换成 Int。

本文讨论的话题有:

*   [什么是数据类型？](#Datatypes)
*   [Java char 转 int:获取 ASCII 值](#Asciivalue)
*   [Java char to int 示例:character . getnumericvalue()](#Character)
*   [示例:String.valueOf()](#string)

## **什么是数据类型？**

[数据类型](https://www.edureka.co/blog/data-types-in-java/)是存储特定类型值的存储容器，如整数、字符、浮点值、布尔值等。数据类型指定了一个[变量](https://www.edureka.co/blog/variables-in-java/)具有的值的类型，以及可以应用于它而不会导致错误的关系、数学或逻辑运算的类型。

特定变量的数据类型的选择取决于多种因素。在大多数情况下，决策是直觉的。例如，

*   如果你想存储一个数值，那么就声明像 int 这样的数据类型
*   对于浮点存储，将数据类型声明为浮点
*   存储短信，声明数据类型为[字符串](https://www.edureka.co/blog/java-string/)
*   要存储单个字符，声明 char 这样的数据类型
*   为了存储二进制值，真或假，将数据类型声明为布尔型

## **Java char 到 int:获取 ASCII 值**

**文件名:【CharToIntExample.java】T2**

代码:

```
public static void main(String args[]){  
char c='Z';  
char c1='9';  
int a=c;  
int b=c1;  
System.out.println(a);  
System.out.println(b);  
}}  

```

编译者:javac CharToIntExample.java 运行者:java 图表示例

**输出**

**![Java char to int output | Edureka | Edureka Blogs](img/f8e670bb84b5c55794049faf06cb6095.png)**

## ****Java char to int 示例:character . getnumericvalue()****

**文件名:【CharToIntExample1.java】T2**

代码:

```
public class CharToIntExample1{  
public static void main(String args[]){  
char c='9';  
int a=Character.getNumericValue(c);  
System.out.println(a);  
}}

```

**编译人:**爪哇 CharToIntExample1.java运行人:爪哇图表示例 1

**输出:**

**![Java char to int output2 | Edureka | Edureka Blogs](img/4a348b0d2e1ea313614ffca15540c01a.png)**

**Java char to int 示例:String.valueOf() :**

**文件名:【CharToIntExample2.java】T2**

代码:

```
public class CharToIntExample2{  
public static void main(String args[]){  
char c='8';  
int a=Integer.parseInt(String.valueOf(c));  
System.out.println(a);  
}}  

```

**编译人:【CharToIntExample2.java 贾瓦茨**

**运行人:** java 图表示例 2

**输出:**

![Java char to int output3 | Edureka | Edureka Blogs](img/e9cef04f6e190d1cd9cbcbdfd131c672.png)

到此，我们结束这篇文章。我希望它能增加你的知识。

如果您有兴趣学习更多关于 Java 的知识，请查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在为您提供 Java 编程的良好开端，并培训您核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*